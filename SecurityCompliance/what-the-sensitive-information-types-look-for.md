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
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Защита от потери данных (DLP) в центре безопасности &amp; Office 365 включает в себя 80 типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показано, как будет выглядеть политика DLP при обнаружении каждого типа.
ms.openlocfilehash: 17fb0b8d745168f8000fba9e6fc42f3c255a1937
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216359"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="37c0f-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="37c0f-104">What the sensitive information types look for</span></span>

<span data-ttu-id="37c0f-p102">Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показано, как будет выглядеть политика DLP при обнаружении каждого типа. Тип конфиденциальной информации определяется шаблоном, который может быть идентифицирован регулярным выражением или функцией. Кроме того, подкрепляющее, такие как ключевые слова и контрольные суммы, можно использовать для определения типа конфиденциальной информации. Уровень вероятности и близость также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type. A sensitive information type is defined by a pattern that can be identified by a regular expression or a function. In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type. Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="37c0f-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="37c0f-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-111">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-111">Format</span></span>

<span data-ttu-id="37c0f-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="37c0f-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-113">Pattern</span></span>

<span data-ttu-id="37c0f-114">С форматированием</span><span class="sxs-lookup"><span data-stu-id="37c0f-114">Formatted:</span></span>
- <span data-ttu-id="37c0f-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="37c0f-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="37c0f-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-116">A hyphen</span></span>
- <span data-ttu-id="37c0f-117">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-117">Four digits</span></span>
- <span data-ttu-id="37c0f-118">дефис; </span><span class="sxs-lookup"><span data-stu-id="37c0f-118">A hyphen</span></span>
- <span data-ttu-id="37c0f-119">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="37c0f-119">A digit</span></span>

<span data-ttu-id="37c0f-120">Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8.</span><span class="sxs-lookup"><span data-stu-id="37c0f-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="37c0f-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-121">Checksum</span></span>

<span data-ttu-id="37c0f-122">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-123">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-123">Definition</span></span>

<span data-ttu-id="37c0f-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="37c0f-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="37c0f-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="37c0f-128">Кэйворд_аба_раутинг</span><span class="sxs-lookup"><span data-stu-id="37c0f-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="37c0f-129">aba</span><span class="sxs-lookup"><span data-stu-id="37c0f-129">aba</span></span>
- <span data-ttu-id="37c0f-130">
aba#</span><span class="sxs-lookup"><span data-stu-id="37c0f-130">aba #</span></span>
- <span data-ttu-id="37c0f-131">
aba routing #</span><span class="sxs-lookup"><span data-stu-id="37c0f-131">aba routing #</span></span>
- <span data-ttu-id="37c0f-132">номер маршрутизации код банка ABA</span><span class="sxs-lookup"><span data-stu-id="37c0f-132">aba routing number</span></span>
- <span data-ttu-id="37c0f-133">
aba#</span><span class="sxs-lookup"><span data-stu-id="37c0f-133">aba#</span></span>
- <span data-ttu-id="37c0f-134">
abarouting#</span><span class="sxs-lookup"><span data-stu-id="37c0f-134">abarouting#</span></span>
- <span data-ttu-id="37c0f-135">
aba number</span><span class="sxs-lookup"><span data-stu-id="37c0f-135">aba number</span></span>
- <span data-ttu-id="37c0f-136">
abaroutingnumber</span><span class="sxs-lookup"><span data-stu-id="37c0f-136">abaroutingnumber</span></span>
- <span data-ttu-id="37c0f-137">
american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="37c0f-137">american bank association routing #</span></span>
- <span data-ttu-id="37c0f-138">
american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="37c0f-138">american bank association routing number</span></span>
- <span data-ttu-id="37c0f-139">
americanbankassociationrouting#</span><span class="sxs-lookup"><span data-stu-id="37c0f-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="37c0f-140">
americanbankassociationroutingnumber</span><span class="sxs-lookup"><span data-stu-id="37c0f-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="37c0f-141">
bank routing number</span><span class="sxs-lookup"><span data-stu-id="37c0f-141">bank routing number</span></span>
- <span data-ttu-id="37c0f-142">
bankrouting#</span><span class="sxs-lookup"><span data-stu-id="37c0f-142">bankrouting#</span></span>
- <span data-ttu-id="37c0f-143">
bankroutingnumber</span><span class="sxs-lookup"><span data-stu-id="37c0f-143">bankroutingnumber</span></span>
- <span data-ttu-id="37c0f-144">
routing transit number</span><span class="sxs-lookup"><span data-stu-id="37c0f-144">routing transit number</span></span>
- <span data-ttu-id="37c0f-145">
RTN
</span><span class="sxs-lookup"><span data-stu-id="37c0f-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="37c0f-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="37c0f-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-147">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-147">Format</span></span>

<span data-ttu-id="37c0f-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="37c0f-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-149">Pattern</span></span>

<span data-ttu-id="37c0f-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-150">Eight digits:</span></span>
- <span data-ttu-id="37c0f-151">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-151">Two digits</span></span>
- <span data-ttu-id="37c0f-152">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-152">A period</span></span>
- <span data-ttu-id="37c0f-153">три цифры; </span><span class="sxs-lookup"><span data-stu-id="37c0f-153">Three digits</span></span>
- <span data-ttu-id="37c0f-154">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-154">A period</span></span>
- <span data-ttu-id="37c0f-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-156">Checksum</span></span>

<span data-ttu-id="37c0f-157">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-158">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-158">Definition</span></span>

<span data-ttu-id="37c0f-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="37c0f-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="37c0f-163">Кэйворд_аржентина_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="37c0f-164">Argentina National Identity number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="37c0f-165">Идентификация</span><span class="sxs-lookup"><span data-stu-id="37c0f-165">Identity</span></span> 
- <span data-ttu-id="37c0f-166">Идентификация национальной идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="37c0f-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="37c0f-167">DNI
</span><span class="sxs-lookup"><span data-stu-id="37c0f-167">DNI</span></span> 
- <span data-ttu-id="37c0f-168">Национальная реестр пользователей NIC</span><span class="sxs-lookup"><span data-stu-id="37c0f-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="37c0f-169">Documento Nacional de Identidad
</span><span class="sxs-lookup"><span data-stu-id="37c0f-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="37c0f-170">Registro Nacional de las Personas
</span><span class="sxs-lookup"><span data-stu-id="37c0f-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="37c0f-171">Identidad
</span><span class="sxs-lookup"><span data-stu-id="37c0f-171">Identidad</span></span> 
- <span data-ttu-id="37c0f-172">Identificación
</span><span class="sxs-lookup"><span data-stu-id="37c0f-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="37c0f-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="37c0f-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-174">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-174">Format</span></span>

<span data-ttu-id="37c0f-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="37c0f-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-176">Pattern</span></span>

<span data-ttu-id="37c0f-p103">Номер счета — 6-10 цифр. Номер филиала банковского состояния Австралии:</span><span class="sxs-lookup"><span data-stu-id="37c0f-p103">Account number is 6-10 digits. Australia bank state branch number:</span></span>
- <span data-ttu-id="37c0f-179">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-179">Three digits</span></span> 
- <span data-ttu-id="37c0f-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-180">A hyphen</span></span> 
- <span data-ttu-id="37c0f-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-182">Checksum</span></span>

<span data-ttu-id="37c0f-183">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-184">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-184">Definition</span></span>

<span data-ttu-id="37c0f-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="37c0f-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="37c0f-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="37c0f-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="37c0f-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="37c0f-193">Кэйворд_аустралиа_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="37c0f-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="37c0f-194">swift bank code</span></span>
- <span data-ttu-id="37c0f-195">
correspondent bank</span><span class="sxs-lookup"><span data-stu-id="37c0f-195">correspondent bank</span></span>
- <span data-ttu-id="37c0f-196">
base currency</span><span class="sxs-lookup"><span data-stu-id="37c0f-196">base currency</span></span>
- <span data-ttu-id="37c0f-197">
usa account</span><span class="sxs-lookup"><span data-stu-id="37c0f-197">usa account</span></span>
- <span data-ttu-id="37c0f-198">
holder address</span><span class="sxs-lookup"><span data-stu-id="37c0f-198">holder address</span></span>
- <span data-ttu-id="37c0f-199">
bank address</span><span class="sxs-lookup"><span data-stu-id="37c0f-199">bank address</span></span>
- <span data-ttu-id="37c0f-200">
information account</span><span class="sxs-lookup"><span data-stu-id="37c0f-200">information account</span></span>
- <span data-ttu-id="37c0f-201">
fund transfers</span><span class="sxs-lookup"><span data-stu-id="37c0f-201">fund transfers</span></span>
- <span data-ttu-id="37c0f-202">
bank charges</span><span class="sxs-lookup"><span data-stu-id="37c0f-202">bank charges</span></span>
- <span data-ttu-id="37c0f-203">
bank details</span><span class="sxs-lookup"><span data-stu-id="37c0f-203">bank details</span></span>
- <span data-ttu-id="37c0f-204">
banking information</span><span class="sxs-lookup"><span data-stu-id="37c0f-204">banking information</span></span>
- <span data-ttu-id="37c0f-205">
full names</span><span class="sxs-lookup"><span data-stu-id="37c0f-205">full names</span></span>
- <span data-ttu-id="37c0f-206">

iaea</span><span class="sxs-lookup"><span data-stu-id="37c0f-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="37c0f-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="37c0f-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-208">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-208">Format</span></span>

<span data-ttu-id="37c0f-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-210">Pattern</span></span>

<span data-ttu-id="37c0f-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="37c0f-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-213">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-213">Two digits</span></span> 
- <span data-ttu-id="37c0f-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="37c0f-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="37c0f-215">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="37c0f-215">OR</span></span>

- <span data-ttu-id="37c0f-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-217">4-9 digits</span></span>

<span data-ttu-id="37c0f-218">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="37c0f-218">OR</span></span>

- <span data-ttu-id="37c0f-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="37c0f-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-220">Checksum</span></span>

<span data-ttu-id="37c0f-221">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-222">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-222">Definition</span></span>

<span data-ttu-id="37c0f-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="37c0f-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="37c0f-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="37c0f-228">Кэйворд_аустралиа_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="37c0f-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="37c0f-229">international driving permits</span></span>
- <span data-ttu-id="37c0f-230">
australian automobile association</span><span class="sxs-lookup"><span data-stu-id="37c0f-230">australian automobile association</span></span>
- <span data-ttu-id="37c0f-231">
international driving permit</span><span class="sxs-lookup"><span data-stu-id="37c0f-231">international driving permit</span></span>
- <span data-ttu-id="37c0f-232">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="37c0f-232">DriverLicence</span></span>
- <span data-ttu-id="37c0f-233">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-233">DriverLicences</span></span>
- <span data-ttu-id="37c0f-234">Драйвер Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-234">Driver Lic</span></span>
- <span data-ttu-id="37c0f-235">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-235">Driver Licence</span></span>
- <span data-ttu-id="37c0f-236">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-236">Driver Licences</span></span>
- <span data-ttu-id="37c0f-237">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="37c0f-237">DriversLic</span></span>
- <span data-ttu-id="37c0f-238">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="37c0f-238">DriversLicence</span></span>
- <span data-ttu-id="37c0f-239">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-239">DriversLicences</span></span>
- <span data-ttu-id="37c0f-240">Драйверы Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-240">Drivers Lic</span></span>
- <span data-ttu-id="37c0f-241">Драйверы ликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-241">Drivers Lics</span></span>
- <span data-ttu-id="37c0f-242">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-242">Drivers Licence</span></span>
- <span data-ttu-id="37c0f-243">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-243">Drivers Licences</span></span>
- <span data-ttu-id="37c0f-244">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="37c0f-244">Driver'Lic</span></span>
- <span data-ttu-id="37c0f-245">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="37c0f-245">Driver'Lics</span></span>
- <span data-ttu-id="37c0f-246">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="37c0f-246">Driver'Licence</span></span>
- <span data-ttu-id="37c0f-247">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="37c0f-247">Driver'Licences</span></span>
- <span data-ttu-id="37c0f-248">Драйвер "Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-248">Driver' Lic</span></span>
- <span data-ttu-id="37c0f-249">Драйвер "ЛИКС</span><span class="sxs-lookup"><span data-stu-id="37c0f-249">Driver' Lics</span></span>
- <span data-ttu-id="37c0f-250">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-250">Driver' Licence</span></span>
- <span data-ttu-id="37c0f-251">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-251">Driver' Licences</span></span>
- <span data-ttu-id="37c0f-252">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="37c0f-252">Driver'sLic</span></span>
- <span data-ttu-id="37c0f-253">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-253">Driver'sLics</span></span>
- <span data-ttu-id="37c0f-254">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="37c0f-254">Driver'sLicence</span></span>
- <span data-ttu-id="37c0f-255">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-255">Driver'sLicences</span></span>
- <span data-ttu-id="37c0f-256">Лик драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-256">Driver's Lic</span></span>
- <span data-ttu-id="37c0f-257">Ликс драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-257">Driver's Lics</span></span>
- <span data-ttu-id="37c0f-258">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-258">Driver's Licence</span></span>
- <span data-ttu-id="37c0f-259">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-259">Driver's Licences</span></span>
- <span data-ttu-id="37c0f-260">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-260">DriverLic#</span></span>
- <span data-ttu-id="37c0f-261">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-261">DriverLics#</span></span>
- <span data-ttu-id="37c0f-262">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="37c0f-262">DriverLicence#</span></span>
- <span data-ttu-id="37c0f-263">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-263">DriverLicences#</span></span>
- <span data-ttu-id="37c0f-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="37c0f-264">Driver Lic#</span></span>
- <span data-ttu-id="37c0f-265">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-265">Driver Lics#</span></span>
- <span data-ttu-id="37c0f-266">Лицензия на драйвер #</span><span class="sxs-lookup"><span data-stu-id="37c0f-266">Driver Licence#</span></span>
- <span data-ttu-id="37c0f-267">Лицензия на драйвер #</span><span class="sxs-lookup"><span data-stu-id="37c0f-267">Driver Licences#</span></span>
- <span data-ttu-id="37c0f-268">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-268">DriversLic#</span></span>
- <span data-ttu-id="37c0f-269">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-269">DriversLics#</span></span>
- <span data-ttu-id="37c0f-270">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="37c0f-270">DriversLicence#</span></span>
- <span data-ttu-id="37c0f-271">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-271">DriversLicences#</span></span>
- <span data-ttu-id="37c0f-272">Drivers Лик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-272">Drivers Lic#</span></span>
- <span data-ttu-id="37c0f-273">Drivers ликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-273">Drivers Lics#</span></span>
- <span data-ttu-id="37c0f-274">Драйвер, лицензия #</span><span class="sxs-lookup"><span data-stu-id="37c0f-274">Drivers Licence#</span></span>
- <span data-ttu-id="37c0f-275">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-275">Drivers Licences#</span></span>
- <span data-ttu-id="37c0f-276">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-276">Driver'Lic#</span></span>
- <span data-ttu-id="37c0f-277">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-277">Driver'Lics#</span></span>
- <span data-ttu-id="37c0f-278">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-278">Driver'Licence#</span></span>
- <span data-ttu-id="37c0f-279">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-279">Driver'Licences#</span></span>
- <span data-ttu-id="37c0f-280">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-280">Driver' Lic#</span></span>
- <span data-ttu-id="37c0f-281">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-281">Driver' Lics#</span></span>
- <span data-ttu-id="37c0f-282">Драйвер "водительская лицензия"</span><span class="sxs-lookup"><span data-stu-id="37c0f-282">Driver' Licence#</span></span>
- <span data-ttu-id="37c0f-283">Водитель # число лицензий</span><span class="sxs-lookup"><span data-stu-id="37c0f-283">Driver' Licences#</span></span>
- <span data-ttu-id="37c0f-284">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-284">Driver'sLic#</span></span>
- <span data-ttu-id="37c0f-285">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-285">Driver'sLics#</span></span>
- <span data-ttu-id="37c0f-286">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="37c0f-286">Driver'sLicence#</span></span>
- <span data-ttu-id="37c0f-287">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-287">Driver'sLicences#</span></span>
- <span data-ttu-id="37c0f-288">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-288">Driver's Lic#</span></span>
- <span data-ttu-id="37c0f-289">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-289">Driver's Lics#</span></span>
- <span data-ttu-id="37c0f-290">Номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-290">Driver's Licence#</span></span>
- <span data-ttu-id="37c0f-291">Лицензии на драйвер #</span><span class="sxs-lookup"><span data-stu-id="37c0f-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="37c0f-292">Кэйворд_аустралиа_дриверс_лиценсе_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="37c0f-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="37c0f-293">aaa</span><span class="sxs-lookup"><span data-stu-id="37c0f-293">aaa</span></span>
- <span data-ttu-id="37c0f-294">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-294">DriverLicense</span></span>
- <span data-ttu-id="37c0f-295">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-295">DriverLicenses</span></span>
- <span data-ttu-id="37c0f-296">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-296">Driver License</span></span>
- <span data-ttu-id="37c0f-297">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-297">Driver Licenses</span></span>
- <span data-ttu-id="37c0f-298">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-298">DriversLicense</span></span>
- <span data-ttu-id="37c0f-299">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-299">DriversLicenses</span></span>
- <span data-ttu-id="37c0f-300">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-300">Drivers License</span></span>
- <span data-ttu-id="37c0f-301">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-301">Drivers Licenses</span></span>
- <span data-ttu-id="37c0f-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="37c0f-302">Driver'License</span></span>
- <span data-ttu-id="37c0f-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="37c0f-303">Driver'Licenses</span></span>
- <span data-ttu-id="37c0f-304">Лицензия "Driver"</span><span class="sxs-lookup"><span data-stu-id="37c0f-304">Driver' License</span></span>
- <span data-ttu-id="37c0f-305">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-305">Driver' Licenses</span></span>
- <span data-ttu-id="37c0f-306">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-306">Driver'sLicense</span></span>
- <span data-ttu-id="37c0f-307">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-307">Driver'sLicenses</span></span>
- <span data-ttu-id="37c0f-308">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-308">Driver's License</span></span>
- <span data-ttu-id="37c0f-309">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-309">Driver's Licenses</span></span>
- <span data-ttu-id="37c0f-310">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-310">DriverLicense#</span></span>
- <span data-ttu-id="37c0f-311">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-311">DriverLicenses#</span></span>
- <span data-ttu-id="37c0f-312">Номер лицензии драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-312">Driver License#</span></span>
- <span data-ttu-id="37c0f-313">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-313">Driver Licenses#</span></span>
- <span data-ttu-id="37c0f-314">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-314">DriversLicense#</span></span>
- <span data-ttu-id="37c0f-315">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-315">DriversLicenses#</span></span>
- <span data-ttu-id="37c0f-316">Driver License #</span><span class="sxs-lookup"><span data-stu-id="37c0f-316">Drivers License#</span></span>
- <span data-ttu-id="37c0f-317">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-317">Drivers Licenses#</span></span>
- <span data-ttu-id="37c0f-318">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-318">Driver'License#</span></span>
- <span data-ttu-id="37c0f-319">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-319">Driver'Licenses#</span></span>
- <span data-ttu-id="37c0f-320">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-320">Driver' License#</span></span>
- <span data-ttu-id="37c0f-321">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-321">Driver' Licenses#</span></span>
- <span data-ttu-id="37c0f-322">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-322">Driver'sLicense#</span></span>
- <span data-ttu-id="37c0f-323">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="37c0f-324">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-324">Driver's License#</span></span>
- <span data-ttu-id="37c0f-325">

Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="37c0f-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="37c0f-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="37c0f-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-327">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-327">Format</span></span>

<span data-ttu-id="37c0f-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-329">Pattern</span></span>

<span data-ttu-id="37c0f-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-330">10-11 digits:</span></span>
- <span data-ttu-id="37c0f-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="37c0f-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="37c0f-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="37c0f-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="37c0f-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="37c0f-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="37c0f-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-335">Checksum</span></span>

<span data-ttu-id="37c0f-336">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-337">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-337">Definition</span></span>

<span data-ttu-id="37c0f-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="37c0f-341">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-341">The checksum passes.</span></span>

<span data-ttu-id="37c0f-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="37c0f-346">Кэйворд_аустралиа_медикал_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="37c0f-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="37c0f-347">bank account details</span></span>
- <span data-ttu-id="37c0f-348">
medicare payments</span><span class="sxs-lookup"><span data-stu-id="37c0f-348">medicare payments</span></span>
- <span data-ttu-id="37c0f-349">
mortgage account</span><span class="sxs-lookup"><span data-stu-id="37c0f-349">mortgage account</span></span>
- <span data-ttu-id="37c0f-350">
bank payments</span><span class="sxs-lookup"><span data-stu-id="37c0f-350">bank payments</span></span>
- <span data-ttu-id="37c0f-351">
information branch</span><span class="sxs-lookup"><span data-stu-id="37c0f-351">information branch</span></span>
- <span data-ttu-id="37c0f-352">
credit card loan</span><span class="sxs-lookup"><span data-stu-id="37c0f-352">credit card loan</span></span>
- <span data-ttu-id="37c0f-353">
department of human services</span><span class="sxs-lookup"><span data-stu-id="37c0f-353">department of human services</span></span>
- <span data-ttu-id="37c0f-354">Локальная служба</span><span class="sxs-lookup"><span data-stu-id="37c0f-354">local service</span></span>
- <span data-ttu-id="37c0f-355">

medicare</span><span class="sxs-lookup"><span data-stu-id="37c0f-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="37c0f-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="37c0f-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-357">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-357">Format</span></span>

<span data-ttu-id="37c0f-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-359">Pattern</span></span>

<span data-ttu-id="37c0f-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-361">Checksum</span></span>

<span data-ttu-id="37c0f-362">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-363">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-363">Definition</span></span>

<span data-ttu-id="37c0f-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-366">Найдено ключевое слово из Кэйворд_пасспорт или Кэйворд_аустралиа_пасспорт_нумбер.</span><span class="sxs-lookup"><span data-stu-id="37c0f-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="37c0f-368">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-368">Keyword_passport</span></span>

- <span data-ttu-id="37c0f-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-369">Passport Number</span></span>
- <span data-ttu-id="37c0f-370">
Passport No</span><span class="sxs-lookup"><span data-stu-id="37c0f-370">Passport No</span></span>
- <span data-ttu-id="37c0f-371">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-371">Passport #</span></span>
- <span data-ttu-id="37c0f-372">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-372">Passport#</span></span>
- <span data-ttu-id="37c0f-373">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="37c0f-373">PassportID</span></span>
- <span data-ttu-id="37c0f-374">Passportno
</span><span class="sxs-lookup"><span data-stu-id="37c0f-374">Passportno</span></span>
- <span data-ttu-id="37c0f-375">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-375">passportnumber</span></span>
- <span data-ttu-id="37c0f-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="37c0f-376">パスポート</span></span>
- <span data-ttu-id="37c0f-377">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-377">パスポート番号</span></span>
- <span data-ttu-id="37c0f-378">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-378">パスポートのNum</span></span>
- <span data-ttu-id="37c0f-379">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-379">パスポート ＃</span></span> 
- <span data-ttu-id="37c0f-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="37c0f-380">Numéro de passeport</span></span>
- <span data-ttu-id="37c0f-381">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="37c0f-381">Passeport n °</span></span>
- <span data-ttu-id="37c0f-382">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="37c0f-382">Passeport Non</span></span>
- <span data-ttu-id="37c0f-383">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-383">Passeport #</span></span>
- <span data-ttu-id="37c0f-384">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-384">Passeport#</span></span>
- <span data-ttu-id="37c0f-385">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="37c0f-385">PasseportNon</span></span>
- <span data-ttu-id="37c0f-386">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="37c0f-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="37c0f-387">Кэйворд_аустралиа_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="37c0f-388">passport</span><span class="sxs-lookup"><span data-stu-id="37c0f-388">passport</span></span>
- <span data-ttu-id="37c0f-389">
passport details</span><span class="sxs-lookup"><span data-stu-id="37c0f-389">passport details</span></span>
- <span data-ttu-id="37c0f-390">
immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="37c0f-390">immigration and citizenship</span></span>
- <span data-ttu-id="37c0f-391">
commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="37c0f-391">commonwealth of australia</span></span>
- <span data-ttu-id="37c0f-392">
department of immigration</span><span class="sxs-lookup"><span data-stu-id="37c0f-392">department of immigration</span></span>
- <span data-ttu-id="37c0f-393">
residential address</span><span class="sxs-lookup"><span data-stu-id="37c0f-393">residential address</span></span>
- <span data-ttu-id="37c0f-394">
department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="37c0f-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="37c0f-395">visa
</span><span class="sxs-lookup"><span data-stu-id="37c0f-395">visa</span></span>
- <span data-ttu-id="37c0f-396">
national identity card</span><span class="sxs-lookup"><span data-stu-id="37c0f-396">national identity card</span></span>
- <span data-ttu-id="37c0f-397">номер паспорта</span><span class="sxs-lookup"><span data-stu-id="37c0f-397">passport number</span></span>
- <span data-ttu-id="37c0f-398">
travel document</span><span class="sxs-lookup"><span data-stu-id="37c0f-398">travel document</span></span>
- <span data-ttu-id="37c0f-399">

issuing authority</span><span class="sxs-lookup"><span data-stu-id="37c0f-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="37c0f-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="37c0f-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-401">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-401">Format</span></span>

<span data-ttu-id="37c0f-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-403">Pattern</span></span>

<span data-ttu-id="37c0f-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="37c0f-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="37c0f-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-405">Three digits</span></span> 
- <span data-ttu-id="37c0f-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="37c0f-406">An optional space</span></span> 
- <span data-ttu-id="37c0f-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-407">Three digits</span></span> 
- <span data-ttu-id="37c0f-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="37c0f-408">An optional space</span></span> 
- <span data-ttu-id="37c0f-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="37c0f-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-410">Checksum</span></span>

<span data-ttu-id="37c0f-411">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-412">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-412">Definition</span></span>

<span data-ttu-id="37c0f-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="37c0f-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="37c0f-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="37c0f-418">Кэйворд_аустралиа_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="37c0f-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="37c0f-419">australian business number</span></span>
- <span data-ttu-id="37c0f-420">
marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="37c0f-420">marginal tax rate</span></span>
- <span data-ttu-id="37c0f-421">
medicare levy</span><span class="sxs-lookup"><span data-stu-id="37c0f-421">medicare levy</span></span>
- <span data-ttu-id="37c0f-422">
portfolio number</span><span class="sxs-lookup"><span data-stu-id="37c0f-422">portfolio number</span></span>
- <span data-ttu-id="37c0f-423">
service veterans</span><span class="sxs-lookup"><span data-stu-id="37c0f-423">service veterans</span></span>
- <span data-ttu-id="37c0f-424">
withholding tax</span><span class="sxs-lookup"><span data-stu-id="37c0f-424">withholding tax</span></span>
- <span data-ttu-id="37c0f-425">
individual tax return</span><span class="sxs-lookup"><span data-stu-id="37c0f-425">individual tax return</span></span>
- <span data-ttu-id="37c0f-426">

tax file number</span><span class="sxs-lookup"><span data-stu-id="37c0f-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="37c0f-427">Кэйворд_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="37c0f-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="37c0f-428">00000001</span><span class="sxs-lookup"><span data-stu-id="37c0f-428">00000000</span></span>
- <span data-ttu-id="37c0f-429">11111111</span><span class="sxs-lookup"><span data-stu-id="37c0f-429">11111111</span></span>
- <span data-ttu-id="37c0f-430">22222222</span><span class="sxs-lookup"><span data-stu-id="37c0f-430">22222222</span></span>
- <span data-ttu-id="37c0f-431">33333333</span><span class="sxs-lookup"><span data-stu-id="37c0f-431">33333333</span></span>
- <span data-ttu-id="37c0f-432">44444444</span><span class="sxs-lookup"><span data-stu-id="37c0f-432">44444444</span></span>
- <span data-ttu-id="37c0f-433">55555555</span><span class="sxs-lookup"><span data-stu-id="37c0f-433">55555555</span></span>
- <span data-ttu-id="37c0f-434">66666666</span><span class="sxs-lookup"><span data-stu-id="37c0f-434">66666666</span></span>
- <span data-ttu-id="37c0f-435">77777777</span><span class="sxs-lookup"><span data-stu-id="37c0f-435">77777777</span></span>
- <span data-ttu-id="37c0f-436">88888888</span><span class="sxs-lookup"><span data-stu-id="37c0f-436">88888888</span></span>
- <span data-ttu-id="37c0f-437">99999999</span><span class="sxs-lookup"><span data-stu-id="37c0f-437">99999999</span></span>
- <span data-ttu-id="37c0f-438">000000000</span><span class="sxs-lookup"><span data-stu-id="37c0f-438">000000000</span></span>
- <span data-ttu-id="37c0f-439">111111111</span><span class="sxs-lookup"><span data-stu-id="37c0f-439">111111111</span></span>
- <span data-ttu-id="37c0f-440">222222222</span><span class="sxs-lookup"><span data-stu-id="37c0f-440">222222222</span></span>
- <span data-ttu-id="37c0f-441">333333333</span><span class="sxs-lookup"><span data-stu-id="37c0f-441">333333333</span></span>
- <span data-ttu-id="37c0f-442">444444444</span><span class="sxs-lookup"><span data-stu-id="37c0f-442">444444444</span></span>
- <span data-ttu-id="37c0f-443">555555555</span><span class="sxs-lookup"><span data-stu-id="37c0f-443">555555555</span></span>
- <span data-ttu-id="37c0f-444">666666666</span><span class="sxs-lookup"><span data-stu-id="37c0f-444">666666666</span></span>
- <span data-ttu-id="37c0f-445">777777777</span><span class="sxs-lookup"><span data-stu-id="37c0f-445">777777777</span></span>
- <span data-ttu-id="37c0f-446">888888888</span><span class="sxs-lookup"><span data-stu-id="37c0f-446">888888888</span></span>
- <span data-ttu-id="37c0f-447">999999999</span><span class="sxs-lookup"><span data-stu-id="37c0f-447">999999999</span></span>
- <span data-ttu-id="37c0f-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="37c0f-448">0000000000</span></span>
- <span data-ttu-id="37c0f-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="37c0f-449">1111111111</span></span>
- <span data-ttu-id="37c0f-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="37c0f-450">2222222222</span></span>
- <span data-ttu-id="37c0f-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="37c0f-451">3333333333</span></span>
- <span data-ttu-id="37c0f-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="37c0f-452">4444444444</span></span>
- <span data-ttu-id="37c0f-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="37c0f-453">5555555555</span></span>
- <span data-ttu-id="37c0f-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="37c0f-454">6666666666</span></span>
- <span data-ttu-id="37c0f-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="37c0f-455">7777777777</span></span>
- <span data-ttu-id="37c0f-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="37c0f-456">8888888888</span></span>
- <span data-ttu-id="37c0f-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="37c0f-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="37c0f-458">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="37c0f-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-459">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-459">Format</span></span>

