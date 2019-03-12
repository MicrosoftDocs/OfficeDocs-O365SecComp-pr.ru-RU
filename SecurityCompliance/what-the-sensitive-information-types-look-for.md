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
ms.collection:
- M365-security-compliance
description: Защита от потери данных (DLP) в центре безопасности &amp; Office 365 включает в себя 80 типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных. В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.
ms.openlocfilehash: e9811b285e98a791570dc91e275cb5cead4f8bc9
ms.sourcegitcommit: 6e8e2b43a4bea31c1e835c5b050824651c6a0094
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/11/2019
ms.locfileid: "30537646"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="16264-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="16264-104">What the sensitive information types look for</span></span>

<span data-ttu-id="16264-105">Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="16264-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="16264-106">В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.</span><span class="sxs-lookup"><span data-stu-id="16264-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="16264-107">Тип конфиденциальной информации определяется шаблоном, который можно идентифицировать регулярным выражением или функцией.</span><span class="sxs-lookup"><span data-stu-id="16264-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="16264-108">Кроме того, для идентификации типа конфиденциальной информации могут использоваться подкрепляющие доказательства, такие как ключевые слова и контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="16264-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="16264-109">Уровень вероятности и расположение слов и знаков также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="16264-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="16264-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="16264-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-111">Format</span><span class="sxs-lookup"><span data-stu-id="16264-111">Format</span></span>

<span data-ttu-id="16264-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="16264-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-113">Pattern</span></span>

<span data-ttu-id="16264-114">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="16264-114">Formatted:</span></span>
- <span data-ttu-id="16264-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="16264-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="16264-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-116">A hyphen</span></span>
- <span data-ttu-id="16264-117">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-117">Four digits</span></span>
- <span data-ttu-id="16264-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-118">A hyphen</span></span>
- <span data-ttu-id="16264-119">цифра.</span><span class="sxs-lookup"><span data-stu-id="16264-119">A digit</span></span>

<span data-ttu-id="16264-120">Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8.</span><span class="sxs-lookup"><span data-stu-id="16264-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="16264-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-121">Checksum</span></span>

<span data-ttu-id="16264-122">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-123">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-123">Definition</span></span>

<span data-ttu-id="16264-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="16264-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="16264-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="16264-128">Кэйворд_аба_раутинг</span><span class="sxs-lookup"><span data-stu-id="16264-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="16264-129">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="16264-129">aba</span></span>
- <span data-ttu-id="16264-130">aba#</span><span class="sxs-lookup"><span data-stu-id="16264-130">aba #</span></span>
- <span data-ttu-id="16264-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="16264-131">aba routing #</span></span>
- <span data-ttu-id="16264-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="16264-132">aba routing number</span></span>
- <span data-ttu-id="16264-133">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="16264-133">aba#</span></span>
- <span data-ttu-id="16264-134">абараутинг #</span><span class="sxs-lookup"><span data-stu-id="16264-134">abarouting#</span></span>
- <span data-ttu-id="16264-135">aba number</span><span class="sxs-lookup"><span data-stu-id="16264-135">aba number</span></span>
- <span data-ttu-id="16264-136">абараутингнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-136">abaroutingnumber</span></span>
- <span data-ttu-id="16264-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="16264-137">american bank association routing #</span></span>
- <span data-ttu-id="16264-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="16264-138">american bank association routing number</span></span>
- <span data-ttu-id="16264-139">американбанкассоЦиатионраутинг #</span><span class="sxs-lookup"><span data-stu-id="16264-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="16264-140">американбанкассоЦиатионраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="16264-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="16264-141">bank routing number</span></span>
- <span data-ttu-id="16264-142">банкраутинг #</span><span class="sxs-lookup"><span data-stu-id="16264-142">bankrouting#</span></span>
- <span data-ttu-id="16264-143">банкраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-143">bankroutingnumber</span></span>
- <span data-ttu-id="16264-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="16264-144">routing transit number</span></span>
- <span data-ttu-id="16264-145">РТН</span><span class="sxs-lookup"><span data-stu-id="16264-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="16264-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="16264-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-147">Format</span><span class="sxs-lookup"><span data-stu-id="16264-147">Format</span></span>

<span data-ttu-id="16264-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="16264-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-149">Pattern</span></span>

<span data-ttu-id="16264-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-150">Eight digits:</span></span>
- <span data-ttu-id="16264-151">две цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-151">Two digits</span></span>
- <span data-ttu-id="16264-152">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-152">A period</span></span>
- <span data-ttu-id="16264-153">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-153">Three digits</span></span>
- <span data-ttu-id="16264-154">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-154">A period</span></span>
- <span data-ttu-id="16264-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-156">Checksum</span></span>

<span data-ttu-id="16264-157">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-158">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-158">Definition</span></span>

<span data-ttu-id="16264-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="16264-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="16264-163">Кэйворд_аржентина_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="16264-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="16264-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="16264-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="16264-165">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="16264-165">Identity</span></span> 
- <span data-ttu-id="16264-166">Идентификация национальной идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="16264-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="16264-167">DNI</span><span class="sxs-lookup"><span data-stu-id="16264-167">DNI</span></span> 
- <span data-ttu-id="16264-168">Национальная реестр пользователей NIC</span><span class="sxs-lookup"><span data-stu-id="16264-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="16264-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="16264-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="16264-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="16264-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="16264-171">ИДЕНТИДАД</span><span class="sxs-lookup"><span data-stu-id="16264-171">Identidad</span></span> 
- <span data-ttu-id="16264-172">ИдентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="16264-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="16264-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="16264-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-174">Format</span><span class="sxs-lookup"><span data-stu-id="16264-174">Format</span></span>

<span data-ttu-id="16264-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="16264-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-176">Pattern</span></span>

<span data-ttu-id="16264-177">Номер счета состоит из 6–10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="16264-178">Номер филиала государственного банка Австралии</span><span class="sxs-lookup"><span data-stu-id="16264-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="16264-179">три цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-179">Three digits</span></span> 
- <span data-ttu-id="16264-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-180">A hyphen</span></span> 
- <span data-ttu-id="16264-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-182">Checksum</span></span>

<span data-ttu-id="16264-183">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-184">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-184">Definition</span></span>

<span data-ttu-id="16264-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="16264-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="16264-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="16264-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="16264-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="16264-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="16264-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="16264-193">Кэйворд_аустралиа_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="16264-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="16264-194">swift bank code</span></span>
- <span data-ttu-id="16264-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="16264-195">correspondent bank</span></span>
- <span data-ttu-id="16264-196">base currency</span><span class="sxs-lookup"><span data-stu-id="16264-196">base currency</span></span>
- <span data-ttu-id="16264-197">usa account</span><span class="sxs-lookup"><span data-stu-id="16264-197">usa account</span></span>
- <span data-ttu-id="16264-198">holder address</span><span class="sxs-lookup"><span data-stu-id="16264-198">holder address</span></span>
- <span data-ttu-id="16264-199">bank address</span><span class="sxs-lookup"><span data-stu-id="16264-199">bank address</span></span>
- <span data-ttu-id="16264-200">information account</span><span class="sxs-lookup"><span data-stu-id="16264-200">information account</span></span>
- <span data-ttu-id="16264-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="16264-201">fund transfers</span></span>
- <span data-ttu-id="16264-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="16264-202">bank charges</span></span>
- <span data-ttu-id="16264-203">bank details</span><span class="sxs-lookup"><span data-stu-id="16264-203">bank details</span></span>
- <span data-ttu-id="16264-204">banking information</span><span class="sxs-lookup"><span data-stu-id="16264-204">banking information</span></span>
- <span data-ttu-id="16264-205">full names</span><span class="sxs-lookup"><span data-stu-id="16264-205">full names</span></span>
- <span data-ttu-id="16264-206">иаеа</span><span class="sxs-lookup"><span data-stu-id="16264-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="16264-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="16264-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-208">Format</span><span class="sxs-lookup"><span data-stu-id="16264-208">Format</span></span>

<span data-ttu-id="16264-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-210">Pattern</span></span>

<span data-ttu-id="16264-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="16264-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="16264-213">две цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-213">Two digits</span></span> 
- <span data-ttu-id="16264-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="16264-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="16264-215">OR</span><span class="sxs-lookup"><span data-stu-id="16264-215">OR</span></span>

- <span data-ttu-id="16264-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="16264-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-217">4-9 digits</span></span>

<span data-ttu-id="16264-218">OR</span><span class="sxs-lookup"><span data-stu-id="16264-218">OR</span></span>

- <span data-ttu-id="16264-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="16264-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-220">Checksum</span></span>

<span data-ttu-id="16264-221">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-222">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-222">Definition</span></span>

<span data-ttu-id="16264-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="16264-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="16264-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="16264-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="16264-228">Кэйворд_аустралиа_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="16264-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="16264-229">international driving permits</span></span>
- <span data-ttu-id="16264-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="16264-230">australian automobile association</span></span>
- <span data-ttu-id="16264-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="16264-231">international driving permit</span></span>
- <span data-ttu-id="16264-232">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="16264-232">DriverLicence</span></span>
- <span data-ttu-id="16264-233">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="16264-233">DriverLicences</span></span>
- <span data-ttu-id="16264-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="16264-234">Driver Lic</span></span>
- <span data-ttu-id="16264-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="16264-235">Driver Licence</span></span>
- <span data-ttu-id="16264-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="16264-236">Driver Licences</span></span>
- <span data-ttu-id="16264-237">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="16264-237">DriversLic</span></span>
- <span data-ttu-id="16264-238">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="16264-238">DriversLicence</span></span>
- <span data-ttu-id="16264-239">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="16264-239">DriversLicences</span></span>
- <span data-ttu-id="16264-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="16264-240">Drivers Lic</span></span>
- <span data-ttu-id="16264-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="16264-241">Drivers Lics</span></span>
- <span data-ttu-id="16264-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="16264-242">Drivers Licence</span></span>
- <span data-ttu-id="16264-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="16264-243">Drivers Licences</span></span>
- <span data-ttu-id="16264-244">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="16264-244">Driver'Lic</span></span>
- <span data-ttu-id="16264-245">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="16264-245">Driver'Lics</span></span>
- <span data-ttu-id="16264-246">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="16264-246">Driver'Licence</span></span>
- <span data-ttu-id="16264-247">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="16264-247">Driver'Licences</span></span>
- <span data-ttu-id="16264-248">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="16264-248">Driver' Lic</span></span>
- <span data-ttu-id="16264-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="16264-249">Driver' Lics</span></span>
- <span data-ttu-id="16264-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="16264-250">Driver' Licence</span></span>
- <span data-ttu-id="16264-251">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="16264-251">Driver' Licences</span></span>
- <span data-ttu-id="16264-252">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="16264-252">Driver'sLic</span></span>
- <span data-ttu-id="16264-253">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="16264-253">Driver'sLics</span></span>
- <span data-ttu-id="16264-254">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="16264-254">Driver'sLicence</span></span>
- <span data-ttu-id="16264-255">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="16264-255">Driver'sLicences</span></span>
- <span data-ttu-id="16264-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="16264-256">Driver's Lic</span></span>
- <span data-ttu-id="16264-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="16264-257">Driver's Lics</span></span>
- <span data-ttu-id="16264-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="16264-258">Driver's Licence</span></span>
- <span data-ttu-id="16264-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="16264-259">Driver's Licences</span></span>
- <span data-ttu-id="16264-260">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="16264-260">DriverLic#</span></span>
- <span data-ttu-id="16264-261">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="16264-261">DriverLics#</span></span>
- <span data-ttu-id="16264-262">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="16264-262">DriverLicence#</span></span>
- <span data-ttu-id="16264-263">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="16264-263">DriverLicences#</span></span>
- <span data-ttu-id="16264-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-264">Driver Lic#</span></span>
- <span data-ttu-id="16264-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-265">Driver Lics#</span></span>
- <span data-ttu-id="16264-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-266">Driver Licence#</span></span>
- <span data-ttu-id="16264-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-267">Driver Licences#</span></span>
- <span data-ttu-id="16264-268">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="16264-268">DriversLic#</span></span>
- <span data-ttu-id="16264-269">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="16264-269">DriversLics#</span></span>
- <span data-ttu-id="16264-270">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="16264-270">DriversLicence#</span></span>
- <span data-ttu-id="16264-271">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="16264-271">DriversLicences#</span></span>
- <span data-ttu-id="16264-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-272">Drivers Lic#</span></span>
- <span data-ttu-id="16264-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-273">Drivers Lics#</span></span>
- <span data-ttu-id="16264-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-274">Drivers Licence#</span></span>
- <span data-ttu-id="16264-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-275">Drivers Licences#</span></span>
- <span data-ttu-id="16264-276">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="16264-276">Driver'Lic#</span></span>
- <span data-ttu-id="16264-277">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="16264-277">Driver'Lics#</span></span>
- <span data-ttu-id="16264-278">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="16264-278">Driver'Licence#</span></span>
- <span data-ttu-id="16264-279">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="16264-279">Driver'Licences#</span></span>
- <span data-ttu-id="16264-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-280">Driver' Lic#</span></span>
- <span data-ttu-id="16264-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-281">Driver' Lics#</span></span>
- <span data-ttu-id="16264-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-282">Driver' Licence#</span></span>
- <span data-ttu-id="16264-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-283">Driver' Licences#</span></span>
- <span data-ttu-id="16264-284">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="16264-284">Driver'sLic#</span></span>
- <span data-ttu-id="16264-285">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="16264-285">Driver'sLics#</span></span>
- <span data-ttu-id="16264-286">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="16264-286">Driver'sLicence#</span></span>
- <span data-ttu-id="16264-287">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="16264-287">Driver'sLicences#</span></span>
- <span data-ttu-id="16264-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-288">Driver's Lic#</span></span>
- <span data-ttu-id="16264-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-289">Driver's Lics#</span></span>
- <span data-ttu-id="16264-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-290">Driver's Licence#</span></span>
- <span data-ttu-id="16264-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="16264-292">Кэйворд_аустралиа_дриверс_лиценсе_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="16264-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="16264-293">AAA</span><span class="sxs-lookup"><span data-stu-id="16264-293">aaa</span></span>
- <span data-ttu-id="16264-294">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-294">DriverLicense</span></span>
- <span data-ttu-id="16264-295">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-295">DriverLicenses</span></span>
- <span data-ttu-id="16264-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="16264-296">Driver License</span></span>
- <span data-ttu-id="16264-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-297">Driver Licenses</span></span>
- <span data-ttu-id="16264-298">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-298">DriversLicense</span></span>
- <span data-ttu-id="16264-299">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-299">DriversLicenses</span></span>
- <span data-ttu-id="16264-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="16264-300">Drivers License</span></span>
- <span data-ttu-id="16264-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-301">Drivers Licenses</span></span>
- <span data-ttu-id="16264-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="16264-302">Driver'License</span></span>
- <span data-ttu-id="16264-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-303">Driver'Licenses</span></span>
- <span data-ttu-id="16264-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="16264-304">Driver' License</span></span>
- <span data-ttu-id="16264-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-305">Driver' Licenses</span></span>
- <span data-ttu-id="16264-306">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-306">Driver'sLicense</span></span>
- <span data-ttu-id="16264-307">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-307">Driver'sLicenses</span></span>
- <span data-ttu-id="16264-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="16264-308">Driver's License</span></span>
- <span data-ttu-id="16264-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-309">Driver's Licenses</span></span>
- <span data-ttu-id="16264-310">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-310">DriverLicense#</span></span>
- <span data-ttu-id="16264-311">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-311">DriverLicenses#</span></span>
- <span data-ttu-id="16264-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="16264-312">Driver License#</span></span>
- <span data-ttu-id="16264-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-313">Driver Licenses#</span></span>
- <span data-ttu-id="16264-314">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-314">DriversLicense#</span></span>
- <span data-ttu-id="16264-315">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-315">DriversLicenses#</span></span>
- <span data-ttu-id="16264-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="16264-316">Drivers License#</span></span>
- <span data-ttu-id="16264-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-317">Drivers Licenses#</span></span>
- <span data-ttu-id="16264-318">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="16264-318">Driver'License#</span></span>
- <span data-ttu-id="16264-319">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-319">Driver'Licenses#</span></span>
- <span data-ttu-id="16264-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="16264-320">Driver' License#</span></span>
- <span data-ttu-id="16264-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-321">Driver' Licenses#</span></span>
- <span data-ttu-id="16264-322">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-322">Driver'sLicense#</span></span>
- <span data-ttu-id="16264-323">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="16264-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="16264-324">Driver's License#</span></span>
- <span data-ttu-id="16264-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="16264-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="16264-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-327">Format</span><span class="sxs-lookup"><span data-stu-id="16264-327">Format</span></span>

<span data-ttu-id="16264-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-329">Pattern</span></span>

<span data-ttu-id="16264-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-330">10-11 digits:</span></span>
- <span data-ttu-id="16264-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="16264-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="16264-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="16264-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="16264-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="16264-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="16264-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-335">Checksum</span></span>

<span data-ttu-id="16264-336">Да</span><span class="sxs-lookup"><span data-stu-id="16264-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-337">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-337">Definition</span></span>

<span data-ttu-id="16264-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="16264-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="16264-341">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-341">The checksum passes.</span></span>

<span data-ttu-id="16264-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="16264-346">Кэйворд_аустралиа_медикал_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="16264-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="16264-347">bank account details</span></span>
- <span data-ttu-id="16264-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="16264-348">medicare payments</span></span>
- <span data-ttu-id="16264-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="16264-349">mortgage account</span></span>
- <span data-ttu-id="16264-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="16264-350">bank payments</span></span>
- <span data-ttu-id="16264-351">information branch</span><span class="sxs-lookup"><span data-stu-id="16264-351">information branch</span></span>
- <span data-ttu-id="16264-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="16264-352">credit card loan</span></span>
- <span data-ttu-id="16264-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="16264-353">department of human services</span></span>
- <span data-ttu-id="16264-354">local service</span><span class="sxs-lookup"><span data-stu-id="16264-354">local service</span></span>
- <span data-ttu-id="16264-355">Медикаре</span><span class="sxs-lookup"><span data-stu-id="16264-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="16264-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="16264-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-357">Format</span><span class="sxs-lookup"><span data-stu-id="16264-357">Format</span></span>

<span data-ttu-id="16264-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-359">Pattern</span></span>

<span data-ttu-id="16264-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-361">Checksum</span></span>

<span data-ttu-id="16264-362">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-363">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-363">Definition</span></span>

<span data-ttu-id="16264-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-366">Найдено ключевое слово из Кэйворд_пасспорт или Кэйворд_аустралиа_пасспорт_нумбер.</span><span class="sxs-lookup"><span data-stu-id="16264-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="16264-368">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-368">Keyword_passport</span></span>

- <span data-ttu-id="16264-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="16264-369">Passport Number</span></span>
- <span data-ttu-id="16264-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="16264-370">Passport No</span></span>
- <span data-ttu-id="16264-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="16264-371">Passport #</span></span>
- <span data-ttu-id="16264-372">Службу</span><span class="sxs-lookup"><span data-stu-id="16264-372">Passport#</span></span>
- <span data-ttu-id="16264-373">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="16264-373">PassportID</span></span>
- <span data-ttu-id="16264-374">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="16264-374">Passportno</span></span>
- <span data-ttu-id="16264-375">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-375">passportnumber</span></span>
- <span data-ttu-id="16264-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="16264-376">パスポート</span></span>
- <span data-ttu-id="16264-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="16264-377">パスポート番号</span></span>
- <span data-ttu-id="16264-378">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="16264-378">パスポートのNum</span></span>
- <span data-ttu-id="16264-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="16264-379">パスポート ＃</span></span> 
- <span data-ttu-id="16264-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="16264-380">Numéro de passeport</span></span>
- <span data-ttu-id="16264-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="16264-381">Passeport n °</span></span>
- <span data-ttu-id="16264-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="16264-382">Passeport Non</span></span>
- <span data-ttu-id="16264-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="16264-383">Passeport #</span></span>
- <span data-ttu-id="16264-384">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="16264-384">Passeport#</span></span>
- <span data-ttu-id="16264-385">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="16264-385">PasseportNon</span></span>
- <span data-ttu-id="16264-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="16264-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="16264-387">Кэйворд_аустралиа_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="16264-388">службу</span><span class="sxs-lookup"><span data-stu-id="16264-388">passport</span></span>
- <span data-ttu-id="16264-389">passport details</span><span class="sxs-lookup"><span data-stu-id="16264-389">passport details</span></span>
- <span data-ttu-id="16264-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="16264-390">immigration and citizenship</span></span>
- <span data-ttu-id="16264-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="16264-391">commonwealth of australia</span></span>
- <span data-ttu-id="16264-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="16264-392">department of immigration</span></span>
- <span data-ttu-id="16264-393">residential address</span><span class="sxs-lookup"><span data-stu-id="16264-393">residential address</span></span>
- <span data-ttu-id="16264-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="16264-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="16264-395">Visa</span><span class="sxs-lookup"><span data-stu-id="16264-395">visa</span></span>
- <span data-ttu-id="16264-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="16264-396">national identity card</span></span>
- <span data-ttu-id="16264-397">passport number</span><span class="sxs-lookup"><span data-stu-id="16264-397">passport number</span></span>
- <span data-ttu-id="16264-398">travel document</span><span class="sxs-lookup"><span data-stu-id="16264-398">travel document</span></span>
- <span data-ttu-id="16264-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="16264-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="16264-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="16264-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-401">Format</span><span class="sxs-lookup"><span data-stu-id="16264-401">Format</span></span>

<span data-ttu-id="16264-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-403">Pattern</span></span>

<span data-ttu-id="16264-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="16264-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="16264-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-405">Three digits</span></span> 
- <span data-ttu-id="16264-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="16264-406">An optional space</span></span> 
- <span data-ttu-id="16264-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-407">Three digits</span></span> 
- <span data-ttu-id="16264-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="16264-408">An optional space</span></span> 
- <span data-ttu-id="16264-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="16264-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-410">Checksum</span></span>

<span data-ttu-id="16264-411">Да</span><span class="sxs-lookup"><span data-stu-id="16264-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-412">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-412">Definition</span></span>

<span data-ttu-id="16264-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="16264-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="16264-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="16264-418">Кэйворд_аустралиа_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="16264-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="16264-419">australian business number</span></span>
- <span data-ttu-id="16264-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="16264-420">marginal tax rate</span></span>
- <span data-ttu-id="16264-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="16264-421">medicare levy</span></span>
- <span data-ttu-id="16264-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="16264-422">portfolio number</span></span>
- <span data-ttu-id="16264-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="16264-423">service veterans</span></span>
- <span data-ttu-id="16264-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="16264-424">withholding tax</span></span>
- <span data-ttu-id="16264-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="16264-425">individual tax return</span></span>
- <span data-ttu-id="16264-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="16264-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="16264-427">Кэйворд_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="16264-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="16264-428">00000001</span><span class="sxs-lookup"><span data-stu-id="16264-428">00000000</span></span>
- <span data-ttu-id="16264-429">11111111</span><span class="sxs-lookup"><span data-stu-id="16264-429">11111111</span></span>
- <span data-ttu-id="16264-430">22222222</span><span class="sxs-lookup"><span data-stu-id="16264-430">22222222</span></span>
- <span data-ttu-id="16264-431">33333333</span><span class="sxs-lookup"><span data-stu-id="16264-431">33333333</span></span>
- <span data-ttu-id="16264-432">44444444</span><span class="sxs-lookup"><span data-stu-id="16264-432">44444444</span></span>
- <span data-ttu-id="16264-433">55555555</span><span class="sxs-lookup"><span data-stu-id="16264-433">55555555</span></span>
- <span data-ttu-id="16264-434">66666666</span><span class="sxs-lookup"><span data-stu-id="16264-434">66666666</span></span>
- <span data-ttu-id="16264-435">77777777</span><span class="sxs-lookup"><span data-stu-id="16264-435">77777777</span></span>
- <span data-ttu-id="16264-436">88888888</span><span class="sxs-lookup"><span data-stu-id="16264-436">88888888</span></span>
- <span data-ttu-id="16264-437">99999999</span><span class="sxs-lookup"><span data-stu-id="16264-437">99999999</span></span>
- <span data-ttu-id="16264-438">000000000</span><span class="sxs-lookup"><span data-stu-id="16264-438">000000000</span></span>
- <span data-ttu-id="16264-439">111111111</span><span class="sxs-lookup"><span data-stu-id="16264-439">111111111</span></span>
- <span data-ttu-id="16264-440">222222222</span><span class="sxs-lookup"><span data-stu-id="16264-440">222222222</span></span>
- <span data-ttu-id="16264-441">333333333</span><span class="sxs-lookup"><span data-stu-id="16264-441">333333333</span></span>
- <span data-ttu-id="16264-442">444444444</span><span class="sxs-lookup"><span data-stu-id="16264-442">444444444</span></span>
- <span data-ttu-id="16264-443">555555555</span><span class="sxs-lookup"><span data-stu-id="16264-443">555555555</span></span>
- <span data-ttu-id="16264-444">666666666</span><span class="sxs-lookup"><span data-stu-id="16264-444">666666666</span></span>
- <span data-ttu-id="16264-445">777777777</span><span class="sxs-lookup"><span data-stu-id="16264-445">777777777</span></span>
- <span data-ttu-id="16264-446">888888888</span><span class="sxs-lookup"><span data-stu-id="16264-446">888888888</span></span>
- <span data-ttu-id="16264-447">999999999</span><span class="sxs-lookup"><span data-stu-id="16264-447">999999999</span></span>
- <span data-ttu-id="16264-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="16264-448">0000000000</span></span>
- <span data-ttu-id="16264-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="16264-449">1111111111</span></span>
- <span data-ttu-id="16264-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="16264-450">2222222222</span></span>
- <span data-ttu-id="16264-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="16264-451">3333333333</span></span>
- <span data-ttu-id="16264-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="16264-452">4444444444</span></span>
- <span data-ttu-id="16264-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="16264-453">5555555555</span></span>
- <span data-ttu-id="16264-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="16264-454">6666666666</span></span>
- <span data-ttu-id="16264-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="16264-455">7777777777</span></span>
- <span data-ttu-id="16264-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="16264-456">8888888888</span></span>
- <span data-ttu-id="16264-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="16264-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="16264-458">Ключ проверки поДлинности Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="16264-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="16264-459">Format</span><span class="sxs-lookup"><span data-stu-id="16264-459">Format</span></span>

<span data-ttu-id="16264-460">Строка "DocumentDb", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="16264-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-461">Pattern</span></span>

- <span data-ttu-id="16264-462">Строка "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="16264-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="16264-463">Любая комбинация из 3-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-464">Символ "больше" (_Гт_), знак равенства (=), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="16264-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="16264-465">Любая комбинация 86 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="16264-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="16264-466">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="16264-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-467">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-467">Checksum</span></span>

<span data-ttu-id="16264-468">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-469">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-469">Definition</span></span>

<span data-ttu-id="16264-470">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-471">Регулярное выражение Цеп_режекс_азуредокументдбаускэй находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-472">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!-- Azure Document DB Auth Key -->
<Entity id="0f587d92-eb28-44a9-bd1c-90f2892b47aa" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureDocumentDBAuthKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
          </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-473">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-473">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-474">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-475">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-476">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-476">contoso</span></span>
- <span data-ttu-id="16264-477">компании</span><span class="sxs-lookup"><span data-stu-id="16264-477">fabrikam</span></span>
- <span data-ttu-id="16264-478">базу</span><span class="sxs-lookup"><span data-stu-id="16264-478">northwind</span></span>
- <span data-ttu-id="16264-479">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-479">sandbox</span></span>
- <span data-ttu-id="16264-480">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-480">onebox</span></span>
- <span data-ttu-id="16264-481">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-481">localhost</span></span>
- <span data-ttu-id="16264-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-482">127.0.0.1</span></span>
- <span data-ttu-id="16264-483">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-483">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-484">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-484">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="16264-485">Строка подключения к базе данных Azure IAAS и строка подключения к SQL Azure</span><span class="sxs-lookup"><span data-stu-id="16264-485">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="16264-486">Format</span><span class="sxs-lookup"><span data-stu-id="16264-486">Format</span></span>

<span data-ttu-id="16264-487">Строка "Server", "Server" или "Data Source", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "клаудапп. Azure". <!--no-hyperlink-->com "или" клаудапп. Azure. <!--no-hyperlink-->NET "или" Database. Windows. <!--no-hyperlink-->NET ", а также строку" Password "или" Password "или" pwd ".</span><span class="sxs-lookup"><span data-stu-id="16264-487">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.<!--no-hyperlink-->com" or "cloudapp.azure.<!--no-hyperlink-->net" or "database.windows.<!--no-hyperlink-->net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-488">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-488">Pattern</span></span>

- <span data-ttu-id="16264-489">Строка "Server", "Server" или "Data Source"</span><span class="sxs-lookup"><span data-stu-id="16264-489">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="16264-490">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-490">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-491">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-491">An equal sign (=)</span></span>
- <span data-ttu-id="16264-492">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-492">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-493">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-493">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-494">Строка "клаудапп. Azure. <!--no-hyperlink-->com "," клаудапп. Azure. <!--no-hyperlink-->NET "или" Database. Windows. <!--no-hyperlink-->NET "</span><span class="sxs-lookup"><span data-stu-id="16264-494">The string "cloudapp.azure.<!--no-hyperlink-->com", "cloudapp.azure.<!--no-hyperlink-->net", or "database.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="16264-495">Любая комбинация из 1-300 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-495">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-496">Строка "Password", "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="16264-496">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="16264-497">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-498">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-498">An equal sign (=)</span></span>
- <span data-ttu-id="16264-499">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-499">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-500">Один или несколько символов, не отделяющая точку с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="16264-500">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="16264-501">Точка с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="16264-501">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-502">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-502">Checksum</span></span>

<span data-ttu-id="16264-503">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-503">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-504">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-504">Definition</span></span>

<span data-ttu-id="16264-505">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-505">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-506">Регулярное выражение Цеп_режекс_азуреконнектионстринг находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-506">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-507">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-507">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IAAS Database Connection String and Azure SQL Connection String-->
<Entity id="ce1a126d-186f-4700-8c0c-486157b953fd" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-508">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-508">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-509">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-509">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-510">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-510">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-511">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-511">contoso</span></span>
- <span data-ttu-id="16264-512">компании</span><span class="sxs-lookup"><span data-stu-id="16264-512">fabrikam</span></span>
- <span data-ttu-id="16264-513">базу</span><span class="sxs-lookup"><span data-stu-id="16264-513">northwind</span></span>
- <span data-ttu-id="16264-514">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-514">sandbox</span></span>
- <span data-ttu-id="16264-515">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-515">onebox</span></span>
- <span data-ttu-id="16264-516">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-516">localhost</span></span>
- <span data-ttu-id="16264-517">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-517">127.0.0.1</span></span>
- <span data-ttu-id="16264-518">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-518">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-519">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-519">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="16264-520">Строка подключения Azure IoT</span><span class="sxs-lookup"><span data-stu-id="16264-520">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="16264-521">Format</span><span class="sxs-lookup"><span data-stu-id="16264-521">Format</span></span>

<span data-ttu-id="16264-522">Строка "HostName", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, включая строки "Azure — Devices. <!--no-hyperlink-->NET "и" шаредакцесскэй ".</span><span class="sxs-lookup"><span data-stu-id="16264-522">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.<!--no-hyperlink-->net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-523">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-523">Pattern</span></span>

- <span data-ttu-id="16264-524">Строка "HostName"</span><span class="sxs-lookup"><span data-stu-id="16264-524">The string "HostName"</span></span>
- <span data-ttu-id="16264-525">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-525">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-526">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-526">An equal sign (=)</span></span>
- <span data-ttu-id="16264-527">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-527">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-528">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-528">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-529">Строка "Azure — Devices. <!--no-hyperlink-->NET "</span><span class="sxs-lookup"><span data-stu-id="16264-529">The string "azure-devices.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="16264-530">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-530">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-531">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="16264-531">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="16264-532">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-532">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-533">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-533">An equal sign (=)</span></span>
- <span data-ttu-id="16264-534">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-534">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-535">Любая комбинация 43 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="16264-535">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="16264-536">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-536">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-537">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-537">Checksum</span></span>

<span data-ttu-id="16264-538">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-538">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-539">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-539">Definition</span></span>

<span data-ttu-id="16264-540">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-540">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-541">Регулярное выражение Цеп_режекс_азуреиотконнектионстринг находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-541">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-542">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-542">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure IoT Connection String-->
<Entity id="0b34bec3-d5d6-4974-b7b0-dcdb5c90c29d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureIoTConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-543">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-543">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-544">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-544">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-545">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-545">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-546">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-546">contoso</span></span>
- <span data-ttu-id="16264-547">компании</span><span class="sxs-lookup"><span data-stu-id="16264-547">fabrikam</span></span>
- <span data-ttu-id="16264-548">базу</span><span class="sxs-lookup"><span data-stu-id="16264-548">northwind</span></span>
- <span data-ttu-id="16264-549">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-549">sandbox</span></span>
- <span data-ttu-id="16264-550">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-550">onebox</span></span>
- <span data-ttu-id="16264-551">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-551">localhost</span></span>
- <span data-ttu-id="16264-552">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-552">127.0.0.1</span></span>
- <span data-ttu-id="16264-553">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-553">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-554">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-554">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="16264-555">Пароль для параметра публикации Azure</span><span class="sxs-lookup"><span data-stu-id="16264-555">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="16264-556">Format</span><span class="sxs-lookup"><span data-stu-id="16264-556">Format</span></span>

<span data-ttu-id="16264-557">Строка "усерпвд =", за которой следует буквенно-цифровая строка.</span><span class="sxs-lookup"><span data-stu-id="16264-557">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-558">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-558">Pattern</span></span>

