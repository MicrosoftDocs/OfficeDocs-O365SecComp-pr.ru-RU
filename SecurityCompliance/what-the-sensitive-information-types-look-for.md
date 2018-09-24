---
title: Что позволяют искать типы конфиденциальной информации
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает в себя 80 типы конфиденциальной информации, готовые к использованию в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показывает, что политики защиты от потери данных выполняет поиск при обнаружении каждого типа.
ms.openlocfilehash: 2e59b322730ca7fa828a685ed3a80c48ebdbbfd8
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972361"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="dc720-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="dc720-104">What the sensitive information types look for</span></span>

<span data-ttu-id="dc720-p102">Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показывает, что политики защиты от потери данных выполняет поиск при обнаружении каждого типа. Тип конфиденциальных данных определяется шаблон, который можно определить по регулярных выражений или функции. Кроме того подтверждающее свидетельств, таких как ключевые слова и контрольные можно использовать для определения типов конфиденциальной информации. Уровень надежности и близость также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="dc720-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="dc720-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="dc720-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-111">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-111">Format</span></span>

<span data-ttu-id="dc720-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="dc720-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-113">Pattern</span></span>

<span data-ttu-id="dc720-114">С форматированием</span><span class="sxs-lookup"><span data-stu-id="dc720-114">Formatted:</span></span>
- <span data-ttu-id="dc720-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="dc720-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="dc720-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-116">A hyphen</span></span>
- <span data-ttu-id="dc720-117">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-117">Four digits</span></span>
- <span data-ttu-id="dc720-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-118">A hyphen</span></span>
- <span data-ttu-id="dc720-119">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dc720-119">A digit</span></span>

<span data-ttu-id="dc720-120">Неформатированный: 9 последовательных цифр Приступая к работе с 0, 1, 2, 3, 6, 7 или 8</span><span class="sxs-lookup"><span data-stu-id="dc720-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="dc720-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-121">Checksum</span></span>

<span data-ttu-id="dc720-122">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-123">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-123">Definition</span></span>

<span data-ttu-id="dc720-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="dc720-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="dc720-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="dc720-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="dc720-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="dc720-129">aba</span><span class="sxs-lookup"><span data-stu-id="dc720-129">aba</span></span>
- <span data-ttu-id="dc720-130">
aba#</span><span class="sxs-lookup"><span data-stu-id="dc720-130">aba #</span></span>
- <span data-ttu-id="dc720-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="dc720-131">aba routing #</span></span>
- <span data-ttu-id="dc720-132">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="dc720-132">aba routing number</span></span>
- <span data-ttu-id="dc720-133">
aba#</span><span class="sxs-lookup"><span data-stu-id="dc720-133">aba#</span></span>
- <span data-ttu-id="dc720-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="dc720-134">abarouting#</span></span>
- <span data-ttu-id="dc720-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="dc720-135">aba number</span></span>
- <span data-ttu-id="dc720-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="dc720-136">abaroutingnumber</span></span>
- <span data-ttu-id="dc720-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="dc720-137">american bank association routing #</span></span>
- <span data-ttu-id="dc720-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="dc720-138">american bank association routing number</span></span>
- <span data-ttu-id="dc720-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="dc720-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="dc720-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="dc720-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="dc720-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="dc720-141">bank routing number</span></span>
- <span data-ttu-id="dc720-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="dc720-142">bankrouting#</span></span>
- <span data-ttu-id="dc720-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="dc720-143">bankroutingnumber</span></span>
- <span data-ttu-id="dc720-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="dc720-144">routing transit number</span></span>
- <span data-ttu-id="dc720-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="dc720-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="dc720-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="dc720-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-147">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-147">Format</span></span>

<span data-ttu-id="dc720-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="dc720-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-149">Pattern</span></span>

<span data-ttu-id="dc720-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-150">Eight digits:</span></span>
- <span data-ttu-id="dc720-151">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-151">Two digits</span></span>
- <span data-ttu-id="dc720-152">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-152">A period</span></span>
- <span data-ttu-id="dc720-153">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-153">Three digits</span></span>
- <span data-ttu-id="dc720-154">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-154">A period</span></span>
- <span data-ttu-id="dc720-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-156">Checksum</span></span>

<span data-ttu-id="dc720-157">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-158">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-158">Definition</span></span>

<span data-ttu-id="dc720-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="dc720-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="dc720-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="dc720-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="dc720-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="dc720-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="dc720-165">Идентификация</span><span class="sxs-lookup"><span data-stu-id="dc720-165">Identity</span></span> 
- <span data-ttu-id="dc720-166">Идентификация национальной идентификационной карты</span><span class="sxs-lookup"><span data-stu-id="dc720-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="dc720-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="dc720-167">DNI</span></span> 
- <span data-ttu-id="dc720-168">Сетевой Адаптер национальный реестра лиц</span><span class="sxs-lookup"><span data-stu-id="dc720-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="dc720-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="dc720-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="dc720-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="dc720-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="dc720-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="dc720-171">Identidad</span></span> 
- <span data-ttu-id="dc720-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="dc720-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="dc720-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="dc720-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-174">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-174">Format</span></span>

<span data-ttu-id="dc720-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="dc720-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-176">Pattern</span></span>

<span data-ttu-id="dc720-p103">Номер учетной записи — 6 до 10 цифр. Номер филиала банка Австралия состояний:</span><span class="sxs-lookup"><span data-stu-id="dc720-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="dc720-179">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-179">Three digits</span></span> 
- <span data-ttu-id="dc720-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-180">A hyphen</span></span> 
- <span data-ttu-id="dc720-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-182">Checksum</span></span>

<span data-ttu-id="dc720-183">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-184">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-184">Definition</span></span>

<span data-ttu-id="dc720-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="dc720-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="dc720-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="dc720-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="dc720-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="dc720-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="dc720-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="dc720-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="dc720-194">swift bank code</span></span>
- <span data-ttu-id="dc720-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="dc720-195">correspondent bank</span></span>
- <span data-ttu-id="dc720-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="dc720-196">base currency</span></span>
- <span data-ttu-id="dc720-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="dc720-197">usa account</span></span>
- <span data-ttu-id="dc720-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="dc720-198">holder address</span></span>
- <span data-ttu-id="dc720-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="dc720-199">bank address</span></span>
- <span data-ttu-id="dc720-200">
information account</span><span class="sxs-lookup"><span data-stu-id="dc720-200">information account</span></span>
- <span data-ttu-id="dc720-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="dc720-201">fund transfers</span></span>
- <span data-ttu-id="dc720-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="dc720-202">bank charges</span></span>
- <span data-ttu-id="dc720-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="dc720-203">bank details</span></span>
- <span data-ttu-id="dc720-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="dc720-204">banking information</span></span>
- <span data-ttu-id="dc720-205">
full names</span><span class="sxs-lookup"><span data-stu-id="dc720-205">full names</span></span>
- <span data-ttu-id="dc720-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="dc720-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="dc720-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="dc720-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-208">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-208">Format</span></span>

<span data-ttu-id="dc720-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-210">Pattern</span></span>

<span data-ttu-id="dc720-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="dc720-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="dc720-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-213">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-213">Two digits</span></span> 
- <span data-ttu-id="dc720-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="dc720-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="dc720-215">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="dc720-215">OR</span></span>

- <span data-ttu-id="dc720-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="dc720-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-217">4-9 digits</span></span>

<span data-ttu-id="dc720-218">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="dc720-218">OR</span></span>

- <span data-ttu-id="dc720-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="dc720-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-220">Checksum</span></span>

<span data-ttu-id="dc720-221">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-222">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-222">Definition</span></span>

<span data-ttu-id="dc720-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="dc720-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="dc720-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="dc720-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="dc720-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="dc720-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="dc720-229">international driving permits</span></span>
- <span data-ttu-id="dc720-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="dc720-230">australian automobile association</span></span>
- <span data-ttu-id="dc720-231">
sydney nsw</span><span class="sxs-lookup"><span data-stu-id="dc720-231">sydney nsw</span></span>
- <span data-ttu-id="dc720-232">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="dc720-232">international driving permit</span></span>
- <span data-ttu-id="dc720-233">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="dc720-233">DriverLicence</span></span>
- <span data-ttu-id="dc720-234">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="dc720-234">DriverLicences</span></span>
- <span data-ttu-id="dc720-235">Драйвер Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-235">Driver Lic</span></span>
- <span data-ttu-id="dc720-236">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-236">Driver Licence</span></span>
- <span data-ttu-id="dc720-237">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-237">Driver Licences</span></span>
- <span data-ttu-id="dc720-238">DriversLic</span><span class="sxs-lookup"><span data-stu-id="dc720-238">DriversLic</span></span>
- <span data-ttu-id="dc720-239">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="dc720-239">DriversLicence</span></span>
- <span data-ttu-id="dc720-240">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="dc720-240">DriversLicences</span></span>
- <span data-ttu-id="dc720-241">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-241">Drivers Lic</span></span>
- <span data-ttu-id="dc720-242">Драйверы Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-242">Drivers Lics</span></span>
- <span data-ttu-id="dc720-243">Лицензия драйверы</span><span class="sxs-lookup"><span data-stu-id="dc720-243">Drivers Licence</span></span>
- <span data-ttu-id="dc720-244">Число лицензий на драйверы</span><span class="sxs-lookup"><span data-stu-id="dc720-244">Drivers Licences</span></span>
- <span data-ttu-id="dc720-245">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-245">Driver'Lic</span></span>
- <span data-ttu-id="dc720-246">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-246">Driver'Lics</span></span>
- <span data-ttu-id="dc720-247">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="dc720-247">Driver'Licence</span></span>
- <span data-ttu-id="dc720-248">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="dc720-248">Driver'Licences</span></span>
- <span data-ttu-id="dc720-249">Драйвер ' Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-249">Driver' Lic</span></span>
- <span data-ttu-id="dc720-250">Драйвер ' Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-250">Driver' Lics</span></span>
- <span data-ttu-id="dc720-251">Драйвер "лицензия</span><span class="sxs-lookup"><span data-stu-id="dc720-251">Driver' Licence</span></span>
- <span data-ttu-id="dc720-252">Драйвер "число лицензий на по</span><span class="sxs-lookup"><span data-stu-id="dc720-252">Driver' Licences</span></span>
- <span data-ttu-id="dc720-253">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="dc720-253">Driver'sLic</span></span>
- <span data-ttu-id="dc720-254">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="dc720-254">Driver'sLics</span></span>
- <span data-ttu-id="dc720-255">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="dc720-255">Driver'sLicence</span></span>
- <span data-ttu-id="dc720-256">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="dc720-256">Driver'sLicences</span></span>
- <span data-ttu-id="dc720-257">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-257">Driver's Lic</span></span>
- <span data-ttu-id="dc720-258">Lics драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-258">Driver's Lics</span></span>
- <span data-ttu-id="dc720-259">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-259">Driver's Licence</span></span>
- <span data-ttu-id="dc720-260">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-260">Driver's Licences</span></span>
- <span data-ttu-id="dc720-261">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-261">DriverLic#</span></span>
- <span data-ttu-id="dc720-262">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-262">DriverLics#</span></span>
- <span data-ttu-id="dc720-263">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="dc720-263">DriverLicence#</span></span>
- <span data-ttu-id="dc720-264">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="dc720-264">DriverLicences#</span></span>
- <span data-ttu-id="dc720-265">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="dc720-265">Driver Lic#</span></span>
- <span data-ttu-id="dc720-266">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-266">Driver Lics#</span></span>
- <span data-ttu-id="dc720-267">Драйвер лицензия #</span><span class="sxs-lookup"><span data-stu-id="dc720-267">Driver Licence#</span></span>
- <span data-ttu-id="dc720-268">Драйвер число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="dc720-268">Driver Licences#</span></span>
- <span data-ttu-id="dc720-269">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-269">DriversLic#</span></span>
- <span data-ttu-id="dc720-270">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-270">DriversLics#</span></span>
- <span data-ttu-id="dc720-271">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="dc720-271">DriversLicence#</span></span>
- <span data-ttu-id="dc720-272">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="dc720-272">DriversLicences#</span></span>
- <span data-ttu-id="dc720-273">Драйверы Lic #</span><span class="sxs-lookup"><span data-stu-id="dc720-273">Drivers Lic#</span></span>
- <span data-ttu-id="dc720-274">Драйверы Lics #</span><span class="sxs-lookup"><span data-stu-id="dc720-274">Drivers Lics#</span></span>
- <span data-ttu-id="dc720-275">Драйверы лицензия #</span><span class="sxs-lookup"><span data-stu-id="dc720-275">Drivers Licence#</span></span>
- <span data-ttu-id="dc720-276">Число лицензий на драйверы #</span><span class="sxs-lookup"><span data-stu-id="dc720-276">Drivers Licences#</span></span>
- <span data-ttu-id="dc720-277">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-277">Driver'Lic#</span></span>
- <span data-ttu-id="dc720-278">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-278">Driver'Lics#</span></span>
- <span data-ttu-id="dc720-279">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="dc720-279">Driver'Licence#</span></span>
- <span data-ttu-id="dc720-280">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="dc720-280">Driver'Licences#</span></span>
- <span data-ttu-id="dc720-281">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-281">Driver' Lic#</span></span>
- <span data-ttu-id="dc720-282">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-282">Driver' Lics#</span></span>
- <span data-ttu-id="dc720-283">Драйвер "лицензия #</span><span class="sxs-lookup"><span data-stu-id="dc720-283">Driver' Licence#</span></span>
- <span data-ttu-id="dc720-284">Драйвер "число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="dc720-284">Driver' Licences#</span></span>
- <span data-ttu-id="dc720-285">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-285">Driver'sLic#</span></span>
- <span data-ttu-id="dc720-286">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-286">Driver'sLics#</span></span>
- <span data-ttu-id="dc720-287">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="dc720-287">Driver'sLicence#</span></span>
- <span data-ttu-id="dc720-288">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="dc720-288">Driver'sLicences#</span></span>
- <span data-ttu-id="dc720-289">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-289">Driver's Lic#</span></span>
- <span data-ttu-id="dc720-290">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-290">Driver's Lics#</span></span>
- <span data-ttu-id="dc720-291">Лицензия водительского #</span><span class="sxs-lookup"><span data-stu-id="dc720-291">Driver's Licence#</span></span>
- <span data-ttu-id="dc720-292">Число лицензий на водительского #</span><span class="sxs-lookup"><span data-stu-id="dc720-292">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="dc720-293">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="dc720-293">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="dc720-294">aaa</span><span class="sxs-lookup"><span data-stu-id="dc720-294">aaa</span></span>
- <span data-ttu-id="dc720-295">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-295">DriverLicense</span></span>
- <span data-ttu-id="dc720-296">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-296">DriverLicenses</span></span>
- <span data-ttu-id="dc720-297">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-297">Driver License</span></span>
- <span data-ttu-id="dc720-298">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-298">Driver Licenses</span></span>
- <span data-ttu-id="dc720-299">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-299">DriversLicense</span></span>
- <span data-ttu-id="dc720-300">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-300">DriversLicenses</span></span>
- <span data-ttu-id="dc720-301">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-301">Drivers License</span></span>
- <span data-ttu-id="dc720-302">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-302">Drivers Licenses</span></span>
- <span data-ttu-id="dc720-303">Driver'License</span><span class="sxs-lookup"><span data-stu-id="dc720-303">Driver'License</span></span>
- <span data-ttu-id="dc720-304">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="dc720-304">Driver'Licenses</span></span>
- <span data-ttu-id="dc720-305">Драйвер "лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-305">Driver' License</span></span>
- <span data-ttu-id="dc720-306">Драйвер "лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-306">Driver' Licenses</span></span>
- <span data-ttu-id="dc720-307">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-307">Driver'sLicense</span></span>
- <span data-ttu-id="dc720-308">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-308">Driver'sLicenses</span></span>
- <span data-ttu-id="dc720-309">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-309">Driver's License</span></span>
- <span data-ttu-id="dc720-310">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-310">Driver's Licenses</span></span>
- <span data-ttu-id="dc720-311">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-311">DriverLicense#</span></span>
- <span data-ttu-id="dc720-312">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-312">DriverLicenses#</span></span>
- <span data-ttu-id="dc720-313">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-313">Driver License#</span></span>
- <span data-ttu-id="dc720-314">Драйвер лицензий #</span><span class="sxs-lookup"><span data-stu-id="dc720-314">Driver Licenses#</span></span>
- <span data-ttu-id="dc720-315">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-315">DriversLicense#</span></span>
- <span data-ttu-id="dc720-316">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-316">DriversLicenses#</span></span>
- <span data-ttu-id="dc720-317">Драйверы лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-317">Drivers License#</span></span>
- <span data-ttu-id="dc720-318">Драйверы лицензий #</span><span class="sxs-lookup"><span data-stu-id="dc720-318">Drivers Licenses#</span></span>
- <span data-ttu-id="dc720-319">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-319">Driver'License#</span></span>
- <span data-ttu-id="dc720-320">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-320">Driver'Licenses#</span></span>
- <span data-ttu-id="dc720-321">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-321">Driver' License#</span></span>
- <span data-ttu-id="dc720-322">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-322">Driver' Licenses#</span></span>
- <span data-ttu-id="dc720-323">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-323">Driver'sLicense#</span></span>
- <span data-ttu-id="dc720-324">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-324">Driver'sLicenses#</span></span>
- <span data-ttu-id="dc720-325">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-325">Driver's License#</span></span>
- <span data-ttu-id="dc720-326">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="dc720-326">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="dc720-327">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="dc720-327">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-328">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-328">Format</span></span>

<span data-ttu-id="dc720-329">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-329">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-330">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-330">Pattern</span></span>

<span data-ttu-id="dc720-331">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-331">10-11 digits:</span></span>
- <span data-ttu-id="dc720-332">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="dc720-332">First digit is in the range 2-6</span></span>
- <span data-ttu-id="dc720-333">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-333">Ninth digit is a check digit</span></span>
- <span data-ttu-id="dc720-334">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="dc720-334">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="dc720-335">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="dc720-335">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-336">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-336">Checksum</span></span>

<span data-ttu-id="dc720-337">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-337">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-338">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-338">Definition</span></span>

<span data-ttu-id="dc720-339">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-339">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-340">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-340">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-341">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="dc720-341">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="dc720-342">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-342">The checksum passes.</span></span>

<span data-ttu-id="dc720-343">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-343">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-344">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-344">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-345">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-345">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-346">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-346">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="dc720-347">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="dc720-347">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="dc720-348">bank account details</span><span class="sxs-lookup"><span data-stu-id="dc720-348">bank account details</span></span>
- <span data-ttu-id="dc720-349">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="dc720-349">medicare payments</span></span>
- <span data-ttu-id="dc720-350">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="dc720-350">mortgage account</span></span>
- <span data-ttu-id="dc720-351">
bank payments</span><span class="sxs-lookup"><span data-stu-id="dc720-351">bank payments</span></span>
- <span data-ttu-id="dc720-352">
information branch</span><span class="sxs-lookup"><span data-stu-id="dc720-352">information branch</span></span>
- <span data-ttu-id="dc720-353">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="dc720-353">credit card loan</span></span>
- <span data-ttu-id="dc720-354">
department of human services</span><span class="sxs-lookup"><span data-stu-id="dc720-354">department of human services</span></span>
- <span data-ttu-id="dc720-355">Локальная служба</span><span class="sxs-lookup"><span data-stu-id="dc720-355">local service</span></span>
- <span data-ttu-id="dc720-356">

medicare</span><span class="sxs-lookup"><span data-stu-id="dc720-356">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="dc720-357">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="dc720-357">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-358">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-358">Format</span></span>

<span data-ttu-id="dc720-359">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-359">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-360">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-360">Pattern</span></span>

<span data-ttu-id="dc720-361">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-361">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-362">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-362">Checksum</span></span>

<span data-ttu-id="dc720-363">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-363">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-364">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-364">Definition</span></span>

<span data-ttu-id="dc720-365">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-366">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-366">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-367">Ключевое слово из Keyword_passport или Keyword_australia_passport_number найти.</span><span class="sxs-lookup"><span data-stu-id="dc720-367">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-368">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-368">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="dc720-369">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-369">Keyword_passport</span></span>

- <span data-ttu-id="dc720-370">Passport Number</span><span class="sxs-lookup"><span data-stu-id="dc720-370">Passport Number</span></span>
- <span data-ttu-id="dc720-371">
Passport No</span><span class="sxs-lookup"><span data-stu-id="dc720-371">Passport No</span></span>
- <span data-ttu-id="dc720-372">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-372">Passport #</span></span>
- <span data-ttu-id="dc720-373">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-373">Passport#</span></span>
- <span data-ttu-id="dc720-374">PassportID</span><span class="sxs-lookup"><span data-stu-id="dc720-374">PassportID</span></span>
- <span data-ttu-id="dc720-375">Passportno
</span><span class="sxs-lookup"><span data-stu-id="dc720-375">Passportno</span></span>
- <span data-ttu-id="dc720-376">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-376">passportnumber</span></span>
- <span data-ttu-id="dc720-377">パスポート</span><span class="sxs-lookup"><span data-stu-id="dc720-377">パスポート</span></span>
- <span data-ttu-id="dc720-378">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-378">パスポート番号</span></span>
- <span data-ttu-id="dc720-379">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="dc720-379">パスポートのNum</span></span>
- <span data-ttu-id="dc720-380">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-380">パスポート ＃</span></span> 
- <span data-ttu-id="dc720-381">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="dc720-381">Numéro de passeport</span></span>
- <span data-ttu-id="dc720-382">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="dc720-382">Passeport n °</span></span>
- <span data-ttu-id="dc720-383">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="dc720-383">Passeport Non</span></span>
- <span data-ttu-id="dc720-384">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-384">Passeport #</span></span>
- <span data-ttu-id="dc720-385">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-385">Passeport#</span></span>
- <span data-ttu-id="dc720-386">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="dc720-386">PasseportNon</span></span>
- <span data-ttu-id="dc720-387">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="dc720-387">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="dc720-388">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="dc720-388">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="dc720-389">passport</span><span class="sxs-lookup"><span data-stu-id="dc720-389">passport</span></span>
- <span data-ttu-id="dc720-390">
passport details</span><span class="sxs-lookup"><span data-stu-id="dc720-390">passport details</span></span>
- <span data-ttu-id="dc720-391">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="dc720-391">immigration and citizenship</span></span>
- <span data-ttu-id="dc720-392">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="dc720-392">commonwealth of australia</span></span>
- <span data-ttu-id="dc720-393">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="dc720-393">department of immigration</span></span>
- <span data-ttu-id="dc720-394">
residential address</span><span class="sxs-lookup"><span data-stu-id="dc720-394">residential address</span></span>
- <span data-ttu-id="dc720-395">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="dc720-395">department of immigration and citizenship</span></span>
- <span data-ttu-id="dc720-396">visa
</span><span class="sxs-lookup"><span data-stu-id="dc720-396">visa</span></span>
- <span data-ttu-id="dc720-397">
national identity card</span><span class="sxs-lookup"><span data-stu-id="dc720-397">national identity card</span></span>
- <span data-ttu-id="dc720-398">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="dc720-398">passport number</span></span>
- <span data-ttu-id="dc720-399">
travel document</span><span class="sxs-lookup"><span data-stu-id="dc720-399">travel document</span></span>
- <span data-ttu-id="dc720-400">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="dc720-400">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="dc720-401">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="dc720-401">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-402">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-402">Format</span></span>

<span data-ttu-id="dc720-403">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-403">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-404">Pattern</span></span>

<span data-ttu-id="dc720-405">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="dc720-405">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="dc720-406">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-406">Three digits</span></span> 
- <span data-ttu-id="dc720-407">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="dc720-407">An optional space</span></span> 
- <span data-ttu-id="dc720-408">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-408">Three digits</span></span> 
- <span data-ttu-id="dc720-409">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="dc720-409">An optional space</span></span> 
- <span data-ttu-id="dc720-410">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="dc720-410">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-411">Checksum</span></span>

<span data-ttu-id="dc720-412">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-413">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-413">Definition</span></span>

<span data-ttu-id="dc720-414">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-415">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-415">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-416">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="dc720-416">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="dc720-417">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-417">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-418">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-418">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="dc720-419">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="dc720-419">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="dc720-420">australian business number</span><span class="sxs-lookup"><span data-stu-id="dc720-420">australian business number</span></span>
- <span data-ttu-id="dc720-421">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="dc720-421">marginal tax rate</span></span>
- <span data-ttu-id="dc720-422">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="dc720-422">medicare levy</span></span>
- <span data-ttu-id="dc720-423">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="dc720-423">portfolio number</span></span>
- <span data-ttu-id="dc720-424">
service veterans</span><span class="sxs-lookup"><span data-stu-id="dc720-424">service veterans</span></span>
- <span data-ttu-id="dc720-425">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="dc720-425">withholding tax</span></span>
- <span data-ttu-id="dc720-426">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="dc720-426">individual tax return</span></span>
- <span data-ttu-id="dc720-427">

tax file number</span><span class="sxs-lookup"><span data-stu-id="dc720-427">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="dc720-428">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="dc720-428">Keyword_number_exclusions</span></span>

- <span data-ttu-id="dc720-429">00000000</span><span class="sxs-lookup"><span data-stu-id="dc720-429">00000000</span></span>
- <span data-ttu-id="dc720-430">11111111</span><span class="sxs-lookup"><span data-stu-id="dc720-430">11111111</span></span>
- <span data-ttu-id="dc720-431">22222222</span><span class="sxs-lookup"><span data-stu-id="dc720-431">22222222</span></span>
- <span data-ttu-id="dc720-432">33333333</span><span class="sxs-lookup"><span data-stu-id="dc720-432">33333333</span></span>
- <span data-ttu-id="dc720-433">44444444</span><span class="sxs-lookup"><span data-stu-id="dc720-433">44444444</span></span>
- <span data-ttu-id="dc720-434">55555555</span><span class="sxs-lookup"><span data-stu-id="dc720-434">55555555</span></span>
- <span data-ttu-id="dc720-435">66666666</span><span class="sxs-lookup"><span data-stu-id="dc720-435">66666666</span></span>
- <span data-ttu-id="dc720-436">77777777</span><span class="sxs-lookup"><span data-stu-id="dc720-436">77777777</span></span>
- <span data-ttu-id="dc720-437">88888888</span><span class="sxs-lookup"><span data-stu-id="dc720-437">88888888</span></span>
- <span data-ttu-id="dc720-438">99999999 включительно</span><span class="sxs-lookup"><span data-stu-id="dc720-438">99999999</span></span>
- <span data-ttu-id="dc720-439">000000000</span><span class="sxs-lookup"><span data-stu-id="dc720-439">000000000</span></span>
- <span data-ttu-id="dc720-440">111111111</span><span class="sxs-lookup"><span data-stu-id="dc720-440">111111111</span></span>
- <span data-ttu-id="dc720-441">222222222</span><span class="sxs-lookup"><span data-stu-id="dc720-441">222222222</span></span>
- <span data-ttu-id="dc720-442">333333333</span><span class="sxs-lookup"><span data-stu-id="dc720-442">333333333</span></span>
- <span data-ttu-id="dc720-443">444444444</span><span class="sxs-lookup"><span data-stu-id="dc720-443">444444444</span></span>
- <span data-ttu-id="dc720-444">555555555</span><span class="sxs-lookup"><span data-stu-id="dc720-444">555555555</span></span>
- <span data-ttu-id="dc720-445">666666666</span><span class="sxs-lookup"><span data-stu-id="dc720-445">666666666</span></span>
- <span data-ttu-id="dc720-446">777777777</span><span class="sxs-lookup"><span data-stu-id="dc720-446">777777777</span></span>
- <span data-ttu-id="dc720-447">888888888</span><span class="sxs-lookup"><span data-stu-id="dc720-447">888888888</span></span>
- <span data-ttu-id="dc720-448">999999999</span><span class="sxs-lookup"><span data-stu-id="dc720-448">999999999</span></span>
- <span data-ttu-id="dc720-449">0000000000</span><span class="sxs-lookup"><span data-stu-id="dc720-449">0000000000</span></span>
- <span data-ttu-id="dc720-450">1111111111</span><span class="sxs-lookup"><span data-stu-id="dc720-450">1111111111</span></span>
- <span data-ttu-id="dc720-451">2222222222</span><span class="sxs-lookup"><span data-stu-id="dc720-451">2222222222</span></span>
- <span data-ttu-id="dc720-452">3333333333</span><span class="sxs-lookup"><span data-stu-id="dc720-452">3333333333</span></span>
- <span data-ttu-id="dc720-453">4444444444</span><span class="sxs-lookup"><span data-stu-id="dc720-453">4444444444</span></span>
- <span data-ttu-id="dc720-454">5555555555</span><span class="sxs-lookup"><span data-stu-id="dc720-454">5555555555</span></span>
- <span data-ttu-id="dc720-455">6666666666</span><span class="sxs-lookup"><span data-stu-id="dc720-455">6666666666</span></span>
- <span data-ttu-id="dc720-456">7777777777</span><span class="sxs-lookup"><span data-stu-id="dc720-456">7777777777</span></span>
- <span data-ttu-id="dc720-457">8888888888</span><span class="sxs-lookup"><span data-stu-id="dc720-457">8888888888</span></span>
- <span data-ttu-id="dc720-458">9999999999</span><span class="sxs-lookup"><span data-stu-id="dc720-458">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="dc720-459">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="dc720-459">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-460">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-460">Format</span></span>

<span data-ttu-id="dc720-461">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="dc720-461">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-462">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-462">Pattern</span></span>

<span data-ttu-id="dc720-463">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="dc720-463">11 digits plus delimiters:</span></span>
- <span data-ttu-id="dc720-464">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="dc720-464">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="dc720-465">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-465">A hyphen</span></span> 
- <span data-ttu-id="dc720-466">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="dc720-466">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="dc720-467">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-467">A period</span></span> 
- <span data-ttu-id="dc720-468">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-468">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-469">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-469">Checksum</span></span>

<span data-ttu-id="dc720-470">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-470">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-471">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-471">Definition</span></span>

<span data-ttu-id="dc720-472">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-472">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-473">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-473">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-474">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-474">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="dc720-475">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-475">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-476">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-476">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="dc720-477">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="dc720-477">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="dc720-478">Identity</span><span class="sxs-lookup"><span data-stu-id="dc720-478">Identity</span></span>
- <span data-ttu-id="dc720-479">Registration</span><span class="sxs-lookup"><span data-stu-id="dc720-479">Registration</span></span>
- <span data-ttu-id="dc720-480">Identification</span><span class="sxs-lookup"><span data-stu-id="dc720-480">Identification</span></span> 
- <span data-ttu-id="dc720-481">ID</span><span class="sxs-lookup"><span data-stu-id="dc720-481">ID</span></span> 
- <span data-ttu-id="dc720-482">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="dc720-482">Identiteitskaart</span></span>
- <span data-ttu-id="dc720-483">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="dc720-483">Registratie nummer</span></span> 
- <span data-ttu-id="dc720-484">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-484">Identificatie nummer</span></span> 
- <span data-ttu-id="dc720-485">Identiteit</span><span class="sxs-lookup"><span data-stu-id="dc720-485">Identiteit</span></span>
- <span data-ttu-id="dc720-486">Registratie</span><span class="sxs-lookup"><span data-stu-id="dc720-486">Registratie</span></span>
- <span data-ttu-id="dc720-487">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="dc720-487">Identificatie</span></span> 
- <span data-ttu-id="dc720-488">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="dc720-488">Carte d’identité</span></span> 
- <span data-ttu-id="dc720-489">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="dc720-489">numéro d'immatriculation</span></span>
- <span data-ttu-id="dc720-490">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="dc720-490">numéro d'identification</span></span>
- <span data-ttu-id="dc720-491">
identité
</span><span class="sxs-lookup"><span data-stu-id="dc720-491">identité</span></span> 
- <span data-ttu-id="dc720-492">inscription
</span><span class="sxs-lookup"><span data-stu-id="dc720-492">inscription</span></span> 
- <span data-ttu-id="dc720-493">Identifikation</span><span class="sxs-lookup"><span data-stu-id="dc720-493">Identifikation</span></span>
- <span data-ttu-id="dc720-494">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="dc720-494">Identifizierung</span></span>
- <span data-ttu-id="dc720-495">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-495">Identifikationsnummer</span></span>
- <span data-ttu-id="dc720-496">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="dc720-496">Personalausweis</span></span>
- <span data-ttu-id="dc720-497">Registrierung</span><span class="sxs-lookup"><span data-stu-id="dc720-497">Registrierung</span></span>
- <span data-ttu-id="dc720-498">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-498">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="dc720-499">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="dc720-499">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-500">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-500">Format</span></span>

<span data-ttu-id="dc720-501">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="dc720-501">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-502">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-502">Pattern</span></span>