<span data-ttu-id="37c0f-460">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="37c0f-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-461">Pattern</span></span>

<span data-ttu-id="37c0f-462">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="37c0f-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="37c0f-463">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="37c0f-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="37c0f-464">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-464">A hyphen</span></span> 
- <span data-ttu-id="37c0f-465">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="37c0f-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="37c0f-466">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-466">A period</span></span> 
- <span data-ttu-id="37c0f-467">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-468">Checksum</span></span>

<span data-ttu-id="37c0f-469">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-470">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-470">Definition</span></span>

<span data-ttu-id="37c0f-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-472">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-473">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="37c0f-474">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-475">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="37c0f-476">Кэйворд_белгиум_натионал_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="37c0f-477">Identity</span><span class="sxs-lookup"><span data-stu-id="37c0f-477">Identity</span></span>
- <span data-ttu-id="37c0f-478">Registration</span><span class="sxs-lookup"><span data-stu-id="37c0f-478">Registration</span></span>
- <span data-ttu-id="37c0f-479">Identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-479">Identification</span></span> 
- <span data-ttu-id="37c0f-480">ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-480">ID</span></span> 
- <span data-ttu-id="37c0f-481">Identiteitskaart</span><span class="sxs-lookup"><span data-stu-id="37c0f-481">Identiteitskaart</span></span>
- <span data-ttu-id="37c0f-482">Registratie nummer 
</span><span class="sxs-lookup"><span data-stu-id="37c0f-482">Registratie nummer</span></span> 
- <span data-ttu-id="37c0f-483">Identificatie nummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-483">Identificatie nummer</span></span> 
- <span data-ttu-id="37c0f-484">Identiteit</span><span class="sxs-lookup"><span data-stu-id="37c0f-484">Identiteit</span></span>
- <span data-ttu-id="37c0f-485">Registratie</span><span class="sxs-lookup"><span data-stu-id="37c0f-485">Registratie</span></span>
- <span data-ttu-id="37c0f-486">Identificatie

</span><span class="sxs-lookup"><span data-stu-id="37c0f-486">Identificatie</span></span> 
- <span data-ttu-id="37c0f-487">Carte d’identité
</span><span class="sxs-lookup"><span data-stu-id="37c0f-487">Carte d’identité</span></span> 
- <span data-ttu-id="37c0f-488">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="37c0f-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="37c0f-489">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-489">numéro d'identification</span></span>
- <span data-ttu-id="37c0f-490">
identité
</span><span class="sxs-lookup"><span data-stu-id="37c0f-490">identité</span></span> 
- <span data-ttu-id="37c0f-491">inscription
</span><span class="sxs-lookup"><span data-stu-id="37c0f-491">inscription</span></span> 
- <span data-ttu-id="37c0f-492">Identifikation</span><span class="sxs-lookup"><span data-stu-id="37c0f-492">Identifikation</span></span>
- <span data-ttu-id="37c0f-493">Identifizierung</span><span class="sxs-lookup"><span data-stu-id="37c0f-493">Identifizierung</span></span>
- <span data-ttu-id="37c0f-494">Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-494">Identifikationsnummer</span></span>
- <span data-ttu-id="37c0f-495">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="37c0f-495">Personalausweis</span></span>
- <span data-ttu-id="37c0f-496">Registrierung</span><span class="sxs-lookup"><span data-stu-id="37c0f-496">Registrierung</span></span>
- <span data-ttu-id="37c0f-497">Registrationsnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="37c0f-498">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="37c0f-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-499">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-499">Format</span></span>

<span data-ttu-id="37c0f-500">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="37c0f-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-501">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-501">Pattern</span></span>

<span data-ttu-id="37c0f-502">С форматированием</span><span class="sxs-lookup"><span data-stu-id="37c0f-502">Formatted:</span></span>
- <span data-ttu-id="37c0f-503">три цифры; </span><span class="sxs-lookup"><span data-stu-id="37c0f-503">Three digits</span></span> 
- <span data-ttu-id="37c0f-504">точка; </span><span class="sxs-lookup"><span data-stu-id="37c0f-504">A period</span></span> 
- <span data-ttu-id="37c0f-505">три цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-505">Three digits</span></span> 
- <span data-ttu-id="37c0f-506">точка; </span><span class="sxs-lookup"><span data-stu-id="37c0f-506">A period</span></span> 
- <span data-ttu-id="37c0f-507">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-507">Three digits</span></span> 
- <span data-ttu-id="37c0f-508">Дефис</span><span class="sxs-lookup"><span data-stu-id="37c0f-508">A hyphen</span></span> 
- <span data-ttu-id="37c0f-509">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-509">Two digits which are check digits</span></span>

<span data-ttu-id="37c0f-510">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="37c0f-510">Unformatted:</span></span>
- <span data-ttu-id="37c0f-511">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="37c0f-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-512">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-512">Checksum</span></span>

<span data-ttu-id="37c0f-513">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-514">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-514">Definition</span></span>

<span data-ttu-id="37c0f-515">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-516">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-517">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="37c0f-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="37c0f-518">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-518">The checksum passes.</span></span>

<span data-ttu-id="37c0f-519">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-520">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-521">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-521">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-522">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="37c0f-523">Кэйворд_бразил_кпф</span><span class="sxs-lookup"><span data-stu-id="37c0f-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="37c0f-524">CPF</span><span class="sxs-lookup"><span data-stu-id="37c0f-524">CPF</span></span>
- <span data-ttu-id="37c0f-525">Identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-525">Identification</span></span>
- <span data-ttu-id="37c0f-526">Registration</span><span class="sxs-lookup"><span data-stu-id="37c0f-526">Registration</span></span>
- <span data-ttu-id="37c0f-527">Revenue</span><span class="sxs-lookup"><span data-stu-id="37c0f-527">Revenue</span></span>
- <span data-ttu-id="37c0f-528">Cadastro de Pessoas Físicas
</span><span class="sxs-lookup"><span data-stu-id="37c0f-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="37c0f-529">Imposto
</span><span class="sxs-lookup"><span data-stu-id="37c0f-529">Imposto</span></span> 
- <span data-ttu-id="37c0f-530">Identificação
</span><span class="sxs-lookup"><span data-stu-id="37c0f-530">Identificação</span></span> 
- <span data-ttu-id="37c0f-531">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="37c0f-531">Inscrição</span></span> 
- <span data-ttu-id="37c0f-532">Receita

</span><span class="sxs-lookup"><span data-stu-id="37c0f-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="37c0f-533">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="37c0f-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-534">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-534">Format</span></span>

<span data-ttu-id="37c0f-535">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="37c0f-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-536">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-536">Pattern</span></span>
<span data-ttu-id="37c0f-537">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="37c0f-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="37c0f-538">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-538">Two digits</span></span> 
- <span data-ttu-id="37c0f-539">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-539">A period</span></span> 
- <span data-ttu-id="37c0f-540">три цифры; </span><span class="sxs-lookup"><span data-stu-id="37c0f-540">Three digits</span></span> 
- <span data-ttu-id="37c0f-541">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-541">A period</span></span> 
- <span data-ttu-id="37c0f-542">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="37c0f-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="37c0f-543">косая черта;</span><span class="sxs-lookup"><span data-stu-id="37c0f-543">A forward slash</span></span> 
- <span data-ttu-id="37c0f-544">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-544">Four-digit branch number</span></span> 
- <span data-ttu-id="37c0f-545">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-545">A hyphen</span></span> 
- <span data-ttu-id="37c0f-546">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-547">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-547">Checksum</span></span>

<span data-ttu-id="37c0f-548">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-549">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-549">Definition</span></span>

<span data-ttu-id="37c0f-550">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-551">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-552">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="37c0f-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="37c0f-553">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-553">The checksum passes.</span></span>

<span data-ttu-id="37c0f-554">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-555">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-556">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-556">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-557">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="37c0f-558">Кэйворд_бразил_кнпж</span><span class="sxs-lookup"><span data-stu-id="37c0f-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="37c0f-559">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="37c0f-559">CNPJ</span></span> 
- <span data-ttu-id="37c0f-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="37c0f-560">CNPJ/MF</span></span> 
- <span data-ttu-id="37c0f-561">CNPJ-MF
</span><span class="sxs-lookup"><span data-stu-id="37c0f-561">CNPJ-MF</span></span> 
- <span data-ttu-id="37c0f-562">National Registry of Legal Entities
</span><span class="sxs-lookup"><span data-stu-id="37c0f-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="37c0f-563">Taxpayers Registry
</span><span class="sxs-lookup"><span data-stu-id="37c0f-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="37c0f-564">Legal entity
</span><span class="sxs-lookup"><span data-stu-id="37c0f-564">Legal entity</span></span> 
- <span data-ttu-id="37c0f-565">Legal entities
</span><span class="sxs-lookup"><span data-stu-id="37c0f-565">Legal entities</span></span> 
- <span data-ttu-id="37c0f-566">Registration Status
</span><span class="sxs-lookup"><span data-stu-id="37c0f-566">Registration Status</span></span> 
- <span data-ttu-id="37c0f-567">Business
</span><span class="sxs-lookup"><span data-stu-id="37c0f-567">Business</span></span> 
- <span data-ttu-id="37c0f-568">Company</span><span class="sxs-lookup"><span data-stu-id="37c0f-568">Company</span></span>
- <span data-ttu-id="37c0f-569">CNPJ
</span><span class="sxs-lookup"><span data-stu-id="37c0f-569">CNPJ</span></span> 
- <span data-ttu-id="37c0f-570">Cadastro Nacional da Pessoa Jurídica
</span><span class="sxs-lookup"><span data-stu-id="37c0f-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="37c0f-571">Cadastro Geral de Contribuintes
</span><span class="sxs-lookup"><span data-stu-id="37c0f-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="37c0f-572">CGC
</span><span class="sxs-lookup"><span data-stu-id="37c0f-572">CGC</span></span> 
- <span data-ttu-id="37c0f-573">Pessoa jurídica
</span><span class="sxs-lookup"><span data-stu-id="37c0f-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="37c0f-574">Pessoas jurídicas
</span><span class="sxs-lookup"><span data-stu-id="37c0f-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="37c0f-575">Situação cadastral
</span><span class="sxs-lookup"><span data-stu-id="37c0f-575">Situação cadastral</span></span> 
- <span data-ttu-id="37c0f-576">Inscrição
</span><span class="sxs-lookup"><span data-stu-id="37c0f-576">Inscrição</span></span> 
- <span data-ttu-id="37c0f-577">Empresa
</span><span class="sxs-lookup"><span data-stu-id="37c0f-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="37c0f-578">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="37c0f-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-579">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-579">Format</span></span>

<span data-ttu-id="37c0f-580">Registro Geral (старый формат): девять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="37c0f-581">Registro de identidade (RIC) (новый формат): 11 цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-582">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-582">Pattern</span></span>

<span data-ttu-id="37c0f-583">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="37c0f-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="37c0f-584">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-584">Two digits</span></span> 
- <span data-ttu-id="37c0f-585">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-585">A period</span></span> 
- <span data-ttu-id="37c0f-586">три цифры; </span><span class="sxs-lookup"><span data-stu-id="37c0f-586">Three digits</span></span> 
- <span data-ttu-id="37c0f-587">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-587">A period</span></span> 
- <span data-ttu-id="37c0f-588">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-588">Three digits</span></span> 
- <span data-ttu-id="37c0f-589">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-589">A hyphen</span></span> 
- <span data-ttu-id="37c0f-590">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-590">One digit which is a check digit</span></span>

<span data-ttu-id="37c0f-591">Registro de identidade (RIC) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="37c0f-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="37c0f-592">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-592">10 digits</span></span> 
- <span data-ttu-id="37c0f-593">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-593">A hyphen</span></span> 
- <span data-ttu-id="37c0f-594">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-595">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-595">Checksum</span></span>

<span data-ttu-id="37c0f-596">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-597">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-597">Definition</span></span>

<span data-ttu-id="37c0f-598">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-599">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-600">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="37c0f-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="37c0f-601">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-601">The checksum passes.</span></span>

<span data-ttu-id="37c0f-602">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-603">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-604">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-604">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-605">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="37c0f-606">Кэйворд_бразил_рг</span><span class="sxs-lookup"><span data-stu-id="37c0f-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="37c0f-607">Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр).</span><span class="sxs-lookup"><span data-stu-id="37c0f-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="37c0f-608">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="37c0f-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-609">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-609">Format</span></span>

<span data-ttu-id="37c0f-610">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-611">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-611">Pattern</span></span>

<span data-ttu-id="37c0f-612">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="37c0f-613">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="37c0f-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="37c0f-614">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-614">Five digits</span></span> 
- <span data-ttu-id="37c0f-615">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-615">A hyphen</span></span> 
- <span data-ttu-id="37c0f-616">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="37c0f-616">Three digits OR</span></span>
- <span data-ttu-id="37c0f-617">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="37c0f-617">A zero "0"</span></span> 
- <span data-ttu-id="37c0f-618">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-619">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-619">Checksum</span></span>

<span data-ttu-id="37c0f-620">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-621">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-621">Definition</span></span>

<span data-ttu-id="37c0f-622">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-623">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-624">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="37c0f-625">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="37c0f-626">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-627">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-628">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-629">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="37c0f-630">Кэйворд_канада_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="37c0f-631">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="37c0f-631">canada savings bonds</span></span>
- <span data-ttu-id="37c0f-632">
canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="37c0f-632">canada revenue agency</span></span>
- <span data-ttu-id="37c0f-633">
canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="37c0f-633">canadian financial institution</span></span>
- <span data-ttu-id="37c0f-634">
direct deposit form</span><span class="sxs-lookup"><span data-stu-id="37c0f-634">direct deposit form</span></span>
- <span data-ttu-id="37c0f-635">
canadian citizen</span><span class="sxs-lookup"><span data-stu-id="37c0f-635">canadian citizen</span></span>
- <span data-ttu-id="37c0f-636">
legal representative</span><span class="sxs-lookup"><span data-stu-id="37c0f-636">legal representative</span></span>
- <span data-ttu-id="37c0f-637">
notary public</span><span class="sxs-lookup"><span data-stu-id="37c0f-637">notary public</span></span>
- <span data-ttu-id="37c0f-638">
commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="37c0f-638">commissioner for oaths</span></span>
- <span data-ttu-id="37c0f-639">
child care benefit</span><span class="sxs-lookup"><span data-stu-id="37c0f-639">child care benefit</span></span>
- <span data-ttu-id="37c0f-640">
universal child care</span><span class="sxs-lookup"><span data-stu-id="37c0f-640">universal child care</span></span>
- <span data-ttu-id="37c0f-641">
canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="37c0f-641">canada child tax benefit</span></span>
- <span data-ttu-id="37c0f-642">
income tax benefit</span><span class="sxs-lookup"><span data-stu-id="37c0f-642">income tax benefit</span></span>
- <span data-ttu-id="37c0f-643">
harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="37c0f-643">harmonized sales tax</span></span>
- <span data-ttu-id="37c0f-644">social insurance number</span><span class="sxs-lookup"><span data-stu-id="37c0f-644">social insurance number</span></span>
- <span data-ttu-id="37c0f-645">
income tax refund</span><span class="sxs-lookup"><span data-stu-id="37c0f-645">income tax refund</span></span>
- <span data-ttu-id="37c0f-646">
child tax benefit</span><span class="sxs-lookup"><span data-stu-id="37c0f-646">child tax benefit</span></span>
- <span data-ttu-id="37c0f-647">
territorial payments</span><span class="sxs-lookup"><span data-stu-id="37c0f-647">territorial payments</span></span>
- <span data-ttu-id="37c0f-648">
institution number</span><span class="sxs-lookup"><span data-stu-id="37c0f-648">institution number</span></span>
- <span data-ttu-id="37c0f-649">
deposit request</span><span class="sxs-lookup"><span data-stu-id="37c0f-649">deposit request</span></span>
- <span data-ttu-id="37c0f-650">
banking information</span><span class="sxs-lookup"><span data-stu-id="37c0f-650">banking information</span></span>
- <span data-ttu-id="37c0f-651">

direct deposit</span><span class="sxs-lookup"><span data-stu-id="37c0f-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="37c0f-652">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="37c0f-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-653">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-653">Format</span></span>

<span data-ttu-id="37c0f-654">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="37c0f-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-655">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-655">Pattern</span></span>

<span data-ttu-id="37c0f-656">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="37c0f-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-657">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-657">Checksum</span></span>

<span data-ttu-id="37c0f-658">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-659">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-659">Definition</span></span>

<span data-ttu-id="37c0f-660">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-661">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-662">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="37c0f-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="37c0f-663">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="37c0f-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-664">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="37c0f-665">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="37c0f-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="37c0f-666">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="37c0f-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="37c0f-667">
Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="37c0f-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="37c0f-668">Кэйворд_канада_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="37c0f-669">DL</span><span class="sxs-lookup"><span data-stu-id="37c0f-669">DL</span></span>
- <span data-ttu-id="37c0f-670">DLS</span><span class="sxs-lookup"><span data-stu-id="37c0f-670">DLS</span></span>
- <span data-ttu-id="37c0f-671">КДЛ</span><span class="sxs-lookup"><span data-stu-id="37c0f-671">CDL</span></span>
- <span data-ttu-id="37c0f-672">КДЛС</span><span class="sxs-lookup"><span data-stu-id="37c0f-672">CDLS</span></span>
- <span data-ttu-id="37c0f-673">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="37c0f-673">DriverLic</span></span>
- <span data-ttu-id="37c0f-674">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-674">DriverLics</span></span>
- <span data-ttu-id="37c0f-675">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-675">DriverLicense</span></span>
- <span data-ttu-id="37c0f-676">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-676">DriverLicenses</span></span>
- <span data-ttu-id="37c0f-677">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="37c0f-677">DriverLicence</span></span>
- <span data-ttu-id="37c0f-678">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-678">DriverLicences</span></span>
- <span data-ttu-id="37c0f-679">Драйвер Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-679">Driver Lic</span></span>
- <span data-ttu-id="37c0f-680">Драйвер ликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-680">Driver Lics</span></span>
- <span data-ttu-id="37c0f-681">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-681">Driver License</span></span>
- <span data-ttu-id="37c0f-682">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-682">Driver Licenses</span></span>
- <span data-ttu-id="37c0f-683">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-683">Driver Licence</span></span>
- <span data-ttu-id="37c0f-684">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-684">Driver Licences</span></span>
- <span data-ttu-id="37c0f-685">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="37c0f-685">DriversLic</span></span>
- <span data-ttu-id="37c0f-686">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-686">DriversLics</span></span>
- <span data-ttu-id="37c0f-687">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="37c0f-687">DriversLicence</span></span>
- <span data-ttu-id="37c0f-688">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-688">DriversLicences</span></span>
- <span data-ttu-id="37c0f-689">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-689">DriversLicense</span></span>
- <span data-ttu-id="37c0f-690">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-690">DriversLicenses</span></span>
- <span data-ttu-id="37c0f-691">Драйверы Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-691">Drivers Lic</span></span>
- <span data-ttu-id="37c0f-692">Драйверы ликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-692">Drivers Lics</span></span>
- <span data-ttu-id="37c0f-693">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-693">Drivers License</span></span>
- <span data-ttu-id="37c0f-694">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-694">Drivers Licenses</span></span>
- <span data-ttu-id="37c0f-695">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-695">Drivers Licence</span></span>
- <span data-ttu-id="37c0f-696">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-696">Drivers Licences</span></span>
- <span data-ttu-id="37c0f-697">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="37c0f-697">Driver'Lic</span></span>
- <span data-ttu-id="37c0f-698">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="37c0f-698">Driver'Lics</span></span>
- <span data-ttu-id="37c0f-699">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="37c0f-699">Driver'License</span></span>
- <span data-ttu-id="37c0f-700">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="37c0f-700">Driver'Licenses</span></span>
- <span data-ttu-id="37c0f-701">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="37c0f-701">Driver'Licence</span></span>
- <span data-ttu-id="37c0f-702">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="37c0f-702">Driver'Licences</span></span>
- <span data-ttu-id="37c0f-703">Драйвер "Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-703">Driver' Lic</span></span>
- <span data-ttu-id="37c0f-704">Драйвер "ЛИКС</span><span class="sxs-lookup"><span data-stu-id="37c0f-704">Driver' Lics</span></span>
- <span data-ttu-id="37c0f-705">Лицензия "Driver"</span><span class="sxs-lookup"><span data-stu-id="37c0f-705">Driver' License</span></span>
- <span data-ttu-id="37c0f-706">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-706">Driver' Licenses</span></span>
- <span data-ttu-id="37c0f-707">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-707">Driver' Licence</span></span>
- <span data-ttu-id="37c0f-708">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-708">Driver' Licences</span></span>
- <span data-ttu-id="37c0f-709">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="37c0f-709">Driver'sLic</span></span>
- <span data-ttu-id="37c0f-710">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-710">Driver'sLics</span></span>
- <span data-ttu-id="37c0f-711">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-711">Driver'sLicense</span></span>
- <span data-ttu-id="37c0f-712">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-712">Driver'sLicenses</span></span>
- <span data-ttu-id="37c0f-713">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="37c0f-713">Driver'sLicence</span></span>
- <span data-ttu-id="37c0f-714">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-714">Driver'sLicences</span></span>
- <span data-ttu-id="37c0f-715">Лик драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-715">Driver's Lic</span></span>
- <span data-ttu-id="37c0f-716">Ликс драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-716">Driver's Lics</span></span>
- <span data-ttu-id="37c0f-717">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-717">Driver's License</span></span>
- <span data-ttu-id="37c0f-718">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-718">Driver's Licenses</span></span>
- <span data-ttu-id="37c0f-719">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-719">Driver's Licence</span></span>
- <span data-ttu-id="37c0f-720">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-720">Driver's Licences</span></span>
- <span data-ttu-id="37c0f-721">Разрешение de Кондуире</span><span class="sxs-lookup"><span data-stu-id="37c0f-721">Permis de Conduire</span></span>
- <span data-ttu-id="37c0f-722">id</span><span class="sxs-lookup"><span data-stu-id="37c0f-722">id</span></span>
- <span data-ttu-id="37c0f-723">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="37c0f-723">ids</span></span>
- <span data-ttu-id="37c0f-724">
idcard number</span><span class="sxs-lookup"><span data-stu-id="37c0f-724">idcard number</span></span>
- <span data-ttu-id="37c0f-725">
idcard numbers</span><span class="sxs-lookup"><span data-stu-id="37c0f-725">idcard numbers</span></span>
- <span data-ttu-id="37c0f-726">
idcard#</span><span class="sxs-lookup"><span data-stu-id="37c0f-726">idcard #</span></span>
- <span data-ttu-id="37c0f-727">
idcard #s</span><span class="sxs-lookup"><span data-stu-id="37c0f-727">idcard #s</span></span>
- <span data-ttu-id="37c0f-728">карточка идкард</span><span class="sxs-lookup"><span data-stu-id="37c0f-728">idcard card</span></span>
- <span data-ttu-id="37c0f-729">карточки идкард</span><span class="sxs-lookup"><span data-stu-id="37c0f-729">idcard cards</span></span>
- <span data-ttu-id="37c0f-730">идкард</span><span class="sxs-lookup"><span data-stu-id="37c0f-730">idcard</span></span>
- <span data-ttu-id="37c0f-731">identification number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-731">identification number</span></span>
- <span data-ttu-id="37c0f-732">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-732">identification numbers</span></span>
- <span data-ttu-id="37c0f-733">identification #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-733">identification #</span></span>
- <span data-ttu-id="37c0f-734">
identification #s</span><span class="sxs-lookup"><span data-stu-id="37c0f-734">identification #s</span></span>
- <span data-ttu-id="37c0f-735">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-735">identification card</span></span>
- <span data-ttu-id="37c0f-736">идентификационные карточки</span><span class="sxs-lookup"><span data-stu-id="37c0f-736">identification cards</span></span>
- <span data-ttu-id="37c0f-737">
identification
</span><span class="sxs-lookup"><span data-stu-id="37c0f-737">identification</span></span> 
- <span data-ttu-id="37c0f-738">DL#</span><span class="sxs-lookup"><span data-stu-id="37c0f-738">DL#</span></span>
- <span data-ttu-id="37c0f-739">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-739">DLS#</span></span> 
- <span data-ttu-id="37c0f-740">CDL#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-740">CDL#</span></span> 
- <span data-ttu-id="37c0f-741">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-741">CDLS#</span></span> 
- <span data-ttu-id="37c0f-742">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-742">DriverLic#</span></span> 
- <span data-ttu-id="37c0f-743">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-743">DriverLics#</span></span> 
- <span data-ttu-id="37c0f-744">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-744">DriverLicense#</span></span> 
- <span data-ttu-id="37c0f-745">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-745">DriverLicenses#</span></span> 
- <span data-ttu-id="37c0f-746">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="37c0f-746">DriverLicence#</span></span> 
- <span data-ttu-id="37c0f-747">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-747">DriverLicences#</span></span> 
- <span data-ttu-id="37c0f-748">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="37c0f-748">Driver Lic#</span></span>
- <span data-ttu-id="37c0f-749">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-749">Driver Lics#</span></span> 
- <span data-ttu-id="37c0f-750">Номер лицензии драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-750">Driver License#</span></span> 
- <span data-ttu-id="37c0f-751">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-751">Driver Licenses#</span></span> 
- <span data-ttu-id="37c0f-752">Номер лицензии драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-752">Driver License#</span></span> 
- <span data-ttu-id="37c0f-753">Лицензия на драйвер #</span><span class="sxs-lookup"><span data-stu-id="37c0f-753">Driver Licences#</span></span> 
- <span data-ttu-id="37c0f-754">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-754">DriversLic#</span></span> 
- <span data-ttu-id="37c0f-755">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-755">DriversLics#</span></span> 
- <span data-ttu-id="37c0f-756">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-756">DriversLicense#</span></span> 
- <span data-ttu-id="37c0f-757">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-757">DriversLicenses#</span></span> 
- <span data-ttu-id="37c0f-758">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="37c0f-758">DriversLicence#</span></span> 
- <span data-ttu-id="37c0f-759">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-759">DriversLicences#</span></span> 
- <span data-ttu-id="37c0f-760">Drivers Лик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-760">Drivers Lic#</span></span> 
- <span data-ttu-id="37c0f-761">Drivers ликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-761">Drivers Lics#</span></span> 
- <span data-ttu-id="37c0f-762">Driver License #</span><span class="sxs-lookup"><span data-stu-id="37c0f-762">Drivers License#</span></span> 
- <span data-ttu-id="37c0f-763">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="37c0f-764">Драйвер, лицензия #</span><span class="sxs-lookup"><span data-stu-id="37c0f-764">Drivers Licence#</span></span> 
- <span data-ttu-id="37c0f-765">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-765">Drivers Licences#</span></span> 
- <span data-ttu-id="37c0f-766">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-766">Driver'Lic#</span></span> 
- <span data-ttu-id="37c0f-767">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-767">Driver'Lics#</span></span> 
- <span data-ttu-id="37c0f-768">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-768">Driver'License#</span></span> 
- <span data-ttu-id="37c0f-769">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="37c0f-770">Driver' Licence#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-770">Driver'Licence#</span></span> 
- <span data-ttu-id="37c0f-771">Driver' Licences#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-771">Driver'Licences#</span></span> 
- <span data-ttu-id="37c0f-772">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-772">Driver' Lic#</span></span> 
- <span data-ttu-id="37c0f-773">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-773">Driver' Lics#</span></span> 
- <span data-ttu-id="37c0f-774">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-774">Driver' License#</span></span> 
- <span data-ttu-id="37c0f-775">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="37c0f-776">Драйвер "водительская лицензия"</span><span class="sxs-lookup"><span data-stu-id="37c0f-776">Driver' Licence#</span></span> 
- <span data-ttu-id="37c0f-777">Водитель # число лицензий</span><span class="sxs-lookup"><span data-stu-id="37c0f-777">Driver' Licences#</span></span> 
- <span data-ttu-id="37c0f-778">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-778">Driver'sLic#</span></span> 
- <span data-ttu-id="37c0f-779">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-779">Driver'sLics#</span></span> 
- <span data-ttu-id="37c0f-780">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="37c0f-781">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="37c0f-782">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="37c0f-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="37c0f-783">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="37c0f-784">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-784">Driver's Lic#</span></span> 
- <span data-ttu-id="37c0f-785">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-785">Driver's Lics#</span></span> 
- <span data-ttu-id="37c0f-786">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-786">Driver's License#</span></span> 
- <span data-ttu-id="37c0f-787">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="37c0f-788">Номер лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-788">Driver's Licence#</span></span> 
- <span data-ttu-id="37c0f-789">Лицензии на драйвер #</span><span class="sxs-lookup"><span data-stu-id="37c0f-789">Driver's Licences#</span></span> 
- <span data-ttu-id="37c0f-790">Разрешение de Кондуире #</span><span class="sxs-lookup"><span data-stu-id="37c0f-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="37c0f-791">кодов</span><span class="sxs-lookup"><span data-stu-id="37c0f-791">id#</span></span> 
- <span data-ttu-id="37c0f-792">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="37c0f-792">ids#</span></span> 
- <span data-ttu-id="37c0f-793">idcard card#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-793">idcard card#</span></span> 
- <span data-ttu-id="37c0f-794">idcard cards#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-794">idcard cards#</span></span> 
- <span data-ttu-id="37c0f-795">idcard#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-795">idcard#</span></span> 
- <span data-ttu-id="37c0f-796">identification card#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-796">identification card#</span></span> 
- <span data-ttu-id="37c0f-797">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-797">identification cards#</span></span> 
- <span data-ttu-id="37c0f-798">identification #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="37c0f-799">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="37c0f-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-800">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-800">Format</span></span>

<span data-ttu-id="37c0f-801">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-802">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-802">Pattern</span></span>

<span data-ttu-id="37c0f-803">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-804">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-804">Checksum</span></span>

<span data-ttu-id="37c0f-805">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-806">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-806">Definition</span></span>