- <span data-ttu-id="16264-559">Строка "усерпвд ="</span><span class="sxs-lookup"><span data-stu-id="16264-559">The string "userpwd="</span></span>
- <span data-ttu-id="16264-560">Любая комбинация букв или цифр в нижнем регистре 60</span><span class="sxs-lookup"><span data-stu-id="16264-560">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="16264-561">Знак кавычек (")</span><span class="sxs-lookup"><span data-stu-id="16264-561">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-562">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-562">Checksum</span></span>

<span data-ttu-id="16264-563">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-563">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-564">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-564">Definition</span></span>

<span data-ttu-id="16264-565">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-565">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-566">Регулярное выражение Цеп_режекс_азурепублишсеттингпассвордс находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-566">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-567">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-567">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```
<!--Azure Publish Setting Password-->
<Entity id="75f4cc8a-a68e-49e5-89ce-fa8f03d286a5" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="CEP_Regex_AzurePublishSettingPasswords" />
       <Any minMatches="0" maxMatches="0">
           <Match idRef="CEP_CommonExampleKeywords" />
       </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-568">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-568">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-569">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-569">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-570">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-570">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-571">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-571">contoso</span></span>
- <span data-ttu-id="16264-572">компании</span><span class="sxs-lookup"><span data-stu-id="16264-572">fabrikam</span></span>
- <span data-ttu-id="16264-573">базу</span><span class="sxs-lookup"><span data-stu-id="16264-573">northwind</span></span>
- <span data-ttu-id="16264-574">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-574">sandbox</span></span>
- <span data-ttu-id="16264-575">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-575">onebox</span></span>
- <span data-ttu-id="16264-576">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-576">localhost</span></span>
- <span data-ttu-id="16264-577">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-577">127.0.0.1</span></span>
- <span data-ttu-id="16264-578">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-578">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-579">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-579">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="16264-580">Строка подключения к кэшу Azure Redis</span><span class="sxs-lookup"><span data-stu-id="16264-580">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="16264-581">Format</span><span class="sxs-lookup"><span data-stu-id="16264-581">Format</span></span>

<span data-ttu-id="16264-582">Строка "Redis. Cache. Windows. <!--no-hyperlink-->NET, за которыми следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "Password" или "pwd".</span><span class="sxs-lookup"><span data-stu-id="16264-582">The string "redis.cache.windows.<!--no-hyperlink-->net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-583">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-583">Pattern</span></span>

- <span data-ttu-id="16264-584">Строка "Redis. Cache. Windows. <!--no-hyperlink-->NET "</span><span class="sxs-lookup"><span data-stu-id="16264-584">The string "redis.cache.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="16264-585">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-585">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-586">Строка "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="16264-586">The string "password" or "pwd"</span></span>
- <span data-ttu-id="16264-587">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-587">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-588">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-588">An equal sign (=)</span></span>
- <span data-ttu-id="16264-589">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-589">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-590">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="16264-590">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="16264-591">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-591">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-592">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-592">Checksum</span></span>

<span data-ttu-id="16264-593">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-593">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-594">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-594">Definition</span></span>

<span data-ttu-id="16264-595">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-596">Регулярное выражение Цеп_режекс_азурередискачеконнектионстринг находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="16264-596">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="16264-597">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-597">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Redis Cache Connection String-->
<Entity id="095a7e6c-efd8-46d5-af7b-5298d53a49fc" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureRedisCacheConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-598">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-598">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-599">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-599">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-600">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-600">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-601">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-601">contoso</span></span>
- <span data-ttu-id="16264-602">компании</span><span class="sxs-lookup"><span data-stu-id="16264-602">fabrikam</span></span>
- <span data-ttu-id="16264-603">базу</span><span class="sxs-lookup"><span data-stu-id="16264-603">northwind</span></span>
- <span data-ttu-id="16264-604">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-604">sandbox</span></span>
- <span data-ttu-id="16264-605">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-605">onebox</span></span>
- <span data-ttu-id="16264-606">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-606">localhost</span></span>
- <span data-ttu-id="16264-607">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-607">127.0.0.1</span></span>
- <span data-ttu-id="16264-608">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-608">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-609">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-609">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="16264-610">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="16264-610">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="16264-611">Format</span><span class="sxs-lookup"><span data-stu-id="16264-611">Format</span></span>

<span data-ttu-id="16264-612">Строка "SIG", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="16264-612">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-613">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-613">Pattern</span></span>

- <span data-ttu-id="16264-614">Строка "SIG"</span><span class="sxs-lookup"><span data-stu-id="16264-614">The string "sig"</span></span>
- <span data-ttu-id="16264-615">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-615">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-616">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-616">An equal sign (=)</span></span>
- <span data-ttu-id="16264-617">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-617">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-618">Любое сочетание 43-53 символов, которые являются буквами нижнего или верхнего регистра, цифрами или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="16264-618">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="16264-619">Строка "% 3D"</span><span class="sxs-lookup"><span data-stu-id="16264-619">The string "%3d"</span></span>
- <span data-ttu-id="16264-620">Любой символ, который не является буквой нижнего или верхнего регистра, цифрой или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="16264-620">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-621">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-621">Checksum</span></span>

<span data-ttu-id="16264-622">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-622">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-623">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-623">Definition</span></span>

<span data-ttu-id="16264-624">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-624">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-625">Регулярное выражение Цеп_режекс_азуресас находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-625">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="16264-626">Строка подключения к служебной шине Azure</span><span class="sxs-lookup"><span data-stu-id="16264-626">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="16264-627">Format</span><span class="sxs-lookup"><span data-stu-id="16264-627">Format</span></span>

<span data-ttu-id="16264-628">Строка "EndPoint", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строки "сервицебус. Windows. <!--no-hyperlink-->NET "и" шаредакцескэй ".</span><span class="sxs-lookup"><span data-stu-id="16264-628">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.<!--no-hyperlink-->net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-629">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-629">Pattern</span></span>

- <span data-ttu-id="16264-630">Строка "EndPoint"</span><span class="sxs-lookup"><span data-stu-id="16264-630">The string "EndPoint"</span></span>
- <span data-ttu-id="16264-631">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-631">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-632">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-632">An equal sign (=)</span></span>
- <span data-ttu-id="16264-633">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-633">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-634">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-634">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-635">Строка "сервицебус. Windows. <!--no-hyperlink-->NET "</span><span class="sxs-lookup"><span data-stu-id="16264-635">The string "servicebus.windows.<!--no-hyperlink-->net"</span></span>
- <span data-ttu-id="16264-636">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-636">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-637">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="16264-637">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="16264-638">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-638">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-639">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-639">An equal sign (=)</span></span>
- <span data-ttu-id="16264-640">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-640">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-641">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="16264-641">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="16264-642">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-642">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-643">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-643">Checksum</span></span>

<span data-ttu-id="16264-644">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-644">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-645">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-645">Definition</span></span>

<span data-ttu-id="16264-646">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-646">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-647">Регулярное выражение Цеп_режекс_азуресервицебусконнектионстринг находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="16264-647">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="16264-648">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-648">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Service Bus Connection String-->
<Entity id="b9a6578f-a83f-4fcd-bf44-2130bae49a6f" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureServiceBusConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-649">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-649">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-650">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-650">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-651">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-651">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-652">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-652">contoso</span></span>
- <span data-ttu-id="16264-653">компании</span><span class="sxs-lookup"><span data-stu-id="16264-653">fabrikam</span></span>
- <span data-ttu-id="16264-654">базу</span><span class="sxs-lookup"><span data-stu-id="16264-654">northwind</span></span>
- <span data-ttu-id="16264-655">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-655">sandbox</span></span>
- <span data-ttu-id="16264-656">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-656">onebox</span></span>
- <span data-ttu-id="16264-657">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-657">localhost</span></span>
- <span data-ttu-id="16264-658">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-658">127.0.0.1</span></span>
- <span data-ttu-id="16264-659">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-659">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-660">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-660">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="16264-661">Ключ учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="16264-661">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="16264-662">Format</span><span class="sxs-lookup"><span data-stu-id="16264-662">Format</span></span>

<span data-ttu-id="16264-663">Строка "Дефаултендпоинтспротокол", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "AccountKey".</span><span class="sxs-lookup"><span data-stu-id="16264-663">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-664">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-664">Pattern</span></span>

- <span data-ttu-id="16264-665">Строка "Дефаултендпоинтспротокол"</span><span class="sxs-lookup"><span data-stu-id="16264-665">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="16264-666">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-666">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-667">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-667">An equal sign (=)</span></span>
- <span data-ttu-id="16264-668">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-668">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-669">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-669">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-670">Строка "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="16264-670">The string "AccountKey"</span></span>
- <span data-ttu-id="16264-671">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-671">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-672">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-672">An equal sign (=)</span></span>
- <span data-ttu-id="16264-673">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="16264-673">0-2 whitespace characters</span></span>
- <span data-ttu-id="16264-674">Любое сочетание 86 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="16264-674">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="16264-675">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="16264-675">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-676">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-676">Checksum</span></span>

<span data-ttu-id="16264-677">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-677">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-678">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-678">Definition</span></span>

<span data-ttu-id="16264-679">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-679">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-680">Регулярное выражение Цеп_режекс_азуресторажеаккаунткэй находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-680">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-681">Регулярное выражение Цеп_азуримулаторсторажеаккаунтфилтер не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-681">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="16264-682">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-682">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key-->
<Entity id="c7bc98e8-551a-4c35-a92d-d2c8cda714a7" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKey" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_AzureEmulatorStorageAccountFilter" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-683">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-683">Keywords</span></span>

#### <a name="cepazureemulatorstorageaccountfilter"></a><span data-ttu-id="16264-684">Цеп_азуримулаторсторажеаккаунтфилтер</span><span class="sxs-lookup"><span data-stu-id="16264-684">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="16264-685">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-685">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/Кбхбексогмгв = =</span><span class="sxs-lookup"><span data-stu-id="16264-686">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-687">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-687">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-688">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-688">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-689">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-689">contoso</span></span>
- <span data-ttu-id="16264-690">компании</span><span class="sxs-lookup"><span data-stu-id="16264-690">fabrikam</span></span>
- <span data-ttu-id="16264-691">базу</span><span class="sxs-lookup"><span data-stu-id="16264-691">northwind</span></span>
- <span data-ttu-id="16264-692">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-692">sandbox</span></span>
- <span data-ttu-id="16264-693">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-693">onebox</span></span>
- <span data-ttu-id="16264-694">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-694">localhost</span></span>
- <span data-ttu-id="16264-695">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-695">127.0.0.1</span></span>
- <span data-ttu-id="16264-696">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-696">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-697">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-697">s-int.<!--no-hyperlink-->net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="16264-698">Ключ учетной записи хранилища Azure (общий)</span><span class="sxs-lookup"><span data-stu-id="16264-698">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="16264-699">Format</span><span class="sxs-lookup"><span data-stu-id="16264-699">Format</span></span>

<span data-ttu-id="16264-700">Любая комбинация 86 строчных или прописных букв, цифр, знаков косой черты (/) или знака плюса (+) перед или за ними следуют символы, указанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="16264-700">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-701">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-701">Pattern</span></span>

- <span data-ttu-id="16264-702">0-1 из символа "больше" (_Гт_), апостроф ('), знак равенства (=), знак кавычек (") или решетка (#)</span><span class="sxs-lookup"><span data-stu-id="16264-702">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="16264-703">Любое сочетание 86 символов, которые представляют собой буквы в нижнем или верхнем регистре, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="16264-703">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="16264-704">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="16264-704">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="16264-705">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-705">Checksum</span></span>

<span data-ttu-id="16264-706">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-706">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-707">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-707">Definition</span></span>

<span data-ttu-id="16264-708">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-708">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-709">Регулярное выражение Цеп_режекс_азуресторажеаккаунткэйженерик находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-709">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="16264-710">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="16264-710">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-711">Format</span><span class="sxs-lookup"><span data-stu-id="16264-711">Format</span></span>

<span data-ttu-id="16264-712">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="16264-712">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-713">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-713">Pattern</span></span>

<span data-ttu-id="16264-714">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="16264-714">11 digits plus delimiters:</span></span>
- <span data-ttu-id="16264-715">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="16264-715">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="16264-716">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-716">A hyphen</span></span> 
- <span data-ttu-id="16264-717">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="16264-717">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="16264-718">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-718">A period</span></span> 
- <span data-ttu-id="16264-719">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-719">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-720">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-720">Checksum</span></span>

<span data-ttu-id="16264-721">Да</span><span class="sxs-lookup"><span data-stu-id="16264-721">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-722">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-722">Definition</span></span>

<span data-ttu-id="16264-723">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-723">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-724">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-724">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-725">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="16264-725">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="16264-726">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-726">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-727">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-727">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="16264-728">Кэйворд_белгиум_натионал_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-728">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="16264-729">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="16264-729">Identity</span></span>
- <span data-ttu-id="16264-730">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="16264-730">Registration</span></span>
- <span data-ttu-id="16264-731">Процедура</span><span class="sxs-lookup"><span data-stu-id="16264-731">Identification</span></span> 
- <span data-ttu-id="16264-732">ИД</span><span class="sxs-lookup"><span data-stu-id="16264-732">ID</span></span> 
- <span data-ttu-id="16264-733">Идентитеитскаарт</span><span class="sxs-lookup"><span data-stu-id="16264-733">Identiteitskaart</span></span>
- <span data-ttu-id="16264-734">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="16264-734">Registratie nummer</span></span> 
- <span data-ttu-id="16264-735">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="16264-735">Identificatie nummer</span></span> 
- <span data-ttu-id="16264-736">Идентитеит</span><span class="sxs-lookup"><span data-stu-id="16264-736">Identiteit</span></span>
- <span data-ttu-id="16264-737">Регистратие</span><span class="sxs-lookup"><span data-stu-id="16264-737">Registratie</span></span>
- <span data-ttu-id="16264-738">Идентификатие</span><span class="sxs-lookup"><span data-stu-id="16264-738">Identificatie</span></span> 
- <span data-ttu-id="16264-739">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="16264-739">Carte d’identité</span></span> 
- <span data-ttu-id="16264-740">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="16264-740">numéro d'immatriculation</span></span>
- <span data-ttu-id="16264-741">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="16264-741">numéro d'identification</span></span>
- <span data-ttu-id="16264-742">идентитé</span><span class="sxs-lookup"><span data-stu-id="16264-742">identité</span></span> 
- <span data-ttu-id="16264-743">инскриптион</span><span class="sxs-lookup"><span data-stu-id="16264-743">inscription</span></span> 
- <span data-ttu-id="16264-744">Идентификатион</span><span class="sxs-lookup"><span data-stu-id="16264-744">Identifikation</span></span>
- <span data-ttu-id="16264-745">Идентифизиерунг</span><span class="sxs-lookup"><span data-stu-id="16264-745">Identifizierung</span></span>
- <span data-ttu-id="16264-746">Идентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-746">Identifikationsnummer</span></span>
- <span data-ttu-id="16264-747">Персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="16264-747">Personalausweis</span></span>
- <span data-ttu-id="16264-748">Регистриерунг</span><span class="sxs-lookup"><span data-stu-id="16264-748">Registrierung</span></span>
- <span data-ttu-id="16264-749">Регистратионснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-749">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="16264-750">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="16264-750">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-751">Format</span><span class="sxs-lookup"><span data-stu-id="16264-751">Format</span></span>

<span data-ttu-id="16264-752">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="16264-752">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-753">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-753">Pattern</span></span>

<span data-ttu-id="16264-754">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="16264-754">Formatted:</span></span>
- <span data-ttu-id="16264-755">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-755">Three digits</span></span> 
- <span data-ttu-id="16264-756">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-756">A period</span></span> 
- <span data-ttu-id="16264-757">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-757">Three digits</span></span> 
- <span data-ttu-id="16264-758">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-758">A period</span></span> 
- <span data-ttu-id="16264-759">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-759">Three digits</span></span> 
- <span data-ttu-id="16264-760">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-760">A hyphen</span></span> 
- <span data-ttu-id="16264-761">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-761">Two digits which are check digits</span></span>

<span data-ttu-id="16264-762">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="16264-762">Unformatted:</span></span>
- <span data-ttu-id="16264-763">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="16264-763">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-764">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-764">Checksum</span></span>

<span data-ttu-id="16264-765">Да</span><span class="sxs-lookup"><span data-stu-id="16264-765">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-766">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-766">Definition</span></span>

<span data-ttu-id="16264-767">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-767">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-768">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-768">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-769">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="16264-769">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="16264-770">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-770">The checksum passes.</span></span>

<span data-ttu-id="16264-771">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-772">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-772">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-773">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-773">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-774">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-774">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="16264-775">Кэйворд_бразил_кпф</span><span class="sxs-lookup"><span data-stu-id="16264-775">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="16264-776">CPF</span><span class="sxs-lookup"><span data-stu-id="16264-776">CPF</span></span>
- <span data-ttu-id="16264-777">Процедура</span><span class="sxs-lookup"><span data-stu-id="16264-777">Identification</span></span>
- <span data-ttu-id="16264-778">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="16264-778">Registration</span></span>
- <span data-ttu-id="16264-779">Реализации</span><span class="sxs-lookup"><span data-stu-id="16264-779">Revenue</span></span>
- <span data-ttu-id="16264-780">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="16264-780">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="16264-781">Импосто</span><span class="sxs-lookup"><span data-stu-id="16264-781">Imposto</span></span> 
- <span data-ttu-id="16264-782">Идентификаçãо</span><span class="sxs-lookup"><span data-stu-id="16264-782">Identificação</span></span> 
- <span data-ttu-id="16264-783">Инскриçãо</span><span class="sxs-lookup"><span data-stu-id="16264-783">Inscrição</span></span> 
- <span data-ttu-id="16264-784">Рецеита</span><span class="sxs-lookup"><span data-stu-id="16264-784">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="16264-785">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="16264-785">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="16264-786">Format</span><span class="sxs-lookup"><span data-stu-id="16264-786">Format</span></span>

<span data-ttu-id="16264-787">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="16264-787">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-788">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-788">Pattern</span></span>
<span data-ttu-id="16264-789">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="16264-789">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="16264-790">две цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-790">Two digits</span></span> 
- <span data-ttu-id="16264-791">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-791">A period</span></span> 
- <span data-ttu-id="16264-792">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-792">Three digits</span></span> 
- <span data-ttu-id="16264-793">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-793">A period</span></span> 
- <span data-ttu-id="16264-794">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="16264-794">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="16264-795">косая черта;</span><span class="sxs-lookup"><span data-stu-id="16264-795">A forward slash</span></span> 
- <span data-ttu-id="16264-796">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-796">Four-digit branch number</span></span> 
- <span data-ttu-id="16264-797">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-797">A hyphen</span></span> 
- <span data-ttu-id="16264-798">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-798">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-799">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-799">Checksum</span></span>

<span data-ttu-id="16264-800">Да</span><span class="sxs-lookup"><span data-stu-id="16264-800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-801">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-801">Definition</span></span>

<span data-ttu-id="16264-802">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-803">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-803">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-804">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="16264-804">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="16264-805">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-805">The checksum passes.</span></span>

<span data-ttu-id="16264-806">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-806">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-807">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-807">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-808">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-808">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-809">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-809">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="16264-810">Кэйворд_бразил_кнпж</span><span class="sxs-lookup"><span data-stu-id="16264-810">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="16264-811">CNPJ</span><span class="sxs-lookup"><span data-stu-id="16264-811">CNPJ</span></span> 
- <span data-ttu-id="16264-812">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="16264-812">CNPJ/MF</span></span> 
- <span data-ttu-id="16264-813">CNPJ – MF</span><span class="sxs-lookup"><span data-stu-id="16264-813">CNPJ-MF</span></span> 
- <span data-ttu-id="16264-814">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="16264-814">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="16264-815">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="16264-815">Taxpayers Registry</span></span> 
- <span data-ttu-id="16264-816">Legal entity</span><span class="sxs-lookup"><span data-stu-id="16264-816">Legal entity</span></span> 
- <span data-ttu-id="16264-817">Legal entities</span><span class="sxs-lookup"><span data-stu-id="16264-817">Legal entities</span></span> 
- <span data-ttu-id="16264-818">Registration Status</span><span class="sxs-lookup"><span data-stu-id="16264-818">Registration Status</span></span> 
- <span data-ttu-id="16264-819">Бизнес</span><span class="sxs-lookup"><span data-stu-id="16264-819">Business</span></span> 
- <span data-ttu-id="16264-820">Company</span><span class="sxs-lookup"><span data-stu-id="16264-820">Company</span></span>
- <span data-ttu-id="16264-821">CNPJ</span><span class="sxs-lookup"><span data-stu-id="16264-821">CNPJ</span></span> 
- <span data-ttu-id="16264-822">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="16264-822">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="16264-823">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="16264-823">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="16264-824">КГК</span><span class="sxs-lookup"><span data-stu-id="16264-824">CGC</span></span> 
- <span data-ttu-id="16264-825">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="16264-825">Pessoa jurídica</span></span> 
- <span data-ttu-id="16264-826">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="16264-826">Pessoas jurídicas</span></span> 
- <span data-ttu-id="16264-827">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="16264-827">Situação cadastral</span></span> 
- <span data-ttu-id="16264-828">Инскриçãо</span><span class="sxs-lookup"><span data-stu-id="16264-828">Inscrição</span></span> 
- <span data-ttu-id="16264-829">Емпреса</span><span class="sxs-lookup"><span data-stu-id="16264-829">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="16264-830">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="16264-830">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="16264-831">Format</span><span class="sxs-lookup"><span data-stu-id="16264-831">Format</span></span>

<span data-ttu-id="16264-832">Registro Geral (старый формат): девять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-832">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="16264-833">Registro de identidade (RIC) (новый формат): 11 цифр</span><span class="sxs-lookup"><span data-stu-id="16264-833">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-834">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-834">Pattern</span></span>

<span data-ttu-id="16264-835">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="16264-835">Registro Geral (old format):</span></span>
- <span data-ttu-id="16264-836">две цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-836">Two digits</span></span> 
- <span data-ttu-id="16264-837">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-837">A period</span></span> 
- <span data-ttu-id="16264-838">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-838">Three digits</span></span> 
- <span data-ttu-id="16264-839">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-839">A period</span></span> 
- <span data-ttu-id="16264-840">три цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-840">Three digits</span></span> 
- <span data-ttu-id="16264-841">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-841">A hyphen</span></span> 
- <span data-ttu-id="16264-842">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-842">One digit which is a check digit</span></span>

<span data-ttu-id="16264-843">Registro de identidade (RIC) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="16264-843">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="16264-844">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-844">10 digits</span></span> 
- <span data-ttu-id="16264-845">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-845">A hyphen</span></span> 
- <span data-ttu-id="16264-846">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-846">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-847">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-847">Checksum</span></span>

<span data-ttu-id="16264-848">Да</span><span class="sxs-lookup"><span data-stu-id="16264-848">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-849">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-849">Definition</span></span>

<span data-ttu-id="16264-850">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-850">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-851">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-851">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-852">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="16264-852">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="16264-853">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-853">The checksum passes.</span></span>

<span data-ttu-id="16264-854">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-854">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-855">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-855">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-856">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-857">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-857">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="16264-858">Кэйворд_бразил_рг</span><span class="sxs-lookup"><span data-stu-id="16264-858">Keyword_brazil_rg</span></span>

<span data-ttu-id="16264-859">Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр).</span><span class="sxs-lookup"><span data-stu-id="16264-859">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="16264-860">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="16264-860">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-861">Format</span><span class="sxs-lookup"><span data-stu-id="16264-861">Format</span></span>

<span data-ttu-id="16264-862">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-862">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-863">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-863">Pattern</span></span>

<span data-ttu-id="16264-864">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-864">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="16264-865">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="16264-865">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="16264-866">пять цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-866">Five digits</span></span> 
- <span data-ttu-id="16264-867">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-867">A hyphen</span></span> 
- <span data-ttu-id="16264-868">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="16264-868">Three digits OR</span></span>
- <span data-ttu-id="16264-869">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="16264-869">A zero "0"</span></span> 
- <span data-ttu-id="16264-870">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-870">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-871">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-871">Checksum</span></span>

<span data-ttu-id="16264-872">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-872">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-873">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-873">Definition</span></span>

<span data-ttu-id="16264-874">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-874">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-875">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-875">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-876">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="16264-876">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="16264-877">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-877">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="16264-878">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-878">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-879">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-879">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-880">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="16264-880">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-881">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-881">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="16264-882">Кэйворд_канада_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-882">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="16264-883">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="16264-883">canada savings bonds</span></span>
- <span data-ttu-id="16264-884">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="16264-884">canada revenue agency</span></span>
- <span data-ttu-id="16264-885">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="16264-885">canadian financial institution</span></span>
- <span data-ttu-id="16264-886">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="16264-886">direct deposit form</span></span>
- <span data-ttu-id="16264-887">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="16264-887">canadian citizen</span></span>
- <span data-ttu-id="16264-888">legal representative</span><span class="sxs-lookup"><span data-stu-id="16264-888">legal representative</span></span>
- <span data-ttu-id="16264-889">notary public</span><span class="sxs-lookup"><span data-stu-id="16264-889">notary public</span></span>
- <span data-ttu-id="16264-890">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="16264-890">commissioner for oaths</span></span>
- <span data-ttu-id="16264-891">child care benefit</span><span class="sxs-lookup"><span data-stu-id="16264-891">child care benefit</span></span>
- <span data-ttu-id="16264-892">universal child care</span><span class="sxs-lookup"><span data-stu-id="16264-892">universal child care</span></span>
- <span data-ttu-id="16264-893">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="16264-893">canada child tax benefit</span></span>
- <span data-ttu-id="16264-894">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="16264-894">income tax benefit</span></span>
- <span data-ttu-id="16264-895">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="16264-895">harmonized sales tax</span></span>
- <span data-ttu-id="16264-896">social insurance number</span><span class="sxs-lookup"><span data-stu-id="16264-896">social insurance number</span></span>
- <span data-ttu-id="16264-897">income tax refund</span><span class="sxs-lookup"><span data-stu-id="16264-897">income tax refund</span></span>
- <span data-ttu-id="16264-898">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="16264-898">child tax benefit</span></span>
- <span data-ttu-id="16264-899">territorial payments</span><span class="sxs-lookup"><span data-stu-id="16264-899">territorial payments</span></span>
- <span data-ttu-id="16264-900">institution number</span><span class="sxs-lookup"><span data-stu-id="16264-900">institution number</span></span>
- <span data-ttu-id="16264-901">deposit request</span><span class="sxs-lookup"><span data-stu-id="16264-901">deposit request</span></span>
- <span data-ttu-id="16264-902">banking information</span><span class="sxs-lookup"><span data-stu-id="16264-902">banking information</span></span>
- <span data-ttu-id="16264-903">direct deposit</span><span class="sxs-lookup"><span data-stu-id="16264-903">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="16264-904">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="16264-904">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-905">Format</span><span class="sxs-lookup"><span data-stu-id="16264-905">Format</span></span>

<span data-ttu-id="16264-906">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="16264-906">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-907">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-907">Pattern</span></span>

<span data-ttu-id="16264-908">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="16264-908">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-909">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-909">Checksum</span></span>

<span data-ttu-id="16264-910">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-910">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-911">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-911">Definition</span></span>

<span data-ttu-id="16264-912">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-913">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-913">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-914">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="16264-914">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="16264-915">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="16264-915">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-916">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-916">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="16264-917">Кэйворд_ [провинце_наме] _дриверс_лиценсе_наме</span><span class="sxs-lookup"><span data-stu-id="16264-917">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="16264-918">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="16264-918">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="16264-919">Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="16264-919">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="16264-920">Кэйворд_канада_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-920">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="16264-921">DL</span><span class="sxs-lookup"><span data-stu-id="16264-921">DL</span></span>
- <span data-ttu-id="16264-922">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="16264-922">DLS</span></span>
- <span data-ttu-id="16264-923">КДЛ</span><span class="sxs-lookup"><span data-stu-id="16264-923">CDL</span></span>
- <span data-ttu-id="16264-924">КДЛС</span><span class="sxs-lookup"><span data-stu-id="16264-924">CDLS</span></span>
- <span data-ttu-id="16264-925">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="16264-925">DriverLic</span></span>
- <span data-ttu-id="16264-926">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="16264-926">DriverLics</span></span>
- <span data-ttu-id="16264-927">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-927">DriverLicense</span></span>
- <span data-ttu-id="16264-928">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-928">DriverLicenses</span></span>
- <span data-ttu-id="16264-929">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="16264-929">DriverLicence</span></span>
- <span data-ttu-id="16264-930">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="16264-930">DriverLicences</span></span>
- <span data-ttu-id="16264-931">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="16264-931">Driver Lic</span></span>
- <span data-ttu-id="16264-932">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="16264-932">Driver Lics</span></span>
- <span data-ttu-id="16264-933">Driver License</span><span class="sxs-lookup"><span data-stu-id="16264-933">Driver License</span></span>
- <span data-ttu-id="16264-934">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-934">Driver Licenses</span></span>
- <span data-ttu-id="16264-935">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="16264-935">Driver Licence</span></span>
- <span data-ttu-id="16264-936">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="16264-936">Driver Licences</span></span>
- <span data-ttu-id="16264-937">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="16264-937">DriversLic</span></span>
- <span data-ttu-id="16264-938">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="16264-938">DriversLics</span></span>
- <span data-ttu-id="16264-939">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="16264-939">DriversLicence</span></span>
- <span data-ttu-id="16264-940">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="16264-940">DriversLicences</span></span>
- <span data-ttu-id="16264-941">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-941">DriversLicense</span></span>
- <span data-ttu-id="16264-942">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-942">DriversLicenses</span></span>
- <span data-ttu-id="16264-943">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="16264-943">Drivers Lic</span></span>
- <span data-ttu-id="16264-944">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="16264-944">Drivers Lics</span></span>
- <span data-ttu-id="16264-945">Drivers License</span><span class="sxs-lookup"><span data-stu-id="16264-945">Drivers License</span></span>
- <span data-ttu-id="16264-946">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-946">Drivers Licenses</span></span>
- <span data-ttu-id="16264-947">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="16264-947">Drivers Licence</span></span>
- <span data-ttu-id="16264-948">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="16264-948">Drivers Licences</span></span>
- <span data-ttu-id="16264-949">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="16264-949">Driver'Lic</span></span>
- <span data-ttu-id="16264-950">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="16264-950">Driver'Lics</span></span>
- <span data-ttu-id="16264-951">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="16264-951">Driver'License</span></span>
- <span data-ttu-id="16264-952">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-952">Driver'Licenses</span></span>
- <span data-ttu-id="16264-953">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="16264-953">Driver'Licence</span></span>
- <span data-ttu-id="16264-954">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="16264-954">Driver'Licences</span></span>
- <span data-ttu-id="16264-955">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="16264-955">Driver' Lic</span></span>
- <span data-ttu-id="16264-956">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="16264-956">Driver' Lics</span></span>
- <span data-ttu-id="16264-957">Driver' License</span><span class="sxs-lookup"><span data-stu-id="16264-957">Driver' License</span></span>
- <span data-ttu-id="16264-958">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-958">Driver' Licenses</span></span>
- <span data-ttu-id="16264-959">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="16264-959">Driver' Licence</span></span>
- <span data-ttu-id="16264-960">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="16264-960">Driver' Licences</span></span>
- <span data-ttu-id="16264-961">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="16264-961">Driver'sLic</span></span>
- <span data-ttu-id="16264-962">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="16264-962">Driver'sLics</span></span>
- <span data-ttu-id="16264-963">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-963">Driver'sLicense</span></span>
- <span data-ttu-id="16264-964">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-964">Driver'sLicenses</span></span>
- <span data-ttu-id="16264-965">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="16264-965">Driver'sLicence</span></span>
- <span data-ttu-id="16264-966">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="16264-966">Driver'sLicences</span></span>
- <span data-ttu-id="16264-967">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="16264-967">Driver's Lic</span></span>
- <span data-ttu-id="16264-968">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="16264-968">Driver's Lics</span></span>
- <span data-ttu-id="16264-969">Driver's License</span><span class="sxs-lookup"><span data-stu-id="16264-969">Driver's License</span></span>
- <span data-ttu-id="16264-970">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-970">Driver's Licenses</span></span>
- <span data-ttu-id="16264-971">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="16264-971">Driver's Licence</span></span>
- <span data-ttu-id="16264-972">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="16264-972">Driver's Licences</span></span>
- <span data-ttu-id="16264-973">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="16264-973">Permis de Conduire</span></span>
- <span data-ttu-id="16264-974">id</span><span class="sxs-lookup"><span data-stu-id="16264-974">id</span></span>
- <span data-ttu-id="16264-975">ids</span><span class="sxs-lookup"><span data-stu-id="16264-975">ids</span></span>
- <span data-ttu-id="16264-976">idcard number</span><span class="sxs-lookup"><span data-stu-id="16264-976">idcard number</span></span>
- <span data-ttu-id="16264-977">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="16264-977">idcard numbers</span></span>
- <span data-ttu-id="16264-978">idcard#</span><span class="sxs-lookup"><span data-stu-id="16264-978">idcard #</span></span>
- <span data-ttu-id="16264-979">idcard #s</span><span class="sxs-lookup"><span data-stu-id="16264-979">idcard #s</span></span>
- <span data-ttu-id="16264-980">idcard card</span><span class="sxs-lookup"><span data-stu-id="16264-980">idcard card</span></span>
- <span data-ttu-id="16264-981">idcard cards</span><span class="sxs-lookup"><span data-stu-id="16264-981">idcard cards</span></span>
- <span data-ttu-id="16264-982">идкард</span><span class="sxs-lookup"><span data-stu-id="16264-982">idcard</span></span>
- <span data-ttu-id="16264-983">identification number</span><span class="sxs-lookup"><span data-stu-id="16264-983">identification number</span></span>
- <span data-ttu-id="16264-984">identification numbers</span><span class="sxs-lookup"><span data-stu-id="16264-984">identification numbers</span></span>
- <span data-ttu-id="16264-985">identification #</span><span class="sxs-lookup"><span data-stu-id="16264-985">identification #</span></span>
- <span data-ttu-id="16264-986">identification #s</span><span class="sxs-lookup"><span data-stu-id="16264-986">identification #s</span></span>
- <span data-ttu-id="16264-987">identification card</span><span class="sxs-lookup"><span data-stu-id="16264-987">identification card</span></span>
- <span data-ttu-id="16264-988">identification cards</span><span class="sxs-lookup"><span data-stu-id="16264-988">identification cards</span></span>
- <span data-ttu-id="16264-989">процедура</span><span class="sxs-lookup"><span data-stu-id="16264-989">identification</span></span> 
- <span data-ttu-id="16264-990">DL</span><span class="sxs-lookup"><span data-stu-id="16264-990">DL#</span></span>
- <span data-ttu-id="16264-991">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="16264-991">DLS#</span></span> 
- <span data-ttu-id="16264-992">КДЛ #</span><span class="sxs-lookup"><span data-stu-id="16264-992">CDL#</span></span> 
- <span data-ttu-id="16264-993">КДЛС #</span><span class="sxs-lookup"><span data-stu-id="16264-993">CDLS#</span></span> 
- <span data-ttu-id="16264-994">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="16264-994">DriverLic#</span></span> 
- <span data-ttu-id="16264-995">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="16264-995">DriverLics#</span></span> 
- <span data-ttu-id="16264-996">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-996">DriverLicense#</span></span> 
- <span data-ttu-id="16264-997">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-997">DriverLicenses#</span></span> 
- <span data-ttu-id="16264-998">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="16264-998">DriverLicence#</span></span> 
- <span data-ttu-id="16264-999">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="16264-999">DriverLicences#</span></span> 
- <span data-ttu-id="16264-1000">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-1000">Driver Lic#</span></span>
- <span data-ttu-id="16264-1001">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-1001">Driver Lics#</span></span> 
- <span data-ttu-id="16264-1002">Driver License#</span><span class="sxs-lookup"><span data-stu-id="16264-1002">Driver License#</span></span> 
- <span data-ttu-id="16264-1003">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-1003">Driver Licenses#</span></span> 
- <span data-ttu-id="16264-1004">Driver License#</span><span class="sxs-lookup"><span data-stu-id="16264-1004">Driver License#</span></span> 
- <span data-ttu-id="16264-1005">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-1005">Driver Licences#</span></span> 
- <span data-ttu-id="16264-1006">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="16264-1006">DriversLic#</span></span> 
- <span data-ttu-id="16264-1007">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="16264-1007">DriversLics#</span></span> 
- <span data-ttu-id="16264-1008">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-1008">DriversLicense#</span></span> 
- <span data-ttu-id="16264-1009">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-1009">DriversLicenses#</span></span> 
- <span data-ttu-id="16264-1010">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="16264-1010">DriversLicence#</span></span> 
- <span data-ttu-id="16264-1011">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="16264-1011">DriversLicences#</span></span> 
- <span data-ttu-id="16264-1012">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-1012">Drivers Lic#</span></span> 
- <span data-ttu-id="16264-1013">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-1013">Drivers Lics#</span></span> 
- <span data-ttu-id="16264-1014">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="16264-1014">Drivers License#</span></span> 
- <span data-ttu-id="16264-1015">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-1015">Drivers Licenses#</span></span> 
- <span data-ttu-id="16264-1016">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-1016">Drivers Licence#</span></span> 
- <span data-ttu-id="16264-1017">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-1017">Drivers Licences#</span></span> 
- <span data-ttu-id="16264-1018">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="16264-1018">Driver'Lic#</span></span> 
- <span data-ttu-id="16264-1019">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="16264-1019">Driver'Lics#</span></span> 
- <span data-ttu-id="16264-1020">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="16264-1020">Driver'License#</span></span> 
- <span data-ttu-id="16264-1021">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-1021">Driver'Licenses#</span></span> 
- <span data-ttu-id="16264-1022">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="16264-1022">Driver'Licence#</span></span> 
- <span data-ttu-id="16264-1023">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="16264-1023">Driver'Licences#</span></span> 
- <span data-ttu-id="16264-1024">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-1024">Driver' Lic#</span></span> 
- <span data-ttu-id="16264-1025">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-1025">Driver' Lics#</span></span> 
- <span data-ttu-id="16264-1026">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="16264-1026">Driver' License#</span></span> 
- <span data-ttu-id="16264-1027">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-1027">Driver' Licenses#</span></span> 
- <span data-ttu-id="16264-1028">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-1028">Driver' Licence#</span></span> 
- <span data-ttu-id="16264-1029">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-1029">Driver' Licences#</span></span> 
- <span data-ttu-id="16264-1030">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="16264-1030">Driver'sLic#</span></span> 
- <span data-ttu-id="16264-1031">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="16264-1031">Driver'sLics#</span></span> 
- <span data-ttu-id="16264-1032">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-1032">Driver'sLicense#</span></span> 
- <span data-ttu-id="16264-1033">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-1033">Driver'sLicenses#</span></span> 
- <span data-ttu-id="16264-1034">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="16264-1034">Driver'sLicence#</span></span> 
- <span data-ttu-id="16264-1035">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="16264-1035">Driver'sLicences#</span></span> 
- <span data-ttu-id="16264-1036">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-1036">Driver's Lic#</span></span> 
- <span data-ttu-id="16264-1037">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-1037">Driver's Lics#</span></span> 
- <span data-ttu-id="16264-1038">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="16264-1038">Driver's License#</span></span> 
- <span data-ttu-id="16264-1039">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-1039">Driver's Licenses#</span></span> 
- <span data-ttu-id="16264-1040">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="16264-1040">Driver's Licence#</span></span> 
- <span data-ttu-id="16264-1041">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="16264-1041">Driver's Licences#</span></span> 
- <span data-ttu-id="16264-1042">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="16264-1042">Permis de Conduire#</span></span> 
- <span data-ttu-id="16264-1043">кодов</span><span class="sxs-lookup"><span data-stu-id="16264-1043">id#</span></span> 
- <span data-ttu-id="16264-1044">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="16264-1044">ids#</span></span> 
- <span data-ttu-id="16264-1045">idcard card#</span><span class="sxs-lookup"><span data-stu-id="16264-1045">idcard card#</span></span> 
- <span data-ttu-id="16264-1046">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="16264-1046">idcard cards#</span></span> 
- <span data-ttu-id="16264-1047">идкард #</span><span class="sxs-lookup"><span data-stu-id="16264-1047">idcard#</span></span> 
- <span data-ttu-id="16264-1048">identification card#</span><span class="sxs-lookup"><span data-stu-id="16264-1048">identification card#</span></span> 
- <span data-ttu-id="16264-1049">identification cards#</span><span class="sxs-lookup"><span data-stu-id="16264-1049">identification cards#</span></span> 
- <span data-ttu-id="16264-1050">процедура</span><span class="sxs-lookup"><span data-stu-id="16264-1050">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="16264-1051">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="16264-1051">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1052">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1052">Format</span></span>

<span data-ttu-id="16264-1053">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1053">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1054">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1054">Pattern</span></span>

<span data-ttu-id="16264-1055">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1055">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1056">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1056">Checksum</span></span>

<span data-ttu-id="16264-1057">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1057">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1058">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1058">Definition</span></span>

<span data-ttu-id="16264-1059">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1059">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1060">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1060">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1061">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="16264-1061">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1062">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1062">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="16264-1063">Кэйворд_канада_хеалс_сервице_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-1063">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="16264-1064">personal health number</span><span class="sxs-lookup"><span data-stu-id="16264-1064">personal health number</span></span>
- <span data-ttu-id="16264-1065">patient information</span><span class="sxs-lookup"><span data-stu-id="16264-1065">patient information</span></span>
- <span data-ttu-id="16264-1066">health services</span><span class="sxs-lookup"><span data-stu-id="16264-1066">health services</span></span>
- <span data-ttu-id="16264-1067">speciality services</span><span class="sxs-lookup"><span data-stu-id="16264-1067">speciality services</span></span>
- <span data-ttu-id="16264-1068">automobile accident</span><span class="sxs-lookup"><span data-stu-id="16264-1068">automobile accident</span></span>
- <span data-ttu-id="16264-1069">patient hospital</span><span class="sxs-lookup"><span data-stu-id="16264-1069">patient hospital</span></span>
- <span data-ttu-id="16264-1070">псичиатрист</span><span class="sxs-lookup"><span data-stu-id="16264-1070">psychiatrist</span></span>
- <span data-ttu-id="16264-1071">workers compensation</span><span class="sxs-lookup"><span data-stu-id="16264-1071">workers compensation</span></span>
- <span data-ttu-id="16264-1072">ограничен</span><span class="sxs-lookup"><span data-stu-id="16264-1072">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="16264-1073">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="16264-1073">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1074">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1074">Format</span></span>

<span data-ttu-id="16264-1075">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1075">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1076">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1076">Pattern</span></span>

<span data-ttu-id="16264-1077">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1077">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1078">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1078">Checksum</span></span>

<span data-ttu-id="16264-1079">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1079">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1080">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1080">Definition</span></span>

<span data-ttu-id="16264-1081">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1081">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1082">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1082">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1083">Найдено ключевое слово из Кэйворд_канада_пасспорт_нумбер или Кэйворд_пасспорт.</span><span class="sxs-lookup"><span data-stu-id="16264-1083">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1084">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1084">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="16264-1085">Кэйворд_канада_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-1085">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="16264-1086">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="16264-1086">canadian citizenship</span></span>
- <span data-ttu-id="16264-1087">canadian passport</span><span class="sxs-lookup"><span data-stu-id="16264-1087">canadian passport</span></span>
- <span data-ttu-id="16264-1088">passport application</span><span class="sxs-lookup"><span data-stu-id="16264-1088">passport application</span></span>
- <span data-ttu-id="16264-1089">passport photos</span><span class="sxs-lookup"><span data-stu-id="16264-1089">passport photos</span></span>
- <span data-ttu-id="16264-1090">certified translator</span><span class="sxs-lookup"><span data-stu-id="16264-1090">certified translator</span></span>
- <span data-ttu-id="16264-1091">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="16264-1091">canadian citizens</span></span>
- <span data-ttu-id="16264-1092">processing times</span><span class="sxs-lookup"><span data-stu-id="16264-1092">processing times</span></span>
- <span data-ttu-id="16264-1093">renewal application</span><span class="sxs-lookup"><span data-stu-id="16264-1093">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="16264-1094">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-1094">Keyword_passport</span></span>

- <span data-ttu-id="16264-1095">Passport Number</span><span class="sxs-lookup"><span data-stu-id="16264-1095">Passport Number</span></span>
- <span data-ttu-id="16264-1096">Passport No</span><span class="sxs-lookup"><span data-stu-id="16264-1096">Passport No</span></span>
- <span data-ttu-id="16264-1097">Passport#</span><span class="sxs-lookup"><span data-stu-id="16264-1097">Passport #</span></span>
- <span data-ttu-id="16264-1098">Службу</span><span class="sxs-lookup"><span data-stu-id="16264-1098">Passport#</span></span>
- <span data-ttu-id="16264-1099">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="16264-1099">PassportID</span></span>
- <span data-ttu-id="16264-1100">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="16264-1100">Passportno</span></span>
- <span data-ttu-id="16264-1101">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-1101">passportnumber</span></span>
- <span data-ttu-id="16264-1102">パスポート</span><span class="sxs-lookup"><span data-stu-id="16264-1102">パスポート</span></span>
- <span data-ttu-id="16264-1103">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="16264-1103">パスポート番号</span></span>
- <span data-ttu-id="16264-1104">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="16264-1104">パスポートのNum</span></span>
- <span data-ttu-id="16264-1105">パスポート #</span><span class="sxs-lookup"><span data-stu-id="16264-1105">パスポート＃</span></span>
- <span data-ttu-id="16264-1106">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="16264-1106">Numéro de passeport</span></span>
- <span data-ttu-id="16264-1107">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="16264-1107">Passeport n °</span></span>
- <span data-ttu-id="16264-1108">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="16264-1108">Passeport Non</span></span>
- <span data-ttu-id="16264-1109">Passeport#</span><span class="sxs-lookup"><span data-stu-id="16264-1109">Passeport #</span></span>
- <span data-ttu-id="16264-1110">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="16264-1110">Passeport#</span></span>
- <span data-ttu-id="16264-1111">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="16264-1111">PasseportNon</span></span>
- <span data-ttu-id="16264-1112">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="16264-1112">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="16264-1113">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="16264-1113">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-1114">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1114">Format</span></span>

<span data-ttu-id="16264-1115">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1115">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1116">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1116">Pattern</span></span>

<span data-ttu-id="16264-1117">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1117">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1118">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1118">Checksum</span></span>

<span data-ttu-id="16264-1119">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1119">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1120">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1120">Definition</span></span>

<span data-ttu-id="16264-1121">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_канада_фин находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1121">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-1122">Найдены по крайней мере два ключевых слова от Кэйворд_канада_фин или Кэйворд_канада_провинцес.</span><span class="sxs-lookup"><span data-stu-id="16264-1122">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1123">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1123">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="16264-1124">Кэйворд_канада_фин</span><span class="sxs-lookup"><span data-stu-id="16264-1124">Keyword_canada_phin</span></span>

- <span data-ttu-id="16264-1125">social insurance number</span><span class="sxs-lookup"><span data-stu-id="16264-1125">social insurance number</span></span>
- <span data-ttu-id="16264-1126">health information act</span><span class="sxs-lookup"><span data-stu-id="16264-1126">health information act</span></span>
- <span data-ttu-id="16264-1127">income tax information</span><span class="sxs-lookup"><span data-stu-id="16264-1127">income tax information</span></span>
- <span data-ttu-id="16264-1128">manitoba health</span><span class="sxs-lookup"><span data-stu-id="16264-1128">manitoba health</span></span>
- <span data-ttu-id="16264-1129">health registration</span><span class="sxs-lookup"><span data-stu-id="16264-1129">health registration</span></span>
- <span data-ttu-id="16264-1130">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="16264-1130">prescription purchases</span></span>
- <span data-ttu-id="16264-1131">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="16264-1131">benefit eligibility</span></span>
- <span data-ttu-id="16264-1132">personal health</span><span class="sxs-lookup"><span data-stu-id="16264-1132">personal health</span></span>
- <span data-ttu-id="16264-1133">power of attorney</span><span class="sxs-lookup"><span data-stu-id="16264-1133">power of attorney</span></span>
- <span data-ttu-id="16264-1134">registration number</span><span class="sxs-lookup"><span data-stu-id="16264-1134">registration number</span></span>
- <span data-ttu-id="16264-1135">personal health number</span><span class="sxs-lookup"><span data-stu-id="16264-1135">personal health number</span></span>
- <span data-ttu-id="16264-1136">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="16264-1136">practitioner referral</span></span>
- <span data-ttu-id="16264-1137">wellness professional</span><span class="sxs-lookup"><span data-stu-id="16264-1137">wellness professional</span></span>
- <span data-ttu-id="16264-1138">patient referral</span><span class="sxs-lookup"><span data-stu-id="16264-1138">patient referral</span></span>
- <span data-ttu-id="16264-1139">health and wellness</span><span class="sxs-lookup"><span data-stu-id="16264-1139">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="16264-1140">Кэйворд_канада_провинцес</span><span class="sxs-lookup"><span data-stu-id="16264-1140">Keyword_canada_provinces</span></span>

- <span data-ttu-id="16264-1141">Нунавут</span><span class="sxs-lookup"><span data-stu-id="16264-1141">Nunavut</span></span>
- <span data-ttu-id="16264-1142">Квебека</span><span class="sxs-lookup"><span data-stu-id="16264-1142">Quebec</span></span>
- <span data-ttu-id="16264-1143">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="16264-1143">Northwest Territories</span></span>
- <span data-ttu-id="16264-1144">Онтарио</span><span class="sxs-lookup"><span data-stu-id="16264-1144">Ontario</span></span>
- <span data-ttu-id="16264-1145">British Columbia</span><span class="sxs-lookup"><span data-stu-id="16264-1145">British Columbia</span></span>
- <span data-ttu-id="16264-1146">Альберта</span><span class="sxs-lookup"><span data-stu-id="16264-1146">Alberta</span></span>
- <span data-ttu-id="16264-1147">Саскачеван</span><span class="sxs-lookup"><span data-stu-id="16264-1147">Saskatchewan</span></span>
- <span data-ttu-id="16264-1148">Манитоба</span><span class="sxs-lookup"><span data-stu-id="16264-1148">Manitoba</span></span>
- <span data-ttu-id="16264-1149">Yukon</span><span class="sxs-lookup"><span data-stu-id="16264-1149">Yukon</span></span>
- <span data-ttu-id="16264-1150">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="16264-1150">Newfoundland and Labrador</span></span>
- <span data-ttu-id="16264-1151">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="16264-1151">New Brunswick</span></span>
- <span data-ttu-id="16264-1152">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="16264-1152">Nova Scotia</span></span>
- <span data-ttu-id="16264-1153">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="16264-1153">Prince Edward Island</span></span>
- <span data-ttu-id="16264-1154">Канада</span><span class="sxs-lookup"><span data-stu-id="16264-1154">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="16264-1155">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="16264-1155">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1156">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1156">Format</span></span>

<span data-ttu-id="16264-1157">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="16264-1157">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1158">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1158">Pattern</span></span>

<span data-ttu-id="16264-1159">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="16264-1159">Formatted:</span></span>
- <span data-ttu-id="16264-1160">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-1160">Three digits</span></span> 
- <span data-ttu-id="16264-1161">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="16264-1161">A hyphen or space</span></span> 
- <span data-ttu-id="16264-1162">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-1162">Three digits</span></span> 
- <span data-ttu-id="16264-1163">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="16264-1163">A hyphen or space</span></span> 
- <span data-ttu-id="16264-1164">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-1164">Three digits</span></span>

<span data-ttu-id="16264-1165">Неформатированные: девять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-1165">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1166">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1166">Checksum</span></span>

<span data-ttu-id="16264-1167">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1167">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1168">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1168">Definition</span></span>

<span data-ttu-id="16264-1169">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1169">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1170">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1170">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1171">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="16264-1171">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="16264-1172">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="16264-1172">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="16264-1173">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="16264-1173">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="16264-1174">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-1174">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="16264-1175">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1175">The checksum passes.</span></span>

<span data-ttu-id="16264-1176">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1177">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1177">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1178">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="16264-1178">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="16264-1179">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1179">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1180">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1180">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="16264-1181">Кэйворд_син</span><span class="sxs-lookup"><span data-stu-id="16264-1181">Keyword_sin</span></span>

- <span data-ttu-id="16264-1182">sin</span><span class="sxs-lookup"><span data-stu-id="16264-1182">sin</span></span> 
- <span data-ttu-id="16264-1183">social insurance</span><span class="sxs-lookup"><span data-stu-id="16264-1183">social insurance</span></span> 
- <span data-ttu-id="16264-1184">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="16264-1184">numero d'assurance sociale</span></span> 
- <span data-ttu-id="16264-1185">грехов</span><span class="sxs-lookup"><span data-stu-id="16264-1185">sins</span></span> 
- <span data-ttu-id="16264-1186">SSN</span><span class="sxs-lookup"><span data-stu-id="16264-1186">ssn</span></span> 
- <span data-ttu-id="16264-1187">ssNS</span><span class="sxs-lookup"><span data-stu-id="16264-1187">ssns</span></span> 
- <span data-ttu-id="16264-1188">social security</span><span class="sxs-lookup"><span data-stu-id="16264-1188">social security</span></span> 
- <span data-ttu-id="16264-1189">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="16264-1189">numero d'assurance social</span></span> 
- <span data-ttu-id="16264-1190">national identification number</span><span class="sxs-lookup"><span data-stu-id="16264-1190">national identification number</span></span> 
- <span data-ttu-id="16264-1191">national id</span><span class="sxs-lookup"><span data-stu-id="16264-1191">national id</span></span> 
- <span data-ttu-id="16264-1192">Синус</span><span class="sxs-lookup"><span data-stu-id="16264-1192">sin#</span></span> 
- <span data-ttu-id="16264-1193">soc ins</span><span class="sxs-lookup"><span data-stu-id="16264-1193">soc ins</span></span> 
- <span data-ttu-id="16264-1194">social ins</span><span class="sxs-lookup"><span data-stu-id="16264-1194">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="16264-1195">Кэйворд_син_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="16264-1195">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="16264-1196">driver's license</span><span class="sxs-lookup"><span data-stu-id="16264-1196">driver's license</span></span> 
- <span data-ttu-id="16264-1197">drivers license</span><span class="sxs-lookup"><span data-stu-id="16264-1197">drivers license</span></span> 
- <span data-ttu-id="16264-1198">driver's licence</span><span class="sxs-lookup"><span data-stu-id="16264-1198">driver's licence</span></span> 
- <span data-ttu-id="16264-1199">drivers licence</span><span class="sxs-lookup"><span data-stu-id="16264-1199">drivers licence</span></span> 
- <span data-ttu-id="16264-1200">ДОБ</span><span class="sxs-lookup"><span data-stu-id="16264-1200">DOB</span></span> 
- <span data-ttu-id="16264-1201">Birthdate</span><span class="sxs-lookup"><span data-stu-id="16264-1201">Birthdate</span></span> 
- <span data-ttu-id="16264-1202">День рождения</span><span class="sxs-lookup"><span data-stu-id="16264-1202">Birthday</span></span> 
- <span data-ttu-id="16264-1203">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="16264-1203">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="16264-1204">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="16264-1204">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1205">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1205">Format</span></span>

<span data-ttu-id="16264-1206">7-8 цифр и разделители — контрольная цифра или буква</span><span class="sxs-lookup"><span data-stu-id="16264-1206">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1207">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1207">Pattern</span></span>

<span data-ttu-id="16264-1208">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="16264-1208">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="16264-1209">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-1209">1-2 digits</span></span> 
- <span data-ttu-id="16264-1210">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-1210">A period</span></span> 
- <span data-ttu-id="16264-1211">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-1211">Three digits</span></span> 
- <span data-ttu-id="16264-1212">точка;</span><span class="sxs-lookup"><span data-stu-id="16264-1212">A period</span></span> 
- <span data-ttu-id="16264-1213">три цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-1213">Three digits</span></span> 
- <span data-ttu-id="16264-1214">тире;</span><span class="sxs-lookup"><span data-stu-id="16264-1214">A dash</span></span> 
- <span data-ttu-id="16264-1215">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-1215">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1216">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1216">Checksum</span></span>

<span data-ttu-id="16264-1217">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1217">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1218">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1218">Definition</span></span>

<span data-ttu-id="16264-1219">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1219">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1220">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1220">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1221">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="16264-1221">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="16264-1222">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1222">The checksum passes.</span></span>

<span data-ttu-id="16264-1223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1224">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1224">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1225">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1225">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1226">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1226">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="16264-1227">Кэйворд_чиле_ид_кард</span><span class="sxs-lookup"><span data-stu-id="16264-1227">Keyword_chile_id_card</span></span>

- <span data-ttu-id="16264-1228">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="16264-1228">National Identification Number</span></span> 
- <span data-ttu-id="16264-1229">Identity card</span><span class="sxs-lookup"><span data-stu-id="16264-1229">Identity card</span></span> 
- <span data-ttu-id="16264-1230">ИД</span><span class="sxs-lookup"><span data-stu-id="16264-1230">ID</span></span> 
- <span data-ttu-id="16264-1231">Процедура</span><span class="sxs-lookup"><span data-stu-id="16264-1231">Identification</span></span> 
- <span data-ttu-id="16264-1232">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="16264-1232">Rol Único Nacional</span></span> 
- <span data-ttu-id="16264-1233">ВЫПОЛНЯЕМ</span><span class="sxs-lookup"><span data-stu-id="16264-1233">RUN</span></span> 
- <span data-ttu-id="16264-1234">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="16264-1234">Rol Único Tributario</span></span> 
- <span data-ttu-id="16264-1235">СНИЖАТЬСЯ</span><span class="sxs-lookup"><span data-stu-id="16264-1235">RUT</span></span> 
- <span data-ttu-id="16264-1236">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="16264-1236">Cédula de Identidad</span></span> 
- <span data-ttu-id="16264-1237">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="16264-1237">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="16264-1238">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="16264-1238">Tarjeta de identificación</span></span> 
- <span data-ttu-id="16264-1239">ИдентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="16264-1239">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="16264-1240">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="16264-1240">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1241">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1241">Format</span></span>

<span data-ttu-id="16264-1242">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1242">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1243">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1243">Pattern</span></span>

<span data-ttu-id="16264-1244">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-1244">18 digits:</span></span>
- <span data-ttu-id="16264-1245">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="16264-1245">Six digits which are an address code</span></span> 
- <span data-ttu-id="16264-1246">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="16264-1246">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="16264-1247">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="16264-1247">Three digits which are an order code</span></span> 
- <span data-ttu-id="16264-1248">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-1248">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1249">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1249">Checksum</span></span>

<span data-ttu-id="16264-1250">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1250">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1251">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1251">Definition</span></span>

<span data-ttu-id="16264-1252">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1252">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1253">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1253">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1254">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="16264-1254">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="16264-1255">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1255">The checksum passes.</span></span>

<span data-ttu-id="16264-1256">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1256">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1257">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1257">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1258">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1258">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1259">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1259">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="16264-1260">Кэйворд_чина_ресидент_ид</span><span class="sxs-lookup"><span data-stu-id="16264-1260">Keyword_china_resident_id</span></span>

- <span data-ttu-id="16264-1261">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="16264-1261">Resident Identity Card</span></span> 
- <span data-ttu-id="16264-1262">NO7</span><span class="sxs-lookup"><span data-stu-id="16264-1262">PRC</span></span> 
- <span data-ttu-id="16264-1263">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="16264-1263">National Identification Card</span></span> 
- <span data-ttu-id="16264-1264">身份证</span><span class="sxs-lookup"><span data-stu-id="16264-1264">身份证</span></span> 
- <span data-ttu-id="16264-1265">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="16264-1265">居民 身份证</span></span> 
- <span data-ttu-id="16264-1266">居民身份证</span><span class="sxs-lookup"><span data-stu-id="16264-1266">居民身份证</span></span> 
- <span data-ttu-id="16264-1267">鉴定</span><span class="sxs-lookup"><span data-stu-id="16264-1267">鉴定</span></span> 
- <span data-ttu-id="16264-1268">身分證</span><span class="sxs-lookup"><span data-stu-id="16264-1268">身分證</span></span> 
- <span data-ttu-id="16264-1269">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="16264-1269">居民 身份證</span></span>
- <span data-ttu-id="16264-1270">鑑定</span><span class="sxs-lookup"><span data-stu-id="16264-1270">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="16264-1271">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="16264-1271">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1272">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1272">Format</span></span>

<span data-ttu-id="16264-1273">16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.</span><span class="sxs-lookup"><span data-stu-id="16264-1273">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1274">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1274">Pattern</span></span>

<span data-ttu-id="16264-1275">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="16264-1275">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1276">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1276">Checksum</span></span>

<span data-ttu-id="16264-1277">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="16264-1277">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1278">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1278">Definition</span></span>

<span data-ttu-id="16264-1279">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1279">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1280">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1280">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1281">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-1281">One of the following is true:</span></span>
    - <span data-ttu-id="16264-1282">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="16264-1282">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="16264-1283">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="16264-1283">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="16264-1284">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-1284">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="16264-1285">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1285">The checksum passes.</span></span>

<span data-ttu-id="16264-1286">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1286">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1287">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1287">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1288">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1288">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1289">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1289">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="16264-1290">Кэйворд_кк_верификатион</span><span class="sxs-lookup"><span data-stu-id="16264-1290">Keyword_cc_verification</span></span>

- <span data-ttu-id="16264-1291">card verification</span><span class="sxs-lookup"><span data-stu-id="16264-1291">card verification</span></span>
- <span data-ttu-id="16264-1292">card identification number</span><span class="sxs-lookup"><span data-stu-id="16264-1292">card identification number</span></span>
- <span data-ttu-id="16264-1293">КВН</span><span class="sxs-lookup"><span data-stu-id="16264-1293">cvn</span></span>
- <span data-ttu-id="16264-1294">cid</span><span class="sxs-lookup"><span data-stu-id="16264-1294">cid</span></span>
- <span data-ttu-id="16264-1295">CVC2</span><span class="sxs-lookup"><span data-stu-id="16264-1295">cvc2</span></span>
- <span data-ttu-id="16264-1296">CVV2</span><span class="sxs-lookup"><span data-stu-id="16264-1296">cvv2</span></span>
- <span data-ttu-id="16264-1297">pin block</span><span class="sxs-lookup"><span data-stu-id="16264-1297">pin block</span></span>
- <span data-ttu-id="16264-1298">security code</span><span class="sxs-lookup"><span data-stu-id="16264-1298">security code</span></span>
- <span data-ttu-id="16264-1299">security number</span><span class="sxs-lookup"><span data-stu-id="16264-1299">security number</span></span>
- <span data-ttu-id="16264-1300">security no</span><span class="sxs-lookup"><span data-stu-id="16264-1300">security no</span></span>
- <span data-ttu-id="16264-1301">issue number</span><span class="sxs-lookup"><span data-stu-id="16264-1301">issue number</span></span>
- <span data-ttu-id="16264-1302">issue no</span><span class="sxs-lookup"><span data-stu-id="16264-1302">issue no</span></span>
- <span data-ttu-id="16264-1303">криптограмме</span><span class="sxs-lookup"><span data-stu-id="16264-1303">cryptogramme</span></span>
- <span data-ttu-id="16264-1304">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="16264-1304">numéro de sécurité</span></span>
- <span data-ttu-id="16264-1305">numero de securite</span><span class="sxs-lookup"><span data-stu-id="16264-1305">numero de securite</span></span>
- <span data-ttu-id="16264-1306">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1306">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="16264-1307">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1307">kreditkartenprufnummer</span></span>
- <span data-ttu-id="16264-1308">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="16264-1308">prüfziffer</span></span>
- <span data-ttu-id="16264-1309">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="16264-1309">prufziffer</span></span>
- <span data-ttu-id="16264-1310">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="16264-1310">sicherheits Kode</span></span>
- <span data-ttu-id="16264-1311">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="16264-1311">sicherheitscode</span></span>
- <span data-ttu-id="16264-1312">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1312">sicherheitsnummer</span></span>
- <span data-ttu-id="16264-1313">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1313">verfalldatum</span></span>
- <span data-ttu-id="16264-1314">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="16264-1314">codice di verifica</span></span>
- <span data-ttu-id="16264-1315">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1315">cod.</span></span> <span data-ttu-id="16264-1316">сикурезза</span><span class="sxs-lookup"><span data-stu-id="16264-1316">sicurezza</span></span>
- <span data-ttu-id="16264-1317">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="16264-1317">cod sicurezza</span></span>
- <span data-ttu-id="16264-1318">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="16264-1318">n autorizzazione</span></span>
- <span data-ttu-id="16264-1319">кóдиго</span><span class="sxs-lookup"><span data-stu-id="16264-1319">código</span></span>
- <span data-ttu-id="16264-1320">кодиго</span><span class="sxs-lookup"><span data-stu-id="16264-1320">codigo</span></span>
- <span data-ttu-id="16264-1321">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1321">cod.</span></span> <span data-ttu-id="16264-1322">СЕГ</span><span class="sxs-lookup"><span data-stu-id="16264-1322">seg</span></span>
- <span data-ttu-id="16264-1323">cod seg</span><span class="sxs-lookup"><span data-stu-id="16264-1323">cod seg</span></span>
- <span data-ttu-id="16264-1324">código de segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1324">código de segurança</span></span>
- <span data-ttu-id="16264-1325">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1325">codigo de seguranca</span></span>
- <span data-ttu-id="16264-1326">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1326">codigo de segurança</span></span>
- <span data-ttu-id="16264-1327">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1327">código de seguranca</span></span>
- <span data-ttu-id="16264-1328">кóд.</span><span class="sxs-lookup"><span data-stu-id="16264-1328">cód.</span></span> <span data-ttu-id="16264-1329">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="16264-1329">segurança</span></span>
- <span data-ttu-id="16264-1330">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1330">cod.</span></span> <span data-ttu-id="16264-1331">сегуранка наложенный платеж.</span><span class="sxs-lookup"><span data-stu-id="16264-1331">seguranca cod.</span></span> <span data-ttu-id="16264-1332">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="16264-1332">segurança</span></span>
- <span data-ttu-id="16264-1333">кóд.</span><span class="sxs-lookup"><span data-stu-id="16264-1333">cód.</span></span> <span data-ttu-id="16264-1334">сегуранка</span><span class="sxs-lookup"><span data-stu-id="16264-1334">seguranca</span></span>
- <span data-ttu-id="16264-1335">cód segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1335">cód segurança</span></span>
- <span data-ttu-id="16264-1336">наложенный на наложенный сегуранка сегуранçа</span><span class="sxs-lookup"><span data-stu-id="16264-1336">cod seguranca cod segurança</span></span>
- <span data-ttu-id="16264-1337">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1337">cód seguranca</span></span>
- <span data-ttu-id="16264-1338">número de verificação</span><span class="sxs-lookup"><span data-stu-id="16264-1338">número de verificação</span></span>
- <span data-ttu-id="16264-1339">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="16264-1339">numero de verificacao</span></span>
- <span data-ttu-id="16264-1340">аблауф</span><span class="sxs-lookup"><span data-stu-id="16264-1340">ablauf</span></span>
- <span data-ttu-id="16264-1341">gültig bis</span><span class="sxs-lookup"><span data-stu-id="16264-1341">gültig bis</span></span>
- <span data-ttu-id="16264-1342">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1342">gültigkeitsdatum</span></span>
- <span data-ttu-id="16264-1343">gultig bis</span><span class="sxs-lookup"><span data-stu-id="16264-1343">gultig bis</span></span>
- <span data-ttu-id="16264-1344">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1344">gultigkeitsdatum</span></span>
- <span data-ttu-id="16264-1345">скаденза</span><span class="sxs-lookup"><span data-stu-id="16264-1345">scadenza</span></span>
- <span data-ttu-id="16264-1346">data scad</span><span class="sxs-lookup"><span data-stu-id="16264-1346">data scad</span></span>
- <span data-ttu-id="16264-1347">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="16264-1347">fecha de expiracion</span></span>
- <span data-ttu-id="16264-1348">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="16264-1348">fecha de venc</span></span>
- <span data-ttu-id="16264-1349">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="16264-1349">vencimiento</span></span>
- <span data-ttu-id="16264-1350">válido hasta</span><span class="sxs-lookup"><span data-stu-id="16264-1350">válido hasta</span></span>
- <span data-ttu-id="16264-1351">valido hasta</span><span class="sxs-lookup"><span data-stu-id="16264-1351">valido hasta</span></span>
- <span data-ttu-id="16264-1352">ВТО</span><span class="sxs-lookup"><span data-stu-id="16264-1352">vto</span></span>
- <span data-ttu-id="16264-1353">data de expiração</span><span class="sxs-lookup"><span data-stu-id="16264-1353">data de expiração</span></span>
- <span data-ttu-id="16264-1354">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="16264-1354">data de expiracao</span></span>
- <span data-ttu-id="16264-1355">data em que expira</span><span class="sxs-lookup"><span data-stu-id="16264-1355">data em que expira</span></span>
- <span data-ttu-id="16264-1356">валидаде</span><span class="sxs-lookup"><span data-stu-id="16264-1356">validade</span></span>
- <span data-ttu-id="16264-1357">Валор</span><span class="sxs-lookup"><span data-stu-id="16264-1357">valor</span></span>
- <span data-ttu-id="16264-1358">венЦименто</span><span class="sxs-lookup"><span data-stu-id="16264-1358">vencimento</span></span>
- <span data-ttu-id="16264-1359">Венк</span><span class="sxs-lookup"><span data-stu-id="16264-1359">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="16264-1360">Кэйворд_кк_наме</span><span class="sxs-lookup"><span data-stu-id="16264-1360">Keyword_cc_name</span></span>

- <span data-ttu-id="16264-1361">АМЕКС</span><span class="sxs-lookup"><span data-stu-id="16264-1361">amex</span></span>
- <span data-ttu-id="16264-1362">american express</span><span class="sxs-lookup"><span data-stu-id="16264-1362">american express</span></span>
- <span data-ttu-id="16264-1363">американекспресс</span><span class="sxs-lookup"><span data-stu-id="16264-1363">americanexpress</span></span>
- <span data-ttu-id="16264-1364">Visa</span><span class="sxs-lookup"><span data-stu-id="16264-1364">Visa</span></span>
- <span data-ttu-id="16264-1365">MasterCard</span><span class="sxs-lookup"><span data-stu-id="16264-1365">mastercard</span></span>
- <span data-ttu-id="16264-1366">master card</span><span class="sxs-lookup"><span data-stu-id="16264-1366">master card</span></span>
- <span data-ttu-id="16264-1367">MC</span><span class="sxs-lookup"><span data-stu-id="16264-1367">mc</span></span> 
- <span data-ttu-id="16264-1368">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="16264-1368">mastercards</span></span>
- <span data-ttu-id="16264-1369">master cards</span><span class="sxs-lookup"><span data-stu-id="16264-1369">master cards</span></span>
- <span data-ttu-id="16264-1370">diner's Club</span><span class="sxs-lookup"><span data-stu-id="16264-1370">diner's Club</span></span>
- <span data-ttu-id="16264-1371">diners club</span><span class="sxs-lookup"><span data-stu-id="16264-1371">diners club</span></span>
- <span data-ttu-id="16264-1372">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="16264-1372">dinersclub</span></span>
- <span data-ttu-id="16264-1373">discover card</span><span class="sxs-lookup"><span data-stu-id="16264-1373">discover card</span></span>
- <span data-ttu-id="16264-1374">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="16264-1374">discovercard</span></span>
- <span data-ttu-id="16264-1375">discover cards</span><span class="sxs-lookup"><span data-stu-id="16264-1375">discover cards</span></span>
- <span data-ttu-id="16264-1376">JCB</span><span class="sxs-lookup"><span data-stu-id="16264-1376">JCB</span></span>
- <span data-ttu-id="16264-1377">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="16264-1377">japanese card bureau</span></span>
- <span data-ttu-id="16264-1378">carte blanche</span><span class="sxs-lookup"><span data-stu-id="16264-1378">carte blanche</span></span>
- <span data-ttu-id="16264-1379">картебланче</span><span class="sxs-lookup"><span data-stu-id="16264-1379">carteblanche</span></span>
- <span data-ttu-id="16264-1380">credit card</span><span class="sxs-lookup"><span data-stu-id="16264-1380">credit card</span></span>
- <span data-ttu-id="16264-1381">Центральной</span><span class="sxs-lookup"><span data-stu-id="16264-1381">cc#</span></span>
- <span data-ttu-id="16264-1382">CC #:</span><span class="sxs-lookup"><span data-stu-id="16264-1382">cc#:</span></span>
- <span data-ttu-id="16264-1383">expiration date</span><span class="sxs-lookup"><span data-stu-id="16264-1383">expiration date</span></span>
- <span data-ttu-id="16264-1384">exp date</span><span class="sxs-lookup"><span data-stu-id="16264-1384">exp date</span></span>
- <span data-ttu-id="16264-1385">expiry date</span><span class="sxs-lookup"><span data-stu-id="16264-1385">expiry date</span></span>
- <span data-ttu-id="16264-1386">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="16264-1386">date d’expiration</span></span>
- <span data-ttu-id="16264-1387">date d'exp</span><span class="sxs-lookup"><span data-stu-id="16264-1387">date d'exp</span></span>
- <span data-ttu-id="16264-1388">date expiration</span><span class="sxs-lookup"><span data-stu-id="16264-1388">date expiration</span></span>
- <span data-ttu-id="16264-1389">bank card</span><span class="sxs-lookup"><span data-stu-id="16264-1389">bank card</span></span>
- <span data-ttu-id="16264-1390">банккард</span><span class="sxs-lookup"><span data-stu-id="16264-1390">bankcard</span></span>
- <span data-ttu-id="16264-1391">card number</span><span class="sxs-lookup"><span data-stu-id="16264-1391">card number</span></span>
- <span data-ttu-id="16264-1392">card num</span><span class="sxs-lookup"><span data-stu-id="16264-1392">card num</span></span>
- <span data-ttu-id="16264-1393">карднумбер</span><span class="sxs-lookup"><span data-stu-id="16264-1393">cardnumber</span></span>
- <span data-ttu-id="16264-1394">карднумберс</span><span class="sxs-lookup"><span data-stu-id="16264-1394">cardnumbers</span></span>
- <span data-ttu-id="16264-1395">card numbers</span><span class="sxs-lookup"><span data-stu-id="16264-1395">card numbers</span></span>
- <span data-ttu-id="16264-1396">кредиткард</span><span class="sxs-lookup"><span data-stu-id="16264-1396">creditcard</span></span>
- <span data-ttu-id="16264-1397">credit cards</span><span class="sxs-lookup"><span data-stu-id="16264-1397">credit cards</span></span>
- <span data-ttu-id="16264-1398">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="16264-1398">creditcards</span></span>
- <span data-ttu-id="16264-1399">CCN</span><span class="sxs-lookup"><span data-stu-id="16264-1399">ccn</span></span>
- <span data-ttu-id="16264-1400">card holder</span><span class="sxs-lookup"><span data-stu-id="16264-1400">card holder</span></span>
- <span data-ttu-id="16264-1401">банков</span><span class="sxs-lookup"><span data-stu-id="16264-1401">cardholder</span></span>
- <span data-ttu-id="16264-1402">card holders</span><span class="sxs-lookup"><span data-stu-id="16264-1402">card holders</span></span>
- <span data-ttu-id="16264-1403">карты</span><span class="sxs-lookup"><span data-stu-id="16264-1403">cardholders</span></span>
- <span data-ttu-id="16264-1404">check card</span><span class="sxs-lookup"><span data-stu-id="16264-1404">check card</span></span>
- <span data-ttu-id="16264-1405">чекккард</span><span class="sxs-lookup"><span data-stu-id="16264-1405">checkcard</span></span>
- <span data-ttu-id="16264-1406">check cards</span><span class="sxs-lookup"><span data-stu-id="16264-1406">check cards</span></span>
- <span data-ttu-id="16264-1407">чекккардс</span><span class="sxs-lookup"><span data-stu-id="16264-1407">checkcards</span></span>
- <span data-ttu-id="16264-1408">debit card</span><span class="sxs-lookup"><span data-stu-id="16264-1408">debit card</span></span>
- <span data-ttu-id="16264-1409">дебиткард</span><span class="sxs-lookup"><span data-stu-id="16264-1409">debitcard</span></span>
- <span data-ttu-id="16264-1410">debit cards</span><span class="sxs-lookup"><span data-stu-id="16264-1410">debit cards</span></span>
- <span data-ttu-id="16264-1411">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="16264-1411">debitcards</span></span>
- <span data-ttu-id="16264-1412">atm card</span><span class="sxs-lookup"><span data-stu-id="16264-1412">atm card</span></span>
- <span data-ttu-id="16264-1413">атмкард</span><span class="sxs-lookup"><span data-stu-id="16264-1413">atmcard</span></span>
- <span data-ttu-id="16264-1414">atm cards</span><span class="sxs-lookup"><span data-stu-id="16264-1414">atm cards</span></span>
- <span data-ttu-id="16264-1415">атмкардс</span><span class="sxs-lookup"><span data-stu-id="16264-1415">atmcards</span></span>
- <span data-ttu-id="16264-1416">енрауте</span><span class="sxs-lookup"><span data-stu-id="16264-1416">enroute</span></span>
- <span data-ttu-id="16264-1417">en route</span><span class="sxs-lookup"><span data-stu-id="16264-1417">en route</span></span>
- <span data-ttu-id="16264-1418">card type</span><span class="sxs-lookup"><span data-stu-id="16264-1418">card type</span></span>
- <span data-ttu-id="16264-1419">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="16264-1419">carte bancaire</span></span>
- <span data-ttu-id="16264-1420">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="16264-1420">carte de crédit</span></span>
- <span data-ttu-id="16264-1421">carte de credit</span><span class="sxs-lookup"><span data-stu-id="16264-1421">carte de credit</span></span>
- <span data-ttu-id="16264-1422">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="16264-1422">numéro de carte</span></span>
- <span data-ttu-id="16264-1423">numero de carte</span><span class="sxs-lookup"><span data-stu-id="16264-1423">numero de carte</span></span>
- <span data-ttu-id="16264-1424">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="16264-1424">nº de la carte</span></span>
- <span data-ttu-id="16264-1425">nº de carte</span><span class="sxs-lookup"><span data-stu-id="16264-1425">nº de carte</span></span>
- <span data-ttu-id="16264-1426">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="16264-1426">kreditkarte</span></span>
- <span data-ttu-id="16264-1427">карте</span><span class="sxs-lookup"><span data-stu-id="16264-1427">karte</span></span>
- <span data-ttu-id="16264-1428">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="16264-1428">karteninhaber</span></span>
- <span data-ttu-id="16264-1429">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="16264-1429">karteninhabers</span></span>
- <span data-ttu-id="16264-1430">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="16264-1430">kreditkarteninhaber</span></span>
- <span data-ttu-id="16264-1431">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="16264-1431">kreditkarteninstitut</span></span>
- <span data-ttu-id="16264-1432">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="16264-1432">kreditkartentyp</span></span>
- <span data-ttu-id="16264-1433">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="16264-1433">eigentümername</span></span>
- <span data-ttu-id="16264-1434">картеннр</span><span class="sxs-lookup"><span data-stu-id="16264-1434">kartennr</span></span> 
- <span data-ttu-id="16264-1435">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1435">kartennummer</span></span>
- <span data-ttu-id="16264-1436">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1436">kreditkartennummer</span></span>
- <span data-ttu-id="16264-1437">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1437">kreditkarten-nummer</span></span>
- <span data-ttu-id="16264-1438">carta di credito</span><span class="sxs-lookup"><span data-stu-id="16264-1438">carta di credito</span></span>
- <span data-ttu-id="16264-1439">carta credito</span><span class="sxs-lookup"><span data-stu-id="16264-1439">carta credito</span></span>
- <span data-ttu-id="16264-1440">Корзина "</span><span class="sxs-lookup"><span data-stu-id="16264-1440">carta</span></span>
- <span data-ttu-id="16264-1441">n carta</span><span class="sxs-lookup"><span data-stu-id="16264-1441">n carta</span></span>
- <span data-ttu-id="16264-1442">НР.</span><span class="sxs-lookup"><span data-stu-id="16264-1442">nr.</span></span> <span data-ttu-id="16264-1443">Корзина "</span><span class="sxs-lookup"><span data-stu-id="16264-1443">carta</span></span>
- <span data-ttu-id="16264-1444">nr carta</span><span class="sxs-lookup"><span data-stu-id="16264-1444">nr carta</span></span>
- <span data-ttu-id="16264-1445">numero carta</span><span class="sxs-lookup"><span data-stu-id="16264-1445">numero carta</span></span>
- <span data-ttu-id="16264-1446">numero della carta</span><span class="sxs-lookup"><span data-stu-id="16264-1446">numero della carta</span></span>
- <span data-ttu-id="16264-1447">numero di carta</span><span class="sxs-lookup"><span data-stu-id="16264-1447">numero di carta</span></span>
- <span data-ttu-id="16264-1448">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="16264-1448">tarjeta credito</span></span>
- <span data-ttu-id="16264-1449">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="16264-1449">tarjeta de credito</span></span>
- <span data-ttu-id="16264-1450">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="16264-1450">tarjeta crédito</span></span>
- <span data-ttu-id="16264-1451">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="16264-1451">tarjeta de crédito</span></span>
- <span data-ttu-id="16264-1452">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="16264-1452">tarjeta de atm</span></span>
- <span data-ttu-id="16264-1453">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="16264-1453">tarjeta atm</span></span>
- <span data-ttu-id="16264-1454">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="16264-1454">tarjeta debito</span></span>
- <span data-ttu-id="16264-1455">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="16264-1455">tarjeta de debito</span></span>
- <span data-ttu-id="16264-1456">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="16264-1456">tarjeta débito</span></span>
- <span data-ttu-id="16264-1457">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="16264-1457">tarjeta de débito</span></span>
- <span data-ttu-id="16264-1458">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1458">nº de tarjeta</span></span>
- <span data-ttu-id="16264-1459">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1459">no.</span></span> <span data-ttu-id="16264-1460">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1460">de tarjeta</span></span>
- <span data-ttu-id="16264-1461">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1461">no de tarjeta</span></span>
- <span data-ttu-id="16264-1462">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1462">numero de tarjeta</span></span>
- <span data-ttu-id="16264-1463">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1463">número de tarjeta</span></span>
- <span data-ttu-id="16264-1464">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="16264-1464">tarjeta no</span></span>
- <span data-ttu-id="16264-1465">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="16264-1465">tarjetahabiente</span></span>
- <span data-ttu-id="16264-1466">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="16264-1466">cartão de crédito</span></span>
- <span data-ttu-id="16264-1467">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="16264-1467">cartão de credito</span></span>
- <span data-ttu-id="16264-1468">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="16264-1468">cartao de crédito</span></span>
- <span data-ttu-id="16264-1469">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="16264-1469">cartao de credito</span></span>
- <span data-ttu-id="16264-1470">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="16264-1470">cartão de débito</span></span>
- <span data-ttu-id="16264-1471">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="16264-1471">cartao de débito</span></span>
- <span data-ttu-id="16264-1472">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="16264-1472">cartão de debito</span></span>
- <span data-ttu-id="16264-1473">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="16264-1473">cartao de debito</span></span>
- <span data-ttu-id="16264-1474">débito automático</span><span class="sxs-lookup"><span data-stu-id="16264-1474">débito automático</span></span>
- <span data-ttu-id="16264-1475">debito automatico</span><span class="sxs-lookup"><span data-stu-id="16264-1475">debito automatico</span></span>
- <span data-ttu-id="16264-1476">número do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1476">número do cartão</span></span>
- <span data-ttu-id="16264-1477">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1477">numero do cartão</span></span> 
- <span data-ttu-id="16264-1478">número do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1478">número do cartao</span></span>
- <span data-ttu-id="16264-1479">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1479">numero do cartao</span></span>
- <span data-ttu-id="16264-1480">número de cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1480">número de cartão</span></span>
- <span data-ttu-id="16264-1481">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1481">numero de cartão</span></span>
- <span data-ttu-id="16264-1482">número de cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1482">número de cartao</span></span>
- <span data-ttu-id="16264-1483">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1483">numero de cartao</span></span>
- <span data-ttu-id="16264-1484">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1484">nº do cartão</span></span>
- <span data-ttu-id="16264-1485">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1485">nº do cartao</span></span>
- <span data-ttu-id="16264-1486">n º.</span><span class="sxs-lookup"><span data-stu-id="16264-1486">nº.</span></span> <span data-ttu-id="16264-1487">do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1487">do cartão</span></span>
- <span data-ttu-id="16264-1488">no do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1488">no do cartão</span></span>
- <span data-ttu-id="16264-1489">no do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1489">no do cartao</span></span>
- <span data-ttu-id="16264-1490">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1490">no.</span></span> <span data-ttu-id="16264-1491">do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1491">do cartão</span></span>
- <span data-ttu-id="16264-1492">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1492">no.</span></span> <span data-ttu-id="16264-1493">do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1493">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="16264-1494">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="16264-1494">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1495">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1495">Format</span></span>

<span data-ttu-id="16264-1496">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1496">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1497">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1497">Pattern</span></span>

<span data-ttu-id="16264-1498">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1498">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1499">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1499">Checksum</span></span>

<span data-ttu-id="16264-1500">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1500">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1501">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1501">Definition</span></span>

<span data-ttu-id="16264-1502">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1502">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1503">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1503">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1504">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="16264-1504">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-1505">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1505">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="16264-1506">Кэйворд_кроатиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="16264-1506">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="16264-1507">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="16264-1507">Croatian identity card</span></span>
- <span data-ttu-id="16264-1508">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="16264-1508">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="16264-1509">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="16264-1509">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1510">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1510">Format</span></span>

<span data-ttu-id="16264-1511">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1511">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1512">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1512">Pattern</span></span>

<span data-ttu-id="16264-1513">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-1513">11 digits:</span></span>
- <span data-ttu-id="16264-1514">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1514">10 digits</span></span> 
- <span data-ttu-id="16264-1515">Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1515">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1516">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1516">Checksum</span></span>

<span data-ttu-id="16264-1517">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1517">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1518">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1518">Definition</span></span>

<span data-ttu-id="16264-1519">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1519">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1520">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1520">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1521">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="16264-1521">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="16264-1522">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1522">The checksum passes.</span></span>

<span data-ttu-id="16264-1523">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1523">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1524">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1524">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1525">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1525">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1526">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1526">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="16264-1527">Кэйворд_кроатиа_оиб_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-1527">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="16264-1528">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="16264-1528">Personal Identification Number</span></span>
- <span data-ttu-id="16264-1529">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="16264-1529">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="16264-1530">OIB</span><span class="sxs-lookup"><span data-stu-id="16264-1530">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="16264-1531">Номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="16264-1531">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1532">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1532">Format</span></span>

<span data-ttu-id="16264-1533">Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)</span><span class="sxs-lookup"><span data-stu-id="16264-1533">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1534">Pattern</span></span>