<span data-ttu-id="dc720-503">С форматированием</span><span class="sxs-lookup"><span data-stu-id="dc720-503">Formatted:</span></span>
- <span data-ttu-id="dc720-504">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-504">Three digits</span></span> 
- <span data-ttu-id="dc720-505">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-505">A period</span></span> 
- <span data-ttu-id="dc720-506">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-506">Three digits</span></span> 
- <span data-ttu-id="dc720-507">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-507">A period</span></span> 
- <span data-ttu-id="dc720-508">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-508">Three digits</span></span> 
- <span data-ttu-id="dc720-509">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-509">A hyphen</span></span> 
- <span data-ttu-id="dc720-510">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-510">Two digits which are check digits</span></span>

<span data-ttu-id="dc720-511">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="dc720-511">Unformatted:</span></span>
- <span data-ttu-id="dc720-512">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="dc720-512">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-513">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-513">Checksum</span></span>

<span data-ttu-id="dc720-514">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-514">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-515">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-515">Definition</span></span>

<span data-ttu-id="dc720-516">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-516">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-517">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-517">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-518">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="dc720-518">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="dc720-519">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-519">The checksum passes.</span></span>

<span data-ttu-id="dc720-520">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-521">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-521">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-522">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-522">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-523">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-523">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="dc720-524">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="dc720-524">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="dc720-525">CPF</span><span class="sxs-lookup"><span data-stu-id="dc720-525">CPF</span></span>
- <span data-ttu-id="dc720-526">Identification</span><span class="sxs-lookup"><span data-stu-id="dc720-526">Identification</span></span>
- <span data-ttu-id="dc720-527">Registration</span><span class="sxs-lookup"><span data-stu-id="dc720-527">Registration</span></span>
- <span data-ttu-id="dc720-528">Revenue</span><span class="sxs-lookup"><span data-stu-id="dc720-528">Revenue</span></span>
- <span data-ttu-id="dc720-529">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="dc720-529">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="dc720-530">Imposto
</span><span class="sxs-lookup"><span data-stu-id="dc720-530">Imposto</span></span> 
- <span data-ttu-id="dc720-531">Identificação
</span><span class="sxs-lookup"><span data-stu-id="dc720-531">Identificação</span></span> 
- <span data-ttu-id="dc720-532">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="dc720-532">Inscrição</span></span> 
- <span data-ttu-id="dc720-533">Receita

</span><span class="sxs-lookup"><span data-stu-id="dc720-533">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="dc720-534">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="dc720-534">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-535">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-535">Format</span></span>

<span data-ttu-id="dc720-536">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="dc720-536">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-537">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-537">Pattern</span></span>
<span data-ttu-id="dc720-538">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="dc720-538">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="dc720-539">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-539">Two digits</span></span> 
- <span data-ttu-id="dc720-540">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-540">A period</span></span> 
- <span data-ttu-id="dc720-541">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-541">Three digits</span></span> 
- <span data-ttu-id="dc720-542">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-542">A period</span></span> 
- <span data-ttu-id="dc720-543">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="dc720-543">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="dc720-544">косая черта;</span><span class="sxs-lookup"><span data-stu-id="dc720-544">A forward slash</span></span> 
- <span data-ttu-id="dc720-545">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-545">Four-digit branch number</span></span> 
- <span data-ttu-id="dc720-546">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-546">A hyphen</span></span> 
- <span data-ttu-id="dc720-547">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-547">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-548">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-548">Checksum</span></span>

<span data-ttu-id="dc720-549">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-549">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-550">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-550">Definition</span></span>

<span data-ttu-id="dc720-551">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-551">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-552">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-552">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-553">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="dc720-553">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="dc720-554">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-554">The checksum passes.</span></span>

<span data-ttu-id="dc720-555">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-555">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-556">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-556">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-557">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-557">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-558">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-558">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="dc720-559">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="dc720-559">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="dc720-560">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="dc720-560">CNPJ</span></span> 
- <span data-ttu-id="dc720-561">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="dc720-561">CNPJ/MF</span></span> 
- <span data-ttu-id="dc720-562">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="dc720-562">CNPJ-MF</span></span> 
- <span data-ttu-id="dc720-563">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="dc720-563">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="dc720-564">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="dc720-564">Taxpayers Registry</span></span> 
- <span data-ttu-id="dc720-565">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="dc720-565">Legal entity</span></span> 
- <span data-ttu-id="dc720-566">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="dc720-566">Legal entities</span></span> 
- <span data-ttu-id="dc720-567">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="dc720-567">Registration Status</span></span> 
- <span data-ttu-id="dc720-568">Business
</span><span class="sxs-lookup"><span data-stu-id="dc720-568">Business</span></span> 
- <span data-ttu-id="dc720-569">Company</span><span class="sxs-lookup"><span data-stu-id="dc720-569">Company</span></span>
- <span data-ttu-id="dc720-570">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="dc720-570">CNPJ</span></span> 
- <span data-ttu-id="dc720-571">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="dc720-571">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="dc720-572">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="dc720-572">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="dc720-573">CGC
</span><span class="sxs-lookup"><span data-stu-id="dc720-573">CGC</span></span> 
- <span data-ttu-id="dc720-574">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="dc720-574">Pessoa jurídica</span></span> 
- <span data-ttu-id="dc720-575">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="dc720-575">Pessoas jurídicas</span></span> 
- <span data-ttu-id="dc720-576">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="dc720-576">Situação cadastral</span></span> 
- <span data-ttu-id="dc720-577">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="dc720-577">Inscrição</span></span> 
- <span data-ttu-id="dc720-578">Empresa
</span><span class="sxs-lookup"><span data-stu-id="dc720-578">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="dc720-579">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="dc720-579">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-580">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-580">Format</span></span>

<span data-ttu-id="dc720-581">Geral Registro (старый формат): девяти цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-581">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="dc720-582">Identidade де Registro (РИК) (новый формат): 11 разрядов</span><span class="sxs-lookup"><span data-stu-id="dc720-582">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-583">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-583">Pattern</span></span>

<span data-ttu-id="dc720-584">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="dc720-584">Registro Geral (old format):</span></span>
- <span data-ttu-id="dc720-585">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-585">Two digits</span></span> 
- <span data-ttu-id="dc720-586">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-586">A period</span></span> 
- <span data-ttu-id="dc720-587">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-587">Three digits</span></span> 
- <span data-ttu-id="dc720-588">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-588">A period</span></span> 
- <span data-ttu-id="dc720-589">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-589">Three digits</span></span> 
- <span data-ttu-id="dc720-590">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-590">A hyphen</span></span> 
- <span data-ttu-id="dc720-591">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-591">One digit which is a check digit</span></span>

<span data-ttu-id="dc720-592">Identidade де Registro (РИК) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="dc720-592">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="dc720-593">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-593">10 digits</span></span> 
- <span data-ttu-id="dc720-594">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-594">A hyphen</span></span> 
- <span data-ttu-id="dc720-595">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-595">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-596">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-596">Checksum</span></span>

<span data-ttu-id="dc720-597">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-597">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-598">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-598">Definition</span></span>

<span data-ttu-id="dc720-599">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-599">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-600">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-600">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-601">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="dc720-601">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="dc720-602">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-602">The checksum passes.</span></span>

<span data-ttu-id="dc720-603">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-603">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-604">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-604">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-605">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-605">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-606">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-606">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="dc720-607">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="dc720-607">Keyword_brazil_rg</span></span>