<span data-ttu-id="37c0f-807">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-808">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-809">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-810">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="37c0f-811">Кэйворд_канада_хеалс_сервице_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="37c0f-812">personal health number</span><span class="sxs-lookup"><span data-stu-id="37c0f-812">personal health number</span></span>
- <span data-ttu-id="37c0f-813">
patient information</span><span class="sxs-lookup"><span data-stu-id="37c0f-813">patient information</span></span>
- <span data-ttu-id="37c0f-814">службы работоспособности</span><span class="sxs-lookup"><span data-stu-id="37c0f-814">health services</span></span>
- <span data-ttu-id="37c0f-815">
speciality services</span><span class="sxs-lookup"><span data-stu-id="37c0f-815">speciality services</span></span>
- <span data-ttu-id="37c0f-816">
automobile accident</span><span class="sxs-lookup"><span data-stu-id="37c0f-816">automobile accident</span></span>
- <span data-ttu-id="37c0f-817">
patient hospital</span><span class="sxs-lookup"><span data-stu-id="37c0f-817">patient hospital</span></span>
- <span data-ttu-id="37c0f-818">
psychiatrist</span><span class="sxs-lookup"><span data-stu-id="37c0f-818">psychiatrist</span></span>
- <span data-ttu-id="37c0f-819">
workers compensation</span><span class="sxs-lookup"><span data-stu-id="37c0f-819">workers compensation</span></span>
- <span data-ttu-id="37c0f-820">
disability</span><span class="sxs-lookup"><span data-stu-id="37c0f-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="37c0f-821">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="37c0f-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-822">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-822">Format</span></span>

<span data-ttu-id="37c0f-823">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-824">Pattern</span></span>

<span data-ttu-id="37c0f-825">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-826">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-826">Checksum</span></span>

<span data-ttu-id="37c0f-827">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-828">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-828">Definition</span></span>

<span data-ttu-id="37c0f-829">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-830">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-831">Найдено ключевое слово из Кэйворд_канада_пасспорт_нумбер или Кэйворд_пасспорт.</span><span class="sxs-lookup"><span data-stu-id="37c0f-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-832">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="37c0f-833">Кэйворд_канада_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="37c0f-834">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="37c0f-834">canadian citizenship</span></span>
- <span data-ttu-id="37c0f-835">
canadian passport</span><span class="sxs-lookup"><span data-stu-id="37c0f-835">canadian passport</span></span>
- <span data-ttu-id="37c0f-836">
passport application</span><span class="sxs-lookup"><span data-stu-id="37c0f-836">passport application</span></span>
- <span data-ttu-id="37c0f-837">
passport photos</span><span class="sxs-lookup"><span data-stu-id="37c0f-837">passport photos</span></span>
- <span data-ttu-id="37c0f-838">
certified translator</span><span class="sxs-lookup"><span data-stu-id="37c0f-838">certified translator</span></span>
- <span data-ttu-id="37c0f-839">
canadian citizens</span><span class="sxs-lookup"><span data-stu-id="37c0f-839">canadian citizens</span></span>
- <span data-ttu-id="37c0f-840">
processing times</span><span class="sxs-lookup"><span data-stu-id="37c0f-840">processing times</span></span>
- <span data-ttu-id="37c0f-841">

renewal application</span><span class="sxs-lookup"><span data-stu-id="37c0f-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="37c0f-842">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-842">Keyword_passport</span></span>

- <span data-ttu-id="37c0f-843">Passport Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-843">Passport Number</span></span>
- <span data-ttu-id="37c0f-844">
Passport No</span><span class="sxs-lookup"><span data-stu-id="37c0f-844">Passport No</span></span>
- <span data-ttu-id="37c0f-845">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-845">Passport #</span></span>
- <span data-ttu-id="37c0f-846">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-846">Passport#</span></span>
- <span data-ttu-id="37c0f-847">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="37c0f-847">PassportID</span></span>
- <span data-ttu-id="37c0f-848">Passportno
</span><span class="sxs-lookup"><span data-stu-id="37c0f-848">Passportno</span></span>
- <span data-ttu-id="37c0f-849">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-849">passportnumber</span></span>
- <span data-ttu-id="37c0f-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="37c0f-850">パスポート</span></span>
- <span data-ttu-id="37c0f-851">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-851">パスポート番号</span></span>
- <span data-ttu-id="37c0f-852">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-852">パスポートのNum</span></span>
- <span data-ttu-id="37c0f-853">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-853">パスポート＃</span></span>
- <span data-ttu-id="37c0f-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="37c0f-854">Numéro de passeport</span></span>
- <span data-ttu-id="37c0f-855">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="37c0f-855">Passeport n °</span></span>
- <span data-ttu-id="37c0f-856">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="37c0f-856">Passeport Non</span></span>
- <span data-ttu-id="37c0f-857">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-857">Passeport #</span></span>
- <span data-ttu-id="37c0f-858">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-858">Passeport#</span></span>
- <span data-ttu-id="37c0f-859">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="37c0f-859">PasseportNon</span></span>
- <span data-ttu-id="37c0f-860">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="37c0f-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="37c0f-861">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-862">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-862">Format</span></span>

<span data-ttu-id="37c0f-863">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-864">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-864">Pattern</span></span>

<span data-ttu-id="37c0f-865">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-866">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-866">Checksum</span></span>

<span data-ttu-id="37c0f-867">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-868">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-868">Definition</span></span>

<span data-ttu-id="37c0f-p104">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_канада_фин находит содержимое, которое соответствует шаблону. Найдены по крайней мере два ключевых слова от Кэйворд_канада_фин или Кэйворд_канада_провинцес.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p104">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern. At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-871">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="37c0f-872">Кэйворд_канада_фин</span><span class="sxs-lookup"><span data-stu-id="37c0f-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="37c0f-873">social insurance number</span><span class="sxs-lookup"><span data-stu-id="37c0f-873">social insurance number</span></span>
- <span data-ttu-id="37c0f-874">
health information act</span><span class="sxs-lookup"><span data-stu-id="37c0f-874">health information act</span></span>
- <span data-ttu-id="37c0f-875">
income tax information</span><span class="sxs-lookup"><span data-stu-id="37c0f-875">income tax information</span></span>
- <span data-ttu-id="37c0f-876">
manitoba health</span><span class="sxs-lookup"><span data-stu-id="37c0f-876">manitoba health</span></span>
- <span data-ttu-id="37c0f-877">
health registration</span><span class="sxs-lookup"><span data-stu-id="37c0f-877">health registration</span></span>
- <span data-ttu-id="37c0f-878">
prescription purchases</span><span class="sxs-lookup"><span data-stu-id="37c0f-878">prescription purchases</span></span>
- <span data-ttu-id="37c0f-879">
benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="37c0f-879">benefit eligibility</span></span>
- <span data-ttu-id="37c0f-880">
personal health</span><span class="sxs-lookup"><span data-stu-id="37c0f-880">personal health</span></span>
- <span data-ttu-id="37c0f-881">
power of attorney</span><span class="sxs-lookup"><span data-stu-id="37c0f-881">power of attorney</span></span>
- <span data-ttu-id="37c0f-882">
registration number</span><span class="sxs-lookup"><span data-stu-id="37c0f-882">registration number</span></span>
- <span data-ttu-id="37c0f-883">personal health number</span><span class="sxs-lookup"><span data-stu-id="37c0f-883">personal health number</span></span>
- <span data-ttu-id="37c0f-884">
practitioner referral</span><span class="sxs-lookup"><span data-stu-id="37c0f-884">practitioner referral</span></span>
- <span data-ttu-id="37c0f-885">
wellness professional</span><span class="sxs-lookup"><span data-stu-id="37c0f-885">wellness professional</span></span>
- <span data-ttu-id="37c0f-886">
patient referral</span><span class="sxs-lookup"><span data-stu-id="37c0f-886">patient referral</span></span>
- <span data-ttu-id="37c0f-887">

health and wellness</span><span class="sxs-lookup"><span data-stu-id="37c0f-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="37c0f-888">Кэйворд_канада_провинцес</span><span class="sxs-lookup"><span data-stu-id="37c0f-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="37c0f-889">Nunavut</span><span class="sxs-lookup"><span data-stu-id="37c0f-889">Nunavut</span></span>
- <span data-ttu-id="37c0f-890">
Quebec</span><span class="sxs-lookup"><span data-stu-id="37c0f-890">Quebec</span></span>
- <span data-ttu-id="37c0f-891">
Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="37c0f-891">Northwest Territories</span></span>
- <span data-ttu-id="37c0f-892">
Ontario</span><span class="sxs-lookup"><span data-stu-id="37c0f-892">Ontario</span></span>
- <span data-ttu-id="37c0f-893">
British Columbia</span><span class="sxs-lookup"><span data-stu-id="37c0f-893">British Columbia</span></span>
- <span data-ttu-id="37c0f-894">
Alberta</span><span class="sxs-lookup"><span data-stu-id="37c0f-894">Alberta</span></span>
- <span data-ttu-id="37c0f-895">
Saskatchewan</span><span class="sxs-lookup"><span data-stu-id="37c0f-895">Saskatchewan</span></span>
- <span data-ttu-id="37c0f-896">
Manitoba</span><span class="sxs-lookup"><span data-stu-id="37c0f-896">Manitoba</span></span>
- <span data-ttu-id="37c0f-897">
Yukon</span><span class="sxs-lookup"><span data-stu-id="37c0f-897">Yukon</span></span>
- <span data-ttu-id="37c0f-898">
Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="37c0f-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="37c0f-899">
New Brunswick</span><span class="sxs-lookup"><span data-stu-id="37c0f-899">New Brunswick</span></span>
- <span data-ttu-id="37c0f-900">
Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="37c0f-900">Nova Scotia</span></span>
- <span data-ttu-id="37c0f-901">
Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="37c0f-901">Prince Edward Island</span></span>
- <span data-ttu-id="37c0f-902">Канада</span><span class="sxs-lookup"><span data-stu-id="37c0f-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="37c0f-903">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="37c0f-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-904">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-904">Format</span></span>

<span data-ttu-id="37c0f-905">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="37c0f-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-906">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-906">Pattern</span></span>

<span data-ttu-id="37c0f-907">С форматированием</span><span class="sxs-lookup"><span data-stu-id="37c0f-907">Formatted:</span></span>
- <span data-ttu-id="37c0f-908">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-908">Three digits</span></span> 
- <span data-ttu-id="37c0f-909">дефис или пробел; </span><span class="sxs-lookup"><span data-stu-id="37c0f-909">A hyphen or space</span></span> 
- <span data-ttu-id="37c0f-910">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-910">Three digits</span></span> 
- <span data-ttu-id="37c0f-911">дефис или пробел; </span><span class="sxs-lookup"><span data-stu-id="37c0f-911">A hyphen or space</span></span> 
- <span data-ttu-id="37c0f-912">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-912">Three digits</span></span>

<span data-ttu-id="37c0f-913">Неформатированные: девять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-914">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-914">Checksum</span></span>

<span data-ttu-id="37c0f-915">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-916">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-916">Definition</span></span>

<span data-ttu-id="37c0f-917">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-918">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-919">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="37c0f-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="37c0f-920">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="37c0f-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="37c0f-921">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="37c0f-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="37c0f-922">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="37c0f-923">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-923">The checksum passes.</span></span>

<span data-ttu-id="37c0f-924">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-925">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-926">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="37c0f-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="37c0f-927">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-927">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-928">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="37c0f-929">Кэйворд_син</span><span class="sxs-lookup"><span data-stu-id="37c0f-929">Keyword_sin</span></span>

- <span data-ttu-id="37c0f-930">Синус</span><span class="sxs-lookup"><span data-stu-id="37c0f-930">sin</span></span> 
- <span data-ttu-id="37c0f-931">social insurance
</span><span class="sxs-lookup"><span data-stu-id="37c0f-931">social insurance</span></span> 
- <span data-ttu-id="37c0f-932">numero d'assurance sociale
</span><span class="sxs-lookup"><span data-stu-id="37c0f-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="37c0f-933">sins
</span><span class="sxs-lookup"><span data-stu-id="37c0f-933">sins</span></span> 
- <span data-ttu-id="37c0f-934">SSN</span><span class="sxs-lookup"><span data-stu-id="37c0f-934">ssn</span></span> 
- <span data-ttu-id="37c0f-935">ssNS</span><span class="sxs-lookup"><span data-stu-id="37c0f-935">ssns</span></span> 
- <span data-ttu-id="37c0f-936">социальное обеспечение безопасности</span><span class="sxs-lookup"><span data-stu-id="37c0f-936">social security</span></span> 
- <span data-ttu-id="37c0f-937">numero d'assurance social
</span><span class="sxs-lookup"><span data-stu-id="37c0f-937">numero d'assurance social</span></span> 
- <span data-ttu-id="37c0f-938">Национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="37c0f-938">national identification number</span></span> 
- <span data-ttu-id="37c0f-939">
national id</span><span class="sxs-lookup"><span data-stu-id="37c0f-939">national id</span></span> 
- <span data-ttu-id="37c0f-940">sin#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-940">sin#</span></span> 
- <span data-ttu-id="37c0f-941">soc ins
</span><span class="sxs-lookup"><span data-stu-id="37c0f-941">soc ins</span></span> 
- <span data-ttu-id="37c0f-942">social ins
</span><span class="sxs-lookup"><span data-stu-id="37c0f-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="37c0f-943">Кэйворд_син_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="37c0f-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="37c0f-944">driver's license</span><span class="sxs-lookup"><span data-stu-id="37c0f-944">driver's license</span></span> 
- <span data-ttu-id="37c0f-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="37c0f-945">drivers license</span></span> 
- <span data-ttu-id="37c0f-946">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-946">driver's licence</span></span> 
- <span data-ttu-id="37c0f-947">drivers licence</span><span class="sxs-lookup"><span data-stu-id="37c0f-947">drivers licence</span></span> 
- <span data-ttu-id="37c0f-948">DOB
</span><span class="sxs-lookup"><span data-stu-id="37c0f-948">DOB</span></span> 
- <span data-ttu-id="37c0f-949">Birthdate</span><span class="sxs-lookup"><span data-stu-id="37c0f-949">Birthdate</span></span> 
- <span data-ttu-id="37c0f-950">День рождения </span><span class="sxs-lookup"><span data-stu-id="37c0f-950">Birthday</span></span> 
- <span data-ttu-id="37c0f-951">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="37c0f-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="37c0f-952">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="37c0f-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-953">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-953">Format</span></span>

<span data-ttu-id="37c0f-954">7-8 цифр и разделители — контрольная цифра или буква</span><span class="sxs-lookup"><span data-stu-id="37c0f-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-955">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-955">Pattern</span></span>

<span data-ttu-id="37c0f-956">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="37c0f-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="37c0f-957">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-957">1-2 digits</span></span> 
- <span data-ttu-id="37c0f-958">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-958">A period</span></span> 
- <span data-ttu-id="37c0f-959">три цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-959">Three digits</span></span> 
- <span data-ttu-id="37c0f-960">точка;</span><span class="sxs-lookup"><span data-stu-id="37c0f-960">A period</span></span> 
- <span data-ttu-id="37c0f-961">три цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-961">Three digits</span></span> 
- <span data-ttu-id="37c0f-962">Тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-962">A dash</span></span> 
- <span data-ttu-id="37c0f-963">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-964">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-964">Checksum</span></span>

<span data-ttu-id="37c0f-965">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-966">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-966">Definition</span></span>

<span data-ttu-id="37c0f-967">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-968">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-969">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="37c0f-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="37c0f-970">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-970">The checksum passes.</span></span>

<span data-ttu-id="37c0f-971">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-972">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-973">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-973">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-974">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="37c0f-975">Кэйворд_чиле_ид_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="37c0f-976">National Identification Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-976">National Identification Number</span></span> 
- <span data-ttu-id="37c0f-977">Identity card</span><span class="sxs-lookup"><span data-stu-id="37c0f-977">Identity card</span></span> 
- <span data-ttu-id="37c0f-978">ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-978">ID</span></span> 
- <span data-ttu-id="37c0f-979">Identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-979">Identification</span></span> 
- <span data-ttu-id="37c0f-980">Rol Único Nacional
</span><span class="sxs-lookup"><span data-stu-id="37c0f-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="37c0f-981">ВЫПОЛНЯЕМ</span><span class="sxs-lookup"><span data-stu-id="37c0f-981">RUN</span></span> 
- <span data-ttu-id="37c0f-982">Rol Único Tributario
</span><span class="sxs-lookup"><span data-stu-id="37c0f-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="37c0f-983">RUT
</span><span class="sxs-lookup"><span data-stu-id="37c0f-983">RUT</span></span> 
- <span data-ttu-id="37c0f-984">Cédula de Identidad
</span><span class="sxs-lookup"><span data-stu-id="37c0f-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="37c0f-985">Número De Identificación Nacional
</span><span class="sxs-lookup"><span data-stu-id="37c0f-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="37c0f-986">Tarjeta de identificación
</span><span class="sxs-lookup"><span data-stu-id="37c0f-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="37c0f-987">Identificación
</span><span class="sxs-lookup"><span data-stu-id="37c0f-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="37c0f-988">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="37c0f-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-989">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-989">Format</span></span>

<span data-ttu-id="37c0f-990">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-991">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-991">Pattern</span></span>

<span data-ttu-id="37c0f-992">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-992">18 digits:</span></span>
- <span data-ttu-id="37c0f-993">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="37c0f-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="37c0f-994">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="37c0f-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-995">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="37c0f-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="37c0f-996">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-997">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-997">Checksum</span></span>

<span data-ttu-id="37c0f-998">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-999">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-999">Definition</span></span>

<span data-ttu-id="37c0f-1000">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1001">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1002">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="37c0f-1003">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1003">The checksum passes.</span></span>

<span data-ttu-id="37c0f-1004">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1005">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1006">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1006">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1007">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="37c0f-1008">Кэйворд_чина_ресидент_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="37c0f-1009">Resident Identity Card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="37c0f-1010">NO7</span><span class="sxs-lookup"><span data-stu-id="37c0f-1010">PRC</span></span> 
- <span data-ttu-id="37c0f-1011">National Identification Card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1011">National Identification Card</span></span> 
- <span data-ttu-id="37c0f-1012">身份证 </span><span class="sxs-lookup"><span data-stu-id="37c0f-1012">身份证</span></span> 
- <span data-ttu-id="37c0f-1013">居民 身份证 </span><span class="sxs-lookup"><span data-stu-id="37c0f-1013">居民 身份证</span></span> 
- <span data-ttu-id="37c0f-1014">居民身份证
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1014">居民身份证</span></span> 
- <span data-ttu-id="37c0f-1015">鉴定

</span><span class="sxs-lookup"><span data-stu-id="37c0f-1015">鉴定</span></span> 
- <span data-ttu-id="37c0f-1016">身分證 </span><span class="sxs-lookup"><span data-stu-id="37c0f-1016">身分證</span></span> 
- <span data-ttu-id="37c0f-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="37c0f-1017">居民 身份證</span></span>
- <span data-ttu-id="37c0f-1018">鑑定 </span><span class="sxs-lookup"><span data-stu-id="37c0f-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="37c0f-1019">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="37c0f-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1020">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1020">Format</span></span>

<span data-ttu-id="37c0f-1021">16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1022">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1022">Pattern</span></span>

<span data-ttu-id="37c0f-1023">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1024">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1024">Checksum</span></span>

<span data-ttu-id="37c0f-1025">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="37c0f-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1026">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1026">Definition</span></span>

<span data-ttu-id="37c0f-1027">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1028">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1029">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1029">One of the following is true:</span></span>
    - <span data-ttu-id="37c0f-1030">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="37c0f-1031">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="37c0f-1032">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="37c0f-1033">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1033">The checksum passes.</span></span>

<span data-ttu-id="37c0f-1034">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1035">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1036">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1036">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1037">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="37c0f-1038">Кэйворд_кк_верификатион</span><span class="sxs-lookup"><span data-stu-id="37c0f-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="37c0f-1039">card verification</span><span class="sxs-lookup"><span data-stu-id="37c0f-1039">card verification</span></span>
- <span data-ttu-id="37c0f-1040">card identification number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1040">card identification number</span></span>
- <span data-ttu-id="37c0f-1041">cvn
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1041">cvn</span></span>
- <span data-ttu-id="37c0f-1042">cid
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1042">cid</span></span>
- <span data-ttu-id="37c0f-1043">CVC2</span><span class="sxs-lookup"><span data-stu-id="37c0f-1043">cvc2</span></span>
- <span data-ttu-id="37c0f-1044">CVV2</span><span class="sxs-lookup"><span data-stu-id="37c0f-1044">cvv2</span></span>
- <span data-ttu-id="37c0f-1045">pin block
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1045">pin block</span></span>
- <span data-ttu-id="37c0f-1046">security code
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1046">security code</span></span>
- <span data-ttu-id="37c0f-1047">security number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1047">security number</span></span>
- <span data-ttu-id="37c0f-1048">security no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1048">security no</span></span>
- <span data-ttu-id="37c0f-1049">issue number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1049">issue number</span></span>
- <span data-ttu-id="37c0f-1050">issue no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1050">issue no</span></span>
- <span data-ttu-id="37c0f-1051">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1051">cryptogramme</span></span>
- <span data-ttu-id="37c0f-1052">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1052">numéro de sécurité</span></span>
- <span data-ttu-id="37c0f-1053">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1053">numero de securite</span></span>
- <span data-ttu-id="37c0f-1054">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="37c0f-1055">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="37c0f-1056">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1056">prüfziffer</span></span>
- <span data-ttu-id="37c0f-1057">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1057">prufziffer</span></span>
- <span data-ttu-id="37c0f-1058">сичерхеитс коде</span><span class="sxs-lookup"><span data-stu-id="37c0f-1058">sicherheits Kode</span></span>
- <span data-ttu-id="37c0f-1059">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1059">sicherheitscode</span></span>
- <span data-ttu-id="37c0f-1060">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="37c0f-1061">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1061">verfalldatum</span></span>
- <span data-ttu-id="37c0f-1062">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1062">codice di verifica</span></span>
- <span data-ttu-id="37c0f-p105">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p105">cod. sicurezza</span></span>
- <span data-ttu-id="37c0f-1065">сикурезза наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1065">cod sicurezza</span></span>
- <span data-ttu-id="37c0f-1066">
n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="37c0f-1066">n autorizzazione</span></span>
- <span data-ttu-id="37c0f-1067">código
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1067">código</span></span>
- <span data-ttu-id="37c0f-1068">codigo
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1068">codigo</span></span>
- <span data-ttu-id="37c0f-p106">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p106">cod. seg</span></span>
- <span data-ttu-id="37c0f-1071">СЕГ наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1071">cod seg</span></span>
- <span data-ttu-id="37c0f-1072">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1072">código de segurança</span></span>
- <span data-ttu-id="37c0f-1073">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1073">codigo de seguranca</span></span>
- <span data-ttu-id="37c0f-1074">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1074">codigo de segurança</span></span>
- <span data-ttu-id="37c0f-1075">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1075">código de seguranca</span></span>
- <span data-ttu-id="37c0f-p107">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p107">cód. segurança</span></span>
- <span data-ttu-id="37c0f-p108">наложен. сегуранка наложенный платеж. сегуранçа</span><span class="sxs-lookup"><span data-stu-id="37c0f-p108">cod. seguranca cod. segurança</span></span>
- <span data-ttu-id="37c0f-p109">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p109">cód. seguranca</span></span>
- <span data-ttu-id="37c0f-1083">кóд сегуранçа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1083">cód segurança</span></span>
- <span data-ttu-id="37c0f-1084">наложенный на наложенный сегуранка сегуранçа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="37c0f-1085">кóд сегуранка</span><span class="sxs-lookup"><span data-stu-id="37c0f-1085">cód seguranca</span></span>
- <span data-ttu-id="37c0f-1086">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1086">número de verificação</span></span>
- <span data-ttu-id="37c0f-1087">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1087">numero de verificacao</span></span>
- <span data-ttu-id="37c0f-1088">ablauf
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1088">ablauf</span></span>
- <span data-ttu-id="37c0f-1089">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1089">gültig bis</span></span>
- <span data-ttu-id="37c0f-1090">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="37c0f-1091">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1091">gultig bis</span></span>
- <span data-ttu-id="37c0f-1092">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="37c0f-1093">scadenza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1093">scadenza</span></span>
- <span data-ttu-id="37c0f-1094">data scad
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1094">data scad</span></span>
- <span data-ttu-id="37c0f-1095">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1095">fecha de expiracion</span></span>
- <span data-ttu-id="37c0f-1096">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1096">fecha de venc</span></span>
- <span data-ttu-id="37c0f-1097">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1097">vencimiento</span></span>
- <span data-ttu-id="37c0f-1098">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1098">válido hasta</span></span>
- <span data-ttu-id="37c0f-1099">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1099">valido hasta</span></span>
- <span data-ttu-id="37c0f-1100">vto
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1100">vto</span></span>
- <span data-ttu-id="37c0f-1101">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1101">data de expiração</span></span>
- <span data-ttu-id="37c0f-1102">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1102">data de expiracao</span></span>
- <span data-ttu-id="37c0f-1103">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1103">data em que expira</span></span>
- <span data-ttu-id="37c0f-1104">validade
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1104">validade</span></span>
- <span data-ttu-id="37c0f-1105">valor
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1105">valor</span></span>
- <span data-ttu-id="37c0f-1106">vencimento
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1106">vencimento</span></span>
- <span data-ttu-id="37c0f-1107">Венк</span><span class="sxs-lookup"><span data-stu-id="37c0f-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="37c0f-1108">Кэйворд_кк_наме</span><span class="sxs-lookup"><span data-stu-id="37c0f-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="37c0f-1109">amex</span><span class="sxs-lookup"><span data-stu-id="37c0f-1109">amex</span></span>
- <span data-ttu-id="37c0f-1110">
american express</span><span class="sxs-lookup"><span data-stu-id="37c0f-1110">american express</span></span>
- <span data-ttu-id="37c0f-1111">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1111">americanexpress</span></span>
- <span data-ttu-id="37c0f-1112">Visa</span><span class="sxs-lookup"><span data-stu-id="37c0f-1112">Visa</span></span>
- <span data-ttu-id="37c0f-1113">mastercard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1113">mastercard</span></span>
- <span data-ttu-id="37c0f-1114">master card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1114">master card</span></span>
- <span data-ttu-id="37c0f-1115">
mc
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1115">mc</span></span> 
- <span data-ttu-id="37c0f-1116">mastercards</span><span class="sxs-lookup"><span data-stu-id="37c0f-1116">mastercards</span></span>
- <span data-ttu-id="37c0f-1117">
master cards</span><span class="sxs-lookup"><span data-stu-id="37c0f-1117">master cards</span></span>
- <span data-ttu-id="37c0f-1118">Клуб Динер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1118">diner's Club</span></span>
- <span data-ttu-id="37c0f-1119">diners club
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1119">diners club</span></span>
- <span data-ttu-id="37c0f-1120">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1120">dinersclub</span></span>
- <span data-ttu-id="37c0f-1121">discover card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1121">discover card</span></span>
- <span data-ttu-id="37c0f-1122">discovercard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1122">discovercard</span></span>
- <span data-ttu-id="37c0f-1123">discover cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1123">discover cards</span></span>
- <span data-ttu-id="37c0f-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="37c0f-1124">JCB</span></span>
- <span data-ttu-id="37c0f-1125">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1125">japanese card bureau</span></span>
- <span data-ttu-id="37c0f-1126">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1126">carte blanche</span></span>
- <span data-ttu-id="37c0f-1127">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1127">carteblanche</span></span>
- <span data-ttu-id="37c0f-1128">credit card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1128">credit card</span></span>
- <span data-ttu-id="37c0f-1129">Центральной</span><span class="sxs-lookup"><span data-stu-id="37c0f-1129">cc#</span></span>
- <span data-ttu-id="37c0f-1130">CC #:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1130">cc#:</span></span>
- <span data-ttu-id="37c0f-1131">
expiration date</span><span class="sxs-lookup"><span data-stu-id="37c0f-1131">expiration date</span></span>
- <span data-ttu-id="37c0f-1132">exp date
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1132">exp date</span></span>
- <span data-ttu-id="37c0f-1133">
expiry date</span><span class="sxs-lookup"><span data-stu-id="37c0f-1133">expiry date</span></span>
- <span data-ttu-id="37c0f-1134">
date d’expiration</span><span class="sxs-lookup"><span data-stu-id="37c0f-1134">date d’expiration</span></span>
- <span data-ttu-id="37c0f-1135">
date d'exp</span><span class="sxs-lookup"><span data-stu-id="37c0f-1135">date d'exp</span></span>
- <span data-ttu-id="37c0f-1136">
date expiration</span><span class="sxs-lookup"><span data-stu-id="37c0f-1136">date expiration</span></span>
- <span data-ttu-id="37c0f-1137">bank card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1137">bank card</span></span>
- <span data-ttu-id="37c0f-1138">
bankcard</span><span class="sxs-lookup"><span data-stu-id="37c0f-1138">bankcard</span></span>
- <span data-ttu-id="37c0f-1139">card number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1139">card number</span></span>
- <span data-ttu-id="37c0f-1140">card num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1140">card num</span></span>
- <span data-ttu-id="37c0f-1141">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1141">cardnumber</span></span>
- <span data-ttu-id="37c0f-1142">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1142">cardnumbers</span></span>
- <span data-ttu-id="37c0f-1143">card numbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1143">card numbers</span></span>
- <span data-ttu-id="37c0f-1144">creditcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1144">creditcard</span></span>
- <span data-ttu-id="37c0f-1145">credit cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1145">credit cards</span></span>
- <span data-ttu-id="37c0f-1146">creditcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1146">creditcards</span></span>
- <span data-ttu-id="37c0f-1147">ccn
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1147">ccn</span></span>
- <span data-ttu-id="37c0f-1148">card holder
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1148">card holder</span></span>
- <span data-ttu-id="37c0f-1149">cardholder
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1149">cardholder</span></span>
- <span data-ttu-id="37c0f-1150">card holders
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1150">card holders</span></span>
- <span data-ttu-id="37c0f-1151">cardholders
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1151">cardholders</span></span>
- <span data-ttu-id="37c0f-1152">check card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1152">check card</span></span>
- <span data-ttu-id="37c0f-1153">checkcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1153">checkcard</span></span>
- <span data-ttu-id="37c0f-1154">check cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1154">check cards</span></span>
- <span data-ttu-id="37c0f-1155">checkcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1155">checkcards</span></span>
- <span data-ttu-id="37c0f-1156">debit card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1156">debit card</span></span>
- <span data-ttu-id="37c0f-1157">debitcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1157">debitcard</span></span>
- <span data-ttu-id="37c0f-1158">debit cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1158">debit cards</span></span>
- <span data-ttu-id="37c0f-1159">debitcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1159">debitcards</span></span>
- <span data-ttu-id="37c0f-1160">atm card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1160">atm card</span></span>
- <span data-ttu-id="37c0f-1161">atmcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1161">atmcard</span></span>
- <span data-ttu-id="37c0f-1162">atm cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1162">atm cards</span></span>
- <span data-ttu-id="37c0f-1163">atmcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1163">atmcards</span></span>
- <span data-ttu-id="37c0f-1164">
enroute</span><span class="sxs-lookup"><span data-stu-id="37c0f-1164">enroute</span></span>
- <span data-ttu-id="37c0f-1165">
en route</span><span class="sxs-lookup"><span data-stu-id="37c0f-1165">en route</span></span>
- <span data-ttu-id="37c0f-1166">card type
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1166">card type</span></span>
- <span data-ttu-id="37c0f-1167">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1167">carte bancaire</span></span>
- <span data-ttu-id="37c0f-1168">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1168">carte de crédit</span></span>
- <span data-ttu-id="37c0f-1169">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1169">carte de credit</span></span>
- <span data-ttu-id="37c0f-1170">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1170">numéro de carte</span></span>
- <span data-ttu-id="37c0f-1171">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1171">numero de carte</span></span>
- <span data-ttu-id="37c0f-1172">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1172">nº de la carte</span></span>
- <span data-ttu-id="37c0f-1173">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1173">nº de carte</span></span>
- <span data-ttu-id="37c0f-1174">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1174">kreditkarte</span></span>
- <span data-ttu-id="37c0f-1175">karte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1175">karte</span></span>
- <span data-ttu-id="37c0f-1176">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1176">karteninhaber</span></span>
- <span data-ttu-id="37c0f-1177">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="37c0f-1177">karteninhabers</span></span>
- <span data-ttu-id="37c0f-1178">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="37c0f-1179">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="37c0f-1180">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1180">kreditkartentyp</span></span>
- <span data-ttu-id="37c0f-1181">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1181">eigentümername</span></span>
- <span data-ttu-id="37c0f-1182">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1182">kartennr</span></span> 
- <span data-ttu-id="37c0f-1183">kartennummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1183">kartennummer</span></span>
- <span data-ttu-id="37c0f-1184">
kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1184">kreditkartennummer</span></span>
- <span data-ttu-id="37c0f-1185">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="37c0f-1186">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1186">carta di credito</span></span>
- <span data-ttu-id="37c0f-1187">carta credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1187">carta credito</span></span>
- <span data-ttu-id="37c0f-1188">Корзина "</span><span class="sxs-lookup"><span data-stu-id="37c0f-1188">carta</span></span>
- <span data-ttu-id="37c0f-1189">n корзина</span><span class="sxs-lookup"><span data-stu-id="37c0f-1189">n carta</span></span>
- <span data-ttu-id="37c0f-p110">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p110">nr. carta</span></span>
- <span data-ttu-id="37c0f-1192">нрная корзина</span><span class="sxs-lookup"><span data-stu-id="37c0f-1192">nr carta</span></span>
- <span data-ttu-id="37c0f-1193">numero carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1193">numero carta</span></span>
- <span data-ttu-id="37c0f-1194">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1194">numero della carta</span></span>
- <span data-ttu-id="37c0f-1195">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1195">numero di carta</span></span>
- <span data-ttu-id="37c0f-1196">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1196">tarjeta credito</span></span>
- <span data-ttu-id="37c0f-1197">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1197">tarjeta de credito</span></span>
- <span data-ttu-id="37c0f-1198">
tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="37c0f-1198">tarjeta crédito</span></span>
- <span data-ttu-id="37c0f-1199">
tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="37c0f-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="37c0f-1200">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1200">tarjeta de atm</span></span>
- <span data-ttu-id="37c0f-1201">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1201">tarjeta atm</span></span>
- <span data-ttu-id="37c0f-1202">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1202">tarjeta debito</span></span>
- <span data-ttu-id="37c0f-1203">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1203">tarjeta de debito</span></span>
- <span data-ttu-id="37c0f-1204">
tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="37c0f-1204">tarjeta débito</span></span>
- <span data-ttu-id="37c0f-1205">
tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="37c0f-1205">tarjeta de débito</span></span>
- <span data-ttu-id="37c0f-1206">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1206">nº de tarjeta</span></span>
- <span data-ttu-id="37c0f-p111">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p111">no. de tarjeta</span></span>
- <span data-ttu-id="37c0f-1209">нет де таржета</span><span class="sxs-lookup"><span data-stu-id="37c0f-1209">no de tarjeta</span></span>
- <span data-ttu-id="37c0f-1210">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1210">numero de tarjeta</span></span>
- <span data-ttu-id="37c0f-1211">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1211">número de tarjeta</span></span>
- <span data-ttu-id="37c0f-1212">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1212">tarjeta no</span></span>
- <span data-ttu-id="37c0f-1213">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1213">tarjetahabiente</span></span>
- <span data-ttu-id="37c0f-1214">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1214">cartão de crédito</span></span>
- <span data-ttu-id="37c0f-1215">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1215">cartão de credito</span></span>
- <span data-ttu-id="37c0f-1216">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1216">cartao de crédito</span></span>
- <span data-ttu-id="37c0f-1217">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1217">cartao de credito</span></span>
- <span data-ttu-id="37c0f-1218">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1218">cartão de débito</span></span>
- <span data-ttu-id="37c0f-1219">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1219">cartao de débito</span></span>
- <span data-ttu-id="37c0f-1220">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1220">cartão de debito</span></span>
- <span data-ttu-id="37c0f-1221">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1221">cartao de debito</span></span>
- <span data-ttu-id="37c0f-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="37c0f-1222">débito automático</span></span>
- <span data-ttu-id="37c0f-1223">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1223">debito automatico</span></span>
- <span data-ttu-id="37c0f-1224">
número do cartão</span><span class="sxs-lookup"><span data-stu-id="37c0f-1224">número do cartão</span></span>
- <span data-ttu-id="37c0f-1225">
numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1225">numero do cartão</span></span> 
- <span data-ttu-id="37c0f-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="37c0f-1226">número do cartao</span></span>
- <span data-ttu-id="37c0f-1227">
numero do cartao</span><span class="sxs-lookup"><span data-stu-id="37c0f-1227">numero do cartao</span></span>
- <span data-ttu-id="37c0f-1228">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1228">número de cartão</span></span>
- <span data-ttu-id="37c0f-1229">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1229">numero de cartão</span></span>
- <span data-ttu-id="37c0f-1230">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1230">número de cartao</span></span>
- <span data-ttu-id="37c0f-1231">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1231">numero de cartao</span></span>
- <span data-ttu-id="37c0f-1232">n º Do картãо</span><span class="sxs-lookup"><span data-stu-id="37c0f-1232">nº do cartão</span></span>
- <span data-ttu-id="37c0f-1233">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1233">nº do cartao</span></span>
- <span data-ttu-id="37c0f-p112">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p112">nº. do cartão</span></span>
- <span data-ttu-id="37c0f-1236">не выполнять картãо</span><span class="sxs-lookup"><span data-stu-id="37c0f-1236">no do cartão</span></span>
- <span data-ttu-id="37c0f-1237">не выполнять картао</span><span class="sxs-lookup"><span data-stu-id="37c0f-1237">no do cartao</span></span>
- <span data-ttu-id="37c0f-p113">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p113">no. do cartão</span></span>
- <span data-ttu-id="37c0f-p114">
no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p114">no. do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="37c0f-1242">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="37c0f-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1243">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1243">Format</span></span>