<span data-ttu-id="16264-1535">Девять цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="16264-1535">Nine digits (old format):</span></span>
- <span data-ttu-id="16264-1536">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1536">Nine digits</span></span>

<span data-ttu-id="16264-1537">OR</span><span class="sxs-lookup"><span data-stu-id="16264-1537">OR</span></span>

- <span data-ttu-id="16264-1538">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="16264-1538">Six digits that represent date of birth</span></span>
- <span data-ttu-id="16264-1539">косая черта;</span><span class="sxs-lookup"><span data-stu-id="16264-1539">A forward slash</span></span>
- <span data-ttu-id="16264-1540">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-1540">Three digits</span></span>

<span data-ttu-id="16264-1541">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="16264-1541">10 digits (new format):</span></span>
- <span data-ttu-id="16264-1542">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1542">10 digits</span></span>

<span data-ttu-id="16264-1543">OR</span><span class="sxs-lookup"><span data-stu-id="16264-1543">OR</span></span>

- <span data-ttu-id="16264-1544">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="16264-1544">Six digits that represent date of birth</span></span>
- <span data-ttu-id="16264-1545">косая черта;</span><span class="sxs-lookup"><span data-stu-id="16264-1545">A forward slash</span></span> 
- <span data-ttu-id="16264-1546">Четыре цифры, где последняя цифра является контрольной цифрой</span><span class="sxs-lookup"><span data-stu-id="16264-1546">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1547">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1547">Checksum</span></span>