<span data-ttu-id="dc720-608">Cédula де identidade идентификационной карты национальный идентификатор для número de rregistro registro де Iidentidade registro geral (в этом ключевых слов с учетом регистра) RG РИК (в этом ключевых слов с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-608">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="dc720-609">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="dc720-609">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-610">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-610">Format</span></span>

<span data-ttu-id="dc720-611">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-611">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-612">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-612">Pattern</span></span>

<span data-ttu-id="dc720-613">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-613">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="dc720-614">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="dc720-614">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="dc720-615">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-615">Five digits</span></span> 
- <span data-ttu-id="dc720-616">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-616">A hyphen</span></span> 
- <span data-ttu-id="dc720-617">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="dc720-617">Three digits OR</span></span>
- <span data-ttu-id="dc720-618">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="dc720-618">A zero "0"</span></span> 
- <span data-ttu-id="dc720-619">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-619">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-620">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-620">Checksum</span></span>

<span data-ttu-id="dc720-621">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-621">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-622">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-622">Definition</span></span>

<span data-ttu-id="dc720-623">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-623">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-624">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-624">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-625">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-625">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="dc720-626">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-626">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="dc720-627">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-627">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-628">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-628">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-629">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-629">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-630">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-630">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="dc720-631">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="dc720-631">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="dc720-632">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="dc720-632">canada savings bonds</span></span>
- <span data-ttu-id="dc720-633">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="dc720-633">canada revenue agency</span></span>
- <span data-ttu-id="dc720-634">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="dc720-634">canadian financial institution</span></span>
- <span data-ttu-id="dc720-635">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="dc720-635">direct deposit form</span></span>
- <span data-ttu-id="dc720-636">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="dc720-636">canadian citizen</span></span>
- <span data-ttu-id="dc720-637">
legal representative</span><span class="sxs-lookup"><span data-stu-id="dc720-637">legal representative</span></span>
- <span data-ttu-id="dc720-638">
notary public</span><span class="sxs-lookup"><span data-stu-id="dc720-638">notary public</span></span>
- <span data-ttu-id="dc720-639">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="dc720-639">commissioner for oaths</span></span>
- <span data-ttu-id="dc720-640">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="dc720-640">child care benefit</span></span>
- <span data-ttu-id="dc720-641">
universal child care</span><span class="sxs-lookup"><span data-stu-id="dc720-641">universal child care</span></span>
- <span data-ttu-id="dc720-642">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="dc720-642">canada child tax benefit</span></span>
- <span data-ttu-id="dc720-643">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="dc720-643">income tax benefit</span></span>
- <span data-ttu-id="dc720-644">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="dc720-644">harmonized sales tax</span></span>
- <span data-ttu-id="dc720-645">social insurance number</span><span class="sxs-lookup"><span data-stu-id="dc720-645">social insurance number</span></span>
- <span data-ttu-id="dc720-646">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="dc720-646">income tax refund</span></span>
- <span data-ttu-id="dc720-647">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="dc720-647">child tax benefit</span></span>
- <span data-ttu-id="dc720-648">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="dc720-648">territorial payments</span></span>
- <span data-ttu-id="dc720-649">
institution number</span><span class="sxs-lookup"><span data-stu-id="dc720-649">institution number</span></span>
- <span data-ttu-id="dc720-650">
deposit request</span><span class="sxs-lookup"><span data-stu-id="dc720-650">deposit request</span></span>
- <span data-ttu-id="dc720-651">
banking information</span><span class="sxs-lookup"><span data-stu-id="dc720-651">banking information</span></span>
- <span data-ttu-id="dc720-652">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="dc720-652">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="dc720-653">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="dc720-653">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-654">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-654">Format</span></span>

<span data-ttu-id="dc720-655">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="dc720-655">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-656">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-656">Pattern</span></span>

<span data-ttu-id="dc720-657">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="dc720-657">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-658">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-658">Checksum</span></span>

<span data-ttu-id="dc720-659">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-659">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-660">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-660">Definition</span></span>

<span data-ttu-id="dc720-661">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-662">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-662">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-663">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="dc720-663">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="dc720-664">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="dc720-664">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-665">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-665">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="dc720-666">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="dc720-666">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="dc720-667">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="dc720-667">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="dc720-668">
Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="dc720-668">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="dc720-669">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="dc720-669">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="dc720-670">DL</span><span class="sxs-lookup"><span data-stu-id="dc720-670">DL</span></span>
- <span data-ttu-id="dc720-671">DLS</span><span class="sxs-lookup"><span data-stu-id="dc720-671">DLS</span></span>
- <span data-ttu-id="dc720-672">CDL</span><span class="sxs-lookup"><span data-stu-id="dc720-672">CDL</span></span>
- <span data-ttu-id="dc720-673">CDLS</span><span class="sxs-lookup"><span data-stu-id="dc720-673">CDLS</span></span>
- <span data-ttu-id="dc720-674">DriverLic</span><span class="sxs-lookup"><span data-stu-id="dc720-674">DriverLic</span></span>
- <span data-ttu-id="dc720-675">DriverLics</span><span class="sxs-lookup"><span data-stu-id="dc720-675">DriverLics</span></span>
- <span data-ttu-id="dc720-676">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-676">DriverLicense</span></span>
- <span data-ttu-id="dc720-677">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-677">DriverLicenses</span></span>
- <span data-ttu-id="dc720-678">DriverLicence</span><span class="sxs-lookup"><span data-stu-id="dc720-678">DriverLicence</span></span>
- <span data-ttu-id="dc720-679">DriverLicences</span><span class="sxs-lookup"><span data-stu-id="dc720-679">DriverLicences</span></span>
- <span data-ttu-id="dc720-680">Драйвер Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-680">Driver Lic</span></span>
- <span data-ttu-id="dc720-681">Драйвер Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-681">Driver Lics</span></span>
- <span data-ttu-id="dc720-682">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-682">Driver License</span></span>
- <span data-ttu-id="dc720-683">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-683">Driver Licenses</span></span>
- <span data-ttu-id="dc720-684">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-684">Driver Licence</span></span>
- <span data-ttu-id="dc720-685">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-685">Driver Licences</span></span>
- <span data-ttu-id="dc720-686">DriversLic</span><span class="sxs-lookup"><span data-stu-id="dc720-686">DriversLic</span></span>
- <span data-ttu-id="dc720-687">DriversLics</span><span class="sxs-lookup"><span data-stu-id="dc720-687">DriversLics</span></span>
- <span data-ttu-id="dc720-688">DriversLicence</span><span class="sxs-lookup"><span data-stu-id="dc720-688">DriversLicence</span></span>
- <span data-ttu-id="dc720-689">DriversLicences</span><span class="sxs-lookup"><span data-stu-id="dc720-689">DriversLicences</span></span>
- <span data-ttu-id="dc720-690">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-690">DriversLicense</span></span>
- <span data-ttu-id="dc720-691">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-691">DriversLicenses</span></span>
- <span data-ttu-id="dc720-692">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-692">Drivers Lic</span></span>
- <span data-ttu-id="dc720-693">Драйверы Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-693">Drivers Lics</span></span>
- <span data-ttu-id="dc720-694">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-694">Drivers License</span></span>
- <span data-ttu-id="dc720-695">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-695">Drivers Licenses</span></span>
- <span data-ttu-id="dc720-696">Лицензия драйверы</span><span class="sxs-lookup"><span data-stu-id="dc720-696">Drivers Licence</span></span>
- <span data-ttu-id="dc720-697">Число лицензий на драйверы</span><span class="sxs-lookup"><span data-stu-id="dc720-697">Drivers Licences</span></span>
- <span data-ttu-id="dc720-698">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-698">Driver'Lic</span></span>
- <span data-ttu-id="dc720-699">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-699">Driver'Lics</span></span>
- <span data-ttu-id="dc720-700">Driver'License</span><span class="sxs-lookup"><span data-stu-id="dc720-700">Driver'License</span></span>
- <span data-ttu-id="dc720-701">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="dc720-701">Driver'Licenses</span></span>
- <span data-ttu-id="dc720-702">Driver'Licence</span><span class="sxs-lookup"><span data-stu-id="dc720-702">Driver'Licence</span></span>
- <span data-ttu-id="dc720-703">Driver'Licences</span><span class="sxs-lookup"><span data-stu-id="dc720-703">Driver'Licences</span></span>
- <span data-ttu-id="dc720-704">Драйвер ' Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-704">Driver' Lic</span></span>
- <span data-ttu-id="dc720-705">Драйвер ' Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-705">Driver' Lics</span></span>
- <span data-ttu-id="dc720-706">Драйвер "лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-706">Driver' License</span></span>
- <span data-ttu-id="dc720-707">Драйвер "лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-707">Driver' Licenses</span></span>
- <span data-ttu-id="dc720-708">Драйвер "лицензия</span><span class="sxs-lookup"><span data-stu-id="dc720-708">Driver' Licence</span></span>
- <span data-ttu-id="dc720-709">Драйвер "число лицензий на по</span><span class="sxs-lookup"><span data-stu-id="dc720-709">Driver' Licences</span></span>
- <span data-ttu-id="dc720-710">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="dc720-710">Driver'sLic</span></span>
- <span data-ttu-id="dc720-711">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="dc720-711">Driver'sLics</span></span>
- <span data-ttu-id="dc720-712">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-712">Driver'sLicense</span></span>
- <span data-ttu-id="dc720-713">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-713">Driver'sLicenses</span></span>
- <span data-ttu-id="dc720-714">Driver'sLicence</span><span class="sxs-lookup"><span data-stu-id="dc720-714">Driver'sLicence</span></span>
- <span data-ttu-id="dc720-715">Driver'sLicences</span><span class="sxs-lookup"><span data-stu-id="dc720-715">Driver'sLicences</span></span>
- <span data-ttu-id="dc720-716">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-716">Driver's Lic</span></span>
- <span data-ttu-id="dc720-717">Lics драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-717">Driver's Lics</span></span>
- <span data-ttu-id="dc720-718">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-718">Driver's License</span></span>
- <span data-ttu-id="dc720-719">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-719">Driver's Licenses</span></span>
- <span data-ttu-id="dc720-720">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-720">Driver's Licence</span></span>
- <span data-ttu-id="dc720-721">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-721">Driver's Licences</span></span>
- <span data-ttu-id="dc720-722">Conduire де Permis</span><span class="sxs-lookup"><span data-stu-id="dc720-722">Permis de Conduire</span></span>
- <span data-ttu-id="dc720-723">id</span><span class="sxs-lookup"><span data-stu-id="dc720-723">id</span></span>
- <span data-ttu-id="dc720-724">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="dc720-724">ids</span></span>
- <span data-ttu-id="dc720-725">
idcard number</span><span class="sxs-lookup"><span data-stu-id="dc720-725">idcard number</span></span>
- <span data-ttu-id="dc720-726">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="dc720-726">idcard numbers</span></span>
- <span data-ttu-id="dc720-727">
idcard#</span><span class="sxs-lookup"><span data-stu-id="dc720-727">idcard #</span></span>
- <span data-ttu-id="dc720-728">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="dc720-728">idcard #s</span></span>
- <span data-ttu-id="dc720-729">idcard карты</span><span class="sxs-lookup"><span data-stu-id="dc720-729">idcard card</span></span>
- <span data-ttu-id="dc720-730">idcard карты</span><span class="sxs-lookup"><span data-stu-id="dc720-730">idcard cards</span></span>
- <span data-ttu-id="dc720-731">idcard</span><span class="sxs-lookup"><span data-stu-id="dc720-731">idcard</span></span>
- <span data-ttu-id="dc720-732">identification number
</span><span class="sxs-lookup"><span data-stu-id="dc720-732">identification number</span></span>
- <span data-ttu-id="dc720-733">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-733">identification numbers</span></span>
- <span data-ttu-id="dc720-734">identification #
</span><span class="sxs-lookup"><span data-stu-id="dc720-734">identification #</span></span>
- <span data-ttu-id="dc720-735">
identification #s</span><span class="sxs-lookup"><span data-stu-id="dc720-735">identification #s</span></span>
- <span data-ttu-id="dc720-736">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="dc720-736">identification card</span></span>
- <span data-ttu-id="dc720-737">Идентификация карты</span><span class="sxs-lookup"><span data-stu-id="dc720-737">identification cards</span></span>
- <span data-ttu-id="dc720-738">
identification
</span><span class="sxs-lookup"><span data-stu-id="dc720-738">identification</span></span> 
- <span data-ttu-id="dc720-739">DL#</span><span class="sxs-lookup"><span data-stu-id="dc720-739">DL#</span></span>
- <span data-ttu-id="dc720-740">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="dc720-740">DLS#</span></span> 
- <span data-ttu-id="dc720-741">CDL#
</span><span class="sxs-lookup"><span data-stu-id="dc720-741">CDL#</span></span> 
- <span data-ttu-id="dc720-742">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="dc720-742">CDLS#</span></span> 
- <span data-ttu-id="dc720-743">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-743">DriverLic#</span></span> 
- <span data-ttu-id="dc720-744">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-744">DriverLics#</span></span> 
- <span data-ttu-id="dc720-745">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-745">DriverLicense#</span></span> 
- <span data-ttu-id="dc720-746">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-746">DriverLicenses#</span></span> 
- <span data-ttu-id="dc720-747">DriverLicence #</span><span class="sxs-lookup"><span data-stu-id="dc720-747">DriverLicence#</span></span> 
- <span data-ttu-id="dc720-748">DriverLicences #</span><span class="sxs-lookup"><span data-stu-id="dc720-748">DriverLicences#</span></span> 
- <span data-ttu-id="dc720-749">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="dc720-749">Driver Lic#</span></span>
- <span data-ttu-id="dc720-750">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-750">Driver Lics#</span></span> 
- <span data-ttu-id="dc720-751">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-751">Driver License#</span></span> 
- <span data-ttu-id="dc720-752">Драйвер лицензий #</span><span class="sxs-lookup"><span data-stu-id="dc720-752">Driver Licenses#</span></span> 
- <span data-ttu-id="dc720-753">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-753">Driver License#</span></span> 
- <span data-ttu-id="dc720-754">Драйвер число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="dc720-754">Driver Licences#</span></span> 
- <span data-ttu-id="dc720-755">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-755">DriversLic#</span></span> 
- <span data-ttu-id="dc720-756">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-756">DriversLics#</span></span> 
- <span data-ttu-id="dc720-757">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-757">DriversLicense#</span></span> 
- <span data-ttu-id="dc720-758">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-758">DriversLicenses#</span></span> 
- <span data-ttu-id="dc720-759">DriversLicence #</span><span class="sxs-lookup"><span data-stu-id="dc720-759">DriversLicence#</span></span> 
- <span data-ttu-id="dc720-760">DriversLicences #</span><span class="sxs-lookup"><span data-stu-id="dc720-760">DriversLicences#</span></span> 
- <span data-ttu-id="dc720-761">Драйверы Lic #</span><span class="sxs-lookup"><span data-stu-id="dc720-761">Drivers Lic#</span></span> 
- <span data-ttu-id="dc720-762">Драйверы Lics #</span><span class="sxs-lookup"><span data-stu-id="dc720-762">Drivers Lics#</span></span> 
- <span data-ttu-id="dc720-763">Драйверы лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-763">Drivers License#</span></span> 
- <span data-ttu-id="dc720-764">Драйверы лицензий #</span><span class="sxs-lookup"><span data-stu-id="dc720-764">Drivers Licenses#</span></span> 
- <span data-ttu-id="dc720-765">Драйверы лицензия #</span><span class="sxs-lookup"><span data-stu-id="dc720-765">Drivers Licence#</span></span> 
- <span data-ttu-id="dc720-766">Число лицензий на драйверы #</span><span class="sxs-lookup"><span data-stu-id="dc720-766">Drivers Licences#</span></span> 
- <span data-ttu-id="dc720-767">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-767">Driver'Lic#</span></span> 
- <span data-ttu-id="dc720-768">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-768">Driver'Lics#</span></span> 
- <span data-ttu-id="dc720-769">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-769">Driver'License#</span></span> 
- <span data-ttu-id="dc720-770">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-770">Driver'Licenses#</span></span> 
- <span data-ttu-id="dc720-771">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="dc720-771">Driver'Licence#</span></span> 
- <span data-ttu-id="dc720-772">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="dc720-772">Driver'Licences#</span></span> 
- <span data-ttu-id="dc720-773">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-773">Driver' Lic#</span></span> 
- <span data-ttu-id="dc720-774">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-774">Driver' Lics#</span></span> 
- <span data-ttu-id="dc720-775">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-775">Driver' License#</span></span> 
- <span data-ttu-id="dc720-776">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-776">Driver' Licenses#</span></span> 
- <span data-ttu-id="dc720-777">Драйвер "лицензия #</span><span class="sxs-lookup"><span data-stu-id="dc720-777">Driver' Licence#</span></span> 
- <span data-ttu-id="dc720-778">Драйвер "число лицензий на #</span><span class="sxs-lookup"><span data-stu-id="dc720-778">Driver' Licences#</span></span> 
- <span data-ttu-id="dc720-779">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-779">Driver'sLic#</span></span> 
- <span data-ttu-id="dc720-780">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-780">Driver'sLics#</span></span> 
- <span data-ttu-id="dc720-781">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-781">Driver'sLicense#</span></span> 
- <span data-ttu-id="dc720-782">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-782">Driver'sLicenses#</span></span> 
- <span data-ttu-id="dc720-783">Driver'sLicence #</span><span class="sxs-lookup"><span data-stu-id="dc720-783">Driver'sLicence#</span></span> 
- <span data-ttu-id="dc720-784">Driver'sLicences #</span><span class="sxs-lookup"><span data-stu-id="dc720-784">Driver'sLicences#</span></span> 
- <span data-ttu-id="dc720-785">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-785">Driver's Lic#</span></span> 
- <span data-ttu-id="dc720-786">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-786">Driver's Lics#</span></span> 
- <span data-ttu-id="dc720-787">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-787">Driver's License#</span></span> 
- <span data-ttu-id="dc720-788">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-788">Driver's Licenses#</span></span> 
- <span data-ttu-id="dc720-789">Лицензия водительского #</span><span class="sxs-lookup"><span data-stu-id="dc720-789">Driver's Licence#</span></span> 
- <span data-ttu-id="dc720-790">Число лицензий на водительского #</span><span class="sxs-lookup"><span data-stu-id="dc720-790">Driver's Licences#</span></span> 
- <span data-ttu-id="dc720-791">Permis de Conduire #</span><span class="sxs-lookup"><span data-stu-id="dc720-791">Permis de Conduire#</span></span> 
- <span data-ttu-id="dc720-792">Идентификатор #</span><span class="sxs-lookup"><span data-stu-id="dc720-792">id#</span></span> 
- <span data-ttu-id="dc720-793">идентификаторы #</span><span class="sxs-lookup"><span data-stu-id="dc720-793">ids#</span></span> 
- <span data-ttu-id="dc720-794">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="dc720-794">idcard card#</span></span> 
- <span data-ttu-id="dc720-795">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="dc720-795">idcard cards#</span></span> 
- <span data-ttu-id="dc720-796">idcard#
</span><span class="sxs-lookup"><span data-stu-id="dc720-796">idcard#</span></span> 
- <span data-ttu-id="dc720-797">identification card#
</span><span class="sxs-lookup"><span data-stu-id="dc720-797">identification card#</span></span> 
- <span data-ttu-id="dc720-798">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="dc720-798">identification cards#</span></span> 
- <span data-ttu-id="dc720-799">identification #
</span><span class="sxs-lookup"><span data-stu-id="dc720-799">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="dc720-800">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="dc720-800">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-801">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-801">Format</span></span>

<span data-ttu-id="dc720-802">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-802">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-803">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-803">Pattern</span></span>

<span data-ttu-id="dc720-804">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-804">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-805">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-805">Checksum</span></span>

<span data-ttu-id="dc720-806">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-806">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-807">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-807">Definition</span></span>

<span data-ttu-id="dc720-808">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-808">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-809">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-809">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-810">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-810">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-811">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-811">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="dc720-812">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="dc720-812">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="dc720-813">personal health number</span><span class="sxs-lookup"><span data-stu-id="dc720-813">personal health number</span></span>
- <span data-ttu-id="dc720-814">
patient information</span><span class="sxs-lookup"><span data-stu-id="dc720-814">patient information</span></span>
- <span data-ttu-id="dc720-815">работоспособность службы</span><span class="sxs-lookup"><span data-stu-id="dc720-815">health services</span></span>
- <span data-ttu-id="dc720-816">
speciality services</span><span class="sxs-lookup"><span data-stu-id="dc720-816">speciality services</span></span>
- <span data-ttu-id="dc720-817">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="dc720-817">automobile accident</span></span>
- <span data-ttu-id="dc720-818">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="dc720-818">patient hospital</span></span>
- <span data-ttu-id="dc720-819">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="dc720-819">psychiatrist</span></span>
- <span data-ttu-id="dc720-820">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="dc720-820">workers compensation</span></span>
- <span data-ttu-id="dc720-821">
disability</span><span class="sxs-lookup"><span data-stu-id="dc720-821">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="dc720-822">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="dc720-822">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-823">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-823">Format</span></span>

<span data-ttu-id="dc720-824">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-824">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-825">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-825">Pattern</span></span>

<span data-ttu-id="dc720-826">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-826">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-827">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-827">Checksum</span></span>

<span data-ttu-id="dc720-828">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-828">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-829">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-829">Definition</span></span>

<span data-ttu-id="dc720-830">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-830">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-831">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-831">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-832">Ключевое слово из Keyword_canada_passport_number или Keyword_passport найти.</span><span class="sxs-lookup"><span data-stu-id="dc720-832">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-833">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-833">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="dc720-834">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="dc720-834">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="dc720-835">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="dc720-835">canadian citizenship</span></span>
- <span data-ttu-id="dc720-836">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="dc720-836">canadian passport</span></span>
- <span data-ttu-id="dc720-837">
passport application</span><span class="sxs-lookup"><span data-stu-id="dc720-837">passport application</span></span>
- <span data-ttu-id="dc720-838">
passport photos</span><span class="sxs-lookup"><span data-stu-id="dc720-838">passport photos</span></span>
- <span data-ttu-id="dc720-839">
certified translator</span><span class="sxs-lookup"><span data-stu-id="dc720-839">certified translator</span></span>
- <span data-ttu-id="dc720-840">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="dc720-840">canadian citizens</span></span>
- <span data-ttu-id="dc720-841">
processing times</span><span class="sxs-lookup"><span data-stu-id="dc720-841">processing times</span></span>
- <span data-ttu-id="dc720-842">

renewal application</span><span class="sxs-lookup"><span data-stu-id="dc720-842">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="dc720-843">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-843">Keyword_passport</span></span>

- <span data-ttu-id="dc720-844">Passport Number</span><span class="sxs-lookup"><span data-stu-id="dc720-844">Passport Number</span></span>
- <span data-ttu-id="dc720-845">
Passport No</span><span class="sxs-lookup"><span data-stu-id="dc720-845">Passport No</span></span>
- <span data-ttu-id="dc720-846">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-846">Passport #</span></span>
- <span data-ttu-id="dc720-847">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-847">Passport#</span></span>
- <span data-ttu-id="dc720-848">PassportID</span><span class="sxs-lookup"><span data-stu-id="dc720-848">PassportID</span></span>
- <span data-ttu-id="dc720-849">Passportno
</span><span class="sxs-lookup"><span data-stu-id="dc720-849">Passportno</span></span>
- <span data-ttu-id="dc720-850">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-850">passportnumber</span></span>
- <span data-ttu-id="dc720-851">パスポート</span><span class="sxs-lookup"><span data-stu-id="dc720-851">パスポート</span></span>
- <span data-ttu-id="dc720-852">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-852">パスポート番号</span></span>
- <span data-ttu-id="dc720-853">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="dc720-853">パスポートのNum</span></span>
- <span data-ttu-id="dc720-854">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-854">パスポート＃</span></span>
- <span data-ttu-id="dc720-855">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="dc720-855">Numéro de passeport</span></span>
- <span data-ttu-id="dc720-856">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="dc720-856">Passeport n °</span></span>
- <span data-ttu-id="dc720-857">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="dc720-857">Passeport Non</span></span>
- <span data-ttu-id="dc720-858">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-858">Passeport #</span></span>
- <span data-ttu-id="dc720-859">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-859">Passeport#</span></span>
- <span data-ttu-id="dc720-860">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="dc720-860">PasseportNon</span></span>
- <span data-ttu-id="dc720-861">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="dc720-861">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="dc720-862">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="dc720-862">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-863">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-863">Format</span></span>

<span data-ttu-id="dc720-864">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-864">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-865">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-865">Pattern</span></span>

<span data-ttu-id="dc720-866">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-866">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-867">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-867">Checksum</span></span>

<span data-ttu-id="dc720-868">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-868">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-869">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-869">Definition</span></span>

<span data-ttu-id="dc720-p104">Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: регулярное выражение Regex_canada_phin находит контент, который соответствует шаблону. По крайней мере два ключевых слов из Keyword_canada_phin или Keyword_canada_provinces находятся...</span><span class="sxs-lookup"><span data-stu-id="dc720-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-872">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-872">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="dc720-873">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="dc720-873">Keyword_canada_phin</span></span>

- <span data-ttu-id="dc720-874">social insurance number</span><span class="sxs-lookup"><span data-stu-id="dc720-874">social insurance number</span></span>
- <span data-ttu-id="dc720-875">
health information act</span><span class="sxs-lookup"><span data-stu-id="dc720-875">health information act</span></span>
- <span data-ttu-id="dc720-876">
income tax information</span><span class="sxs-lookup"><span data-stu-id="dc720-876">income tax information</span></span>
- <span data-ttu-id="dc720-877">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="dc720-877">manitoba health</span></span>
- <span data-ttu-id="dc720-878">
health registration</span><span class="sxs-lookup"><span data-stu-id="dc720-878">health registration</span></span>
- <span data-ttu-id="dc720-879">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="dc720-879">prescription purchases</span></span>
- <span data-ttu-id="dc720-880">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="dc720-880">benefit eligibility</span></span>
- <span data-ttu-id="dc720-881">
personal health</span><span class="sxs-lookup"><span data-stu-id="dc720-881">personal health</span></span>
- <span data-ttu-id="dc720-882">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="dc720-882">power of attorney</span></span>
- <span data-ttu-id="dc720-883">
registration number</span><span class="sxs-lookup"><span data-stu-id="dc720-883">registration number</span></span>
- <span data-ttu-id="dc720-884">personal health number</span><span class="sxs-lookup"><span data-stu-id="dc720-884">personal health number</span></span>
- <span data-ttu-id="dc720-885">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="dc720-885">practitioner referral</span></span>
- <span data-ttu-id="dc720-886">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="dc720-886">wellness professional</span></span>
- <span data-ttu-id="dc720-887">
patient referral</span><span class="sxs-lookup"><span data-stu-id="dc720-887">patient referral</span></span>
- <span data-ttu-id="dc720-888">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="dc720-888">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="dc720-889">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="dc720-889">Keyword_canada_provinces</span></span>

- <span data-ttu-id="dc720-890">Nunavut</span><span class="sxs-lookup"><span data-stu-id="dc720-890">Nunavut</span></span>
- <span data-ttu-id="dc720-891">
Quebec</span><span class="sxs-lookup"><span data-stu-id="dc720-891">Quebec</span></span>
- <span data-ttu-id="dc720-892">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="dc720-892">Northwest Territories</span></span>
- <span data-ttu-id="dc720-893">
Ontario</span><span class="sxs-lookup"><span data-stu-id="dc720-893">Ontario</span></span>
- <span data-ttu-id="dc720-894">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="dc720-894">British Columbia</span></span>
- <span data-ttu-id="dc720-895">
Alberta</span><span class="sxs-lookup"><span data-stu-id="dc720-895">Alberta</span></span>
- <span data-ttu-id="dc720-896">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="dc720-896">Saskatchewan</span></span>
- <span data-ttu-id="dc720-897">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="dc720-897">Manitoba</span></span>
- <span data-ttu-id="dc720-898">
Yukon</span><span class="sxs-lookup"><span data-stu-id="dc720-898">Yukon</span></span>
- <span data-ttu-id="dc720-899">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="dc720-899">Newfoundland and Labrador</span></span>
- <span data-ttu-id="dc720-900">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="dc720-900">New Brunswick</span></span>
- <span data-ttu-id="dc720-901">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="dc720-901">Nova Scotia</span></span>
- <span data-ttu-id="dc720-902">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="dc720-902">Prince Edward Island</span></span>
- <span data-ttu-id="dc720-903">Канада</span><span class="sxs-lookup"><span data-stu-id="dc720-903">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="dc720-904">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="dc720-904">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-905">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-905">Format</span></span>

<span data-ttu-id="dc720-906">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="dc720-906">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-907">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-907">Pattern</span></span>

<span data-ttu-id="dc720-908">С форматированием</span><span class="sxs-lookup"><span data-stu-id="dc720-908">Formatted:</span></span>
- <span data-ttu-id="dc720-909">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-909">Three digits</span></span> 
- <span data-ttu-id="dc720-910">дефис или пробел; </span><span class="sxs-lookup"><span data-stu-id="dc720-910">A hyphen or space</span></span> 
- <span data-ttu-id="dc720-911">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-911">Three digits</span></span> 
- <span data-ttu-id="dc720-912">дефис или пробел; </span><span class="sxs-lookup"><span data-stu-id="dc720-912">A hyphen or space</span></span> 
- <span data-ttu-id="dc720-913">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-913">Three digits</span></span>

<span data-ttu-id="dc720-914">Неформатированный: Девяти цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-914">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-915">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-915">Checksum</span></span>

<span data-ttu-id="dc720-916">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-916">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-917">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-917">Definition</span></span>

<span data-ttu-id="dc720-918">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-918">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-919">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-919">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-920">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="dc720-920">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="dc720-921">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="dc720-921">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="dc720-922">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="dc720-922">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="dc720-923">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-923">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="dc720-924">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-924">The checksum passes.</span></span>

<span data-ttu-id="dc720-925">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-925">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-926">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-926">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-927">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="dc720-927">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="dc720-928">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-928">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-929">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-929">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="dc720-930">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="dc720-930">Keyword_sin</span></span>

- <span data-ttu-id="dc720-931">sin</span><span class="sxs-lookup"><span data-stu-id="dc720-931">sin</span></span> 
- <span data-ttu-id="dc720-932">social insurance
</span><span class="sxs-lookup"><span data-stu-id="dc720-932">social insurance</span></span> 
- <span data-ttu-id="dc720-933">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="dc720-933">numero d'assurance sociale</span></span> 
- <span data-ttu-id="dc720-934">sins
</span><span class="sxs-lookup"><span data-stu-id="dc720-934">sins</span></span> 
- <span data-ttu-id="dc720-935">SSN</span><span class="sxs-lookup"><span data-stu-id="dc720-935">ssn</span></span> 
- <span data-ttu-id="dc720-936">ssNS</span><span class="sxs-lookup"><span data-stu-id="dc720-936">ssns</span></span> 
- <span data-ttu-id="dc720-937">социального страхования</span><span class="sxs-lookup"><span data-stu-id="dc720-937">social security</span></span> 
- <span data-ttu-id="dc720-938">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="dc720-938">numero d'assurance social</span></span> 
- <span data-ttu-id="dc720-939">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="dc720-939">national identification number</span></span> 
- <span data-ttu-id="dc720-940">
national id</span><span class="sxs-lookup"><span data-stu-id="dc720-940">national id</span></span> 
- <span data-ttu-id="dc720-941">sin#
</span><span class="sxs-lookup"><span data-stu-id="dc720-941">sin#</span></span> 
- <span data-ttu-id="dc720-942">soc ins
</span><span class="sxs-lookup"><span data-stu-id="dc720-942">soc ins</span></span> 
- <span data-ttu-id="dc720-943">social ins
</span><span class="sxs-lookup"><span data-stu-id="dc720-943">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="dc720-944">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="dc720-944">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="dc720-945">driver's license</span><span class="sxs-lookup"><span data-stu-id="dc720-945">driver's license</span></span> 
- <span data-ttu-id="dc720-946">drivers license</span><span class="sxs-lookup"><span data-stu-id="dc720-946">drivers license</span></span> 
- <span data-ttu-id="dc720-947">Лицензия водительского удостоверения</span><span class="sxs-lookup"><span data-stu-id="dc720-947">driver's licence</span></span> 
- <span data-ttu-id="dc720-948">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dc720-948">drivers licence</span></span> 
- <span data-ttu-id="dc720-949">DOB
</span><span class="sxs-lookup"><span data-stu-id="dc720-949">DOB</span></span> 
- <span data-ttu-id="dc720-950">Birthdate</span><span class="sxs-lookup"><span data-stu-id="dc720-950">Birthdate</span></span> 
- <span data-ttu-id="dc720-951">День рождения </span><span class="sxs-lookup"><span data-stu-id="dc720-951">Birthday</span></span> 
- <span data-ttu-id="dc720-952">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="dc720-952">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="dc720-953">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="dc720-953">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-954">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-954">Format</span></span>

<span data-ttu-id="dc720-955">7-8 цифр, а также разделители контрольный разряд или буква</span><span class="sxs-lookup"><span data-stu-id="dc720-955">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-956">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-956">Pattern</span></span>

<span data-ttu-id="dc720-957">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="dc720-957">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="dc720-958">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="dc720-958">1-2 digits</span></span> 
- <span data-ttu-id="dc720-959">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-959">A period</span></span> 
- <span data-ttu-id="dc720-960">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-960">Three digits</span></span> 
- <span data-ttu-id="dc720-961">точка;</span><span class="sxs-lookup"><span data-stu-id="dc720-961">A period</span></span> 
- <span data-ttu-id="dc720-962">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-962">Three digits</span></span> 
- <span data-ttu-id="dc720-963">Тире</span><span class="sxs-lookup"><span data-stu-id="dc720-963">A dash</span></span> 
- <span data-ttu-id="dc720-964">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-964">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-965">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-965">Checksum</span></span>

<span data-ttu-id="dc720-966">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-967">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-967">Definition</span></span>

<span data-ttu-id="dc720-968">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-969">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-969">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-970">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="dc720-970">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="dc720-971">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-971">The checksum passes.</span></span>

<span data-ttu-id="dc720-972">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-972">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-973">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-973">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-974">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-974">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-975">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-975">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="dc720-976">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-976">Keyword_chile_id_card</span></span>

- <span data-ttu-id="dc720-977">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-977">National Identification Number</span></span> 
- <span data-ttu-id="dc720-978">Identity card</span><span class="sxs-lookup"><span data-stu-id="dc720-978">Identity card</span></span> 
- <span data-ttu-id="dc720-979">ID</span><span class="sxs-lookup"><span data-stu-id="dc720-979">ID</span></span> 
- <span data-ttu-id="dc720-980">Identification</span><span class="sxs-lookup"><span data-stu-id="dc720-980">Identification</span></span> 
- <span data-ttu-id="dc720-981">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="dc720-981">Rol Único Nacional</span></span> 
- <span data-ttu-id="dc720-982">ЗАПУСК</span><span class="sxs-lookup"><span data-stu-id="dc720-982">RUN</span></span> 
- <span data-ttu-id="dc720-983">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="dc720-983">Rol Único Tributario</span></span> 
- <span data-ttu-id="dc720-984">RUT
</span><span class="sxs-lookup"><span data-stu-id="dc720-984">RUT</span></span> 
- <span data-ttu-id="dc720-985">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="dc720-985">Cédula de Identidad</span></span> 
- <span data-ttu-id="dc720-986">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="dc720-986">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="dc720-987">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="dc720-987">Tarjeta de identificación</span></span> 
- <span data-ttu-id="dc720-988">Identificación
</span><span class="sxs-lookup"><span data-stu-id="dc720-988">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="dc720-989">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="dc720-989">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-990">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-990">Format</span></span>

<span data-ttu-id="dc720-991">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-991">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-992">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-992">Pattern</span></span>

<span data-ttu-id="dc720-993">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-993">18 digits:</span></span>
- <span data-ttu-id="dc720-994">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="dc720-994">Six digits which are an address code</span></span> 
- <span data-ttu-id="dc720-995">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="dc720-995">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="dc720-996">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="dc720-996">Three digits which are an order code</span></span> 
- <span data-ttu-id="dc720-997">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-997">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-998">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-998">Checksum</span></span>

<span data-ttu-id="dc720-999">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-999">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1000">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1000">Definition</span></span>

<span data-ttu-id="dc720-1001">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1001">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1002">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1002">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1003">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="dc720-1003">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="dc720-1004">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1004">The checksum passes.</span></span>

<span data-ttu-id="dc720-1005">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1005">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1006">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1006">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1007">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1007">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1008">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1008">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="dc720-1009">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="dc720-1009">Keyword_china_resident_id</span></span>

- <span data-ttu-id="dc720-1010">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1010">Resident Identity Card</span></span> 
- <span data-ttu-id="dc720-1011">PRC
</span><span class="sxs-lookup"><span data-stu-id="dc720-1011">PRC</span></span> 
- <span data-ttu-id="dc720-1012">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1012">National Identification Card</span></span> 
- <span data-ttu-id="dc720-1013">身份证 </span><span class="sxs-lookup"><span data-stu-id="dc720-1013">身份证</span></span> 
- <span data-ttu-id="dc720-1014">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="dc720-1014">居民 身份证</span></span> 
- <span data-ttu-id="dc720-1015">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="dc720-1015">居民身份证</span></span> 
- <span data-ttu-id="dc720-1016">鉴定

</span><span class="sxs-lookup"><span data-stu-id="dc720-1016">鉴定</span></span> 
- <span data-ttu-id="dc720-1017">身分證 </span><span class="sxs-lookup"><span data-stu-id="dc720-1017">身分證</span></span> 
- <span data-ttu-id="dc720-1018">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="dc720-1018">居民 身份證</span></span>
- <span data-ttu-id="dc720-1019">鑑定 </span><span class="sxs-lookup"><span data-stu-id="dc720-1019">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="dc720-1020">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="dc720-1020">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1021">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1021">Format</span></span>

<span data-ttu-id="dc720-1022">16 цифр, которые могут иметь формат или неформатированные (dddddddddddddddd) и должно пройти проверку Luhn.</span><span class="sxs-lookup"><span data-stu-id="dc720-1022">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1023">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1023">Pattern</span></span>

<span data-ttu-id="dc720-1024">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="dc720-1024">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1025">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1025">Checksum</span></span>

<span data-ttu-id="dc720-1026">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="dc720-1026">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1027">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1027">Definition</span></span>

<span data-ttu-id="dc720-1028">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1028">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1029">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1029">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1030">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-1030">One of the following is true:</span></span>
    - <span data-ttu-id="dc720-1031">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="dc720-1031">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="dc720-1032">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="dc720-1032">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="dc720-1033">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-1033">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="dc720-1034">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1034">The checksum passes.</span></span>

<span data-ttu-id="dc720-1035">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1035">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1036">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1036">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1037">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1037">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1038">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1038">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="dc720-1039">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="dc720-1039">Keyword_cc_verification</span></span>

- <span data-ttu-id="dc720-1040">card verification</span><span class="sxs-lookup"><span data-stu-id="dc720-1040">card verification</span></span>
- <span data-ttu-id="dc720-1041">card identification number</span><span class="sxs-lookup"><span data-stu-id="dc720-1041">card identification number</span></span>
- <span data-ttu-id="dc720-1042">cvn
</span><span class="sxs-lookup"><span data-stu-id="dc720-1042">cvn</span></span>
- <span data-ttu-id="dc720-1043">cid
</span><span class="sxs-lookup"><span data-stu-id="dc720-1043">cid</span></span>
- <span data-ttu-id="dc720-1044">cvc2</span><span class="sxs-lookup"><span data-stu-id="dc720-1044">cvc2</span></span>
- <span data-ttu-id="dc720-1045">cvv2</span><span class="sxs-lookup"><span data-stu-id="dc720-1045">cvv2</span></span>
- <span data-ttu-id="dc720-1046">pin block
</span><span class="sxs-lookup"><span data-stu-id="dc720-1046">pin block</span></span>
- <span data-ttu-id="dc720-1047">security code
</span><span class="sxs-lookup"><span data-stu-id="dc720-1047">security code</span></span>
- <span data-ttu-id="dc720-1048">security number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1048">security number</span></span>
- <span data-ttu-id="dc720-1049">security no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1049">security no</span></span>
- <span data-ttu-id="dc720-1050">issue number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1050">issue number</span></span>
- <span data-ttu-id="dc720-1051">issue no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1051">issue no</span></span>
- <span data-ttu-id="dc720-1052">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="dc720-1052">cryptogramme</span></span>
- <span data-ttu-id="dc720-1053">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="dc720-1053">numéro de sécurité</span></span>
- <span data-ttu-id="dc720-1054">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="dc720-1054">numero de securite</span></span>
- <span data-ttu-id="dc720-1055">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1055">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="dc720-1056">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1056">kreditkartenprufnummer</span></span>
- <span data-ttu-id="dc720-1057">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1057">prüfziffer</span></span>
- <span data-ttu-id="dc720-1058">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1058">prufziffer</span></span>
- <span data-ttu-id="dc720-1059">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="dc720-1059">sicherheits Kode</span></span>
- <span data-ttu-id="dc720-1060">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="dc720-1060">sicherheitscode</span></span>
- <span data-ttu-id="dc720-1061">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1061">sicherheitsnummer</span></span>
- <span data-ttu-id="dc720-1062">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1062">verfalldatum</span></span>
- <span data-ttu-id="dc720-1063">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="dc720-1063">codice di verifica</span></span>
- <span data-ttu-id="dc720-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="dc720-p105">cod. sicurezza</span></span>
- <span data-ttu-id="dc720-1066">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="dc720-1066">cod sicurezza</span></span>
- <span data-ttu-id="dc720-1067">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="dc720-1067">n autorizzazione</span></span>
- <span data-ttu-id="dc720-1068">código
</span><span class="sxs-lookup"><span data-stu-id="dc720-1068">código</span></span>
- <span data-ttu-id="dc720-1069">codigo
</span><span class="sxs-lookup"><span data-stu-id="dc720-1069">codigo</span></span>
- <span data-ttu-id="dc720-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="dc720-p106">cod. seg</span></span>
- <span data-ttu-id="dc720-1072">COD seg</span><span class="sxs-lookup"><span data-stu-id="dc720-1072">cod seg</span></span>
- <span data-ttu-id="dc720-1073">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-1073">código de segurança</span></span>
- <span data-ttu-id="dc720-1074">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-1074">codigo de seguranca</span></span>
- <span data-ttu-id="dc720-1075">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-1075">codigo de segurança</span></span>
- <span data-ttu-id="dc720-1076">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-1076">código de seguranca</span></span>
- <span data-ttu-id="dc720-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-p107">cód. segurança</span></span>
- <span data-ttu-id="dc720-p108">COD. seguranca cod. segurança</span><span class="sxs-lookup"><span data-stu-id="dc720-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="dc720-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-p109">cód. seguranca</span></span>
- <span data-ttu-id="dc720-1084">cód segurança</span><span class="sxs-lookup"><span data-stu-id="dc720-1084">cód segurança</span></span>
- <span data-ttu-id="dc720-1085">решить seguranca cod segurança</span><span class="sxs-lookup"><span data-stu-id="dc720-1085">cod seguranca cod segurança</span></span>
- <span data-ttu-id="dc720-1086">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="dc720-1086">cód seguranca</span></span>
- <span data-ttu-id="dc720-1087">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="dc720-1087">número de verificação</span></span>
- <span data-ttu-id="dc720-1088">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1088">numero de verificacao</span></span>
- <span data-ttu-id="dc720-1089">ablauf
</span><span class="sxs-lookup"><span data-stu-id="dc720-1089">ablauf</span></span>
- <span data-ttu-id="dc720-1090">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="dc720-1090">gültig bis</span></span>
- <span data-ttu-id="dc720-1091">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1091">gültigkeitsdatum</span></span>
- <span data-ttu-id="dc720-1092">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="dc720-1092">gultig bis</span></span>
- <span data-ttu-id="dc720-1093">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1093">gultigkeitsdatum</span></span>
- <span data-ttu-id="dc720-1094">scadenza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1094">scadenza</span></span>
- <span data-ttu-id="dc720-1095">data scad
</span><span class="sxs-lookup"><span data-stu-id="dc720-1095">data scad</span></span>
- <span data-ttu-id="dc720-1096">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="dc720-1096">fecha de expiracion</span></span>
- <span data-ttu-id="dc720-1097">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="dc720-1097">fecha de venc</span></span>
- <span data-ttu-id="dc720-1098">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="dc720-1098">vencimiento</span></span>
- <span data-ttu-id="dc720-1099">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1099">válido hasta</span></span>
- <span data-ttu-id="dc720-1100">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1100">valido hasta</span></span>
- <span data-ttu-id="dc720-1101">vto
</span><span class="sxs-lookup"><span data-stu-id="dc720-1101">vto</span></span>
- <span data-ttu-id="dc720-1102">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="dc720-1102">data de expiração</span></span>
- <span data-ttu-id="dc720-1103">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1103">data de expiracao</span></span>
- <span data-ttu-id="dc720-1104">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="dc720-1104">data em que expira</span></span>
- <span data-ttu-id="dc720-1105">validade
</span><span class="sxs-lookup"><span data-stu-id="dc720-1105">validade</span></span>
- <span data-ttu-id="dc720-1106">valor
</span><span class="sxs-lookup"><span data-stu-id="dc720-1106">valor</span></span>
- <span data-ttu-id="dc720-1107">vencimento
</span><span class="sxs-lookup"><span data-stu-id="dc720-1107">vencimento</span></span>
- <span data-ttu-id="dc720-1108">Venc</span><span class="sxs-lookup"><span data-stu-id="dc720-1108">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="dc720-1109">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="dc720-1109">Keyword_cc_name</span></span>

- <span data-ttu-id="dc720-1110">amex</span><span class="sxs-lookup"><span data-stu-id="dc720-1110">amex</span></span>
- <span data-ttu-id="dc720-1111">
american express</span><span class="sxs-lookup"><span data-stu-id="dc720-1111">american express</span></span>
- <span data-ttu-id="dc720-1112">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="dc720-1112">americanexpress</span></span>
- <span data-ttu-id="dc720-1113">Visa</span><span class="sxs-lookup"><span data-stu-id="dc720-1113">Visa</span></span>
- <span data-ttu-id="dc720-1114">mastercard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1114">mastercard</span></span>
- <span data-ttu-id="dc720-1115">master card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1115">master card</span></span>
- <span data-ttu-id="dc720-1116">
mc
</span><span class="sxs-lookup"><span data-stu-id="dc720-1116">mc</span></span> 
- <span data-ttu-id="dc720-1117">mastercards</span><span class="sxs-lookup"><span data-stu-id="dc720-1117">mastercards</span></span>
- <span data-ttu-id="dc720-1118">
master cards</span><span class="sxs-lookup"><span data-stu-id="dc720-1118">master cards</span></span>
- <span data-ttu-id="dc720-1119">в diner клуба</span><span class="sxs-lookup"><span data-stu-id="dc720-1119">diner's Club</span></span>
- <span data-ttu-id="dc720-1120">diners club
</span><span class="sxs-lookup"><span data-stu-id="dc720-1120">diners club</span></span>
- <span data-ttu-id="dc720-1121">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="dc720-1121">dinersclub</span></span>
- <span data-ttu-id="dc720-1122">discover card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1122">discover card</span></span>
- <span data-ttu-id="dc720-1123">discovercard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1123">discovercard</span></span>
- <span data-ttu-id="dc720-1124">discover cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1124">discover cards</span></span>
- <span data-ttu-id="dc720-1125">JCB</span><span class="sxs-lookup"><span data-stu-id="dc720-1125">JCB</span></span>
- <span data-ttu-id="dc720-1126">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="dc720-1126">japanese card bureau</span></span>
- <span data-ttu-id="dc720-1127">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="dc720-1127">carte blanche</span></span>
- <span data-ttu-id="dc720-1128">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="dc720-1128">carteblanche</span></span>
- <span data-ttu-id="dc720-1129">credit card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1129">credit card</span></span>
- <span data-ttu-id="dc720-1130">CC #</span><span class="sxs-lookup"><span data-stu-id="dc720-1130">cc#</span></span>
- <span data-ttu-id="dc720-1131">cc #:</span><span class="sxs-lookup"><span data-stu-id="dc720-1131">cc#:</span></span>
- <span data-ttu-id="dc720-1132">
expiration date</span><span class="sxs-lookup"><span data-stu-id="dc720-1132">expiration date</span></span>
- <span data-ttu-id="dc720-1133">exp date
</span><span class="sxs-lookup"><span data-stu-id="dc720-1133">exp date</span></span>
- <span data-ttu-id="dc720-1134">
expiry date</span><span class="sxs-lookup"><span data-stu-id="dc720-1134">expiry date</span></span>
- <span data-ttu-id="dc720-1135">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="dc720-1135">date d’expiration</span></span>
- <span data-ttu-id="dc720-1136">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="dc720-1136">date d'exp</span></span>
- <span data-ttu-id="dc720-1137">
date expiration</span><span class="sxs-lookup"><span data-stu-id="dc720-1137">date expiration</span></span>
- <span data-ttu-id="dc720-1138">bank card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1138">bank card</span></span>
- <span data-ttu-id="dc720-1139">
bankcard</span><span class="sxs-lookup"><span data-stu-id="dc720-1139">bankcard</span></span>
- <span data-ttu-id="dc720-1140">card number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1140">card number</span></span>
- <span data-ttu-id="dc720-1141">card num
</span><span class="sxs-lookup"><span data-stu-id="dc720-1141">card num</span></span>
- <span data-ttu-id="dc720-1142">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1142">cardnumber</span></span>
- <span data-ttu-id="dc720-1143">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-1143">cardnumbers</span></span>
- <span data-ttu-id="dc720-1144">card numbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-1144">card numbers</span></span>
- <span data-ttu-id="dc720-1145">creditcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1145">creditcard</span></span>
- <span data-ttu-id="dc720-1146">credit cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1146">credit cards</span></span>
- <span data-ttu-id="dc720-1147">creditcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1147">creditcards</span></span>
- <span data-ttu-id="dc720-1148">ccn
</span><span class="sxs-lookup"><span data-stu-id="dc720-1148">ccn</span></span>
- <span data-ttu-id="dc720-1149">card holder
</span><span class="sxs-lookup"><span data-stu-id="dc720-1149">card holder</span></span>
- <span data-ttu-id="dc720-1150">cardholder
</span><span class="sxs-lookup"><span data-stu-id="dc720-1150">cardholder</span></span>
- <span data-ttu-id="dc720-1151">card holders
</span><span class="sxs-lookup"><span data-stu-id="dc720-1151">card holders</span></span>
- <span data-ttu-id="dc720-1152">cardholders
</span><span class="sxs-lookup"><span data-stu-id="dc720-1152">cardholders</span></span>
- <span data-ttu-id="dc720-1153">check card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1153">check card</span></span>
- <span data-ttu-id="dc720-1154">checkcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1154">checkcard</span></span>
- <span data-ttu-id="dc720-1155">check cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1155">check cards</span></span>
- <span data-ttu-id="dc720-1156">checkcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1156">checkcards</span></span>
- <span data-ttu-id="dc720-1157">debit card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1157">debit card</span></span>
- <span data-ttu-id="dc720-1158">debitcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1158">debitcard</span></span>
- <span data-ttu-id="dc720-1159">debit cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1159">debit cards</span></span>
- <span data-ttu-id="dc720-1160">debitcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1160">debitcards</span></span>
- <span data-ttu-id="dc720-1161">atm card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1161">atm card</span></span>
- <span data-ttu-id="dc720-1162">atmcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1162">atmcard</span></span>
- <span data-ttu-id="dc720-1163">atm cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1163">atm cards</span></span>
- <span data-ttu-id="dc720-1164">atmcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1164">atmcards</span></span>
- <span data-ttu-id="dc720-1165">
enroute</span><span class="sxs-lookup"><span data-stu-id="dc720-1165">enroute</span></span>
- <span data-ttu-id="dc720-1166">
en route</span><span class="sxs-lookup"><span data-stu-id="dc720-1166">en route</span></span>
- <span data-ttu-id="dc720-1167">card type
</span><span class="sxs-lookup"><span data-stu-id="dc720-1167">card type</span></span>
- <span data-ttu-id="dc720-1168">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="dc720-1168">carte bancaire</span></span>
- <span data-ttu-id="dc720-1169">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="dc720-1169">carte de crédit</span></span>
- <span data-ttu-id="dc720-1170">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="dc720-1170">carte de credit</span></span>
- <span data-ttu-id="dc720-1171">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1171">numéro de carte</span></span>
- <span data-ttu-id="dc720-1172">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1172">numero de carte</span></span>
- <span data-ttu-id="dc720-1173">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1173">nº de la carte</span></span>
- <span data-ttu-id="dc720-1174">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1174">nº de carte</span></span>
- <span data-ttu-id="dc720-1175">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1175">kreditkarte</span></span>
- <span data-ttu-id="dc720-1176">karte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1176">karte</span></span>
- <span data-ttu-id="dc720-1177">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1177">karteninhaber</span></span>
- <span data-ttu-id="dc720-1178">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="dc720-1178">karteninhabers</span></span>
- <span data-ttu-id="dc720-1179">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1179">kreditkarteninhaber</span></span>
- <span data-ttu-id="dc720-1180">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="dc720-1180">kreditkarteninstitut</span></span>
- <span data-ttu-id="dc720-1181">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="dc720-1181">kreditkartentyp</span></span>
- <span data-ttu-id="dc720-1182">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="dc720-1182">eigentümername</span></span>
- <span data-ttu-id="dc720-1183">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1183">kartennr</span></span> 
- <span data-ttu-id="dc720-1184">kartennummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1184">kartennummer</span></span>
- <span data-ttu-id="dc720-1185">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1185">kreditkartennummer</span></span>
- <span data-ttu-id="dc720-1186">kreditkarten nummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1186">kreditkarten-nummer</span></span>
- <span data-ttu-id="dc720-1187">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1187">carta di credito</span></span>
- <span data-ttu-id="dc720-1188">carta credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1188">carta credito</span></span>
- <span data-ttu-id="dc720-1189">carta</span><span class="sxs-lookup"><span data-stu-id="dc720-1189">carta</span></span>
- <span data-ttu-id="dc720-1190">n carta</span><span class="sxs-lookup"><span data-stu-id="dc720-1190">n carta</span></span>
- <span data-ttu-id="dc720-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-p110">nr. carta</span></span>
- <span data-ttu-id="dc720-1193">nr carta</span><span class="sxs-lookup"><span data-stu-id="dc720-1193">nr carta</span></span>
- <span data-ttu-id="dc720-1194">numero carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1194">numero carta</span></span>
- <span data-ttu-id="dc720-1195">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1195">numero della carta</span></span>
- <span data-ttu-id="dc720-1196">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1196">numero di carta</span></span>
- <span data-ttu-id="dc720-1197">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1197">tarjeta credito</span></span>
- <span data-ttu-id="dc720-1198">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1198">tarjeta de credito</span></span>
- <span data-ttu-id="dc720-1199">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="dc720-1199">tarjeta crédito</span></span>
- <span data-ttu-id="dc720-1200">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="dc720-1200">tarjeta de crédito</span></span>
- <span data-ttu-id="dc720-1201">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="dc720-1201">tarjeta de atm</span></span>
- <span data-ttu-id="dc720-1202">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="dc720-1202">tarjeta atm</span></span>
- <span data-ttu-id="dc720-1203">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1203">tarjeta debito</span></span>
- <span data-ttu-id="dc720-1204">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1204">tarjeta de debito</span></span>
- <span data-ttu-id="dc720-1205">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="dc720-1205">tarjeta débito</span></span>
- <span data-ttu-id="dc720-1206">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="dc720-1206">tarjeta de débito</span></span>
- <span data-ttu-id="dc720-1207">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1207">nº de tarjeta</span></span>
- <span data-ttu-id="dc720-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-p111">no. de tarjeta</span></span>
- <span data-ttu-id="dc720-1210">Не де tarjeta</span><span class="sxs-lookup"><span data-stu-id="dc720-1210">no de tarjeta</span></span>
- <span data-ttu-id="dc720-1211">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1211">numero de tarjeta</span></span>
- <span data-ttu-id="dc720-1212">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1212">número de tarjeta</span></span>
- <span data-ttu-id="dc720-1213">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1213">tarjeta no</span></span>
- <span data-ttu-id="dc720-1214">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="dc720-1214">tarjetahabiente</span></span>
- <span data-ttu-id="dc720-1215">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1215">cartão de crédito</span></span>
- <span data-ttu-id="dc720-1216">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1216">cartão de credito</span></span>
- <span data-ttu-id="dc720-1217">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1217">cartao de crédito</span></span>
- <span data-ttu-id="dc720-1218">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1218">cartao de credito</span></span>
- <span data-ttu-id="dc720-1219">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1219">cartão de débito</span></span>
- <span data-ttu-id="dc720-1220">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1220">cartao de débito</span></span>
- <span data-ttu-id="dc720-1221">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1221">cartão de debito</span></span>
- <span data-ttu-id="dc720-1222">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1222">cartao de debito</span></span>
- <span data-ttu-id="dc720-1223">débito automático</span><span class="sxs-lookup"><span data-stu-id="dc720-1223">débito automático</span></span>
- <span data-ttu-id="dc720-1224">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="dc720-1224">debito automatico</span></span>
- <span data-ttu-id="dc720-1225">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="dc720-1225">número do cartão</span></span>
- <span data-ttu-id="dc720-1226">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-1226">numero do cartão</span></span> 
- <span data-ttu-id="dc720-1227">número do cartao</span><span class="sxs-lookup"><span data-stu-id="dc720-1227">número do cartao</span></span>
- <span data-ttu-id="dc720-1228">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="dc720-1228">numero do cartao</span></span>
- <span data-ttu-id="dc720-1229">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-1229">número de cartão</span></span>
- <span data-ttu-id="dc720-1230">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-1230">numero de cartão</span></span>
- <span data-ttu-id="dc720-1231">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1231">número de cartao</span></span>
- <span data-ttu-id="dc720-1232">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1232">numero de cartao</span></span>
- <span data-ttu-id="dc720-1233">Действие cartão nº</span><span class="sxs-lookup"><span data-stu-id="dc720-1233">nº do cartão</span></span>
- <span data-ttu-id="dc720-1234">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1234">nº do cartao</span></span>
- <span data-ttu-id="dc720-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-p112">nº. do cartão</span></span>
- <span data-ttu-id="dc720-1237">не cartão действие</span><span class="sxs-lookup"><span data-stu-id="dc720-1237">no do cartão</span></span>
- <span data-ttu-id="dc720-1238">не cartao действие</span><span class="sxs-lookup"><span data-stu-id="dc720-1238">no do cartao</span></span>
- <span data-ttu-id="dc720-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-p113">no. do cartão</span></span>
- <span data-ttu-id="dc720-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="dc720-1243">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="dc720-1243">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1244">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1244">Format</span></span>

<span data-ttu-id="dc720-1245">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1245">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1246">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1246">Pattern</span></span>

<span data-ttu-id="dc720-1247">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1247">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1248">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1248">Checksum</span></span>

<span data-ttu-id="dc720-1249">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1249">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1250">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1250">Definition</span></span>

<span data-ttu-id="dc720-1251">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1251">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1252">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1252">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1253">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="dc720-1253">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1254">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1254">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="dc720-1255">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-1255">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="dc720-1256">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="dc720-1256">Croatian identity card</span></span>
- <span data-ttu-id="dc720-1257">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="dc720-1257">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="dc720-1258">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="dc720-1258">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1259">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1259">Format</span></span>

<span data-ttu-id="dc720-1260">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1260">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1261">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1261">Pattern</span></span>

<span data-ttu-id="dc720-1262">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-1262">10 digits:</span></span>
- <span data-ttu-id="dc720-1263">шесть цифр в виде ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="dc720-1263">Six digits in the form DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="dc720-1264">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-1264">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1265">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1265">Checksum</span></span>

<span data-ttu-id="dc720-1266">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1266">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1267">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1267">Definition</span></span>

<span data-ttu-id="dc720-1268">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1268">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1269">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1269">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1270">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-1270">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="dc720-1271">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1271">The checksum passes.</span></span>

<span data-ttu-id="dc720-1272">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1272">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1273">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1273">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1274">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1274">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1275">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1275">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="dc720-1276">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="dc720-1276">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="dc720-1277">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="dc720-1277">Personal Identification Number</span></span>
- <span data-ttu-id="dc720-1278">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="dc720-1278">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="dc720-1279">OIB
</span><span class="sxs-lookup"><span data-stu-id="dc720-1279">OIB</span></span> 

   
## <a name="czech-national-identity-card-number"></a><span data-ttu-id="dc720-1280">	Номер внутреннего удостоверения личности для Чехии</span><span class="sxs-lookup"><span data-stu-id="dc720-1280">Czech National Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1281">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1281">Format</span></span>

<span data-ttu-id="dc720-1282">10 цифр с косой чертой.</span><span class="sxs-lookup"><span data-stu-id="dc720-1282">10 digits containing a forward slash</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1283">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1283">Pattern</span></span>

<span data-ttu-id="dc720-1284">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-1284">10 digits:</span></span>
- <span data-ttu-id="dc720-1285">шесть цифр — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="dc720-1285">Six digits which are the date of birth</span></span> 
- <span data-ttu-id="dc720-1286">косая черта;</span><span class="sxs-lookup"><span data-stu-id="dc720-1286">A forward slash</span></span> 
- <span data-ttu-id="dc720-1287">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-1287">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1288">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1288">Checksum</span></span>

<span data-ttu-id="dc720-1289">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1289">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1290">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1290">Definition</span></span>

<span data-ttu-id="dc720-p115">Политика защиты от потери данных — это 85% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_czech_id_card поиска контента, который соответствует шаблону. Ключевое слово из Keyword_czech_id_card найти. Контрольная сумма передает.</span><span class="sxs-lookup"><span data-stu-id="dc720-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech National Identity Card Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_czech_id_card"/>
     <Match idRef="Keyword_czech_id_card"/>
  </Pattern>
</Entity>
```


### <a name="keywords"></a><span data-ttu-id="dc720-1294">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1294">Keywords</span></span>

- <span data-ttu-id="dc720-1295">Keyword_czech_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-1295">Keyword_czech_id_card</span></span>
- <span data-ttu-id="dc720-1296">Czech national identity card</span><span class="sxs-lookup"><span data-stu-id="dc720-1296">Czech national identity card</span></span>
- <span data-ttu-id="dc720-1297">Občanský průka</span><span class="sxs-lookup"><span data-stu-id="dc720-1297">Občanský průka</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="dc720-1298">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="dc720-1298">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1299">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1299">Format</span></span>

<span data-ttu-id="dc720-1300">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="dc720-1300">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1301">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1301">Pattern</span></span>

<span data-ttu-id="dc720-1302">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-1302">10 digits:</span></span>
- <span data-ttu-id="dc720-1303">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="dc720-1303">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="dc720-1304">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-1304">A hyphen</span></span> 
- <span data-ttu-id="dc720-1305">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-1305">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1306">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1306">Checksum</span></span>

<span data-ttu-id="dc720-1307">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1307">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1308">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1308">Definition</span></span>

<span data-ttu-id="dc720-p116">Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: регулярное выражение Regex_denmark_id находит контент, который соответствует шаблону. Ключевое слово из Keyword_denmark_id найти. Контрольная сумма передает.</span><span class="sxs-lookup"><span data-stu-id="dc720-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1312">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1312">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="dc720-1313">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="dc720-1313">Keyword_denmark_id</span></span>

- <span data-ttu-id="dc720-1314">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="dc720-1314">Personal Identification Number</span></span>
- <span data-ttu-id="dc720-1315">CPR</span><span class="sxs-lookup"><span data-stu-id="dc720-1315">CPR</span></span>
- <span data-ttu-id="dc720-1316">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="dc720-1316">Det Centrale Personregister</span></span>
- <span data-ttu-id="dc720-1317">Personnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1317">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="dc720-1318">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="dc720-1318">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1319">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1319">Format</span></span>

<span data-ttu-id="dc720-1320">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1320">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1321">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1321">Pattern</span></span>

<span data-ttu-id="dc720-1322">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="dc720-1322">Pattern must include all of the following:</span></span>
- <span data-ttu-id="dc720-1323">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="dc720-1323">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="dc720-1324">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="dc720-1324">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="dc720-1325">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="dc720-1325">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1326">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1326">Checksum</span></span>

<span data-ttu-id="dc720-1327">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1327">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1328">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1328">Definition</span></span>

<span data-ttu-id="dc720-1329">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1329">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1330">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1330">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1331">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1331">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1332">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1332">Keywords</span></span>

<span data-ttu-id="dc720-1333">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1333">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="dc720-1334">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="dc720-1334">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1335">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1335">Format</span></span>

<span data-ttu-id="dc720-1336">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1336">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1337">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1337">Pattern</span></span>

<span data-ttu-id="dc720-1338">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="dc720-1338">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1339">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1339">Checksum</span></span>

<span data-ttu-id="dc720-1340">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1340">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1341">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1341">Definition</span></span>

<span data-ttu-id="dc720-1342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1343">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-1343">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1344">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-1344">At least one of the following is true:</span></span>
    - <span data-ttu-id="dc720-1345">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="dc720-1345">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="dc720-1346">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="dc720-1346">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="dc720-1347">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="dc720-1347">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="dc720-1348">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="dc720-1348">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="dc720-1349">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-1349">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="dc720-1350">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1350">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1351">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1351">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="dc720-1352">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="dc720-1352">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="dc720-1353">Номер счета</span><span class="sxs-lookup"><span data-stu-id="dc720-1353">account number</span></span> 
- <span data-ttu-id="dc720-1354">card number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1354">card number</span></span> 
- <span data-ttu-id="dc720-1355">card no.
</span><span class="sxs-lookup"><span data-stu-id="dc720-1355">card no.</span></span> 
- <span data-ttu-id="dc720-1356">security number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1356">security number</span></span> 
- <span data-ttu-id="dc720-1357">CC #</span><span class="sxs-lookup"><span data-stu-id="dc720-1357">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="dc720-1358">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="dc720-1358">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="dc720-1359">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1359">acct nbr</span></span> 
- <span data-ttu-id="dc720-1360">acct num
</span><span class="sxs-lookup"><span data-stu-id="dc720-1360">acct num</span></span> 
- <span data-ttu-id="dc720-1361">acct no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1361">acct no</span></span> 
- <span data-ttu-id="dc720-1362">american express
</span><span class="sxs-lookup"><span data-stu-id="dc720-1362">american express</span></span> 
- <span data-ttu-id="dc720-1363">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="dc720-1363">americanexpress</span></span> 
- <span data-ttu-id="dc720-1364">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="dc720-1364">americano espresso</span></span> 
- <span data-ttu-id="dc720-1365">amex</span><span class="sxs-lookup"><span data-stu-id="dc720-1365">amex</span></span> 
- <span data-ttu-id="dc720-1366">atm card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1366">atm card</span></span> 
- <span data-ttu-id="dc720-1367">atm cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1367">atm cards</span></span> 
- <span data-ttu-id="dc720-1368">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1368">atm kaart</span></span> 
- <span data-ttu-id="dc720-1369">atmcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1369">atmcard</span></span> 
- <span data-ttu-id="dc720-1370">atmcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1370">atmcards</span></span> 
- <span data-ttu-id="dc720-1371">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1371">atmkaart</span></span> 
- <span data-ttu-id="dc720-1372">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="dc720-1372">atmkaarten</span></span> 
- <span data-ttu-id="dc720-1373">bancontact
</span><span class="sxs-lookup"><span data-stu-id="dc720-1373">bancontact</span></span> 
- <span data-ttu-id="dc720-1374">bank card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1374">bank card</span></span> 
- <span data-ttu-id="dc720-1375">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1375">bankkaart</span></span> 
- <span data-ttu-id="dc720-1376">card holder
</span><span class="sxs-lookup"><span data-stu-id="dc720-1376">card holder</span></span> 
- <span data-ttu-id="dc720-1377">card holders
</span><span class="sxs-lookup"><span data-stu-id="dc720-1377">card holders</span></span> 
- <span data-ttu-id="dc720-1378">card num
</span><span class="sxs-lookup"><span data-stu-id="dc720-1378">card num</span></span> 
- <span data-ttu-id="dc720-1379">card number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1379">card number</span></span> 
- <span data-ttu-id="dc720-1380">card numbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-1380">card numbers</span></span> 
- <span data-ttu-id="dc720-1381">card type
</span><span class="sxs-lookup"><span data-stu-id="dc720-1381">card type</span></span> 
- <span data-ttu-id="dc720-1382">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="dc720-1382">cardano numerico</span></span> 
- <span data-ttu-id="dc720-1383">cardholder
</span><span class="sxs-lookup"><span data-stu-id="dc720-1383">cardholder</span></span> 
- <span data-ttu-id="dc720-1384">cardholders
</span><span class="sxs-lookup"><span data-stu-id="dc720-1384">cardholders</span></span> 
- <span data-ttu-id="dc720-1385">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1385">cardnumber</span></span> 
- <span data-ttu-id="dc720-1386">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-1386">cardnumbers</span></span> 
- <span data-ttu-id="dc720-1387">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="dc720-1387">carta bianca</span></span> 
- <span data-ttu-id="dc720-1388">carta credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1388">carta credito</span></span> 
- <span data-ttu-id="dc720-1389">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1389">carta di credito</span></span> 
- <span data-ttu-id="dc720-1390">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1390">cartao de credito</span></span> 
- <span data-ttu-id="dc720-1391">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1391">cartao de crédito</span></span> 
- <span data-ttu-id="dc720-1392">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1392">cartao de debito</span></span> 
- <span data-ttu-id="dc720-1393">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1393">cartao de débito</span></span> 
- <span data-ttu-id="dc720-1394">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="dc720-1394">carte bancaire</span></span> 
- <span data-ttu-id="dc720-1395">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="dc720-1395">carte blanche</span></span> 
- <span data-ttu-id="dc720-1396">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="dc720-1396">carte bleue</span></span> 
- <span data-ttu-id="dc720-1397">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="dc720-1397">carte de credit</span></span> 
- <span data-ttu-id="dc720-1398">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="dc720-1398">carte de crédit</span></span> 
- <span data-ttu-id="dc720-1399">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1399">carte di credito</span></span> 
- <span data-ttu-id="dc720-1400">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="dc720-1400">carteblanche</span></span> 
- <span data-ttu-id="dc720-1401">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1401">cartão de credito</span></span> 
- <span data-ttu-id="dc720-1402">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1402">cartão de crédito</span></span> 
- <span data-ttu-id="dc720-1403">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1403">cartão de debito</span></span> 
- <span data-ttu-id="dc720-1404">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1404">cartão de débito</span></span> 
- <span data-ttu-id="dc720-1405">cb
</span><span class="sxs-lookup"><span data-stu-id="dc720-1405">cb</span></span> 
- <span data-ttu-id="dc720-1406">ccn
</span><span class="sxs-lookup"><span data-stu-id="dc720-1406">ccn</span></span> 
- <span data-ttu-id="dc720-1407">check card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1407">check card</span></span> 
- <span data-ttu-id="dc720-1408">check cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1408">check cards</span></span> 
- <span data-ttu-id="dc720-1409">checkcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1409">checkcard</span></span>
- <span data-ttu-id="dc720-1410">checkcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1410">checkcards</span></span> 
- <span data-ttu-id="dc720-1411">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1411">chequekaart</span></span> 
- <span data-ttu-id="dc720-1412">cirrus
</span><span class="sxs-lookup"><span data-stu-id="dc720-1412">cirrus</span></span> 
- <span data-ttu-id="dc720-1413">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="dc720-1413">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="dc720-1414">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1414">controlekaart</span></span> 
- <span data-ttu-id="dc720-1415">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="dc720-1415">controlekaarten</span></span> 
- <span data-ttu-id="dc720-1416">credit card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1416">credit card</span></span> 
- <span data-ttu-id="dc720-1417">credit cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1417">credit cards</span></span> 
- <span data-ttu-id="dc720-1418">creditcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1418">creditcard</span></span> 
- <span data-ttu-id="dc720-1419">creditcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1419">creditcards</span></span> 
- <span data-ttu-id="dc720-1420">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1420">debetkaart</span></span> 
- <span data-ttu-id="dc720-1421">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="dc720-1421">debetkaarten</span></span> 
- <span data-ttu-id="dc720-1422">debit card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1422">debit card</span></span> 
- <span data-ttu-id="dc720-1423">debit cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1423">debit cards</span></span> 
- <span data-ttu-id="dc720-1424">debitcard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1424">debitcard</span></span> 
- <span data-ttu-id="dc720-1425">debitcards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1425">debitcards</span></span> 
- <span data-ttu-id="dc720-1426">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="dc720-1426">debito automatico</span></span> 
- <span data-ttu-id="dc720-1427">diners club
</span><span class="sxs-lookup"><span data-stu-id="dc720-1427">diners club</span></span> 
- <span data-ttu-id="dc720-1428">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="dc720-1428">dinersclub</span></span> 
- <span data-ttu-id="dc720-1429">обнаружение</span><span class="sxs-lookup"><span data-stu-id="dc720-1429">discover</span></span> 
- <span data-ttu-id="dc720-1430">discover card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1430">discover card</span></span> 
- <span data-ttu-id="dc720-1431">discover cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1431">discover cards</span></span> 
- <span data-ttu-id="dc720-1432">discovercard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1432">discovercard</span></span> 
- <span data-ttu-id="dc720-1433">discovercards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1433">discovercards</span></span> 
- <span data-ttu-id="dc720-1434">débito automático</span><span class="sxs-lookup"><span data-stu-id="dc720-1434">débito automático</span></span>
- <span data-ttu-id="dc720-1435">
edc
</span><span class="sxs-lookup"><span data-stu-id="dc720-1435">edc</span></span> 
- <span data-ttu-id="dc720-1436">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="dc720-1436">eigentümername</span></span> 
- <span data-ttu-id="dc720-1437">european debit card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1437">european debit card</span></span> 
- <span data-ttu-id="dc720-1438">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1438">hoofdkaart</span></span> 
- <span data-ttu-id="dc720-1439">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="dc720-1439">hoofdkaarten</span></span> 
- <span data-ttu-id="dc720-1440">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="dc720-1440">in viaggio</span></span> 
- <span data-ttu-id="dc720-1441">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="dc720-1441">japanese card bureau</span></span> 
- <span data-ttu-id="dc720-1442">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="dc720-1442">japanse kaartdienst</span></span> 
- <span data-ttu-id="dc720-1443">jcb
</span><span class="sxs-lookup"><span data-stu-id="dc720-1443">jcb</span></span> 
- <span data-ttu-id="dc720-1444">kaart
</span><span class="sxs-lookup"><span data-stu-id="dc720-1444">kaart</span></span> 
- <span data-ttu-id="dc720-1445">kaart num
</span><span class="sxs-lookup"><span data-stu-id="dc720-1445">kaart num</span></span> 
- <span data-ttu-id="dc720-1446">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="dc720-1446">kaartaantal</span></span> 
- <span data-ttu-id="dc720-1447">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="dc720-1447">kaartaantallen</span></span> 
- <span data-ttu-id="dc720-1448">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="dc720-1448">kaarthouder</span></span> 
- <span data-ttu-id="dc720-1449">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="dc720-1449">kaarthouders</span></span> 
- <span data-ttu-id="dc720-1450">karte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1450">karte</span></span>  
- <span data-ttu-id="dc720-1451">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1451">karteninhaber</span></span> 
- <span data-ttu-id="dc720-1452">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="dc720-1452">karteninhabers</span></span>
- <span data-ttu-id="dc720-1453">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1453">kartennr</span></span> 
- <span data-ttu-id="dc720-1454">kartennummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1454">kartennummer</span></span> 
- <span data-ttu-id="dc720-1455">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1455">kreditkarte</span></span> 
- <span data-ttu-id="dc720-1456">kreditkarten nummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1456">kreditkarten-nummer</span></span> 
- <span data-ttu-id="dc720-1457">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1457">kreditkarteninhaber</span></span> 
- <span data-ttu-id="dc720-1458">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="dc720-1458">kreditkarteninstitut</span></span> 
- <span data-ttu-id="dc720-1459">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1459">kreditkartennummer</span></span> 
- <span data-ttu-id="dc720-1460">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="dc720-1460">kreditkartentyp</span></span> 
- <span data-ttu-id="dc720-1461">maestro
</span><span class="sxs-lookup"><span data-stu-id="dc720-1461">maestro</span></span> 
- <span data-ttu-id="dc720-1462">master card
</span><span class="sxs-lookup"><span data-stu-id="dc720-1462">master card</span></span> 
- <span data-ttu-id="dc720-1463">master cards
</span><span class="sxs-lookup"><span data-stu-id="dc720-1463">master cards</span></span> 
- <span data-ttu-id="dc720-1464">mastercard
</span><span class="sxs-lookup"><span data-stu-id="dc720-1464">mastercard</span></span> 
- <span data-ttu-id="dc720-1465">mastercards</span><span class="sxs-lookup"><span data-stu-id="dc720-1465">mastercards</span></span> 
- <span data-ttu-id="dc720-1466">mc</span><span class="sxs-lookup"><span data-stu-id="dc720-1466">mc</span></span> 
- <span data-ttu-id="dc720-1467">mister cash
</span><span class="sxs-lookup"><span data-stu-id="dc720-1467">mister cash</span></span> 
- <span data-ttu-id="dc720-1468">n carta</span><span class="sxs-lookup"><span data-stu-id="dc720-1468">n carta</span></span> 
- <span data-ttu-id="dc720-1469">carta</span><span class="sxs-lookup"><span data-stu-id="dc720-1469">carta</span></span> 
- <span data-ttu-id="dc720-1470">Не де tarjeta</span><span class="sxs-lookup"><span data-stu-id="dc720-1470">no de tarjeta</span></span> 
- <span data-ttu-id="dc720-1471">не cartao действие</span><span class="sxs-lookup"><span data-stu-id="dc720-1471">no do cartao</span></span> 
- <span data-ttu-id="dc720-1472">не cartão действие</span><span class="sxs-lookup"><span data-stu-id="dc720-1472">no do cartão</span></span> 
- <span data-ttu-id="dc720-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="dc720-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-p118">no. do cartao</span></span> 
- <span data-ttu-id="dc720-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-p119">no. do cartão</span></span> 
- <span data-ttu-id="dc720-1479">nr carta</span><span class="sxs-lookup"><span data-stu-id="dc720-1479">nr carta</span></span> 
- <span data-ttu-id="dc720-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-p120">nr. carta</span></span> 
- <span data-ttu-id="dc720-1482">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1482">numeri di scheda</span></span> 
- <span data-ttu-id="dc720-1483">numero carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1483">numero carta</span></span> 
- <span data-ttu-id="dc720-1484">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1484">numero de cartao</span></span> 
- <span data-ttu-id="dc720-1485">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1485">numero de carte</span></span> 
- <span data-ttu-id="dc720-1486">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-1486">numero de cartão</span></span> 
- <span data-ttu-id="dc720-1487">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1487">numero de tarjeta</span></span>
- <span data-ttu-id="dc720-1488">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1488">numero della carta</span></span> 
- <span data-ttu-id="dc720-1489">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1489">numero di carta</span></span> 
- <span data-ttu-id="dc720-1490">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1490">numero di scheda</span></span> 
- <span data-ttu-id="dc720-1491">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1491">numero do cartao</span></span> 
- <span data-ttu-id="dc720-1492">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-1492">numero do cartão</span></span> 
- <span data-ttu-id="dc720-1493">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1493">numéro de carte</span></span> 
- <span data-ttu-id="dc720-1494">nº carta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1494">nº carta</span></span> 
- <span data-ttu-id="dc720-1495">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1495">nº de carte</span></span> 
- <span data-ttu-id="dc720-1496">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="dc720-1496">nº de la carte</span></span> 
- <span data-ttu-id="dc720-1497">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1497">nº de tarjeta</span></span> 
- <span data-ttu-id="dc720-1498">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1498">nº do cartao</span></span> 
- <span data-ttu-id="dc720-1499">Действие cartão nº</span><span class="sxs-lookup"><span data-stu-id="dc720-1499">nº do cartão</span></span> 
- <span data-ttu-id="dc720-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-p121">nº. do cartão</span></span> 
- <span data-ttu-id="dc720-1502">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1502">número de cartao</span></span> 
- <span data-ttu-id="dc720-1503">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="dc720-1503">número de cartão</span></span> 
- <span data-ttu-id="dc720-1504">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1504">número de tarjeta</span></span> 
- <span data-ttu-id="dc720-1505">número do cartao</span><span class="sxs-lookup"><span data-stu-id="dc720-1505">número do cartao</span></span> 
- <span data-ttu-id="dc720-1506">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="dc720-1506">scheda dell'assegno</span></span> 
- <span data-ttu-id="dc720-1507">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="dc720-1507">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="dc720-1508">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="dc720-1508">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="dc720-1509">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="dc720-1509">scheda della banca</span></span> 
- <span data-ttu-id="dc720-1510">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="dc720-1510">scheda di controllo</span></span> 
- <span data-ttu-id="dc720-1511">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1511">scheda di debito</span></span> 
- <span data-ttu-id="dc720-1512">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="dc720-1512">scheda matrice</span></span> 
- <span data-ttu-id="dc720-1513">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="dc720-1513">schede dell'atmosfera</span></span> 
- <span data-ttu-id="dc720-1514">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="dc720-1514">schede di controllo</span></span> 
- <span data-ttu-id="dc720-1515">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1515">schede di debito</span></span> 
- <span data-ttu-id="dc720-1516">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="dc720-1516">schede matrici</span></span> 
- <span data-ttu-id="dc720-1517">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1517">scoprono la scheda</span></span> 
- <span data-ttu-id="dc720-1518">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="dc720-1518">scoprono le schede</span></span> 
- <span data-ttu-id="dc720-1519">solo
</span><span class="sxs-lookup"><span data-stu-id="dc720-1519">solo</span></span> 
- <span data-ttu-id="dc720-1520">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1520">supporti di scheda</span></span> 
- <span data-ttu-id="dc720-1521">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1521">supporto di scheda</span></span> 
- <span data-ttu-id="dc720-1522">ключ</span><span class="sxs-lookup"><span data-stu-id="dc720-1522">switch</span></span> 
- <span data-ttu-id="dc720-1523">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="dc720-1523">tarjeta atm</span></span> 
- <span data-ttu-id="dc720-1524">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1524">tarjeta credito</span></span> 
- <span data-ttu-id="dc720-1525">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="dc720-1525">tarjeta de atm</span></span> 
- <span data-ttu-id="dc720-1526">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1526">tarjeta de credito</span></span> 
- <span data-ttu-id="dc720-1527">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1527">tarjeta de debito</span></span> 
- <span data-ttu-id="dc720-1528">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="dc720-1528">tarjeta debito</span></span> 
- <span data-ttu-id="dc720-1529">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1529">tarjeta no</span></span>
- <span data-ttu-id="dc720-1530">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="dc720-1530">tarjetahabiente</span></span> 
- <span data-ttu-id="dc720-1531">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1531">tipo della scheda</span></span> 
- <span data-ttu-id="dc720-1532">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="dc720-1532">ufficio giapponese della</span></span> 
- <span data-ttu-id="dc720-1533">scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1533">scheda</span></span> 
- <span data-ttu-id="dc720-1534">v pay
</span><span class="sxs-lookup"><span data-stu-id="dc720-1534">v pay</span></span> 
- <span data-ttu-id="dc720-1535">v оплаты</span><span class="sxs-lookup"><span data-stu-id="dc720-1535">v-pay</span></span> 
- <span data-ttu-id="dc720-1536">visa
</span><span class="sxs-lookup"><span data-stu-id="dc720-1536">visa</span></span> 
- <span data-ttu-id="dc720-1537">visa plus
</span><span class="sxs-lookup"><span data-stu-id="dc720-1537">visa plus</span></span> 
- <span data-ttu-id="dc720-1538">visa electron
</span><span class="sxs-lookup"><span data-stu-id="dc720-1538">visa electron</span></span> 
- <span data-ttu-id="dc720-1539">visto
</span><span class="sxs-lookup"><span data-stu-id="dc720-1539">visto</span></span> 
- <span data-ttu-id="dc720-1540">visum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1540">visum</span></span> 
- <span data-ttu-id="dc720-1541">vpay
</span><span class="sxs-lookup"><span data-stu-id="dc720-1541">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="dc720-1542">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="dc720-1542">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="dc720-1543">card identification number</span><span class="sxs-lookup"><span data-stu-id="dc720-1543">card identification number</span></span>
- <span data-ttu-id="dc720-1544">card verification</span><span class="sxs-lookup"><span data-stu-id="dc720-1544">card verification</span></span> 
- <span data-ttu-id="dc720-1545">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="dc720-1545">cardi la verifica</span></span> 
- <span data-ttu-id="dc720-1546">cid
</span><span class="sxs-lookup"><span data-stu-id="dc720-1546">cid</span></span> 
- <span data-ttu-id="dc720-1547">COD seg</span><span class="sxs-lookup"><span data-stu-id="dc720-1547">cod seg</span></span> 
- <span data-ttu-id="dc720-1548">COD seguranca</span><span class="sxs-lookup"><span data-stu-id="dc720-1548">cod seguranca</span></span> 
- <span data-ttu-id="dc720-1549">COD segurança</span><span class="sxs-lookup"><span data-stu-id="dc720-1549">cod segurança</span></span> 
- <span data-ttu-id="dc720-1550">COD sicurezza</span><span class="sxs-lookup"><span data-stu-id="dc720-1550">cod sicurezza</span></span> 
- <span data-ttu-id="dc720-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="dc720-p122">cod. seg</span></span> 
- <span data-ttu-id="dc720-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-p123">cod. seguranca</span></span> 
- <span data-ttu-id="dc720-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-p124">cod. segurança</span></span> 
- <span data-ttu-id="dc720-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="dc720-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="dc720-1559">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1559">codice di sicurezza</span></span> 
- <span data-ttu-id="dc720-1560">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="dc720-1560">codice di verifica</span></span> 
- <span data-ttu-id="dc720-1561">codigo
</span><span class="sxs-lookup"><span data-stu-id="dc720-1561">codigo</span></span> 
- <span data-ttu-id="dc720-1562">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-1562">codigo de seguranca</span></span> 
- <span data-ttu-id="dc720-1563">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-1563">codigo de segurança</span></span> 
- <span data-ttu-id="dc720-1564">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="dc720-1564">crittogramma</span></span> 
- <span data-ttu-id="dc720-1565">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="dc720-1565">cryptogram</span></span> 
- <span data-ttu-id="dc720-1566">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="dc720-1566">cryptogramme</span></span> 
- <span data-ttu-id="dc720-1567">CV2</span><span class="sxs-lookup"><span data-stu-id="dc720-1567">cv2</span></span> 
- <span data-ttu-id="dc720-1568">cvc
</span><span class="sxs-lookup"><span data-stu-id="dc720-1568">cvc</span></span> 
- <span data-ttu-id="dc720-1569">cvc2</span><span class="sxs-lookup"><span data-stu-id="dc720-1569">cvc2</span></span> 
- <span data-ttu-id="dc720-1570">cvn
</span><span class="sxs-lookup"><span data-stu-id="dc720-1570">cvn</span></span> 
- <span data-ttu-id="dc720-1571">cvv
</span><span class="sxs-lookup"><span data-stu-id="dc720-1571">cvv</span></span> 
- <span data-ttu-id="dc720-1572">cvv2</span><span class="sxs-lookup"><span data-stu-id="dc720-1572">cvv2</span></span> 
- <span data-ttu-id="dc720-1573">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="dc720-1573">cód seguranca</span></span> 
- <span data-ttu-id="dc720-1574">cód segurança</span><span class="sxs-lookup"><span data-stu-id="dc720-1574">cód segurança</span></span> 
- <span data-ttu-id="dc720-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-p126">cód. seguranca</span></span> 
- <span data-ttu-id="dc720-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-p127">cód. segurança</span></span> 
- <span data-ttu-id="dc720-1579">código
</span><span class="sxs-lookup"><span data-stu-id="dc720-1579">código</span></span> 
- <span data-ttu-id="dc720-1580">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="dc720-1580">código de seguranca</span></span> 
- <span data-ttu-id="dc720-1581">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="dc720-1581">código de segurança</span></span> 
- <span data-ttu-id="dc720-1582">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="dc720-1582">de kaart controle</span></span> 
- <span data-ttu-id="dc720-1583">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="dc720-1583">geeft nr uit</span></span> 
- <span data-ttu-id="dc720-1584">issue no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1584">issue no</span></span> 
- <span data-ttu-id="dc720-1585">issue number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1585">issue number</span></span> 
- <span data-ttu-id="dc720-1586">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1586">kaartidentificatienummer</span></span> 
- <span data-ttu-id="dc720-1587">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1587">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="dc720-1588">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1588">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="dc720-1589">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="dc720-1589">kwestieaantal</span></span> 
- <span data-ttu-id="dc720-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="dc720-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="dc720-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="dc720-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="dc720-1594">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="dc720-1594">numero de securite</span></span> 
- <span data-ttu-id="dc720-1595">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1595">numero de verificacao</span></span> 
- <span data-ttu-id="dc720-1596">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="dc720-1596">numero dell'edizione</span></span> 
- <span data-ttu-id="dc720-1597">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="dc720-1597">numero di identificazione della</span></span> 
- <span data-ttu-id="dc720-1598">scheda
</span><span class="sxs-lookup"><span data-stu-id="dc720-1598">scheda</span></span> 
- <span data-ttu-id="dc720-1599">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1599">numero di sicurezza</span></span> 
- <span data-ttu-id="dc720-1600">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="dc720-1600">numero van veiligheid</span></span> 
- <span data-ttu-id="dc720-1601">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="dc720-1601">numéro de sécurité</span></span> 
- <span data-ttu-id="dc720-1602">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="dc720-1602">nº autorizzazione</span></span> 
- <span data-ttu-id="dc720-1603">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="dc720-1603">número de verificação</span></span> 
- <span data-ttu-id="dc720-1604">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="dc720-1604">perno il blocco</span></span> 
- <span data-ttu-id="dc720-1605">pin block
</span><span class="sxs-lookup"><span data-stu-id="dc720-1605">pin block</span></span> 
- <span data-ttu-id="dc720-1606">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1606">prufziffer</span></span> 
- <span data-ttu-id="dc720-1607">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1607">prüfziffer</span></span> 
- <span data-ttu-id="dc720-1608">security code
</span><span class="sxs-lookup"><span data-stu-id="dc720-1608">security code</span></span> 
- <span data-ttu-id="dc720-1609">security no
</span><span class="sxs-lookup"><span data-stu-id="dc720-1609">security no</span></span> 
- <span data-ttu-id="dc720-1610">security number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1610">security number</span></span> 
- <span data-ttu-id="dc720-1611">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="dc720-1611">sicherheits kode</span></span> 
- <span data-ttu-id="dc720-1612">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="dc720-1612">sicherheitscode</span></span> 
- <span data-ttu-id="dc720-1613">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1613">sicherheitsnummer</span></span> 
- <span data-ttu-id="dc720-1614">speldblok
</span><span class="sxs-lookup"><span data-stu-id="dc720-1614">speldblok</span></span> 
- <span data-ttu-id="dc720-1615">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1615">veiligheid nr</span></span> 
- <span data-ttu-id="dc720-1616">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="dc720-1616">veiligheidsaantal</span></span> 
- <span data-ttu-id="dc720-1617">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="dc720-1617">veiligheidscode</span></span> 
- <span data-ttu-id="dc720-1618">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-1618">veiligheidsnummer</span></span> 
- <span data-ttu-id="dc720-1619">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1619">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="dc720-1620">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="dc720-1620">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="dc720-1621">ablauf
</span><span class="sxs-lookup"><span data-stu-id="dc720-1621">ablauf</span></span> 
- <span data-ttu-id="dc720-1622">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="dc720-1622">data de expiracao</span></span> 
- <span data-ttu-id="dc720-1623">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="dc720-1623">data de expiração</span></span> 
- <span data-ttu-id="dc720-1624">data del exp
</span><span class="sxs-lookup"><span data-stu-id="dc720-1624">data del exp</span></span> 
- <span data-ttu-id="dc720-1625">data di exp
</span><span class="sxs-lookup"><span data-stu-id="dc720-1625">data di exp</span></span> 
- <span data-ttu-id="dc720-1626">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1626">data di scadenza</span></span> 
- <span data-ttu-id="dc720-1627">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="dc720-1627">data em que expira</span></span> 
- <span data-ttu-id="dc720-1628">data scad
</span><span class="sxs-lookup"><span data-stu-id="dc720-1628">data scad</span></span> 
- <span data-ttu-id="dc720-1629">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1629">data scadenza</span></span> 
- <span data-ttu-id="dc720-1630">date de validité
</span><span class="sxs-lookup"><span data-stu-id="dc720-1630">date de validité</span></span> 
- <span data-ttu-id="dc720-1631">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="dc720-1631">datum afloop</span></span> 
- <span data-ttu-id="dc720-1632">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="dc720-1632">datum van exp</span></span> 
- <span data-ttu-id="dc720-1633">de afloop
</span><span class="sxs-lookup"><span data-stu-id="dc720-1633">de afloop</span></span> 
- <span data-ttu-id="dc720-1634">espira
</span><span class="sxs-lookup"><span data-stu-id="dc720-1634">espira</span></span> 
- <span data-ttu-id="dc720-1635">espira
</span><span class="sxs-lookup"><span data-stu-id="dc720-1635">espira</span></span> 
- <span data-ttu-id="dc720-1636">exp date
</span><span class="sxs-lookup"><span data-stu-id="dc720-1636">exp date</span></span> 
- <span data-ttu-id="dc720-1637">exp datum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1637">exp datum</span></span> 
- <span data-ttu-id="dc720-1638">истечение срока действия</span><span class="sxs-lookup"><span data-stu-id="dc720-1638">expiration</span></span> 
- <span data-ttu-id="dc720-1639">expire
</span><span class="sxs-lookup"><span data-stu-id="dc720-1639">expire</span></span> 
- <span data-ttu-id="dc720-1640">expires
</span><span class="sxs-lookup"><span data-stu-id="dc720-1640">expires</span></span> 
- <span data-ttu-id="dc720-1641">expiry
</span><span class="sxs-lookup"><span data-stu-id="dc720-1641">expiry</span></span> 
- <span data-ttu-id="dc720-1642">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="dc720-1642">fecha de expiracion</span></span> 
- <span data-ttu-id="dc720-1643">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="dc720-1643">fecha de venc</span></span> 
- <span data-ttu-id="dc720-1644">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="dc720-1644">gultig bis</span></span> 
- <span data-ttu-id="dc720-1645">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1645">gultigkeitsdatum</span></span> 
- <span data-ttu-id="dc720-1646">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="dc720-1646">gültig bis</span></span> 
- <span data-ttu-id="dc720-1647">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1647">gültigkeitsdatum</span></span> 
- <span data-ttu-id="dc720-1648">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1648">la scadenza</span></span> 
- <span data-ttu-id="dc720-1649">scadenza
</span><span class="sxs-lookup"><span data-stu-id="dc720-1649">scadenza</span></span> 
- <span data-ttu-id="dc720-1650">valable
</span><span class="sxs-lookup"><span data-stu-id="dc720-1650">valable</span></span> 
- <span data-ttu-id="dc720-1651">validade
</span><span class="sxs-lookup"><span data-stu-id="dc720-1651">validade</span></span> 
- <span data-ttu-id="dc720-1652">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1652">valido hasta</span></span> 
- <span data-ttu-id="dc720-1653">valor
</span><span class="sxs-lookup"><span data-stu-id="dc720-1653">valor</span></span> 
- <span data-ttu-id="dc720-1654">venc
</span><span class="sxs-lookup"><span data-stu-id="dc720-1654">venc</span></span> 
- <span data-ttu-id="dc720-1655">vencimento
</span><span class="sxs-lookup"><span data-stu-id="dc720-1655">vencimento</span></span> 
- <span data-ttu-id="dc720-1656">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="dc720-1656">vencimiento</span></span> 
- <span data-ttu-id="dc720-1657">verloopt
</span><span class="sxs-lookup"><span data-stu-id="dc720-1657">verloopt</span></span> 
- <span data-ttu-id="dc720-1658">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="dc720-1658">vervaldag</span></span> 
- <span data-ttu-id="dc720-1659">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1659">vervaldatum</span></span> 
- <span data-ttu-id="dc720-1660">vto
</span><span class="sxs-lookup"><span data-stu-id="dc720-1660">vto</span></span> 
- <span data-ttu-id="dc720-1661">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="dc720-1661">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="dc720-1662">Номер водительского удостоверения ЕС</span><span class="sxs-lookup"><span data-stu-id="dc720-1662">EU Driver's License Number</span></span>

<span data-ttu-id="dc720-1663">Для получения дополнительных сведений см [Тип конфиденциальных данных номер водительского удостоверения ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="dc720-1663">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="dc720-1664">Национальный ЕС идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="dc720-1664">EU National Identification Number</span></span>

<span data-ttu-id="dc720-1665">Для получения дополнительных сведений см [ЕС национальный идентификационный номер тип конфиденциальных данных](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="dc720-1665">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="dc720-1666">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="dc720-1666">EU Passport Number</span></span>

<span data-ttu-id="dc720-1667">Для получения дополнительных сведений см [номер паспорта ЕС тип конфиденциальных данных](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="dc720-1667">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="dc720-1668">Страховой номер для ЕС или иметь эквивалентные права идентификатор</span><span class="sxs-lookup"><span data-stu-id="dc720-1668">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="dc720-1669">Для получения дополнительных сведений, видеть [страховой номер для ЕС или эквивалентный идентификатор типа конфиденциальной информации](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="dc720-1669">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="dc720-1670">Идентификационный номер налога ЕС</span><span class="sxs-lookup"><span data-stu-id="dc720-1670">EU Tax Identification Number</span></span>

<span data-ttu-id="dc720-1671">Для получения дополнительных сведений см [идентификационный номер налога ЕС тип конфиденциальных данных](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="dc720-1671">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="dc720-1672">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="dc720-1672">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1673">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1673">Format</span></span>

<span data-ttu-id="dc720-1674">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="dc720-1674">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1675">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1675">Pattern</span></span>

<span data-ttu-id="dc720-1676">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="dc720-1676">Pattern must include all of the following:</span></span>
- <span data-ttu-id="dc720-1677">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="dc720-1677">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="dc720-1678">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="dc720-1678">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="dc720-1679">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="dc720-1679">Three-digit personal identification number</span></span> 
- <span data-ttu-id="dc720-1680">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-1680">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1681">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1681">Checksum</span></span>

<span data-ttu-id="dc720-1682">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1682">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1683">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1683">Definition</span></span>

<span data-ttu-id="dc720-1684">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1684">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1685">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1685">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1686">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="dc720-1686">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="dc720-1687">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1687">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1688">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1688">Keywords</span></span>

- <span data-ttu-id="dc720-1689">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="dc720-1689">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="dc720-1690">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="dc720-1690">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="dc720-1691">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="dc720-1691">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="dc720-1692">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="dc720-1692">Personbeteckning</span></span>
- <span data-ttu-id="dc720-1693">Personnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1693">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="dc720-1694">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="dc720-1694">Finland Passport Number</span></span>

<span data-ttu-id="dc720-p130">Форматирование сочетание девяти буквы и цифры сочетание шаблон девяти только буквы и цифры: два букв (без учета регистра) семь цифр контрольной суммой нет определения политики DLP — 75% уверены в том, что он обнаружил этот тип конфиденциальных данных, если в Близость 300 знаков: регулярное выражение Regex_finland_passport_number находит контент, который соответствует шаблону. Ключевое слово из Keyword_finland_passport_number найти. <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity> Passi Passport Keyword_finland_passport_number ключевых слов</span><span class="sxs-lookup"><span data-stu-id="dc720-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="dc720-1699">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="dc720-1699">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1700">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1700">Format</span></span>

<span data-ttu-id="dc720-1701">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1701">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1702">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1702">Pattern</span></span>

<span data-ttu-id="dc720-1703">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="dc720-1703">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1704">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1704">Checksum</span></span>

<span data-ttu-id="dc720-1705">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1705">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1706">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1706">Definition</span></span>

<span data-ttu-id="dc720-1707">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1707">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1708">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-1708">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1709">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-1709">At least one of the following is true:</span></span>
- <span data-ttu-id="dc720-1710">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="dc720-1710">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="dc720-1711">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-1711">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1712">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1712">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="dc720-1713">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="dc720-1713">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="dc720-1714">drivers licence</span><span class="sxs-lookup"><span data-stu-id="dc720-1714">drivers licence</span></span>
- <span data-ttu-id="dc720-1715">drivers license</span><span class="sxs-lookup"><span data-stu-id="dc720-1715">drivers license</span></span>
- <span data-ttu-id="dc720-1716">driving licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-1716">driving licence</span></span>
- <span data-ttu-id="dc720-1717">управляющий лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-1717">driving license</span></span>
- <span data-ttu-id="dc720-1718">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="dc720-1718">permis de conduire</span></span>
- <span data-ttu-id="dc720-1719">
licence number</span><span class="sxs-lookup"><span data-stu-id="dc720-1719">licence number</span></span>
- <span data-ttu-id="dc720-1720">
license number</span><span class="sxs-lookup"><span data-stu-id="dc720-1720">license number</span></span>
- <span data-ttu-id="dc720-1721">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="dc720-1721">licence numbers</span></span>
- <span data-ttu-id="dc720-1722">

license numbers</span><span class="sxs-lookup"><span data-stu-id="dc720-1722">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="dc720-1723">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="dc720-1723">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1724">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1724">Format</span></span>

<span data-ttu-id="dc720-1725">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1725">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1726">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1726">Pattern</span></span>

<span data-ttu-id="dc720-1727">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1727">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1728">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1728">Checksum</span></span>

<span data-ttu-id="dc720-1729">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1729">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1730">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1730">Definition</span></span>

<span data-ttu-id="dc720-1731">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1731">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1732">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-1732">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1733">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1733">Keywords</span></span>

<span data-ttu-id="dc720-1734">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1734">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="dc720-1735">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="dc720-1735">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1736">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1736">Format</span></span>

<span data-ttu-id="dc720-1737">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="dc720-1737">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1738">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1738">Pattern</span></span>

<span data-ttu-id="dc720-1739">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="dc720-1739">Nine digits and letters:</span></span>
- <span data-ttu-id="dc720-1740">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-1740">Two digits</span></span> 
- <span data-ttu-id="dc720-1741">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-1741">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-1742">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-1742">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1743">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1743">Checksum</span></span>

<span data-ttu-id="dc720-1744">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1744">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1745">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1745">Definition</span></span>

<span data-ttu-id="dc720-1746">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1746">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1747">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1747">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1748">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="dc720-1748">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1749">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1749">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="dc720-1750">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-1750">Keyword_passport</span></span>

- <span data-ttu-id="dc720-1751">Passport Number</span><span class="sxs-lookup"><span data-stu-id="dc720-1751">Passport Number</span></span>
- <span data-ttu-id="dc720-1752">
Passport No</span><span class="sxs-lookup"><span data-stu-id="dc720-1752">Passport No</span></span>
- <span data-ttu-id="dc720-1753">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-1753">Passport #</span></span>
- <span data-ttu-id="dc720-1754">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-1754">Passport#</span></span>
- <span data-ttu-id="dc720-1755">PassportID</span><span class="sxs-lookup"><span data-stu-id="dc720-1755">PassportID</span></span>
- <span data-ttu-id="dc720-1756">Passportno
</span><span class="sxs-lookup"><span data-stu-id="dc720-1756">Passportno</span></span>
- <span data-ttu-id="dc720-1757">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-1757">passportnumber</span></span>
- <span data-ttu-id="dc720-1758">パスポート</span><span class="sxs-lookup"><span data-stu-id="dc720-1758">パスポート</span></span>
- <span data-ttu-id="dc720-1759">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-1759">パスポート番号</span></span>
- <span data-ttu-id="dc720-1760">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="dc720-1760">パスポートのNum</span></span>
- <span data-ttu-id="dc720-1761">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-1761">パスポート ＃</span></span> 
- <span data-ttu-id="dc720-1762">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="dc720-1762">Numéro de passeport</span></span>
- <span data-ttu-id="dc720-1763">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="dc720-1763">Passeport n °</span></span>
- <span data-ttu-id="dc720-1764">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="dc720-1764">Passeport Non</span></span>
- <span data-ttu-id="dc720-1765">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-1765">Passeport #</span></span>
- <span data-ttu-id="dc720-1766">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-1766">Passeport#</span></span>
- <span data-ttu-id="dc720-1767">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="dc720-1767">PasseportNon</span></span>
- <span data-ttu-id="dc720-1768">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="dc720-1768">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="dc720-1769">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="dc720-1769">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1770">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1770">Format</span></span>

<span data-ttu-id="dc720-1771">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1771">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1772">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1772">Pattern</span></span>

<span data-ttu-id="dc720-1773">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="dc720-1773">Must match one of two patterns:</span></span>
- <span data-ttu-id="dc720-1774">13 цифр, пробел, а затем две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-1774">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="dc720-1775">или</span><span class="sxs-lookup"><span data-stu-id="dc720-1775">or</span></span>
- <span data-ttu-id="dc720-1776">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1776">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1777">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1777">Checksum</span></span>

<span data-ttu-id="dc720-1778">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1778">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1779">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1779">Definition</span></span>

<span data-ttu-id="dc720-1780">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1780">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1781">Функция Func_french_insee или Func_fr_insee находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-1781">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1782">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="dc720-1782">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="dc720-1783">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1783">The checksum passes.</span></span>

<span data-ttu-id="dc720-1784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1785">Функция Func_french_insee или Func_fr_insee находит контент, который соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-1785">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1786">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="dc720-1786">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="dc720-1787">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1787">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1788">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1788">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="dc720-1789">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="dc720-1789">Keyword_fr_insee</span></span>

- <span data-ttu-id="dc720-1790">insee</span><span class="sxs-lookup"><span data-stu-id="dc720-1790">insee</span></span>
- <span data-ttu-id="dc720-1791">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="dc720-1791">securité sociale</span></span>
- <span data-ttu-id="dc720-1792">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="dc720-1792">securite sociale</span></span>
- <span data-ttu-id="dc720-1793">
national id</span><span class="sxs-lookup"><span data-stu-id="dc720-1793">national id</span></span>
- <span data-ttu-id="dc720-1794">
national identification</span><span class="sxs-lookup"><span data-stu-id="dc720-1794">national identification</span></span>
- <span data-ttu-id="dc720-1795">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="dc720-1795">numéro d'identité</span></span>
- <span data-ttu-id="dc720-1796">Нет d'identité</span><span class="sxs-lookup"><span data-stu-id="dc720-1796">no d'identité</span></span>
- <span data-ttu-id="dc720-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="dc720-p131">no. d'identité</span></span>
- <span data-ttu-id="dc720-1799">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="dc720-1799">numero d'identite</span></span>
- <span data-ttu-id="dc720-1800">не d'identite</span><span class="sxs-lookup"><span data-stu-id="dc720-1800">no d'identite</span></span>
- <span data-ttu-id="dc720-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="dc720-p132">no. d'identite</span></span>
- <span data-ttu-id="dc720-1803">social security number
</span><span class="sxs-lookup"><span data-stu-id="dc720-1803">social security number</span></span>
- <span data-ttu-id="dc720-1804">
social security code</span><span class="sxs-lookup"><span data-stu-id="dc720-1804">social security code</span></span>
- <span data-ttu-id="dc720-1805">social insurance number</span><span class="sxs-lookup"><span data-stu-id="dc720-1805">social insurance number</span></span>
- <span data-ttu-id="dc720-1806">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="dc720-1806">le numéro d'identification nationale</span></span>
- <span data-ttu-id="dc720-1807">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="dc720-1807">d'identité nationale</span></span>
- <span data-ttu-id="dc720-1808">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="dc720-1808">numéro de sécurité sociale</span></span>
- <span data-ttu-id="dc720-1809">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="dc720-1809">le code de la sécurité sociale</span></span>
- <span data-ttu-id="dc720-1810">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="dc720-1810">numéro d'assurance sociale</span></span>
- <span data-ttu-id="dc720-1811">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="dc720-1811">numéro de sécu</span></span>
- <span data-ttu-id="dc720-1812">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="dc720-1812">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="dc720-1813">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="dc720-1813">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1814">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1814">Format</span></span>

<span data-ttu-id="dc720-1815">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="dc720-1815">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1816">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1816">Pattern</span></span>

<span data-ttu-id="dc720-1817">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-1817">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="dc720-1818">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="dc720-1818">A digit or letter</span></span> 
- <span data-ttu-id="dc720-1819">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-1819">Two digits</span></span> 
- <span data-ttu-id="dc720-1820">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="dc720-1820">Six digits or letters</span></span> 
- <span data-ttu-id="dc720-1821">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dc720-1821">A digit</span></span> 
- <span data-ttu-id="dc720-1822">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="dc720-1822">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1823">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1823">Checksum</span></span>

<span data-ttu-id="dc720-1824">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1825">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1825">Definition</span></span>

<span data-ttu-id="dc720-1826">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1826">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1827">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1827">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1828">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-1828">At least one of the following is true:</span></span>
    - <span data-ttu-id="dc720-1829">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-1829">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="dc720-1830">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="dc720-1830">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="dc720-1831">найдено ключевое слово из Keyword_german_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="dc720-1831">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="dc720-1832">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1832">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1833">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1833">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="dc720-1834">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="dc720-1834">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="dc720-1835">Führerschein</span><span class="sxs-lookup"><span data-stu-id="dc720-1835">Führerschein</span></span>
- <span data-ttu-id="dc720-1836">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="dc720-1836">Fuhrerschein</span></span>
- <span data-ttu-id="dc720-1837">Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="dc720-1837">Fuehrerschein</span></span>
- <span data-ttu-id="dc720-1838">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1838">Führerscheinnummer</span></span>
- <span data-ttu-id="dc720-1839">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1839">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="dc720-1840">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1840">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="dc720-1841">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="dc720-1841">Führerschein-</span></span> 
- <span data-ttu-id="dc720-1842">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="dc720-1842">Fuhrerschein-</span></span> 
- <span data-ttu-id="dc720-1843">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="dc720-1843">Fuehrerschein-</span></span> 
- <span data-ttu-id="dc720-1844">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="dc720-1844">FührerscheinnummerNr</span></span>
- <span data-ttu-id="dc720-1845">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="dc720-1845">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="dc720-1846">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="dc720-1846">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="dc720-1847">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1847">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="dc720-1848">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1848">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="dc720-1849">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1849">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="dc720-1850">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1850">Führerschein- Nr</span></span>
- <span data-ttu-id="dc720-1851">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1851">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="dc720-1852">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1852">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="dc720-1853">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="dc720-1853">Führerschein- Klasse</span></span> 
- <span data-ttu-id="dc720-1854">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="dc720-1854">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="dc720-1855">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1855">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="dc720-1856">FührerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="dc720-1856">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="dc720-1857">FuhrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="dc720-1857">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="dc720-1858">FuehrerscheinnummerNr</span><span class="sxs-lookup"><span data-stu-id="dc720-1858">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="dc720-1859">FührerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1859">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="dc720-1860">FuhrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1860">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="dc720-1861">FuehrerscheinnummerKlasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1861">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="dc720-1862">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1862">Führerschein- Nr</span></span> 
- <span data-ttu-id="dc720-1863">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1863">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="dc720-1864">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1864">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="dc720-1865">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="dc720-1865">Führerschein- Klasse</span></span> 
- <span data-ttu-id="dc720-1866">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="dc720-1866">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="dc720-1867">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1867">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="dc720-1868">DL</span><span class="sxs-lookup"><span data-stu-id="dc720-1868">DL</span></span> 
- <span data-ttu-id="dc720-1869">DLS</span><span class="sxs-lookup"><span data-stu-id="dc720-1869">DLS</span></span>
- <span data-ttu-id="dc720-1870">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="dc720-1870">Driv Lic</span></span> 
- <span data-ttu-id="dc720-1871">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="dc720-1871">Driv Licen</span></span> 
- <span data-ttu-id="dc720-1872">Driv License</span><span class="sxs-lookup"><span data-stu-id="dc720-1872">Driv License</span></span>
- <span data-ttu-id="dc720-1873">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="dc720-1873">Driv Licenses</span></span> 
- <span data-ttu-id="dc720-1874">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-1874">Driv Licence</span></span> 
- <span data-ttu-id="dc720-1875">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-1875">Driv Licences</span></span> 
- <span data-ttu-id="dc720-1876">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="dc720-1876">Driv Lic</span></span> 
- <span data-ttu-id="dc720-1877">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="dc720-1877">Driver Licen</span></span> 
- <span data-ttu-id="dc720-1878">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-1878">Driver License</span></span> 
- <span data-ttu-id="dc720-1879">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-1879">Driver Licenses</span></span> 
- <span data-ttu-id="dc720-1880">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-1880">Driver Licence</span></span> 
- <span data-ttu-id="dc720-1881">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-1881">Driver Licences</span></span> 
- <span data-ttu-id="dc720-1882">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-1882">Drivers Lic</span></span> 
- <span data-ttu-id="dc720-1883">Драйверы Licen</span><span class="sxs-lookup"><span data-stu-id="dc720-1883">Drivers Licen</span></span> 
- <span data-ttu-id="dc720-1884">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-1884">Drivers License</span></span> 
- <span data-ttu-id="dc720-1885">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-1885">Drivers Licenses</span></span> 
- <span data-ttu-id="dc720-1886">Лицензия драйверы</span><span class="sxs-lookup"><span data-stu-id="dc720-1886">Drivers Licence</span></span> 
- <span data-ttu-id="dc720-1887">Число лицензий на драйверы</span><span class="sxs-lookup"><span data-stu-id="dc720-1887">Drivers Licences</span></span> 
- <span data-ttu-id="dc720-1888">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-1888">Driver's Lic</span></span> 
- <span data-ttu-id="dc720-1889">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="dc720-1889">Driver's Licen</span></span> 
- <span data-ttu-id="dc720-1890">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-1890">Driver's License</span></span> 
- <span data-ttu-id="dc720-1891">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-1891">Driver's Licenses</span></span> 
- <span data-ttu-id="dc720-1892">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-1892">Driver's Licence</span></span> 
- <span data-ttu-id="dc720-1893">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-1893">Driver's Licences</span></span> 
- <span data-ttu-id="dc720-1894">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="dc720-1894">Driving Lic</span></span> 
- <span data-ttu-id="dc720-1895">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="dc720-1895">Driving Licen</span></span> 
- <span data-ttu-id="dc720-1896">Driving License
</span><span class="sxs-lookup"><span data-stu-id="dc720-1896">Driving License</span></span> 
- <span data-ttu-id="dc720-1897">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="dc720-1897">Driving Licenses</span></span> 
- <span data-ttu-id="dc720-1898">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="dc720-1898">Driving Licence</span></span> 
- <span data-ttu-id="dc720-1899">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="dc720-1899">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="dc720-1900">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="dc720-1900">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="dc720-1901">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1901">Nr-Führerschein</span></span> 
- <span data-ttu-id="dc720-1902">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1902">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="dc720-1903">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1903">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="dc720-1904">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1904">No-Führerschein</span></span> 
- <span data-ttu-id="dc720-1905">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1905">No-Fuhrerschein</span></span> 
- <span data-ttu-id="dc720-1906">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1906">No-Fuehrerschein</span></span> 
- <span data-ttu-id="dc720-1907">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1907">N-Führerschein</span></span> 
- <span data-ttu-id="dc720-1908">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1908">N-Fuhrerschein</span></span> 
- <span data-ttu-id="dc720-1909">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="dc720-1909">N-Fuehrerschein</span></span>
- <span data-ttu-id="dc720-1910">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1910">Nr-Führerschein</span></span> 
- <span data-ttu-id="dc720-1911">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1911">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="dc720-1912">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1912">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="dc720-1913">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1913">No-Führerschein</span></span> 
- <span data-ttu-id="dc720-1914">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1914">No-Fuhrerschein</span></span> 
- <span data-ttu-id="dc720-1915">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1915">No-Fuehrerschein</span></span> 
- <span data-ttu-id="dc720-1916">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1916">N-Führerschein</span></span> 
- <span data-ttu-id="dc720-1917">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="dc720-1917">N-Fuhrerschein</span></span> 
- <span data-ttu-id="dc720-1918">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="dc720-1918">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="dc720-1919">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="dc720-1919">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="dc720-1920">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="dc720-1920">ausstellungsdatum</span></span>
- <span data-ttu-id="dc720-1921">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="dc720-1921">ausstellungsort</span></span>
- <span data-ttu-id="dc720-1922">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="dc720-1922">ausstellende behöde</span></span>
- <span data-ttu-id="dc720-1923">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="dc720-1923">ausstellende behorde</span></span>
- <span data-ttu-id="dc720-1924">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="dc720-1924">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="dc720-1925">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="dc720-1925">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1926">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1926">Format</span></span>

<span data-ttu-id="dc720-1927">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="dc720-1927">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1928">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1928">Pattern</span></span>

<span data-ttu-id="dc720-1929">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="dc720-1929">Pattern must include all of the following:</span></span>
- <span data-ttu-id="dc720-1930">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="dc720-1930">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="dc720-1931">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-1931">Three digits</span></span> 
- <span data-ttu-id="dc720-1932">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="dc720-1932">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="dc720-1933">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dc720-1933">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1934">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1934">Checksum</span></span>

<span data-ttu-id="dc720-1935">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-1935">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1936">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1936">Definition</span></span>

<span data-ttu-id="dc720-1937">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1937">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1938">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1938">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1939">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="dc720-1939">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="dc720-1940">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1940">The checksum passes.</span></span>

<span data-ttu-id="dc720-1941">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1941">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1942">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1942">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1943">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="dc720-1943">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="dc720-1944">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-1944">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-1945">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1945">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="dc720-1946">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-1946">Keyword_german_passport</span></span>

- <span data-ttu-id="dc720-1947">reisepass</span><span class="sxs-lookup"><span data-stu-id="dc720-1947">reisepass</span></span>
- <span data-ttu-id="dc720-1948">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="dc720-1948">reisepasse</span></span>
- <span data-ttu-id="dc720-1949">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1949">reisepassnummer</span></span>
- <span data-ttu-id="dc720-1950">passport</span><span class="sxs-lookup"><span data-stu-id="dc720-1950">passport</span></span>
- <span data-ttu-id="dc720-1951">

passports</span><span class="sxs-lookup"><span data-stu-id="dc720-1951">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="dc720-1952">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="dc720-1952">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="dc720-1953">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="dc720-1953">geburtsdatum</span></span>
- <span data-ttu-id="dc720-1954">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="dc720-1954">ausstellungsdatum</span></span>
- <span data-ttu-id="dc720-1955">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="dc720-1955">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="dc720-1956">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="dc720-1956">Keyword_german_passport_number</span></span>

<span data-ttu-id="dc720-1957">Не-Nr Reisepass-Reisepass</span><span class="sxs-lookup"><span data-stu-id="dc720-1957">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="dc720-1958">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="dc720-1958">Keyword_german_passport1</span></span>

<span data-ttu-id="dc720-1959">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="dc720-1959">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="dc720-1960">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="dc720-1960">Keyword_german_passport2</span></span>

<span data-ttu-id="dc720-1961">bnationalit.t</span><span class="sxs-lookup"><span data-stu-id="dc720-1961">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="dc720-1962">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="dc720-1962">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1963">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1963">Format</span></span>

<span data-ttu-id="dc720-1964">Начиная с 1 ноября 2010 г.: девяти только буквы и цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-1964">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="dc720-1965">От 1 апреля 1987 до 31 октября 2010:10 цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-1965">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1966">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1966">Pattern</span></span>

<span data-ttu-id="dc720-1967">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="dc720-1967">Since 1 November 2010:</span></span>
- <span data-ttu-id="dc720-1968">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-1968">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-1969">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1969">Eight digits</span></span>

<span data-ttu-id="dc720-1970">От 1 апреля 1987 до 31 октября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="dc720-1970">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="dc720-1971">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-1971">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1972">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1972">Checksum</span></span>

<span data-ttu-id="dc720-1973">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-1973">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-1974">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-1974">Definition</span></span>

<span data-ttu-id="dc720-1975">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-1975">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-1976">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-1976">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-1977">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="dc720-1977">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-1978">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-1978">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="dc720-1979">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-1979">Keyword_germany_id_card</span></span>

- <span data-ttu-id="dc720-1980">Identity Card</span><span class="sxs-lookup"><span data-stu-id="dc720-1980">Identity Card</span></span>
- <span data-ttu-id="dc720-1981">ID</span><span class="sxs-lookup"><span data-stu-id="dc720-1981">ID</span></span>
- <span data-ttu-id="dc720-1982">Identification</span><span class="sxs-lookup"><span data-stu-id="dc720-1982">Identification</span></span>
- <span data-ttu-id="dc720-1983">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="dc720-1983">Personalausweis</span></span>
- <span data-ttu-id="dc720-1984">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-1984">Identifizierungsnummer</span></span>
- <span data-ttu-id="dc720-1985">Ausweis</span><span class="sxs-lookup"><span data-stu-id="dc720-1985">Ausweis</span></span>
- <span data-ttu-id="dc720-1986">Identifikation</span><span class="sxs-lookup"><span data-stu-id="dc720-1986">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="dc720-1987">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="dc720-1987">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="dc720-1988">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-1988">Format</span></span>

<span data-ttu-id="dc720-1989">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="dc720-1989">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-1990">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-1990">Pattern</span></span>

<span data-ttu-id="dc720-1991">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="dc720-1991">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="dc720-1992">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="dc720-1992">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="dc720-1993">Тире</span><span class="sxs-lookup"><span data-stu-id="dc720-1993">A dash</span></span> 
- <span data-ttu-id="dc720-1994">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-1994">Six digits</span></span>

<span data-ttu-id="dc720-1995">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="dc720-1995">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="dc720-1996">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="dc720-1996">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="dc720-1997">Тире</span><span class="sxs-lookup"><span data-stu-id="dc720-1997">A dash</span></span> 
- <span data-ttu-id="dc720-1998">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-1998">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-1999">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-1999">Checksum</span></span>

<span data-ttu-id="dc720-2000">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2000">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2001">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2001">Definition</span></span>

<span data-ttu-id="dc720-2002">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2002">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2003">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2003">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2004">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="dc720-2004">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2005">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2005">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="dc720-2006">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-2006">Keyword_greece_id_card</span></span>

- <span data-ttu-id="dc720-2007">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="dc720-2007">Greek identity Card</span></span>
- <span data-ttu-id="dc720-2008">Tautotita</span><span class="sxs-lookup"><span data-stu-id="dc720-2008">Tautotita</span></span>
- <span data-ttu-id="dc720-2009">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="dc720-2009">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="dc720-2010">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="dc720-2010">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="dc720-2011">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="dc720-2011">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2012">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2012">Format</span></span>

<span data-ttu-id="dc720-2013">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="dc720-2013">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2014">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2014">Pattern</span></span>

<span data-ttu-id="dc720-2015">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="dc720-2015">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="dc720-2016">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="dc720-2016">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2017">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2017">Six digits</span></span> 
- <span data-ttu-id="dc720-2018">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="dc720-2018">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2019">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2019">Checksum</span></span>

<span data-ttu-id="dc720-2020">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2020">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2021">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2021">Definition</span></span>

<span data-ttu-id="dc720-2022">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2022">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2023">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2023">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2024">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="dc720-2024">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="dc720-2025">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2025">The checksum passes.</span></span>

<span data-ttu-id="dc720-2026">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2026">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2027">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2027">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2028">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2028">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2029">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2029">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="dc720-2030">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-2030">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="dc720-2031">Hong Kong Identity Card</span><span class="sxs-lookup"><span data-stu-id="dc720-2031">Hong Kong Identity Card</span></span>
- <span data-ttu-id="dc720-2032">HKID</span><span class="sxs-lookup"><span data-stu-id="dc720-2032">HKID</span></span>
- <span data-ttu-id="dc720-2033">ID card</span><span class="sxs-lookup"><span data-stu-id="dc720-2033">ID card</span></span>
- <span data-ttu-id="dc720-2034">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2034">香港身份證</span></span> 
- <span data-ttu-id="dc720-2035">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2035">香港永久性居民身份證</span></span> 
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="dc720-2036">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2036">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2037">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2037">Format</span></span>

<span data-ttu-id="dc720-2038">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2038">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2039">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2039">Pattern</span></span>

<span data-ttu-id="dc720-2040">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2040">10 letters or digits:</span></span>
- <span data-ttu-id="dc720-2041">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="dc720-2041">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2042">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2042">Four digits</span></span> 
- <span data-ttu-id="dc720-2043">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="dc720-2043">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2044">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2044">Checksum</span></span>

<span data-ttu-id="dc720-2045">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2045">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2046">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2046">Definition</span></span>

<span data-ttu-id="dc720-2047">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2047">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2048">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2048">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2049">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-2049">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="dc720-2050">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2050">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2051">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2051">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="dc720-2052">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2052">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="dc720-2053">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2053">Permanent Account Number</span></span> 
- <span data-ttu-id="dc720-2054">PAN
</span><span class="sxs-lookup"><span data-stu-id="dc720-2054">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="dc720-2055">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="dc720-2055">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2056">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2056">Format</span></span>

<span data-ttu-id="dc720-2057">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="dc720-2057">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2058">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2058">Pattern</span></span>

<span data-ttu-id="dc720-2059">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2059">12 digits:</span></span>
- <span data-ttu-id="dc720-2060">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2060">Four digits</span></span> 
- <span data-ttu-id="dc720-2061">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="dc720-2061">An optional space or dash</span></span> 
- <span data-ttu-id="dc720-2062">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2062">Four digits</span></span> 
- <span data-ttu-id="dc720-2063">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="dc720-2063">An optional space or dash</span></span> 
- <span data-ttu-id="dc720-2064">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="dc720-2064">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2065">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2065">Checksum</span></span>

<span data-ttu-id="dc720-2066">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2066">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2067">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2067">Definition</span></span>

<span data-ttu-id="dc720-p133">Политика защиты от потери данных — это 85% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_india_aadhaar поиска контента, который соответствует шаблону. Ключевое слово из Keyword_india_aadhar найти. Контрольная сумма передает. Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_india_aadhaar поиска контента, который соответствует шаблону. Контрольная сумма передает. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="dc720-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="dc720-2074">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2074">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="dc720-2075">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="dc720-2075">Keyword_india_aadhar</span></span>
- <span data-ttu-id="dc720-2076">Aadhar</span><span class="sxs-lookup"><span data-stu-id="dc720-2076">Aadhar</span></span>
- <span data-ttu-id="dc720-2077">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="dc720-2077">Aadhaar</span></span>
- <span data-ttu-id="dc720-2078">UID</span><span class="sxs-lookup"><span data-stu-id="dc720-2078">UID</span></span>
- <span data-ttu-id="dc720-2079">आधार</span><span class="sxs-lookup"><span data-stu-id="dc720-2079">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="dc720-2080">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="dc720-2080">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2081">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2081">Format</span></span>

<span data-ttu-id="dc720-2082">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="dc720-2082">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2083">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2083">Pattern</span></span>

<span data-ttu-id="dc720-2084">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2084">16 digits:</span></span>
- <span data-ttu-id="dc720-2085">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="dc720-2085">Two-digit province code</span></span> 
- <span data-ttu-id="dc720-2086">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="dc720-2086">A period (optional)</span></span> 
- <span data-ttu-id="dc720-2087">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="dc720-2087">Two-digit regency or city code</span></span> 
- <span data-ttu-id="dc720-2088">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="dc720-2088">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="dc720-2089">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="dc720-2089">A period (optional)</span></span> 
- <span data-ttu-id="dc720-2090">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="dc720-2090">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="dc720-2091">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="dc720-2091">A period (optional)</span></span> 
- <span data-ttu-id="dc720-2092">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2092">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2093">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2093">Checksum</span></span>

<span data-ttu-id="dc720-2094">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2094">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2095">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2095">Definition</span></span>

<span data-ttu-id="dc720-2096">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2096">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2097">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-2097">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2098">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="dc720-2098">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="dc720-2099">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2099">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2100">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-2100">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2101">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2101">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="dc720-2102">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="dc720-2102">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="dc720-2103">KTP</span><span class="sxs-lookup"><span data-stu-id="dc720-2103">KTP</span></span>
- <span data-ttu-id="dc720-2104">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="dc720-2104">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="dc720-2105">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="dc720-2105">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="dc720-2106">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2106">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2107">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2107">Format</span></span>

<span data-ttu-id="dc720-2108">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="dc720-2108">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2109">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2109">Pattern</span></span>

<span data-ttu-id="dc720-2110">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="dc720-2110">Pattern must include all of the following:</span></span>

- <span data-ttu-id="dc720-2111">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="dc720-2111">Two-letter country code</span></span>
- <span data-ttu-id="dc720-2112">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="dc720-2112">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="dc720-2113">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="dc720-2113">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="dc720-2114">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2114">1-3 letters or digits</span></span>

<span data-ttu-id="dc720-p134">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="dc720-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="dc720-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="dc720-2117">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2118">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2118">Checksum</span></span>

<span data-ttu-id="dc720-2119">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2119">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2120">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2120">Definition</span></span>

<span data-ttu-id="dc720-2121">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2121">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2122">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2122">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2123">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2123">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2124">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2124">Keywords</span></span>

<span data-ttu-id="dc720-2125">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2125">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="dc720-2126">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="dc720-2126">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2127">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2127">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="dc720-2128">IPv4:</span><span class="sxs-lookup"><span data-stu-id="dc720-2128">IPv4:</span></span>
<span data-ttu-id="dc720-2129">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="dc720-2129">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="dc720-2130">Протокол IPv6</span><span class="sxs-lookup"><span data-stu-id="dc720-2130">IPv6:</span></span>
<span data-ttu-id="dc720-2131"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="dc720-2131">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2132">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2132">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2133">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2133">Checksum</span></span>

<span data-ttu-id="dc720-2134">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2134">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2135">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2135">Definition</span></span>

<span data-ttu-id="dc720-2136">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2136">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2137">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2137">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2138">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="dc720-2138">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="dc720-2139">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2139">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2140">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2140">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2141">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="dc720-2141">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="dc720-2142">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2142">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2143">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2143">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2144">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="dc720-2144">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2145">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2145">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="dc720-2146">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="dc720-2146">Keyword_ipaddress</span></span>

- <span data-ttu-id="dc720-2147">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-2147">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="dc720-2148">ip address
</span><span class="sxs-lookup"><span data-stu-id="dc720-2148">ip address</span></span> 
- <span data-ttu-id="dc720-2149">ip addresses</span><span class="sxs-lookup"><span data-stu-id="dc720-2149">ip addresses</span></span>
- <span data-ttu-id="dc720-2150">internet protocol</span><span class="sxs-lookup"><span data-stu-id="dc720-2150">internet protocol</span></span>
- <span data-ttu-id="dc720-2151">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="dc720-2151">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="dc720-2152">Международные классификации болезней (ICD 10 см)</span><span class="sxs-lookup"><span data-stu-id="dc720-2152">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2153">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2153">Format</span></span>

<span data-ttu-id="dc720-2154">Словарь</span><span class="sxs-lookup"><span data-stu-id="dc720-2154">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2155">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2155">Pattern</span></span>

<span data-ttu-id="dc720-2156">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="dc720-2156">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2157">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2157">Checksum</span></span>

<span data-ttu-id="dc720-2158">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2158">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2159">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2159">Definition</span></span>

<span data-ttu-id="dc720-2160">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2160">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2161">Ключевое слово из Dictionary_icd_10_cm найти.</span><span class="sxs-lookup"><span data-stu-id="dc720-2161">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="dc720-2162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2162">Keywords</span></span>

<span data-ttu-id="dc720-p135">Любой терминов из словаря Dictionary_icd_10_cm ключевое слово, которого выполняется на основе [International классификации болезней, версия одной десятой, клинических изменения (ICD 10 см)](https://go.microsoft.com/fwlink/?linkid=852604). Этот тип только поиск терминов, не страхования коды.</span><span class="sxs-lookup"><span data-stu-id="dc720-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="dc720-2165">Международные классификации болезней (ICD 9 CM)</span><span class="sxs-lookup"><span data-stu-id="dc720-2165">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2166">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2166">Format</span></span>

<span data-ttu-id="dc720-2167">Словарь</span><span class="sxs-lookup"><span data-stu-id="dc720-2167">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2168">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2168">Pattern</span></span>

<span data-ttu-id="dc720-2169">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="dc720-2169">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2170">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2170">Checksum</span></span>

<span data-ttu-id="dc720-2171">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2172">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2172">Definition</span></span>

<span data-ttu-id="dc720-2173">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2173">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2174">Ключевое слово из Dictionary_icd_9_cm найти.</span><span class="sxs-lookup"><span data-stu-id="dc720-2174">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2175">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2175">Keywords</span></span>

<span data-ttu-id="dc720-p136">Любой терминов из словаря Dictionary_icd_9_cm ключевое слово, которого выполняется на основе [International классификации болезней, Revision девятая, клинических изменения (ICD 9 см)](https://go.microsoft.com/fwlink/?linkid=852605). Этот тип только поиск терминов, не страхования коды.</span><span class="sxs-lookup"><span data-stu-id="dc720-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="dc720-2178">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="dc720-2178">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2179">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2179">Format</span></span>

<span data-ttu-id="dc720-2180">Использован старый формат (до 31 декабря 2012 г.):</span><span class="sxs-lookup"><span data-stu-id="dc720-2180">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="dc720-2181">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="dc720-2181">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="dc720-2182">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="dc720-2182">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="dc720-2183">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="dc720-2183">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2184">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2184">Pattern</span></span>

<span data-ttu-id="dc720-2185">Использован старый формат (до 31 декабря 2012 г.):</span><span class="sxs-lookup"><span data-stu-id="dc720-2185">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="dc720-2186">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-2186">Seven digits</span></span> 
- <span data-ttu-id="dc720-2187">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="dc720-2187">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="dc720-2188">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="dc720-2188">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="dc720-2189">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-2189">Seven digits</span></span> 
- <span data-ttu-id="dc720-2190">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="dc720-2190">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="dc720-2191">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="dc720-2191">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2192">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2192">Checksum</span></span>

<span data-ttu-id="dc720-2193">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2194">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2194">Definition</span></span>

<span data-ttu-id="dc720-2195">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2196">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-2196">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2197">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-2197">One of the following is true:</span></span>
    - <span data-ttu-id="dc720-2198">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="dc720-2198">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="dc720-2199">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-2199">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="dc720-2200">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2200">The checksum passes.</span></span>

<span data-ttu-id="dc720-2201">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2201">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2202">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2202">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2203">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2203">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2204">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2204">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="dc720-2205">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="dc720-2205">Keyword_ireland_pps</span></span>

- <span data-ttu-id="dc720-2206">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="dc720-2206">Personal Public Service Number</span></span> 
- <span data-ttu-id="dc720-2207">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2207">PPS Number</span></span> 
- <span data-ttu-id="dc720-2208">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="dc720-2208">PPS Num</span></span> 
- <span data-ttu-id="dc720-2209">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2209">PPS No.</span></span> 
- <span data-ttu-id="dc720-2210">PPS #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2210">PPS #</span></span> 
- <span data-ttu-id="dc720-2211">PPS #</span><span class="sxs-lookup"><span data-stu-id="dc720-2211">PPS#</span></span> 
- <span data-ttu-id="dc720-2212">PPSN
</span><span class="sxs-lookup"><span data-stu-id="dc720-2212">PPSN</span></span> 
- <span data-ttu-id="dc720-2213">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-2213">Public Services Card</span></span> 
- <span data-ttu-id="dc720-2214">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="dc720-2214">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="dc720-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="dc720-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="dc720-2217">PSP
</span><span class="sxs-lookup"><span data-stu-id="dc720-2217">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="dc720-2218">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="dc720-2218">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2219">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2219">Format</span></span>

<span data-ttu-id="dc720-2220">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2220">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2221">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2221">Pattern</span></span>

<span data-ttu-id="dc720-2222">С форматированием</span><span class="sxs-lookup"><span data-stu-id="dc720-2222">Formatted:</span></span>
- <span data-ttu-id="dc720-2223">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2223">Two digits</span></span> 
- <span data-ttu-id="dc720-2224">Тире</span><span class="sxs-lookup"><span data-stu-id="dc720-2224">A dash</span></span> 
- <span data-ttu-id="dc720-2225">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2225">Three digits</span></span> 
- <span data-ttu-id="dc720-2226">Тире</span><span class="sxs-lookup"><span data-stu-id="dc720-2226">A dash</span></span> 
- <span data-ttu-id="dc720-2227">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2227">Eight digits</span></span>

<span data-ttu-id="dc720-2228">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="dc720-2228">Unformatted:</span></span>
- <span data-ttu-id="dc720-2229">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2229">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2230">Checksum</span></span>

<span data-ttu-id="dc720-2231">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2232">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2232">Definition</span></span>

<span data-ttu-id="dc720-2233">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2234">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2234">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2235">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-2235">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2236">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2236">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="dc720-2237">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2237">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="dc720-2238">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2238">Bank Account Number</span></span> 
- <span data-ttu-id="dc720-2239">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="dc720-2239">Bank Account</span></span> 
- <span data-ttu-id="dc720-2240">Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2240">Account Number</span></span> 
- <span data-ttu-id="dc720-2241">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="dc720-2241">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="dc720-2242">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="dc720-2242">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2243">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2243">Format</span></span>

<span data-ttu-id="dc720-2244">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2245">Pattern</span></span>

<span data-ttu-id="dc720-2246">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2247">Checksum</span></span>

<span data-ttu-id="dc720-2248">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2248">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2249">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2249">Definition</span></span>

<span data-ttu-id="dc720-2250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2251">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2251">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2252">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="dc720-2252">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="dc720-2253">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2253">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2254">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2254">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="dc720-2255">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="dc720-2255">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="dc720-2256">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="dc720-2256">מספר זהות</span></span> 
- <span data-ttu-id="dc720-2257">National ID Number</span><span class="sxs-lookup"><span data-stu-id="dc720-2257">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="dc720-2258">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="dc720-2258">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2259">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2259">Format</span></span>

<span data-ttu-id="dc720-2260">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2260">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2261">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2261">Pattern</span></span>

- <span data-ttu-id="dc720-2262">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2262">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="dc720-2263">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-2263">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2264">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-2264">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2265">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="dc720-2265">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="dc720-2266">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-2266">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2267">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2267">Checksum</span></span>

<span data-ttu-id="dc720-2268">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2269">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2269">Definition</span></span>

<span data-ttu-id="dc720-2270">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2271">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2271">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2272">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-2272">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2273">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2273">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="dc720-2274">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2274">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="dc720-2275">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="dc720-2275">numero di patente di guida</span></span> 
- <span data-ttu-id="dc720-2276">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="dc720-2276">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="dc720-2277">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="dc720-2277">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2278">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2278">Format</span></span>

<span data-ttu-id="dc720-2279">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2279">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2280">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2280">Pattern</span></span>

<span data-ttu-id="dc720-2281">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="dc720-2281">Bank account number:</span></span>
- <span data-ttu-id="dc720-2282">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2282">Seven or eight digits</span></span>
- <span data-ttu-id="dc720-2283">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="dc720-2283">Bank account branch code:</span></span>
- <span data-ttu-id="dc720-2284">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2284">Four digits</span></span> 
- <span data-ttu-id="dc720-2285">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2285">A space or dash (optional)</span></span> 
- <span data-ttu-id="dc720-2286">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2286">Three digits</span></span>

<span data-ttu-id="dc720-2287">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2287">Checksum</span></span>

<span data-ttu-id="dc720-2288">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2288">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2289">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2289">Definition</span></span>

<span data-ttu-id="dc720-2290">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2290">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2291">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-2291">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2292">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="dc720-2292">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="dc720-2293">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-2293">One of the following is true:</span></span>
- <span data-ttu-id="dc720-2294">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2294">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2295">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="dc720-2295">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="dc720-2296">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2296">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2297">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2297">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2298">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="dc720-2298">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2299">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2299">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="dc720-2300">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="dc720-2300">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="dc720-2301">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2301">Checking Account Number</span></span> 
- <span data-ttu-id="dc720-2302">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="dc720-2302">Checking Account</span></span> 
- <span data-ttu-id="dc720-2303">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2303">Checking Account #</span></span> 
- <span data-ttu-id="dc720-2304">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2304">Checking Acct Number</span></span> 
- <span data-ttu-id="dc720-2305">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2305">Checking Acct #</span></span> 
- <span data-ttu-id="dc720-2306">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2306">Checking Acct No.</span></span> 
- <span data-ttu-id="dc720-2307">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2307">Checking Account No.</span></span> 
- <span data-ttu-id="dc720-2308">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2308">Bank Account Number</span></span> 
- <span data-ttu-id="dc720-2309">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="dc720-2309">Bank Account</span></span> 
- <span data-ttu-id="dc720-2310">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2310">Bank Account #</span></span> 
- <span data-ttu-id="dc720-2311">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2311">Bank Acct Number</span></span> 
- <span data-ttu-id="dc720-2312">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2312">Bank Acct #</span></span> 
- <span data-ttu-id="dc720-2313">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2313">Bank Acct No.</span></span> 
- <span data-ttu-id="dc720-2314">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2314">Bank Account No.</span></span> 
- <span data-ttu-id="dc720-2315">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2315">Savings Account Number</span></span> 
- <span data-ttu-id="dc720-2316">Учетная запись экономии</span><span class="sxs-lookup"><span data-stu-id="dc720-2316">Savings Account</span></span> 
- <span data-ttu-id="dc720-2317">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2317">Savings Account #</span></span> 
- <span data-ttu-id="dc720-2318">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2318">Savings Acct Number</span></span> 
- <span data-ttu-id="dc720-2319">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2319">Savings Acct #</span></span> 
- <span data-ttu-id="dc720-2320">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2320">Savings Acct No.</span></span> 
- <span data-ttu-id="dc720-2321">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2321">Savings Account No.</span></span> 
- <span data-ttu-id="dc720-2322">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2322">Debit Account Number</span></span> 
- <span data-ttu-id="dc720-2323">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="dc720-2323">Debit Account</span></span> 
- <span data-ttu-id="dc720-2324">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2324">Debit Account #</span></span> 
- <span data-ttu-id="dc720-2325">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2325">Debit Acct Number</span></span> 
- <span data-ttu-id="dc720-2326">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2326">Debit Acct #</span></span> 
- <span data-ttu-id="dc720-2327">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2327">Debit Acct No.</span></span> 
- <span data-ttu-id="dc720-2328">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2328">Debit Account No.</span></span> 
- <span data-ttu-id="dc720-2329">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="dc720-2329">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="dc720-2330">＃アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="dc720-2330">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="dc720-2331">＃勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="dc720-2331">＃勘定の確認</span></span> 
- <span data-ttu-id="dc720-2332">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="dc720-2332">勘定番号の確認</span></span> 
- <span data-ttu-id="dc720-2333">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="dc720-2333">口座番号の確認</span></span> 
- <span data-ttu-id="dc720-2334">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="dc720-2334">銀行口座番号</span></span> 
- <span data-ttu-id="dc720-2335">銀行口座</span><span class="sxs-lookup"><span data-stu-id="dc720-2335">銀行口座</span></span> 
- <span data-ttu-id="dc720-2336">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2336">銀行口座＃</span></span> 
- <span data-ttu-id="dc720-2337">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2337">銀行の勘定番号</span></span> 
- <span data-ttu-id="dc720-2338">銀行のacct＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2338">銀行のacct＃</span></span> 
- <span data-ttu-id="dc720-2339">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="dc720-2339">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="dc720-2340">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="dc720-2340">銀行口座番号</span></span>
- <span data-ttu-id="dc720-2341">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2341">普通預金口座番号</span></span> 
- <span data-ttu-id="dc720-2342">預金口座
</span><span class="sxs-lookup"><span data-stu-id="dc720-2342">預金口座</span></span> 
- <span data-ttu-id="dc720-2343">貯蓄口座＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2343">貯蓄口座＃</span></span> 
- <span data-ttu-id="dc720-2344">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="dc720-2344">貯蓄勘定の数</span></span> 
- <span data-ttu-id="dc720-2345">貯蓄勘定＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2345">貯蓄勘定＃</span></span> 
- <span data-ttu-id="dc720-2346">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2346">貯蓄勘定番号</span></span> 
- <span data-ttu-id="dc720-2347">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2347">普通預金口座番号</span></span> 
- <span data-ttu-id="dc720-2348">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2348">引き落とし口座番号</span></span> 
- <span data-ttu-id="dc720-2349">口座番号</span><span class="sxs-lookup"><span data-stu-id="dc720-2349">口座番号</span></span> 
- <span data-ttu-id="dc720-2350">口座番号＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2350">口座番号＃</span></span> 
- <span data-ttu-id="dc720-2351">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2351">デビットのacct番号</span></span> 
- <span data-ttu-id="dc720-2352">デビット勘定＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2352">デビット勘定＃</span></span> 
- <span data-ttu-id="dc720-2353">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2353">デビットACCTの番号</span></span> 
- <span data-ttu-id="dc720-2354">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2354">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="dc720-2355">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="dc720-2355">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="dc720-2356">Otemachi</span><span class="sxs-lookup"><span data-stu-id="dc720-2356">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="dc720-2357">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="dc720-2357">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2358">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2358">Format</span></span>

<span data-ttu-id="dc720-2359">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2359">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2360">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2360">Pattern</span></span>

<span data-ttu-id="dc720-2361">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2361">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2362">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2362">Checksum</span></span>

<span data-ttu-id="dc720-2363">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2363">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2364">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2364">Definition</span></span>

<span data-ttu-id="dc720-2365">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2365">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2366">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2366">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2367">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-2367">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2368">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2368">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="dc720-2369">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2369">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="dc720-2370">dl#</span><span class="sxs-lookup"><span data-stu-id="dc720-2370">dl#</span></span> 
- <span data-ttu-id="dc720-2371">СПИСОК РАССЫЛКИ #</span><span class="sxs-lookup"><span data-stu-id="dc720-2371">DL＃</span></span> 
- <span data-ttu-id="dc720-2372">dls#</span><span class="sxs-lookup"><span data-stu-id="dc720-2372">dls#</span></span> 
- <span data-ttu-id="dc720-2373">СПИСКИ РАССЫЛКИ #</span><span class="sxs-lookup"><span data-stu-id="dc720-2373">DLS＃</span></span> 
- <span data-ttu-id="dc720-2374">driver license</span><span class="sxs-lookup"><span data-stu-id="dc720-2374">driver license</span></span> 
- <span data-ttu-id="dc720-2375">driver licenses</span><span class="sxs-lookup"><span data-stu-id="dc720-2375">driver licenses</span></span> 
- <span data-ttu-id="dc720-2376">drivers license</span><span class="sxs-lookup"><span data-stu-id="dc720-2376">drivers license</span></span> 
- <span data-ttu-id="dc720-2377">driver's license</span><span class="sxs-lookup"><span data-stu-id="dc720-2377">driver's license</span></span> 
- <span data-ttu-id="dc720-2378">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="dc720-2378">drivers licenses</span></span> 
- <span data-ttu-id="dc720-2379">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="dc720-2379">driver's licenses</span></span> 
- <span data-ttu-id="dc720-2380">driving licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-2380">driving licence</span></span> 
- <span data-ttu-id="dc720-2381">lic#</span><span class="sxs-lookup"><span data-stu-id="dc720-2381">lic#</span></span> 
- <span data-ttu-id="dc720-2382">LIC #</span><span class="sxs-lookup"><span data-stu-id="dc720-2382">LIC＃</span></span> 
- <span data-ttu-id="dc720-2383">lics#</span><span class="sxs-lookup"><span data-stu-id="dc720-2383">lics#</span></span> 
- <span data-ttu-id="dc720-2384">Код состояния</span><span class="sxs-lookup"><span data-stu-id="dc720-2384">state id</span></span> 
- <span data-ttu-id="dc720-2385">state identification
</span><span class="sxs-lookup"><span data-stu-id="dc720-2385">state identification</span></span> 
- <span data-ttu-id="dc720-2386">state identification number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2386">state identification number</span></span> 
- <span data-ttu-id="dc720-2387">低所得国＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2387">低所得国＃</span></span> 
- <span data-ttu-id="dc720-2388">免許証</span><span class="sxs-lookup"><span data-stu-id="dc720-2388">免許証</span></span> 
- <span data-ttu-id="dc720-2389">状態ID</span><span class="sxs-lookup"><span data-stu-id="dc720-2389">状態ID</span></span>
- <span data-ttu-id="dc720-2390">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="dc720-2390">状態の識別</span></span> 
- <span data-ttu-id="dc720-2391">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2391">状態の識別番号</span></span> 
- <span data-ttu-id="dc720-2392">運転免許</span><span class="sxs-lookup"><span data-stu-id="dc720-2392">運転免許</span></span> 
- <span data-ttu-id="dc720-2393">運転免許証</span><span class="sxs-lookup"><span data-stu-id="dc720-2393">運転免許証</span></span> 
- <span data-ttu-id="dc720-2394">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="dc720-2394">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="dc720-2395">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="dc720-2395">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2396">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2396">Format</span></span>

<span data-ttu-id="dc720-2397">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2397">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2398">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2398">Pattern</span></span>

<span data-ttu-id="dc720-2399">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2399">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2400">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2400">Checksum</span></span>

<span data-ttu-id="dc720-2401">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2401">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2402">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2402">Definition</span></span>

<span data-ttu-id="dc720-2403">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2403">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2404">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2404">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2405">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="dc720-2405">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2406">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2406">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="dc720-2407">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-2407">Keyword_jp_passport</span></span>

- <span data-ttu-id="dc720-2408">パスポート
</span><span class="sxs-lookup"><span data-stu-id="dc720-2408">パスポート</span></span> 
- <span data-ttu-id="dc720-2409">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2409">パスポート番号</span></span> 
- <span data-ttu-id="dc720-2410">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="dc720-2410">パスポートのNum</span></span> 
- <span data-ttu-id="dc720-2411">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2411">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="dc720-2412">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="dc720-2412">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2413">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2413">Format</span></span>

<span data-ttu-id="dc720-2414">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="dc720-2414">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2415">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2415">Pattern</span></span>

<span data-ttu-id="dc720-2416">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2416">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2417">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2417">Checksum</span></span>

<span data-ttu-id="dc720-2418">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2418">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2419">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2419">Definition</span></span>

<span data-ttu-id="dc720-2420">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2420">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2421">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2421">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2422">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-2422">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2423">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2423">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="dc720-2424">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2424">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="dc720-2425">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="dc720-2425">Resident Registration Number</span></span>
- <span data-ttu-id="dc720-2426">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2426">Resident Register Number</span></span> 
- <span data-ttu-id="dc720-2427">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2427">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="dc720-2428">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2428">Resident Registration No.</span></span> 
- <span data-ttu-id="dc720-2429">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2429">Resident Register No.</span></span> 
- <span data-ttu-id="dc720-2430">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2430">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="dc720-2431">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2431">Basic Resident Register No.</span></span> 
- <span data-ttu-id="dc720-2432">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="dc720-2432">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="dc720-2433">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2433">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="dc720-2434">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="dc720-2434">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="dc720-2435">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2435">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="dc720-2436">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2436">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2437">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2437">Format</span></span>

<span data-ttu-id="dc720-2438">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2438">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2439">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2439">Pattern</span></span>

<span data-ttu-id="dc720-2440">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2440">7-12 digits:</span></span>
- <span data-ttu-id="dc720-2441">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2441">Four digits</span></span> 
- <span data-ttu-id="dc720-2442">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2442">A hyphen (optional)</span></span> 
- <span data-ttu-id="dc720-2443">Шести цифр или</span><span class="sxs-lookup"><span data-stu-id="dc720-2443">Six digits OR</span></span>
- <span data-ttu-id="dc720-2444">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2444">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2445">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2445">Checksum</span></span>

<span data-ttu-id="dc720-2446">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2446">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2447">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2447">Definition</span></span>

<span data-ttu-id="dc720-2448">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2448">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2449">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2449">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2450">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="dc720-2450">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="dc720-2451">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2451">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2452">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2452">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2453">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="dc720-2453">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2454">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2454">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="dc720-2455">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="dc720-2455">Keyword_jp_sin</span></span>

- <span data-ttu-id="dc720-2456">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2456">Social Insurance No.</span></span> 
- <span data-ttu-id="dc720-2457">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="dc720-2457">Social Insurance Num</span></span> 
- <span data-ttu-id="dc720-2458">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2458">Social Insurance Number</span></span> 
- <span data-ttu-id="dc720-2459">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="dc720-2459">社会保険のテンキー</span></span> 
- <span data-ttu-id="dc720-2460">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2460">社会保険番号</span></span> 
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="dc720-2461">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="dc720-2461">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2462">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2462">Format</span></span>

<span data-ttu-id="dc720-2463">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="dc720-2463">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2464">Pattern</span></span>

<span data-ttu-id="dc720-2465">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2465">12 digits:</span></span>
- <span data-ttu-id="dc720-2466">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="dc720-2466">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="dc720-2467">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="dc720-2467">A dash (optional)</span></span> 
- <span data-ttu-id="dc720-2468">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="dc720-2468">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="dc720-2469">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="dc720-2469">A dash (optional)</span></span> 
- <span data-ttu-id="dc720-2470">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="dc720-2470">Three random digits</span></span> 
- <span data-ttu-id="dc720-2471">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2471">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2472">Checksum</span></span>

<span data-ttu-id="dc720-2473">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2474">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2474">Definition</span></span>

<span data-ttu-id="dc720-2475">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2476">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2476">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2477">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="dc720-2477">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2478">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2478">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="dc720-2479">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2479">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="dc720-2480">MyKad</span><span class="sxs-lookup"><span data-stu-id="dc720-2480">MyKad</span></span> 
- <span data-ttu-id="dc720-2481">Identity Card</span><span class="sxs-lookup"><span data-stu-id="dc720-2481">Identity Card</span></span> 
- <span data-ttu-id="dc720-2482">Карточка</span><span class="sxs-lookup"><span data-stu-id="dc720-2482">ID Card</span></span> 
- <span data-ttu-id="dc720-2483">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="dc720-2483">Identification Card</span></span> 
- <span data-ttu-id="dc720-2484">Digital Application Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-2484">Digital Application Card</span></span> 
- <span data-ttu-id="dc720-2485">Kad Akuan Diri
</span><span class="sxs-lookup"><span data-stu-id="dc720-2485">Kad Akuan Diri</span></span> 
- <span data-ttu-id="dc720-2486">Kad Aplikasi Digital
</span><span class="sxs-lookup"><span data-stu-id="dc720-2486">Kad Aplikasi Digital</span></span> 
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="dc720-2487">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2487">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2488">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2488">Format</span></span>

<span data-ttu-id="dc720-2489">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="dc720-2489">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2490">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2490">Pattern</span></span>

<span data-ttu-id="dc720-2491">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2491">8-9 digits:</span></span>
- <span data-ttu-id="dc720-2492">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2492">Three digits</span></span> 
- <span data-ttu-id="dc720-2493">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="dc720-2493">A space (optional)</span></span> 
- <span data-ttu-id="dc720-2494">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2494">Three digits</span></span> 
- <span data-ttu-id="dc720-2495">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="dc720-2495">A space (optional)</span></span> 
- <span data-ttu-id="dc720-2496">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2496">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2497">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2497">Checksum</span></span>

<span data-ttu-id="dc720-2498">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2498">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2499">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2499">Definition</span></span>

<span data-ttu-id="dc720-2500">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2500">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2501">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2501">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2502">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="dc720-2502">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="dc720-2503">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-2503">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="dc720-2504">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2504">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2505">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2505">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="dc720-2506">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="dc720-2506">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="dc720-2507">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2507">Citizen service number</span></span> 
- <span data-ttu-id="dc720-2508">BSN

</span><span class="sxs-lookup"><span data-stu-id="dc720-2508">BSN</span></span> 
- <span data-ttu-id="dc720-2509">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-2509">Burgerservicenummer</span></span> 
- <span data-ttu-id="dc720-2510">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-2510">Sofinummer</span></span> 
- <span data-ttu-id="dc720-2511">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-2511">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="dc720-2512">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="dc720-2512">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="dc720-2513">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="dc720-2513">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2514">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2514">Format</span></span>

<span data-ttu-id="dc720-2515">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2515">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2516">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2516">Pattern</span></span>

<span data-ttu-id="dc720-2517">Три буквы (не регистр) четырех цифр пространства (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2517">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2518">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2518">Checksum</span></span>

<span data-ttu-id="dc720-2519">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2519">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2520">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2520">Definition</span></span>

<span data-ttu-id="dc720-2521">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2521">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2522">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2522">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2523">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="dc720-2523">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="dc720-2524">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2524">The checksum passes.</span></span>

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

<span data-ttu-id="dc720-2525">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2525">Keywords</span></span>

<span data-ttu-id="dc720-2526">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="dc720-2526">Keyword_nz_terms</span></span>

- <span data-ttu-id="dc720-2527">NHI
</span><span class="sxs-lookup"><span data-stu-id="dc720-2527">NHI</span></span> 
- <span data-ttu-id="dc720-2528">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="dc720-2528">New Zealand</span></span> 
- <span data-ttu-id="dc720-2529">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="dc720-2529">Health</span></span> 
- <span data-ttu-id="dc720-2530">treatment
</span><span class="sxs-lookup"><span data-stu-id="dc720-2530">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="dc720-2531">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="dc720-2531">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2532">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2532">Format</span></span>

<span data-ttu-id="dc720-2533">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="dc720-2533">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2534">Pattern</span></span>

<span data-ttu-id="dc720-2535">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2535">11 digits:</span></span>
- <span data-ttu-id="dc720-2536">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="dc720-2536">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="dc720-2537">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-2537">Three-digit individual number</span></span> 
- <span data-ttu-id="dc720-2538">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2538">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2539">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2539">Checksum</span></span>

<span data-ttu-id="dc720-2540">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2540">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2541">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2541">Definition</span></span>

<span data-ttu-id="dc720-2542">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2542">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2543">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2543">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2544">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-2544">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="dc720-2545">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2545">The checksum passes.</span></span>
- <span data-ttu-id="dc720-2546">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2546">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2547">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2547">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2548">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2548">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2549">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2549">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="dc720-2550">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2550">Keyword_norway_id_number</span></span>

- <span data-ttu-id="dc720-2551">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="dc720-2551">Personal identification number</span></span>
- <span data-ttu-id="dc720-2552">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="dc720-2552">Norwegian ID Number</span></span>
- <span data-ttu-id="dc720-2553">ID Number</span><span class="sxs-lookup"><span data-stu-id="dc720-2553">ID Number</span></span>
- <span data-ttu-id="dc720-2554">Identification</span><span class="sxs-lookup"><span data-stu-id="dc720-2554">Identification</span></span>
- <span data-ttu-id="dc720-2555">Personnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-2555">Personnummer</span></span>
- <span data-ttu-id="dc720-2556">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="dc720-2556">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="dc720-2557">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="dc720-2557">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2558">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2558">Format</span></span>

<span data-ttu-id="dc720-2559">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="dc720-2559">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2560">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2560">Pattern</span></span>

<span data-ttu-id="dc720-2561">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2561">12 digits:</span></span>
- <span data-ttu-id="dc720-2562">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2562">Four digits</span></span> 
- <span data-ttu-id="dc720-2563">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-2563">A hyphen</span></span> 
- <span data-ttu-id="dc720-2564">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-2564">Seven digits</span></span> 
- <span data-ttu-id="dc720-2565">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-2565">A hyphen</span></span> 
- <span data-ttu-id="dc720-2566">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dc720-2566">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2567">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2567">Checksum</span></span>

<span data-ttu-id="dc720-2568">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2568">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2569">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2569">Definition</span></span>

<span data-ttu-id="dc720-2570">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2571">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2571">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2572">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="dc720-2572">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2573">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2573">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="dc720-2574">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="dc720-2574">Keyword_philippines_id</span></span>

- <span data-ttu-id="dc720-2575">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="dc720-2575">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="dc720-2576">UMID
</span><span class="sxs-lookup"><span data-stu-id="dc720-2576">UMID</span></span> 
- <span data-ttu-id="dc720-2577">Identity Card</span><span class="sxs-lookup"><span data-stu-id="dc720-2577">Identity Card</span></span> 
- <span data-ttu-id="dc720-2578">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="dc720-2578">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="dc720-2579">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="dc720-2579">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2580">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2580">Format</span></span>

<span data-ttu-id="dc720-2581">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2581">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2582">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2582">Pattern</span></span>

<span data-ttu-id="dc720-2583">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2583">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2584">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2584">Checksum</span></span>

<span data-ttu-id="dc720-2585">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2586">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2586">Definition</span></span>

<span data-ttu-id="dc720-p138">Политики защиты от потери данных — 75% уверены в том, что этот тип конфиденциальных данных обнаружил if в рамках близости 300 знаков: Func_polish_national_id поиска контента, который соответствует шаблону. Ключевое слово из Keyword_polish_national_id_passport_number найти. Контрольная сумма передает.</span><span class="sxs-lookup"><span data-stu-id="dc720-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2590">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2590">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="dc720-2591">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2591">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="dc720-2592">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="dc720-2592">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="dc720-2593">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="dc720-2593">Dowód Tożsamości</span></span> 
- <span data-ttu-id="dc720-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="dc720-p139">dow. os.</span></span> 

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="dc720-2596">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="dc720-2596">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2597">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2597">Format</span></span>

<span data-ttu-id="dc720-2598">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="dc720-2598">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2599">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2599">Pattern</span></span>

<span data-ttu-id="dc720-2600">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2600">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2601">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2601">Checksum</span></span>

<span data-ttu-id="dc720-2602">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2602">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2603">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2603">Definition</span></span>

<span data-ttu-id="dc720-2604">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2604">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2605">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2605">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2606">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-2606">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="dc720-2607">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2607">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2608">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2608">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="dc720-2609">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2609">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="dc720-2610">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="dc720-2610">Nr PESEL</span></span>
- <span data-ttu-id="dc720-2611">PESEL</span><span class="sxs-lookup"><span data-stu-id="dc720-2611">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="dc720-2612">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="dc720-2612">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2613">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2613">Format</span></span>

<span data-ttu-id="dc720-2614">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2614">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2615">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2615">Pattern</span></span>

<span data-ttu-id="dc720-2616">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2616">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2617">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2617">Checksum</span></span>

<span data-ttu-id="dc720-2618">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2618">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2619">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2619">Definition</span></span>

<span data-ttu-id="dc720-2620">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2620">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2621">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2621">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2622">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-2622">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="dc720-2623">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2623">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2624">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2624">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="dc720-2625">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2625">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="dc720-2626">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="dc720-2626">Nazwa i nr dowodu tożsamości</span></span> 
- <span data-ttu-id="dc720-2627">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="dc720-2627">Dowód Tożsamości</span></span> 
- <span data-ttu-id="dc720-p140">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="dc720-p140">dow. os.</span></span> 

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="dc720-2630">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="dc720-2630">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2631">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2631">Format</span></span>

<span data-ttu-id="dc720-2632">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2632">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2633">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2633">Pattern</span></span>

<span data-ttu-id="dc720-2634">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2634">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2635">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2635">Checksum</span></span>

<span data-ttu-id="dc720-2636">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2636">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2637">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2637">Definition</span></span>

<span data-ttu-id="dc720-2638">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2638">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2639">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2639">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2640">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="dc720-2640">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2641">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2641">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="dc720-2642">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="dc720-2642">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="dc720-2643">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="dc720-2643">Citizen Card</span></span>
- <span data-ttu-id="dc720-2644">National ID Card</span><span class="sxs-lookup"><span data-stu-id="dc720-2644">National ID Card</span></span>
- <span data-ttu-id="dc720-2645">CC</span><span class="sxs-lookup"><span data-stu-id="dc720-2645">CC</span></span>
- <span data-ttu-id="dc720-2646">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="dc720-2646">Cartão de Cidadão</span></span>
- <span data-ttu-id="dc720-2647">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="dc720-2647">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="dc720-2648">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="dc720-2648">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2649">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2649">Format</span></span>

<span data-ttu-id="dc720-2650">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2650">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2651">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2651">Pattern</span></span>

<span data-ttu-id="dc720-2652">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2652">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2653">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2653">Checksum</span></span>

<span data-ttu-id="dc720-2654">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2654">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2655">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2655">Definition</span></span>

<span data-ttu-id="dc720-2656">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2656">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2657">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2657">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2658">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="dc720-2658">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2659">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2659">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="dc720-2660">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="dc720-2660">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="dc720-2661">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-2661">Identification Card</span></span> 
- <span data-ttu-id="dc720-2662">I card number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2662">I card number</span></span> 
- <span data-ttu-id="dc720-2663">идентификатор</span><span class="sxs-lookup"><span data-stu-id="dc720-2663">ID number</span></span> 
- <span data-ttu-id="dc720-2664">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="dc720-2664">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="dc720-2665">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="dc720-2665">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2666">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2666">Format</span></span>

<span data-ttu-id="dc720-2667">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2667">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2668">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2668">Pattern</span></span>

- <span data-ttu-id="dc720-2669">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2669">Nine letters and digits:</span></span>
- <span data-ttu-id="dc720-2670">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="dc720-2670">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2671">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-2671">Seven digits</span></span> 
- <span data-ttu-id="dc720-2672">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="dc720-2672">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2673">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2673">Checksum</span></span>

<span data-ttu-id="dc720-2674">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2674">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2675">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2675">Definition</span></span>

<span data-ttu-id="dc720-2676">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2676">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2677">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2677">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2678">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="dc720-2678">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="dc720-2679">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2679">The checksum passes.</span></span>

<span data-ttu-id="dc720-2680">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2681">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2681">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2682">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2682">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2683">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2683">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="dc720-2684">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="dc720-2684">Keyword_singapore_nric</span></span>

- <span data-ttu-id="dc720-2685">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-2685">National Registration Identity Card</span></span> 
- <span data-ttu-id="dc720-2686">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2686">Identity Card Number</span></span> 
- <span data-ttu-id="dc720-2687">NRIC
</span><span class="sxs-lookup"><span data-stu-id="dc720-2687">NRIC</span></span> 
- <span data-ttu-id="dc720-2688">IC
</span><span class="sxs-lookup"><span data-stu-id="dc720-2688">IC</span></span> 
- <span data-ttu-id="dc720-2689">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2689">Foreign Identification Number</span></span> 
- <span data-ttu-id="dc720-2690">FIN
</span><span class="sxs-lookup"><span data-stu-id="dc720-2690">FIN</span></span> 
- <span data-ttu-id="dc720-2691">身份证 </span><span class="sxs-lookup"><span data-stu-id="dc720-2691">身份证</span></span> 
- <span data-ttu-id="dc720-2692">身份證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2692">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="dc720-2693">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="dc720-2693">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2694">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2694">Format</span></span>

<span data-ttu-id="dc720-2695">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="dc720-2695">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2696">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2696">Pattern</span></span>

<span data-ttu-id="dc720-2697">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2697">13 digits:</span></span>
- <span data-ttu-id="dc720-2698">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="dc720-2698">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="dc720-2699">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2699">Four digits</span></span> 
- <span data-ttu-id="dc720-2700">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="dc720-2700">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="dc720-2701">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="dc720-2701">The digit "8" or "9"</span></span> 
- <span data-ttu-id="dc720-2702">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="dc720-2702">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2703">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2703">Checksum</span></span>

<span data-ttu-id="dc720-2704">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2704">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2705">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2705">Definition</span></span>

<span data-ttu-id="dc720-2706">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2706">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2707">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2707">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2708">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-2708">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="dc720-2709">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2709">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2710">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2710">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="dc720-2711">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2711">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="dc720-2712">Identity card</span><span class="sxs-lookup"><span data-stu-id="dc720-2712">Identity card</span></span>
- <span data-ttu-id="dc720-2713">ID</span><span class="sxs-lookup"><span data-stu-id="dc720-2713">ID</span></span>
- <span data-ttu-id="dc720-2714">Identification</span><span class="sxs-lookup"><span data-stu-id="dc720-2714">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="dc720-2715">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="dc720-2715">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2716">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2716">Format</span></span>

<span data-ttu-id="dc720-2717">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="dc720-2717">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2718">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2718">Pattern</span></span>

<span data-ttu-id="dc720-2719">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2719">13 digits:</span></span>
- <span data-ttu-id="dc720-2720">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="dc720-2720">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="dc720-2721">дефис;</span><span class="sxs-lookup"><span data-stu-id="dc720-2721">A hyphen</span></span> 
- <span data-ttu-id="dc720-2722">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="dc720-2722">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="dc720-2723">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="dc720-2723">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="dc720-2724">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="dc720-2724">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="dc720-2725">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="dc720-2725">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2726">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2726">Checksum</span></span>

<span data-ttu-id="dc720-2727">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2727">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2728">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2728">Definition</span></span>

<span data-ttu-id="dc720-2729">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2729">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2730">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2730">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2731">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-2731">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="dc720-2732">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2732">The checksum passes.</span></span>

<span data-ttu-id="dc720-2733">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2733">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2734">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2734">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2735">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2735">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2736">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2736">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="dc720-2737">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="dc720-2737">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="dc720-2738">National ID card
</span><span class="sxs-lookup"><span data-stu-id="dc720-2738">National ID card</span></span> 
- <span data-ttu-id="dc720-2739">Citizen's Registration Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2739">Citizen's Registration Number</span></span> 
- <span data-ttu-id="dc720-2740">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="dc720-2740">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="dc720-2741">RRN
</span><span class="sxs-lookup"><span data-stu-id="dc720-2741">RRN</span></span> 
- <span data-ttu-id="dc720-2742">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="dc720-2742">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="dc720-2743">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2743">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2744">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2744">Format</span></span>

<span data-ttu-id="dc720-2745">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2745">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2746">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2746">Pattern</span></span>

<span data-ttu-id="dc720-2747">цифры 11-12:</span><span class="sxs-lookup"><span data-stu-id="dc720-2747">11-12 digits:</span></span>
- <span data-ttu-id="dc720-2748">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2748">Two digits</span></span> 
- <span data-ttu-id="dc720-2749">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2749">A forward slash (optional)</span></span> 
- <span data-ttu-id="dc720-2750">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2750">7-8 digits</span></span> 
- <span data-ttu-id="dc720-2751">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2751">A forward slash (optional)</span></span> 
- <span data-ttu-id="dc720-2752">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2752">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2753">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2753">Checksum</span></span>

<span data-ttu-id="dc720-2754">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2754">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2755">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2755">Definition</span></span>

<span data-ttu-id="dc720-2756">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2757">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2757">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2758">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2758">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2759">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2759">Keywords</span></span>

<span data-ttu-id="dc720-2760">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2760">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="dc720-2761">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="dc720-2761">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2762">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2762">Format</span></span>

<span data-ttu-id="dc720-2763">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="dc720-2763">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2764">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2764">Pattern</span></span>

<span data-ttu-id="dc720-2765">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="dc720-2765">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="dc720-2766">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2766">2-4 digits (optional)</span></span> 
- <span data-ttu-id="dc720-2767">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="dc720-2767">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="dc720-2768">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="dc720-2768">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="dc720-2769">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2769">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2770">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2770">Checksum</span></span>

<span data-ttu-id="dc720-2771">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2771">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2772">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2772">Definition</span></span>

<span data-ttu-id="dc720-2773">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2773">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2774">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2774">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2775">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2775">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2776">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2776">Keywords</span></span>

<span data-ttu-id="dc720-2777">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2777">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="dc720-2778">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="dc720-2778">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2779">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2779">Format</span></span>

<span data-ttu-id="dc720-2780">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2780">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2781">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2781">Pattern</span></span>

<span data-ttu-id="dc720-2782">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2782">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2783">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2783">Checksum</span></span>

<span data-ttu-id="dc720-2784">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2784">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2785">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2785">Definition</span></span>

<span data-ttu-id="dc720-2786">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2786">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2787">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-2787">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2788">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-2788">One of the following is true:</span></span>
    - <span data-ttu-id="dc720-2789">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="dc720-2789">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="dc720-2790">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="dc720-2790">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-2791">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2791">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="dc720-2792">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-2792">Keyword_sweden_passport</span></span>

- <span data-ttu-id="dc720-2793">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="dc720-2793">visa requirements</span></span> 
- <span data-ttu-id="dc720-2794">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="dc720-2794">Alien Registration Card</span></span> 
- <span data-ttu-id="dc720-2795">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="dc720-2795">Schengen visas</span></span> 
- <span data-ttu-id="dc720-2796">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="dc720-2796">Schengen visa</span></span> 
- <span data-ttu-id="dc720-2797">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="dc720-2797">Visa Processing</span></span> 
- <span data-ttu-id="dc720-2798">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="dc720-2798">Visa Type</span></span> 
- <span data-ttu-id="dc720-2799">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="dc720-2799">Single Entry</span></span> 
- <span data-ttu-id="dc720-2800">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="dc720-2800">Multiple Entry</span></span> 
- <span data-ttu-id="dc720-2801">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="dc720-2801">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="dc720-2802">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-2802">Keyword_passport</span></span>

- <span data-ttu-id="dc720-2803">Passport Number</span><span class="sxs-lookup"><span data-stu-id="dc720-2803">Passport Number</span></span> 
- <span data-ttu-id="dc720-2804">
Passport No</span><span class="sxs-lookup"><span data-stu-id="dc720-2804">Passport No</span></span> 
- <span data-ttu-id="dc720-2805">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-2805">Passport #</span></span> 
- <span data-ttu-id="dc720-2806">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-2806">Passport#</span></span> 
- <span data-ttu-id="dc720-2807">PassportID</span><span class="sxs-lookup"><span data-stu-id="dc720-2807">PassportID</span></span> 
- <span data-ttu-id="dc720-2808">Passportno
</span><span class="sxs-lookup"><span data-stu-id="dc720-2808">Passportno</span></span> 
- <span data-ttu-id="dc720-2809">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-2809">passportnumber</span></span> 
- <span data-ttu-id="dc720-2810">パスポート</span><span class="sxs-lookup"><span data-stu-id="dc720-2810">パスポート</span></span> 
- <span data-ttu-id="dc720-2811">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2811">パスポート番号</span></span> 
- <span data-ttu-id="dc720-2812">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="dc720-2812">パスポートのNum</span></span> 
- <span data-ttu-id="dc720-2813">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2813">パスポート＃</span></span> 
- <span data-ttu-id="dc720-2814">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="dc720-2814">Numéro de passeport</span></span> 
- <span data-ttu-id="dc720-2815">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="dc720-2815">Passeport n °</span></span> 
- <span data-ttu-id="dc720-2816">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="dc720-2816">Passeport Non</span></span> 
- <span data-ttu-id="dc720-2817">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-2817">Passeport #</span></span> 
- <span data-ttu-id="dc720-2818">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-2818">Passeport#</span></span> 
- <span data-ttu-id="dc720-2819">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="dc720-2819">PasseportNon</span></span> 
- <span data-ttu-id="dc720-2820">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="dc720-2820">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="dc720-2821">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="dc720-2821">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2822">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2822">Format</span></span>

<span data-ttu-id="dc720-2823">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2823">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2824">Pattern</span></span>

<span data-ttu-id="dc720-2825">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-2825">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="dc720-2826">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-2826">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2827">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="dc720-2827">An optional space</span></span> 
- <span data-ttu-id="dc720-2828">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2828">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="dc720-2829">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="dc720-2829">An optional space</span></span> 
- <span data-ttu-id="dc720-2830">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="dc720-2830">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2831">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2831">Checksum</span></span>

<span data-ttu-id="dc720-2832">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2832">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2833">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2833">Definition</span></span>

<span data-ttu-id="dc720-2834">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2834">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2835">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2835">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2836">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="dc720-2836">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2837">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2837">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="dc720-2838">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="dc720-2838">Keyword_swift</span></span>

- <span data-ttu-id="dc720-2839">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="dc720-2839">international organization for standardization 9362</span></span> 
- <span data-ttu-id="dc720-2840">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="dc720-2840">iso 9362</span></span> 
- <span data-ttu-id="dc720-2841">iso9362</span><span class="sxs-lookup"><span data-stu-id="dc720-2841">iso9362</span></span> 
- <span data-ttu-id="dc720-2842">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="dc720-2842">swift\#</span></span> 
- <span data-ttu-id="dc720-2843">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="dc720-2843">swiftcode</span></span> 
- <span data-ttu-id="dc720-2844">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-2844">swiftnumber</span></span> 
- <span data-ttu-id="dc720-2845">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-2845">swiftroutingnumber</span></span> 
- <span data-ttu-id="dc720-2846">код SWIFT</span><span class="sxs-lookup"><span data-stu-id="dc720-2846">swift code</span></span> 
- <span data-ttu-id="dc720-2847">swift number #
</span><span class="sxs-lookup"><span data-stu-id="dc720-2847">swift number #</span></span> 
- <span data-ttu-id="dc720-2848">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2848">swift routing number</span></span> 
- <span data-ttu-id="dc720-2849">bic number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2849">bic number</span></span> 
- <span data-ttu-id="dc720-2850">bic code
</span><span class="sxs-lookup"><span data-stu-id="dc720-2850">bic code</span></span> 
- <span data-ttu-id="dc720-2851">БИК\#</span><span class="sxs-lookup"><span data-stu-id="dc720-2851">bic \#</span></span> 
- <span data-ttu-id="dc720-2852">БИК\#</span><span class="sxs-lookup"><span data-stu-id="dc720-2852">bic\#</span></span> 
- <span data-ttu-id="dc720-2853">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="dc720-2853">bank identifier code</span></span> 
- <span data-ttu-id="dc720-2854">標準化9362</span><span class="sxs-lookup"><span data-stu-id="dc720-2854">標準化9362</span></span> 
- <span data-ttu-id="dc720-2855">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-2855">迅速＃</span></span> 
- <span data-ttu-id="dc720-2856">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="dc720-2856">SWIFTコード</span></span> 
- <span data-ttu-id="dc720-2857">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2857">SWIFT番号</span></span> 
- <span data-ttu-id="dc720-2858">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2858">迅速なルーティング番号</span></span> 
- <span data-ttu-id="dc720-2859">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-2859">BIC番号</span></span> 
- <span data-ttu-id="dc720-2860">BICコード
</span><span class="sxs-lookup"><span data-stu-id="dc720-2860">BICコード</span></span> 
- <span data-ttu-id="dc720-2861">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="dc720-2861">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="dc720-2862">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="dc720-2862">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="dc720-2863">rapide\#</span><span class="sxs-lookup"><span data-stu-id="dc720-2863">rapide \#</span></span> 
- <span data-ttu-id="dc720-2864">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="dc720-2864">code SWIFT</span></span> 
- <span data-ttu-id="dc720-2865">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="dc720-2865">le numéro de swift</span></span> 
- <span data-ttu-id="dc720-2866">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="dc720-2866">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="dc720-2867">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="dc720-2867">le numéro BIC</span></span> 
- <span data-ttu-id="dc720-2868">\#БИК</span><span class="sxs-lookup"><span data-stu-id="dc720-2868">\# BIC</span></span> 
- <span data-ttu-id="dc720-2869">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="dc720-2869">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="dc720-2870">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="dc720-2870">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2871">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2871">Format</span></span>

<span data-ttu-id="dc720-2872">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2872">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2873">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2873">Pattern</span></span>

<span data-ttu-id="dc720-2874">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2874">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="dc720-2875">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-2875">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2876">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="dc720-2876">The digit "1" or "2"</span></span> 
- <span data-ttu-id="dc720-2877">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2877">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2878">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2878">Checksum</span></span>

<span data-ttu-id="dc720-2879">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2879">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2880">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2880">Definition</span></span>

<span data-ttu-id="dc720-2881">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2881">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2882">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2882">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2883">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="dc720-2883">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="dc720-2884">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2884">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2885">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2885">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="dc720-2886">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="dc720-2886">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="dc720-2887">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="dc720-2887">身份證字號</span></span> 
- <span data-ttu-id="dc720-2888">身份證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2888">身份證</span></span> 
- <span data-ttu-id="dc720-2889">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="dc720-2889">身份證號碼</span></span> 
- <span data-ttu-id="dc720-2890">身份證號
</span><span class="sxs-lookup"><span data-stu-id="dc720-2890">身份證號</span></span> 
- <span data-ttu-id="dc720-2891">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="dc720-2891">身分證字號</span></span> 
- <span data-ttu-id="dc720-2892">身分證 </span><span class="sxs-lookup"><span data-stu-id="dc720-2892">身分證</span></span> 
- <span data-ttu-id="dc720-2893">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="dc720-2893">身分證號碼</span></span> 
- <span data-ttu-id="dc720-2894">身份證號
</span><span class="sxs-lookup"><span data-stu-id="dc720-2894">身份證號</span></span> 
- <span data-ttu-id="dc720-2895">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="dc720-2895">身分證統一編號</span></span> 
- <span data-ttu-id="dc720-2896">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="dc720-2896">國民身分證統一編號</span></span> 
- <span data-ttu-id="dc720-2897">簽名
</span><span class="sxs-lookup"><span data-stu-id="dc720-2897">簽名</span></span> 
- <span data-ttu-id="dc720-2898">蓋章
</span><span class="sxs-lookup"><span data-stu-id="dc720-2898">蓋章</span></span> 
- <span data-ttu-id="dc720-2899">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="dc720-2899">簽名或蓋章</span></span> 
- <span data-ttu-id="dc720-2900">簽章</span><span class="sxs-lookup"><span data-stu-id="dc720-2900">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="dc720-2901">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="dc720-2901">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2902">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2902">Format</span></span>

- <span data-ttu-id="dc720-2903">Номер паспорта Биометрическая: девяти цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2903">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="dc720-2904">Номер паспорта не Биометрическая: девяти цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2904">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2905">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2905">Pattern</span></span>
<span data-ttu-id="dc720-2906">Номер паспорта Биометрическая:</span><span class="sxs-lookup"><span data-stu-id="dc720-2906">Biometric passport number:</span></span>
- <span data-ttu-id="dc720-2907">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="dc720-2907">The digit "3"</span></span> 
- <span data-ttu-id="dc720-2908">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2908">Eight digits</span></span>

<span data-ttu-id="dc720-2909">Номер паспорта Биометрическая без поддержки:</span><span class="sxs-lookup"><span data-stu-id="dc720-2909">Non-biometric passport number:</span></span>
- <span data-ttu-id="dc720-2910">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2910">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2911">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2911">Checksum</span></span>

<span data-ttu-id="dc720-2912">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2912">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2913">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2913">Definition</span></span>

<span data-ttu-id="dc720-2914">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2914">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2915">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2915">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2916">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="dc720-2916">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2917">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2917">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="dc720-2918">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-2918">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="dc720-2919">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="dc720-2919">ROC passport number</span></span> 
- <span data-ttu-id="dc720-2920">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="dc720-2920">Passport number</span></span> 
- <span data-ttu-id="dc720-2921">Passport не</span><span class="sxs-lookup"><span data-stu-id="dc720-2921">Passport no</span></span> 
- <span data-ttu-id="dc720-2922">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="dc720-2922">Passport Num</span></span> 
- <span data-ttu-id="dc720-2923">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-2923">Passport #</span></span> 
- <span data-ttu-id="dc720-2924">护照
</span><span class="sxs-lookup"><span data-stu-id="dc720-2924">护照</span></span> 
- <span data-ttu-id="dc720-2925">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="dc720-2925">中華民國護照</span></span> 
- <span data-ttu-id="dc720-2926">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="dc720-2926">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="dc720-2927">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="dc720-2927">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2928">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2928">Format</span></span>

<span data-ttu-id="dc720-2929">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2929">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2930">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2930">Pattern</span></span>

<span data-ttu-id="dc720-2931">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="dc720-2931">10 letters and digits:</span></span>
- <span data-ttu-id="dc720-2932">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="dc720-2932">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="dc720-2933">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-2933">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2934">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2934">Checksum</span></span>

<span data-ttu-id="dc720-2935">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2935">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2936">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2936">Definition</span></span>

<span data-ttu-id="dc720-2937">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2937">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2938">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2938">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2939">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="dc720-2939">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2940">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2940">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="dc720-2941">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="dc720-2941">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="dc720-2942">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="dc720-2942">Resident Certificate</span></span> 
- <span data-ttu-id="dc720-2943">Резидентной Cert</span><span class="sxs-lookup"><span data-stu-id="dc720-2943">Resident Cert</span></span> 
- <span data-ttu-id="dc720-2944">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="dc720-2944">Resident Cert.</span></span> 
- <span data-ttu-id="dc720-2945">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="dc720-2945">Identification card</span></span> 
- <span data-ttu-id="dc720-2946">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="dc720-2946">Alien Resident Certificate</span></span> 
- <span data-ttu-id="dc720-2947">ARC
</span><span class="sxs-lookup"><span data-stu-id="dc720-2947">ARC</span></span> 
- <span data-ttu-id="dc720-2948">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="dc720-2948">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="dc720-2949">TARC
</span><span class="sxs-lookup"><span data-stu-id="dc720-2949">TARC</span></span> 
- <span data-ttu-id="dc720-2950">居留證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2950">居留證</span></span> 
- <span data-ttu-id="dc720-2951">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2951">外僑居留證</span></span> 
- <span data-ttu-id="dc720-2952">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="dc720-2952">台灣地區居留證</span></span> 
   
## <a name="uk-drivers-license-number"></a><span data-ttu-id="dc720-p141">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="dc720-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2955">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2955">Format</span></span>

<span data-ttu-id="dc720-2956">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-2956">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2957">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2957">Pattern</span></span>

<span data-ttu-id="dc720-2958">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2958">18 letters and digits:</span></span>
- <span data-ttu-id="dc720-2959">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="dc720-2959">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="dc720-2960">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dc720-2960">One digit</span></span> 
- <span data-ttu-id="dc720-2961">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="dc720-2961">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="dc720-2962">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="dc720-2962">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="dc720-2963">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-2963">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2964">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2964">Checksum</span></span>

<span data-ttu-id="dc720-2965">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-2965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2966">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2966">Definition</span></span>

<span data-ttu-id="dc720-2967">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2967">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2968">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2968">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2969">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="dc720-2969">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="dc720-2970">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-2970">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-2971">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-2971">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="dc720-2972">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="dc720-2972">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="dc720-2973">DVLA
</span><span class="sxs-lookup"><span data-stu-id="dc720-2973">DVLA</span></span> 
- <span data-ttu-id="dc720-2974">light vans
</span><span class="sxs-lookup"><span data-stu-id="dc720-2974">light vans</span></span> 
- <span data-ttu-id="dc720-2975">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="dc720-2975">quadbikes</span></span> 
- <span data-ttu-id="dc720-2976">motor cars
</span><span class="sxs-lookup"><span data-stu-id="dc720-2976">motor cars</span></span> 
- <span data-ttu-id="dc720-2977">125cc</span><span class="sxs-lookup"><span data-stu-id="dc720-2977">125cc</span></span> 
- <span data-ttu-id="dc720-2978">sidecar
</span><span class="sxs-lookup"><span data-stu-id="dc720-2978">sidecar</span></span> 
- <span data-ttu-id="dc720-2979">tricycles
</span><span class="sxs-lookup"><span data-stu-id="dc720-2979">tricycles</span></span> 
- <span data-ttu-id="dc720-2980">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="dc720-2980">motorcycles</span></span> 
- <span data-ttu-id="dc720-2981">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-2981">photocard licence</span></span> 
- <span data-ttu-id="dc720-2982">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="dc720-2982">learner drivers</span></span> 
- <span data-ttu-id="dc720-2983">licence holder
</span><span class="sxs-lookup"><span data-stu-id="dc720-2983">licence holder</span></span> 
- <span data-ttu-id="dc720-2984">licence holders
</span><span class="sxs-lookup"><span data-stu-id="dc720-2984">licence holders</span></span> 
- <span data-ttu-id="dc720-2985">driving licences
</span><span class="sxs-lookup"><span data-stu-id="dc720-2985">driving licences</span></span> 
- <span data-ttu-id="dc720-2986">driving licence
</span><span class="sxs-lookup"><span data-stu-id="dc720-2986">driving licence</span></span> 
- <span data-ttu-id="dc720-2987">dual control car
</span><span class="sxs-lookup"><span data-stu-id="dc720-2987">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="dc720-p142">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="dc720-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-2990">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-2990">Format</span></span>

<span data-ttu-id="dc720-2991">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2991">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-2992">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-2992">Pattern</span></span>

<span data-ttu-id="dc720-2993">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="dc720-2993">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-2994">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-2994">Checksum</span></span>

<span data-ttu-id="dc720-2995">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-2995">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-2996">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-2996">Definition</span></span>

<span data-ttu-id="dc720-2997">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-2997">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-2998">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-2998">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-2999">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="dc720-2999">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-3000">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3000">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="dc720-3001">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="dc720-3001">Keyword_uk_electoral</span></span>

- <span data-ttu-id="dc720-3002">council nomination
</span><span class="sxs-lookup"><span data-stu-id="dc720-3002">council nomination</span></span> 
- <span data-ttu-id="dc720-3003">nomination form
</span><span class="sxs-lookup"><span data-stu-id="dc720-3003">nomination form</span></span> 
- <span data-ttu-id="dc720-3004">electoral register

</span><span class="sxs-lookup"><span data-stu-id="dc720-3004">electoral register</span></span> 
- <span data-ttu-id="dc720-3005">electoral roll</span><span class="sxs-lookup"><span data-stu-id="dc720-3005">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="dc720-p143">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="dc720-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3008">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3008">Format</span></span>

<span data-ttu-id="dc720-3009">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="dc720-3009">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3010">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3010">Pattern</span></span>

<span data-ttu-id="dc720-3011">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-3011">10-17 digits:</span></span>
- <span data-ttu-id="dc720-3012">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-3012">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="dc720-3013">Пробел</span><span class="sxs-lookup"><span data-stu-id="dc720-3013">A space</span></span> 
- <span data-ttu-id="dc720-3014">Три цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3014">Three digits</span></span> 
- <span data-ttu-id="dc720-3015">Пробел</span><span class="sxs-lookup"><span data-stu-id="dc720-3015">A space</span></span> 
- <span data-ttu-id="dc720-3016">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3016">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3017">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3017">Checksum</span></span>

<span data-ttu-id="dc720-3018">Да</span><span class="sxs-lookup"><span data-stu-id="dc720-3018">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-3019">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3019">Definition</span></span>

<span data-ttu-id="dc720-3020">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3020">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3021">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3021">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3022">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-3022">One of the following is true:</span></span>
    - <span data-ttu-id="dc720-3023">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="dc720-3023">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="dc720-3024">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="dc720-3024">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="dc720-3025">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="dc720-3025">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="dc720-3026">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="dc720-3026">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-3027">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3027">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="dc720-3028">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="dc720-3028">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="dc720-3029">national health service
</span><span class="sxs-lookup"><span data-stu-id="dc720-3029">national health service</span></span> 
- <span data-ttu-id="dc720-3030">nhs
</span><span class="sxs-lookup"><span data-stu-id="dc720-3030">nhs</span></span> 
- <span data-ttu-id="dc720-3031">health services authority

</span><span class="sxs-lookup"><span data-stu-id="dc720-3031">health services authority</span></span> 
- <span data-ttu-id="dc720-3032">health authority</span><span class="sxs-lookup"><span data-stu-id="dc720-3032">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="dc720-3033">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="dc720-3033">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="dc720-3034">patient id
</span><span class="sxs-lookup"><span data-stu-id="dc720-3034">patient id</span></span> 
- <span data-ttu-id="dc720-3035">patient identification
</span><span class="sxs-lookup"><span data-stu-id="dc720-3035">patient identification</span></span> 
- <span data-ttu-id="dc720-3036">patient no

</span><span class="sxs-lookup"><span data-stu-id="dc720-3036">patient no</span></span> 
- <span data-ttu-id="dc720-3037">patient number</span><span class="sxs-lookup"><span data-stu-id="dc720-3037">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="dc720-3038">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="dc720-3038">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="dc720-3039">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="dc720-3039">GP</span></span> 
- <span data-ttu-id="dc720-3040">DOB
</span><span class="sxs-lookup"><span data-stu-id="dc720-3040">DOB</span></span> 
- <span data-ttu-id="dc720-3041">D.O.B</span><span class="sxs-lookup"><span data-stu-id="dc720-3041">D.O.B</span></span> 
- <span data-ttu-id="dc720-3042">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="dc720-3042">Date of Birth</span></span> 
- <span data-ttu-id="dc720-3043">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="dc720-3043">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="dc720-p144">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="dc720-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3046">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3046">Format</span></span>

<span data-ttu-id="dc720-3047">7 или 9 символы, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3047">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3048">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3048">Pattern</span></span>

<span data-ttu-id="dc720-3049">Два возможных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="dc720-3049">Two possible patterns:</span></span>

- <span data-ttu-id="dc720-3050">Две буквы (допустимый NINOs использовать только определенных символов в этом префикс, который проверяет этот шаблон; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="dc720-3050">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="dc720-3051">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-3051">Six digits</span></span>
- <span data-ttu-id="dc720-3052">Либо 'A', 'B', 'C', или имелся "(только для определенных символов в допускаются суффикс; не учитывают регистр, как префикс)</span><span class="sxs-lookup"><span data-stu-id="dc720-3052">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="dc720-3053">OR</span><span class="sxs-lookup"><span data-stu-id="dc720-3053">OR</span></span>

- <span data-ttu-id="dc720-3054">Два букв</span><span class="sxs-lookup"><span data-stu-id="dc720-3054">Two letters</span></span>
- <span data-ttu-id="dc720-3055">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3055">A space or dash</span></span>
- <span data-ttu-id="dc720-3056">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3056">Two digits</span></span>
- <span data-ttu-id="dc720-3057">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3057">A space or dash</span></span>
- <span data-ttu-id="dc720-3058">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3058">Two digits</span></span>
- <span data-ttu-id="dc720-3059">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3059">A space or dash</span></span>
- <span data-ttu-id="dc720-3060">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3060">Two digits</span></span>
- <span data-ttu-id="dc720-3061">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3061">A space or dash</span></span>
- <span data-ttu-id="dc720-3062">Либо '', 'B', 'C', или имелся "</span><span class="sxs-lookup"><span data-stu-id="dc720-3062">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3063">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3063">Checksum</span></span>

<span data-ttu-id="dc720-3064">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-3064">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-3065">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3065">Definition</span></span>

<span data-ttu-id="dc720-3066">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3066">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3067">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-3067">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3068">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="dc720-3068">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="dc720-3069">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3069">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3070">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-3070">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3071">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="dc720-3071">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-3072">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3072">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="dc720-3073">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="dc720-3073">Keyword_uk_nino</span></span>

- <span data-ttu-id="dc720-3074">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3074">national insurance number</span></span> 
- <span data-ttu-id="dc720-3075">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="dc720-3075">national insurance contributions</span></span> 
- <span data-ttu-id="dc720-3076">protection act
</span><span class="sxs-lookup"><span data-stu-id="dc720-3076">protection act</span></span> 
- <span data-ttu-id="dc720-3077">insurance
</span><span class="sxs-lookup"><span data-stu-id="dc720-3077">insurance</span></span> 
- <span data-ttu-id="dc720-3078">social security number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3078">social security number</span></span> 
- <span data-ttu-id="dc720-3079">insurance application
</span><span class="sxs-lookup"><span data-stu-id="dc720-3079">insurance application</span></span> 
- <span data-ttu-id="dc720-3080">medical application
</span><span class="sxs-lookup"><span data-stu-id="dc720-3080">medical application</span></span> 
- <span data-ttu-id="dc720-3081">social insurance
</span><span class="sxs-lookup"><span data-stu-id="dc720-3081">social insurance</span></span> 
- <span data-ttu-id="dc720-3082">medical attention
</span><span class="sxs-lookup"><span data-stu-id="dc720-3082">medical attention</span></span> 
- <span data-ttu-id="dc720-3083">социального страхования</span><span class="sxs-lookup"><span data-stu-id="dc720-3083">social security</span></span> 
- <span data-ttu-id="dc720-3084">great britain
</span><span class="sxs-lookup"><span data-stu-id="dc720-3084">great britain</span></span> 
- <span data-ttu-id="dc720-3085">insurance
</span><span class="sxs-lookup"><span data-stu-id="dc720-3085">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="dc720-p145">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="dc720-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3088">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3088">Format</span></span>

<span data-ttu-id="dc720-3089">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-3089">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3090">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3090">Pattern</span></span>

<span data-ttu-id="dc720-3091">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="dc720-3091">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3092">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3092">Checksum</span></span>

<span data-ttu-id="dc720-3093">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-3093">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-3094">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3094">Definition</span></span>

<span data-ttu-id="dc720-3095">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3095">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3096">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-3096">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3097">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="dc720-3097">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-3098">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3098">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="dc720-3099">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="dc720-3099">Keyword_passport</span></span>

- <span data-ttu-id="dc720-3100">Passport Number</span><span class="sxs-lookup"><span data-stu-id="dc720-3100">Passport Number</span></span> 
- <span data-ttu-id="dc720-3101">
Passport No</span><span class="sxs-lookup"><span data-stu-id="dc720-3101">Passport No</span></span> 
- <span data-ttu-id="dc720-3102">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3102">Passport #</span></span> 
- <span data-ttu-id="dc720-3103">Passport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3103">Passport#</span></span> 
- <span data-ttu-id="dc720-3104">PassportID</span><span class="sxs-lookup"><span data-stu-id="dc720-3104">PassportID</span></span> 
- <span data-ttu-id="dc720-3105">Passportno
</span><span class="sxs-lookup"><span data-stu-id="dc720-3105">Passportno</span></span> 
- <span data-ttu-id="dc720-3106">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="dc720-3106">passportnumber</span></span> 
- <span data-ttu-id="dc720-3107">パスポート</span><span class="sxs-lookup"><span data-stu-id="dc720-3107">パスポート</span></span> 
- <span data-ttu-id="dc720-3108">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="dc720-3108">パスポート番号</span></span> 
- <span data-ttu-id="dc720-3109">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="dc720-3109">パスポートのNum</span></span> 
- <span data-ttu-id="dc720-3110">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="dc720-3110">パスポート＃</span></span> 
- <span data-ttu-id="dc720-3111">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="dc720-3111">Numéro de passeport</span></span> 
- <span data-ttu-id="dc720-3112">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="dc720-3112">Passeport n °</span></span> 
- <span data-ttu-id="dc720-3113">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="dc720-3113">Passeport Non</span></span> 
- <span data-ttu-id="dc720-3114">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3114">Passeport #</span></span> 
- <span data-ttu-id="dc720-3115">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3115">Passeport#</span></span> 
- <span data-ttu-id="dc720-3116">PasseportNon</span><span class="sxs-lookup"><span data-stu-id="dc720-3116">PasseportNon</span></span> 
- <span data-ttu-id="dc720-3117">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="dc720-3117">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="dc720-3118">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="dc720-3118">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3119">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3119">Format</span></span>

<span data-ttu-id="dc720-3120">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-3120">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3121">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3121">Pattern</span></span>

<span data-ttu-id="dc720-3122">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-3122">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3123">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3123">Checksum</span></span>

<span data-ttu-id="dc720-3124">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-3124">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-3125">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3125">Definition</span></span>

<span data-ttu-id="dc720-3126">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3126">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3127">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-3127">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3128">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="dc720-3128">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="dc720-3129">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3129">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="dc720-3130">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="dc720-3130">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="dc720-3131">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3131">Checking Account Number</span></span> 
- <span data-ttu-id="dc720-3132">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="dc720-3132">Checking Account</span></span> 
- <span data-ttu-id="dc720-3133">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3133">Checking Account #</span></span> 
- <span data-ttu-id="dc720-3134">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3134">Checking Acct Number</span></span> 
- <span data-ttu-id="dc720-3135">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3135">Checking Acct #</span></span> 
- <span data-ttu-id="dc720-3136">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3136">Checking Acct No.</span></span> 
- <span data-ttu-id="dc720-3137">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3137">Checking Account No.</span></span> 
- <span data-ttu-id="dc720-3138">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3138">Bank Account Number</span></span> 
- <span data-ttu-id="dc720-3139">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3139">Bank Account #</span></span> 
- <span data-ttu-id="dc720-3140">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3140">Bank Acct Number</span></span> 
- <span data-ttu-id="dc720-3141">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3141">Bank Acct #</span></span> 
- <span data-ttu-id="dc720-3142">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3142">Bank Acct No.</span></span> 
- <span data-ttu-id="dc720-3143">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3143">Bank Account No.</span></span> 
- <span data-ttu-id="dc720-3144">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3144">Savings Account Number</span></span> 
- <span data-ttu-id="dc720-3145">Savings Account.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3145">Savings Account.</span></span> 
- <span data-ttu-id="dc720-3146">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3146">Savings Account #</span></span> 
- <span data-ttu-id="dc720-3147">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3147">Savings Acct Number</span></span> 
- <span data-ttu-id="dc720-3148">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3148">Savings Acct #</span></span> 
- <span data-ttu-id="dc720-3149">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3149">Savings Acct No.</span></span> 
- <span data-ttu-id="dc720-3150">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3150">Savings Account No.</span></span> 
- <span data-ttu-id="dc720-3151">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3151">Debit Account Number</span></span> 
- <span data-ttu-id="dc720-3152">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="dc720-3152">Debit Account</span></span> 
- <span data-ttu-id="dc720-3153">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3153">Debit Account #</span></span> 
- <span data-ttu-id="dc720-3154">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3154">Debit Acct Number</span></span> 
- <span data-ttu-id="dc720-3155">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3155">Debit Acct #</span></span> 
- <span data-ttu-id="dc720-3156">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3156">Debit Acct No.</span></span> 
- <span data-ttu-id="dc720-3157">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="dc720-3157">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="dc720-3158">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="dc720-3158">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3159">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3159">Format</span></span>

<span data-ttu-id="dc720-3160">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="dc720-3160">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3161">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3161">Pattern</span></span>

<span data-ttu-id="dc720-3162">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="dc720-3162">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="dc720-3163">Подойдут девять цифр в формате ццц ццц ццц.</span><span class="sxs-lookup"><span data-stu-id="dc720-3163">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="dc720-3164">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="dc720-3164">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3165">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3165">Checksum</span></span>

<span data-ttu-id="dc720-3166">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-3166">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-3167">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3167">Definition</span></span>

<span data-ttu-id="dc720-3168">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3168">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3169">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-3169">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3170">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="dc720-3170">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="dc720-3171">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="dc720-3171">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="dc720-3172">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3172">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3173">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="dc720-3173">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3174">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="dc720-3174">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="dc720-3175">находится ключевое слово из Keyword_us_drivers_license_abbreviations;</span><span class="sxs-lookup"><span data-stu-id="dc720-3175">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="dc720-3176">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="dc720-3176">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-3177">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3177">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="dc720-3178">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="dc720-3178">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="dc720-3179">DL</span><span class="sxs-lookup"><span data-stu-id="dc720-3179">DL</span></span> 
- <span data-ttu-id="dc720-3180">DLS</span><span class="sxs-lookup"><span data-stu-id="dc720-3180">DLS</span></span> 
- <span data-ttu-id="dc720-3181">CDL</span><span class="sxs-lookup"><span data-stu-id="dc720-3181">CDL</span></span> 
- <span data-ttu-id="dc720-3182">CDLS</span><span class="sxs-lookup"><span data-stu-id="dc720-3182">CDLS</span></span> 
- <span data-ttu-id="dc720-3183">ID</span><span class="sxs-lookup"><span data-stu-id="dc720-3183">ID</span></span> 
- <span data-ttu-id="dc720-3184">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="dc720-3184">IDs</span></span> 
- <span data-ttu-id="dc720-3185">DL#</span><span class="sxs-lookup"><span data-stu-id="dc720-3185">DL#</span></span> 
- <span data-ttu-id="dc720-3186">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3186">DLS#</span></span> 
- <span data-ttu-id="dc720-3187">CDL#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3187">CDL#</span></span> 
- <span data-ttu-id="dc720-3188">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3188">CDLS#</span></span> 
- <span data-ttu-id="dc720-3189">ID#</span><span class="sxs-lookup"><span data-stu-id="dc720-3189">ID#</span></span>
- <span data-ttu-id="dc720-3190">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3190">IDs#</span></span> 
- <span data-ttu-id="dc720-3191">идентификатор</span><span class="sxs-lookup"><span data-stu-id="dc720-3191">ID number</span></span> 
- <span data-ttu-id="dc720-3192">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-3192">ID numbers</span></span> 
- <span data-ttu-id="dc720-3193">LIC</span><span class="sxs-lookup"><span data-stu-id="dc720-3193">LIC</span></span> 
- <span data-ttu-id="dc720-3194">LIC#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3194">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="dc720-3195">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="dc720-3195">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="dc720-3196">DriverLic</span><span class="sxs-lookup"><span data-stu-id="dc720-3196">DriverLic</span></span> 
- <span data-ttu-id="dc720-3197">DriverLics</span><span class="sxs-lookup"><span data-stu-id="dc720-3197">DriverLics</span></span> 
- <span data-ttu-id="dc720-3198">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-3198">DriverLicense</span></span> 
- <span data-ttu-id="dc720-3199">DriverLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-3199">DriverLicenses</span></span> 
- <span data-ttu-id="dc720-3200">Драйвер Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-3200">Driver Lic</span></span> 
- <span data-ttu-id="dc720-3201">Драйвер Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-3201">Driver Lics</span></span> 
- <span data-ttu-id="dc720-3202">Драйвер лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-3202">Driver License</span></span> 
- <span data-ttu-id="dc720-3203">Драйвер лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-3203">Driver Licenses</span></span> 
- <span data-ttu-id="dc720-3204">DriversLic</span><span class="sxs-lookup"><span data-stu-id="dc720-3204">DriversLic</span></span> 
- <span data-ttu-id="dc720-3205">DriversLics</span><span class="sxs-lookup"><span data-stu-id="dc720-3205">DriversLics</span></span> 
- <span data-ttu-id="dc720-3206">DriversLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-3206">DriversLicense</span></span> 
- <span data-ttu-id="dc720-3207">DriversLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-3207">DriversLicenses</span></span> 
- <span data-ttu-id="dc720-3208">Драйверы Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-3208">Drivers Lic</span></span> 
- <span data-ttu-id="dc720-3209">Драйверы Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-3209">Drivers Lics</span></span> 
- <span data-ttu-id="dc720-3210">Драйверы лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-3210">Drivers License</span></span> 
- <span data-ttu-id="dc720-3211">Драйверы лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-3211">Drivers Licenses</span></span> 
- <span data-ttu-id="dc720-3212">Driver'Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-3212">Driver'Lic</span></span> 
- <span data-ttu-id="dc720-3213">Driver'Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-3213">Driver'Lics</span></span> 
- <span data-ttu-id="dc720-3214">Driver'License</span><span class="sxs-lookup"><span data-stu-id="dc720-3214">Driver'License</span></span> 
- <span data-ttu-id="dc720-3215">Driver'Licenses</span><span class="sxs-lookup"><span data-stu-id="dc720-3215">Driver'Licenses</span></span> 
- <span data-ttu-id="dc720-3216">Драйвер ' Lic</span><span class="sxs-lookup"><span data-stu-id="dc720-3216">Driver' Lic</span></span> 
- <span data-ttu-id="dc720-3217">Драйвер ' Lics</span><span class="sxs-lookup"><span data-stu-id="dc720-3217">Driver' Lics</span></span> 
- <span data-ttu-id="dc720-3218">Драйвер "лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-3218">Driver' License</span></span> 
- <span data-ttu-id="dc720-3219">Драйвер "лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-3219">Driver' Licenses</span></span>
- <span data-ttu-id="dc720-3220">Driver'sLic</span><span class="sxs-lookup"><span data-stu-id="dc720-3220">Driver'sLic</span></span> 
- <span data-ttu-id="dc720-3221">Driver'sLics</span><span class="sxs-lookup"><span data-stu-id="dc720-3221">Driver'sLics</span></span> 
- <span data-ttu-id="dc720-3222">Driver'sLicense</span><span class="sxs-lookup"><span data-stu-id="dc720-3222">Driver'sLicense</span></span> 
- <span data-ttu-id="dc720-3223">Driver'sLicenses</span><span class="sxs-lookup"><span data-stu-id="dc720-3223">Driver'sLicenses</span></span> 
- <span data-ttu-id="dc720-3224">Lic драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-3224">Driver's Lic</span></span> 
- <span data-ttu-id="dc720-3225">Lics драйвера</span><span class="sxs-lookup"><span data-stu-id="dc720-3225">Driver's Lics</span></span> 
- <span data-ttu-id="dc720-3226">Водительского удостоверения для лицензии</span><span class="sxs-lookup"><span data-stu-id="dc720-3226">Driver's License</span></span> 
- <span data-ttu-id="dc720-3227">Водительского удостоверения для лицензий</span><span class="sxs-lookup"><span data-stu-id="dc720-3227">Driver's Licenses</span></span> 
- <span data-ttu-id="dc720-3228">identification number
</span><span class="sxs-lookup"><span data-stu-id="dc720-3228">identification number</span></span> 
- <span data-ttu-id="dc720-3229">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="dc720-3229">identification numbers</span></span> 
- <span data-ttu-id="dc720-3230">identification #
</span><span class="sxs-lookup"><span data-stu-id="dc720-3230">identification #</span></span> 
- <span data-ttu-id="dc720-3231">Карточка</span><span class="sxs-lookup"><span data-stu-id="dc720-3231">id card</span></span> 
- <span data-ttu-id="dc720-3232">Идентификатор карточки</span><span class="sxs-lookup"><span data-stu-id="dc720-3232">id cards</span></span> 
- <span data-ttu-id="dc720-3233">Идентификация карточки</span><span class="sxs-lookup"><span data-stu-id="dc720-3233">identification card</span></span> 
- <span data-ttu-id="dc720-3234">Идентификация карты</span><span class="sxs-lookup"><span data-stu-id="dc720-3234">identification cards</span></span> 
- <span data-ttu-id="dc720-3235">DriverLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-3235">DriverLic#</span></span> 
- <span data-ttu-id="dc720-3236">DriverLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-3236">DriverLics#</span></span> 
- <span data-ttu-id="dc720-3237">DriverLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-3237">DriverLicense#</span></span> 
- <span data-ttu-id="dc720-3238">DriverLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-3238">DriverLicenses#</span></span> 
- <span data-ttu-id="dc720-3239">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="dc720-3239">Driver Lic#</span></span> 
- <span data-ttu-id="dc720-3240">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3240">Driver Lics#</span></span> 
- <span data-ttu-id="dc720-3241">Драйвер лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-3241">Driver License#</span></span> 
- <span data-ttu-id="dc720-3242">Драйвер лицензий #</span><span class="sxs-lookup"><span data-stu-id="dc720-3242">Driver Licenses#</span></span> 
- <span data-ttu-id="dc720-3243">DriversLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-3243">DriversLic#</span></span> 
- <span data-ttu-id="dc720-3244">DriversLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-3244">DriversLics#</span></span> 
- <span data-ttu-id="dc720-3245">DriversLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-3245">DriversLicense#</span></span> 
- <span data-ttu-id="dc720-3246">DriversLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-3246">DriversLicenses#</span></span> 
- <span data-ttu-id="dc720-3247">Драйверы Lic #</span><span class="sxs-lookup"><span data-stu-id="dc720-3247">Drivers Lic#</span></span> 
- <span data-ttu-id="dc720-3248">Драйверы Lics #</span><span class="sxs-lookup"><span data-stu-id="dc720-3248">Drivers Lics#</span></span> 
- <span data-ttu-id="dc720-3249">Драйверы лицензии #</span><span class="sxs-lookup"><span data-stu-id="dc720-3249">Drivers License#</span></span> 
- <span data-ttu-id="dc720-3250">Драйверы лицензий #</span><span class="sxs-lookup"><span data-stu-id="dc720-3250">Drivers Licenses#</span></span> 
- <span data-ttu-id="dc720-3251">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3251">Driver'Lic#</span></span> 
- <span data-ttu-id="dc720-3252">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3252">Driver'Lics#</span></span> 
- <span data-ttu-id="dc720-3253">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3253">Driver'License#</span></span> 
- <span data-ttu-id="dc720-3254">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3254">Driver'Licenses#</span></span> 
- <span data-ttu-id="dc720-3255">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3255">Driver' Lic#</span></span> 
- <span data-ttu-id="dc720-3256">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3256">Driver' Lics#</span></span> 
- <span data-ttu-id="dc720-3257">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3257">Driver' License#</span></span> 
- <span data-ttu-id="dc720-3258">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3258">Driver' Licenses#</span></span> 
- <span data-ttu-id="dc720-3259">Driver'sLic #</span><span class="sxs-lookup"><span data-stu-id="dc720-3259">Driver'sLic#</span></span> 
- <span data-ttu-id="dc720-3260">Driver'sLics #</span><span class="sxs-lookup"><span data-stu-id="dc720-3260">Driver'sLics#</span></span> 
- <span data-ttu-id="dc720-3261">Driver'sLicense #</span><span class="sxs-lookup"><span data-stu-id="dc720-3261">Driver'sLicense#</span></span> 
- <span data-ttu-id="dc720-3262">Driver'sLicenses #</span><span class="sxs-lookup"><span data-stu-id="dc720-3262">Driver'sLicenses#</span></span> 
- <span data-ttu-id="dc720-3263">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3263">Driver's Lic#</span></span> 
- <span data-ttu-id="dc720-3264">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3264">Driver's Lics#</span></span> 
- <span data-ttu-id="dc720-3265">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3265">Driver's License#</span></span> 
- <span data-ttu-id="dc720-3266">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3266">Driver's Licenses#</span></span> 
- <span data-ttu-id="dc720-3267">Карточка #</span><span class="sxs-lookup"><span data-stu-id="dc720-3267">id card#</span></span> 
- <span data-ttu-id="dc720-3268">id cards#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3268">id cards#</span></span> 
- <span data-ttu-id="dc720-3269">identification card#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3269">identification card#</span></span> 
- <span data-ttu-id="dc720-3270">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3270">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="dc720-3271">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="dc720-3271">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="dc720-3272">Аббревиатура штата (например, NY)
</span><span class="sxs-lookup"><span data-stu-id="dc720-3272">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="dc720-3273">Название штата (например, New York)
</span><span class="sxs-lookup"><span data-stu-id="dc720-3273">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="dc720-3274">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="dc720-3274">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3275">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3275">Format</span></span>

<span data-ttu-id="dc720-3276">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="dc720-3276">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3277">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3277">Pattern</span></span>

<span data-ttu-id="dc720-3278">С форматированием</span><span class="sxs-lookup"><span data-stu-id="dc720-3278">Formatted:</span></span>
- <span data-ttu-id="dc720-3279">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="dc720-3279">The digit "9"</span></span> 
- <span data-ttu-id="dc720-3280">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3280">Two digits</span></span> 
- <span data-ttu-id="dc720-3281">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3281">A space or dash</span></span> 
- <span data-ttu-id="dc720-3282">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="dc720-3282">A "7" or "8"</span></span> 
- <span data-ttu-id="dc720-3283">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="dc720-3283">A digit</span></span> 
- <span data-ttu-id="dc720-3284">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="dc720-3284">A space, or dash</span></span> 
- <span data-ttu-id="dc720-3285">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3285">Four digits</span></span>

<span data-ttu-id="dc720-3286">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="dc720-3286">Unformatted:</span></span>
- <span data-ttu-id="dc720-3287">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="dc720-3287">The digit "9"</span></span> 
- <span data-ttu-id="dc720-3288">Две цифры</span><span class="sxs-lookup"><span data-stu-id="dc720-3288">Two digits</span></span> 
- <span data-ttu-id="dc720-3289">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="dc720-3289">A "7" or "8"</span></span> 
- <span data-ttu-id="dc720-3290">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="dc720-3290">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3291">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3291">Checksum</span></span>

<span data-ttu-id="dc720-3292">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-3292">No</span></span>

### <a name="definition"></a><span data-ttu-id="dc720-3293">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3293">Definition</span></span>

<span data-ttu-id="dc720-3294">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3294">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3295">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3295">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3296">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-3296">At least one of the following is true:</span></span>
    - <span data-ttu-id="dc720-3297">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="dc720-3297">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="dc720-3298">функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-3298">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="dc720-3299">функция Func_us_date находит дату в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="dc720-3299">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="dc720-3300">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="dc720-3300">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="dc720-3301">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3301">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3302">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3302">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3303">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="dc720-3303">At least one of the following is true:</span></span>
    - <span data-ttu-id="dc720-3304">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="dc720-3304">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="dc720-3305">функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-3305">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="dc720-3306">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="dc720-3306">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-3307">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3307">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="dc720-3308">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="dc720-3308">Keyword_itin</span></span>

- <span data-ttu-id="dc720-3309">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="dc720-3309">taxpayer</span></span> 
- <span data-ttu-id="dc720-3310">tax id
</span><span class="sxs-lookup"><span data-stu-id="dc720-3310">tax id</span></span> 
- <span data-ttu-id="dc720-3311">tax identification
</span><span class="sxs-lookup"><span data-stu-id="dc720-3311">tax identification</span></span> 
- <span data-ttu-id="dc720-3312">itin
</span><span class="sxs-lookup"><span data-stu-id="dc720-3312">itin</span></span> 
- <span data-ttu-id="dc720-3313">SSN</span><span class="sxs-lookup"><span data-stu-id="dc720-3313">ssn</span></span> 
- <span data-ttu-id="dc720-3314">tin
</span><span class="sxs-lookup"><span data-stu-id="dc720-3314">tin</span></span> 
- <span data-ttu-id="dc720-3315">социального страхования</span><span class="sxs-lookup"><span data-stu-id="dc720-3315">social security</span></span> 
- <span data-ttu-id="dc720-3316">tax payer
</span><span class="sxs-lookup"><span data-stu-id="dc720-3316">tax payer</span></span> 
- <span data-ttu-id="dc720-3317">itins
</span><span class="sxs-lookup"><span data-stu-id="dc720-3317">itins</span></span> 
- <span data-ttu-id="dc720-3318">taxid

</span><span class="sxs-lookup"><span data-stu-id="dc720-3318">taxid</span></span> 
- <span data-ttu-id="dc720-3319">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="dc720-3319">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="dc720-3320">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="dc720-3320">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="dc720-3321">License</span><span class="sxs-lookup"><span data-stu-id="dc720-3321">License</span></span> 
- <span data-ttu-id="dc720-3322">DL</span><span class="sxs-lookup"><span data-stu-id="dc720-3322">DL</span></span> 
- <span data-ttu-id="dc720-3323">DOB
</span><span class="sxs-lookup"><span data-stu-id="dc720-3323">DOB</span></span> 
- <span data-ttu-id="dc720-3324">Birthdate</span><span class="sxs-lookup"><span data-stu-id="dc720-3324">Birthdate</span></span> 
- <span data-ttu-id="dc720-3325">День рождения </span><span class="sxs-lookup"><span data-stu-id="dc720-3325">Birthday</span></span> 
- <span data-ttu-id="dc720-3326">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="dc720-3326">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="dc720-3327">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="dc720-3327">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="dc720-3328">Формат</span><span class="sxs-lookup"><span data-stu-id="dc720-3328">Format</span></span>

<span data-ttu-id="dc720-3329">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="dc720-3329">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="dc720-3330">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="dc720-3330">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="dc720-3331">Шаблон</span><span class="sxs-lookup"><span data-stu-id="dc720-3331">Pattern</span></span>

<span data-ttu-id="dc720-3332">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="dc720-3332">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="dc720-3333">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="dc720-3333">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="dc720-3334">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="dc720-3334">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="dc720-3335">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="dc720-3335">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="dc720-3336">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="dc720-3336">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="dc720-3337">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="dc720-3337">Checksum</span></span>

<span data-ttu-id="dc720-3338">Нет</span><span class="sxs-lookup"><span data-stu-id="dc720-3338">No</span></span>


### <a name="definition"></a><span data-ttu-id="dc720-3339">Определение</span><span class="sxs-lookup"><span data-stu-id="dc720-3339">Definition</span></span>

<span data-ttu-id="dc720-3340">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3340">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3341">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3341">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3342">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="dc720-3342">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="dc720-3343">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3343">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3344">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3344">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3345">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="dc720-3345">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="dc720-3346">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3346">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3347">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3347">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3348">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="dc720-3348">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="dc720-3349">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3349">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="dc720-3350">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="dc720-3350">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="dc720-3351">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3351">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="dc720-3352">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="dc720-3352">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="dc720-3353">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="dc720-3353">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="dc720-3354">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="dc720-3354">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="dc720-3355">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="dc720-3355">Keyword_ssn</span></span>

- <span data-ttu-id="dc720-3356">Social Security
</span><span class="sxs-lookup"><span data-stu-id="dc720-3356">Social Security</span></span> 
- <span data-ttu-id="dc720-3357">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3357">Social Security#</span></span> 
- <span data-ttu-id="dc720-3358">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="dc720-3358">Soc Sec</span></span> 
- <span data-ttu-id="dc720-3359">SSN</span><span class="sxs-lookup"><span data-stu-id="dc720-3359">SSN</span></span> 
- <span data-ttu-id="dc720-3360">SSNS
</span><span class="sxs-lookup"><span data-stu-id="dc720-3360">SSNS</span></span> 
- <span data-ttu-id="dc720-3361">SSN#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3361">SSN#</span></span> 
- <span data-ttu-id="dc720-3362">SS#
</span><span class="sxs-lookup"><span data-stu-id="dc720-3362">SS#</span></span> 
- <span data-ttu-id="dc720-3363">SSID
</span><span class="sxs-lookup"><span data-stu-id="dc720-3363">SSID</span></span> 
   