<span data-ttu-id="37c0f-1244">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1245">Pattern</span></span>

<span data-ttu-id="37c0f-1246">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1247">Checksum</span></span>

<span data-ttu-id="37c0f-1248">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1249">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1249">Definition</span></span>

<span data-ttu-id="37c0f-1250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1251">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1252">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="37c0f-1254">Кэйворд_кроатиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="37c0f-1255">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="37c0f-1255">Croatian identity card</span></span>
- <span data-ttu-id="37c0f-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="37c0f-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="37c0f-1257">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="37c0f-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1258">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1258">Format</span></span>

<span data-ttu-id="37c0f-1259">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="37c0f-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1260">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1260">Pattern</span></span>

<span data-ttu-id="37c0f-1261">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1261">11 digits:</span></span>
- <span data-ttu-id="37c0f-1262">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1262">10 digits</span></span> 
- <span data-ttu-id="37c0f-1263">Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1264">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1264">Checksum</span></span>

<span data-ttu-id="37c0f-1265">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1266">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1266">Definition</span></span>

<span data-ttu-id="37c0f-1267">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1268">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1269">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="37c0f-1270">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1270">The checksum passes.</span></span>

<span data-ttu-id="37c0f-1271">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1272">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1273">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1273">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1274">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="37c0f-1275">Кэйворд_кроатиа_оиб_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="37c0f-1276">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1276">Personal Identification Number</span></span>
- <span data-ttu-id="37c0f-1277">Osobni identifikacijski broj
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="37c0f-1278">OIB
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="37c0f-1279">Номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="37c0f-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1280">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1280">Format</span></span>

<span data-ttu-id="37c0f-1281">Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1282">Pattern</span></span>

<span data-ttu-id="37c0f-1283">Девять цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="37c0f-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="37c0f-1284">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1284">Nine digits</span></span>

<span data-ttu-id="37c0f-1285">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="37c0f-1285">OR</span></span>

- <span data-ttu-id="37c0f-1286">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="37c0f-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="37c0f-1287">косая черта;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1287">A forward slash</span></span>
- <span data-ttu-id="37c0f-1288">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-1288">Three digits</span></span>

<span data-ttu-id="37c0f-1289">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="37c0f-1289">10 digits (new format):</span></span>
- <span data-ttu-id="37c0f-1290">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1290">10 digits</span></span>

<span data-ttu-id="37c0f-1291">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="37c0f-1291">OR</span></span>

- <span data-ttu-id="37c0f-1292">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="37c0f-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="37c0f-1293">косая черта;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1293">A forward slash</span></span> 
- <span data-ttu-id="37c0f-1294">Четыре цифры, где последняя цифра является контрольной цифрой</span><span class="sxs-lookup"><span data-stu-id="37c0f-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1295">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1295">Checksum</span></span>

<span data-ttu-id="37c0f-1296">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1297">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1297">Definition</span></span>

<span data-ttu-id="37c0f-p115">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_кзеч_ид_кард находит содержимое, которое соответствует шаблону; Найдено ключевое слово из Кэйворд_кзеч_ид_кард. Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p115">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern. A keyword from Keyword_czech_id_card is found. The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="37c0f-1301">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1301">Keywords</span></span>

- <span data-ttu-id="37c0f-1302">номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="37c0f-1302">czech personal identity number</span></span>
- <span data-ttu-id="37c0f-1303">Роднé číсло</span><span class="sxs-lookup"><span data-stu-id="37c0f-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="37c0f-1304">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="37c0f-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1305">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1305">Format</span></span>

<span data-ttu-id="37c0f-1306">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1307">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1307">Pattern</span></span>

<span data-ttu-id="37c0f-1308">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1308">10 digits:</span></span>
- <span data-ttu-id="37c0f-1309">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-1310">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1310">A hyphen</span></span> 
- <span data-ttu-id="37c0f-1311">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1312">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1312">Checksum</span></span>

<span data-ttu-id="37c0f-1313">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1314">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1314">Definition</span></span>

<span data-ttu-id="37c0f-p116">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_денмарк_ид находит содержимое, которое соответствует шаблону. Найдено ключевое слово из Кэйворд_денмарк_ид. Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p116">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern. A keyword from Keyword_denmark_id is found. The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1318">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="37c0f-1319">Кэйворд_денмарк_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="37c0f-1320">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1320">Personal Identification Number</span></span>
- <span data-ttu-id="37c0f-1321">CPR</span><span class="sxs-lookup"><span data-stu-id="37c0f-1321">CPR</span></span>
- <span data-ttu-id="37c0f-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="37c0f-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="37c0f-1323">Personnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="37c0f-1324">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1325">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1325">Format</span></span>

<span data-ttu-id="37c0f-1326">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1327">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1327">Pattern</span></span>

<span data-ttu-id="37c0f-1328">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="37c0f-1329">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="37c0f-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="37c0f-1330">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="37c0f-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="37c0f-1331">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="37c0f-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1332">Checksum</span></span>

<span data-ttu-id="37c0f-1333">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1334">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1334">Definition</span></span>

<span data-ttu-id="37c0f-1335">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1336">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1337">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1338">Keywords</span></span>

<span data-ttu-id="37c0f-1339">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="37c0f-1340">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="37c0f-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1341">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1341">Format</span></span>

<span data-ttu-id="37c0f-1342">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1343">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1343">Pattern</span></span>

<span data-ttu-id="37c0f-1344">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1345">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1345">Checksum</span></span>

<span data-ttu-id="37c0f-1346">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1347">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1347">Definition</span></span>

<span data-ttu-id="37c0f-1348">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1349">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1350">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="37c0f-1351">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="37c0f-1352">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="37c0f-1353">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="37c0f-1354">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="37c0f-1355">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="37c0f-1356">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1356">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1357">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="37c0f-1358">Кэйворд_еу_дебит_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="37c0f-1359">номер счета</span><span class="sxs-lookup"><span data-stu-id="37c0f-1359">account number</span></span> 
- <span data-ttu-id="37c0f-1360">card number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1360">card number</span></span> 
- <span data-ttu-id="37c0f-1361">card no.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1361">card no.</span></span> 
- <span data-ttu-id="37c0f-1362">security number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1362">security number</span></span> 
- <span data-ttu-id="37c0f-1363">Центральной</span><span class="sxs-lookup"><span data-stu-id="37c0f-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="37c0f-1364">Кэйворд_кард_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="37c0f-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="37c0f-1365">acct nbr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1365">acct nbr</span></span> 
- <span data-ttu-id="37c0f-1366">acct num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1366">acct num</span></span> 
- <span data-ttu-id="37c0f-1367">acct no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1367">acct no</span></span> 
- <span data-ttu-id="37c0f-1368">american express
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1368">american express</span></span> 
- <span data-ttu-id="37c0f-1369">americanexpress
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1369">americanexpress</span></span> 
- <span data-ttu-id="37c0f-1370">americano espresso
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1370">americano espresso</span></span> 
- <span data-ttu-id="37c0f-1371">amex</span><span class="sxs-lookup"><span data-stu-id="37c0f-1371">amex</span></span> 
- <span data-ttu-id="37c0f-1372">atm card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1372">atm card</span></span> 
- <span data-ttu-id="37c0f-1373">atm cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1373">atm cards</span></span> 
- <span data-ttu-id="37c0f-1374">atm kaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1374">atm kaart</span></span> 
- <span data-ttu-id="37c0f-1375">atmcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1375">atmcard</span></span> 
- <span data-ttu-id="37c0f-1376">atmcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1376">atmcards</span></span> 
- <span data-ttu-id="37c0f-1377">atmkaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1377">atmkaart</span></span> 
- <span data-ttu-id="37c0f-1378">atmkaarten
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1378">atmkaarten</span></span> 
- <span data-ttu-id="37c0f-1379">bancontact
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1379">bancontact</span></span> 
- <span data-ttu-id="37c0f-1380">bank card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1380">bank card</span></span> 
- <span data-ttu-id="37c0f-1381">bankkaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1381">bankkaart</span></span> 
- <span data-ttu-id="37c0f-1382">card holder
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1382">card holder</span></span> 
- <span data-ttu-id="37c0f-1383">card holders
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1383">card holders</span></span> 
- <span data-ttu-id="37c0f-1384">card num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1384">card num</span></span> 
- <span data-ttu-id="37c0f-1385">card number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1385">card number</span></span> 
- <span data-ttu-id="37c0f-1386">card numbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1386">card numbers</span></span> 
- <span data-ttu-id="37c0f-1387">card type
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1387">card type</span></span> 
- <span data-ttu-id="37c0f-1388">cardano numerico
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1388">cardano numerico</span></span> 
- <span data-ttu-id="37c0f-1389">cardholder
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1389">cardholder</span></span> 
- <span data-ttu-id="37c0f-1390">cardholders
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1390">cardholders</span></span> 
- <span data-ttu-id="37c0f-1391">cardnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1391">cardnumber</span></span> 
- <span data-ttu-id="37c0f-1392">cardnumbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1392">cardnumbers</span></span> 
- <span data-ttu-id="37c0f-1393">carta bianca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1393">carta bianca</span></span> 
- <span data-ttu-id="37c0f-1394">carta credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1394">carta credito</span></span> 
- <span data-ttu-id="37c0f-1395">carta di credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1395">carta di credito</span></span> 
- <span data-ttu-id="37c0f-1396">cartao de credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1396">cartao de credito</span></span> 
- <span data-ttu-id="37c0f-1397">cartao de crédito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1397">cartao de crédito</span></span> 
- <span data-ttu-id="37c0f-1398">cartao de debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1398">cartao de debito</span></span> 
- <span data-ttu-id="37c0f-1399">cartao de débito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1399">cartao de débito</span></span> 
- <span data-ttu-id="37c0f-1400">carte bancaire
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1400">carte bancaire</span></span> 
- <span data-ttu-id="37c0f-1401">carte blanche
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1401">carte blanche</span></span> 
- <span data-ttu-id="37c0f-1402">carte bleue
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1402">carte bleue</span></span> 
- <span data-ttu-id="37c0f-1403">carte de credit
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1403">carte de credit</span></span> 
- <span data-ttu-id="37c0f-1404">carte de crédit
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1404">carte de crédit</span></span> 
- <span data-ttu-id="37c0f-1405">carte di credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1405">carte di credito</span></span> 
- <span data-ttu-id="37c0f-1406">carteblanche
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1406">carteblanche</span></span> 
- <span data-ttu-id="37c0f-1407">cartão de credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1407">cartão de credito</span></span> 
- <span data-ttu-id="37c0f-1408">cartão de crédito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1408">cartão de crédito</span></span> 
- <span data-ttu-id="37c0f-1409">cartão de debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1409">cartão de debito</span></span> 
- <span data-ttu-id="37c0f-1410">cartão de débito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1410">cartão de débito</span></span> 
- <span data-ttu-id="37c0f-1411">cb
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1411">cb</span></span> 
- <span data-ttu-id="37c0f-1412">ccn
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1412">ccn</span></span> 
- <span data-ttu-id="37c0f-1413">check card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1413">check card</span></span> 
- <span data-ttu-id="37c0f-1414">check cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1414">check cards</span></span> 
- <span data-ttu-id="37c0f-1415">checkcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1415">checkcard</span></span>
- <span data-ttu-id="37c0f-1416">checkcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1416">checkcards</span></span> 
- <span data-ttu-id="37c0f-1417">chequekaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1417">chequekaart</span></span> 
- <span data-ttu-id="37c0f-1418">cirrus
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1418">cirrus</span></span> 
- <span data-ttu-id="37c0f-1419">cirrus-edc-maestro
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="37c0f-1420">controlekaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1420">controlekaart</span></span> 
- <span data-ttu-id="37c0f-1421">controlekaarten
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1421">controlekaarten</span></span> 
- <span data-ttu-id="37c0f-1422">credit card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1422">credit card</span></span> 
- <span data-ttu-id="37c0f-1423">credit cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1423">credit cards</span></span> 
- <span data-ttu-id="37c0f-1424">creditcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1424">creditcard</span></span> 
- <span data-ttu-id="37c0f-1425">creditcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1425">creditcards</span></span> 
- <span data-ttu-id="37c0f-1426">debetkaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1426">debetkaart</span></span> 
- <span data-ttu-id="37c0f-1427">debetkaarten
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1427">debetkaarten</span></span> 
- <span data-ttu-id="37c0f-1428">debit card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1428">debit card</span></span> 
- <span data-ttu-id="37c0f-1429">debit cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1429">debit cards</span></span> 
- <span data-ttu-id="37c0f-1430">debitcard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1430">debitcard</span></span> 
- <span data-ttu-id="37c0f-1431">debitcards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1431">debitcards</span></span> 
- <span data-ttu-id="37c0f-1432">debito automatico
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1432">debito automatico</span></span> 
- <span data-ttu-id="37c0f-1433">diners club
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1433">diners club</span></span> 
- <span data-ttu-id="37c0f-1434">dinersclub
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1434">dinersclub</span></span> 
- <span data-ttu-id="37c0f-1435">Повтор</span><span class="sxs-lookup"><span data-stu-id="37c0f-1435">discover</span></span> 
- <span data-ttu-id="37c0f-1436">discover card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1436">discover card</span></span> 
- <span data-ttu-id="37c0f-1437">discover cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1437">discover cards</span></span> 
- <span data-ttu-id="37c0f-1438">discovercard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1438">discovercard</span></span> 
- <span data-ttu-id="37c0f-1439">discovercards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1439">discovercards</span></span> 
- <span data-ttu-id="37c0f-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="37c0f-1440">débito automático</span></span>
- <span data-ttu-id="37c0f-1441">
edc
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1441">edc</span></span> 
- <span data-ttu-id="37c0f-1442">eigentümername
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1442">eigentümername</span></span> 
- <span data-ttu-id="37c0f-1443">european debit card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1443">european debit card</span></span> 
- <span data-ttu-id="37c0f-1444">hoofdkaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1444">hoofdkaart</span></span> 
- <span data-ttu-id="37c0f-1445">hoofdkaarten
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="37c0f-1446">in viaggio
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1446">in viaggio</span></span> 
- <span data-ttu-id="37c0f-1447">japanese card bureau
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1447">japanese card bureau</span></span> 
- <span data-ttu-id="37c0f-1448">japanse kaartdienst
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="37c0f-1449">jcb
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1449">jcb</span></span> 
- <span data-ttu-id="37c0f-1450">kaart
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1450">kaart</span></span> 
- <span data-ttu-id="37c0f-1451">kaart num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1451">kaart num</span></span> 
- <span data-ttu-id="37c0f-1452">kaartaantal
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1452">kaartaantal</span></span> 
- <span data-ttu-id="37c0f-1453">kaartaantallen
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1453">kaartaantallen</span></span> 
- <span data-ttu-id="37c0f-1454">kaarthouder
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1454">kaarthouder</span></span> 
- <span data-ttu-id="37c0f-1455">kaarthouders
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1455">kaarthouders</span></span> 
- <span data-ttu-id="37c0f-1456">karte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1456">karte</span></span>  
- <span data-ttu-id="37c0f-1457">karteninhaber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1457">karteninhaber</span></span> 
- <span data-ttu-id="37c0f-1458">karteninhabers</span><span class="sxs-lookup"><span data-stu-id="37c0f-1458">karteninhabers</span></span>
- <span data-ttu-id="37c0f-1459">
kartennr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1459">kartennr</span></span> 
- <span data-ttu-id="37c0f-1460">kartennummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1460">kartennummer</span></span> 
- <span data-ttu-id="37c0f-1461">kreditkarte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1461">kreditkarte</span></span> 
- <span data-ttu-id="37c0f-1462">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="37c0f-1463">kreditkarteninhaber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="37c0f-1464">kreditkarteninstitut
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="37c0f-1465">kreditkartennummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="37c0f-1466">kreditkartentyp
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="37c0f-1467">maestro
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1467">maestro</span></span> 
- <span data-ttu-id="37c0f-1468">master card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1468">master card</span></span> 
- <span data-ttu-id="37c0f-1469">master cards
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1469">master cards</span></span> 
- <span data-ttu-id="37c0f-1470">mastercard
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1470">mastercard</span></span> 
- <span data-ttu-id="37c0f-1471">mastercards</span><span class="sxs-lookup"><span data-stu-id="37c0f-1471">mastercards</span></span> 
- <span data-ttu-id="37c0f-1472">MC</span><span class="sxs-lookup"><span data-stu-id="37c0f-1472">mc</span></span> 
- <span data-ttu-id="37c0f-1473">mister cash
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1473">mister cash</span></span> 
- <span data-ttu-id="37c0f-1474">n корзина</span><span class="sxs-lookup"><span data-stu-id="37c0f-1474">n carta</span></span> 
- <span data-ttu-id="37c0f-1475">Корзина "</span><span class="sxs-lookup"><span data-stu-id="37c0f-1475">carta</span></span> 
- <span data-ttu-id="37c0f-1476">нет де таржета</span><span class="sxs-lookup"><span data-stu-id="37c0f-1476">no de tarjeta</span></span> 
- <span data-ttu-id="37c0f-1477">не выполнять картао</span><span class="sxs-lookup"><span data-stu-id="37c0f-1477">no do cartao</span></span> 
- <span data-ttu-id="37c0f-1478">не выполнять картãо</span><span class="sxs-lookup"><span data-stu-id="37c0f-1478">no do cartão</span></span> 
- <span data-ttu-id="37c0f-p117">no. de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p117">no. de tarjeta</span></span> 
- <span data-ttu-id="37c0f-p118">no. do cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p118">no. do cartao</span></span> 
- <span data-ttu-id="37c0f-p119">no. do cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p119">no. do cartão</span></span> 
- <span data-ttu-id="37c0f-1485">нрная корзина</span><span class="sxs-lookup"><span data-stu-id="37c0f-1485">nr carta</span></span> 
- <span data-ttu-id="37c0f-p120">nr. carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p120">nr. carta</span></span> 
- <span data-ttu-id="37c0f-1488">numeri di scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1488">numeri di scheda</span></span> 
- <span data-ttu-id="37c0f-1489">numero carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1489">numero carta</span></span> 
- <span data-ttu-id="37c0f-1490">numero de cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1490">numero de cartao</span></span> 
- <span data-ttu-id="37c0f-1491">numero de carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1491">numero de carte</span></span> 
- <span data-ttu-id="37c0f-1492">numero de cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1492">numero de cartão</span></span> 
- <span data-ttu-id="37c0f-1493">numero de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1493">numero de tarjeta</span></span>
- <span data-ttu-id="37c0f-1494">numero della carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1494">numero della carta</span></span> 
- <span data-ttu-id="37c0f-1495">numero di carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1495">numero di carta</span></span> 
- <span data-ttu-id="37c0f-1496">numero di scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1496">numero di scheda</span></span> 
- <span data-ttu-id="37c0f-1497">numero do cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1497">numero do cartao</span></span> 
- <span data-ttu-id="37c0f-1498">numero do cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1498">numero do cartão</span></span> 
- <span data-ttu-id="37c0f-1499">numéro de carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1499">numéro de carte</span></span> 
- <span data-ttu-id="37c0f-1500">nº carta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1500">nº carta</span></span> 
- <span data-ttu-id="37c0f-1501">nº de carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1501">nº de carte</span></span> 
- <span data-ttu-id="37c0f-1502">nº de la carte
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1502">nº de la carte</span></span> 
- <span data-ttu-id="37c0f-1503">nº de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="37c0f-1504">nº do cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1504">nº do cartao</span></span> 
- <span data-ttu-id="37c0f-1505">n º Do картãо</span><span class="sxs-lookup"><span data-stu-id="37c0f-1505">nº do cartão</span></span> 
- <span data-ttu-id="37c0f-p121">nº. do cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p121">nº. do cartão</span></span> 
- <span data-ttu-id="37c0f-1508">número de cartao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1508">número de cartao</span></span> 
- <span data-ttu-id="37c0f-1509">número de cartão
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1509">número de cartão</span></span> 
- <span data-ttu-id="37c0f-1510">número de tarjeta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1510">número de tarjeta</span></span> 
- <span data-ttu-id="37c0f-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="37c0f-1511">número do cartao</span></span> 
- <span data-ttu-id="37c0f-1512">scheda dell'assegno
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="37c0f-1513">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="37c0f-1514">scheda dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="37c0f-1515">scheda della banca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1515">scheda della banca</span></span> 
- <span data-ttu-id="37c0f-1516">scheda di controllo
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1516">scheda di controllo</span></span> 
- <span data-ttu-id="37c0f-1517">scheda di debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1517">scheda di debito</span></span> 
- <span data-ttu-id="37c0f-1518">scheda matrice
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1518">scheda matrice</span></span> 
- <span data-ttu-id="37c0f-1519">schede dell'atmosfera
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="37c0f-1520">schede di controllo
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1520">schede di controllo</span></span> 
- <span data-ttu-id="37c0f-1521">schede di debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1521">schede di debito</span></span> 
- <span data-ttu-id="37c0f-1522">schede matrici
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1522">schede matrici</span></span> 
- <span data-ttu-id="37c0f-1523">scoprono la scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="37c0f-1524">scoprono le schede
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1524">scoprono le schede</span></span> 
- <span data-ttu-id="37c0f-1525">solo
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1525">solo</span></span> 
- <span data-ttu-id="37c0f-1526">supporti di scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1526">supporti di scheda</span></span> 
- <span data-ttu-id="37c0f-1527">supporto di scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1527">supporto di scheda</span></span> 
- <span data-ttu-id="37c0f-1528">ключ</span><span class="sxs-lookup"><span data-stu-id="37c0f-1528">switch</span></span> 
- <span data-ttu-id="37c0f-1529">tarjeta atm
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1529">tarjeta atm</span></span> 
- <span data-ttu-id="37c0f-1530">tarjeta credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1530">tarjeta credito</span></span> 
- <span data-ttu-id="37c0f-1531">tarjeta de atm
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="37c0f-1532">tarjeta de credito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="37c0f-1533">tarjeta de debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="37c0f-1534">tarjeta debito
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1534">tarjeta debito</span></span> 
- <span data-ttu-id="37c0f-1535">tarjeta no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1535">tarjeta no</span></span>
- <span data-ttu-id="37c0f-1536">tarjetahabiente
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="37c0f-1537">tipo della scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1537">tipo della scheda</span></span> 
- <span data-ttu-id="37c0f-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="37c0f-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="37c0f-1539">scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1539">scheda</span></span> 
- <span data-ttu-id="37c0f-1540">v pay
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1540">v pay</span></span> 
- <span data-ttu-id="37c0f-1541">v — оплата</span><span class="sxs-lookup"><span data-stu-id="37c0f-1541">v-pay</span></span> 
- <span data-ttu-id="37c0f-1542">visa
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1542">visa</span></span> 
- <span data-ttu-id="37c0f-1543">visa plus
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1543">visa plus</span></span> 
- <span data-ttu-id="37c0f-1544">visa electron
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1544">visa electron</span></span> 
- <span data-ttu-id="37c0f-1545">visto
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1545">visto</span></span> 
- <span data-ttu-id="37c0f-1546">visum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1546">visum</span></span> 
- <span data-ttu-id="37c0f-1547">vpay
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="37c0f-1548">Кэйворд_кард_секурити_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="37c0f-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="37c0f-1549">card identification number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1549">card identification number</span></span>
- <span data-ttu-id="37c0f-1550">card verification</span><span class="sxs-lookup"><span data-stu-id="37c0f-1550">card verification</span></span> 
- <span data-ttu-id="37c0f-1551">cardi la verifica
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1551">cardi la verifica</span></span> 
- <span data-ttu-id="37c0f-1552">cid
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1552">cid</span></span> 
- <span data-ttu-id="37c0f-1553">СЕГ наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1553">cod seg</span></span> 
- <span data-ttu-id="37c0f-1554">сегуранка наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1554">cod seguranca</span></span> 
- <span data-ttu-id="37c0f-1555">сегуранçа наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1555">cod segurança</span></span> 
- <span data-ttu-id="37c0f-1556">сикурезза наложенного платежа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1556">cod sicurezza</span></span> 
- <span data-ttu-id="37c0f-p122">cod. seg
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p122">cod. seg</span></span> 
- <span data-ttu-id="37c0f-p123">cod. seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p123">cod. seguranca</span></span> 
- <span data-ttu-id="37c0f-p124">cod. segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p124">cod. segurança</span></span> 
- <span data-ttu-id="37c0f-p125">cod. sicurezza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p125">cod. sicurezza</span></span> 
- <span data-ttu-id="37c0f-1565">codice di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="37c0f-1566">codice di verifica
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1566">codice di verifica</span></span> 
- <span data-ttu-id="37c0f-1567">codigo
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1567">codigo</span></span> 
- <span data-ttu-id="37c0f-1568">codigo de seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="37c0f-1569">codigo de segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1569">codigo de segurança</span></span> 
- <span data-ttu-id="37c0f-1570">crittogramma
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1570">crittogramma</span></span> 
- <span data-ttu-id="37c0f-1571">cryptogram
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1571">cryptogram</span></span> 
- <span data-ttu-id="37c0f-1572">cryptogramme
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1572">cryptogramme</span></span> 
- <span data-ttu-id="37c0f-1573">CV2</span><span class="sxs-lookup"><span data-stu-id="37c0f-1573">cv2</span></span> 
- <span data-ttu-id="37c0f-1574">cvc
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1574">cvc</span></span> 
- <span data-ttu-id="37c0f-1575">CVC2</span><span class="sxs-lookup"><span data-stu-id="37c0f-1575">cvc2</span></span> 
- <span data-ttu-id="37c0f-1576">cvn
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1576">cvn</span></span> 
- <span data-ttu-id="37c0f-1577">cvv
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1577">cvv</span></span> 
- <span data-ttu-id="37c0f-1578">CVV2</span><span class="sxs-lookup"><span data-stu-id="37c0f-1578">cvv2</span></span> 
- <span data-ttu-id="37c0f-1579">кóд сегуранка</span><span class="sxs-lookup"><span data-stu-id="37c0f-1579">cód seguranca</span></span> 
- <span data-ttu-id="37c0f-1580">кóд сегуранçа</span><span class="sxs-lookup"><span data-stu-id="37c0f-1580">cód segurança</span></span> 
- <span data-ttu-id="37c0f-p126">cód. seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p126">cód. seguranca</span></span> 
- <span data-ttu-id="37c0f-p127">cód. segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p127">cód. segurança</span></span> 
- <span data-ttu-id="37c0f-1585">código
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1585">código</span></span> 
- <span data-ttu-id="37c0f-1586">código de seguranca
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1586">código de seguranca</span></span> 
- <span data-ttu-id="37c0f-1587">código de segurança
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1587">código de segurança</span></span> 
- <span data-ttu-id="37c0f-1588">de kaart controle
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1588">de kaart controle</span></span> 
- <span data-ttu-id="37c0f-1589">geeft nr uit
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1589">geeft nr uit</span></span> 
- <span data-ttu-id="37c0f-1590">issue no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1590">issue no</span></span> 
- <span data-ttu-id="37c0f-1591">issue number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1591">issue number</span></span> 
- <span data-ttu-id="37c0f-1592">kaartidentificatienummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="37c0f-1593">kreditkartenprufnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="37c0f-1594">kreditkartenprüfnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="37c0f-1595">kwestieaantal
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1595">kwestieaantal</span></span> 
- <span data-ttu-id="37c0f-p128">no. dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p128">no. dell'edizione</span></span> 
- <span data-ttu-id="37c0f-p129">no. di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p129">no. di sicurezza</span></span> 
- <span data-ttu-id="37c0f-1600">numero de securite
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1600">numero de securite</span></span> 
- <span data-ttu-id="37c0f-1601">numero de verificacao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1601">numero de verificacao</span></span> 
- <span data-ttu-id="37c0f-1602">numero dell'edizione
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="37c0f-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="37c0f-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="37c0f-1604">scheda
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1604">scheda</span></span> 
- <span data-ttu-id="37c0f-1605">numero di sicurezza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="37c0f-1606">numero van veiligheid
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="37c0f-1607">numéro de sécurité
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="37c0f-1608">nº autorizzazione
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="37c0f-1609">número de verificação
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1609">número de verificação</span></span> 
- <span data-ttu-id="37c0f-1610">perno il blocco
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1610">perno il blocco</span></span> 
- <span data-ttu-id="37c0f-1611">pin block
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1611">pin block</span></span> 
- <span data-ttu-id="37c0f-1612">prufziffer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1612">prufziffer</span></span> 
- <span data-ttu-id="37c0f-1613">prüfziffer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1613">prüfziffer</span></span> 
- <span data-ttu-id="37c0f-1614">security code
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1614">security code</span></span> 
- <span data-ttu-id="37c0f-1615">security no
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1615">security no</span></span> 
- <span data-ttu-id="37c0f-1616">security number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1616">security number</span></span> 
- <span data-ttu-id="37c0f-1617">sicherheits kode
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1617">sicherheits kode</span></span> 
- <span data-ttu-id="37c0f-1618">sicherheitscode
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1618">sicherheitscode</span></span> 
- <span data-ttu-id="37c0f-1619">sicherheitsnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="37c0f-1620">speldblok
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1620">speldblok</span></span> 
- <span data-ttu-id="37c0f-1621">veiligheid nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1621">veiligheid nr</span></span> 
- <span data-ttu-id="37c0f-1622">veiligheidsaantal
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="37c0f-1623">veiligheidscode
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1623">veiligheidscode</span></span> 
- <span data-ttu-id="37c0f-1624">veiligheidsnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="37c0f-1625">verfalldatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="37c0f-1626">Кэйворд_кард_експиратион_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="37c0f-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="37c0f-1627">ablauf
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1627">ablauf</span></span> 
- <span data-ttu-id="37c0f-1628">data de expiracao
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1628">data de expiracao</span></span> 
- <span data-ttu-id="37c0f-1629">data de expiração
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1629">data de expiração</span></span> 
- <span data-ttu-id="37c0f-1630">data del exp
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1630">data del exp</span></span> 
- <span data-ttu-id="37c0f-1631">data di exp
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1631">data di exp</span></span> 
- <span data-ttu-id="37c0f-1632">data di scadenza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1632">data di scadenza</span></span> 
- <span data-ttu-id="37c0f-1633">data em que expira
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1633">data em que expira</span></span> 
- <span data-ttu-id="37c0f-1634">data scad
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1634">data scad</span></span> 
- <span data-ttu-id="37c0f-1635">data scadenza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1635">data scadenza</span></span> 
- <span data-ttu-id="37c0f-1636">date de validité
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1636">date de validité</span></span> 
- <span data-ttu-id="37c0f-1637">datum afloop
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1637">datum afloop</span></span> 
- <span data-ttu-id="37c0f-1638">datum van exp
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1638">datum van exp</span></span> 
- <span data-ttu-id="37c0f-1639">de afloop
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1639">de afloop</span></span> 
- <span data-ttu-id="37c0f-1640">espira
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1640">espira</span></span> 
- <span data-ttu-id="37c0f-1641">espira
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1641">espira</span></span> 
- <span data-ttu-id="37c0f-1642">exp date
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1642">exp date</span></span> 
- <span data-ttu-id="37c0f-1643">exp datum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1643">exp datum</span></span> 
- <span data-ttu-id="37c0f-1644">срока действия</span><span class="sxs-lookup"><span data-stu-id="37c0f-1644">expiration</span></span> 
- <span data-ttu-id="37c0f-1645">expire
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1645">expire</span></span> 
- <span data-ttu-id="37c0f-1646">expires
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1646">expires</span></span> 
- <span data-ttu-id="37c0f-1647">expiry
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1647">expiry</span></span> 
- <span data-ttu-id="37c0f-1648">fecha de expiracion
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="37c0f-1649">fecha de venc
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1649">fecha de venc</span></span> 
- <span data-ttu-id="37c0f-1650">gultig bis
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1650">gultig bis</span></span> 
- <span data-ttu-id="37c0f-1651">gultigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="37c0f-1652">gültig bis
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1652">gültig bis</span></span> 
- <span data-ttu-id="37c0f-1653">gültigkeitsdatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="37c0f-1654">la scadenza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1654">la scadenza</span></span> 
- <span data-ttu-id="37c0f-1655">scadenza
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1655">scadenza</span></span> 
- <span data-ttu-id="37c0f-1656">valable
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1656">valable</span></span> 
- <span data-ttu-id="37c0f-1657">validade
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1657">validade</span></span> 
- <span data-ttu-id="37c0f-1658">valido hasta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1658">valido hasta</span></span> 
- <span data-ttu-id="37c0f-1659">valor
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1659">valor</span></span> 
- <span data-ttu-id="37c0f-1660">venc
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1660">venc</span></span> 
- <span data-ttu-id="37c0f-1661">vencimento
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1661">vencimento</span></span> 
- <span data-ttu-id="37c0f-1662">vencimiento
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1662">vencimiento</span></span> 
- <span data-ttu-id="37c0f-1663">verloopt
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1663">verloopt</span></span> 
- <span data-ttu-id="37c0f-1664">vervaldag
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1664">vervaldag</span></span> 
- <span data-ttu-id="37c0f-1665">vervaldatum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1665">vervaldatum</span></span> 
- <span data-ttu-id="37c0f-1666">vto
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1666">vto</span></span> 
- <span data-ttu-id="37c0f-1667">válido hasta
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="37c0f-1668">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="37c0f-1668">EU Driver's License Number</span></span>