<span data-ttu-id="16264-1548">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1549">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1549">Definition</span></span>

<span data-ttu-id="16264-1550">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_кзеч_ид_кард находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-1551">находится ключевое слово из Keyword_czech_id_card;</span><span class="sxs-lookup"><span data-stu-id="16264-1551">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="16264-1552">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1552">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="16264-1553">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1553">Keywords</span></span>

- <span data-ttu-id="16264-1554">номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="16264-1554">czech personal identity number</span></span>
- <span data-ttu-id="16264-1555">Роднé číсло</span><span class="sxs-lookup"><span data-stu-id="16264-1555">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="16264-1556">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="16264-1556">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1557">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1557">Format</span></span>

<span data-ttu-id="16264-1558">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="16264-1558">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1559">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1559">Pattern</span></span>

<span data-ttu-id="16264-1560">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-1560">10 digits:</span></span>
- <span data-ttu-id="16264-1561">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="16264-1561">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="16264-1562">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-1562">A hyphen</span></span> 
- <span data-ttu-id="16264-1563">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-1563">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1564">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1564">Checksum</span></span>

<span data-ttu-id="16264-1565">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1565">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1566">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1566">Definition</span></span>

<span data-ttu-id="16264-1567">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_денмарк_ид находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1567">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-1568">находится ключевое слово из Keyword_denmark_id;</span><span class="sxs-lookup"><span data-stu-id="16264-1568">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="16264-1569">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1569">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-1570">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1570">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="16264-1571">Кэйворд_денмарк_ид</span><span class="sxs-lookup"><span data-stu-id="16264-1571">Keyword_denmark_id</span></span>

- <span data-ttu-id="16264-1572">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="16264-1572">Personal Identification Number</span></span>
- <span data-ttu-id="16264-1573">CPR</span><span class="sxs-lookup"><span data-stu-id="16264-1573">CPR</span></span>
- <span data-ttu-id="16264-1574">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="16264-1574">Det Centrale Personregister</span></span>
- <span data-ttu-id="16264-1575">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1575">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="16264-1576">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="16264-1576">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1577">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1577">Format</span></span>

<span data-ttu-id="16264-1578">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1578">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1579">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1579">Pattern</span></span>

<span data-ttu-id="16264-1580">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="16264-1580">Pattern must include all of the following:</span></span>
- <span data-ttu-id="16264-1581">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="16264-1581">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="16264-1582">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="16264-1582">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="16264-1583">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="16264-1583">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1584">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1584">Checksum</span></span>

<span data-ttu-id="16264-1585">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1585">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1586">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1586">Definition</span></span>

<span data-ttu-id="16264-1587">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1587">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1588">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1588">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1589">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1589">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-1590">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1590">Keywords</span></span>

<span data-ttu-id="16264-1591">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1591">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="16264-1592">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="16264-1592">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1593">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1593">Format</span></span>

<span data-ttu-id="16264-1594">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1594">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1595">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1595">Pattern</span></span>

<span data-ttu-id="16264-1596">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="16264-1596">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1597">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1597">Checksum</span></span>

<span data-ttu-id="16264-1598">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1598">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1599">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1599">Definition</span></span>

<span data-ttu-id="16264-1600">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1600">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1601">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1601">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1602">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-1602">At least one of the following is true:</span></span>
    - <span data-ttu-id="16264-1603">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="16264-1603">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="16264-1604">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="16264-1604">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="16264-1605">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="16264-1605">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="16264-1606">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="16264-1606">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="16264-1607">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-1607">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="16264-1608">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1608">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1609">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1609">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="16264-1610">Кэйворд_еу_дебит_кард</span><span class="sxs-lookup"><span data-stu-id="16264-1610">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="16264-1611">account number</span><span class="sxs-lookup"><span data-stu-id="16264-1611">account number</span></span> 
- <span data-ttu-id="16264-1612">card number</span><span class="sxs-lookup"><span data-stu-id="16264-1612">card number</span></span> 
- <span data-ttu-id="16264-1613">card no.</span><span class="sxs-lookup"><span data-stu-id="16264-1613">card no.</span></span> 
- <span data-ttu-id="16264-1614">security number</span><span class="sxs-lookup"><span data-stu-id="16264-1614">security number</span></span> 
- <span data-ttu-id="16264-1615">Центральной</span><span class="sxs-lookup"><span data-stu-id="16264-1615">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="16264-1616">Кэйворд_кард_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="16264-1616">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="16264-1617">acct nbr</span><span class="sxs-lookup"><span data-stu-id="16264-1617">acct nbr</span></span> 
- <span data-ttu-id="16264-1618">acct num</span><span class="sxs-lookup"><span data-stu-id="16264-1618">acct num</span></span> 
- <span data-ttu-id="16264-1619">acct no</span><span class="sxs-lookup"><span data-stu-id="16264-1619">acct no</span></span> 
- <span data-ttu-id="16264-1620">american express</span><span class="sxs-lookup"><span data-stu-id="16264-1620">american express</span></span> 
- <span data-ttu-id="16264-1621">американекспресс</span><span class="sxs-lookup"><span data-stu-id="16264-1621">americanexpress</span></span> 
- <span data-ttu-id="16264-1622">americano espresso</span><span class="sxs-lookup"><span data-stu-id="16264-1622">americano espresso</span></span> 
- <span data-ttu-id="16264-1623">АМЕКС</span><span class="sxs-lookup"><span data-stu-id="16264-1623">amex</span></span> 
- <span data-ttu-id="16264-1624">atm card</span><span class="sxs-lookup"><span data-stu-id="16264-1624">atm card</span></span> 
- <span data-ttu-id="16264-1625">atm cards</span><span class="sxs-lookup"><span data-stu-id="16264-1625">atm cards</span></span> 
- <span data-ttu-id="16264-1626">atm kaart</span><span class="sxs-lookup"><span data-stu-id="16264-1626">atm kaart</span></span> 
- <span data-ttu-id="16264-1627">атмкард</span><span class="sxs-lookup"><span data-stu-id="16264-1627">atmcard</span></span> 
- <span data-ttu-id="16264-1628">атмкардс</span><span class="sxs-lookup"><span data-stu-id="16264-1628">atmcards</span></span> 
- <span data-ttu-id="16264-1629">атмкаарт</span><span class="sxs-lookup"><span data-stu-id="16264-1629">atmkaart</span></span> 
- <span data-ttu-id="16264-1630">атмкаартен</span><span class="sxs-lookup"><span data-stu-id="16264-1630">atmkaarten</span></span> 
- <span data-ttu-id="16264-1631">банконтакт</span><span class="sxs-lookup"><span data-stu-id="16264-1631">bancontact</span></span> 
- <span data-ttu-id="16264-1632">bank card</span><span class="sxs-lookup"><span data-stu-id="16264-1632">bank card</span></span> 
- <span data-ttu-id="16264-1633">банккаарт</span><span class="sxs-lookup"><span data-stu-id="16264-1633">bankkaart</span></span> 
- <span data-ttu-id="16264-1634">card holder</span><span class="sxs-lookup"><span data-stu-id="16264-1634">card holder</span></span> 
- <span data-ttu-id="16264-1635">card holders</span><span class="sxs-lookup"><span data-stu-id="16264-1635">card holders</span></span> 
- <span data-ttu-id="16264-1636">card num</span><span class="sxs-lookup"><span data-stu-id="16264-1636">card num</span></span> 
- <span data-ttu-id="16264-1637">card number</span><span class="sxs-lookup"><span data-stu-id="16264-1637">card number</span></span> 
- <span data-ttu-id="16264-1638">card numbers</span><span class="sxs-lookup"><span data-stu-id="16264-1638">card numbers</span></span> 
- <span data-ttu-id="16264-1639">card type</span><span class="sxs-lookup"><span data-stu-id="16264-1639">card type</span></span> 
- <span data-ttu-id="16264-1640">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="16264-1640">cardano numerico</span></span> 
- <span data-ttu-id="16264-1641">банков</span><span class="sxs-lookup"><span data-stu-id="16264-1641">cardholder</span></span> 
- <span data-ttu-id="16264-1642">карты</span><span class="sxs-lookup"><span data-stu-id="16264-1642">cardholders</span></span> 
- <span data-ttu-id="16264-1643">карднумбер</span><span class="sxs-lookup"><span data-stu-id="16264-1643">cardnumber</span></span> 
- <span data-ttu-id="16264-1644">карднумберс</span><span class="sxs-lookup"><span data-stu-id="16264-1644">cardnumbers</span></span> 
- <span data-ttu-id="16264-1645">carta bianca</span><span class="sxs-lookup"><span data-stu-id="16264-1645">carta bianca</span></span> 
- <span data-ttu-id="16264-1646">carta credito</span><span class="sxs-lookup"><span data-stu-id="16264-1646">carta credito</span></span> 
- <span data-ttu-id="16264-1647">carta di credito</span><span class="sxs-lookup"><span data-stu-id="16264-1647">carta di credito</span></span> 
- <span data-ttu-id="16264-1648">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="16264-1648">cartao de credito</span></span> 
- <span data-ttu-id="16264-1649">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="16264-1649">cartao de crédito</span></span> 
- <span data-ttu-id="16264-1650">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="16264-1650">cartao de debito</span></span> 
- <span data-ttu-id="16264-1651">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="16264-1651">cartao de débito</span></span> 
- <span data-ttu-id="16264-1652">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="16264-1652">carte bancaire</span></span> 
- <span data-ttu-id="16264-1653">carte blanche</span><span class="sxs-lookup"><span data-stu-id="16264-1653">carte blanche</span></span> 
- <span data-ttu-id="16264-1654">carte bleue</span><span class="sxs-lookup"><span data-stu-id="16264-1654">carte bleue</span></span> 
- <span data-ttu-id="16264-1655">carte de credit</span><span class="sxs-lookup"><span data-stu-id="16264-1655">carte de credit</span></span> 
- <span data-ttu-id="16264-1656">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="16264-1656">carte de crédit</span></span> 
- <span data-ttu-id="16264-1657">carte di credito</span><span class="sxs-lookup"><span data-stu-id="16264-1657">carte di credito</span></span> 
- <span data-ttu-id="16264-1658">картебланче</span><span class="sxs-lookup"><span data-stu-id="16264-1658">carteblanche</span></span> 
- <span data-ttu-id="16264-1659">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="16264-1659">cartão de credito</span></span> 
- <span data-ttu-id="16264-1660">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="16264-1660">cartão de crédito</span></span> 
- <span data-ttu-id="16264-1661">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="16264-1661">cartão de debito</span></span> 
- <span data-ttu-id="16264-1662">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="16264-1662">cartão de débito</span></span> 
- <span data-ttu-id="16264-1663">cb</span><span class="sxs-lookup"><span data-stu-id="16264-1663">cb</span></span> 
- <span data-ttu-id="16264-1664">CCN</span><span class="sxs-lookup"><span data-stu-id="16264-1664">ccn</span></span> 
- <span data-ttu-id="16264-1665">check card</span><span class="sxs-lookup"><span data-stu-id="16264-1665">check card</span></span> 
- <span data-ttu-id="16264-1666">check cards</span><span class="sxs-lookup"><span data-stu-id="16264-1666">check cards</span></span> 
- <span data-ttu-id="16264-1667">чекккард</span><span class="sxs-lookup"><span data-stu-id="16264-1667">checkcard</span></span>
- <span data-ttu-id="16264-1668">чекккардс</span><span class="sxs-lookup"><span data-stu-id="16264-1668">checkcards</span></span> 
- <span data-ttu-id="16264-1669">чекуекаарт</span><span class="sxs-lookup"><span data-stu-id="16264-1669">chequekaart</span></span> 
- <span data-ttu-id="16264-1670">Logic</span><span class="sxs-lookup"><span data-stu-id="16264-1670">cirrus</span></span> 
- <span data-ttu-id="16264-1671">Cirrus центр EDC — Маестро</span><span class="sxs-lookup"><span data-stu-id="16264-1671">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="16264-1672">контролекаарт</span><span class="sxs-lookup"><span data-stu-id="16264-1672">controlekaart</span></span> 
- <span data-ttu-id="16264-1673">контролекаартен</span><span class="sxs-lookup"><span data-stu-id="16264-1673">controlekaarten</span></span> 
- <span data-ttu-id="16264-1674">credit card</span><span class="sxs-lookup"><span data-stu-id="16264-1674">credit card</span></span> 
- <span data-ttu-id="16264-1675">credit cards</span><span class="sxs-lookup"><span data-stu-id="16264-1675">credit cards</span></span> 
- <span data-ttu-id="16264-1676">кредиткард</span><span class="sxs-lookup"><span data-stu-id="16264-1676">creditcard</span></span> 
- <span data-ttu-id="16264-1677">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="16264-1677">creditcards</span></span> 
- <span data-ttu-id="16264-1678">дебеткаарт</span><span class="sxs-lookup"><span data-stu-id="16264-1678">debetkaart</span></span> 
- <span data-ttu-id="16264-1679">дебеткаартен</span><span class="sxs-lookup"><span data-stu-id="16264-1679">debetkaarten</span></span> 
- <span data-ttu-id="16264-1680">debit card</span><span class="sxs-lookup"><span data-stu-id="16264-1680">debit card</span></span> 
- <span data-ttu-id="16264-1681">debit cards</span><span class="sxs-lookup"><span data-stu-id="16264-1681">debit cards</span></span> 
- <span data-ttu-id="16264-1682">дебиткард</span><span class="sxs-lookup"><span data-stu-id="16264-1682">debitcard</span></span> 
- <span data-ttu-id="16264-1683">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="16264-1683">debitcards</span></span> 
- <span data-ttu-id="16264-1684">debito automatico</span><span class="sxs-lookup"><span data-stu-id="16264-1684">debito automatico</span></span> 
- <span data-ttu-id="16264-1685">diners club</span><span class="sxs-lookup"><span data-stu-id="16264-1685">diners club</span></span> 
- <span data-ttu-id="16264-1686">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="16264-1686">dinersclub</span></span> 
- <span data-ttu-id="16264-1687">Повтор</span><span class="sxs-lookup"><span data-stu-id="16264-1687">discover</span></span> 
- <span data-ttu-id="16264-1688">discover card</span><span class="sxs-lookup"><span data-stu-id="16264-1688">discover card</span></span> 
- <span data-ttu-id="16264-1689">discover cards</span><span class="sxs-lookup"><span data-stu-id="16264-1689">discover cards</span></span> 
- <span data-ttu-id="16264-1690">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="16264-1690">discovercard</span></span> 
- <span data-ttu-id="16264-1691">дисковеркардс</span><span class="sxs-lookup"><span data-stu-id="16264-1691">discovercards</span></span> 
- <span data-ttu-id="16264-1692">débito automático</span><span class="sxs-lookup"><span data-stu-id="16264-1692">débito automático</span></span>
- <span data-ttu-id="16264-1693">центр EDC</span><span class="sxs-lookup"><span data-stu-id="16264-1693">edc</span></span> 
- <span data-ttu-id="16264-1694">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="16264-1694">eigentümername</span></span> 
- <span data-ttu-id="16264-1695">european debit card</span><span class="sxs-lookup"><span data-stu-id="16264-1695">european debit card</span></span> 
- <span data-ttu-id="16264-1696">хуфдкаарт</span><span class="sxs-lookup"><span data-stu-id="16264-1696">hoofdkaart</span></span> 
- <span data-ttu-id="16264-1697">хуфдкаартен</span><span class="sxs-lookup"><span data-stu-id="16264-1697">hoofdkaarten</span></span> 
- <span data-ttu-id="16264-1698">in viaggio</span><span class="sxs-lookup"><span data-stu-id="16264-1698">in viaggio</span></span> 
- <span data-ttu-id="16264-1699">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="16264-1699">japanese card bureau</span></span> 
- <span data-ttu-id="16264-1700">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="16264-1700">japanse kaartdienst</span></span> 
- <span data-ttu-id="16264-1701">JCB</span><span class="sxs-lookup"><span data-stu-id="16264-1701">jcb</span></span> 
- <span data-ttu-id="16264-1702">каарт</span><span class="sxs-lookup"><span data-stu-id="16264-1702">kaart</span></span> 
- <span data-ttu-id="16264-1703">kaart num</span><span class="sxs-lookup"><span data-stu-id="16264-1703">kaart num</span></span> 
- <span data-ttu-id="16264-1704">каартаантал</span><span class="sxs-lookup"><span data-stu-id="16264-1704">kaartaantal</span></span> 
- <span data-ttu-id="16264-1705">каартаанталлен</span><span class="sxs-lookup"><span data-stu-id="16264-1705">kaartaantallen</span></span> 
- <span data-ttu-id="16264-1706">каарсаудер</span><span class="sxs-lookup"><span data-stu-id="16264-1706">kaarthouder</span></span> 
- <span data-ttu-id="16264-1707">каарсаудерс</span><span class="sxs-lookup"><span data-stu-id="16264-1707">kaarthouders</span></span> 
- <span data-ttu-id="16264-1708">карте</span><span class="sxs-lookup"><span data-stu-id="16264-1708">karte</span></span>  
- <span data-ttu-id="16264-1709">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="16264-1709">karteninhaber</span></span> 
- <span data-ttu-id="16264-1710">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="16264-1710">karteninhabers</span></span>
- <span data-ttu-id="16264-1711">картеннр</span><span class="sxs-lookup"><span data-stu-id="16264-1711">kartennr</span></span> 
- <span data-ttu-id="16264-1712">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1712">kartennummer</span></span> 
- <span data-ttu-id="16264-1713">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="16264-1713">kreditkarte</span></span> 
- <span data-ttu-id="16264-1714">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1714">kreditkarten-nummer</span></span> 
- <span data-ttu-id="16264-1715">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="16264-1715">kreditkarteninhaber</span></span> 
- <span data-ttu-id="16264-1716">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="16264-1716">kreditkarteninstitut</span></span> 
- <span data-ttu-id="16264-1717">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1717">kreditkartennummer</span></span> 
- <span data-ttu-id="16264-1718">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="16264-1718">kreditkartentyp</span></span> 
- <span data-ttu-id="16264-1719">Маестро</span><span class="sxs-lookup"><span data-stu-id="16264-1719">maestro</span></span> 
- <span data-ttu-id="16264-1720">master card</span><span class="sxs-lookup"><span data-stu-id="16264-1720">master card</span></span> 
- <span data-ttu-id="16264-1721">master cards</span><span class="sxs-lookup"><span data-stu-id="16264-1721">master cards</span></span> 
- <span data-ttu-id="16264-1722">MasterCard</span><span class="sxs-lookup"><span data-stu-id="16264-1722">mastercard</span></span> 
- <span data-ttu-id="16264-1723">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="16264-1723">mastercards</span></span> 
- <span data-ttu-id="16264-1724">MC</span><span class="sxs-lookup"><span data-stu-id="16264-1724">mc</span></span> 
- <span data-ttu-id="16264-1725">mister cash</span><span class="sxs-lookup"><span data-stu-id="16264-1725">mister cash</span></span> 
- <span data-ttu-id="16264-1726">n carta</span><span class="sxs-lookup"><span data-stu-id="16264-1726">n carta</span></span> 
- <span data-ttu-id="16264-1727">Корзина "</span><span class="sxs-lookup"><span data-stu-id="16264-1727">carta</span></span> 
- <span data-ttu-id="16264-1728">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1728">no de tarjeta</span></span> 
- <span data-ttu-id="16264-1729">no do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1729">no do cartao</span></span> 
- <span data-ttu-id="16264-1730">no do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1730">no do cartão</span></span> 
- <span data-ttu-id="16264-1731">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1731">no.</span></span> <span data-ttu-id="16264-1732">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1732">de tarjeta</span></span> 
- <span data-ttu-id="16264-1733">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1733">no.</span></span> <span data-ttu-id="16264-1734">do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1734">do cartao</span></span> 
- <span data-ttu-id="16264-1735">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1735">no.</span></span> <span data-ttu-id="16264-1736">do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1736">do cartão</span></span> 
- <span data-ttu-id="16264-1737">nr carta</span><span class="sxs-lookup"><span data-stu-id="16264-1737">nr carta</span></span> 
- <span data-ttu-id="16264-1738">НР.</span><span class="sxs-lookup"><span data-stu-id="16264-1738">nr.</span></span> <span data-ttu-id="16264-1739">Корзина "</span><span class="sxs-lookup"><span data-stu-id="16264-1739">carta</span></span> 
- <span data-ttu-id="16264-1740">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="16264-1740">numeri di scheda</span></span> 
- <span data-ttu-id="16264-1741">numero carta</span><span class="sxs-lookup"><span data-stu-id="16264-1741">numero carta</span></span> 
- <span data-ttu-id="16264-1742">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1742">numero de cartao</span></span> 
- <span data-ttu-id="16264-1743">numero de carte</span><span class="sxs-lookup"><span data-stu-id="16264-1743">numero de carte</span></span> 
- <span data-ttu-id="16264-1744">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1744">numero de cartão</span></span> 
- <span data-ttu-id="16264-1745">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1745">numero de tarjeta</span></span>
- <span data-ttu-id="16264-1746">numero della carta</span><span class="sxs-lookup"><span data-stu-id="16264-1746">numero della carta</span></span> 
- <span data-ttu-id="16264-1747">numero di carta</span><span class="sxs-lookup"><span data-stu-id="16264-1747">numero di carta</span></span> 
- <span data-ttu-id="16264-1748">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="16264-1748">numero di scheda</span></span> 
- <span data-ttu-id="16264-1749">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1749">numero do cartao</span></span> 
- <span data-ttu-id="16264-1750">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1750">numero do cartão</span></span> 
- <span data-ttu-id="16264-1751">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="16264-1751">numéro de carte</span></span> 
- <span data-ttu-id="16264-1752">nº carta</span><span class="sxs-lookup"><span data-stu-id="16264-1752">nº carta</span></span> 
- <span data-ttu-id="16264-1753">nº de carte</span><span class="sxs-lookup"><span data-stu-id="16264-1753">nº de carte</span></span> 
- <span data-ttu-id="16264-1754">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="16264-1754">nº de la carte</span></span> 
- <span data-ttu-id="16264-1755">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1755">nº de tarjeta</span></span> 
- <span data-ttu-id="16264-1756">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1756">nº do cartao</span></span> 
- <span data-ttu-id="16264-1757">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1757">nº do cartão</span></span> 
- <span data-ttu-id="16264-1758">n º.</span><span class="sxs-lookup"><span data-stu-id="16264-1758">nº.</span></span> <span data-ttu-id="16264-1759">do cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1759">do cartão</span></span> 
- <span data-ttu-id="16264-1760">número de cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1760">número de cartao</span></span> 
- <span data-ttu-id="16264-1761">número de cartão</span><span class="sxs-lookup"><span data-stu-id="16264-1761">número de cartão</span></span> 
- <span data-ttu-id="16264-1762">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="16264-1762">número de tarjeta</span></span> 
- <span data-ttu-id="16264-1763">número do cartao</span><span class="sxs-lookup"><span data-stu-id="16264-1763">número do cartao</span></span> 
- <span data-ttu-id="16264-1764">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="16264-1764">scheda dell'assegno</span></span> 
- <span data-ttu-id="16264-1765">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="16264-1765">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="16264-1766">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="16264-1766">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="16264-1767">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="16264-1767">scheda della banca</span></span> 
- <span data-ttu-id="16264-1768">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="16264-1768">scheda di controllo</span></span> 
- <span data-ttu-id="16264-1769">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="16264-1769">scheda di debito</span></span> 
- <span data-ttu-id="16264-1770">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="16264-1770">scheda matrice</span></span> 
- <span data-ttu-id="16264-1771">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="16264-1771">schede dell'atmosfera</span></span> 
- <span data-ttu-id="16264-1772">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="16264-1772">schede di controllo</span></span> 
- <span data-ttu-id="16264-1773">schede di debito</span><span class="sxs-lookup"><span data-stu-id="16264-1773">schede di debito</span></span> 
- <span data-ttu-id="16264-1774">schede matrici</span><span class="sxs-lookup"><span data-stu-id="16264-1774">schede matrici</span></span> 
- <span data-ttu-id="16264-1775">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="16264-1775">scoprono la scheda</span></span> 
- <span data-ttu-id="16264-1776">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="16264-1776">scoprono le schede</span></span> 
- <span data-ttu-id="16264-1777">ОС</span><span class="sxs-lookup"><span data-stu-id="16264-1777">solo</span></span> 
- <span data-ttu-id="16264-1778">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="16264-1778">supporti di scheda</span></span> 
- <span data-ttu-id="16264-1779">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="16264-1779">supporto di scheda</span></span> 
- <span data-ttu-id="16264-1780">отключен</span><span class="sxs-lookup"><span data-stu-id="16264-1780">switch</span></span> 
- <span data-ttu-id="16264-1781">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="16264-1781">tarjeta atm</span></span> 
- <span data-ttu-id="16264-1782">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="16264-1782">tarjeta credito</span></span> 
- <span data-ttu-id="16264-1783">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="16264-1783">tarjeta de atm</span></span> 
- <span data-ttu-id="16264-1784">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="16264-1784">tarjeta de credito</span></span> 
- <span data-ttu-id="16264-1785">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="16264-1785">tarjeta de debito</span></span> 
- <span data-ttu-id="16264-1786">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="16264-1786">tarjeta debito</span></span> 
- <span data-ttu-id="16264-1787">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="16264-1787">tarjeta no</span></span>
- <span data-ttu-id="16264-1788">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="16264-1788">tarjetahabiente</span></span> 
- <span data-ttu-id="16264-1789">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="16264-1789">tipo della scheda</span></span> 
- <span data-ttu-id="16264-1790">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="16264-1790">ufficio giapponese della</span></span> 
- <span data-ttu-id="16264-1791">счеда</span><span class="sxs-lookup"><span data-stu-id="16264-1791">scheda</span></span> 
- <span data-ttu-id="16264-1792">v pay</span><span class="sxs-lookup"><span data-stu-id="16264-1792">v pay</span></span> 
- <span data-ttu-id="16264-1793">v — оплата</span><span class="sxs-lookup"><span data-stu-id="16264-1793">v-pay</span></span> 
- <span data-ttu-id="16264-1794">Visa</span><span class="sxs-lookup"><span data-stu-id="16264-1794">visa</span></span> 
- <span data-ttu-id="16264-1795">visa plus</span><span class="sxs-lookup"><span data-stu-id="16264-1795">visa plus</span></span> 
- <span data-ttu-id="16264-1796">visa electron</span><span class="sxs-lookup"><span data-stu-id="16264-1796">visa electron</span></span> 
- <span data-ttu-id="16264-1797">висто</span><span class="sxs-lookup"><span data-stu-id="16264-1797">visto</span></span> 
- <span data-ttu-id="16264-1798">висум</span><span class="sxs-lookup"><span data-stu-id="16264-1798">visum</span></span> 
- <span data-ttu-id="16264-1799">впай</span><span class="sxs-lookup"><span data-stu-id="16264-1799">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="16264-1800">Кэйворд_кард_секурити_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="16264-1800">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="16264-1801">card identification number</span><span class="sxs-lookup"><span data-stu-id="16264-1801">card identification number</span></span>
- <span data-ttu-id="16264-1802">card verification</span><span class="sxs-lookup"><span data-stu-id="16264-1802">card verification</span></span> 
- <span data-ttu-id="16264-1803">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="16264-1803">cardi la verifica</span></span> 
- <span data-ttu-id="16264-1804">cid</span><span class="sxs-lookup"><span data-stu-id="16264-1804">cid</span></span> 
- <span data-ttu-id="16264-1805">cod seg</span><span class="sxs-lookup"><span data-stu-id="16264-1805">cod seg</span></span> 
- <span data-ttu-id="16264-1806">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1806">cod seguranca</span></span> 
- <span data-ttu-id="16264-1807">cod segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1807">cod segurança</span></span> 
- <span data-ttu-id="16264-1808">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="16264-1808">cod sicurezza</span></span> 
- <span data-ttu-id="16264-1809">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1809">cod.</span></span> <span data-ttu-id="16264-1810">СЕГ</span><span class="sxs-lookup"><span data-stu-id="16264-1810">seg</span></span> 
- <span data-ttu-id="16264-1811">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1811">cod.</span></span> <span data-ttu-id="16264-1812">сегуранка</span><span class="sxs-lookup"><span data-stu-id="16264-1812">seguranca</span></span> 
- <span data-ttu-id="16264-1813">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1813">cod.</span></span> <span data-ttu-id="16264-1814">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="16264-1814">segurança</span></span> 
- <span data-ttu-id="16264-1815">наложен.</span><span class="sxs-lookup"><span data-stu-id="16264-1815">cod.</span></span> <span data-ttu-id="16264-1816">сикурезза</span><span class="sxs-lookup"><span data-stu-id="16264-1816">sicurezza</span></span> 
- <span data-ttu-id="16264-1817">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="16264-1817">codice di sicurezza</span></span> 
- <span data-ttu-id="16264-1818">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="16264-1818">codice di verifica</span></span> 
- <span data-ttu-id="16264-1819">кодиго</span><span class="sxs-lookup"><span data-stu-id="16264-1819">codigo</span></span> 
- <span data-ttu-id="16264-1820">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1820">codigo de seguranca</span></span> 
- <span data-ttu-id="16264-1821">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1821">codigo de segurança</span></span> 
- <span data-ttu-id="16264-1822">криттограмма</span><span class="sxs-lookup"><span data-stu-id="16264-1822">crittogramma</span></span> 
- <span data-ttu-id="16264-1823">криптограм</span><span class="sxs-lookup"><span data-stu-id="16264-1823">cryptogram</span></span> 
- <span data-ttu-id="16264-1824">криптограмме</span><span class="sxs-lookup"><span data-stu-id="16264-1824">cryptogramme</span></span> 
- <span data-ttu-id="16264-1825">CV2</span><span class="sxs-lookup"><span data-stu-id="16264-1825">cv2</span></span> 
- <span data-ttu-id="16264-1826">КВК</span><span class="sxs-lookup"><span data-stu-id="16264-1826">cvc</span></span> 
- <span data-ttu-id="16264-1827">CVC2</span><span class="sxs-lookup"><span data-stu-id="16264-1827">cvc2</span></span> 
- <span data-ttu-id="16264-1828">КВН</span><span class="sxs-lookup"><span data-stu-id="16264-1828">cvn</span></span> 
- <span data-ttu-id="16264-1829">КВВ</span><span class="sxs-lookup"><span data-stu-id="16264-1829">cvv</span></span> 
- <span data-ttu-id="16264-1830">CVV2</span><span class="sxs-lookup"><span data-stu-id="16264-1830">cvv2</span></span> 
- <span data-ttu-id="16264-1831">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1831">cód seguranca</span></span> 
- <span data-ttu-id="16264-1832">cód segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1832">cód segurança</span></span> 
- <span data-ttu-id="16264-1833">кóд.</span><span class="sxs-lookup"><span data-stu-id="16264-1833">cód.</span></span> <span data-ttu-id="16264-1834">сегуранка</span><span class="sxs-lookup"><span data-stu-id="16264-1834">seguranca</span></span> 
- <span data-ttu-id="16264-1835">кóд.</span><span class="sxs-lookup"><span data-stu-id="16264-1835">cód.</span></span> <span data-ttu-id="16264-1836">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="16264-1836">segurança</span></span> 
- <span data-ttu-id="16264-1837">кóдиго</span><span class="sxs-lookup"><span data-stu-id="16264-1837">código</span></span> 
- <span data-ttu-id="16264-1838">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="16264-1838">código de seguranca</span></span> 
- <span data-ttu-id="16264-1839">código de segurança</span><span class="sxs-lookup"><span data-stu-id="16264-1839">código de segurança</span></span> 
- <span data-ttu-id="16264-1840">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="16264-1840">de kaart controle</span></span> 
- <span data-ttu-id="16264-1841">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="16264-1841">geeft nr uit</span></span> 
- <span data-ttu-id="16264-1842">issue no</span><span class="sxs-lookup"><span data-stu-id="16264-1842">issue no</span></span> 
- <span data-ttu-id="16264-1843">issue number</span><span class="sxs-lookup"><span data-stu-id="16264-1843">issue number</span></span> 
- <span data-ttu-id="16264-1844">каартидентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1844">kaartidentificatienummer</span></span> 
- <span data-ttu-id="16264-1845">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1845">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="16264-1846">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1846">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="16264-1847">квестиеаантал</span><span class="sxs-lookup"><span data-stu-id="16264-1847">kwestieaantal</span></span> 
- <span data-ttu-id="16264-1848">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1848">no.</span></span> <span data-ttu-id="16264-1849">делл'едизионе</span><span class="sxs-lookup"><span data-stu-id="16264-1849">dell'edizione</span></span> 
- <span data-ttu-id="16264-1850">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-1850">no.</span></span> <span data-ttu-id="16264-1851">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="16264-1851">di sicurezza</span></span> 
- <span data-ttu-id="16264-1852">numero de securite</span><span class="sxs-lookup"><span data-stu-id="16264-1852">numero de securite</span></span> 
- <span data-ttu-id="16264-1853">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="16264-1853">numero de verificacao</span></span> 
- <span data-ttu-id="16264-1854">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="16264-1854">numero dell'edizione</span></span> 
- <span data-ttu-id="16264-1855">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="16264-1855">numero di identificazione della</span></span> 
- <span data-ttu-id="16264-1856">счеда</span><span class="sxs-lookup"><span data-stu-id="16264-1856">scheda</span></span> 
- <span data-ttu-id="16264-1857">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="16264-1857">numero di sicurezza</span></span> 
- <span data-ttu-id="16264-1858">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="16264-1858">numero van veiligheid</span></span> 
- <span data-ttu-id="16264-1859">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="16264-1859">numéro de sécurité</span></span> 
- <span data-ttu-id="16264-1860">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="16264-1860">nº autorizzazione</span></span> 
- <span data-ttu-id="16264-1861">número de verificação</span><span class="sxs-lookup"><span data-stu-id="16264-1861">número de verificação</span></span> 
- <span data-ttu-id="16264-1862">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="16264-1862">perno il blocco</span></span> 
- <span data-ttu-id="16264-1863">pin block</span><span class="sxs-lookup"><span data-stu-id="16264-1863">pin block</span></span> 
- <span data-ttu-id="16264-1864">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="16264-1864">prufziffer</span></span> 
- <span data-ttu-id="16264-1865">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="16264-1865">prüfziffer</span></span> 
- <span data-ttu-id="16264-1866">security code</span><span class="sxs-lookup"><span data-stu-id="16264-1866">security code</span></span> 
- <span data-ttu-id="16264-1867">security no</span><span class="sxs-lookup"><span data-stu-id="16264-1867">security no</span></span> 
- <span data-ttu-id="16264-1868">security number</span><span class="sxs-lookup"><span data-stu-id="16264-1868">security number</span></span> 
- <span data-ttu-id="16264-1869">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="16264-1869">sicherheits kode</span></span> 
- <span data-ttu-id="16264-1870">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="16264-1870">sicherheitscode</span></span> 
- <span data-ttu-id="16264-1871">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1871">sicherheitsnummer</span></span> 
- <span data-ttu-id="16264-1872">спелдблок</span><span class="sxs-lookup"><span data-stu-id="16264-1872">speldblok</span></span> 
- <span data-ttu-id="16264-1873">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="16264-1873">veiligheid nr</span></span> 
- <span data-ttu-id="16264-1874">веилигхеидсаантал</span><span class="sxs-lookup"><span data-stu-id="16264-1874">veiligheidsaantal</span></span> 
- <span data-ttu-id="16264-1875">веилигхеидскоде</span><span class="sxs-lookup"><span data-stu-id="16264-1875">veiligheidscode</span></span> 
- <span data-ttu-id="16264-1876">веилигхеидснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1876">veiligheidsnummer</span></span> 
- <span data-ttu-id="16264-1877">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1877">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="16264-1878">Кэйворд_кард_експиратион_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="16264-1878">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="16264-1879">аблауф</span><span class="sxs-lookup"><span data-stu-id="16264-1879">ablauf</span></span> 
- <span data-ttu-id="16264-1880">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="16264-1880">data de expiracao</span></span> 
- <span data-ttu-id="16264-1881">data de expiração</span><span class="sxs-lookup"><span data-stu-id="16264-1881">data de expiração</span></span> 
- <span data-ttu-id="16264-1882">data del exp</span><span class="sxs-lookup"><span data-stu-id="16264-1882">data del exp</span></span> 
- <span data-ttu-id="16264-1883">data di exp</span><span class="sxs-lookup"><span data-stu-id="16264-1883">data di exp</span></span> 
- <span data-ttu-id="16264-1884">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="16264-1884">data di scadenza</span></span> 
- <span data-ttu-id="16264-1885">data em que expira</span><span class="sxs-lookup"><span data-stu-id="16264-1885">data em que expira</span></span> 
- <span data-ttu-id="16264-1886">data scad</span><span class="sxs-lookup"><span data-stu-id="16264-1886">data scad</span></span> 
- <span data-ttu-id="16264-1887">data scadenza</span><span class="sxs-lookup"><span data-stu-id="16264-1887">data scadenza</span></span> 
- <span data-ttu-id="16264-1888">date de validité</span><span class="sxs-lookup"><span data-stu-id="16264-1888">date de validité</span></span> 
- <span data-ttu-id="16264-1889">datum afloop</span><span class="sxs-lookup"><span data-stu-id="16264-1889">datum afloop</span></span> 
- <span data-ttu-id="16264-1890">datum van exp</span><span class="sxs-lookup"><span data-stu-id="16264-1890">datum van exp</span></span> 
- <span data-ttu-id="16264-1891">de afloop</span><span class="sxs-lookup"><span data-stu-id="16264-1891">de afloop</span></span> 
- <span data-ttu-id="16264-1892">еспира</span><span class="sxs-lookup"><span data-stu-id="16264-1892">espira</span></span> 
- <span data-ttu-id="16264-1893">еспира</span><span class="sxs-lookup"><span data-stu-id="16264-1893">espira</span></span> 
- <span data-ttu-id="16264-1894">exp date</span><span class="sxs-lookup"><span data-stu-id="16264-1894">exp date</span></span> 
- <span data-ttu-id="16264-1895">exp datum</span><span class="sxs-lookup"><span data-stu-id="16264-1895">exp datum</span></span> 
- <span data-ttu-id="16264-1896">срока действия</span><span class="sxs-lookup"><span data-stu-id="16264-1896">expiration</span></span> 
- <span data-ttu-id="16264-1897">истекает</span><span class="sxs-lookup"><span data-stu-id="16264-1897">expire</span></span> 
- <span data-ttu-id="16264-1898">истекает</span><span class="sxs-lookup"><span data-stu-id="16264-1898">expires</span></span> 
- <span data-ttu-id="16264-1899">окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="16264-1899">expiry</span></span> 
- <span data-ttu-id="16264-1900">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="16264-1900">fecha de expiracion</span></span> 
- <span data-ttu-id="16264-1901">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="16264-1901">fecha de venc</span></span> 
- <span data-ttu-id="16264-1902">gultig bis</span><span class="sxs-lookup"><span data-stu-id="16264-1902">gultig bis</span></span> 
- <span data-ttu-id="16264-1903">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1903">gultigkeitsdatum</span></span> 
- <span data-ttu-id="16264-1904">gültig bis</span><span class="sxs-lookup"><span data-stu-id="16264-1904">gültig bis</span></span> 
- <span data-ttu-id="16264-1905">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1905">gültigkeitsdatum</span></span> 
- <span data-ttu-id="16264-1906">la scadenza</span><span class="sxs-lookup"><span data-stu-id="16264-1906">la scadenza</span></span> 
- <span data-ttu-id="16264-1907">скаденза</span><span class="sxs-lookup"><span data-stu-id="16264-1907">scadenza</span></span> 
- <span data-ttu-id="16264-1908">валабле</span><span class="sxs-lookup"><span data-stu-id="16264-1908">valable</span></span> 
- <span data-ttu-id="16264-1909">валидаде</span><span class="sxs-lookup"><span data-stu-id="16264-1909">validade</span></span> 
- <span data-ttu-id="16264-1910">valido hasta</span><span class="sxs-lookup"><span data-stu-id="16264-1910">valido hasta</span></span> 
- <span data-ttu-id="16264-1911">Валор</span><span class="sxs-lookup"><span data-stu-id="16264-1911">valor</span></span> 
- <span data-ttu-id="16264-1912">Венк</span><span class="sxs-lookup"><span data-stu-id="16264-1912">venc</span></span> 
- <span data-ttu-id="16264-1913">венЦименто</span><span class="sxs-lookup"><span data-stu-id="16264-1913">vencimento</span></span> 
- <span data-ttu-id="16264-1914">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="16264-1914">vencimiento</span></span> 
- <span data-ttu-id="16264-1915">верлупт</span><span class="sxs-lookup"><span data-stu-id="16264-1915">verloopt</span></span> 
- <span data-ttu-id="16264-1916">вервалдаг</span><span class="sxs-lookup"><span data-stu-id="16264-1916">vervaldag</span></span> 
- <span data-ttu-id="16264-1917">вервалдатум</span><span class="sxs-lookup"><span data-stu-id="16264-1917">vervaldatum</span></span> 
- <span data-ttu-id="16264-1918">ВТО</span><span class="sxs-lookup"><span data-stu-id="16264-1918">vto</span></span> 
- <span data-ttu-id="16264-1919">válido hasta</span><span class="sxs-lookup"><span data-stu-id="16264-1919">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="16264-1920">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="16264-1920">EU Driver's License Number</span></span>