<span data-ttu-id="37c0f-1669">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="37c0f-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="37c0f-1670">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="37c0f-1670">EU National Identification Number</span></span>

<span data-ttu-id="37c0f-1671">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационНого номера ЕС](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="37c0f-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="37c0f-1672">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="37c0f-1672">EU Passport Number</span></span>

<span data-ttu-id="37c0f-1673">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="37c0f-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="37c0f-1674">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="37c0f-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="37c0f-1675">Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="37c0f-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="37c0f-1676">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="37c0f-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="37c0f-1677">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогОвого кода ЕС](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="37c0f-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="37c0f-1678">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="37c0f-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1679">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1679">Format</span></span>

<span data-ttu-id="37c0f-1680">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1681">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1681">Pattern</span></span>

<span data-ttu-id="37c0f-1682">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="37c0f-1683">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="37c0f-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="37c0f-1684">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="37c0f-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="37c0f-1685">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="37c0f-1686">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1687">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1687">Checksum</span></span>

<span data-ttu-id="37c0f-1688">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1689">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1689">Definition</span></span>

<span data-ttu-id="37c0f-1690">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1691">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1692">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="37c0f-1693">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1694">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1694">Keywords</span></span>

- <span data-ttu-id="37c0f-1695">Кэйворд_финниш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="37c0f-1696">

Sosiaaliturvatunnus</span><span class="sxs-lookup"><span data-stu-id="37c0f-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="37c0f-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="37c0f-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="37c0f-1698">Personbeteckning</span><span class="sxs-lookup"><span data-stu-id="37c0f-1698">Personbeteckning</span></span>
- <span data-ttu-id="37c0f-1699">Personnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="37c0f-1700">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="37c0f-1700">Finland Passport Number</span></span>

<span data-ttu-id="37c0f-p130">Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Режекс_финланд_пасспорт_нумбер находит содержимое, которое соответствует шаблону. Найдено ключевое слово из Кэйворд_финланд_пасспорт_нумбер. Ключевые слова <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity></span><span class="sxs-lookup"><span data-stu-id="37c0f-p130">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern. A keyword from Keyword_finland_passport_number is found. <!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity> Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="37c0f-1705">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="37c0f-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1706">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1706">Format</span></span>

<span data-ttu-id="37c0f-1707">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1708">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1708">Pattern</span></span>

<span data-ttu-id="37c0f-1709">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1710">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1710">Checksum</span></span>

<span data-ttu-id="37c0f-1711">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1712">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1712">Definition</span></span>

<span data-ttu-id="37c0f-1713">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1714">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1715">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="37c0f-1716">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="37c0f-1717">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1717">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1718">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="37c0f-1719">Кэйворд_френч_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="37c0f-1720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="37c0f-1720">drivers licence</span></span>
- <span data-ttu-id="37c0f-1721">drivers license</span><span class="sxs-lookup"><span data-stu-id="37c0f-1721">drivers license</span></span>
- <span data-ttu-id="37c0f-1722">driving licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1722">driving licence</span></span>
- <span data-ttu-id="37c0f-1723">Управление лицензией</span><span class="sxs-lookup"><span data-stu-id="37c0f-1723">driving license</span></span>
- <span data-ttu-id="37c0f-1724">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="37c0f-1724">permis de conduire</span></span>
- <span data-ttu-id="37c0f-1725">
licence number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1725">licence number</span></span>
- <span data-ttu-id="37c0f-1726">
license number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1726">license number</span></span>
- <span data-ttu-id="37c0f-1727">
licence numbers</span><span class="sxs-lookup"><span data-stu-id="37c0f-1727">licence numbers</span></span>
- <span data-ttu-id="37c0f-1728">

license numbers</span><span class="sxs-lookup"><span data-stu-id="37c0f-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="37c0f-1729">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1730">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1730">Format</span></span>

<span data-ttu-id="37c0f-1731">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1732">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1732">Pattern</span></span>

<span data-ttu-id="37c0f-1733">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1734">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1734">Checksum</span></span>

<span data-ttu-id="37c0f-1735">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1736">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1736">Definition</span></span>

<span data-ttu-id="37c0f-1737">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1738">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1739">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1739">Keywords</span></span>

<span data-ttu-id="37c0f-1740">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="37c0f-1741">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="37c0f-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1742">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1742">Format</span></span>

<span data-ttu-id="37c0f-1743">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1744">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1744">Pattern</span></span>

<span data-ttu-id="37c0f-1745">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="37c0f-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="37c0f-1746">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-1746">Two digits</span></span> 
- <span data-ttu-id="37c0f-1747">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-1748">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1749">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1749">Checksum</span></span>

<span data-ttu-id="37c0f-1750">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1751">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1751">Definition</span></span>

<span data-ttu-id="37c0f-1752">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1753">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1754">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1755">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="37c0f-1756">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-1756">Keyword_passport</span></span>

- <span data-ttu-id="37c0f-1757">Passport Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1757">Passport Number</span></span>
- <span data-ttu-id="37c0f-1758">
Passport No</span><span class="sxs-lookup"><span data-stu-id="37c0f-1758">Passport No</span></span>
- <span data-ttu-id="37c0f-1759">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1759">Passport #</span></span>
- <span data-ttu-id="37c0f-1760">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1760">Passport#</span></span>
- <span data-ttu-id="37c0f-1761">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="37c0f-1761">PassportID</span></span>
- <span data-ttu-id="37c0f-1762">Passportno
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1762">Passportno</span></span>
- <span data-ttu-id="37c0f-1763">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1763">passportnumber</span></span>
- <span data-ttu-id="37c0f-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="37c0f-1764">パスポート</span></span>
- <span data-ttu-id="37c0f-1765">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1765">パスポート番号</span></span>
- <span data-ttu-id="37c0f-1766">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1766">パスポートのNum</span></span>
- <span data-ttu-id="37c0f-1767">
パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1767">パスポート ＃</span></span> 
- <span data-ttu-id="37c0f-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="37c0f-1768">Numéro de passeport</span></span>
- <span data-ttu-id="37c0f-1769">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="37c0f-1769">Passeport n °</span></span>
- <span data-ttu-id="37c0f-1770">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1770">Passeport Non</span></span>
- <span data-ttu-id="37c0f-1771">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1771">Passeport #</span></span>
- <span data-ttu-id="37c0f-1772">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1772">Passeport#</span></span>
- <span data-ttu-id="37c0f-1773">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1773">PasseportNon</span></span>
- <span data-ttu-id="37c0f-1774">

Passeportn °</span><span class="sxs-lookup"><span data-stu-id="37c0f-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="37c0f-1775">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1776">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1776">Format</span></span>

<span data-ttu-id="37c0f-1777">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1778">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1778">Pattern</span></span>

<span data-ttu-id="37c0f-1779">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="37c0f-1780">13 цифр, за которыми следует пробел, за которым следуют две цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="37c0f-1781">или</span><span class="sxs-lookup"><span data-stu-id="37c0f-1781">or</span></span>
- <span data-ttu-id="37c0f-1782">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1783">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1783">Checksum</span></span>

<span data-ttu-id="37c0f-1784">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1785">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1785">Definition</span></span>

<span data-ttu-id="37c0f-1786">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1787">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1788">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="37c0f-1789">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1789">The checksum passes.</span></span>

<span data-ttu-id="37c0f-1790">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1791">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1792">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="37c0f-1793">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1793">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1794">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="37c0f-1795">Кэйворд_фр_инси</span><span class="sxs-lookup"><span data-stu-id="37c0f-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="37c0f-1796">insee</span><span class="sxs-lookup"><span data-stu-id="37c0f-1796">insee</span></span>
- <span data-ttu-id="37c0f-1797">
securité sociale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1797">securité sociale</span></span>
- <span data-ttu-id="37c0f-1798">
securite sociale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1798">securite sociale</span></span>
- <span data-ttu-id="37c0f-1799">
national id</span><span class="sxs-lookup"><span data-stu-id="37c0f-1799">national id</span></span>
- <span data-ttu-id="37c0f-1800">
national identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-1800">national identification</span></span>
- <span data-ttu-id="37c0f-1801">
numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="37c0f-1801">numéro d'identité</span></span>
- <span data-ttu-id="37c0f-1802">нет д'идентитé</span><span class="sxs-lookup"><span data-stu-id="37c0f-1802">no d'identité</span></span>
- <span data-ttu-id="37c0f-p131">
no. d'identité</span><span class="sxs-lookup"><span data-stu-id="37c0f-p131">no. d'identité</span></span>
- <span data-ttu-id="37c0f-1805">
numero d'identite</span><span class="sxs-lookup"><span data-stu-id="37c0f-1805">numero d'identite</span></span>
- <span data-ttu-id="37c0f-1806">нет д'идентите</span><span class="sxs-lookup"><span data-stu-id="37c0f-1806">no d'identite</span></span>
- <span data-ttu-id="37c0f-p132">
no. d'identite</span><span class="sxs-lookup"><span data-stu-id="37c0f-p132">no. d'identite</span></span>
- <span data-ttu-id="37c0f-1809">social security number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1809">social security number</span></span>
- <span data-ttu-id="37c0f-1810">
social security code</span><span class="sxs-lookup"><span data-stu-id="37c0f-1810">social security code</span></span>
- <span data-ttu-id="37c0f-1811">social insurance number</span><span class="sxs-lookup"><span data-stu-id="37c0f-1811">social insurance number</span></span>
- <span data-ttu-id="37c0f-1812">
le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="37c0f-1813">
d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1813">d'identité nationale</span></span>
- <span data-ttu-id="37c0f-1814">
numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="37c0f-1815">
le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="37c0f-1816">
numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="37c0f-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="37c0f-1817">
numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="37c0f-1817">numéro de sécu</span></span>
- <span data-ttu-id="37c0f-1818">
code sécu
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="37c0f-1819">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="37c0f-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1820">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1820">Format</span></span>

<span data-ttu-id="37c0f-1821">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1822">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1822">Pattern</span></span>

<span data-ttu-id="37c0f-1823">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="37c0f-1824">цифра или буква; </span><span class="sxs-lookup"><span data-stu-id="37c0f-1824">A digit or letter</span></span> 
- <span data-ttu-id="37c0f-1825">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-1825">Two digits</span></span> 
- <span data-ttu-id="37c0f-1826">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="37c0f-1826">Six digits or letters</span></span> 
- <span data-ttu-id="37c0f-1827">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="37c0f-1827">A digit</span></span> 
- <span data-ttu-id="37c0f-1828">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="37c0f-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1829">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1829">Checksum</span></span>

<span data-ttu-id="37c0f-1830">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1831">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1831">Definition</span></span>

<span data-ttu-id="37c0f-1832">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1833">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1834">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="37c0f-1835">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="37c0f-1836">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="37c0f-1837">найдено ключевое слово из Keyword_german_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="37c0f-1838">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1838">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1839">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="37c0f-1840">Кэйворд_жерман_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="37c0f-1841">Führerschein</span><span class="sxs-lookup"><span data-stu-id="37c0f-1841">Führerschein</span></span>
- <span data-ttu-id="37c0f-1842">
Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="37c0f-1842">Fuhrerschein</span></span>
- <span data-ttu-id="37c0f-1843">Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="37c0f-1843">Fuehrerschein</span></span>
- <span data-ttu-id="37c0f-1844">
Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="37c0f-1845">
Fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="37c0f-1846">
Fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="37c0f-1847">
Führerschein-
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1847">Führerschein-</span></span> 
- <span data-ttu-id="37c0f-1848">Fuhrerschein-
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="37c0f-1849">Fuehrerschein-
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="37c0f-1850">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="37c0f-1851">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="37c0f-1852">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="37c0f-1853">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="37c0f-1854">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="37c0f-1855">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="37c0f-1856">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="37c0f-1857">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="37c0f-1858">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="37c0f-1859">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="37c0f-1860">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="37c0f-1861">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="37c0f-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="37c0f-1862">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="37c0f-1863">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="37c0f-1864">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="37c0f-1865">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="37c0f-1866">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="37c0f-1867">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="37c0f-1868">Führerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="37c0f-1869">Fuhrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="37c0f-1870">Fuehrerschein- Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="37c0f-1871">Führerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="37c0f-1872">Fuhrerschein- Klasse
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="37c0f-1873">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="37c0f-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="37c0f-1874">DL</span><span class="sxs-lookup"><span data-stu-id="37c0f-1874">DL</span></span> 
- <span data-ttu-id="37c0f-1875">DLS</span><span class="sxs-lookup"><span data-stu-id="37c0f-1875">DLS</span></span>
- <span data-ttu-id="37c0f-1876">
Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1876">Driv Lic</span></span> 
- <span data-ttu-id="37c0f-1877">Driv Licen
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1877">Driv Licen</span></span> 
- <span data-ttu-id="37c0f-1878">Driv License</span><span class="sxs-lookup"><span data-stu-id="37c0f-1878">Driv License</span></span>
- <span data-ttu-id="37c0f-1879">
Driv Licenses
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1879">Driv Licenses</span></span> 
- <span data-ttu-id="37c0f-1880">Driv Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1880">Driv Licence</span></span> 
- <span data-ttu-id="37c0f-1881">Driv Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1881">Driv Licences</span></span> 
- <span data-ttu-id="37c0f-1882">Driv Lic
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1882">Driv Lic</span></span> 
- <span data-ttu-id="37c0f-1883">Driver Licen
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1883">Driver Licen</span></span> 
- <span data-ttu-id="37c0f-1884">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1884">Driver License</span></span> 
- <span data-ttu-id="37c0f-1885">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-1885">Driver Licenses</span></span> 
- <span data-ttu-id="37c0f-1886">Driver Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1886">Driver Licence</span></span> 
- <span data-ttu-id="37c0f-1887">Driver Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1887">Driver Licences</span></span> 
- <span data-ttu-id="37c0f-1888">Драйверы Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-1888">Drivers Lic</span></span> 
- <span data-ttu-id="37c0f-1889">Драйверы лицен</span><span class="sxs-lookup"><span data-stu-id="37c0f-1889">Drivers Licen</span></span> 
- <span data-ttu-id="37c0f-1890">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-1890">Drivers License</span></span> 
- <span data-ttu-id="37c0f-1891">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="37c0f-1892">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-1892">Drivers Licence</span></span> 
- <span data-ttu-id="37c0f-1893">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-1893">Drivers Licences</span></span> 
- <span data-ttu-id="37c0f-1894">Лик драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-1894">Driver's Lic</span></span> 
- <span data-ttu-id="37c0f-1895">Driver's Licen
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1895">Driver's Licen</span></span> 
- <span data-ttu-id="37c0f-1896">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1896">Driver's License</span></span> 
- <span data-ttu-id="37c0f-1897">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="37c0f-1898">Driver's Licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1898">Driver's Licence</span></span> 
- <span data-ttu-id="37c0f-1899">Driver's Licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1899">Driver's Licences</span></span> 
- <span data-ttu-id="37c0f-1900">Driving Lic
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1900">Driving Lic</span></span> 
- <span data-ttu-id="37c0f-1901">Driving Licen
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1901">Driving Licen</span></span> 
- <span data-ttu-id="37c0f-1902">Driving License
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1902">Driving License</span></span> 
- <span data-ttu-id="37c0f-1903">Driving Licenses
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1903">Driving Licenses</span></span> 
- <span data-ttu-id="37c0f-1904">Driving Licence

</span><span class="sxs-lookup"><span data-stu-id="37c0f-1904">Driving Licence</span></span> 
- <span data-ttu-id="37c0f-1905">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="37c0f-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="37c0f-1906">Кэйворд_жерман_дриверс_лиценсе_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="37c0f-1907">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="37c0f-1908">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="37c0f-1909">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="37c0f-1910">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1910">No-Führerschein</span></span> 
- <span data-ttu-id="37c0f-1911">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="37c0f-1912">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="37c0f-1913">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1913">N-Führerschein</span></span> 
- <span data-ttu-id="37c0f-1914">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="37c0f-1915">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="37c0f-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="37c0f-1916">
Nr-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="37c0f-1917">Nr-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="37c0f-1918">Nr-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="37c0f-1919">No-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1919">No-Führerschein</span></span> 
- <span data-ttu-id="37c0f-1920">No-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="37c0f-1921">No-Fuehrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="37c0f-1922">N-Führerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1922">N-Führerschein</span></span> 
- <span data-ttu-id="37c0f-1923">N-Fuhrerschein
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="37c0f-1924">N-Fuehrerschein</span><span class="sxs-lookup"><span data-stu-id="37c0f-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="37c0f-1925">Кэйворд_жерман_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="37c0f-1926">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="37c0f-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="37c0f-1927">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="37c0f-1927">ausstellungsort</span></span>
- <span data-ttu-id="37c0f-1928">
ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="37c0f-1928">ausstellende behöde</span></span>
- <span data-ttu-id="37c0f-1929">
ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="37c0f-1929">ausstellende behorde</span></span>
- <span data-ttu-id="37c0f-1930">

ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="37c0f-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="37c0f-1931">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="37c0f-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1932">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1932">Format</span></span>

<span data-ttu-id="37c0f-1933">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1934">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1934">Pattern</span></span>

<span data-ttu-id="37c0f-1935">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="37c0f-1936">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="37c0f-1937">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-1937">Three digits</span></span> 
- <span data-ttu-id="37c0f-1938">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="37c0f-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="37c0f-1939">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="37c0f-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1940">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1940">Checksum</span></span>

<span data-ttu-id="37c0f-1941">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1942">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1942">Definition</span></span>

<span data-ttu-id="37c0f-1943">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1944">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1945">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="37c0f-1946">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1946">The checksum passes.</span></span>

<span data-ttu-id="37c0f-1947">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1948">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1949">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="37c0f-1950">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1950">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-1951">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="37c0f-1952">Кэйворд_жерман_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="37c0f-1953">reisepass</span><span class="sxs-lookup"><span data-stu-id="37c0f-1953">reisepass</span></span>
- <span data-ttu-id="37c0f-1954">
reisepasse</span><span class="sxs-lookup"><span data-stu-id="37c0f-1954">reisepasse</span></span>
- <span data-ttu-id="37c0f-1955">
reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1955">reisepassnummer</span></span>
- <span data-ttu-id="37c0f-1956">passport</span><span class="sxs-lookup"><span data-stu-id="37c0f-1956">passport</span></span>
- <span data-ttu-id="37c0f-1957">

passports</span><span class="sxs-lookup"><span data-stu-id="37c0f-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="37c0f-1958">Кэйворд_жерман_пасспорт_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="37c0f-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="37c0f-1959">geburtsdatum</span><span class="sxs-lookup"><span data-stu-id="37c0f-1959">geburtsdatum</span></span>
- <span data-ttu-id="37c0f-1960">ausstellungsdatum</span><span class="sxs-lookup"><span data-stu-id="37c0f-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="37c0f-1961">
ausstellungsort</span><span class="sxs-lookup"><span data-stu-id="37c0f-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="37c0f-1962">Кэйворд_жерман_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="37c0f-1963">No — Реисепасс НР — Реисепасс</span><span class="sxs-lookup"><span data-stu-id="37c0f-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="37c0f-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="37c0f-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="37c0f-1965">Reisepass-Nr
</span><span class="sxs-lookup"><span data-stu-id="37c0f-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="37c0f-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="37c0f-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="37c0f-1967">бнатионалит. t</span><span class="sxs-lookup"><span data-stu-id="37c0f-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="37c0f-1968">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="37c0f-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1969">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1969">Format</span></span>

<span data-ttu-id="37c0f-1970">С 1 ноября 2010: девять букв и цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="37c0f-1971">От 1 апреля 1987 до 31 октября 2010:10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1972">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1972">Pattern</span></span>

<span data-ttu-id="37c0f-1973">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="37c0f-1974">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-1975">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1975">Eight digits</span></span>

<span data-ttu-id="37c0f-1976">От 1 апреля 1987 до 31 октября 2010:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="37c0f-1977">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-1978">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-1978">Checksum</span></span>

<span data-ttu-id="37c0f-1979">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-1980">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-1980">Definition</span></span>

<span data-ttu-id="37c0f-1981">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-1982">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-1983">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-1984">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="37c0f-1985">Кэйворд_жермани_ид_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="37c0f-1986">Identity Card</span><span class="sxs-lookup"><span data-stu-id="37c0f-1986">Identity Card</span></span>
- <span data-ttu-id="37c0f-1987">ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-1987">ID</span></span>
- <span data-ttu-id="37c0f-1988">Identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-1988">Identification</span></span>
- <span data-ttu-id="37c0f-1989">Personalausweis</span><span class="sxs-lookup"><span data-stu-id="37c0f-1989">Personalausweis</span></span>
- <span data-ttu-id="37c0f-1990">Identifizierungsnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="37c0f-1991">Ausweis</span><span class="sxs-lookup"><span data-stu-id="37c0f-1991">Ausweis</span></span>
- <span data-ttu-id="37c0f-1992">Identifikation</span><span class="sxs-lookup"><span data-stu-id="37c0f-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="37c0f-1993">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="37c0f-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-1994">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-1994">Format</span></span>

<span data-ttu-id="37c0f-1995">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="37c0f-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-1996">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-1996">Pattern</span></span>

<span data-ttu-id="37c0f-1997">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="37c0f-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="37c0f-1998">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="37c0f-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="37c0f-1999">Тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-1999">A dash</span></span> 
- <span data-ttu-id="37c0f-2000">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2000">Six digits</span></span>

<span data-ttu-id="37c0f-2001">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="37c0f-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="37c0f-2002">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="37c0f-2003">Тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-2003">A dash</span></span> 
- <span data-ttu-id="37c0f-2004">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2005">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2005">Checksum</span></span>

<span data-ttu-id="37c0f-2006">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2007">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2007">Definition</span></span>

<span data-ttu-id="37c0f-2008">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2009">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2010">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2011">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="37c0f-2012">Кэйворд_грице_ид_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="37c0f-2013">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2013">Greek identity Card</span></span>
- <span data-ttu-id="37c0f-2014">Tautotita</span><span class="sxs-lookup"><span data-stu-id="37c0f-2014">Tautotita</span></span>
- <span data-ttu-id="37c0f-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="37c0f-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="37c0f-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="37c0f-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="37c0f-2017">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2018">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2018">Format</span></span>

<span data-ttu-id="37c0f-2019">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2020">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2020">Pattern</span></span>

<span data-ttu-id="37c0f-2021">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="37c0f-2022">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2023">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2023">Six digits</span></span> 
- <span data-ttu-id="37c0f-2024">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="37c0f-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2025">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2025">Checksum</span></span>

<span data-ttu-id="37c0f-2026">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2027">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2027">Definition</span></span>

<span data-ttu-id="37c0f-2028">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2029">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2030">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="37c0f-2031">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2031">The checksum passes.</span></span>

<span data-ttu-id="37c0f-2032">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2033">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2034">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2034">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2035">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="37c0f-2036">Кэйворд_хонг_конг_ид_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="37c0f-2037">идентификационная карточка Гонконг</span><span class="sxs-lookup"><span data-stu-id="37c0f-2037">hong kong identity card</span></span>
- <span data-ttu-id="37c0f-2038">ХКИДК</span><span class="sxs-lookup"><span data-stu-id="37c0f-2038">HKIDC</span></span>
- <span data-ttu-id="37c0f-2039">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-2039">id card</span></span>
- <span data-ttu-id="37c0f-2040">identity card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2040">identity card</span></span>
- <span data-ttu-id="37c0f-2041">идентификационная карточка HK</span><span class="sxs-lookup"><span data-stu-id="37c0f-2041">hk identity card</span></span>
- <span data-ttu-id="37c0f-2042">Идентификатор Гонконг</span><span class="sxs-lookup"><span data-stu-id="37c0f-2042">hong kong id</span></span>
- <span data-ttu-id="37c0f-2043">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2043">香港身份證</span></span>
- <span data-ttu-id="37c0f-2044">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="37c0f-2045">身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2045">身份證</span></span>
- <span data-ttu-id="37c0f-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2046">身份証</span></span>
- <span data-ttu-id="37c0f-2047">身分證 </span><span class="sxs-lookup"><span data-stu-id="37c0f-2047">身分證</span></span>
- <span data-ttu-id="37c0f-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2048">身分証</span></span>
- <span data-ttu-id="37c0f-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2049">香港身份証</span></span>
- <span data-ttu-id="37c0f-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2050">香港身分證</span></span>
- <span data-ttu-id="37c0f-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2051">香港身分証</span></span>
- <span data-ttu-id="37c0f-2052">香港身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2052">香港身份證</span></span>
- <span data-ttu-id="37c0f-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2053">香港居民身份證</span></span>
- <span data-ttu-id="37c0f-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2054">香港居民身份証</span></span>
- <span data-ttu-id="37c0f-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2055">香港居民身分證</span></span>
- <span data-ttu-id="37c0f-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2056">香港居民身分証</span></span>
- <span data-ttu-id="37c0f-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="37c0f-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="37c0f-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="37c0f-2060">香港永久性居民身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="37c0f-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="37c0f-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="37c0f-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="37c0f-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="37c0f-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="37c0f-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="37c0f-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="37c0f-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="37c0f-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="37c0f-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="37c0f-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="37c0f-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="37c0f-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="37c0f-2073">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2074">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2074">Format</span></span>

<span data-ttu-id="37c0f-2075">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2076">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2076">Pattern</span></span>

<span data-ttu-id="37c0f-2077">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2077">10 letters or digits:</span></span>
- <span data-ttu-id="37c0f-2078">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2079">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2079">Four digits</span></span> 
- <span data-ttu-id="37c0f-2080">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2081">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2081">Checksum</span></span>

<span data-ttu-id="37c0f-2082">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2083">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2083">Definition</span></span>

<span data-ttu-id="37c0f-2084">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2085">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2086">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="37c0f-2087">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2088">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="37c0f-2089">Кэйворд_индиа_перманент_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="37c0f-2090">Permanent Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="37c0f-2091">PAN
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="37c0f-2092">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2093">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2093">Format</span></span>

<span data-ttu-id="37c0f-2094">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2095">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2095">Pattern</span></span>

<span data-ttu-id="37c0f-2096">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2096">12 digits:</span></span>
- <span data-ttu-id="37c0f-2097">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2097">Four digits</span></span> 
- <span data-ttu-id="37c0f-2098">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2098">An optional space or dash</span></span> 
- <span data-ttu-id="37c0f-2099">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2099">Four digits</span></span> 
- <span data-ttu-id="37c0f-2100">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2100">An optional space or dash</span></span> 
- <span data-ttu-id="37c0f-2101">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2102">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2102">Checksum</span></span>

<span data-ttu-id="37c0f-2103">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2104">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2104">Definition</span></span>

<span data-ttu-id="37c0f-p133">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону; Найдено ключевое слово из Кэйворд_индиа_аадхар. Контрольная сумма проходит проверку. Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону; Контрольная сумма проходит проверку. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="37c0f-p133">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. A keyword from Keyword_india_aadhar is found. The checksum passes. A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern. The checksum passes. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span></span>

### <a name="keywords"></a><span data-ttu-id="37c0f-2111">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="37c0f-2112">Кэйворд_индиа_аадхар</span><span class="sxs-lookup"><span data-stu-id="37c0f-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="37c0f-2113">Aadhar</span><span class="sxs-lookup"><span data-stu-id="37c0f-2113">Aadhar</span></span>
- <span data-ttu-id="37c0f-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="37c0f-2114">Aadhaar</span></span>
- <span data-ttu-id="37c0f-2115">UID</span><span class="sxs-lookup"><span data-stu-id="37c0f-2115">UID</span></span>
- <span data-ttu-id="37c0f-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="37c0f-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="37c0f-2117">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2118">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2118">Format</span></span>

<span data-ttu-id="37c0f-2119">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2120">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2120">Pattern</span></span>

<span data-ttu-id="37c0f-2121">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2121">16 digits:</span></span>
- <span data-ttu-id="37c0f-2122">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2122">Two-digit province code</span></span> 
- <span data-ttu-id="37c0f-2123">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2123">A period (optional)</span></span> 
- <span data-ttu-id="37c0f-2124">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="37c0f-2125">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="37c0f-2126">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2126">A period (optional)</span></span> 
- <span data-ttu-id="37c0f-2127">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-2128">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2128">A period (optional)</span></span> 
- <span data-ttu-id="37c0f-2129">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2130">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2130">Checksum</span></span>

<span data-ttu-id="37c0f-2131">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2132">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2132">Definition</span></span>

<span data-ttu-id="37c0f-2133">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2134">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2135">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="37c0f-2136">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2137">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2138">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="37c0f-2139">Кэйворд_индонесиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="37c0f-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="37c0f-2140">KTP</span></span>
- <span data-ttu-id="37c0f-2141">Kartu Tanda Penduduk
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="37c0f-2142">Nomor Induk Kependudukan
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="37c0f-2143">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2144">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2144">Format</span></span>

<span data-ttu-id="37c0f-2145">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2146">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2146">Pattern</span></span>

<span data-ttu-id="37c0f-2147">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="37c0f-2148">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="37c0f-2148">Two-letter country code</span></span>
- <span data-ttu-id="37c0f-2149">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="37c0f-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="37c0f-2150">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="37c0f-2151">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2151">1-3 letters or digits</span></span>

<span data-ttu-id="37c0f-p134">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="37c0f-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="37c0f-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="37c0f-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2155">Checksum</span></span>

<span data-ttu-id="37c0f-2156">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2157">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2157">Definition</span></span>

<span data-ttu-id="37c0f-2158">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2159">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2160">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2161">Keywords</span></span>

<span data-ttu-id="37c0f-2162">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="37c0f-2163">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="37c0f-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2164">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="37c0f-2165">IPv4:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2165">IPv4:</span></span>
<span data-ttu-id="37c0f-2166">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="37c0f-2167">Протокол IPv6</span><span class="sxs-lookup"><span data-stu-id="37c0f-2167">IPv6:</span></span>
<span data-ttu-id="37c0f-2168"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="37c0f-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2169">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2170">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2170">Checksum</span></span>

<span data-ttu-id="37c0f-2171">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2172">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2172">Definition</span></span>

<span data-ttu-id="37c0f-2173">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2174">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2175">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="37c0f-2176">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2177">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2178">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="37c0f-2179">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2180">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2181">Не обнаружено ключевых слов из списка Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2181">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2182">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="37c0f-2183">Кэйворд_ипаддресс</span><span class="sxs-lookup"><span data-stu-id="37c0f-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="37c0f-2184">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="37c0f-2185">ip address
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2185">ip address</span></span> 
- <span data-ttu-id="37c0f-2186">ip addresses</span><span class="sxs-lookup"><span data-stu-id="37c0f-2186">ip addresses</span></span>
- <span data-ttu-id="37c0f-2187">internet protocol</span><span class="sxs-lookup"><span data-stu-id="37c0f-2187">internet protocol</span></span>
- <span data-ttu-id="37c0f-2188">
IP-כתובת ה
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="37c0f-2189">Международная классификация Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2190">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2190">Format</span></span>

<span data-ttu-id="37c0f-2191">Словаря</span><span class="sxs-lookup"><span data-stu-id="37c0f-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2192">Pattern</span></span>

<span data-ttu-id="37c0f-2193">Недопустим</span><span class="sxs-lookup"><span data-stu-id="37c0f-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2194">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2194">Checksum</span></span>

<span data-ttu-id="37c0f-2195">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2196">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2196">Definition</span></span>

<span data-ttu-id="37c0f-2197">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2198">Найдено ключевое слово из Dictionary_icd_10_cm.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="37c0f-2199">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2199">Keywords</span></span>

<span data-ttu-id="37c0f-p135">Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятОй редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604). Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p135">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604). This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="37c0f-2202">Международная классификация Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2203">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2203">Format</span></span>

<span data-ttu-id="37c0f-2204">Словаря</span><span class="sxs-lookup"><span data-stu-id="37c0f-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2205">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2205">Pattern</span></span>

<span data-ttu-id="37c0f-2206">Недопустим</span><span class="sxs-lookup"><span data-stu-id="37c0f-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2207">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2207">Checksum</span></span>

<span data-ttu-id="37c0f-2208">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2209">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2209">Definition</span></span>

<span data-ttu-id="37c0f-2210">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2211">Найдено ключевое слово из Dictionary_icd_9_cm.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2212">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2212">Keywords</span></span>

<span data-ttu-id="37c0f-p136">Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятОй редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605). Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p136">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605). This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="37c0f-2215">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2216">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2216">Format</span></span>

<span data-ttu-id="37c0f-2217">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="37c0f-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="37c0f-2218">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="37c0f-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="37c0f-2219">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="37c0f-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="37c0f-2220">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2221">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2221">Pattern</span></span>

<span data-ttu-id="37c0f-2222">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="37c0f-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="37c0f-2223">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2223">Seven digits</span></span> 
- <span data-ttu-id="37c0f-2224">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="37c0f-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="37c0f-2225">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="37c0f-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="37c0f-2226">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2226">Seven digits</span></span> 
- <span data-ttu-id="37c0f-2227">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="37c0f-2228">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="37c0f-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2229">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2229">Checksum</span></span>

<span data-ttu-id="37c0f-2230">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2231">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2231">Definition</span></span>

<span data-ttu-id="37c0f-2232">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2233">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2234">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2234">One of the following is true:</span></span>
    - <span data-ttu-id="37c0f-2235">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="37c0f-2236">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="37c0f-2237">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2237">The checksum passes.</span></span>

<span data-ttu-id="37c0f-2238">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2239">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2240">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2240">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2241">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="37c0f-2242">Кэйворд_иреланд_ппс</span><span class="sxs-lookup"><span data-stu-id="37c0f-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="37c0f-2243">Personal Public Service Number 
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="37c0f-2244">PPS Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2244">PPS Number</span></span> 
- <span data-ttu-id="37c0f-2245">PPS Num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2245">PPS Num</span></span> 
- <span data-ttu-id="37c0f-2246">PPS No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2246">PPS No.</span></span> 
- <span data-ttu-id="37c0f-2247">PPS #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2247">PPS #</span></span> 
- <span data-ttu-id="37c0f-2248">PPS</span><span class="sxs-lookup"><span data-stu-id="37c0f-2248">PPS#</span></span> 
- <span data-ttu-id="37c0f-2249">PPSN
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2249">PPSN</span></span> 
- <span data-ttu-id="37c0f-2250">Public Services Card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2250">Public Services Card</span></span> 
- <span data-ttu-id="37c0f-2251">Uimhir Phearsanta Seirbhíse Poiblí
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="37c0f-p137">Uimh. PSP
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p137">Uimh. PSP</span></span> 
- <span data-ttu-id="37c0f-2254">PSP
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="37c0f-2255">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="37c0f-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2256">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2256">Format</span></span>

<span data-ttu-id="37c0f-2257">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2258">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2258">Pattern</span></span>

<span data-ttu-id="37c0f-2259">С форматированием</span><span class="sxs-lookup"><span data-stu-id="37c0f-2259">Formatted:</span></span>
- <span data-ttu-id="37c0f-2260">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2260">Two digits</span></span> 
- <span data-ttu-id="37c0f-2261">Тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-2261">A dash</span></span> 
- <span data-ttu-id="37c0f-2262">три цифры; </span><span class="sxs-lookup"><span data-stu-id="37c0f-2262">Three digits</span></span> 
- <span data-ttu-id="37c0f-2263">Тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-2263">A dash</span></span> 
- <span data-ttu-id="37c0f-2264">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2264">Eight digits</span></span>

<span data-ttu-id="37c0f-2265">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="37c0f-2265">Unformatted:</span></span>
- <span data-ttu-id="37c0f-2266">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2267">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2267">Checksum</span></span>

<span data-ttu-id="37c0f-2268">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2269">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2269">Definition</span></span>

<span data-ttu-id="37c0f-2270">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2271">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2272">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2273">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="37c0f-2274">Кэйворд_исраел_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="37c0f-2275">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2275">Bank Account Number</span></span> 
- <span data-ttu-id="37c0f-2276">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2276">Bank Account</span></span> 
- <span data-ttu-id="37c0f-2277">Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2277">Account Number</span></span> 
- <span data-ttu-id="37c0f-2278">מספר חשבון בנק
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="37c0f-2279">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="37c0f-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2280">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2280">Format</span></span>

<span data-ttu-id="37c0f-2281">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2282">Pattern</span></span>

<span data-ttu-id="37c0f-2283">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2284">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2284">Checksum</span></span>

<span data-ttu-id="37c0f-2285">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2286">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2286">Definition</span></span>

<span data-ttu-id="37c0f-2287">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2288">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2289">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="37c0f-2290">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2290">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2291">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="37c0f-2292">Кэйворд_исраел_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="37c0f-2293">מספר זהות
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2293">מספר זהות</span></span> 
- <span data-ttu-id="37c0f-2294">National ID Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="37c0f-2295">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2296">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2296">Format</span></span>

<span data-ttu-id="37c0f-2297">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2298">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2298">Pattern</span></span>

- <span data-ttu-id="37c0f-2299">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="37c0f-2300">одна буква (без учета регистра); </span><span class="sxs-lookup"><span data-stu-id="37c0f-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2301">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2302">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="37c0f-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="37c0f-2303">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2304">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2304">Checksum</span></span>

<span data-ttu-id="37c0f-2305">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2306">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2306">Definition</span></span>

<span data-ttu-id="37c0f-2307">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2308">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2309">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2310">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="37c0f-2311">Кэйворд_итали_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="37c0f-2312">numero di patente di guida
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="37c0f-2313">patente di guida
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="37c0f-2314">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2315">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2315">Format</span></span>

<span data-ttu-id="37c0f-2316">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2317">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2317">Pattern</span></span>

<span data-ttu-id="37c0f-2318">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2318">Bank account number:</span></span>
- <span data-ttu-id="37c0f-2319">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2319">Seven or eight digits</span></span>
- <span data-ttu-id="37c0f-2320">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2320">Bank account branch code:</span></span>
- <span data-ttu-id="37c0f-2321">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2321">Four digits</span></span> 
- <span data-ttu-id="37c0f-2322">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="37c0f-2323">три цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2323">Three digits</span></span>

<span data-ttu-id="37c0f-2324">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2324">Checksum</span></span>

<span data-ttu-id="37c0f-2325">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2326">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2326">Definition</span></span>

<span data-ttu-id="37c0f-2327">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2328">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2329">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="37c0f-2330">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2330">One of the following is true:</span></span>
- <span data-ttu-id="37c0f-2331">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2332">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="37c0f-2333">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2334">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2335">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2336">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="37c0f-2337">Кэйворд_жп_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="37c0f-2338">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2338">Checking Account Number</span></span> 
- <span data-ttu-id="37c0f-2339">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2339">Checking Account</span></span> 
- <span data-ttu-id="37c0f-2340">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2340">Checking Account #</span></span> 
- <span data-ttu-id="37c0f-2341">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="37c0f-2342">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2342">Checking Acct #</span></span> 
- <span data-ttu-id="37c0f-2343">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="37c0f-2344">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2344">Checking Account No.</span></span> 
- <span data-ttu-id="37c0f-2345">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2345">Bank Account Number</span></span> 
- <span data-ttu-id="37c0f-2346">Bank Account
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2346">Bank Account</span></span> 
- <span data-ttu-id="37c0f-2347">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2347">Bank Account #</span></span> 
- <span data-ttu-id="37c0f-2348">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="37c0f-2349">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2349">Bank Acct #</span></span> 
- <span data-ttu-id="37c0f-2350">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="37c0f-2351">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2351">Bank Account No.</span></span> 
- <span data-ttu-id="37c0f-2352">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2352">Savings Account Number</span></span> 
- <span data-ttu-id="37c0f-2353">Учетная запись сбережений</span><span class="sxs-lookup"><span data-stu-id="37c0f-2353">Savings Account</span></span> 
- <span data-ttu-id="37c0f-2354">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2354">Savings Account #</span></span> 
- <span data-ttu-id="37c0f-2355">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="37c0f-2356">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2356">Savings Acct #</span></span> 
- <span data-ttu-id="37c0f-2357">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="37c0f-2358">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2358">Savings Account No.</span></span> 
- <span data-ttu-id="37c0f-2359">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2359">Debit Account Number</span></span> 
- <span data-ttu-id="37c0f-2360">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2360">Debit Account</span></span> 
- <span data-ttu-id="37c0f-2361">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2361">Debit Account #</span></span> 
- <span data-ttu-id="37c0f-2362">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="37c0f-2363">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2363">Debit Acct #</span></span> 
- <span data-ttu-id="37c0f-2364">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="37c0f-2365">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2365">Debit Account No.</span></span> 
- <span data-ttu-id="37c0f-2366">口座番号を当座預金口座の確認
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="37c0f-2367">＃アカウントの確認、勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="37c0f-2368">＃勘定の確認
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="37c0f-2369">勘定番号の確認
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="37c0f-2370">口座番号の確認
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2370">口座番号の確認</span></span> 
- <span data-ttu-id="37c0f-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="37c0f-2371">銀行口座番号</span></span> 
- <span data-ttu-id="37c0f-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="37c0f-2372">銀行口座</span></span> 
- <span data-ttu-id="37c0f-2373">銀行口座＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2373">銀行口座＃</span></span> 
- <span data-ttu-id="37c0f-2374">銀行の勘定番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="37c0f-2375">銀行のacct＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="37c0f-2376">銀行の勘定いいえ
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="37c0f-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="37c0f-2377">銀行口座番号</span></span>
- <span data-ttu-id="37c0f-2378">
普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="37c0f-2379">預金口座
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2379">預金口座</span></span> 
- <span data-ttu-id="37c0f-2380">貯蓄口座＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="37c0f-2381">貯蓄勘定の数
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="37c0f-2382">貯蓄勘定＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="37c0f-2383">貯蓄勘定番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="37c0f-2384">普通預金口座番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="37c0f-2385">引き落とし口座番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="37c0f-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="37c0f-2386">口座番号</span></span> 
- <span data-ttu-id="37c0f-2387">口座番号＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2387">口座番号＃</span></span> 
- <span data-ttu-id="37c0f-2388">デビットのacct番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="37c0f-2389">デビット勘定＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="37c0f-2390">デビットACCTの番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="37c0f-2391">デビット口座番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="37c0f-2392">Кэйворд_жп_банк_бранч_коде</span><span class="sxs-lookup"><span data-stu-id="37c0f-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="37c0f-2393">Otemachi</span><span class="sxs-lookup"><span data-stu-id="37c0f-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="37c0f-2394">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2395">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2395">Format</span></span>

<span data-ttu-id="37c0f-2396">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2397">Pattern</span></span>

<span data-ttu-id="37c0f-2398">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2399">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2399">Checksum</span></span>

<span data-ttu-id="37c0f-2400">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2401">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2401">Definition</span></span>

<span data-ttu-id="37c0f-2402">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2403">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2404">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2405">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="37c0f-2406">Кэйворд_жп_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="37c0f-2407">dl#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2407">dl#</span></span> 
- <span data-ttu-id="37c0f-2408">DL</span><span class="sxs-lookup"><span data-stu-id="37c0f-2408">DL＃</span></span> 
- <span data-ttu-id="37c0f-2409">dls#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2409">dls#</span></span> 
- <span data-ttu-id="37c0f-2410">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="37c0f-2410">DLS＃</span></span> 
- <span data-ttu-id="37c0f-2411">driver license</span><span class="sxs-lookup"><span data-stu-id="37c0f-2411">driver license</span></span> 
- <span data-ttu-id="37c0f-2412">driver licenses</span><span class="sxs-lookup"><span data-stu-id="37c0f-2412">driver licenses</span></span> 
- <span data-ttu-id="37c0f-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="37c0f-2413">drivers license</span></span> 
- <span data-ttu-id="37c0f-2414">driver's license</span><span class="sxs-lookup"><span data-stu-id="37c0f-2414">driver's license</span></span> 
- <span data-ttu-id="37c0f-2415">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="37c0f-2415">drivers licenses</span></span> 
- <span data-ttu-id="37c0f-2416">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="37c0f-2416">driver's licenses</span></span> 
- <span data-ttu-id="37c0f-2417">driving licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2417">driving licence</span></span> 
- <span data-ttu-id="37c0f-2418">lic#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2418">lic#</span></span> 
- <span data-ttu-id="37c0f-2419">Лик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-2419">LIC＃</span></span> 
- <span data-ttu-id="37c0f-2420">lics#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2420">lics#</span></span> 
- <span data-ttu-id="37c0f-2421">идентификатор состояния</span><span class="sxs-lookup"><span data-stu-id="37c0f-2421">state id</span></span> 
- <span data-ttu-id="37c0f-2422">state identification
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2422">state identification</span></span> 
- <span data-ttu-id="37c0f-2423">state identification number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2423">state identification number</span></span> 
- <span data-ttu-id="37c0f-2424">低所得国＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2424">低所得国＃</span></span> 
- <span data-ttu-id="37c0f-2425">免許証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2425">免許証</span></span> 
- <span data-ttu-id="37c0f-2426">状態ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-2426">状態ID</span></span>
- <span data-ttu-id="37c0f-2427">
状態の識別
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2427">状態の識別</span></span> 
- <span data-ttu-id="37c0f-2428">状態の識別番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2428">状態の識別番号</span></span> 
- <span data-ttu-id="37c0f-2429">運転免許</span><span class="sxs-lookup"><span data-stu-id="37c0f-2429">運転免許</span></span> 
- <span data-ttu-id="37c0f-2430">運転免許証</span><span class="sxs-lookup"><span data-stu-id="37c0f-2430">運転免許証</span></span> 
- <span data-ttu-id="37c0f-2431">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="37c0f-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="37c0f-2432">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2433">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2433">Format</span></span>

<span data-ttu-id="37c0f-2434">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2435">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2435">Pattern</span></span>

<span data-ttu-id="37c0f-2436">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2437">Checksum</span></span>

<span data-ttu-id="37c0f-2438">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2439">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2439">Definition</span></span>

<span data-ttu-id="37c0f-2440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2441">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2442">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="37c0f-2444">Кэйворд_жп_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="37c0f-2445">パスポート
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2445">パスポート</span></span> 
- <span data-ttu-id="37c0f-2446">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2446">パスポート番号</span></span> 
- <span data-ttu-id="37c0f-2447">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2447">パスポートのNum</span></span> 
- <span data-ttu-id="37c0f-2448">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="37c0f-2449">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2450">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2450">Format</span></span>

<span data-ttu-id="37c0f-2451">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="37c0f-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2452">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2452">Pattern</span></span>

<span data-ttu-id="37c0f-2453">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2454">Checksum</span></span>

<span data-ttu-id="37c0f-2455">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2456">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2456">Definition</span></span>

<span data-ttu-id="37c0f-2457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2458">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2459">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="37c0f-2461">Кэйворд_жп_ресидент_регистратион_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="37c0f-2462">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-2462">Resident Registration Number</span></span>
- <span data-ttu-id="37c0f-2463">Resident Register Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2463">Resident Register Number</span></span> 
- <span data-ttu-id="37c0f-2464">Residents Basic Registry Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="37c0f-2465">Resident Registration No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="37c0f-2466">Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2466">Resident Register No.</span></span> 
- <span data-ttu-id="37c0f-2467">Residents Basic Registry No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="37c0f-2468">Basic Resident Register No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="37c0f-2469">住民登録番号、登録番号をレジデント
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="37c0f-2470">住民基本登録番号、登録番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="37c0f-2471">住民基本レジストリ番号を常駐
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="37c0f-2472">登録番号を常駐住民基本台帳登録番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="37c0f-2473">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2474">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2474">Format</span></span>

<span data-ttu-id="37c0f-2475">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2476">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2476">Pattern</span></span>

<span data-ttu-id="37c0f-2477">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2477">7-12 digits:</span></span>
- <span data-ttu-id="37c0f-2478">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2478">Four digits</span></span> 
- <span data-ttu-id="37c0f-2479">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="37c0f-2480">Шесть цифр или</span><span class="sxs-lookup"><span data-stu-id="37c0f-2480">Six digits OR</span></span>
- <span data-ttu-id="37c0f-2481">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2482">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2482">Checksum</span></span>

<span data-ttu-id="37c0f-2483">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2484">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2484">Definition</span></span>

<span data-ttu-id="37c0f-2485">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2486">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2487">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="37c0f-2488">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2489">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2490">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2490">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2491">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="37c0f-2492">Кэйворд_жп_син</span><span class="sxs-lookup"><span data-stu-id="37c0f-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="37c0f-2493">Social Insurance No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="37c0f-2494">Social Insurance Num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="37c0f-2495">Social Insurance Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="37c0f-2496">社会保険のテンキー
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="37c0f-2497">社会保険番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="37c0f-2498">Номер карточки для японского языка</span><span class="sxs-lookup"><span data-stu-id="37c0f-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2499">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2499">Format</span></span>

<span data-ttu-id="37c0f-2500">12 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2501">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2501">Pattern</span></span>

<span data-ttu-id="37c0f-2502">12 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2502">12 letters and digits:</span></span>
- <span data-ttu-id="37c0f-2503">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="37c0f-2504">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2504">Eight digits</span></span> 
- <span data-ttu-id="37c0f-2505">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2506">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2506">Checksum</span></span>

<span data-ttu-id="37c0f-2507">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2508">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2508">Definition</span></span>

<span data-ttu-id="37c0f-2509">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2510">Регулярное выражение Режекс_жп_ресиденце_кард_нумбер находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2511">Найдено ключевое слово из Кэйворд_жп_ресиденце_кард_нумбер.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2512">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="37c0f-2513">Кэйворд_жп_ресиденце_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="37c0f-2514">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="37c0f-2514">Residence card number</span></span>
- <span data-ttu-id="37c0f-2515">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="37c0f-2515">Residence card no</span></span>
- <span data-ttu-id="37c0f-2516">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="37c0f-2516">Residence card #</span></span>
- <span data-ttu-id="37c0f-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="37c0f-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="37c0f-2518">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2519">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2519">Format</span></span>

<span data-ttu-id="37c0f-2520">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2521">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2521">Pattern</span></span>

<span data-ttu-id="37c0f-2522">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2522">12 digits:</span></span>
- <span data-ttu-id="37c0f-2523">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-2524">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2524">A dash (optional)</span></span> 
- <span data-ttu-id="37c0f-2525">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="37c0f-2526">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2526">A dash (optional)</span></span> 
- <span data-ttu-id="37c0f-2527">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2527">Three random digits</span></span> 
- <span data-ttu-id="37c0f-2528">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2529">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2529">Checksum</span></span>

<span data-ttu-id="37c0f-2530">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2531">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2531">Definition</span></span>