<span data-ttu-id="16264-1921">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="16264-1921">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="16264-1922">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="16264-1922">EU National Identification Number</span></span>

<span data-ttu-id="16264-1923">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационНого номера ЕС](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="16264-1923">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="16264-1924">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="16264-1924">EU Passport Number</span></span>

<span data-ttu-id="16264-1925">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="16264-1925">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="16264-1926">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="16264-1926">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="16264-1927">Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="16264-1927">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="16264-1928">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="16264-1928">EU Tax Identification Number</span></span>

<span data-ttu-id="16264-1929">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогОвого кода ЕС](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="16264-1929">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="16264-1930">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="16264-1930">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="16264-1931">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1931">Format</span></span>

<span data-ttu-id="16264-1932">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="16264-1932">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1933">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1933">Pattern</span></span>

<span data-ttu-id="16264-1934">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="16264-1934">Pattern must include all of the following:</span></span>
- <span data-ttu-id="16264-1935">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="16264-1935">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="16264-1936">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="16264-1936">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="16264-1937">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="16264-1937">Three-digit personal identification number</span></span> 
- <span data-ttu-id="16264-1938">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-1938">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1939">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1939">Checksum</span></span>

<span data-ttu-id="16264-1940">Да</span><span class="sxs-lookup"><span data-stu-id="16264-1940">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1941">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1941">Definition</span></span>

<span data-ttu-id="16264-1942">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1942">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1943">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-1943">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1944">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="16264-1944">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="16264-1945">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-1945">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-1946">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1946">Keywords</span></span>

- <span data-ttu-id="16264-1947">Кэйворд_финниш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="16264-1947">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="16264-1948">Сосиаалитурватуннус</span><span class="sxs-lookup"><span data-stu-id="16264-1948">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="16264-1949">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="16264-1949">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="16264-1950">Персонбетеккнинг</span><span class="sxs-lookup"><span data-stu-id="16264-1950">Personbeteckning</span></span>
- <span data-ttu-id="16264-1951">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-1951">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="16264-1952">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="16264-1952">Finland Passport Number</span></span>

<span data-ttu-id="16264-1953">Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Режекс_финланд_пасспорт_нумбер находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1953">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-1954">находится ключевое слово из Keyword_finland_passport_number.</span><span class="sxs-lookup"><span data-stu-id="16264-1954">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="16264-1955"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="16264-1955"></span></span>
<span data-ttu-id="16264-1956">Ключевые слова Кэйворд_финланд_пасспорт_нумбер Passport Пасси</span><span class="sxs-lookup"><span data-stu-id="16264-1956">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="16264-1957">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="16264-1957">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1958">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1958">Format</span></span>

<span data-ttu-id="16264-1959">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1959">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1960">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1960">Pattern</span></span>

<span data-ttu-id="16264-1961">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="16264-1961">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1962">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1962">Checksum</span></span>

<span data-ttu-id="16264-1963">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1963">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1964">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1964">Definition</span></span>

<span data-ttu-id="16264-1965">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1965">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1966">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1966">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-1967">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-1967">At least one of the following is true:</span></span>
- <span data-ttu-id="16264-1968">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="16264-1968">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="16264-1969">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-1969">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-1970">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1970">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="16264-1971">Кэйворд_френч_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-1971">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="16264-1972">drivers licence</span><span class="sxs-lookup"><span data-stu-id="16264-1972">drivers licence</span></span>
- <span data-ttu-id="16264-1973">drivers license</span><span class="sxs-lookup"><span data-stu-id="16264-1973">drivers license</span></span>
- <span data-ttu-id="16264-1974">driving licence</span><span class="sxs-lookup"><span data-stu-id="16264-1974">driving licence</span></span>
- <span data-ttu-id="16264-1975">driving license</span><span class="sxs-lookup"><span data-stu-id="16264-1975">driving license</span></span>
- <span data-ttu-id="16264-1976">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="16264-1976">permis de conduire</span></span>
- <span data-ttu-id="16264-1977">licence number</span><span class="sxs-lookup"><span data-stu-id="16264-1977">licence number</span></span>
- <span data-ttu-id="16264-1978">license number</span><span class="sxs-lookup"><span data-stu-id="16264-1978">license number</span></span>
- <span data-ttu-id="16264-1979">licence numbers</span><span class="sxs-lookup"><span data-stu-id="16264-1979">licence numbers</span></span>
- <span data-ttu-id="16264-1980">license numbers</span><span class="sxs-lookup"><span data-stu-id="16264-1980">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="16264-1981">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="16264-1981">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="16264-1982">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1982">Format</span></span>

<span data-ttu-id="16264-1983">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1983">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1984">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1984">Pattern</span></span>

<span data-ttu-id="16264-1985">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-1985">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-1986">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-1986">Checksum</span></span>

<span data-ttu-id="16264-1987">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1987">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-1988">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-1988">Definition</span></span>

<span data-ttu-id="16264-1989">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-1989">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-1990">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-1990">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-1991">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-1991">Keywords</span></span>

<span data-ttu-id="16264-1992">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-1992">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="16264-1993">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="16264-1993">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-1994">Format</span><span class="sxs-lookup"><span data-stu-id="16264-1994">Format</span></span>

<span data-ttu-id="16264-1995">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="16264-1995">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-1996">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-1996">Pattern</span></span>

<span data-ttu-id="16264-1997">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="16264-1997">Nine digits and letters:</span></span>
- <span data-ttu-id="16264-1998">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-1998">Two digits</span></span> 
- <span data-ttu-id="16264-1999">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-1999">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="16264-2000">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-2000">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2001">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2001">Checksum</span></span>

<span data-ttu-id="16264-2002">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2002">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2003">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2003">Definition</span></span>

<span data-ttu-id="16264-2004">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2005">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2005">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2006">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="16264-2006">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2007">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2007">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="16264-2008">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-2008">Keyword_passport</span></span>

- <span data-ttu-id="16264-2009">Passport Number</span><span class="sxs-lookup"><span data-stu-id="16264-2009">Passport Number</span></span>
- <span data-ttu-id="16264-2010">Passport No</span><span class="sxs-lookup"><span data-stu-id="16264-2010">Passport No</span></span>
- <span data-ttu-id="16264-2011">Passport#</span><span class="sxs-lookup"><span data-stu-id="16264-2011">Passport #</span></span>
- <span data-ttu-id="16264-2012">Службу</span><span class="sxs-lookup"><span data-stu-id="16264-2012">Passport#</span></span>
- <span data-ttu-id="16264-2013">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="16264-2013">PassportID</span></span>
- <span data-ttu-id="16264-2014">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="16264-2014">Passportno</span></span>
- <span data-ttu-id="16264-2015">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2015">passportnumber</span></span>
- <span data-ttu-id="16264-2016">パスポート</span><span class="sxs-lookup"><span data-stu-id="16264-2016">パスポート</span></span>
- <span data-ttu-id="16264-2017">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="16264-2017">パスポート番号</span></span>
- <span data-ttu-id="16264-2018">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="16264-2018">パスポートのNum</span></span>
- <span data-ttu-id="16264-2019">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="16264-2019">パスポート ＃</span></span> 
- <span data-ttu-id="16264-2020">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="16264-2020">Numéro de passeport</span></span>
- <span data-ttu-id="16264-2021">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="16264-2021">Passeport n °</span></span>
- <span data-ttu-id="16264-2022">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="16264-2022">Passeport Non</span></span>
- <span data-ttu-id="16264-2023">Passeport#</span><span class="sxs-lookup"><span data-stu-id="16264-2023">Passeport #</span></span>
- <span data-ttu-id="16264-2024">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="16264-2024">Passeport#</span></span>
- <span data-ttu-id="16264-2025">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="16264-2025">PasseportNon</span></span>
- <span data-ttu-id="16264-2026">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="16264-2026">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="16264-2027">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="16264-2027">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2028">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2028">Format</span></span>

<span data-ttu-id="16264-2029">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2029">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2030">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2030">Pattern</span></span>

<span data-ttu-id="16264-2031">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="16264-2031">Must match one of two patterns:</span></span>
- <span data-ttu-id="16264-2032">13 цифр, за которыми следует пробел, за которым следуют две цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-2032">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="16264-2033">или</span><span class="sxs-lookup"><span data-stu-id="16264-2033">or</span></span>
- <span data-ttu-id="16264-2034">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2034">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2035">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2035">Checksum</span></span>

<span data-ttu-id="16264-2036">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2036">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2037">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2037">Definition</span></span>

<span data-ttu-id="16264-2038">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2038">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2039">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-2039">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2040">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="16264-2040">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="16264-2041">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2041">The checksum passes.</span></span>

<span data-ttu-id="16264-2042">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2042">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2043">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-2043">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2044">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="16264-2044">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="16264-2045">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2045">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2046">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2046">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="16264-2047">Кэйворд_фр_инси</span><span class="sxs-lookup"><span data-stu-id="16264-2047">Keyword_fr_insee</span></span>

- <span data-ttu-id="16264-2048">INSEE</span><span class="sxs-lookup"><span data-stu-id="16264-2048">insee</span></span>
- <span data-ttu-id="16264-2049">securité sociale</span><span class="sxs-lookup"><span data-stu-id="16264-2049">securité sociale</span></span>
- <span data-ttu-id="16264-2050">securite sociale</span><span class="sxs-lookup"><span data-stu-id="16264-2050">securite sociale</span></span>
- <span data-ttu-id="16264-2051">national id</span><span class="sxs-lookup"><span data-stu-id="16264-2051">national id</span></span>
- <span data-ttu-id="16264-2052">national identification</span><span class="sxs-lookup"><span data-stu-id="16264-2052">national identification</span></span>
- <span data-ttu-id="16264-2053">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="16264-2053">numéro d'identité</span></span>
- <span data-ttu-id="16264-2054">no d'identité</span><span class="sxs-lookup"><span data-stu-id="16264-2054">no d'identité</span></span>
- <span data-ttu-id="16264-2055">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-2055">no.</span></span> <span data-ttu-id="16264-2056">д'идентитé</span><span class="sxs-lookup"><span data-stu-id="16264-2056">d'identité</span></span>
- <span data-ttu-id="16264-2057">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="16264-2057">numero d'identite</span></span>
- <span data-ttu-id="16264-2058">no d'identite</span><span class="sxs-lookup"><span data-stu-id="16264-2058">no d'identite</span></span>
- <span data-ttu-id="16264-2059">Нет.</span><span class="sxs-lookup"><span data-stu-id="16264-2059">no.</span></span> <span data-ttu-id="16264-2060">д'идентите</span><span class="sxs-lookup"><span data-stu-id="16264-2060">d'identite</span></span>
- <span data-ttu-id="16264-2061">social security number</span><span class="sxs-lookup"><span data-stu-id="16264-2061">social security number</span></span>
- <span data-ttu-id="16264-2062">social security code</span><span class="sxs-lookup"><span data-stu-id="16264-2062">social security code</span></span>
- <span data-ttu-id="16264-2063">social insurance number</span><span class="sxs-lookup"><span data-stu-id="16264-2063">social insurance number</span></span>
- <span data-ttu-id="16264-2064">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="16264-2064">le numéro d'identification nationale</span></span>
- <span data-ttu-id="16264-2065">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="16264-2065">d'identité nationale</span></span>
- <span data-ttu-id="16264-2066">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="16264-2066">numéro de sécurité sociale</span></span>
- <span data-ttu-id="16264-2067">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="16264-2067">le code de la sécurité sociale</span></span>
- <span data-ttu-id="16264-2068">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="16264-2068">numéro d'assurance sociale</span></span>
- <span data-ttu-id="16264-2069">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="16264-2069">numéro de sécu</span></span>
- <span data-ttu-id="16264-2070">code sécu</span><span class="sxs-lookup"><span data-stu-id="16264-2070">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="16264-2071">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="16264-2071">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2072">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2072">Format</span></span>

<span data-ttu-id="16264-2073">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="16264-2073">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2074">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2074">Pattern</span></span>

<span data-ttu-id="16264-2075">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-2075">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="16264-2076">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="16264-2076">A digit or letter</span></span> 
- <span data-ttu-id="16264-2077">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2077">Two digits</span></span> 
- <span data-ttu-id="16264-2078">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="16264-2078">Six digits or letters</span></span> 
- <span data-ttu-id="16264-2079">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="16264-2079">A digit</span></span> 
- <span data-ttu-id="16264-2080">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="16264-2080">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2081">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2081">Checksum</span></span>

<span data-ttu-id="16264-2082">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2083">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2083">Definition</span></span>

<span data-ttu-id="16264-2084">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2084">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2085">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2085">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2086">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-2086">At least one of the following is true:</span></span>
    - <span data-ttu-id="16264-2087">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="16264-2087">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="16264-2088">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="16264-2088">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="16264-2089">найдено ключевое слово из Keyword_german_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="16264-2089">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="16264-2090">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2090">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2091">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2091">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="16264-2092">Кэйворд_жерман_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2092">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="16264-2093">Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2093">Führerschein</span></span>
- <span data-ttu-id="16264-2094">Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2094">Fuhrerschein</span></span>
- <span data-ttu-id="16264-2095">Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2095">Fuehrerschein</span></span>
- <span data-ttu-id="16264-2096">Фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2096">Führerscheinnummer</span></span>
- <span data-ttu-id="16264-2097">Фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2097">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="16264-2098">Фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2098">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="16264-2099">Фüхрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="16264-2099">Führerschein-</span></span> 
- <span data-ttu-id="16264-2100">Фухрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="16264-2100">Fuhrerschein-</span></span> 
- <span data-ttu-id="16264-2101">Фуехрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="16264-2101">Fuehrerschein-</span></span> 
- <span data-ttu-id="16264-2102">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="16264-2102">FührerscheinnummerNr</span></span>
- <span data-ttu-id="16264-2103">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="16264-2103">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="16264-2104">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="16264-2104">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="16264-2105">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="16264-2105">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="16264-2106">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="16264-2106">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="16264-2107">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="16264-2107">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="16264-2108">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="16264-2108">Führerschein- Nr</span></span>
- <span data-ttu-id="16264-2109">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="16264-2109">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="16264-2110">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="16264-2110">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="16264-2111">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="16264-2111">Führerschein- Klasse</span></span> 
- <span data-ttu-id="16264-2112">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="16264-2112">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="16264-2113">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="16264-2113">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="16264-2114">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="16264-2114">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="16264-2115">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="16264-2115">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="16264-2116">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="16264-2116">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="16264-2117">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="16264-2117">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="16264-2118">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="16264-2118">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="16264-2119">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="16264-2119">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="16264-2120">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="16264-2120">Führerschein- Nr</span></span> 
- <span data-ttu-id="16264-2121">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="16264-2121">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="16264-2122">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="16264-2122">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="16264-2123">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="16264-2123">Führerschein- Klasse</span></span> 
- <span data-ttu-id="16264-2124">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="16264-2124">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="16264-2125">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="16264-2125">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="16264-2126">DL</span><span class="sxs-lookup"><span data-stu-id="16264-2126">DL</span></span> 
- <span data-ttu-id="16264-2127">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="16264-2127">DLS</span></span>
- <span data-ttu-id="16264-2128">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="16264-2128">Driv Lic</span></span> 
- <span data-ttu-id="16264-2129">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="16264-2129">Driv Licen</span></span> 
- <span data-ttu-id="16264-2130">Driv License</span><span class="sxs-lookup"><span data-stu-id="16264-2130">Driv License</span></span>
- <span data-ttu-id="16264-2131">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2131">Driv Licenses</span></span> 
- <span data-ttu-id="16264-2132">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="16264-2132">Driv Licence</span></span> 
- <span data-ttu-id="16264-2133">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="16264-2133">Driv Licences</span></span> 
- <span data-ttu-id="16264-2134">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="16264-2134">Driv Lic</span></span> 
- <span data-ttu-id="16264-2135">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="16264-2135">Driver Licen</span></span> 
- <span data-ttu-id="16264-2136">Driver License</span><span class="sxs-lookup"><span data-stu-id="16264-2136">Driver License</span></span> 
- <span data-ttu-id="16264-2137">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2137">Driver Licenses</span></span> 
- <span data-ttu-id="16264-2138">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="16264-2138">Driver Licence</span></span> 
- <span data-ttu-id="16264-2139">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="16264-2139">Driver Licences</span></span> 
- <span data-ttu-id="16264-2140">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="16264-2140">Drivers Lic</span></span> 
- <span data-ttu-id="16264-2141">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="16264-2141">Drivers Licen</span></span> 
- <span data-ttu-id="16264-2142">Drivers License</span><span class="sxs-lookup"><span data-stu-id="16264-2142">Drivers License</span></span> 
- <span data-ttu-id="16264-2143">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2143">Drivers Licenses</span></span> 
- <span data-ttu-id="16264-2144">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="16264-2144">Drivers Licence</span></span> 
- <span data-ttu-id="16264-2145">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="16264-2145">Drivers Licences</span></span> 
- <span data-ttu-id="16264-2146">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="16264-2146">Driver's Lic</span></span> 
- <span data-ttu-id="16264-2147">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="16264-2147">Driver's Licen</span></span> 
- <span data-ttu-id="16264-2148">Driver's License</span><span class="sxs-lookup"><span data-stu-id="16264-2148">Driver's License</span></span> 
- <span data-ttu-id="16264-2149">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2149">Driver's Licenses</span></span> 
- <span data-ttu-id="16264-2150">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="16264-2150">Driver's Licence</span></span> 
- <span data-ttu-id="16264-2151">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="16264-2151">Driver's Licences</span></span> 
- <span data-ttu-id="16264-2152">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="16264-2152">Driving Lic</span></span> 
- <span data-ttu-id="16264-2153">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="16264-2153">Driving Licen</span></span> 
- <span data-ttu-id="16264-2154">Driving License</span><span class="sxs-lookup"><span data-stu-id="16264-2154">Driving License</span></span> 
- <span data-ttu-id="16264-2155">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2155">Driving Licenses</span></span> 
- <span data-ttu-id="16264-2156">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="16264-2156">Driving Licence</span></span> 
- <span data-ttu-id="16264-2157">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="16264-2157">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="16264-2158">Кэйворд_жерман_дриверс_лиценсе_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="16264-2158">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="16264-2159">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2159">Nr-Führerschein</span></span> 
- <span data-ttu-id="16264-2160">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2160">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="16264-2161">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2161">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="16264-2162">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2162">No-Führerschein</span></span> 
- <span data-ttu-id="16264-2163">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2163">No-Fuhrerschein</span></span> 
- <span data-ttu-id="16264-2164">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2164">No-Fuehrerschein</span></span> 
- <span data-ttu-id="16264-2165">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2165">N-Führerschein</span></span> 
- <span data-ttu-id="16264-2166">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2166">N-Fuhrerschein</span></span> 
- <span data-ttu-id="16264-2167">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2167">N-Fuehrerschein</span></span>
- <span data-ttu-id="16264-2168">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2168">Nr-Führerschein</span></span> 
- <span data-ttu-id="16264-2169">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2169">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="16264-2170">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2170">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="16264-2171">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2171">No-Führerschein</span></span> 
- <span data-ttu-id="16264-2172">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2172">No-Fuhrerschein</span></span> 
- <span data-ttu-id="16264-2173">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2173">No-Fuehrerschein</span></span> 
- <span data-ttu-id="16264-2174">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2174">N-Führerschein</span></span> 
- <span data-ttu-id="16264-2175">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2175">N-Fuhrerschein</span></span> 
- <span data-ttu-id="16264-2176">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="16264-2176">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="16264-2177">Кэйворд_жерман_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-2177">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="16264-2178">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-2178">ausstellungsdatum</span></span>
- <span data-ttu-id="16264-2179">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="16264-2179">ausstellungsort</span></span>
- <span data-ttu-id="16264-2180">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="16264-2180">ausstellende behöde</span></span>
- <span data-ttu-id="16264-2181">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="16264-2181">ausstellende behorde</span></span>
- <span data-ttu-id="16264-2182">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="16264-2182">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="16264-2183">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="16264-2183">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2184">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2184">Format</span></span>

<span data-ttu-id="16264-2185">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="16264-2185">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2186">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2186">Pattern</span></span>

<span data-ttu-id="16264-2187">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="16264-2187">Pattern must include all of the following:</span></span>
- <span data-ttu-id="16264-2188">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="16264-2188">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="16264-2189">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2189">Three digits</span></span> 
- <span data-ttu-id="16264-2190">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="16264-2190">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="16264-2191">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="16264-2191">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2192">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2192">Checksum</span></span>

<span data-ttu-id="16264-2193">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2194">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2194">Definition</span></span>

<span data-ttu-id="16264-2195">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2196">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2196">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2197">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="16264-2197">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="16264-2198">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2198">The checksum passes.</span></span>

<span data-ttu-id="16264-2199">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2199">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2200">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2200">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2201">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="16264-2201">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="16264-2202">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2202">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2203">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2203">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="16264-2204">Кэйворд_жерман_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-2204">Keyword_german_passport</span></span>

- <span data-ttu-id="16264-2205">реисепасс</span><span class="sxs-lookup"><span data-stu-id="16264-2205">reisepass</span></span>
- <span data-ttu-id="16264-2206">реисепассе</span><span class="sxs-lookup"><span data-stu-id="16264-2206">reisepasse</span></span>
- <span data-ttu-id="16264-2207">реисепасснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2207">reisepassnummer</span></span>
- <span data-ttu-id="16264-2208">службу</span><span class="sxs-lookup"><span data-stu-id="16264-2208">passport</span></span>
- <span data-ttu-id="16264-2209">паспорты</span><span class="sxs-lookup"><span data-stu-id="16264-2209">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="16264-2210">Кэйворд_жерман_пасспорт_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="16264-2210">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="16264-2211">жебуртсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-2211">geburtsdatum</span></span>
- <span data-ttu-id="16264-2212">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="16264-2212">ausstellungsdatum</span></span>
- <span data-ttu-id="16264-2213">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="16264-2213">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="16264-2214">Кэйворд_жерман_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2214">Keyword_german_passport_number</span></span>

<span data-ttu-id="16264-2215">No — Реисепасс НР — Реисепасс</span><span class="sxs-lookup"><span data-stu-id="16264-2215">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="16264-2216">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="16264-2216">Keyword_german_passport1</span></span>

<span data-ttu-id="16264-2217">Реисепасс — НР</span><span class="sxs-lookup"><span data-stu-id="16264-2217">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="16264-2218">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="16264-2218">Keyword_german_passport2</span></span>

<span data-ttu-id="16264-2219">бнатионалит. t</span><span class="sxs-lookup"><span data-stu-id="16264-2219">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="16264-2220">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="16264-2220">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2221">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2221">Format</span></span>

<span data-ttu-id="16264-2222">С 1 ноября 2010: девять букв и цифр</span><span class="sxs-lookup"><span data-stu-id="16264-2222">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="16264-2223">От 1 апреля 1987 до 31 октября 2010:10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2223">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2224">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2224">Pattern</span></span>

<span data-ttu-id="16264-2225">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="16264-2225">Since 1 November 2010:</span></span>
- <span data-ttu-id="16264-2226">одна буква (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-2226">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="16264-2227">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2227">Eight digits</span></span>

<span data-ttu-id="16264-2228">От 1 апреля 1987 до 31 октября 2010:</span><span class="sxs-lookup"><span data-stu-id="16264-2228">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="16264-2229">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2229">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2230">Checksum</span></span>

<span data-ttu-id="16264-2231">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2231">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2232">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2232">Definition</span></span>

<span data-ttu-id="16264-2233">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2233">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2234">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2234">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2235">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="16264-2235">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2236">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2236">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="16264-2237">Кэйворд_жермани_ид_кард</span><span class="sxs-lookup"><span data-stu-id="16264-2237">Keyword_germany_id_card</span></span>

- <span data-ttu-id="16264-2238">Identity Card</span><span class="sxs-lookup"><span data-stu-id="16264-2238">Identity Card</span></span>
- <span data-ttu-id="16264-2239">ИД</span><span class="sxs-lookup"><span data-stu-id="16264-2239">ID</span></span>
- <span data-ttu-id="16264-2240">Процедура</span><span class="sxs-lookup"><span data-stu-id="16264-2240">Identification</span></span>
- <span data-ttu-id="16264-2241">Персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="16264-2241">Personalausweis</span></span>
- <span data-ttu-id="16264-2242">Идентифизиерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2242">Identifizierungsnummer</span></span>
- <span data-ttu-id="16264-2243">Аусвеис</span><span class="sxs-lookup"><span data-stu-id="16264-2243">Ausweis</span></span>
- <span data-ttu-id="16264-2244">Идентификатион</span><span class="sxs-lookup"><span data-stu-id="16264-2244">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="16264-2245">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="16264-2245">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="16264-2246">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2246">Format</span></span>

<span data-ttu-id="16264-2247">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="16264-2247">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2248">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2248">Pattern</span></span>

<span data-ttu-id="16264-2249">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="16264-2249">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="16264-2250">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="16264-2250">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="16264-2251">тире;</span><span class="sxs-lookup"><span data-stu-id="16264-2251">A dash</span></span> 
- <span data-ttu-id="16264-2252">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2252">Six digits</span></span>

<span data-ttu-id="16264-2253">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="16264-2253">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="16264-2254">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="16264-2254">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="16264-2255">тире;</span><span class="sxs-lookup"><span data-stu-id="16264-2255">A dash</span></span> 
- <span data-ttu-id="16264-2256">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2256">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2257">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2257">Checksum</span></span>

<span data-ttu-id="16264-2258">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2258">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2259">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2259">Definition</span></span>

<span data-ttu-id="16264-2260">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2260">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2261">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2261">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2262">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="16264-2262">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2263">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2263">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="16264-2264">Кэйворд_грице_ид_кард</span><span class="sxs-lookup"><span data-stu-id="16264-2264">Keyword_greece_id_card</span></span>

- <span data-ttu-id="16264-2265">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="16264-2265">Greek identity Card</span></span>
- <span data-ttu-id="16264-2266">Таутотита</span><span class="sxs-lookup"><span data-stu-id="16264-2266">Tautotita</span></span>
- <span data-ttu-id="16264-2267">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="16264-2267">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="16264-2268">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="16264-2268">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="16264-2269">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="16264-2269">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2270">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2270">Format</span></span>

<span data-ttu-id="16264-2271">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="16264-2271">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2272">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2272">Pattern</span></span>

<span data-ttu-id="16264-2273">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="16264-2273">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="16264-2274">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-2274">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="16264-2275">шесть цифр; </span><span class="sxs-lookup"><span data-stu-id="16264-2275">Six digits</span></span> 
- <span data-ttu-id="16264-2276">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="16264-2276">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2277">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2277">Checksum</span></span>

<span data-ttu-id="16264-2278">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2278">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2279">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2279">Definition</span></span>

<span data-ttu-id="16264-2280">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2280">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2281">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2281">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2282">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="16264-2282">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="16264-2283">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2283">The checksum passes.</span></span>

<span data-ttu-id="16264-2284">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2284">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2285">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2285">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2286">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2286">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2287">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2287">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="16264-2288">Кэйворд_хонг_конг_ид_кард</span><span class="sxs-lookup"><span data-stu-id="16264-2288">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="16264-2289">идентификационная карточка Гонконг</span><span class="sxs-lookup"><span data-stu-id="16264-2289">hong kong identity card</span></span>
- <span data-ttu-id="16264-2290">ХКИДК</span><span class="sxs-lookup"><span data-stu-id="16264-2290">HKIDC</span></span>
- <span data-ttu-id="16264-2291">id card</span><span class="sxs-lookup"><span data-stu-id="16264-2291">id card</span></span>
- <span data-ttu-id="16264-2292">identity card</span><span class="sxs-lookup"><span data-stu-id="16264-2292">identity card</span></span>
- <span data-ttu-id="16264-2293">идентификационная карточка HK</span><span class="sxs-lookup"><span data-stu-id="16264-2293">hk identity card</span></span>
- <span data-ttu-id="16264-2294">Идентификатор Гонконг</span><span class="sxs-lookup"><span data-stu-id="16264-2294">hong kong id</span></span>
- <span data-ttu-id="16264-2295">香港身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2295">香港身份證</span></span>
- <span data-ttu-id="16264-2296">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2296">香港永久性居民身份證</span></span>
- <span data-ttu-id="16264-2297">身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2297">身份證</span></span>
- <span data-ttu-id="16264-2298">身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2298">身份証</span></span>
- <span data-ttu-id="16264-2299">身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2299">身分證</span></span>
- <span data-ttu-id="16264-2300">身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2300">身分証</span></span>
- <span data-ttu-id="16264-2301">香港身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2301">香港身份証</span></span>
- <span data-ttu-id="16264-2302">香港身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2302">香港身分證</span></span>
- <span data-ttu-id="16264-2303">香港身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2303">香港身分証</span></span>
- <span data-ttu-id="16264-2304">香港身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2304">香港身份證</span></span>
- <span data-ttu-id="16264-2305">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2305">香港居民身份證</span></span>
- <span data-ttu-id="16264-2306">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2306">香港居民身份証</span></span>
- <span data-ttu-id="16264-2307">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2307">香港居民身分證</span></span>
- <span data-ttu-id="16264-2308">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2308">香港居民身分証</span></span>
- <span data-ttu-id="16264-2309">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2309">香港永久性居民身份証</span></span>
- <span data-ttu-id="16264-2310">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2310">香港永久性居民身分證</span></span>
- <span data-ttu-id="16264-2311">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2311">香港永久性居民身分証</span></span>
- <span data-ttu-id="16264-2312">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2312">香港永久性居民身份證</span></span>
- <span data-ttu-id="16264-2313">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2313">香港非永久性居民身份證</span></span>
- <span data-ttu-id="16264-2314">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2314">香港非永久性居民身份証</span></span>
- <span data-ttu-id="16264-2315">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2315">香港非永久性居民身分證</span></span>
- <span data-ttu-id="16264-2316">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2316">香港非永久性居民身分証</span></span>
- <span data-ttu-id="16264-2317">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2317">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="16264-2318">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2318">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="16264-2319">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2319">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="16264-2320">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2320">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="16264-2321">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="16264-2321">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="16264-2322">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="16264-2322">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="16264-2323">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="16264-2323">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="16264-2324">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="16264-2324">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="16264-2325">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="16264-2325">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2326">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2326">Format</span></span>

<span data-ttu-id="16264-2327">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2327">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2328">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2328">Pattern</span></span>

<span data-ttu-id="16264-2329">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2329">10 letters or digits:</span></span>
- <span data-ttu-id="16264-2330">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-2330">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="16264-2331">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2331">Four digits</span></span> 
- <span data-ttu-id="16264-2332">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="16264-2332">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2333">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2333">Checksum</span></span>

<span data-ttu-id="16264-2334">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2335">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2335">Definition</span></span>

<span data-ttu-id="16264-2336">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2337">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2337">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2338">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="16264-2338">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="16264-2339">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2339">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2340">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2340">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="16264-2341">Кэйворд_индиа_перманент_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2341">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="16264-2342">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2342">Permanent Account Number</span></span> 
- <span data-ttu-id="16264-2343">ПАНОРАМИРОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16264-2343">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="16264-2344">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="16264-2344">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2345">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2345">Format</span></span>

<span data-ttu-id="16264-2346">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="16264-2346">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2347">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2347">Pattern</span></span>

<span data-ttu-id="16264-2348">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2348">12 digits:</span></span>
- <span data-ttu-id="16264-2349">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-2349">Four digits</span></span> 
- <span data-ttu-id="16264-2350">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="16264-2350">An optional space or dash</span></span> 
- <span data-ttu-id="16264-2351">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-2351">Four digits</span></span> 
- <span data-ttu-id="16264-2352">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="16264-2352">An optional space or dash</span></span> 
- <span data-ttu-id="16264-2353">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="16264-2353">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2354">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2354">Checksum</span></span>

<span data-ttu-id="16264-2355">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2355">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2356">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2356">Definition</span></span>

<span data-ttu-id="16264-2357">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2357">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-2358">находится ключевое слово из Keyword_india_aadhar;</span><span class="sxs-lookup"><span data-stu-id="16264-2358">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="16264-2359">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2359">The checksum passes.</span></span>
<span data-ttu-id="16264-2360">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-2361">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2361">The checksum passes.</span></span>
<span data-ttu-id="16264-2362"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="16264-2362"></span></span>

### <a name="keywords"></a><span data-ttu-id="16264-2363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2363">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="16264-2364">Кэйворд_индиа_аадхар</span><span class="sxs-lookup"><span data-stu-id="16264-2364">Keyword_india_aadhar</span></span>
- <span data-ttu-id="16264-2365">Аадхар</span><span class="sxs-lookup"><span data-stu-id="16264-2365">Aadhar</span></span>
- <span data-ttu-id="16264-2366">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="16264-2366">Aadhaar</span></span>
- <span data-ttu-id="16264-2367">UID</span><span class="sxs-lookup"><span data-stu-id="16264-2367">UID</span></span>
- <span data-ttu-id="16264-2368">आधार</span><span class="sxs-lookup"><span data-stu-id="16264-2368">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="16264-2369">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="16264-2369">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2370">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2370">Format</span></span>

<span data-ttu-id="16264-2371">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="16264-2371">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2372">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2372">Pattern</span></span>

<span data-ttu-id="16264-2373">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2373">16 digits:</span></span>
- <span data-ttu-id="16264-2374">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="16264-2374">Two-digit province code</span></span> 
- <span data-ttu-id="16264-2375">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="16264-2375">A period (optional)</span></span> 
- <span data-ttu-id="16264-2376">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="16264-2376">Two-digit regency or city code</span></span> 
- <span data-ttu-id="16264-2377">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="16264-2377">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="16264-2378">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="16264-2378">A period (optional)</span></span> 
- <span data-ttu-id="16264-2379">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="16264-2379">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="16264-2380">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="16264-2380">A period (optional)</span></span> 
- <span data-ttu-id="16264-2381">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-2381">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2382">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2382">Checksum</span></span>

<span data-ttu-id="16264-2383">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2383">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2384">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2384">Definition</span></span>

<span data-ttu-id="16264-2385">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2386">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-2386">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2387">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="16264-2387">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="16264-2388">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2388">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2389">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-2389">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2390">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2390">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="16264-2391">Кэйворд_индонесиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="16264-2391">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="16264-2392">KTP</span><span class="sxs-lookup"><span data-stu-id="16264-2392">KTP</span></span>
- <span data-ttu-id="16264-2393">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="16264-2393">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="16264-2394">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="16264-2394">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="16264-2395">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="16264-2395">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2396">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2396">Format</span></span>

<span data-ttu-id="16264-2397">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="16264-2397">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2398">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2398">Pattern</span></span>

<span data-ttu-id="16264-2399">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="16264-2399">Pattern must include all of the following:</span></span>

- <span data-ttu-id="16264-2400">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="16264-2400">Two-letter country code</span></span>
- <span data-ttu-id="16264-2401">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="16264-2401">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="16264-2402">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="16264-2402">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="16264-2403">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2403">1-3 letters or digits</span></span>

<span data-ttu-id="16264-p134">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="16264-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="16264-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="16264-2406">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2407">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2407">Checksum</span></span>

<span data-ttu-id="16264-2408">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2408">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2409">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2409">Definition</span></span>

<span data-ttu-id="16264-2410">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2410">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2411">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2411">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2412">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2412">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2413">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2413">Keywords</span></span>

<span data-ttu-id="16264-2414">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2414">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="16264-2415">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="16264-2415">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="16264-2416">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2416">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="16264-2417">IPv4</span><span class="sxs-lookup"><span data-stu-id="16264-2417">IPv4:</span></span>
<span data-ttu-id="16264-2418">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="16264-2418">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="16264-2419">Поддерживающ</span><span class="sxs-lookup"><span data-stu-id="16264-2419">IPv6:</span></span>
<span data-ttu-id="16264-2420"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="16264-2420">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2421">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2421">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2422">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2422">Checksum</span></span>

<span data-ttu-id="16264-2423">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2424">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2424">Definition</span></span>

<span data-ttu-id="16264-2425">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2425">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2426">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2426">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2427">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="16264-2427">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="16264-2428">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2428">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2429">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2429">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2430">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="16264-2430">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="16264-2431">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2431">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2432">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2432">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2433">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="16264-2433">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2434">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2434">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="16264-2435">Кэйворд_ипаддресс</span><span class="sxs-lookup"><span data-stu-id="16264-2435">Keyword_ipaddress</span></span>

- <span data-ttu-id="16264-2436">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-2436">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="16264-2437">ip address</span><span class="sxs-lookup"><span data-stu-id="16264-2437">ip address</span></span> 
- <span data-ttu-id="16264-2438">ip addresses</span><span class="sxs-lookup"><span data-stu-id="16264-2438">ip addresses</span></span>
- <span data-ttu-id="16264-2439">internet protocol</span><span class="sxs-lookup"><span data-stu-id="16264-2439">internet protocol</span></span>
- <span data-ttu-id="16264-2440">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="16264-2440">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="16264-2441">Международная классификация Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="16264-2441">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2442">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2442">Format</span></span>

<span data-ttu-id="16264-2443">Dictionary</span><span class="sxs-lookup"><span data-stu-id="16264-2443">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2444">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2444">Pattern</span></span>

<span data-ttu-id="16264-2445">Недопустим</span><span class="sxs-lookup"><span data-stu-id="16264-2445">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2446">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2446">Checksum</span></span>

<span data-ttu-id="16264-2447">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2447">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2448">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2448">Definition</span></span>

<span data-ttu-id="16264-2449">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2449">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2450">Найдено ключевое слово из Dictionary_icd_10_cm.</span><span class="sxs-lookup"><span data-stu-id="16264-2450">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="16264-2451">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2451">Keywords</span></span>

<span data-ttu-id="16264-2452">Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятОй редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="16264-2452">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="16264-2453">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="16264-2453">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="16264-2454">Международная классификация Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="16264-2454">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2455">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2455">Format</span></span>

<span data-ttu-id="16264-2456">Dictionary</span><span class="sxs-lookup"><span data-stu-id="16264-2456">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2457">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2457">Pattern</span></span>

<span data-ttu-id="16264-2458">Недопустим</span><span class="sxs-lookup"><span data-stu-id="16264-2458">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2459">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2459">Checksum</span></span>

<span data-ttu-id="16264-2460">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2460">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2461">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2461">Definition</span></span>

<span data-ttu-id="16264-2462">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2462">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2463">Найдено ключевое слово из Dictionary_icd_9_cm.</span><span class="sxs-lookup"><span data-stu-id="16264-2463">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2464">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2464">Keywords</span></span>

<span data-ttu-id="16264-2465">Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятОй редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="16264-2465">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="16264-2466">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="16264-2466">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="16264-2467">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="16264-2467">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2468">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2468">Format</span></span>

<span data-ttu-id="16264-2469">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="16264-2469">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="16264-2470">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="16264-2470">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="16264-2471">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="16264-2471">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="16264-2472">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="16264-2472">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2473">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2473">Pattern</span></span>

<span data-ttu-id="16264-2474">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="16264-2474">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="16264-2475">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-2475">Seven digits</span></span> 
- <span data-ttu-id="16264-2476">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="16264-2476">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="16264-2477">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="16264-2477">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="16264-2478">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-2478">Seven digits</span></span> 
- <span data-ttu-id="16264-2479">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="16264-2479">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="16264-2480">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="16264-2480">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2481">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2481">Checksum</span></span>

<span data-ttu-id="16264-2482">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2482">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2483">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2483">Definition</span></span>

<span data-ttu-id="16264-2484">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2484">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2485">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-2485">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2486">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-2486">One of the following is true:</span></span>
    - <span data-ttu-id="16264-2487">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="16264-2487">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="16264-2488">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-2488">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="16264-2489">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2489">The checksum passes.</span></span>

<span data-ttu-id="16264-2490">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2490">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2491">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2491">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2492">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2492">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2493">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2493">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="16264-2494">Кэйворд_иреланд_ппс</span><span class="sxs-lookup"><span data-stu-id="16264-2494">Keyword_ireland_pps</span></span>

- <span data-ttu-id="16264-2495">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="16264-2495">Personal Public Service Number</span></span> 
- <span data-ttu-id="16264-2496">PPS Number</span><span class="sxs-lookup"><span data-stu-id="16264-2496">PPS Number</span></span> 
- <span data-ttu-id="16264-2497">PPS Num</span><span class="sxs-lookup"><span data-stu-id="16264-2497">PPS Num</span></span> 
- <span data-ttu-id="16264-2498">PPS No.</span><span class="sxs-lookup"><span data-stu-id="16264-2498">PPS No.</span></span> 
- <span data-ttu-id="16264-2499">PPS #</span><span class="sxs-lookup"><span data-stu-id="16264-2499">PPS #</span></span> 
- <span data-ttu-id="16264-2500">PPS</span><span class="sxs-lookup"><span data-stu-id="16264-2500">PPS#</span></span> 
- <span data-ttu-id="16264-2501">ППСН</span><span class="sxs-lookup"><span data-stu-id="16264-2501">PPSN</span></span> 
- <span data-ttu-id="16264-2502">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="16264-2502">Public Services Card</span></span> 
- <span data-ttu-id="16264-2503">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="16264-2503">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="16264-2504">Уимх.</span><span class="sxs-lookup"><span data-stu-id="16264-2504">Uimh.</span></span> <span data-ttu-id="16264-2505">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="16264-2505">PSP</span></span> 
- <span data-ttu-id="16264-2506">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="16264-2506">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="16264-2507">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="16264-2507">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2508">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2508">Format</span></span>

<span data-ttu-id="16264-2509">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2509">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2510">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2510">Pattern</span></span>

<span data-ttu-id="16264-2511">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="16264-2511">Formatted:</span></span>
- <span data-ttu-id="16264-2512">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2512">Two digits</span></span> 
- <span data-ttu-id="16264-2513">Тире</span><span class="sxs-lookup"><span data-stu-id="16264-2513">A dash</span></span> 
- <span data-ttu-id="16264-2514">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2514">Three digits</span></span> 
- <span data-ttu-id="16264-2515">Тире</span><span class="sxs-lookup"><span data-stu-id="16264-2515">A dash</span></span> 
- <span data-ttu-id="16264-2516">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="16264-2516">Eight digits</span></span>

<span data-ttu-id="16264-2517">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="16264-2517">Unformatted:</span></span>
- <span data-ttu-id="16264-2518">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2518">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2519">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2519">Checksum</span></span>

<span data-ttu-id="16264-2520">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2520">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2521">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2521">Definition</span></span>

<span data-ttu-id="16264-2522">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2522">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2523">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2523">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2524">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="16264-2524">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2525">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2525">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="16264-2526">Кэйворд_исраел_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2526">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="16264-2527">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2527">Bank Account Number</span></span> 
- <span data-ttu-id="16264-2528">Bank Account</span><span class="sxs-lookup"><span data-stu-id="16264-2528">Bank Account</span></span> 
- <span data-ttu-id="16264-2529">Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2529">Account Number</span></span> 
- <span data-ttu-id="16264-2530">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="16264-2530">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="16264-2531">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="16264-2531">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="16264-2532">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2532">Format</span></span>

<span data-ttu-id="16264-2533">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2534">Pattern</span></span>

<span data-ttu-id="16264-2535">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2536">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2536">Checksum</span></span>

<span data-ttu-id="16264-2537">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2537">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2538">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2538">Definition</span></span>

<span data-ttu-id="16264-2539">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2540">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2540">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2541">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="16264-2541">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="16264-2542">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2542">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2543">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2543">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="16264-2544">Кэйворд_исраел_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="16264-2544">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="16264-2545">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="16264-2545">מספר זהות</span></span> 
- <span data-ttu-id="16264-2546">National ID Number</span><span class="sxs-lookup"><span data-stu-id="16264-2546">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="16264-2547">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="16264-2547">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2548">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2548">Format</span></span>

<span data-ttu-id="16264-2549">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2549">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2550">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2550">Pattern</span></span>

- <span data-ttu-id="16264-2551">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2551">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="16264-2552">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-2552">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="16264-2553">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-2553">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="16264-2554">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="16264-2554">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="16264-2555">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-2555">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2556">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2556">Checksum</span></span>

<span data-ttu-id="16264-2557">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2557">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2558">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2558">Definition</span></span>

<span data-ttu-id="16264-2559">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2559">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2560">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2560">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2561">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="16264-2561">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2562">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2562">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="16264-2563">Кэйворд_итали_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2563">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="16264-2564">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="16264-2564">numero di patente di guida</span></span> 
- <span data-ttu-id="16264-2565">patente di guida</span><span class="sxs-lookup"><span data-stu-id="16264-2565">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="16264-2566">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="16264-2566">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2567">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2567">Format</span></span>

<span data-ttu-id="16264-2568">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2568">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2569">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2569">Pattern</span></span>

<span data-ttu-id="16264-2570">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="16264-2570">Bank account number:</span></span>
- <span data-ttu-id="16264-2571">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2571">Seven or eight digits</span></span>
- <span data-ttu-id="16264-2572">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="16264-2572">Bank account branch code:</span></span>
- <span data-ttu-id="16264-2573">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2573">Four digits</span></span> 
- <span data-ttu-id="16264-2574">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="16264-2574">A space or dash (optional)</span></span> 
- <span data-ttu-id="16264-2575">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2575">Three digits</span></span>

<span data-ttu-id="16264-2576">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2576">Checksum</span></span>

<span data-ttu-id="16264-2577">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2577">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2578">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2578">Definition</span></span>

<span data-ttu-id="16264-2579">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2580">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-2580">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2581">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="16264-2581">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="16264-2582">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-2582">One of the following is true:</span></span>
- <span data-ttu-id="16264-2583">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2583">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2584">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="16264-2584">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="16264-2585">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2586">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2586">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2587">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="16264-2587">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2588">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2588">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="16264-2589">Кэйворд_жп_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="16264-2589">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="16264-2590">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2590">Checking Account Number</span></span> 
- <span data-ttu-id="16264-2591">Checking Account</span><span class="sxs-lookup"><span data-stu-id="16264-2591">Checking Account</span></span> 
- <span data-ttu-id="16264-2592">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="16264-2592">Checking Account #</span></span> 
- <span data-ttu-id="16264-2593">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-2593">Checking Acct Number</span></span> 
- <span data-ttu-id="16264-2594">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-2594">Checking Acct #</span></span> 
- <span data-ttu-id="16264-2595">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-2595">Checking Acct No.</span></span> 
- <span data-ttu-id="16264-2596">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-2596">Checking Account No.</span></span> 
- <span data-ttu-id="16264-2597">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2597">Bank Account Number</span></span> 
- <span data-ttu-id="16264-2598">Bank Account</span><span class="sxs-lookup"><span data-stu-id="16264-2598">Bank Account</span></span> 
- <span data-ttu-id="16264-2599">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="16264-2599">Bank Account #</span></span> 
- <span data-ttu-id="16264-2600">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-2600">Bank Acct Number</span></span> 
- <span data-ttu-id="16264-2601">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-2601">Bank Acct #</span></span> 
- <span data-ttu-id="16264-2602">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-2602">Bank Acct No.</span></span> 
- <span data-ttu-id="16264-2603">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-2603">Bank Account No.</span></span> 
- <span data-ttu-id="16264-2604">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2604">Savings Account Number</span></span> 
- <span data-ttu-id="16264-2605">Savings Account</span><span class="sxs-lookup"><span data-stu-id="16264-2605">Savings Account</span></span> 
- <span data-ttu-id="16264-2606">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="16264-2606">Savings Account #</span></span> 
- <span data-ttu-id="16264-2607">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-2607">Savings Acct Number</span></span> 
- <span data-ttu-id="16264-2608">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-2608">Savings Acct #</span></span> 
- <span data-ttu-id="16264-2609">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-2609">Savings Acct No.</span></span> 
- <span data-ttu-id="16264-2610">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-2610">Savings Account No.</span></span> 
- <span data-ttu-id="16264-2611">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-2611">Debit Account Number</span></span> 
- <span data-ttu-id="16264-2612">Debit Account</span><span class="sxs-lookup"><span data-stu-id="16264-2612">Debit Account</span></span> 
- <span data-ttu-id="16264-2613">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="16264-2613">Debit Account #</span></span> 
- <span data-ttu-id="16264-2614">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-2614">Debit Acct Number</span></span> 
- <span data-ttu-id="16264-2615">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-2615">Debit Acct #</span></span> 
- <span data-ttu-id="16264-2616">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-2616">Debit Acct No.</span></span> 
- <span data-ttu-id="16264-2617">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-2617">Debit Account No.</span></span> 
- <span data-ttu-id="16264-2618">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="16264-2618">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="16264-2619">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="16264-2619">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="16264-2620">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="16264-2620">＃勘定の確認</span></span> 
- <span data-ttu-id="16264-2621">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="16264-2621">勘定番号の確認</span></span> 
- <span data-ttu-id="16264-2622">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="16264-2622">口座番号の確認</span></span> 
- <span data-ttu-id="16264-2623">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2623">銀行口座番号</span></span> 
- <span data-ttu-id="16264-2624">銀行口座</span><span class="sxs-lookup"><span data-stu-id="16264-2624">銀行口座</span></span> 
- <span data-ttu-id="16264-2625">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="16264-2625">銀行口座＃</span></span> 
- <span data-ttu-id="16264-2626">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="16264-2626">銀行の勘定番号</span></span> 
- <span data-ttu-id="16264-2627">銀行のаккт #</span><span class="sxs-lookup"><span data-stu-id="16264-2627">銀行のacct＃</span></span> 
- <span data-ttu-id="16264-2628">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="16264-2628">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="16264-2629">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2629">銀行口座番号</span></span>
- <span data-ttu-id="16264-2630">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2630">普通預金口座番号</span></span> 
- <span data-ttu-id="16264-2631">預金口座</span><span class="sxs-lookup"><span data-stu-id="16264-2631">預金口座</span></span> 
- <span data-ttu-id="16264-2632">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="16264-2632">貯蓄口座＃</span></span> 
- <span data-ttu-id="16264-2633">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="16264-2633">貯蓄勘定の数</span></span> 
- <span data-ttu-id="16264-2634">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="16264-2634">貯蓄勘定＃</span></span> 
- <span data-ttu-id="16264-2635">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="16264-2635">貯蓄勘定番号</span></span> 
- <span data-ttu-id="16264-2636">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2636">普通預金口座番号</span></span> 
- <span data-ttu-id="16264-2637">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2637">引き落とし口座番号</span></span> 
- <span data-ttu-id="16264-2638">口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2638">口座番号</span></span> 
- <span data-ttu-id="16264-2639">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="16264-2639">口座番号＃</span></span> 
- <span data-ttu-id="16264-2640">デビットのаккт番号</span><span class="sxs-lookup"><span data-stu-id="16264-2640">デビットのacct番号</span></span> 
- <span data-ttu-id="16264-2641">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="16264-2641">デビット勘定＃</span></span> 
- <span data-ttu-id="16264-2642">デビットакктの番号</span><span class="sxs-lookup"><span data-stu-id="16264-2642">デビットACCTの番号</span></span> 
- <span data-ttu-id="16264-2643">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="16264-2643">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="16264-2644">Кэйворд_жп_банк_бранч_коде</span><span class="sxs-lookup"><span data-stu-id="16264-2644">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="16264-2645">Отемачи</span><span class="sxs-lookup"><span data-stu-id="16264-2645">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="16264-2646">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="16264-2646">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2647">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2647">Format</span></span>

<span data-ttu-id="16264-2648">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2648">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2649">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2649">Pattern</span></span>

<span data-ttu-id="16264-2650">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2650">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2651">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2651">Checksum</span></span>

<span data-ttu-id="16264-2652">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2652">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2653">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2653">Definition</span></span>

<span data-ttu-id="16264-2654">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2654">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2655">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2655">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2656">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="16264-2656">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2657">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2657">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="16264-2658">Кэйворд_жп_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2658">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="16264-2659">DL</span><span class="sxs-lookup"><span data-stu-id="16264-2659">dl#</span></span> 
- <span data-ttu-id="16264-2660">DL</span><span class="sxs-lookup"><span data-stu-id="16264-2660">DL＃</span></span> 
- <span data-ttu-id="16264-2661">библиотек</span><span class="sxs-lookup"><span data-stu-id="16264-2661">dls#</span></span> 
- <span data-ttu-id="16264-2662">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="16264-2662">DLS＃</span></span> 
- <span data-ttu-id="16264-2663">driver license</span><span class="sxs-lookup"><span data-stu-id="16264-2663">driver license</span></span> 
- <span data-ttu-id="16264-2664">driver licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2664">driver licenses</span></span> 
- <span data-ttu-id="16264-2665">drivers license</span><span class="sxs-lookup"><span data-stu-id="16264-2665">drivers license</span></span> 
- <span data-ttu-id="16264-2666">driver's license</span><span class="sxs-lookup"><span data-stu-id="16264-2666">driver's license</span></span> 
- <span data-ttu-id="16264-2667">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2667">drivers licenses</span></span> 
- <span data-ttu-id="16264-2668">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="16264-2668">driver's licenses</span></span> 
- <span data-ttu-id="16264-2669">driving licence</span><span class="sxs-lookup"><span data-stu-id="16264-2669">driving licence</span></span> 
- <span data-ttu-id="16264-2670">Лик #</span><span class="sxs-lookup"><span data-stu-id="16264-2670">lic#</span></span> 
- <span data-ttu-id="16264-2671">Лик #</span><span class="sxs-lookup"><span data-stu-id="16264-2671">LIC＃</span></span> 
- <span data-ttu-id="16264-2672">ликс #</span><span class="sxs-lookup"><span data-stu-id="16264-2672">lics#</span></span> 
- <span data-ttu-id="16264-2673">state id</span><span class="sxs-lookup"><span data-stu-id="16264-2673">state id</span></span> 
- <span data-ttu-id="16264-2674">state identification</span><span class="sxs-lookup"><span data-stu-id="16264-2674">state identification</span></span> 
- <span data-ttu-id="16264-2675">state identification number</span><span class="sxs-lookup"><span data-stu-id="16264-2675">state identification number</span></span> 
- <span data-ttu-id="16264-2676">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="16264-2676">低所得国＃</span></span> 
- <span data-ttu-id="16264-2677">免許証</span><span class="sxs-lookup"><span data-stu-id="16264-2677">免許証</span></span> 
- <span data-ttu-id="16264-2678">状態ид</span><span class="sxs-lookup"><span data-stu-id="16264-2678">状態ID</span></span>
- <span data-ttu-id="16264-2679">状態の識別</span><span class="sxs-lookup"><span data-stu-id="16264-2679">状態の識別</span></span> 
- <span data-ttu-id="16264-2680">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="16264-2680">状態の識別番号</span></span> 
- <span data-ttu-id="16264-2681">運転免許</span><span class="sxs-lookup"><span data-stu-id="16264-2681">運転免許</span></span> 
- <span data-ttu-id="16264-2682">運転免許証</span><span class="sxs-lookup"><span data-stu-id="16264-2682">運転免許証</span></span> 
- <span data-ttu-id="16264-2683">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="16264-2683">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="16264-2684">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="16264-2684">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2685">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2685">Format</span></span>

<span data-ttu-id="16264-2686">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2686">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2687">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2687">Pattern</span></span>

<span data-ttu-id="16264-2688">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2688">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2689">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2689">Checksum</span></span>

<span data-ttu-id="16264-2690">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2690">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2691">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2691">Definition</span></span>

<span data-ttu-id="16264-2692">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2692">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2693">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2693">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2694">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="16264-2694">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2695">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2695">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="16264-2696">Кэйворд_жп_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-2696">Keyword_jp_passport</span></span>

- <span data-ttu-id="16264-2697">パスポート</span><span class="sxs-lookup"><span data-stu-id="16264-2697">パスポート</span></span> 
- <span data-ttu-id="16264-2698">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="16264-2698">パスポート番号</span></span> 
- <span data-ttu-id="16264-2699">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="16264-2699">パスポートのNum</span></span> 
- <span data-ttu-id="16264-2700">パスポート #</span><span class="sxs-lookup"><span data-stu-id="16264-2700">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="16264-2701">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="16264-2701">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2702">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2702">Format</span></span>

<span data-ttu-id="16264-2703">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2703">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2704">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2704">Pattern</span></span>

<span data-ttu-id="16264-2705">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2705">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2706">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2706">Checksum</span></span>

<span data-ttu-id="16264-2707">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2707">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2708">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2708">Definition</span></span>

<span data-ttu-id="16264-2709">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2709">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2710">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2710">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2711">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="16264-2711">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2712">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2712">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="16264-2713">Кэйворд_жп_ресидент_регистратион_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2713">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="16264-2714">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="16264-2714">Resident Registration Number</span></span>
- <span data-ttu-id="16264-2715">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="16264-2715">Resident Register Number</span></span> 
- <span data-ttu-id="16264-2716">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="16264-2716">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="16264-2717">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="16264-2717">Resident Registration No.</span></span> 
- <span data-ttu-id="16264-2718">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="16264-2718">Resident Register No.</span></span> 
- <span data-ttu-id="16264-2719">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="16264-2719">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="16264-2720">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="16264-2720">Basic Resident Register No.</span></span> 
- <span data-ttu-id="16264-2721">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="16264-2721">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="16264-2722">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="16264-2722">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="16264-2723">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="16264-2723">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="16264-2724">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="16264-2724">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="16264-2725">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="16264-2725">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2726">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2726">Format</span></span>

<span data-ttu-id="16264-2727">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2727">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2728">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2728">Pattern</span></span>

<span data-ttu-id="16264-2729">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="16264-2729">7-12 digits:</span></span>
- <span data-ttu-id="16264-2730">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="16264-2730">Four digits</span></span> 
- <span data-ttu-id="16264-2731">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="16264-2731">A hyphen (optional)</span></span> 
- <span data-ttu-id="16264-2732">Шесть цифр или</span><span class="sxs-lookup"><span data-stu-id="16264-2732">Six digits OR</span></span>
- <span data-ttu-id="16264-2733">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2733">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2734">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2734">Checksum</span></span>

<span data-ttu-id="16264-2735">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2736">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2736">Definition</span></span>

<span data-ttu-id="16264-2737">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2737">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2738">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2738">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2739">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="16264-2739">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="16264-2740">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2740">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2741">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2741">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2742">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="16264-2742">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2743">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2743">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="16264-2744">Кэйворд_жп_син</span><span class="sxs-lookup"><span data-stu-id="16264-2744">Keyword_jp_sin</span></span>

- <span data-ttu-id="16264-2745">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="16264-2745">Social Insurance No.</span></span> 
- <span data-ttu-id="16264-2746">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="16264-2746">Social Insurance Num</span></span> 
- <span data-ttu-id="16264-2747">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="16264-2747">Social Insurance Number</span></span> 
- <span data-ttu-id="16264-2748">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="16264-2748">社会保険のテンキー</span></span> 
- <span data-ttu-id="16264-2749">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="16264-2749">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="16264-2750">Номер карточки для японского языка</span><span class="sxs-lookup"><span data-stu-id="16264-2750">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2751">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2751">Format</span></span>

<span data-ttu-id="16264-2752">12 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="16264-2752">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2753">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2753">Pattern</span></span>

<span data-ttu-id="16264-2754">12 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2754">12 letters and digits:</span></span>
- <span data-ttu-id="16264-2755">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-2755">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="16264-2756">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2756">Eight digits</span></span> 
- <span data-ttu-id="16264-2757">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-2757">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2758">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2758">Checksum</span></span>

<span data-ttu-id="16264-2759">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2759">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2760">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2760">Definition</span></span>

<span data-ttu-id="16264-2761">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2761">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2762">Регулярное выражение Режекс_жп_ресиденце_кард_нумбер находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2762">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2763">Найдено ключевое слово из Кэйворд_жп_ресиденце_кард_нумбер.</span><span class="sxs-lookup"><span data-stu-id="16264-2763">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2764">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2764">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="16264-2765">Кэйворд_жп_ресиденце_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2765">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="16264-2766">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="16264-2766">Residence card number</span></span>
- <span data-ttu-id="16264-2767">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="16264-2767">Residence card no</span></span>
- <span data-ttu-id="16264-2768">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="16264-2768">Residence card #</span></span>
- <span data-ttu-id="16264-2769">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="16264-2769">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="16264-2770">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="16264-2770">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2771">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2771">Format</span></span>

<span data-ttu-id="16264-2772">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="16264-2772">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2773">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2773">Pattern</span></span>

<span data-ttu-id="16264-2774">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2774">12 digits:</span></span>
- <span data-ttu-id="16264-2775">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="16264-2775">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="16264-2776">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="16264-2776">A dash (optional)</span></span> 
- <span data-ttu-id="16264-2777">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="16264-2777">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="16264-2778">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="16264-2778">A dash (optional)</span></span> 
- <span data-ttu-id="16264-2779">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-2779">Three random digits</span></span> 
- <span data-ttu-id="16264-2780">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-2780">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2781">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2781">Checksum</span></span>

<span data-ttu-id="16264-2782">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2782">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2783">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2783">Definition</span></span>

<span data-ttu-id="16264-2784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2785">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2785">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2786">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="16264-2786">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2787">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2787">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="16264-2788">Кэйворд_малайсиа_ид_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2788">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="16264-2789">карточка цифрового приложения</span><span class="sxs-lookup"><span data-stu-id="16264-2789">digital application card</span></span>
- <span data-ttu-id="16264-2790">i/c</span><span class="sxs-lookup"><span data-stu-id="16264-2790">i/c</span></span>
- <span data-ttu-id="16264-2791">i/c нет</span><span class="sxs-lookup"><span data-stu-id="16264-2791">i/c no</span></span>
- <span data-ttu-id="16264-2792">внутренних</span><span class="sxs-lookup"><span data-stu-id="16264-2792">ic</span></span>
- <span data-ttu-id="16264-2793">МФ нет</span><span class="sxs-lookup"><span data-stu-id="16264-2793">ic no</span></span>
- <span data-ttu-id="16264-2794">id card</span><span class="sxs-lookup"><span data-stu-id="16264-2794">id card</span></span>
- <span data-ttu-id="16264-2795">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="16264-2795">identification Card</span></span>
- <span data-ttu-id="16264-2796">identity card</span><span class="sxs-lookup"><span data-stu-id="16264-2796">identity card</span></span>
- <span data-ttu-id="16264-2797">k/p</span><span class="sxs-lookup"><span data-stu-id="16264-2797">k/p</span></span>
- <span data-ttu-id="16264-2798">k/p</span><span class="sxs-lookup"><span data-stu-id="16264-2798">k/p no</span></span>
- <span data-ttu-id="16264-2799">кад акуан Дири</span><span class="sxs-lookup"><span data-stu-id="16264-2799">kad akuan diri</span></span>
- <span data-ttu-id="16264-2800">кад апликаси Digital</span><span class="sxs-lookup"><span data-stu-id="16264-2800">kad aplikasi digital</span></span>
- <span data-ttu-id="16264-2801">кад пенженалан Малайзии</span><span class="sxs-lookup"><span data-stu-id="16264-2801">kad pengenalan malaysia</span></span>
- <span data-ttu-id="16264-2802">ключев</span><span class="sxs-lookup"><span data-stu-id="16264-2802">kp</span></span>
- <span data-ttu-id="16264-2803">ключевой номер</span><span class="sxs-lookup"><span data-stu-id="16264-2803">kp no</span></span>
- <span data-ttu-id="16264-2804">микад</span><span class="sxs-lookup"><span data-stu-id="16264-2804">mykad</span></span>
- <span data-ttu-id="16264-2805">Микас</span><span class="sxs-lookup"><span data-stu-id="16264-2805">mykas</span></span>
- <span data-ttu-id="16264-2806">микид</span><span class="sxs-lookup"><span data-stu-id="16264-2806">mykid</span></span>
- <span data-ttu-id="16264-2807">МИПР</span><span class="sxs-lookup"><span data-stu-id="16264-2807">mypr</span></span>
- <span data-ttu-id="16264-2808">митентера</span><span class="sxs-lookup"><span data-stu-id="16264-2808">mytentera</span></span>
- <span data-ttu-id="16264-2809">идентификационная карточка Малайзии</span><span class="sxs-lookup"><span data-stu-id="16264-2809">malaysia identity card</span></span>
- <span data-ttu-id="16264-2810">идентификационная карточка малайсиан</span><span class="sxs-lookup"><span data-stu-id="16264-2810">malaysian identity card</span></span>
- <span data-ttu-id="16264-2811">NRIC</span><span class="sxs-lookup"><span data-stu-id="16264-2811">nric</span></span>
- <span data-ttu-id="16264-2812">Личная идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="16264-2812">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="16264-2813">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="16264-2813">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2814">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2814">Format</span></span>

<span data-ttu-id="16264-2815">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="16264-2815">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2816">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2816">Pattern</span></span>

<span data-ttu-id="16264-2817">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2817">8-9 digits:</span></span>
- <span data-ttu-id="16264-2818">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-2818">Three digits</span></span> 
- <span data-ttu-id="16264-2819">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="16264-2819">A space (optional)</span></span> 
- <span data-ttu-id="16264-2820">три цифры; </span><span class="sxs-lookup"><span data-stu-id="16264-2820">Three digits</span></span> 
- <span data-ttu-id="16264-2821">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="16264-2821">A space (optional)</span></span> 
- <span data-ttu-id="16264-2822">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-2822">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2823">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2823">Checksum</span></span>

<span data-ttu-id="16264-2824">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2824">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2825">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2825">Definition</span></span>

<span data-ttu-id="16264-2826">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2826">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2827">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2827">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2828">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="16264-2828">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="16264-2829">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-2829">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="16264-2830">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2830">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2831">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2831">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="16264-2832">Кэйворд_несерландс_бсн</span><span class="sxs-lookup"><span data-stu-id="16264-2832">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="16264-2833">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="16264-2833">Citizen service number</span></span> 
- <span data-ttu-id="16264-2834">BSN</span><span class="sxs-lookup"><span data-stu-id="16264-2834">BSN</span></span> 
- <span data-ttu-id="16264-2835">Буржерсервиценуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2835">Burgerservicenummer</span></span> 
- <span data-ttu-id="16264-2836">Софинуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2836">Sofinummer</span></span> 
- <span data-ttu-id="16264-2837">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="16264-2837">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="16264-2838">Персунснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2838">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="16264-2839">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="16264-2839">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2840">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2840">Format</span></span>

<span data-ttu-id="16264-2841">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-2841">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2842">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2842">Pattern</span></span>

<span data-ttu-id="16264-2843">Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2843">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2844">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2844">Checksum</span></span>

<span data-ttu-id="16264-2845">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2845">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2846">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2846">Definition</span></span>

<span data-ttu-id="16264-2847">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2848">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2848">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2849">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="16264-2849">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="16264-2850">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2850">The checksum passes.</span></span>

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

<span data-ttu-id="16264-2851">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2851">Keywords</span></span>

<span data-ttu-id="16264-2852">Кэйворд_нз_термс</span><span class="sxs-lookup"><span data-stu-id="16264-2852">Keyword_nz_terms</span></span>

- <span data-ttu-id="16264-2853">НХИ</span><span class="sxs-lookup"><span data-stu-id="16264-2853">NHI</span></span> 
- <span data-ttu-id="16264-2854">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="16264-2854">New Zealand</span></span> 
- <span data-ttu-id="16264-2855">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="16264-2855">Health</span></span> 
- <span data-ttu-id="16264-2856">обращения</span><span class="sxs-lookup"><span data-stu-id="16264-2856">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="16264-2857">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="16264-2857">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2858">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2858">Format</span></span>

<span data-ttu-id="16264-2859">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2859">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2860">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2860">Pattern</span></span>

<span data-ttu-id="16264-2861">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2861">11 digits:</span></span>
- <span data-ttu-id="16264-2862">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="16264-2862">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="16264-2863">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-2863">Three-digit individual number</span></span> 
- <span data-ttu-id="16264-2864">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-2864">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2865">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2865">Checksum</span></span>

<span data-ttu-id="16264-2866">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2866">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2867">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2867">Definition</span></span>

<span data-ttu-id="16264-2868">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2868">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2869">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2869">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2870">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="16264-2870">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="16264-2871">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2871">The checksum passes.</span></span>
- <span data-ttu-id="16264-2872">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2873">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2873">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2874">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2874">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2875">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2875">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="16264-2876">Кэйворд_норвай_ид_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2876">Keyword_norway_id_number</span></span>

- <span data-ttu-id="16264-2877">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="16264-2877">Personal identification number</span></span>
- <span data-ttu-id="16264-2878">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="16264-2878">Norwegian ID Number</span></span>
- <span data-ttu-id="16264-2879">ID Number</span><span class="sxs-lookup"><span data-stu-id="16264-2879">ID Number</span></span>
- <span data-ttu-id="16264-2880">Процедура</span><span class="sxs-lookup"><span data-stu-id="16264-2880">Identification</span></span>
- <span data-ttu-id="16264-2881">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2881">Personnummer</span></span>
- <span data-ttu-id="16264-2882">Фøдселснуммер</span><span class="sxs-lookup"><span data-stu-id="16264-2882">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="16264-2883">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="16264-2883">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2884">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2884">Format</span></span>

<span data-ttu-id="16264-2885">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="16264-2885">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2886">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2886">Pattern</span></span>

<span data-ttu-id="16264-2887">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2887">12 digits:</span></span>
- <span data-ttu-id="16264-2888">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-2888">Four digits</span></span> 
- <span data-ttu-id="16264-2889">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-2889">A hyphen</span></span> 
- <span data-ttu-id="16264-2890">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-2890">Seven digits</span></span> 
- <span data-ttu-id="16264-2891">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-2891">A hyphen</span></span> 
- <span data-ttu-id="16264-2892">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="16264-2892">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2893">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2893">Checksum</span></span>

<span data-ttu-id="16264-2894">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2894">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2895">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2895">Definition</span></span>

<span data-ttu-id="16264-2896">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2896">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2897">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2897">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2898">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="16264-2898">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2899">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2899">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="16264-2900">Кэйворд_филиппинес_ид</span><span class="sxs-lookup"><span data-stu-id="16264-2900">Keyword_philippines_id</span></span>

- <span data-ttu-id="16264-2901">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="16264-2901">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="16264-2902">Умид</span><span class="sxs-lookup"><span data-stu-id="16264-2902">UMID</span></span> 
- <span data-ttu-id="16264-2903">Identity Card</span><span class="sxs-lookup"><span data-stu-id="16264-2903">Identity Card</span></span> 
- <span data-ttu-id="16264-2904">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="16264-2904">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="16264-2905">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="16264-2905">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="16264-2906">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2906">Format</span></span>

<span data-ttu-id="16264-2907">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2907">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2908">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2908">Pattern</span></span>

<span data-ttu-id="16264-2909">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2909">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2910">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2910">Checksum</span></span>

<span data-ttu-id="16264-2911">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2911">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2912">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2912">Definition</span></span>

<span data-ttu-id="16264-2913">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_полиш_натионал_ид находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2913">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="16264-2914">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="16264-2914">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="16264-2915">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2915">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2916">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2916">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="16264-2917">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2917">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="16264-2918">Довóд особисти</span><span class="sxs-lookup"><span data-stu-id="16264-2918">Dowód osobisty</span></span>
- <span data-ttu-id="16264-2919">Нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="16264-2919">Numer dowodu osobistego</span></span>
- <span data-ttu-id="16264-2920">Назва i нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="16264-2920">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="16264-2921">Назва i НР доводу особистего</span><span class="sxs-lookup"><span data-stu-id="16264-2921">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="16264-2922">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="16264-2922">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="16264-2923">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="16264-2923">Dowód Tożsamości</span></span>
- <span data-ttu-id="16264-2924">Dow.</span><span class="sxs-lookup"><span data-stu-id="16264-2924">dow.</span></span> <span data-ttu-id="16264-2925">совместим.</span><span class="sxs-lookup"><span data-stu-id="16264-2925">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="16264-2926">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="16264-2926">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="16264-2927">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2927">Format</span></span>

<span data-ttu-id="16264-2928">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2928">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2929">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2929">Pattern</span></span>

<span data-ttu-id="16264-2930">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2930">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2931">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2931">Checksum</span></span>

<span data-ttu-id="16264-2932">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2932">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2933">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2933">Definition</span></span>

<span data-ttu-id="16264-2934">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2934">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2935">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2935">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2936">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="16264-2936">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="16264-2937">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2937">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2938">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2938">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="16264-2939">Кэйворд_песел_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2939">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="16264-2940">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="16264-2940">Nr PESEL</span></span>
- <span data-ttu-id="16264-2941">PESEL</span><span class="sxs-lookup"><span data-stu-id="16264-2941">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="16264-2942">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="16264-2942">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="16264-2943">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2943">Format</span></span>

<span data-ttu-id="16264-2944">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2944">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2945">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2945">Pattern</span></span>

<span data-ttu-id="16264-2946">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2946">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2947">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2947">Checksum</span></span>

<span data-ttu-id="16264-2948">Да</span><span class="sxs-lookup"><span data-stu-id="16264-2948">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2949">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2949">Definition</span></span>

<span data-ttu-id="16264-2950">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2950">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2951">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2951">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2952">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="16264-2952">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="16264-2953">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-2953">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2954">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2954">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="16264-2955">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-2955">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="16264-2956">Нумер пасзпорту</span><span class="sxs-lookup"><span data-stu-id="16264-2956">Numer paszportu</span></span>
- <span data-ttu-id="16264-2957">НР.</span><span class="sxs-lookup"><span data-stu-id="16264-2957">Nr.</span></span> <span data-ttu-id="16264-2958">Пасзпорту</span><span class="sxs-lookup"><span data-stu-id="16264-2958">Paszportu</span></span>
- <span data-ttu-id="16264-2959">Пасзпорт</span><span class="sxs-lookup"><span data-stu-id="16264-2959">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="16264-2960">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="16264-2960">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2961">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2961">Format</span></span>

<span data-ttu-id="16264-2962">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2962">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2963">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2963">Pattern</span></span>

<span data-ttu-id="16264-2964">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2964">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2965">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2965">Checksum</span></span>

<span data-ttu-id="16264-2966">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2966">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2967">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2967">Definition</span></span>

<span data-ttu-id="16264-2968">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2969">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2969">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2970">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="16264-2970">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-2971">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2971">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="16264-2972">Кэйворд_португал_Цитизен_кард</span><span class="sxs-lookup"><span data-stu-id="16264-2972">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="16264-2973">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="16264-2973">Citizen Card</span></span>
- <span data-ttu-id="16264-2974">National ID Card</span><span class="sxs-lookup"><span data-stu-id="16264-2974">National ID Card</span></span>
- <span data-ttu-id="16264-2975">CC</span><span class="sxs-lookup"><span data-stu-id="16264-2975">CC</span></span>
- <span data-ttu-id="16264-2976">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="16264-2976">Cartão de Cidadão</span></span>
- <span data-ttu-id="16264-2977">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="16264-2977">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="16264-2978">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="16264-2978">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="16264-2979">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2979">Format</span></span>

<span data-ttu-id="16264-2980">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2980">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2981">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2981">Pattern</span></span>

<span data-ttu-id="16264-2982">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2982">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-2983">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-2983">Checksum</span></span>

<span data-ttu-id="16264-2984">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-2984">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-2985">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-2985">Definition</span></span>

<span data-ttu-id="16264-2986">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-2987">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-2987">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-2988">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="16264-2988">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-2989">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-2989">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="16264-2990">Кэйворд_сауди_арабиа_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="16264-2990">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="16264-2991">Identification Card</span><span class="sxs-lookup"><span data-stu-id="16264-2991">Identification Card</span></span> 
- <span data-ttu-id="16264-2992">I card number</span><span class="sxs-lookup"><span data-stu-id="16264-2992">I card number</span></span> 
- <span data-ttu-id="16264-2993">ID number</span><span class="sxs-lookup"><span data-stu-id="16264-2993">ID number</span></span> 
- <span data-ttu-id="16264-2994">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="16264-2994">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="16264-2995">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="16264-2995">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-2996">Format</span><span class="sxs-lookup"><span data-stu-id="16264-2996">Format</span></span>

<span data-ttu-id="16264-2997">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-2997">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-2998">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-2998">Pattern</span></span>

- <span data-ttu-id="16264-2999">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-2999">Nine letters and digits:</span></span>
- <span data-ttu-id="16264-3000">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-3000">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="16264-3001">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-3001">Seven digits</span></span> 
- <span data-ttu-id="16264-3002">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="16264-3002">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3003">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3003">Checksum</span></span>

<span data-ttu-id="16264-3004">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3004">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3005">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3005">Definition</span></span>

<span data-ttu-id="16264-3006">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3006">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3007">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3007">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3008">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="16264-3008">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="16264-3009">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3009">The checksum passes.</span></span>

<span data-ttu-id="16264-3010">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3010">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3011">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3011">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3012">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3012">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3013">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3013">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="16264-3014">Кэйворд_сингапоре_нрик</span><span class="sxs-lookup"><span data-stu-id="16264-3014">Keyword_singapore_nric</span></span>

- <span data-ttu-id="16264-3015">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="16264-3015">National Registration Identity Card</span></span> 
- <span data-ttu-id="16264-3016">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="16264-3016">Identity Card Number</span></span> 
- <span data-ttu-id="16264-3017">NRIC</span><span class="sxs-lookup"><span data-stu-id="16264-3017">NRIC</span></span> 
- <span data-ttu-id="16264-3018">ВНУТРЕННИХ</span><span class="sxs-lookup"><span data-stu-id="16264-3018">IC</span></span> 
- <span data-ttu-id="16264-3019">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="16264-3019">Foreign Identification Number</span></span> 
- <span data-ttu-id="16264-3020">ПРОЦЕНТ</span><span class="sxs-lookup"><span data-stu-id="16264-3020">FIN</span></span> 
- <span data-ttu-id="16264-3021">身份证</span><span class="sxs-lookup"><span data-stu-id="16264-3021">身份证</span></span> 
- <span data-ttu-id="16264-3022">身份證</span><span class="sxs-lookup"><span data-stu-id="16264-3022">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="16264-3023">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="16264-3023">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3024">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3024">Format</span></span>

<span data-ttu-id="16264-3025">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="16264-3025">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3026">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3026">Pattern</span></span>

<span data-ttu-id="16264-3027">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-3027">13 digits:</span></span>
- <span data-ttu-id="16264-3028">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="16264-3028">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="16264-3029">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-3029">Four digits</span></span> 
- <span data-ttu-id="16264-3030">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="16264-3030">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="16264-3031">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="16264-3031">The digit "8" or "9"</span></span> 
- <span data-ttu-id="16264-3032">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="16264-3032">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3033">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3033">Checksum</span></span>

<span data-ttu-id="16264-3034">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3034">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3035">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3035">Definition</span></span>

<span data-ttu-id="16264-3036">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3036">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3037">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3037">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3038">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="16264-3038">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="16264-3039">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3039">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3040">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3040">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="16264-3041">Кэйворд_саус_африка_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3041">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="16264-3042">Identity card</span><span class="sxs-lookup"><span data-stu-id="16264-3042">Identity card</span></span>
- <span data-ttu-id="16264-3043">ИД</span><span class="sxs-lookup"><span data-stu-id="16264-3043">ID</span></span>
- <span data-ttu-id="16264-3044">Процедура</span><span class="sxs-lookup"><span data-stu-id="16264-3044">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="16264-3045">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="16264-3045">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3046">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3046">Format</span></span>

<span data-ttu-id="16264-3047">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="16264-3047">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3048">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3048">Pattern</span></span>

<span data-ttu-id="16264-3049">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-3049">13 digits:</span></span>
- <span data-ttu-id="16264-3050">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="16264-3050">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="16264-3051">дефис;</span><span class="sxs-lookup"><span data-stu-id="16264-3051">A hyphen</span></span> 
- <span data-ttu-id="16264-3052">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="16264-3052">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="16264-3053">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="16264-3053">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="16264-3054">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="16264-3054">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="16264-3055">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="16264-3055">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3056">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3056">Checksum</span></span>

<span data-ttu-id="16264-3057">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3057">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3058">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3058">Definition</span></span>

<span data-ttu-id="16264-3059">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3059">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3060">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3060">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3061">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="16264-3061">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="16264-3062">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3062">The checksum passes.</span></span>

<span data-ttu-id="16264-3063">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3063">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3064">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3064">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3065">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3065">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3066">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3066">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="16264-3067">Кэйворд_саус_кореа_ресидент_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3067">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="16264-3068">National ID card</span><span class="sxs-lookup"><span data-stu-id="16264-3068">National ID card</span></span> 
- <span data-ttu-id="16264-3069">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="16264-3069">Citizen's Registration Number</span></span> 
- <span data-ttu-id="16264-3070">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="16264-3070">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="16264-3071">РРН</span><span class="sxs-lookup"><span data-stu-id="16264-3071">RRN</span></span> 
- <span data-ttu-id="16264-3072">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="16264-3072">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="16264-3073">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="16264-3073">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-3074">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3074">Format</span></span>

<span data-ttu-id="16264-3075">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3075">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3076">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3076">Pattern</span></span>

<span data-ttu-id="16264-3077">11-12 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-3077">11-12 digits:</span></span>
- <span data-ttu-id="16264-3078">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3078">Two digits</span></span> 
- <span data-ttu-id="16264-3079">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="16264-3079">A forward slash (optional)</span></span> 
- <span data-ttu-id="16264-3080">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3080">7-8 digits</span></span> 
- <span data-ttu-id="16264-3081">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="16264-3081">A forward slash (optional)</span></span> 
- <span data-ttu-id="16264-3082">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3082">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3083">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3083">Checksum</span></span>

<span data-ttu-id="16264-3084">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3084">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3085">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3085">Definition</span></span>

<span data-ttu-id="16264-3086">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3086">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3087">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3087">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3088">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3088">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3089">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3089">Keywords</span></span>

<span data-ttu-id="16264-3090">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3090">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="16264-3091">Строка подключения к SQL Server</span><span class="sxs-lookup"><span data-stu-id="16264-3091">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="16264-3092">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3092">Format</span></span>

<span data-ttu-id="16264-3093">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId", за которыми следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="16264-3093">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3094">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3094">Pattern</span></span>

- <span data-ttu-id="16264-3095">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId"</span><span class="sxs-lookup"><span data-stu-id="16264-3095">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="16264-3096">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="16264-3096">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="16264-3097">Строка "Password" или "pwd", где "pwd" не предшествует буква нижнего регистра</span><span class="sxs-lookup"><span data-stu-id="16264-3097">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="16264-3098">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="16264-3098">An equal sign (=)</span></span>
- <span data-ttu-id="16264-3099">Любой символ, не являющийся знаком доллара ($), символ процента (%), больше символа (_Гт_), символ "@", символ "@", знак кавычек ("), точка с запятой (;), левая фигурная скобка ([) или левая квадратная скобка ({)</span><span class="sxs-lookup"><span data-stu-id="16264-3099">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="16264-3100">Любая комбинация 7-128 символов, не отделяющая точку с запятой (;), косая черта (/) или кавычки (").</span><span class="sxs-lookup"><span data-stu-id="16264-3100">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="16264-3101">Точка с запятой (;) или кавычки (")</span><span class="sxs-lookup"><span data-stu-id="16264-3101">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3102">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3102">Checksum</span></span>

<span data-ttu-id="16264-3103">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3103">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3104">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3104">Definition</span></span>

<span data-ttu-id="16264-3105">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3106">Регулярное выражение Цеп_режекс_склсерверконнектионстринг находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3106">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3107">**Не** найдено ключевое слово из цеп_глобалфилтер.</span><span class="sxs-lookup"><span data-stu-id="16264-3107">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="16264-3108">Регулярное выражение Цеп_пассвордплацехолдер не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3108">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3109">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3109">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```
<!---SQL Server Connection String>
<Entity id="e76b6205-d3cb-46f2-bd63-c90153f2f97d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_SQLServerConnectionString" />
        <Any minMatches="0" maxMatches="0">
            <Match idRef="CEP_GlobalFilter" />
            <Match idRef="CEP_PasswordPlaceHolder" />
            <Match idRef="CEP_CommonExampleKeywords" />
        </Any>
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3110">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3110">Keywords</span></span>

#### <a name="cepglobalfilter"></a><span data-ttu-id="16264-3111">Цеп_глобалфилтер</span><span class="sxs-lookup"><span data-stu-id="16264-3111">CEP_GlobalFilter</span></span>

- <span data-ttu-id="16264-3112">Некоторые пароли</span><span class="sxs-lookup"><span data-stu-id="16264-3112">some-password</span></span>
- <span data-ttu-id="16264-3113">сомепассворд</span><span class="sxs-lookup"><span data-stu-id="16264-3113">somepassword</span></span>
- <span data-ttu-id="16264-3114">Секретпассворд</span><span class="sxs-lookup"><span data-stu-id="16264-3114">secretPassword</span></span>
- <span data-ttu-id="16264-3115">примером</span><span class="sxs-lookup"><span data-stu-id="16264-3115">sample</span></span>

#### <a name="ceppasswordplaceholder"></a><span data-ttu-id="16264-3116">Цеп_пассвордплацехолдер</span><span class="sxs-lookup"><span data-stu-id="16264-3116">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="16264-3117">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-3117">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-3118">Пароль или pwd, за которым следует 0-2 пробелов, знак равенства (=), 0-2 пробелы и звездочка (\*)--или--</span><span class="sxs-lookup"><span data-stu-id="16264-3118">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="16264-3119">Пароль или pwd, а затем:</span><span class="sxs-lookup"><span data-stu-id="16264-3119">Password or pwd followed by:</span></span>
    - <span data-ttu-id="16264-3120">Знак равенства (=)</span><span class="sxs-lookup"><span data-stu-id="16264-3120">Equal sign (=)</span></span>
    - <span data-ttu-id="16264-3121">Символ "меньше" (_Лт_)</span><span class="sxs-lookup"><span data-stu-id="16264-3121">Less than symbol (<)</span></span>
    - <span data-ttu-id="16264-3122">Любое сочетание 1-200 символов, которые являются буквами верхнего или нижнего регистра, цифрами, звездочкой (\*), дефисом (-), подчеркиванием (_) или символом пробела</span><span class="sxs-lookup"><span data-stu-id="16264-3122">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="16264-3123">Символ "больше" (_Гт_)</span><span class="sxs-lookup"><span data-stu-id="16264-3123">Greater than symbol (>)</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="16264-3124">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="16264-3124">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="16264-3125">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="16264-3125">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="16264-3126">компанией</span><span class="sxs-lookup"><span data-stu-id="16264-3126">contoso</span></span>
- <span data-ttu-id="16264-3127">компании</span><span class="sxs-lookup"><span data-stu-id="16264-3127">fabrikam</span></span>
- <span data-ttu-id="16264-3128">базу</span><span class="sxs-lookup"><span data-stu-id="16264-3128">northwind</span></span>
- <span data-ttu-id="16264-3129">песочниц</span><span class="sxs-lookup"><span data-stu-id="16264-3129">sandbox</span></span>
- <span data-ttu-id="16264-3130">онебокс</span><span class="sxs-lookup"><span data-stu-id="16264-3130">onebox</span></span>
- <span data-ttu-id="16264-3131">localhost</span><span class="sxs-lookup"><span data-stu-id="16264-3131">localhost</span></span>
- <span data-ttu-id="16264-3132">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="16264-3132">127.0.0.1</span></span>
- <span data-ttu-id="16264-3133">тестакс. <!--no-hyperlink-->com-</span><span class="sxs-lookup"><span data-stu-id="16264-3133">testacs.<!--no-hyperlink-->com</span></span>
- <span data-ttu-id="16264-3134">s — int.<!--no-hyperlink-->NET</span><span class="sxs-lookup"><span data-stu-id="16264-3134">s-int.<!--no-hyperlink-->net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="16264-3135">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="16264-3135">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="16264-3136">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3136">Format</span></span>

<span data-ttu-id="16264-3137">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="16264-3137">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3138">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3138">Pattern</span></span>

<span data-ttu-id="16264-3139">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="16264-3139">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="16264-3140">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="16264-3140">2-4 digits (optional)</span></span> 
- <span data-ttu-id="16264-3141">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="16264-3141">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="16264-3142">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="16264-3142">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="16264-3143">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-3143">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3144">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3144">Checksum</span></span>

<span data-ttu-id="16264-3145">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3145">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3146">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3146">Definition</span></span>

<span data-ttu-id="16264-3147">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3147">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3148">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3148">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3149">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3149">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3150">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3150">Keywords</span></span>

<span data-ttu-id="16264-3151">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3151">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="16264-3152">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="16264-3152">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3153">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3153">Format</span></span>

<span data-ttu-id="16264-3154">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3154">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3155">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3155">Pattern</span></span>

<span data-ttu-id="16264-3156">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3156">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3157">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3157">Checksum</span></span>

<span data-ttu-id="16264-3158">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3158">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3159">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3159">Definition</span></span>

<span data-ttu-id="16264-3160">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3160">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3161">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3161">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3162">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-3162">One of the following is true:</span></span>
    - <span data-ttu-id="16264-3163">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="16264-3163">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="16264-3164">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="16264-3164">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3165">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3165">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="16264-3166">Кэйворд_сведен_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-3166">Keyword_sweden_passport</span></span>

- <span data-ttu-id="16264-3167">visa requirements</span><span class="sxs-lookup"><span data-stu-id="16264-3167">visa requirements</span></span> 
- <span data-ttu-id="16264-3168">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="16264-3168">Alien Registration Card</span></span> 
- <span data-ttu-id="16264-3169">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="16264-3169">Schengen visas</span></span> 
- <span data-ttu-id="16264-3170">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="16264-3170">Schengen visa</span></span> 
- <span data-ttu-id="16264-3171">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="16264-3171">Visa Processing</span></span> 
- <span data-ttu-id="16264-3172">Visa Type</span><span class="sxs-lookup"><span data-stu-id="16264-3172">Visa Type</span></span> 
- <span data-ttu-id="16264-3173">Single Entry</span><span class="sxs-lookup"><span data-stu-id="16264-3173">Single Entry</span></span> 
- <span data-ttu-id="16264-3174">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="16264-3174">Multiple Entry</span></span> 
- <span data-ttu-id="16264-3175">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="16264-3175">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="16264-3176">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-3176">Keyword_passport</span></span>

- <span data-ttu-id="16264-3177">Passport Number</span><span class="sxs-lookup"><span data-stu-id="16264-3177">Passport Number</span></span> 
- <span data-ttu-id="16264-3178">Passport No</span><span class="sxs-lookup"><span data-stu-id="16264-3178">Passport No</span></span> 
- <span data-ttu-id="16264-3179">Passport#</span><span class="sxs-lookup"><span data-stu-id="16264-3179">Passport #</span></span> 
- <span data-ttu-id="16264-3180">Службу</span><span class="sxs-lookup"><span data-stu-id="16264-3180">Passport#</span></span> 
- <span data-ttu-id="16264-3181">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="16264-3181">PassportID</span></span> 
- <span data-ttu-id="16264-3182">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="16264-3182">Passportno</span></span> 
- <span data-ttu-id="16264-3183">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3183">passportnumber</span></span> 
- <span data-ttu-id="16264-3184">パスポート</span><span class="sxs-lookup"><span data-stu-id="16264-3184">パスポート</span></span> 
- <span data-ttu-id="16264-3185">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="16264-3185">パスポート番号</span></span> 
- <span data-ttu-id="16264-3186">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="16264-3186">パスポートのNum</span></span> 
- <span data-ttu-id="16264-3187">パスポート #</span><span class="sxs-lookup"><span data-stu-id="16264-3187">パスポート＃</span></span> 
- <span data-ttu-id="16264-3188">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="16264-3188">Numéro de passeport</span></span> 
- <span data-ttu-id="16264-3189">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="16264-3189">Passeport n °</span></span> 
- <span data-ttu-id="16264-3190">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="16264-3190">Passeport Non</span></span> 
- <span data-ttu-id="16264-3191">Passeport#</span><span class="sxs-lookup"><span data-stu-id="16264-3191">Passeport #</span></span> 
- <span data-ttu-id="16264-3192">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="16264-3192">Passeport#</span></span> 
- <span data-ttu-id="16264-3193">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="16264-3193">PasseportNon</span></span> 
- <span data-ttu-id="16264-3194">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="16264-3194">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="16264-3195">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="16264-3195">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="16264-3196">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3196">Format</span></span>

<span data-ttu-id="16264-3197">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-3197">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3198">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3198">Pattern</span></span>

<span data-ttu-id="16264-3199">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3199">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="16264-3200">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-3200">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="16264-3201">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="16264-3201">An optional space</span></span> 
- <span data-ttu-id="16264-3202">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="16264-3202">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="16264-3203">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="16264-3203">An optional space</span></span> 
- <span data-ttu-id="16264-3204">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="16264-3204">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3205">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3205">Checksum</span></span>

<span data-ttu-id="16264-3206">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3206">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3207">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3207">Definition</span></span>

<span data-ttu-id="16264-3208">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3208">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3209">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3209">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3210">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="16264-3210">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3211">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3211">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="16264-3212">Кэйворд_свифт</span><span class="sxs-lookup"><span data-stu-id="16264-3212">Keyword_swift</span></span>

- <span data-ttu-id="16264-3213">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="16264-3213">international organization for standardization 9362</span></span> 
- <span data-ttu-id="16264-3214">iso 9362</span><span class="sxs-lookup"><span data-stu-id="16264-3214">iso 9362</span></span> 
- <span data-ttu-id="16264-3215">iso9362</span><span class="sxs-lookup"><span data-stu-id="16264-3215">iso9362</span></span> 
- <span data-ttu-id="16264-3216">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="16264-3216">swift\#</span></span> 
- <span data-ttu-id="16264-3217">свифткоде</span><span class="sxs-lookup"><span data-stu-id="16264-3217">swiftcode</span></span> 
- <span data-ttu-id="16264-3218">свифтнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3218">swiftnumber</span></span> 
- <span data-ttu-id="16264-3219">свифтраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3219">swiftroutingnumber</span></span> 
- <span data-ttu-id="16264-3220">swift code</span><span class="sxs-lookup"><span data-stu-id="16264-3220">swift code</span></span> 
- <span data-ttu-id="16264-3221">swift number #</span><span class="sxs-lookup"><span data-stu-id="16264-3221">swift number #</span></span> 
- <span data-ttu-id="16264-3222">swift routing number</span><span class="sxs-lookup"><span data-stu-id="16264-3222">swift routing number</span></span> 
- <span data-ttu-id="16264-3223">bic number</span><span class="sxs-lookup"><span data-stu-id="16264-3223">bic number</span></span> 
- <span data-ttu-id="16264-3224">bic code</span><span class="sxs-lookup"><span data-stu-id="16264-3224">bic code</span></span> 
- <span data-ttu-id="16264-3225">БИК\#</span><span class="sxs-lookup"><span data-stu-id="16264-3225">bic \#</span></span> 
- <span data-ttu-id="16264-3226">БИК\#</span><span class="sxs-lookup"><span data-stu-id="16264-3226">bic\#</span></span> 
- <span data-ttu-id="16264-3227">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="16264-3227">bank identifier code</span></span> 
- <span data-ttu-id="16264-3228">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="16264-3228">標準化9362</span></span> 
- <span data-ttu-id="16264-3229">迅速 #</span><span class="sxs-lookup"><span data-stu-id="16264-3229">迅速＃</span></span> 
- <span data-ttu-id="16264-3230">Свифтコード</span><span class="sxs-lookup"><span data-stu-id="16264-3230">SWIFTコード</span></span> 
- <span data-ttu-id="16264-3231">Свифт番号</span><span class="sxs-lookup"><span data-stu-id="16264-3231">SWIFT番号</span></span> 
- <span data-ttu-id="16264-3232">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="16264-3232">迅速なルーティング番号</span></span> 
- <span data-ttu-id="16264-3233">Бик番号</span><span class="sxs-lookup"><span data-stu-id="16264-3233">BIC番号</span></span> 
- <span data-ttu-id="16264-3234">Бикコード</span><span class="sxs-lookup"><span data-stu-id="16264-3234">BICコード</span></span> 
- <span data-ttu-id="16264-3235">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="16264-3235">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="16264-3236">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="16264-3236">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="16264-3237">Быстрая\#</span><span class="sxs-lookup"><span data-stu-id="16264-3237">rapide \#</span></span> 
- <span data-ttu-id="16264-3238">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="16264-3238">code SWIFT</span></span> 
- <span data-ttu-id="16264-3239">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="16264-3239">le numéro de swift</span></span> 
- <span data-ttu-id="16264-3240">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="16264-3240">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="16264-3241">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="16264-3241">le numéro BIC</span></span> 
- <span data-ttu-id="16264-3242">\#БИК</span><span class="sxs-lookup"><span data-stu-id="16264-3242">\# BIC</span></span> 
- <span data-ttu-id="16264-3243">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="16264-3243">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="16264-3244">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="16264-3244">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="16264-3245">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3245">Format</span></span>

<span data-ttu-id="16264-3246">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3246">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3247">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3247">Pattern</span></span>

<span data-ttu-id="16264-3248">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3248">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="16264-3249">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-3249">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="16264-3250">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="16264-3250">The digit "1" or "2"</span></span> 
- <span data-ttu-id="16264-3251">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3251">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3252">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3252">Checksum</span></span>

<span data-ttu-id="16264-3253">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3253">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3254">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3254">Definition</span></span>

<span data-ttu-id="16264-3255">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3255">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3256">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3256">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3257">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="16264-3257">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="16264-3258">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3258">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3259">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3259">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="16264-3260">Кэйворд_таиванесе_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="16264-3260">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="16264-3261">身份證字號</span><span class="sxs-lookup"><span data-stu-id="16264-3261">身份證字號</span></span> 
- <span data-ttu-id="16264-3262">身份證</span><span class="sxs-lookup"><span data-stu-id="16264-3262">身份證</span></span> 
- <span data-ttu-id="16264-3263">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="16264-3263">身份證號碼</span></span> 
- <span data-ttu-id="16264-3264">身份證號</span><span class="sxs-lookup"><span data-stu-id="16264-3264">身份證號</span></span> 
- <span data-ttu-id="16264-3265">身分證字號</span><span class="sxs-lookup"><span data-stu-id="16264-3265">身分證字號</span></span> 
- <span data-ttu-id="16264-3266">身分證</span><span class="sxs-lookup"><span data-stu-id="16264-3266">身分證</span></span> 
- <span data-ttu-id="16264-3267">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="16264-3267">身分證號碼</span></span> 
- <span data-ttu-id="16264-3268">身份證號</span><span class="sxs-lookup"><span data-stu-id="16264-3268">身份證號</span></span> 
- <span data-ttu-id="16264-3269">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="16264-3269">身分證統一編號</span></span> 
- <span data-ttu-id="16264-3270">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="16264-3270">國民身分證統一編號</span></span> 
- <span data-ttu-id="16264-3271">簽名</span><span class="sxs-lookup"><span data-stu-id="16264-3271">簽名</span></span> 
- <span data-ttu-id="16264-3272">蓋章</span><span class="sxs-lookup"><span data-stu-id="16264-3272">蓋章</span></span> 
- <span data-ttu-id="16264-3273">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="16264-3273">簽名或蓋章</span></span> 
- <span data-ttu-id="16264-3274">簽章</span><span class="sxs-lookup"><span data-stu-id="16264-3274">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="16264-3275">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="16264-3275">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3276">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3276">Format</span></span>

- <span data-ttu-id="16264-3277">Номер биометрического паспорта: девять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3277">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="16264-3278">Номер биометрической службы Passport: девять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3278">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3279">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3279">Pattern</span></span>
<span data-ttu-id="16264-3280">Номер биометрического паспорта:</span><span class="sxs-lookup"><span data-stu-id="16264-3280">Biometric passport number:</span></span>
- <span data-ttu-id="16264-3281">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="16264-3281">The digit "3"</span></span> 
- <span data-ttu-id="16264-3282">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3282">Eight digits</span></span>

<span data-ttu-id="16264-3283">Номер биометрической службы Passport:</span><span class="sxs-lookup"><span data-stu-id="16264-3283">Non-biometric passport number:</span></span>
- <span data-ttu-id="16264-3284">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3284">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3285">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3285">Checksum</span></span>

<span data-ttu-id="16264-3286">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3287">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3287">Definition</span></span>

<span data-ttu-id="16264-3288">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3289">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3289">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3290">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="16264-3290">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3291">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3291">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="16264-3292">Кэйворд_таиван_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-3292">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="16264-3293">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="16264-3293">ROC passport number</span></span> 
- <span data-ttu-id="16264-3294">Passport number</span><span class="sxs-lookup"><span data-stu-id="16264-3294">Passport number</span></span> 
- <span data-ttu-id="16264-3295">Passport no</span><span class="sxs-lookup"><span data-stu-id="16264-3295">Passport no</span></span> 
- <span data-ttu-id="16264-3296">Passport Num</span><span class="sxs-lookup"><span data-stu-id="16264-3296">Passport Num</span></span> 
- <span data-ttu-id="16264-3297">Passport #</span><span class="sxs-lookup"><span data-stu-id="16264-3297">Passport #</span></span> 
- <span data-ttu-id="16264-3298">护照</span><span class="sxs-lookup"><span data-stu-id="16264-3298">护照</span></span> 
- <span data-ttu-id="16264-3299">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="16264-3299">中華民國護照</span></span> 
- <span data-ttu-id="16264-3300">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="16264-3300">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="16264-3301">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="16264-3301">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3302">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3302">Format</span></span>

<span data-ttu-id="16264-3303">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3303">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3304">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3304">Pattern</span></span>

<span data-ttu-id="16264-3305">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-3305">10 letters and digits:</span></span>
- <span data-ttu-id="16264-3306">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="16264-3306">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="16264-3307">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3307">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3308">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3308">Checksum</span></span>

<span data-ttu-id="16264-3309">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3309">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3310">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3310">Definition</span></span>

<span data-ttu-id="16264-3311">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3311">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3312">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3312">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3313">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="16264-3313">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3314">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3314">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="16264-3315">Кэйворд_таиван_ресидент_цертификате</span><span class="sxs-lookup"><span data-stu-id="16264-3315">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="16264-3316">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="16264-3316">Resident Certificate</span></span> 
- <span data-ttu-id="16264-3317">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="16264-3317">Resident Cert</span></span> 
- <span data-ttu-id="16264-3318">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="16264-3318">Resident Cert.</span></span> 
- <span data-ttu-id="16264-3319">Identification card</span><span class="sxs-lookup"><span data-stu-id="16264-3319">Identification card</span></span> 
- <span data-ttu-id="16264-3320">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="16264-3320">Alien Resident Certificate</span></span> 
- <span data-ttu-id="16264-3321">ГИПЕРБОЛ</span><span class="sxs-lookup"><span data-stu-id="16264-3321">ARC</span></span> 
- <span data-ttu-id="16264-3322">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="16264-3322">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="16264-3323">TARC</span><span class="sxs-lookup"><span data-stu-id="16264-3323">TARC</span></span> 
- <span data-ttu-id="16264-3324">居留證</span><span class="sxs-lookup"><span data-stu-id="16264-3324">居留證</span></span> 
- <span data-ttu-id="16264-3325">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="16264-3325">外僑居留證</span></span> 
- <span data-ttu-id="16264-3326">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="16264-3326">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="16264-3327">Код идентификации для тайского заполнения</span><span class="sxs-lookup"><span data-stu-id="16264-3327">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="16264-3328">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3328">Format</span></span>

<span data-ttu-id="16264-3329">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3329">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3330">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3330">Pattern</span></span>

<span data-ttu-id="16264-3331">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="16264-3331">13 digits:</span></span>
- <span data-ttu-id="16264-3332">Первая цифра не равна 0 или 9</span><span class="sxs-lookup"><span data-stu-id="16264-3332">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="16264-3333">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3333">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3334">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3334">Checksum</span></span>

<span data-ttu-id="16264-3335">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3335">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3336">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3336">Definition</span></span>

<span data-ttu-id="16264-3337">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3337">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3338">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3338">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3339">Найдено ключевое слово из Кэйворд_саи_Цитизен_ид.</span><span class="sxs-lookup"><span data-stu-id="16264-3339">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="16264-3340">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3340">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3341">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3341">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3342">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3342">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="16264-3343">Кэйворд_саи_Цитизен_ид</span><span class="sxs-lookup"><span data-stu-id="16264-3343">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="16264-3344">ID Number</span><span class="sxs-lookup"><span data-stu-id="16264-3344">ID Number</span></span>
- <span data-ttu-id="16264-3345">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="16264-3345">Identification Number</span></span>
- <span data-ttu-id="16264-3346">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="16264-3346">บัตรประชาชน</span></span>
- <span data-ttu-id="16264-3347">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="16264-3347">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="16264-3348">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="16264-3348">บัตรประชาชน</span></span>
- <span data-ttu-id="16264-3349">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="16264-3349">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="16264-3350">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="16264-3350">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3351">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3351">Format</span></span>

<span data-ttu-id="16264-3352">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3352">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3353">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3353">Pattern</span></span>

<span data-ttu-id="16264-3354">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3354">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3355">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3355">Checksum</span></span>

<span data-ttu-id="16264-3356">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3356">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3357">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3357">Definition</span></span>

<span data-ttu-id="16264-3358">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3358">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3359">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3359">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3360">Найдено ключевое слово из Кэйворд_туркиш_натионал_ид.</span><span class="sxs-lookup"><span data-stu-id="16264-3360">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="16264-3361">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3362">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3362">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3363">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3363">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="16264-3364">Кэйворд_туркиш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="16264-3364">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="16264-3365">TC Кимлик No</span><span class="sxs-lookup"><span data-stu-id="16264-3365">TC Kimlik No</span></span>
- <span data-ttu-id="16264-3366">TC Кимлик нумарасı</span><span class="sxs-lookup"><span data-stu-id="16264-3366">TC Kimlik numarası</span></span>
- <span data-ttu-id="16264-3367">Ватандаşлıк нумарасı</span><span class="sxs-lookup"><span data-stu-id="16264-3367">Vatandaşlık numarası</span></span>
- <span data-ttu-id="16264-3368">Ватандаşлıк нет</span><span class="sxs-lookup"><span data-stu-id="16264-3368">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="16264-p141">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="16264-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3371">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3371">Format</span></span>

<span data-ttu-id="16264-3372">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-3372">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3373">Pattern</span></span>

<span data-ttu-id="16264-3374">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3374">18 letters and digits:</span></span>
- <span data-ttu-id="16264-3375">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="16264-3375">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="16264-3376">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="16264-3376">One digit</span></span> 
- <span data-ttu-id="16264-3377">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="16264-3377">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="16264-3378">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="16264-3378">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="16264-3379">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3379">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3380">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3380">Checksum</span></span>

<span data-ttu-id="16264-3381">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3382">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3382">Definition</span></span>

<span data-ttu-id="16264-3383">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3383">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3384">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3384">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3385">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="16264-3385">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="16264-3386">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3386">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3387">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3387">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="16264-3388">Кэйворд_ук_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-3388">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="16264-3389">ДВЛА</span><span class="sxs-lookup"><span data-stu-id="16264-3389">DVLA</span></span> 
- <span data-ttu-id="16264-3390">light vans</span><span class="sxs-lookup"><span data-stu-id="16264-3390">light vans</span></span> 
- <span data-ttu-id="16264-3391">куадбикес</span><span class="sxs-lookup"><span data-stu-id="16264-3391">quadbikes</span></span> 
- <span data-ttu-id="16264-3392">motor cars</span><span class="sxs-lookup"><span data-stu-id="16264-3392">motor cars</span></span> 
- <span data-ttu-id="16264-3393">125cc</span><span class="sxs-lookup"><span data-stu-id="16264-3393">125cc</span></span> 
- <span data-ttu-id="16264-3394">сидекар</span><span class="sxs-lookup"><span data-stu-id="16264-3394">sidecar</span></span> 
- <span data-ttu-id="16264-3395">трициклес</span><span class="sxs-lookup"><span data-stu-id="16264-3395">tricycles</span></span> 
- <span data-ttu-id="16264-3396">моторциклес</span><span class="sxs-lookup"><span data-stu-id="16264-3396">motorcycles</span></span> 
- <span data-ttu-id="16264-3397">photocard licence</span><span class="sxs-lookup"><span data-stu-id="16264-3397">photocard licence</span></span> 
- <span data-ttu-id="16264-3398">learner drivers</span><span class="sxs-lookup"><span data-stu-id="16264-3398">learner drivers</span></span> 
- <span data-ttu-id="16264-3399">licence holder</span><span class="sxs-lookup"><span data-stu-id="16264-3399">licence holder</span></span> 
- <span data-ttu-id="16264-3400">licence holders</span><span class="sxs-lookup"><span data-stu-id="16264-3400">licence holders</span></span> 
- <span data-ttu-id="16264-3401">driving licences</span><span class="sxs-lookup"><span data-stu-id="16264-3401">driving licences</span></span> 
- <span data-ttu-id="16264-3402">driving licence</span><span class="sxs-lookup"><span data-stu-id="16264-3402">driving licence</span></span> 
- <span data-ttu-id="16264-3403">dual control car</span><span class="sxs-lookup"><span data-stu-id="16264-3403">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="16264-p142">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="16264-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3406">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3406">Format</span></span>

<span data-ttu-id="16264-3407">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-3407">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3408">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3408">Pattern</span></span>

<span data-ttu-id="16264-3409">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="16264-3409">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3410">Checksum</span></span>

<span data-ttu-id="16264-3411">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3411">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3412">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3412">Definition</span></span>

<span data-ttu-id="16264-3413">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3413">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3414">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3414">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3415">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="16264-3415">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3416">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3416">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="16264-3417">Кэйворд_ук_електорал</span><span class="sxs-lookup"><span data-stu-id="16264-3417">Keyword_uk_electoral</span></span>

- <span data-ttu-id="16264-3418">council nomination</span><span class="sxs-lookup"><span data-stu-id="16264-3418">council nomination</span></span> 
- <span data-ttu-id="16264-3419">nomination form</span><span class="sxs-lookup"><span data-stu-id="16264-3419">nomination form</span></span> 
- <span data-ttu-id="16264-3420">electoral register</span><span class="sxs-lookup"><span data-stu-id="16264-3420">electoral register</span></span> 
- <span data-ttu-id="16264-3421">electoral roll</span><span class="sxs-lookup"><span data-stu-id="16264-3421">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="16264-p143">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="16264-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3424">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3424">Format</span></span>

<span data-ttu-id="16264-3425">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="16264-3425">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3426">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3426">Pattern</span></span>

<span data-ttu-id="16264-3427">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3427">10-17 digits:</span></span>
- <span data-ttu-id="16264-3428">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3428">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="16264-3429">Пробел</span><span class="sxs-lookup"><span data-stu-id="16264-3429">A space</span></span> 
- <span data-ttu-id="16264-3430">Три цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3430">Three digits</span></span> 
- <span data-ttu-id="16264-3431">Пробел</span><span class="sxs-lookup"><span data-stu-id="16264-3431">A space</span></span> 
- <span data-ttu-id="16264-3432">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3432">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3433">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3433">Checksum</span></span>

<span data-ttu-id="16264-3434">Да</span><span class="sxs-lookup"><span data-stu-id="16264-3434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3435">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3435">Definition</span></span>

<span data-ttu-id="16264-3436">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3437">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3437">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3438">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-3438">One of the following is true:</span></span>
    - <span data-ttu-id="16264-3439">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="16264-3439">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="16264-3440">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="16264-3440">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="16264-3441">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="16264-3441">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="16264-3442">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="16264-3442">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3443">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="16264-3444">Кэйворд_ук_нхс_нумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3444">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="16264-3445">national health service</span><span class="sxs-lookup"><span data-stu-id="16264-3445">national health service</span></span> 
- <span data-ttu-id="16264-3446">NHS</span><span class="sxs-lookup"><span data-stu-id="16264-3446">nhs</span></span> 
- <span data-ttu-id="16264-3447">health services authority</span><span class="sxs-lookup"><span data-stu-id="16264-3447">health services authority</span></span> 
- <span data-ttu-id="16264-3448">health authority</span><span class="sxs-lookup"><span data-stu-id="16264-3448">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="16264-3449">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="16264-3449">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="16264-3450">patient id</span><span class="sxs-lookup"><span data-stu-id="16264-3450">patient id</span></span> 
- <span data-ttu-id="16264-3451">patient identification</span><span class="sxs-lookup"><span data-stu-id="16264-3451">patient identification</span></span> 
- <span data-ttu-id="16264-3452">patient no</span><span class="sxs-lookup"><span data-stu-id="16264-3452">patient no</span></span> 
- <span data-ttu-id="16264-3453">patient number</span><span class="sxs-lookup"><span data-stu-id="16264-3453">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="16264-3454">Кэйворд_ук_нхс_нумбер_доб</span><span class="sxs-lookup"><span data-stu-id="16264-3454">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="16264-3455">ГРУПП</span><span class="sxs-lookup"><span data-stu-id="16264-3455">GP</span></span> 
- <span data-ttu-id="16264-3456">ДОБ</span><span class="sxs-lookup"><span data-stu-id="16264-3456">DOB</span></span> 
- <span data-ttu-id="16264-3457">D. O. B</span><span class="sxs-lookup"><span data-stu-id="16264-3457">D.O.B</span></span> 
- <span data-ttu-id="16264-3458">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="16264-3458">Date of Birth</span></span> 
- <span data-ttu-id="16264-3459">Birth Date</span><span class="sxs-lookup"><span data-stu-id="16264-3459">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="16264-p144">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="16264-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="16264-3462">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3462">Format</span></span>

<span data-ttu-id="16264-3463">7 символов или 9 символов, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3463">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3464">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3464">Pattern</span></span>

<span data-ttu-id="16264-3465">Два возможных шаблона:</span><span class="sxs-lookup"><span data-stu-id="16264-3465">Two possible patterns:</span></span>

- <span data-ttu-id="16264-3466">Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-3466">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="16264-3467">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3467">Six digits</span></span>
- <span data-ttu-id="16264-3468">"A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="16264-3468">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="16264-3469">OR</span><span class="sxs-lookup"><span data-stu-id="16264-3469">OR</span></span>

- <span data-ttu-id="16264-3470">Две буквы</span><span class="sxs-lookup"><span data-stu-id="16264-3470">Two letters</span></span>
- <span data-ttu-id="16264-3471">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3471">A space or dash</span></span>
- <span data-ttu-id="16264-3472">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3472">Two digits</span></span>
- <span data-ttu-id="16264-3473">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3473">A space or dash</span></span>
- <span data-ttu-id="16264-3474">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3474">Two digits</span></span>
- <span data-ttu-id="16264-3475">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3475">A space or dash</span></span>
- <span data-ttu-id="16264-3476">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3476">Two digits</span></span>
- <span data-ttu-id="16264-3477">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3477">A space or dash</span></span>
- <span data-ttu-id="16264-3478">Значение "A", "B", "C" или "'D"</span><span class="sxs-lookup"><span data-stu-id="16264-3478">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3479">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3479">Checksum</span></span>

<span data-ttu-id="16264-3480">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3480">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3481">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3481">Definition</span></span>

<span data-ttu-id="16264-3482">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3482">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3483">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3483">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3484">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="16264-3484">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="16264-3485">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3485">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3486">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3486">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3487">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="16264-3487">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3488">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3488">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="16264-3489">Кэйворд_ук_нино</span><span class="sxs-lookup"><span data-stu-id="16264-3489">Keyword_uk_nino</span></span>

- <span data-ttu-id="16264-3490">national insurance number</span><span class="sxs-lookup"><span data-stu-id="16264-3490">national insurance number</span></span> 
- <span data-ttu-id="16264-3491">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="16264-3491">national insurance contributions</span></span> 
- <span data-ttu-id="16264-3492">protection act</span><span class="sxs-lookup"><span data-stu-id="16264-3492">protection act</span></span> 
- <span data-ttu-id="16264-3493">страхования</span><span class="sxs-lookup"><span data-stu-id="16264-3493">insurance</span></span> 
- <span data-ttu-id="16264-3494">social security number</span><span class="sxs-lookup"><span data-stu-id="16264-3494">social security number</span></span> 
- <span data-ttu-id="16264-3495">insurance application</span><span class="sxs-lookup"><span data-stu-id="16264-3495">insurance application</span></span> 
- <span data-ttu-id="16264-3496">medical application</span><span class="sxs-lookup"><span data-stu-id="16264-3496">medical application</span></span> 
- <span data-ttu-id="16264-3497">social insurance</span><span class="sxs-lookup"><span data-stu-id="16264-3497">social insurance</span></span> 
- <span data-ttu-id="16264-3498">medical attention</span><span class="sxs-lookup"><span data-stu-id="16264-3498">medical attention</span></span> 
- <span data-ttu-id="16264-3499">social security</span><span class="sxs-lookup"><span data-stu-id="16264-3499">social security</span></span> 
- <span data-ttu-id="16264-3500">great britain</span><span class="sxs-lookup"><span data-stu-id="16264-3500">great britain</span></span> 
- <span data-ttu-id="16264-3501">страхования</span><span class="sxs-lookup"><span data-stu-id="16264-3501">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="16264-p145">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="16264-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3504">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3504">Format</span></span>

<span data-ttu-id="16264-3505">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3505">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3506">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3506">Pattern</span></span>

<span data-ttu-id="16264-3507">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="16264-3507">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3508">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3508">Checksum</span></span>

<span data-ttu-id="16264-3509">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3509">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3510">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3510">Definition</span></span>

<span data-ttu-id="16264-3511">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3511">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3512">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3512">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3513">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="16264-3513">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3514">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3514">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="16264-3515">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="16264-3515">Keyword_passport</span></span>

- <span data-ttu-id="16264-3516">Passport Number</span><span class="sxs-lookup"><span data-stu-id="16264-3516">Passport Number</span></span> 
- <span data-ttu-id="16264-3517">Passport No</span><span class="sxs-lookup"><span data-stu-id="16264-3517">Passport No</span></span> 
- <span data-ttu-id="16264-3518">Passport#</span><span class="sxs-lookup"><span data-stu-id="16264-3518">Passport #</span></span> 
- <span data-ttu-id="16264-3519">Службу</span><span class="sxs-lookup"><span data-stu-id="16264-3519">Passport#</span></span> 
- <span data-ttu-id="16264-3520">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="16264-3520">PassportID</span></span> 
- <span data-ttu-id="16264-3521">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="16264-3521">Passportno</span></span> 
- <span data-ttu-id="16264-3522">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="16264-3522">passportnumber</span></span> 
- <span data-ttu-id="16264-3523">パスポート</span><span class="sxs-lookup"><span data-stu-id="16264-3523">パスポート</span></span> 
- <span data-ttu-id="16264-3524">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="16264-3524">パスポート番号</span></span> 
- <span data-ttu-id="16264-3525">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="16264-3525">パスポートのNum</span></span> 
- <span data-ttu-id="16264-3526">パスポート #</span><span class="sxs-lookup"><span data-stu-id="16264-3526">パスポート＃</span></span> 
- <span data-ttu-id="16264-3527">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="16264-3527">Numéro de passeport</span></span> 
- <span data-ttu-id="16264-3528">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="16264-3528">Passeport n °</span></span> 
- <span data-ttu-id="16264-3529">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="16264-3529">Passeport Non</span></span> 
- <span data-ttu-id="16264-3530">Passeport#</span><span class="sxs-lookup"><span data-stu-id="16264-3530">Passeport #</span></span> 
- <span data-ttu-id="16264-3531">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="16264-3531">Passeport#</span></span> 
- <span data-ttu-id="16264-3532">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="16264-3532">PasseportNon</span></span> 
- <span data-ttu-id="16264-3533">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="16264-3533">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="16264-3534">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="16264-3534">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3535">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3535">Format</span></span>

<span data-ttu-id="16264-3536">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3536">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3537">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3537">Pattern</span></span>

<span data-ttu-id="16264-3538">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3538">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3539">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3539">Checksum</span></span>

<span data-ttu-id="16264-3540">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3540">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3541">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3541">Definition</span></span>

<span data-ttu-id="16264-3542">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3542">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3543">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3543">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3544">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="16264-3544">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="16264-3545">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3545">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="16264-3546">Кэйворд_уса_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="16264-3546">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="16264-3547">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-3547">Checking Account Number</span></span> 
- <span data-ttu-id="16264-3548">Checking Account</span><span class="sxs-lookup"><span data-stu-id="16264-3548">Checking Account</span></span> 
- <span data-ttu-id="16264-3549">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="16264-3549">Checking Account #</span></span> 
- <span data-ttu-id="16264-3550">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-3550">Checking Acct Number</span></span> 
- <span data-ttu-id="16264-3551">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-3551">Checking Acct #</span></span> 
- <span data-ttu-id="16264-3552">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-3552">Checking Acct No.</span></span> 
- <span data-ttu-id="16264-3553">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-3553">Checking Account No.</span></span> 
- <span data-ttu-id="16264-3554">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-3554">Bank Account Number</span></span> 
- <span data-ttu-id="16264-3555">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="16264-3555">Bank Account #</span></span> 
- <span data-ttu-id="16264-3556">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-3556">Bank Acct Number</span></span> 
- <span data-ttu-id="16264-3557">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-3557">Bank Acct #</span></span> 
- <span data-ttu-id="16264-3558">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-3558">Bank Acct No.</span></span> 
- <span data-ttu-id="16264-3559">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-3559">Bank Account No.</span></span> 
- <span data-ttu-id="16264-3560">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-3560">Savings Account Number</span></span> 
- <span data-ttu-id="16264-3561">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="16264-3561">Savings Account.</span></span> 
- <span data-ttu-id="16264-3562">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="16264-3562">Savings Account #</span></span> 
- <span data-ttu-id="16264-3563">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-3563">Savings Acct Number</span></span> 
- <span data-ttu-id="16264-3564">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-3564">Savings Acct #</span></span> 
- <span data-ttu-id="16264-3565">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-3565">Savings Acct No.</span></span> 
- <span data-ttu-id="16264-3566">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-3566">Savings Account No.</span></span> 
- <span data-ttu-id="16264-3567">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="16264-3567">Debit Account Number</span></span> 
- <span data-ttu-id="16264-3568">Debit Account</span><span class="sxs-lookup"><span data-stu-id="16264-3568">Debit Account</span></span> 
- <span data-ttu-id="16264-3569">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="16264-3569">Debit Account #</span></span> 
- <span data-ttu-id="16264-3570">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="16264-3570">Debit Acct Number</span></span> 
- <span data-ttu-id="16264-3571">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="16264-3571">Debit Acct #</span></span> 
- <span data-ttu-id="16264-3572">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="16264-3572">Debit Acct No.</span></span> 
- <span data-ttu-id="16264-3573">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="16264-3573">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="16264-3574">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="16264-3574">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="16264-3575">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3575">Format</span></span>

<span data-ttu-id="16264-3576">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="16264-3576">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3577">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3577">Pattern</span></span>

<span data-ttu-id="16264-3578">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="16264-3578">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="16264-3579">Девять цифр, отформатированных как DDD DDD DDD, будут совпадают.</span><span class="sxs-lookup"><span data-stu-id="16264-3579">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="16264-3580">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="16264-3580">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3581">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3581">Checksum</span></span>

<span data-ttu-id="16264-3582">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3582">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3583">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3583">Definition</span></span>

<span data-ttu-id="16264-3584">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3585">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3585">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3586">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="16264-3586">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="16264-3587">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="16264-3587">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="16264-3588">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3588">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3589">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="16264-3589">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3590">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="16264-3590">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="16264-3591">находится ключевое слово из Keyword_us_drivers_license_abbreviations.</span><span class="sxs-lookup"><span data-stu-id="16264-3591">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="16264-3592">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="16264-3592">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3593">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3593">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="16264-3594">Кэйворд_ус_дриверс_лиценсе_аббревиатионс</span><span class="sxs-lookup"><span data-stu-id="16264-3594">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="16264-3595">DL</span><span class="sxs-lookup"><span data-stu-id="16264-3595">DL</span></span> 
- <span data-ttu-id="16264-3596">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="16264-3596">DLS</span></span> 
- <span data-ttu-id="16264-3597">КДЛ</span><span class="sxs-lookup"><span data-stu-id="16264-3597">CDL</span></span> 
- <span data-ttu-id="16264-3598">КДЛС</span><span class="sxs-lookup"><span data-stu-id="16264-3598">CDLS</span></span> 
- <span data-ttu-id="16264-3599">ИД</span><span class="sxs-lookup"><span data-stu-id="16264-3599">ID</span></span> 
- <span data-ttu-id="16264-3600">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="16264-3600">IDs</span></span> 
- <span data-ttu-id="16264-3601">DL</span><span class="sxs-lookup"><span data-stu-id="16264-3601">DL#</span></span> 
- <span data-ttu-id="16264-3602">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="16264-3602">DLS#</span></span> 
- <span data-ttu-id="16264-3603">КДЛ #</span><span class="sxs-lookup"><span data-stu-id="16264-3603">CDL#</span></span> 
- <span data-ttu-id="16264-3604">КДЛС #</span><span class="sxs-lookup"><span data-stu-id="16264-3604">CDLS#</span></span> 
- <span data-ttu-id="16264-3605">КОДОВ</span><span class="sxs-lookup"><span data-stu-id="16264-3605">ID#</span></span>
- <span data-ttu-id="16264-3606">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="16264-3606">IDs#</span></span> 
- <span data-ttu-id="16264-3607">ID number</span><span class="sxs-lookup"><span data-stu-id="16264-3607">ID number</span></span> 
- <span data-ttu-id="16264-3608">ID numbers</span><span class="sxs-lookup"><span data-stu-id="16264-3608">ID numbers</span></span> 
- <span data-ttu-id="16264-3609">Лик</span><span class="sxs-lookup"><span data-stu-id="16264-3609">LIC</span></span> 
- <span data-ttu-id="16264-3610">Лик #</span><span class="sxs-lookup"><span data-stu-id="16264-3610">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="16264-3611">Кэйворд_ус_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-3611">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="16264-3612">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="16264-3612">DriverLic</span></span> 
- <span data-ttu-id="16264-3613">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="16264-3613">DriverLics</span></span> 
- <span data-ttu-id="16264-3614">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-3614">DriverLicense</span></span> 
- <span data-ttu-id="16264-3615">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-3615">DriverLicenses</span></span> 
- <span data-ttu-id="16264-3616">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="16264-3616">Driver Lic</span></span> 
- <span data-ttu-id="16264-3617">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="16264-3617">Driver Lics</span></span> 
- <span data-ttu-id="16264-3618">Driver License</span><span class="sxs-lookup"><span data-stu-id="16264-3618">Driver License</span></span> 
- <span data-ttu-id="16264-3619">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-3619">Driver Licenses</span></span> 
- <span data-ttu-id="16264-3620">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="16264-3620">DriversLic</span></span> 
- <span data-ttu-id="16264-3621">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="16264-3621">DriversLics</span></span> 
- <span data-ttu-id="16264-3622">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-3622">DriversLicense</span></span> 
- <span data-ttu-id="16264-3623">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-3623">DriversLicenses</span></span> 
- <span data-ttu-id="16264-3624">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="16264-3624">Drivers Lic</span></span> 
- <span data-ttu-id="16264-3625">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="16264-3625">Drivers Lics</span></span> 
- <span data-ttu-id="16264-3626">Drivers License</span><span class="sxs-lookup"><span data-stu-id="16264-3626">Drivers License</span></span> 
- <span data-ttu-id="16264-3627">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-3627">Drivers Licenses</span></span> 
- <span data-ttu-id="16264-3628">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="16264-3628">Driver'Lic</span></span> 
- <span data-ttu-id="16264-3629">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="16264-3629">Driver'Lics</span></span> 
- <span data-ttu-id="16264-3630">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="16264-3630">Driver'License</span></span> 
- <span data-ttu-id="16264-3631">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-3631">Driver'Licenses</span></span> 
- <span data-ttu-id="16264-3632">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="16264-3632">Driver' Lic</span></span> 
- <span data-ttu-id="16264-3633">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="16264-3633">Driver' Lics</span></span> 
- <span data-ttu-id="16264-3634">Driver' License</span><span class="sxs-lookup"><span data-stu-id="16264-3634">Driver' License</span></span> 
- <span data-ttu-id="16264-3635">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-3635">Driver' Licenses</span></span>
- <span data-ttu-id="16264-3636">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="16264-3636">Driver'sLic</span></span> 
- <span data-ttu-id="16264-3637">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="16264-3637">Driver'sLics</span></span> 
- <span data-ttu-id="16264-3638">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="16264-3638">Driver'sLicense</span></span> 
- <span data-ttu-id="16264-3639">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="16264-3639">Driver'sLicenses</span></span> 
- <span data-ttu-id="16264-3640">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="16264-3640">Driver's Lic</span></span> 
- <span data-ttu-id="16264-3641">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="16264-3641">Driver's Lics</span></span> 
- <span data-ttu-id="16264-3642">Driver's License</span><span class="sxs-lookup"><span data-stu-id="16264-3642">Driver's License</span></span> 
- <span data-ttu-id="16264-3643">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-3643">Driver's Licenses</span></span> 
- <span data-ttu-id="16264-3644">identification number</span><span class="sxs-lookup"><span data-stu-id="16264-3644">identification number</span></span> 
- <span data-ttu-id="16264-3645">identification numbers</span><span class="sxs-lookup"><span data-stu-id="16264-3645">identification numbers</span></span> 
- <span data-ttu-id="16264-3646">identification #</span><span class="sxs-lookup"><span data-stu-id="16264-3646">identification #</span></span> 
- <span data-ttu-id="16264-3647">id card</span><span class="sxs-lookup"><span data-stu-id="16264-3647">id card</span></span> 
- <span data-ttu-id="16264-3648">id cards</span><span class="sxs-lookup"><span data-stu-id="16264-3648">id cards</span></span> 
- <span data-ttu-id="16264-3649">identification card</span><span class="sxs-lookup"><span data-stu-id="16264-3649">identification card</span></span> 
- <span data-ttu-id="16264-3650">identification cards</span><span class="sxs-lookup"><span data-stu-id="16264-3650">identification cards</span></span> 
- <span data-ttu-id="16264-3651">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="16264-3651">DriverLic#</span></span> 
- <span data-ttu-id="16264-3652">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="16264-3652">DriverLics#</span></span> 
- <span data-ttu-id="16264-3653">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-3653">DriverLicense#</span></span> 
- <span data-ttu-id="16264-3654">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-3654">DriverLicenses#</span></span> 
- <span data-ttu-id="16264-3655">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-3655">Driver Lic#</span></span> 
- <span data-ttu-id="16264-3656">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-3656">Driver Lics#</span></span> 
- <span data-ttu-id="16264-3657">Driver License#</span><span class="sxs-lookup"><span data-stu-id="16264-3657">Driver License#</span></span> 
- <span data-ttu-id="16264-3658">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-3658">Driver Licenses#</span></span> 
- <span data-ttu-id="16264-3659">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="16264-3659">DriversLic#</span></span> 
- <span data-ttu-id="16264-3660">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="16264-3660">DriversLics#</span></span> 
- <span data-ttu-id="16264-3661">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-3661">DriversLicense#</span></span> 
- <span data-ttu-id="16264-3662">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-3662">DriversLicenses#</span></span> 
- <span data-ttu-id="16264-3663">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-3663">Drivers Lic#</span></span> 
- <span data-ttu-id="16264-3664">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-3664">Drivers Lics#</span></span> 
- <span data-ttu-id="16264-3665">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="16264-3665">Drivers License#</span></span> 
- <span data-ttu-id="16264-3666">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-3666">Drivers Licenses#</span></span> 
- <span data-ttu-id="16264-3667">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="16264-3667">Driver'Lic#</span></span> 
- <span data-ttu-id="16264-3668">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="16264-3668">Driver'Lics#</span></span> 
- <span data-ttu-id="16264-3669">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="16264-3669">Driver'License#</span></span> 
- <span data-ttu-id="16264-3670">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="16264-3670">Driver'Licenses#</span></span> 
- <span data-ttu-id="16264-3671">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-3671">Driver' Lic#</span></span> 
- <span data-ttu-id="16264-3672">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-3672">Driver' Lics#</span></span> 
- <span data-ttu-id="16264-3673">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="16264-3673">Driver' License#</span></span> 
- <span data-ttu-id="16264-3674">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-3674">Driver' Licenses#</span></span> 
- <span data-ttu-id="16264-3675">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="16264-3675">Driver'sLic#</span></span> 
- <span data-ttu-id="16264-3676">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="16264-3676">Driver'sLics#</span></span> 
- <span data-ttu-id="16264-3677">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="16264-3677">Driver'sLicense#</span></span> 
- <span data-ttu-id="16264-3678">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="16264-3678">Driver'sLicenses#</span></span> 
- <span data-ttu-id="16264-3679">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="16264-3679">Driver's Lic#</span></span> 
- <span data-ttu-id="16264-3680">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="16264-3680">Driver's Lics#</span></span> 
- <span data-ttu-id="16264-3681">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="16264-3681">Driver's License#</span></span> 
- <span data-ttu-id="16264-3682">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="16264-3682">Driver's Licenses#</span></span> 
- <span data-ttu-id="16264-3683">id card#</span><span class="sxs-lookup"><span data-stu-id="16264-3683">id card#</span></span> 
- <span data-ttu-id="16264-3684">id cards#</span><span class="sxs-lookup"><span data-stu-id="16264-3684">id cards#</span></span> 
- <span data-ttu-id="16264-3685">identification card#</span><span class="sxs-lookup"><span data-stu-id="16264-3685">identification card#</span></span> 
- <span data-ttu-id="16264-3686">identification cards#</span><span class="sxs-lookup"><span data-stu-id="16264-3686">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="16264-3687">Кэйворд_ [стате_наме] _дриверс_лиценсе_наме</span><span class="sxs-lookup"><span data-stu-id="16264-3687">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="16264-3688">Аббревиатура штата (например, NY)</span><span class="sxs-lookup"><span data-stu-id="16264-3688">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="16264-3689">Название штата (например, New York)</span><span class="sxs-lookup"><span data-stu-id="16264-3689">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="16264-3690">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="16264-3690">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-3691">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3691">Format</span></span>

<span data-ttu-id="16264-3692">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="16264-3692">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3693">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3693">Pattern</span></span>

<span data-ttu-id="16264-3694">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="16264-3694">Formatted:</span></span>
- <span data-ttu-id="16264-3695">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="16264-3695">The digit "9"</span></span> 
- <span data-ttu-id="16264-3696">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3696">Two digits</span></span> 
- <span data-ttu-id="16264-3697">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3697">A space or dash</span></span> 
- <span data-ttu-id="16264-3698">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="16264-3698">A "7" or "8"</span></span> 
- <span data-ttu-id="16264-3699">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="16264-3699">A digit</span></span> 
- <span data-ttu-id="16264-3700">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="16264-3700">A space, or dash</span></span> 
- <span data-ttu-id="16264-3701">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3701">Four digits</span></span>

<span data-ttu-id="16264-3702">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="16264-3702">Unformatted:</span></span>
- <span data-ttu-id="16264-3703">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="16264-3703">The digit "9"</span></span> 
- <span data-ttu-id="16264-3704">Две цифры</span><span class="sxs-lookup"><span data-stu-id="16264-3704">Two digits</span></span> 
- <span data-ttu-id="16264-3705">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="16264-3705">A "7" or "8"</span></span> 
- <span data-ttu-id="16264-3706">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="16264-3706">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3707">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3707">Checksum</span></span>

<span data-ttu-id="16264-3708">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3708">No</span></span>

### <a name="definition"></a><span data-ttu-id="16264-3709">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3709">Definition</span></span>

<span data-ttu-id="16264-3710">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3710">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3711">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3711">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3712">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-3712">At least one of the following is true:</span></span>
    - <span data-ttu-id="16264-3713">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="16264-3713">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="16264-3714">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="16264-3714">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="16264-3715">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-3715">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="16264-3716">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="16264-3716">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="16264-3717">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3717">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3718">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3718">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3719">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="16264-3719">At least one of the following is true:</span></span>
    - <span data-ttu-id="16264-3720">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="16264-3720">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="16264-3721">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="16264-3721">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="16264-3722">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="16264-3722">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3723">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3723">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="16264-3724">Кэйворд_итин</span><span class="sxs-lookup"><span data-stu-id="16264-3724">Keyword_itin</span></span>

- <span data-ttu-id="16264-3725">дубликат</span><span class="sxs-lookup"><span data-stu-id="16264-3725">taxpayer</span></span> 
- <span data-ttu-id="16264-3726">tax id</span><span class="sxs-lookup"><span data-stu-id="16264-3726">tax id</span></span> 
- <span data-ttu-id="16264-3727">tax identification</span><span class="sxs-lookup"><span data-stu-id="16264-3727">tax identification</span></span> 
- <span data-ttu-id="16264-3728">SharePointв</span><span class="sxs-lookup"><span data-stu-id="16264-3728">itin</span></span> 
- <span data-ttu-id="16264-3729">SSN</span><span class="sxs-lookup"><span data-stu-id="16264-3729">ssn</span></span> 
- <span data-ttu-id="16264-3730">ИНН</span><span class="sxs-lookup"><span data-stu-id="16264-3730">tin</span></span> 
- <span data-ttu-id="16264-3731">social security</span><span class="sxs-lookup"><span data-stu-id="16264-3731">social security</span></span> 
- <span data-ttu-id="16264-3732">tax payer</span><span class="sxs-lookup"><span data-stu-id="16264-3732">tax payer</span></span> 
- <span data-ttu-id="16264-3733">итинс</span><span class="sxs-lookup"><span data-stu-id="16264-3733">itins</span></span> 
- <span data-ttu-id="16264-3734">такси</span><span class="sxs-lookup"><span data-stu-id="16264-3734">taxid</span></span> 
- <span data-ttu-id="16264-3735">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="16264-3735">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="16264-3736">Кэйворд_итин_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="16264-3736">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="16264-3737">License</span><span class="sxs-lookup"><span data-stu-id="16264-3737">License</span></span> 
- <span data-ttu-id="16264-3738">DL</span><span class="sxs-lookup"><span data-stu-id="16264-3738">DL</span></span> 
- <span data-ttu-id="16264-3739">ДОБ</span><span class="sxs-lookup"><span data-stu-id="16264-3739">DOB</span></span> 
- <span data-ttu-id="16264-3740">Birthdate</span><span class="sxs-lookup"><span data-stu-id="16264-3740">Birthdate</span></span> 
- <span data-ttu-id="16264-3741">День рождения</span><span class="sxs-lookup"><span data-stu-id="16264-3741">Birthday</span></span> 
- <span data-ttu-id="16264-3742">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="16264-3742">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="16264-3743">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="16264-3743">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="16264-3744">Format</span><span class="sxs-lookup"><span data-stu-id="16264-3744">Format</span></span>

<span data-ttu-id="16264-3745">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="16264-3745">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="16264-3746">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="16264-3746">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="16264-3747">Шаблон</span><span class="sxs-lookup"><span data-stu-id="16264-3747">Pattern</span></span>

<span data-ttu-id="16264-3748">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="16264-3748">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="16264-3749">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="16264-3749">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="16264-3750">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="16264-3750">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="16264-3751">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="16264-3751">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="16264-3752">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="16264-3752">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="16264-3753">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="16264-3753">Checksum</span></span>

<span data-ttu-id="16264-3754">Нет</span><span class="sxs-lookup"><span data-stu-id="16264-3754">No</span></span>


### <a name="definition"></a><span data-ttu-id="16264-3755">Определение</span><span class="sxs-lookup"><span data-stu-id="16264-3755">Definition</span></span>

<span data-ttu-id="16264-3756">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3756">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3757">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3757">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3758">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="16264-3758">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="16264-3759">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3759">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3760">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3760">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3761">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="16264-3761">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="16264-3762">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3762">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3763">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3763">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3764">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="16264-3764">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="16264-3765">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3765">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="16264-3766">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="16264-3766">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="16264-3767">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3767">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="16264-3768">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="16264-3768">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="16264-3769">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="16264-3769">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="16264-3770">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="16264-3770">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="16264-3771">Кэйворд_ссн</span><span class="sxs-lookup"><span data-stu-id="16264-3771">Keyword_ssn</span></span>

- <span data-ttu-id="16264-3772">Social Security</span><span class="sxs-lookup"><span data-stu-id="16264-3772">Social Security</span></span> 
- <span data-ttu-id="16264-3773">Social Security#</span><span class="sxs-lookup"><span data-stu-id="16264-3773">Social Security#</span></span> 
- <span data-ttu-id="16264-3774">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="16264-3774">Soc Sec</span></span> 
- <span data-ttu-id="16264-3775">SSN</span><span class="sxs-lookup"><span data-stu-id="16264-3775">SSN</span></span> 
- <span data-ttu-id="16264-3776">SSNS</span><span class="sxs-lookup"><span data-stu-id="16264-3776">SSNS</span></span> 
- <span data-ttu-id="16264-3777">SSN</span><span class="sxs-lookup"><span data-stu-id="16264-3777">SSN#</span></span> 
- <span data-ttu-id="16264-3778">НН</span><span class="sxs-lookup"><span data-stu-id="16264-3778">SS#</span></span> 
- <span data-ttu-id="16264-3779">SSID</span><span class="sxs-lookup"><span data-stu-id="16264-3779">SSID</span></span> 
   