<span data-ttu-id="37c0f-2532">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2533">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2534">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2535">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="37c0f-2536">Кэйворд_малайсиа_ид_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="37c0f-2537">карточка цифрового приложения</span><span class="sxs-lookup"><span data-stu-id="37c0f-2537">digital application card</span></span>
- <span data-ttu-id="37c0f-2538">i/c</span><span class="sxs-lookup"><span data-stu-id="37c0f-2538">i/c</span></span>
- <span data-ttu-id="37c0f-2539">i/c нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2539">i/c no</span></span>
- <span data-ttu-id="37c0f-2540">внутренних</span><span class="sxs-lookup"><span data-stu-id="37c0f-2540">ic</span></span>
- <span data-ttu-id="37c0f-2541">МФ нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2541">ic no</span></span>
- <span data-ttu-id="37c0f-2542">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-2542">id card</span></span>
- <span data-ttu-id="37c0f-2543">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-2543">identification Card</span></span>
- <span data-ttu-id="37c0f-2544">identity card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2544">identity card</span></span>
- <span data-ttu-id="37c0f-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="37c0f-2545">k/p</span></span>
- <span data-ttu-id="37c0f-2546">k/p</span><span class="sxs-lookup"><span data-stu-id="37c0f-2546">k/p no</span></span>
- <span data-ttu-id="37c0f-2547">кад акуан Дири</span><span class="sxs-lookup"><span data-stu-id="37c0f-2547">kad akuan diri</span></span>
- <span data-ttu-id="37c0f-2548">кад апликаси Digital</span><span class="sxs-lookup"><span data-stu-id="37c0f-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="37c0f-2549">кад пенженалан Малайзии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="37c0f-2550">ключев</span><span class="sxs-lookup"><span data-stu-id="37c0f-2550">kp</span></span>
- <span data-ttu-id="37c0f-2551">ключевой номер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2551">kp no</span></span>
- <span data-ttu-id="37c0f-2552">микад</span><span class="sxs-lookup"><span data-stu-id="37c0f-2552">mykad</span></span>
- <span data-ttu-id="37c0f-2553">Микас</span><span class="sxs-lookup"><span data-stu-id="37c0f-2553">mykas</span></span>
- <span data-ttu-id="37c0f-2554">микид</span><span class="sxs-lookup"><span data-stu-id="37c0f-2554">mykid</span></span>
- <span data-ttu-id="37c0f-2555">МИПР</span><span class="sxs-lookup"><span data-stu-id="37c0f-2555">mypr</span></span>
- <span data-ttu-id="37c0f-2556">митентера</span><span class="sxs-lookup"><span data-stu-id="37c0f-2556">mytentera</span></span>
- <span data-ttu-id="37c0f-2557">идентификационная карточка Малайзии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2557">malaysia identity card</span></span>
- <span data-ttu-id="37c0f-2558">идентификационная карточка малайсиан</span><span class="sxs-lookup"><span data-stu-id="37c0f-2558">malaysian identity card</span></span>
- <span data-ttu-id="37c0f-2559">NRIC</span><span class="sxs-lookup"><span data-stu-id="37c0f-2559">nric</span></span>
- <span data-ttu-id="37c0f-2560">Личная идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="37c0f-2561">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2562">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2562">Format</span></span>

<span data-ttu-id="37c0f-2563">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2564">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2564">Pattern</span></span>

<span data-ttu-id="37c0f-2565">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2565">8-9 digits:</span></span>
- <span data-ttu-id="37c0f-2566">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2566">Three digits</span></span> 
- <span data-ttu-id="37c0f-2567">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="37c0f-2567">A space (optional)</span></span> 
- <span data-ttu-id="37c0f-2568">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2568">Three digits</span></span> 
- <span data-ttu-id="37c0f-2569">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="37c0f-2569">A space (optional)</span></span> 
- <span data-ttu-id="37c0f-2570">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2571">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2571">Checksum</span></span>

<span data-ttu-id="37c0f-2572">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2573">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2573">Definition</span></span>

<span data-ttu-id="37c0f-2574">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2575">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2576">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="37c0f-2577">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="37c0f-2578">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2578">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2579">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="37c0f-2580">Кэйворд_несерландс_бсн</span><span class="sxs-lookup"><span data-stu-id="37c0f-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="37c0f-2581">Citizen service number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2581">Citizen service number</span></span> 
- <span data-ttu-id="37c0f-2582">BSN

</span><span class="sxs-lookup"><span data-stu-id="37c0f-2582">BSN</span></span> 
- <span data-ttu-id="37c0f-2583">Burgerservicenummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="37c0f-2584">Sofinummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2584">Sofinummer</span></span> 
- <span data-ttu-id="37c0f-2585">Persoonsgebonden nummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="37c0f-2586">Persoonsnummer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="37c0f-2587">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2588">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2588">Format</span></span>

<span data-ttu-id="37c0f-2589">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2590">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2590">Pattern</span></span>

<span data-ttu-id="37c0f-2591">Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2592">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2592">Checksum</span></span>

<span data-ttu-id="37c0f-2593">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2594">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2594">Definition</span></span>

<span data-ttu-id="37c0f-2595">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2596">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2597">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="37c0f-2598">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2598">The checksum passes.</span></span>

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

<span data-ttu-id="37c0f-2599">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2599">Keywords</span></span>

<span data-ttu-id="37c0f-2600">Кэйворд_нз_термс</span><span class="sxs-lookup"><span data-stu-id="37c0f-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="37c0f-2601">NHI
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2601">NHI</span></span> 
- <span data-ttu-id="37c0f-2602">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="37c0f-2602">New Zealand</span></span> 
- <span data-ttu-id="37c0f-2603">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="37c0f-2603">Health</span></span> 
- <span data-ttu-id="37c0f-2604">treatment
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="37c0f-2605">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2606">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2606">Format</span></span>

<span data-ttu-id="37c0f-2607">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="37c0f-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2608">Pattern</span></span>

<span data-ttu-id="37c0f-2609">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2609">11 digits:</span></span>
- <span data-ttu-id="37c0f-2610">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-2611">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="37c0f-2612">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2613">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2613">Checksum</span></span>

<span data-ttu-id="37c0f-2614">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2615">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2615">Definition</span></span>

<span data-ttu-id="37c0f-2616">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2617">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2618">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="37c0f-2619">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2619">The checksum passes.</span></span>
- <span data-ttu-id="37c0f-2620">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2621">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2622">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2622">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2623">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="37c0f-2624">Кэйворд_норвай_ид_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="37c0f-2625">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="37c0f-2625">Personal identification number</span></span>
- <span data-ttu-id="37c0f-2626">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="37c0f-2627">ID Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-2627">ID Number</span></span>
- <span data-ttu-id="37c0f-2628">Identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-2628">Identification</span></span>
- <span data-ttu-id="37c0f-2629">Personnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-2629">Personnummer</span></span>
- <span data-ttu-id="37c0f-2630">Fødselsnummer</span><span class="sxs-lookup"><span data-stu-id="37c0f-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="37c0f-2631">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="37c0f-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2632">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2632">Format</span></span>

<span data-ttu-id="37c0f-2633">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2634">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2634">Pattern</span></span>

<span data-ttu-id="37c0f-2635">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2635">12 digits:</span></span>
- <span data-ttu-id="37c0f-2636">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2636">Four digits</span></span> 
- <span data-ttu-id="37c0f-2637">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2637">A hyphen</span></span> 
- <span data-ttu-id="37c0f-2638">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2638">Seven digits</span></span> 
- <span data-ttu-id="37c0f-2639">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2639">A hyphen</span></span> 
- <span data-ttu-id="37c0f-2640">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="37c0f-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2641">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2641">Checksum</span></span>

<span data-ttu-id="37c0f-2642">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2643">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2643">Definition</span></span>

<span data-ttu-id="37c0f-2644">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2645">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2646">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2647">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="37c0f-2648">Кэйворд_филиппинес_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="37c0f-2649">Unified Multi-Purpose ID
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="37c0f-2650">UMID
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2650">UMID</span></span> 
- <span data-ttu-id="37c0f-2651">Identity Card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2651">Identity Card</span></span> 
- <span data-ttu-id="37c0f-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="37c0f-2653">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="37c0f-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2654">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2654">Format</span></span>

<span data-ttu-id="37c0f-2655">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2656">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2656">Pattern</span></span>

<span data-ttu-id="37c0f-2657">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2658">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2658">Checksum</span></span>

<span data-ttu-id="37c0f-2659">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2660">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2660">Definition</span></span>

<span data-ttu-id="37c0f-p138">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_полиш_натионал_ид находит содержимое, которое соответствует шаблону; Найдено ключевое слово из Кэйворд_полиш_натионал_ид_пасспорт_нумбер. Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-p138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern. A keyword from Keyword_polish_national_id_passport_number is found. The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2664">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="37c0f-2665">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="37c0f-2666">Довóд особисти</span><span class="sxs-lookup"><span data-stu-id="37c0f-2666">Dowód osobisty</span></span>
- <span data-ttu-id="37c0f-2667">Нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="37c0f-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="37c0f-2668">Назва i нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="37c0f-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="37c0f-2669">Назва i НР доводу особистего</span><span class="sxs-lookup"><span data-stu-id="37c0f-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="37c0f-2670">Nazwa i nr dowodu tożsamości
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="37c0f-2671">Dowód Tożsamości
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="37c0f-p139">dow. os.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-p139">dow. os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="37c0f-2674">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="37c0f-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2675">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2675">Format</span></span>

<span data-ttu-id="37c0f-2676">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="37c0f-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2677">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2677">Pattern</span></span>

<span data-ttu-id="37c0f-2678">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2679">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2679">Checksum</span></span>

<span data-ttu-id="37c0f-2680">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2681">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2681">Definition</span></span>

<span data-ttu-id="37c0f-2682">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2683">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2684">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="37c0f-2685">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2686">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="37c0f-2687">Кэйворд_песел_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="37c0f-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="37c0f-2688">Nr PESEL</span></span>
- <span data-ttu-id="37c0f-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="37c0f-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="37c0f-2690">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="37c0f-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2691">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2691">Format</span></span>

<span data-ttu-id="37c0f-2692">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2693">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2693">Pattern</span></span>

<span data-ttu-id="37c0f-2694">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2695">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2695">Checksum</span></span>

<span data-ttu-id="37c0f-2696">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2697">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2697">Definition</span></span>

<span data-ttu-id="37c0f-2698">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2699">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2700">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="37c0f-2701">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2701">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2702">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="37c0f-2703">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="37c0f-2704">Нумер пасзпорту</span><span class="sxs-lookup"><span data-stu-id="37c0f-2704">Numer paszportu</span></span>
- <span data-ttu-id="37c0f-p140">НР. Пасзпорту</span><span class="sxs-lookup"><span data-stu-id="37c0f-p140">Nr. Paszportu</span></span>
- <span data-ttu-id="37c0f-2707">Пасзпорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="37c0f-2708">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2709">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2709">Format</span></span>

<span data-ttu-id="37c0f-2710">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2711">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2711">Pattern</span></span>

<span data-ttu-id="37c0f-2712">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2713">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2713">Checksum</span></span>

<span data-ttu-id="37c0f-2714">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2715">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2715">Definition</span></span>

<span data-ttu-id="37c0f-2716">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2717">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2718">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2719">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="37c0f-2720">Кэйворд_португал_Цитизен_кард</span><span class="sxs-lookup"><span data-stu-id="37c0f-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="37c0f-2721">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2721">Citizen Card</span></span>
- <span data-ttu-id="37c0f-2722">National ID Card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2722">National ID Card</span></span>
- <span data-ttu-id="37c0f-2723">CC</span><span class="sxs-lookup"><span data-stu-id="37c0f-2723">CC</span></span>
- <span data-ttu-id="37c0f-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="37c0f-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="37c0f-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="37c0f-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="37c0f-2726">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="37c0f-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2727">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2727">Format</span></span>

<span data-ttu-id="37c0f-2728">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2729">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2729">Pattern</span></span>

<span data-ttu-id="37c0f-2730">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2731">Checksum</span></span>

<span data-ttu-id="37c0f-2732">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2733">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2733">Definition</span></span>

<span data-ttu-id="37c0f-2734">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2735">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2736">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2737">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="37c0f-2738">Кэйворд_сауди_арабиа_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="37c0f-2739">Identification Card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2739">Identification Card</span></span> 
- <span data-ttu-id="37c0f-2740">I card number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2740">I card number</span></span> 
- <span data-ttu-id="37c0f-2741">идентификатор</span><span class="sxs-lookup"><span data-stu-id="37c0f-2741">ID number</span></span> 
- <span data-ttu-id="37c0f-2742">الوطنية الهوية بطاقة رقم
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="37c0f-2743">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2744">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2744">Format</span></span>

<span data-ttu-id="37c0f-2745">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2746">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2746">Pattern</span></span>

- <span data-ttu-id="37c0f-2747">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="37c0f-2748">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2749">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2749">Seven digits</span></span> 
- <span data-ttu-id="37c0f-2750">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2751">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2751">Checksum</span></span>

<span data-ttu-id="37c0f-2752">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2753">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2753">Definition</span></span>

<span data-ttu-id="37c0f-2754">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2755">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2756">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="37c0f-2757">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2757">The checksum passes.</span></span>

<span data-ttu-id="37c0f-2758">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2759">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2760">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2760">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2761">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="37c0f-2762">Кэйворд_сингапоре_нрик</span><span class="sxs-lookup"><span data-stu-id="37c0f-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="37c0f-2763">National Registration Identity Card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="37c0f-2764">Identity Card Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2764">Identity Card Number</span></span> 
- <span data-ttu-id="37c0f-2765">NRIC
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2765">NRIC</span></span> 
- <span data-ttu-id="37c0f-2766">IC
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2766">IC</span></span> 
- <span data-ttu-id="37c0f-2767">Foreign Identification Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="37c0f-2768">FIN
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2768">FIN</span></span> 
- <span data-ttu-id="37c0f-2769">身份证 </span><span class="sxs-lookup"><span data-stu-id="37c0f-2769">身份证</span></span> 
- <span data-ttu-id="37c0f-2770">身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="37c0f-2771">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="37c0f-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2772">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2772">Format</span></span>

<span data-ttu-id="37c0f-2773">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2774">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2774">Pattern</span></span>

<span data-ttu-id="37c0f-2775">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2775">13 digits:</span></span>
- <span data-ttu-id="37c0f-2776">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-2777">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2777">Four digits</span></span> 
- <span data-ttu-id="37c0f-2778">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="37c0f-2779">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="37c0f-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="37c0f-2780">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="37c0f-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2781">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2781">Checksum</span></span>

<span data-ttu-id="37c0f-2782">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2783">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2783">Definition</span></span>

<span data-ttu-id="37c0f-2784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2785">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2786">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="37c0f-2787">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2788">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="37c0f-2789">Кэйворд_саус_африка_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="37c0f-2790">Identity card</span><span class="sxs-lookup"><span data-stu-id="37c0f-2790">Identity card</span></span>
- <span data-ttu-id="37c0f-2791">ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-2791">ID</span></span>
- <span data-ttu-id="37c0f-2792">Identification</span><span class="sxs-lookup"><span data-stu-id="37c0f-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="37c0f-2793">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="37c0f-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2794">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2794">Format</span></span>

<span data-ttu-id="37c0f-2795">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2796">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2796">Pattern</span></span>

<span data-ttu-id="37c0f-2797">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2797">13 digits:</span></span>
- <span data-ttu-id="37c0f-2798">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="37c0f-2799">дефис;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2799">A hyphen</span></span> 
- <span data-ttu-id="37c0f-2800">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="37c0f-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="37c0f-2801">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="37c0f-2802">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="37c0f-2803">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2804">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2804">Checksum</span></span>

<span data-ttu-id="37c0f-2805">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2806">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2806">Definition</span></span>

<span data-ttu-id="37c0f-2807">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2808">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2809">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="37c0f-2810">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2810">The checksum passes.</span></span>

<span data-ttu-id="37c0f-2811">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2812">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2813">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2813">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2814">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="37c0f-2815">Кэйворд_саус_кореа_ресидент_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="37c0f-2816">National ID card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2816">National ID card</span></span> 
- <span data-ttu-id="37c0f-2817">Citizen's Registration Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="37c0f-2818">Jumin deungnok beonho
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="37c0f-2819">RRN
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2819">RRN</span></span> 
- <span data-ttu-id="37c0f-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="37c0f-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="37c0f-2821">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2822">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2822">Format</span></span>

<span data-ttu-id="37c0f-2823">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2824">Pattern</span></span>

<span data-ttu-id="37c0f-2825">11-12 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2825">11-12 digits:</span></span>
- <span data-ttu-id="37c0f-2826">две цифры; </span><span class="sxs-lookup"><span data-stu-id="37c0f-2826">Two digits</span></span> 
- <span data-ttu-id="37c0f-2827">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="37c0f-2828">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2828">7-8 digits</span></span> 
- <span data-ttu-id="37c0f-2829">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="37c0f-2830">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2831">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2831">Checksum</span></span>

<span data-ttu-id="37c0f-2832">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2833">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2833">Definition</span></span>

<span data-ttu-id="37c0f-2834">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2835">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2836">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2837">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2837">Keywords</span></span>

<span data-ttu-id="37c0f-2838">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="37c0f-2839">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="37c0f-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2840">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2840">Format</span></span>

<span data-ttu-id="37c0f-2841">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2842">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2842">Pattern</span></span>

<span data-ttu-id="37c0f-2843">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="37c0f-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="37c0f-2844">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="37c0f-2845">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="37c0f-2846">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="37c0f-2847">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2848">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2848">Checksum</span></span>

<span data-ttu-id="37c0f-2849">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2850">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2850">Definition</span></span>

<span data-ttu-id="37c0f-2851">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2852">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2853">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2854">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2854">Keywords</span></span>

<span data-ttu-id="37c0f-2855">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="37c0f-2856">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="37c0f-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2857">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2857">Format</span></span>

<span data-ttu-id="37c0f-2858">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2859">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2859">Pattern</span></span>

<span data-ttu-id="37c0f-2860">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2861">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2861">Checksum</span></span>

<span data-ttu-id="37c0f-2862">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2863">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2863">Definition</span></span>

<span data-ttu-id="37c0f-2864">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2865">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2866">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2866">One of the following is true:</span></span>
    - <span data-ttu-id="37c0f-2867">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="37c0f-2868">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2868">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-2869">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="37c0f-2870">Кэйворд_сведен_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="37c0f-2871">visa requirements
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2871">visa requirements</span></span> 
- <span data-ttu-id="37c0f-2872">Alien Registration Card
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="37c0f-2873">Schengen visas
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2873">Schengen visas</span></span> 
- <span data-ttu-id="37c0f-2874">Schengen visa
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2874">Schengen visa</span></span> 
- <span data-ttu-id="37c0f-2875">Visa Processing
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2875">Visa Processing</span></span> 
- <span data-ttu-id="37c0f-2876">Visa Type
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2876">Visa Type</span></span> 
- <span data-ttu-id="37c0f-2877">Single Entry
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2877">Single Entry</span></span> 
- <span data-ttu-id="37c0f-2878">Multiple Entry
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2878">Multiple Entry</span></span> 
- <span data-ttu-id="37c0f-2879">G3 Processing Fees

</span><span class="sxs-lookup"><span data-stu-id="37c0f-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="37c0f-2880">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2880">Keyword_passport</span></span>

- <span data-ttu-id="37c0f-2881">Passport Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-2881">Passport Number</span></span> 
- <span data-ttu-id="37c0f-2882">
Passport No</span><span class="sxs-lookup"><span data-stu-id="37c0f-2882">Passport No</span></span> 
- <span data-ttu-id="37c0f-2883">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2883">Passport #</span></span> 
- <span data-ttu-id="37c0f-2884">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2884">Passport#</span></span> 
- <span data-ttu-id="37c0f-2885">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="37c0f-2885">PassportID</span></span> 
- <span data-ttu-id="37c0f-2886">Passportno
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2886">Passportno</span></span> 
- <span data-ttu-id="37c0f-2887">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2887">passportnumber</span></span> 
- <span data-ttu-id="37c0f-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="37c0f-2888">パスポート</span></span> 
- <span data-ttu-id="37c0f-2889">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2889">パスポート番号</span></span> 
- <span data-ttu-id="37c0f-2890">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2890">パスポートのNum</span></span> 
- <span data-ttu-id="37c0f-2891">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2891">パスポート＃</span></span> 
- <span data-ttu-id="37c0f-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="37c0f-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="37c0f-2893">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="37c0f-2893">Passeport n °</span></span> 
- <span data-ttu-id="37c0f-2894">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2894">Passeport Non</span></span> 
- <span data-ttu-id="37c0f-2895">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2895">Passeport #</span></span> 
- <span data-ttu-id="37c0f-2896">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2896">Passeport#</span></span> 
- <span data-ttu-id="37c0f-2897">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2897">PasseportNon</span></span> 
- <span data-ttu-id="37c0f-2898">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="37c0f-2899">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="37c0f-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2900">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2900">Format</span></span>

<span data-ttu-id="37c0f-2901">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2902">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2902">Pattern</span></span>

<span data-ttu-id="37c0f-2903">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="37c0f-2904">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2905">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="37c0f-2905">An optional space</span></span> 
- <span data-ttu-id="37c0f-2906">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="37c0f-2907">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="37c0f-2907">An optional space</span></span> 
- <span data-ttu-id="37c0f-2908">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2909">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2909">Checksum</span></span>

<span data-ttu-id="37c0f-2910">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2911">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2911">Definition</span></span>

<span data-ttu-id="37c0f-2912">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2913">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2914">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2915">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="37c0f-2916">Кэйворд_свифт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2916">Keyword_swift</span></span>

- <span data-ttu-id="37c0f-2917">international organization for standardization 9362
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="37c0f-2918">iso 9362
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2918">iso 9362</span></span> 
- <span data-ttu-id="37c0f-2919">iso9362</span><span class="sxs-lookup"><span data-stu-id="37c0f-2919">iso9362</span></span> 
- <span data-ttu-id="37c0f-2920">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2920">swift\#</span></span> 
- <span data-ttu-id="37c0f-2921">swiftcode
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2921">swiftcode</span></span> 
- <span data-ttu-id="37c0f-2922">swiftnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2922">swiftnumber</span></span> 
- <span data-ttu-id="37c0f-2923">swiftroutingnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="37c0f-2924">код SWIFT</span><span class="sxs-lookup"><span data-stu-id="37c0f-2924">swift code</span></span> 
- <span data-ttu-id="37c0f-2925">swift number #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2925">swift number #</span></span> 
- <span data-ttu-id="37c0f-2926">swift routing number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2926">swift routing number</span></span> 
- <span data-ttu-id="37c0f-2927">bic number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2927">bic number</span></span> 
- <span data-ttu-id="37c0f-2928">bic code
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2928">bic code</span></span> 
- <span data-ttu-id="37c0f-2929">БИК\#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2929">bic \#</span></span> 
- <span data-ttu-id="37c0f-2930">БИК\#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2930">bic\#</span></span> 
- <span data-ttu-id="37c0f-2931">bank identifier code
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2931">bank identifier code</span></span> 
- <span data-ttu-id="37c0f-2932">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="37c0f-2932">標準化9362</span></span> 
- <span data-ttu-id="37c0f-2933">迅速＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2933">迅速＃</span></span> 
- <span data-ttu-id="37c0f-2934">SWIFTコード
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2934">SWIFTコード</span></span> 
- <span data-ttu-id="37c0f-2935">SWIFT番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2935">SWIFT番号</span></span> 
- <span data-ttu-id="37c0f-2936">迅速なルーティング番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="37c0f-2937">BIC番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2937">BIC番号</span></span> 
- <span data-ttu-id="37c0f-2938">BICコード
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2938">BICコード</span></span> 
- <span data-ttu-id="37c0f-2939">銀行識別コードのための国際組織
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="37c0f-2940">Organisation internationale de normalisation 9362
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="37c0f-2941">Быстрая\#</span><span class="sxs-lookup"><span data-stu-id="37c0f-2941">rapide \#</span></span> 
- <span data-ttu-id="37c0f-2942">code SWIFT
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2942">code SWIFT</span></span> 
- <span data-ttu-id="37c0f-2943">le numéro de swift
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2943">le numéro de swift</span></span> 
- <span data-ttu-id="37c0f-2944">swift numéro d'acheminement
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="37c0f-2945">le numéro BIC
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2945">le numéro BIC</span></span> 
- <span data-ttu-id="37c0f-2946">\#БИК</span><span class="sxs-lookup"><span data-stu-id="37c0f-2946">\# BIC</span></span> 
- <span data-ttu-id="37c0f-2947">code identificateur de banque
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="37c0f-2948">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="37c0f-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2949">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2949">Format</span></span>

<span data-ttu-id="37c0f-2950">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2951">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2951">Pattern</span></span>

<span data-ttu-id="37c0f-2952">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="37c0f-2953">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-2954">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="37c0f-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="37c0f-2955">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2956">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2956">Checksum</span></span>

<span data-ttu-id="37c0f-2957">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2958">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2958">Definition</span></span>

<span data-ttu-id="37c0f-2959">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2960">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2961">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="37c0f-2962">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2963">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="37c0f-2964">Кэйворд_таиванесе_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="37c0f-2965">身份證字號
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2965">身份證字號</span></span> 
- <span data-ttu-id="37c0f-2966">身份證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2966">身份證</span></span> 
- <span data-ttu-id="37c0f-2967">身份證號碼
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2967">身份證號碼</span></span> 
- <span data-ttu-id="37c0f-2968">身份證號
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2968">身份證號</span></span> 
- <span data-ttu-id="37c0f-2969">身分證字號
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2969">身分證字號</span></span> 
- <span data-ttu-id="37c0f-2970">身分證 </span><span class="sxs-lookup"><span data-stu-id="37c0f-2970">身分證</span></span> 
- <span data-ttu-id="37c0f-2971">身分證號碼
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2971">身分證號碼</span></span> 
- <span data-ttu-id="37c0f-2972">身份證號
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2972">身份證號</span></span> 
- <span data-ttu-id="37c0f-2973">身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2973">身分證統一編號</span></span> 
- <span data-ttu-id="37c0f-2974">國民身分證統一編號
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="37c0f-2975">簽名
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2975">簽名</span></span> 
- <span data-ttu-id="37c0f-2976">蓋章
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2976">蓋章</span></span> 
- <span data-ttu-id="37c0f-2977">簽名或蓋章

</span><span class="sxs-lookup"><span data-stu-id="37c0f-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="37c0f-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="37c0f-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="37c0f-2979">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="37c0f-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-2980">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-2980">Format</span></span>

- <span data-ttu-id="37c0f-2981">Номер биометрического паспорта: девять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="37c0f-2982">Номер биометрической службы Passport: девять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-2983">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-2983">Pattern</span></span>
<span data-ttu-id="37c0f-2984">Номер биометрического паспорта:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2984">Biometric passport number:</span></span>
- <span data-ttu-id="37c0f-2985">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="37c0f-2985">The digit "3"</span></span> 
- <span data-ttu-id="37c0f-2986">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2986">Eight digits</span></span>

<span data-ttu-id="37c0f-2987">Номер биометрической службы Passport:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="37c0f-2988">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-2989">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-2989">Checksum</span></span>

<span data-ttu-id="37c0f-2990">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-2991">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-2991">Definition</span></span>

<span data-ttu-id="37c0f-2992">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-2993">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-2994">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="37c0f-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-2995">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="37c0f-2996">Кэйворд_таиван_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="37c0f-2997">ROC passport number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-2997">ROC passport number</span></span> 
- <span data-ttu-id="37c0f-2998">Номер паспорта</span><span class="sxs-lookup"><span data-stu-id="37c0f-2998">Passport number</span></span> 
- <span data-ttu-id="37c0f-2999">Паспорт нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-2999">Passport no</span></span> 
- <span data-ttu-id="37c0f-3000">Passport Num
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3000">Passport Num</span></span> 
- <span data-ttu-id="37c0f-3001">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3001">Passport #</span></span> 
- <span data-ttu-id="37c0f-3002">护照
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3002">护照</span></span> 
- <span data-ttu-id="37c0f-3003">中華民國護照
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3003">中華民國護照</span></span> 
- <span data-ttu-id="37c0f-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="37c0f-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="37c0f-3005">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="37c0f-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3006">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3006">Format</span></span>

<span data-ttu-id="37c0f-3007">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3008">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3008">Pattern</span></span>

<span data-ttu-id="37c0f-3009">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3009">10 letters and digits:</span></span>
- <span data-ttu-id="37c0f-3010">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="37c0f-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="37c0f-3011">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3012">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3012">Checksum</span></span>

<span data-ttu-id="37c0f-3013">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3014">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3014">Definition</span></span>

<span data-ttu-id="37c0f-3015">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3016">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3017">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-3018">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="37c0f-3019">Кэйворд_таиван_ресидент_цертификате</span><span class="sxs-lookup"><span data-stu-id="37c0f-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="37c0f-3020">Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3020">Resident Certificate</span></span> 
- <span data-ttu-id="37c0f-3021">Резидентный сертификат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3021">Resident Cert</span></span> 
- <span data-ttu-id="37c0f-3022">Resident Cert.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3022">Resident Cert.</span></span> 
- <span data-ttu-id="37c0f-3023">Идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-3023">Identification card</span></span> 
- <span data-ttu-id="37c0f-3024">Alien Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="37c0f-3025">ГИПЕРБОЛ</span><span class="sxs-lookup"><span data-stu-id="37c0f-3025">ARC</span></span> 
- <span data-ttu-id="37c0f-3026">Taiwan Area Resident Certificate
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="37c0f-3027">TARC
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3027">TARC</span></span> 
- <span data-ttu-id="37c0f-3028">居留證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3028">居留證</span></span> 
- <span data-ttu-id="37c0f-3029">外僑居留證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3029">外僑居留證</span></span> 
- <span data-ttu-id="37c0f-3030">台灣地區居留證
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="37c0f-3031">Код идентификации для тайского заполнения</span><span class="sxs-lookup"><span data-stu-id="37c0f-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3032">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3032">Format</span></span>

<span data-ttu-id="37c0f-3033">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3034">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3034">Pattern</span></span>

<span data-ttu-id="37c0f-3035">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3035">13 digits:</span></span>
- <span data-ttu-id="37c0f-3036">Первая цифра не равна 0 или 9</span><span class="sxs-lookup"><span data-stu-id="37c0f-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="37c0f-3037">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3038">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3038">Checksum</span></span>

<span data-ttu-id="37c0f-3039">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3040">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3040">Definition</span></span>

<span data-ttu-id="37c0f-3041">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3042">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3043">Найдено ключевое слово из Кэйворд_саи_Цитизен_ид.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="37c0f-3044">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3045">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3046">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="37c0f-3047">Кэйворд_саи_Цитизен_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="37c0f-3048">ID Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-3048">ID Number</span></span>
- <span data-ttu-id="37c0f-3049">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3049">Identification Number</span></span>
- <span data-ttu-id="37c0f-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="37c0f-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="37c0f-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="37c0f-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="37c0f-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="37c0f-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="37c0f-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="37c0f-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="37c0f-3054">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3055">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3055">Format</span></span>

<span data-ttu-id="37c0f-3056">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="37c0f-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3057">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3057">Pattern</span></span>

<span data-ttu-id="37c0f-3058">11 разрядов</span><span class="sxs-lookup"><span data-stu-id="37c0f-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3059">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3059">Checksum</span></span>

<span data-ttu-id="37c0f-3060">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3061">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3061">Definition</span></span>

<span data-ttu-id="37c0f-3062">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3063">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3064">Найдено ключевое слово из Кэйворд_туркиш_натионал_ид.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="37c0f-3065">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3066">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3067">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="37c0f-3068">Кэйворд_туркиш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="37c0f-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="37c0f-3069">TC Кимлик No</span><span class="sxs-lookup"><span data-stu-id="37c0f-3069">TC Kimlik No</span></span>
- <span data-ttu-id="37c0f-3070">TC Кимлик нумарасı</span><span class="sxs-lookup"><span data-stu-id="37c0f-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="37c0f-3071">Ватандаşлıк нумарасı</span><span class="sxs-lookup"><span data-stu-id="37c0f-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="37c0f-3072">Ватандаşлıк нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="37c0f-p141">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="37c0f-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3075">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3075">Format</span></span>

<span data-ttu-id="37c0f-3076">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3077">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3077">Pattern</span></span>

<span data-ttu-id="37c0f-3078">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3078">18 letters and digits:</span></span>
- <span data-ttu-id="37c0f-3079">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="37c0f-3080">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="37c0f-3080">One digit</span></span> 
- <span data-ttu-id="37c0f-3081">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="37c0f-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="37c0f-3082">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="37c0f-3083">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3084">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3084">Checksum</span></span>

<span data-ttu-id="37c0f-3085">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3086">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3086">Definition</span></span>

<span data-ttu-id="37c0f-3087">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3088">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3089">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="37c0f-3090">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-3091">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="37c0f-3092">Кэйворд_ук_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="37c0f-3093">DVLA
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3093">DVLA</span></span> 
- <span data-ttu-id="37c0f-3094">light vans
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3094">light vans</span></span> 
- <span data-ttu-id="37c0f-3095">quadbikes
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3095">quadbikes</span></span> 
- <span data-ttu-id="37c0f-3096">motor cars
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3096">motor cars</span></span> 
- <span data-ttu-id="37c0f-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="37c0f-3097">125cc</span></span> 
- <span data-ttu-id="37c0f-3098">sidecar
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3098">sidecar</span></span> 
- <span data-ttu-id="37c0f-3099">tricycles
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3099">tricycles</span></span> 
- <span data-ttu-id="37c0f-3100">motorcycles
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3100">motorcycles</span></span> 
- <span data-ttu-id="37c0f-3101">photocard licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3101">photocard licence</span></span> 
- <span data-ttu-id="37c0f-3102">learner drivers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3102">learner drivers</span></span> 
- <span data-ttu-id="37c0f-3103">licence holder
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3103">licence holder</span></span> 
- <span data-ttu-id="37c0f-3104">licence holders
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3104">licence holders</span></span> 
- <span data-ttu-id="37c0f-3105">driving licences
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3105">driving licences</span></span> 
- <span data-ttu-id="37c0f-3106">driving licence
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3106">driving licence</span></span> 
- <span data-ttu-id="37c0f-3107">dual control car
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="37c0f-p142">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="37c0f-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3110">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3110">Format</span></span>

<span data-ttu-id="37c0f-3111">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3112">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3112">Pattern</span></span>

<span data-ttu-id="37c0f-3113">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3114">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3114">Checksum</span></span>

<span data-ttu-id="37c0f-3115">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3116">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3116">Definition</span></span>

<span data-ttu-id="37c0f-3117">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3118">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3119">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3119">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3120">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="37c0f-3121">Кэйворд_ук_електорал</span><span class="sxs-lookup"><span data-stu-id="37c0f-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="37c0f-3122">council nomination
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3122">council nomination</span></span> 
- <span data-ttu-id="37c0f-3123">nomination form
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3123">nomination form</span></span> 
- <span data-ttu-id="37c0f-3124">electoral register

</span><span class="sxs-lookup"><span data-stu-id="37c0f-3124">electoral register</span></span> 
- <span data-ttu-id="37c0f-3125">electoral roll</span><span class="sxs-lookup"><span data-stu-id="37c0f-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="37c0f-p143">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="37c0f-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3128">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3128">Format</span></span>

<span data-ttu-id="37c0f-3129">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3130">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3130">Pattern</span></span>

<span data-ttu-id="37c0f-3131">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3131">10-17 digits:</span></span>
- <span data-ttu-id="37c0f-3132">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="37c0f-3133">Пробел</span><span class="sxs-lookup"><span data-stu-id="37c0f-3133">A space</span></span> 
- <span data-ttu-id="37c0f-3134">Три цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3134">Three digits</span></span> 
- <span data-ttu-id="37c0f-3135">Пробел</span><span class="sxs-lookup"><span data-stu-id="37c0f-3135">A space</span></span> 
- <span data-ttu-id="37c0f-3136">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3137">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3137">Checksum</span></span>

<span data-ttu-id="37c0f-3138">Да</span><span class="sxs-lookup"><span data-stu-id="37c0f-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3139">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3139">Definition</span></span>

<span data-ttu-id="37c0f-3140">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3141">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3142">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3142">One of the following is true:</span></span>
    - <span data-ttu-id="37c0f-3143">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="37c0f-3144">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="37c0f-3145">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="37c0f-3146">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3146">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3147">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="37c0f-3148">Кэйворд_ук_нхс_нумбер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="37c0f-3149">national health service
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3149">national health service</span></span> 
- <span data-ttu-id="37c0f-3150">nhs
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3150">nhs</span></span> 
- <span data-ttu-id="37c0f-3151">health services authority

</span><span class="sxs-lookup"><span data-stu-id="37c0f-3151">health services authority</span></span> 
- <span data-ttu-id="37c0f-3152">health authority</span><span class="sxs-lookup"><span data-stu-id="37c0f-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="37c0f-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="37c0f-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="37c0f-3154">patient id
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3154">patient id</span></span> 
- <span data-ttu-id="37c0f-3155">patient identification
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3155">patient identification</span></span> 
- <span data-ttu-id="37c0f-3156">patient no

</span><span class="sxs-lookup"><span data-stu-id="37c0f-3156">patient no</span></span> 
- <span data-ttu-id="37c0f-3157">patient number</span><span class="sxs-lookup"><span data-stu-id="37c0f-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="37c0f-3158">Кэйворд_ук_нхс_нумбер_доб</span><span class="sxs-lookup"><span data-stu-id="37c0f-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="37c0f-3159">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="37c0f-3159">GP</span></span> 
- <span data-ttu-id="37c0f-3160">DOB
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3160">DOB</span></span> 
- <span data-ttu-id="37c0f-3161">D. O. B</span><span class="sxs-lookup"><span data-stu-id="37c0f-3161">D.O.B</span></span> 
- <span data-ttu-id="37c0f-3162">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3162">Date of Birth</span></span> 
- <span data-ttu-id="37c0f-3163">Birth Date
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="37c0f-p144">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="37c0f-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3166">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3166">Format</span></span>

<span data-ttu-id="37c0f-3167">7 символов или 9 символов, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3168">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3168">Pattern</span></span>

<span data-ttu-id="37c0f-3169">Два возможных шаблона:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3169">Two possible patterns:</span></span>

- <span data-ttu-id="37c0f-3170">Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="37c0f-3171">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3171">Six digits</span></span>
- <span data-ttu-id="37c0f-3172">"A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="37c0f-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="37c0f-3173">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="37c0f-3173">OR</span></span>

- <span data-ttu-id="37c0f-3174">Две буквы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3174">Two letters</span></span>
- <span data-ttu-id="37c0f-3175">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3175">A space or dash</span></span>
- <span data-ttu-id="37c0f-3176">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3176">Two digits</span></span>
- <span data-ttu-id="37c0f-3177">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3177">A space or dash</span></span>
- <span data-ttu-id="37c0f-3178">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3178">Two digits</span></span>
- <span data-ttu-id="37c0f-3179">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3179">A space or dash</span></span>
- <span data-ttu-id="37c0f-3180">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3180">Two digits</span></span>
- <span data-ttu-id="37c0f-3181">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3181">A space or dash</span></span>
- <span data-ttu-id="37c0f-3182">Значение "A", "B", "C" или "'D"</span><span class="sxs-lookup"><span data-stu-id="37c0f-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3183">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3183">Checksum</span></span>

<span data-ttu-id="37c0f-3184">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3185">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3185">Definition</span></span>

<span data-ttu-id="37c0f-3186">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3187">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3188">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="37c0f-3189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3190">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3191">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3191">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="37c0f-3193">Кэйворд_ук_нино</span><span class="sxs-lookup"><span data-stu-id="37c0f-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="37c0f-3194">national insurance number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3194">national insurance number</span></span> 
- <span data-ttu-id="37c0f-3195">national insurance contributions
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3195">national insurance contributions</span></span> 
- <span data-ttu-id="37c0f-3196">protection act
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3196">protection act</span></span> 
- <span data-ttu-id="37c0f-3197">insurance
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3197">insurance</span></span> 
- <span data-ttu-id="37c0f-3198">social security number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3198">social security number</span></span> 
- <span data-ttu-id="37c0f-3199">insurance application
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3199">insurance application</span></span> 
- <span data-ttu-id="37c0f-3200">medical application
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3200">medical application</span></span> 
- <span data-ttu-id="37c0f-3201">social insurance
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3201">social insurance</span></span> 
- <span data-ttu-id="37c0f-3202">medical attention
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3202">medical attention</span></span> 
- <span data-ttu-id="37c0f-3203">социальное обеспечение безопасности</span><span class="sxs-lookup"><span data-stu-id="37c0f-3203">social security</span></span> 
- <span data-ttu-id="37c0f-3204">great britain
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3204">great britain</span></span> 
- <span data-ttu-id="37c0f-3205">insurance
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="37c0f-p145">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="37c0f-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3208">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3208">Format</span></span>

<span data-ttu-id="37c0f-3209">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3210">Pattern</span></span>

<span data-ttu-id="37c0f-3211">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3212">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3212">Checksum</span></span>

<span data-ttu-id="37c0f-3213">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3214">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3214">Definition</span></span>

<span data-ttu-id="37c0f-3215">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3216">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3217">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-3218">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="37c0f-3219">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="37c0f-3219">Keyword_passport</span></span>

- <span data-ttu-id="37c0f-3220">Passport Number</span><span class="sxs-lookup"><span data-stu-id="37c0f-3220">Passport Number</span></span> 
- <span data-ttu-id="37c0f-3221">
Passport No</span><span class="sxs-lookup"><span data-stu-id="37c0f-3221">Passport No</span></span> 
- <span data-ttu-id="37c0f-3222">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3222">Passport #</span></span> 
- <span data-ttu-id="37c0f-3223">Passport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3223">Passport#</span></span> 
- <span data-ttu-id="37c0f-3224">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="37c0f-3224">PassportID</span></span> 
- <span data-ttu-id="37c0f-3225">Passportno
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3225">Passportno</span></span> 
- <span data-ttu-id="37c0f-3226">passportnumber
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3226">passportnumber</span></span> 
- <span data-ttu-id="37c0f-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="37c0f-3227">パスポート</span></span> 
- <span data-ttu-id="37c0f-3228">パスポート番号
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3228">パスポート番号</span></span> 
- <span data-ttu-id="37c0f-3229">パスポートのNum
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3229">パスポートのNum</span></span> 
- <span data-ttu-id="37c0f-3230">パスポート＃
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3230">パスポート＃</span></span> 
- <span data-ttu-id="37c0f-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="37c0f-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="37c0f-3232">
Passeport n °</span><span class="sxs-lookup"><span data-stu-id="37c0f-3232">Passeport n °</span></span> 
- <span data-ttu-id="37c0f-3233">Passeport Non
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3233">Passeport Non</span></span> 
- <span data-ttu-id="37c0f-3234">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3234">Passeport #</span></span> 
- <span data-ttu-id="37c0f-3235">Passeport#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3235">Passeport#</span></span> 
- <span data-ttu-id="37c0f-3236">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3236">PasseportNon</span></span> 
- <span data-ttu-id="37c0f-3237">Passeportn °
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="37c0f-3238">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="37c0f-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3239">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3239">Format</span></span>

<span data-ttu-id="37c0f-3240">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3241">Pattern</span></span>

<span data-ttu-id="37c0f-3242">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3243">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3243">Checksum</span></span>

<span data-ttu-id="37c0f-3244">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3245">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3245">Definition</span></span>

<span data-ttu-id="37c0f-3246">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3247">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3248">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="37c0f-3249">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="37c0f-3250">Кэйворд_уса_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="37c0f-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="37c0f-3251">Checking Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3251">Checking Account Number</span></span> 
- <span data-ttu-id="37c0f-3252">Checking Account
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3252">Checking Account</span></span> 
- <span data-ttu-id="37c0f-3253">Checking Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3253">Checking Account #</span></span> 
- <span data-ttu-id="37c0f-3254">Checking Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="37c0f-3255">Checking Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3255">Checking Acct #</span></span> 
- <span data-ttu-id="37c0f-3256">Checking Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="37c0f-3257">Checking Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3257">Checking Account No.</span></span> 
- <span data-ttu-id="37c0f-3258">Bank Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3258">Bank Account Number</span></span> 
- <span data-ttu-id="37c0f-3259">Bank Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3259">Bank Account #</span></span> 
- <span data-ttu-id="37c0f-3260">Bank Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="37c0f-3261">Bank Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3261">Bank Acct #</span></span> 
- <span data-ttu-id="37c0f-3262">Bank Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="37c0f-3263">Bank Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3263">Bank Account No.</span></span> 
- <span data-ttu-id="37c0f-3264">Savings Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3264">Savings Account Number</span></span> 
- <span data-ttu-id="37c0f-3265">Savings Account.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3265">Savings Account.</span></span> 
- <span data-ttu-id="37c0f-3266">Savings Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3266">Savings Account #</span></span> 
- <span data-ttu-id="37c0f-3267">Savings Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="37c0f-3268">Savings Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3268">Savings Acct #</span></span> 
- <span data-ttu-id="37c0f-3269">Savings Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="37c0f-3270">Savings Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3270">Savings Account No.</span></span> 
- <span data-ttu-id="37c0f-3271">Debit Account Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3271">Debit Account Number</span></span> 
- <span data-ttu-id="37c0f-3272">Debit Account
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3272">Debit Account</span></span> 
- <span data-ttu-id="37c0f-3273">Debit Account #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3273">Debit Account #</span></span> 
- <span data-ttu-id="37c0f-3274">Debit Acct Number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="37c0f-3275">Debit Acct #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3275">Debit Acct #</span></span> 
- <span data-ttu-id="37c0f-3276">Debit Acct No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="37c0f-3277">Debit Account No.
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="37c0f-3278">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="37c0f-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3279">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3279">Format</span></span>

<span data-ttu-id="37c0f-3280">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3281">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3281">Pattern</span></span>

<span data-ttu-id="37c0f-3282">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="37c0f-3283">Подойдут девять цифр в формате ццц ццц ццц.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="37c0f-3284">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3285">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3285">Checksum</span></span>

<span data-ttu-id="37c0f-3286">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3287">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3287">Definition</span></span>

<span data-ttu-id="37c0f-3288">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3289">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3290">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="37c0f-3291">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="37c0f-3292">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3293">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3294">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="37c0f-3295">находится ключевое слово из Keyword_us_drivers_license_abbreviations;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="37c0f-3296">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3297">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="37c0f-3298">Кэйворд_ус_дриверс_лиценсе_аббревиатионс</span><span class="sxs-lookup"><span data-stu-id="37c0f-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="37c0f-3299">DL</span><span class="sxs-lookup"><span data-stu-id="37c0f-3299">DL</span></span> 
- <span data-ttu-id="37c0f-3300">DLS</span><span class="sxs-lookup"><span data-stu-id="37c0f-3300">DLS</span></span> 
- <span data-ttu-id="37c0f-3301">КДЛ</span><span class="sxs-lookup"><span data-stu-id="37c0f-3301">CDL</span></span> 
- <span data-ttu-id="37c0f-3302">КДЛС</span><span class="sxs-lookup"><span data-stu-id="37c0f-3302">CDLS</span></span> 
- <span data-ttu-id="37c0f-3303">ID</span><span class="sxs-lookup"><span data-stu-id="37c0f-3303">ID</span></span> 
- <span data-ttu-id="37c0f-3304">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3304">IDs</span></span> 
- <span data-ttu-id="37c0f-3305">DL#</span><span class="sxs-lookup"><span data-stu-id="37c0f-3305">DL#</span></span> 
- <span data-ttu-id="37c0f-3306">
DLS#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3306">DLS#</span></span> 
- <span data-ttu-id="37c0f-3307">CDL#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3307">CDL#</span></span> 
- <span data-ttu-id="37c0f-3308">CDLS#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3308">CDLS#</span></span> 
- <span data-ttu-id="37c0f-3309">ID#</span><span class="sxs-lookup"><span data-stu-id="37c0f-3309">ID#</span></span>
- <span data-ttu-id="37c0f-3310">
IDs#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3310">IDs#</span></span> 
- <span data-ttu-id="37c0f-3311">идентификатор</span><span class="sxs-lookup"><span data-stu-id="37c0f-3311">ID number</span></span> 
- <span data-ttu-id="37c0f-3312">ID numbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3312">ID numbers</span></span> 
- <span data-ttu-id="37c0f-3313">Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3313">LIC</span></span> 
- <span data-ttu-id="37c0f-3314">LIC#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="37c0f-3315">Кэйворд_ус_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="37c0f-3316">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3316">DriverLic</span></span> 
- <span data-ttu-id="37c0f-3317">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-3317">DriverLics</span></span> 
- <span data-ttu-id="37c0f-3318">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-3318">DriverLicense</span></span> 
- <span data-ttu-id="37c0f-3319">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-3319">DriverLicenses</span></span> 
- <span data-ttu-id="37c0f-3320">Драйвер Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3320">Driver Lic</span></span> 
- <span data-ttu-id="37c0f-3321">Драйвер ликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-3321">Driver Lics</span></span> 
- <span data-ttu-id="37c0f-3322">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3322">Driver License</span></span> 
- <span data-ttu-id="37c0f-3323">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3323">Driver Licenses</span></span> 
- <span data-ttu-id="37c0f-3324">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3324">DriversLic</span></span> 
- <span data-ttu-id="37c0f-3325">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-3325">DriversLics</span></span> 
- <span data-ttu-id="37c0f-3326">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-3326">DriversLicense</span></span> 
- <span data-ttu-id="37c0f-3327">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-3327">DriversLicenses</span></span> 
- <span data-ttu-id="37c0f-3328">Драйверы Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3328">Drivers Lic</span></span> 
- <span data-ttu-id="37c0f-3329">Драйверы ликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-3329">Drivers Lics</span></span> 
- <span data-ttu-id="37c0f-3330">Лицензия на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3330">Drivers License</span></span> 
- <span data-ttu-id="37c0f-3331">Лицензии на драйверы</span><span class="sxs-lookup"><span data-stu-id="37c0f-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="37c0f-3332">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="37c0f-3332">Driver'Lic</span></span> 
- <span data-ttu-id="37c0f-3333">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="37c0f-3333">Driver'Lics</span></span> 
- <span data-ttu-id="37c0f-3334">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="37c0f-3334">Driver'License</span></span> 
- <span data-ttu-id="37c0f-3335">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="37c0f-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="37c0f-3336">Драйвер "Лик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3336">Driver' Lic</span></span> 
- <span data-ttu-id="37c0f-3337">Драйвер "ЛИКС</span><span class="sxs-lookup"><span data-stu-id="37c0f-3337">Driver' Lics</span></span> 
- <span data-ttu-id="37c0f-3338">Лицензия "Driver"</span><span class="sxs-lookup"><span data-stu-id="37c0f-3338">Driver' License</span></span> 
- <span data-ttu-id="37c0f-3339">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3339">Driver' Licenses</span></span>
- <span data-ttu-id="37c0f-3340">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="37c0f-3340">Driver'sLic</span></span> 
- <span data-ttu-id="37c0f-3341">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="37c0f-3341">Driver'sLics</span></span> 
- <span data-ttu-id="37c0f-3342">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="37c0f-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="37c0f-3343">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="37c0f-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="37c0f-3344">Лик драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-3344">Driver's Lic</span></span> 
- <span data-ttu-id="37c0f-3345">Ликс драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-3345">Driver's Lics</span></span> 
- <span data-ttu-id="37c0f-3346">Лицензия на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3346">Driver's License</span></span> 
- <span data-ttu-id="37c0f-3347">Лицензии на драйвер</span><span class="sxs-lookup"><span data-stu-id="37c0f-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="37c0f-3348">identification number
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3348">identification number</span></span> 
- <span data-ttu-id="37c0f-3349">identification numbers
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3349">identification numbers</span></span> 
- <span data-ttu-id="37c0f-3350">identification #
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3350">identification #</span></span> 
- <span data-ttu-id="37c0f-3351">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-3351">id card</span></span> 
- <span data-ttu-id="37c0f-3352">идентификационные карточки</span><span class="sxs-lookup"><span data-stu-id="37c0f-3352">id cards</span></span> 
- <span data-ttu-id="37c0f-3353">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="37c0f-3353">identification card</span></span> 
- <span data-ttu-id="37c0f-3354">идентификационные карточки</span><span class="sxs-lookup"><span data-stu-id="37c0f-3354">identification cards</span></span> 
- <span data-ttu-id="37c0f-3355">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3355">DriverLic#</span></span> 
- <span data-ttu-id="37c0f-3356">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3356">DriverLics#</span></span> 
- <span data-ttu-id="37c0f-3357">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3357">DriverLicense#</span></span> 
- <span data-ttu-id="37c0f-3358">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="37c0f-3359">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="37c0f-3359">Driver Lic#</span></span> 
- <span data-ttu-id="37c0f-3360">
Driver Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3360">Driver Lics#</span></span> 
- <span data-ttu-id="37c0f-3361">Номер лицензии драйвера</span><span class="sxs-lookup"><span data-stu-id="37c0f-3361">Driver License#</span></span> 
- <span data-ttu-id="37c0f-3362">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="37c0f-3363">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3363">DriversLic#</span></span> 
- <span data-ttu-id="37c0f-3364">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3364">DriversLics#</span></span> 
- <span data-ttu-id="37c0f-3365">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3365">DriversLicense#</span></span> 
- <span data-ttu-id="37c0f-3366">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="37c0f-3367">Drivers Лик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="37c0f-3368">Drivers ликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="37c0f-3369">Driver License #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3369">Drivers License#</span></span> 
- <span data-ttu-id="37c0f-3370">Лицензии на драйверы #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="37c0f-3371">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="37c0f-3372">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="37c0f-3373">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3373">Driver'License#</span></span> 
- <span data-ttu-id="37c0f-3374">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="37c0f-3375">Driver' Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="37c0f-3376">Driver' Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="37c0f-3377">Driver' License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3377">Driver' License#</span></span> 
- <span data-ttu-id="37c0f-3378">Driver' Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="37c0f-3379">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="37c0f-3380">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="37c0f-3381">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="37c0f-3382">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="37c0f-3383">Driver's Lic#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="37c0f-3384">Driver's Lics#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="37c0f-3385">Driver's License#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3385">Driver's License#</span></span> 
- <span data-ttu-id="37c0f-3386">Driver's Licenses#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="37c0f-3387">Идентификатор карточки #</span><span class="sxs-lookup"><span data-stu-id="37c0f-3387">id card#</span></span> 
- <span data-ttu-id="37c0f-3388">id cards#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3388">id cards#</span></span> 
- <span data-ttu-id="37c0f-3389">identification card#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3389">identification card#</span></span> 
- <span data-ttu-id="37c0f-3390">identification cards#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="37c0f-3391">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="37c0f-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="37c0f-3392">Аббревиатура штата (например, NY)
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="37c0f-3393">Название штата (например, New York)
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="37c0f-3394">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3395">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3395">Format</span></span>

<span data-ttu-id="37c0f-3396">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="37c0f-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3397">Pattern</span></span>

<span data-ttu-id="37c0f-3398">С форматированием</span><span class="sxs-lookup"><span data-stu-id="37c0f-3398">Formatted:</span></span>
- <span data-ttu-id="37c0f-3399">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="37c0f-3399">The digit "9"</span></span> 
- <span data-ttu-id="37c0f-3400">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3400">Two digits</span></span> 
- <span data-ttu-id="37c0f-3401">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3401">A space or dash</span></span> 
- <span data-ttu-id="37c0f-3402">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="37c0f-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="37c0f-3403">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="37c0f-3403">A digit</span></span> 
- <span data-ttu-id="37c0f-3404">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="37c0f-3404">A space, or dash</span></span> 
- <span data-ttu-id="37c0f-3405">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3405">Four digits</span></span>

<span data-ttu-id="37c0f-3406">Без форматирования</span><span class="sxs-lookup"><span data-stu-id="37c0f-3406">Unformatted:</span></span>
- <span data-ttu-id="37c0f-3407">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="37c0f-3407">The digit "9"</span></span> 
- <span data-ttu-id="37c0f-3408">Две цифры</span><span class="sxs-lookup"><span data-stu-id="37c0f-3408">Two digits</span></span> 
- <span data-ttu-id="37c0f-3409">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="37c0f-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="37c0f-3410">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="37c0f-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3411">Checksum</span></span>

<span data-ttu-id="37c0f-3412">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="37c0f-3413">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3413">Definition</span></span>

<span data-ttu-id="37c0f-3414">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3415">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3416">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="37c0f-3417">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="37c0f-3418">функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="37c0f-3419">функция Func_us_date находит дату в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="37c0f-3420">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="37c0f-3421">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3422">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3423">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="37c0f-3424">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="37c0f-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="37c0f-3425">функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="37c0f-3426">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3426">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3427">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="37c0f-3428">Кэйворд_итин</span><span class="sxs-lookup"><span data-stu-id="37c0f-3428">Keyword_itin</span></span>

- <span data-ttu-id="37c0f-3429">taxpayer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3429">taxpayer</span></span> 
- <span data-ttu-id="37c0f-3430">tax id
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3430">tax id</span></span> 
- <span data-ttu-id="37c0f-3431">tax identification
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3431">tax identification</span></span> 
- <span data-ttu-id="37c0f-3432">itin
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3432">itin</span></span> 
- <span data-ttu-id="37c0f-3433">SSN</span><span class="sxs-lookup"><span data-stu-id="37c0f-3433">ssn</span></span> 
- <span data-ttu-id="37c0f-3434">tin
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3434">tin</span></span> 
- <span data-ttu-id="37c0f-3435">социальное обеспечение безопасности</span><span class="sxs-lookup"><span data-stu-id="37c0f-3435">social security</span></span> 
- <span data-ttu-id="37c0f-3436">tax payer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3436">tax payer</span></span> 
- <span data-ttu-id="37c0f-3437">itins
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3437">itins</span></span> 
- <span data-ttu-id="37c0f-3438">taxid

</span><span class="sxs-lookup"><span data-stu-id="37c0f-3438">taxid</span></span> 
- <span data-ttu-id="37c0f-3439">individual taxpayer
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="37c0f-3440">Кэйворд_итин_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="37c0f-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="37c0f-3441">License</span><span class="sxs-lookup"><span data-stu-id="37c0f-3441">License</span></span> 
- <span data-ttu-id="37c0f-3442">DL</span><span class="sxs-lookup"><span data-stu-id="37c0f-3442">DL</span></span> 
- <span data-ttu-id="37c0f-3443">DOB
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3443">DOB</span></span> 
- <span data-ttu-id="37c0f-3444">Birthdate</span><span class="sxs-lookup"><span data-stu-id="37c0f-3444">Birthdate</span></span> 
- <span data-ttu-id="37c0f-3445">День рождения </span><span class="sxs-lookup"><span data-stu-id="37c0f-3445">Birthday</span></span> 
- <span data-ttu-id="37c0f-3446">Date of Birth
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="37c0f-3447">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="37c0f-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="37c0f-3448">Формат</span><span class="sxs-lookup"><span data-stu-id="37c0f-3448">Format</span></span>

<span data-ttu-id="37c0f-3449">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="37c0f-3450">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="37c0f-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="37c0f-3451">Шаблон</span><span class="sxs-lookup"><span data-stu-id="37c0f-3451">Pattern</span></span>

<span data-ttu-id="37c0f-3452">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="37c0f-3453">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="37c0f-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="37c0f-3454">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="37c0f-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="37c0f-3455">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="37c0f-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="37c0f-3456">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="37c0f-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="37c0f-3457">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="37c0f-3457">Checksum</span></span>

<span data-ttu-id="37c0f-3458">Нет</span><span class="sxs-lookup"><span data-stu-id="37c0f-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="37c0f-3459">Определение</span><span class="sxs-lookup"><span data-stu-id="37c0f-3459">Definition</span></span>

<span data-ttu-id="37c0f-3460">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3461">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3462">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="37c0f-3463">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3464">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3465">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="37c0f-3466">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3467">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3468">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="37c0f-3469">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="37c0f-3470">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="37c0f-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="37c0f-3471">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="37c0f-3472">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="37c0f-3473">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="37c0f-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="37c0f-3474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="37c0f-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="37c0f-3475">Кэйворд_ссн</span><span class="sxs-lookup"><span data-stu-id="37c0f-3475">Keyword_ssn</span></span>

- <span data-ttu-id="37c0f-3476">Social Security
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3476">Social Security</span></span> 
- <span data-ttu-id="37c0f-3477">Social Security#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3477">Social Security#</span></span> 
- <span data-ttu-id="37c0f-3478">Soc Sec
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3478">Soc Sec</span></span> 
- <span data-ttu-id="37c0f-3479">SSN</span><span class="sxs-lookup"><span data-stu-id="37c0f-3479">SSN</span></span> 
- <span data-ttu-id="37c0f-3480">SSNS
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3480">SSNS</span></span> 
- <span data-ttu-id="37c0f-3481">SSN#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3481">SSN#</span></span> 
- <span data-ttu-id="37c0f-3482">SS#
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3482">SS#</span></span> 
- <span data-ttu-id="37c0f-3483">SSID
</span><span class="sxs-lookup"><span data-stu-id="37c0f-3483">SSID</span></span> 
   

