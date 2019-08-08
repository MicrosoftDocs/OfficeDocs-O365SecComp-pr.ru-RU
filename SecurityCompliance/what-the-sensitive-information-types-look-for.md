---
title: Что позволяют искать типы конфиденциальной информации
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 05/20/2019
audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Защита от потери данных (DLP) в центре безопасности &amp; Office 365 включает в себя 80 типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных. В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.
ms.openlocfilehash: 7f5c879b35f77ef142b8c45965357715f577832e
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230383"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="5c862-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="5c862-104">What the sensitive information types look for</span></span>

<span data-ttu-id="5c862-105">Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="5c862-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="5c862-106">В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.</span><span class="sxs-lookup"><span data-stu-id="5c862-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="5c862-107">Тип конфиденциальной информации определяется шаблоном, который можно идентифицировать регулярным выражением или функцией.</span><span class="sxs-lookup"><span data-stu-id="5c862-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="5c862-108">Кроме того, для идентификации типа конфиденциальной информации могут использоваться подкрепляющие доказательства, такие как ключевые слова и контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="5c862-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="5c862-109">Уровень вероятности и расположение слов и знаков также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="5c862-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="5c862-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="5c862-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-111">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-111">Format</span></span>

<span data-ttu-id="5c862-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="5c862-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-113">Pattern</span></span>

<span data-ttu-id="5c862-114">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="5c862-114">Formatted:</span></span>
- <span data-ttu-id="5c862-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="5c862-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="5c862-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-116">A hyphen</span></span>
- <span data-ttu-id="5c862-117">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-117">Four digits</span></span>
- <span data-ttu-id="5c862-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-118">A hyphen</span></span>
- <span data-ttu-id="5c862-119">цифра.</span><span class="sxs-lookup"><span data-stu-id="5c862-119">A digit</span></span>

<span data-ttu-id="5c862-120">Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8.</span><span class="sxs-lookup"><span data-stu-id="5c862-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="5c862-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-121">Checksum</span></span>

<span data-ttu-id="5c862-122">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-123">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-123">Definition</span></span>

<span data-ttu-id="5c862-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="5c862-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="5c862-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="5c862-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="5c862-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="5c862-129">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="5c862-129">aba</span></span>
- <span data-ttu-id="5c862-130">aba#</span><span class="sxs-lookup"><span data-stu-id="5c862-130">aba #</span></span>
- <span data-ttu-id="5c862-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="5c862-131">aba routing #</span></span>
- <span data-ttu-id="5c862-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="5c862-132">aba routing number</span></span>
- <span data-ttu-id="5c862-133">код банка ABA #</span><span class="sxs-lookup"><span data-stu-id="5c862-133">aba#</span></span>
- <span data-ttu-id="5c862-134">абараутинг #</span><span class="sxs-lookup"><span data-stu-id="5c862-134">abarouting#</span></span>
- <span data-ttu-id="5c862-135">aba number</span><span class="sxs-lookup"><span data-stu-id="5c862-135">aba number</span></span>
- <span data-ttu-id="5c862-136">абараутингнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-136">abaroutingnumber</span></span>
- <span data-ttu-id="5c862-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="5c862-137">american bank association routing #</span></span>
- <span data-ttu-id="5c862-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="5c862-138">american bank association routing number</span></span>
- <span data-ttu-id="5c862-139">американбанкассоЦиатионраутинг #</span><span class="sxs-lookup"><span data-stu-id="5c862-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="5c862-140">американбанкассоЦиатионраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="5c862-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="5c862-141">bank routing number</span></span>
- <span data-ttu-id="5c862-142">банкраутинг #</span><span class="sxs-lookup"><span data-stu-id="5c862-142">bankrouting#</span></span>
- <span data-ttu-id="5c862-143">банкраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-143">bankroutingnumber</span></span>
- <span data-ttu-id="5c862-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="5c862-144">routing transit number</span></span>
- <span data-ttu-id="5c862-145">ртн</span><span class="sxs-lookup"><span data-stu-id="5c862-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="5c862-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="5c862-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-147">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-147">Format</span></span>

<span data-ttu-id="5c862-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="5c862-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-149">Pattern</span></span>

<span data-ttu-id="5c862-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-150">Eight digits:</span></span>
- <span data-ttu-id="5c862-151">две цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-151">Two digits</span></span>
- <span data-ttu-id="5c862-152">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-152">A period</span></span>
- <span data-ttu-id="5c862-153">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-153">Three digits</span></span>
- <span data-ttu-id="5c862-154">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-154">A period</span></span>
- <span data-ttu-id="5c862-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-156">Checksum</span></span>

<span data-ttu-id="5c862-157">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-158">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-158">Definition</span></span>

<span data-ttu-id="5c862-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="5c862-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="5c862-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="5c862-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="5c862-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="5c862-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="5c862-165">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="5c862-165">Identity</span></span> 
- <span data-ttu-id="5c862-166">Идентификация национальной идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="5c862-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="5c862-167">DNI</span><span class="sxs-lookup"><span data-stu-id="5c862-167">DNI</span></span> 
- <span data-ttu-id="5c862-168">Национальная реестр пользователей NIC</span><span class="sxs-lookup"><span data-stu-id="5c862-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="5c862-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="5c862-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="5c862-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="5c862-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="5c862-171">идентидад</span><span class="sxs-lookup"><span data-stu-id="5c862-171">Identidad</span></span> 
- <span data-ttu-id="5c862-172">идентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="5c862-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="5c862-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="5c862-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-174">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-174">Format</span></span>

<span data-ttu-id="5c862-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="5c862-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-176">Pattern</span></span>

<span data-ttu-id="5c862-177">Номер счета состоит из 6–10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="5c862-178">Номер филиала государственного банка Австралии</span><span class="sxs-lookup"><span data-stu-id="5c862-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="5c862-179">три цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-179">Three digits</span></span> 
- <span data-ttu-id="5c862-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-180">A hyphen</span></span> 
- <span data-ttu-id="5c862-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-182">Checksum</span></span>

<span data-ttu-id="5c862-183">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-184">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-184">Definition</span></span>

<span data-ttu-id="5c862-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="5c862-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="5c862-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="5c862-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="5c862-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="5c862-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="5c862-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="5c862-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="5c862-194">swift bank code</span></span>
- <span data-ttu-id="5c862-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="5c862-195">correspondent bank</span></span>
- <span data-ttu-id="5c862-196">base currency</span><span class="sxs-lookup"><span data-stu-id="5c862-196">base currency</span></span>
- <span data-ttu-id="5c862-197">usa account</span><span class="sxs-lookup"><span data-stu-id="5c862-197">usa account</span></span>
- <span data-ttu-id="5c862-198">holder address</span><span class="sxs-lookup"><span data-stu-id="5c862-198">holder address</span></span>
- <span data-ttu-id="5c862-199">bank address</span><span class="sxs-lookup"><span data-stu-id="5c862-199">bank address</span></span>
- <span data-ttu-id="5c862-200">information account</span><span class="sxs-lookup"><span data-stu-id="5c862-200">information account</span></span>
- <span data-ttu-id="5c862-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="5c862-201">fund transfers</span></span>
- <span data-ttu-id="5c862-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="5c862-202">bank charges</span></span>
- <span data-ttu-id="5c862-203">bank details</span><span class="sxs-lookup"><span data-stu-id="5c862-203">bank details</span></span>
- <span data-ttu-id="5c862-204">banking information</span><span class="sxs-lookup"><span data-stu-id="5c862-204">banking information</span></span>
- <span data-ttu-id="5c862-205">full names</span><span class="sxs-lookup"><span data-stu-id="5c862-205">full names</span></span>
- <span data-ttu-id="5c862-206">иаеа</span><span class="sxs-lookup"><span data-stu-id="5c862-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="5c862-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="5c862-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-208">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-208">Format</span></span>

<span data-ttu-id="5c862-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-210">Pattern</span></span>

<span data-ttu-id="5c862-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="5c862-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-213">две цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-213">Two digits</span></span> 
- <span data-ttu-id="5c862-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="5c862-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="5c862-215">OR</span><span class="sxs-lookup"><span data-stu-id="5c862-215">OR</span></span>

- <span data-ttu-id="5c862-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-217">4-9 digits</span></span>

<span data-ttu-id="5c862-218">OR</span><span class="sxs-lookup"><span data-stu-id="5c862-218">OR</span></span>

- <span data-ttu-id="5c862-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="5c862-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-220">Checksum</span></span>

<span data-ttu-id="5c862-221">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-222">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-222">Definition</span></span>

<span data-ttu-id="5c862-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="5c862-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="5c862-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="5c862-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="5c862-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="5c862-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="5c862-229">international driving permits</span></span>
- <span data-ttu-id="5c862-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="5c862-230">australian automobile association</span></span>
- <span data-ttu-id="5c862-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="5c862-231">international driving permit</span></span>
- <span data-ttu-id="5c862-232">дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="5c862-232">DriverLicence</span></span>
- <span data-ttu-id="5c862-233">дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="5c862-233">DriverLicences</span></span>
- <span data-ttu-id="5c862-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-234">Driver Lic</span></span>
- <span data-ttu-id="5c862-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-235">Driver Licence</span></span>
- <span data-ttu-id="5c862-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-236">Driver Licences</span></span>
- <span data-ttu-id="5c862-237">дриверслик</span><span class="sxs-lookup"><span data-stu-id="5c862-237">DriversLic</span></span>
- <span data-ttu-id="5c862-238">дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="5c862-238">DriversLicence</span></span>
- <span data-ttu-id="5c862-239">дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="5c862-239">DriversLicences</span></span>
- <span data-ttu-id="5c862-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-240">Drivers Lic</span></span>
- <span data-ttu-id="5c862-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-241">Drivers Lics</span></span>
- <span data-ttu-id="5c862-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-242">Drivers Licence</span></span>
- <span data-ttu-id="5c862-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-243">Drivers Licences</span></span>
- <span data-ttu-id="5c862-244">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="5c862-244">Driver'Lic</span></span>
- <span data-ttu-id="5c862-245">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="5c862-245">Driver'Lics</span></span>
- <span data-ttu-id="5c862-246">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-246">Driver'Licence</span></span>
- <span data-ttu-id="5c862-247">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-247">Driver'Licences</span></span>
- <span data-ttu-id="5c862-248">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-248">Driver' Lic</span></span>
- <span data-ttu-id="5c862-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-249">Driver' Lics</span></span>
- <span data-ttu-id="5c862-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-250">Driver' Licence</span></span>
- <span data-ttu-id="5c862-251">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-251">Driver' Licences</span></span>
- <span data-ttu-id="5c862-252">дривер'слик</span><span class="sxs-lookup"><span data-stu-id="5c862-252">Driver'sLic</span></span>
- <span data-ttu-id="5c862-253">дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="5c862-253">Driver'sLics</span></span>
- <span data-ttu-id="5c862-254">дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="5c862-254">Driver'sLicence</span></span>
- <span data-ttu-id="5c862-255">дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="5c862-255">Driver'sLicences</span></span>
- <span data-ttu-id="5c862-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-256">Driver's Lic</span></span>
- <span data-ttu-id="5c862-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-257">Driver's Lics</span></span>
- <span data-ttu-id="5c862-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-258">Driver's Licence</span></span>
- <span data-ttu-id="5c862-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-259">Driver's Licences</span></span>
- <span data-ttu-id="5c862-260">дриверлик #</span><span class="sxs-lookup"><span data-stu-id="5c862-260">DriverLic#</span></span>
- <span data-ttu-id="5c862-261">дриверликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-261">DriverLics#</span></span>
- <span data-ttu-id="5c862-262">дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="5c862-262">DriverLicence#</span></span>
- <span data-ttu-id="5c862-263">дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="5c862-263">DriverLicences#</span></span>
- <span data-ttu-id="5c862-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-264">Driver Lic#</span></span>
- <span data-ttu-id="5c862-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-265">Driver Lics#</span></span>
- <span data-ttu-id="5c862-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-266">Driver Licence#</span></span>
- <span data-ttu-id="5c862-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-267">Driver Licences#</span></span>
- <span data-ttu-id="5c862-268">дриверслик #</span><span class="sxs-lookup"><span data-stu-id="5c862-268">DriversLic#</span></span>
- <span data-ttu-id="5c862-269">дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-269">DriversLics#</span></span>
- <span data-ttu-id="5c862-270">дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="5c862-270">DriversLicence#</span></span>
- <span data-ttu-id="5c862-271">дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="5c862-271">DriversLicences#</span></span>
- <span data-ttu-id="5c862-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-272">Drivers Lic#</span></span>
- <span data-ttu-id="5c862-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-273">Drivers Lics#</span></span>
- <span data-ttu-id="5c862-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-274">Drivers Licence#</span></span>
- <span data-ttu-id="5c862-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-275">Drivers Licences#</span></span>
- <span data-ttu-id="5c862-276">Driver ' LIC #</span><span class="sxs-lookup"><span data-stu-id="5c862-276">Driver'Lic#</span></span>
- <span data-ttu-id="5c862-277">Driver ' LICS #</span><span class="sxs-lookup"><span data-stu-id="5c862-277">Driver'Lics#</span></span>
- <span data-ttu-id="5c862-278">Driver ' Licence #</span><span class="sxs-lookup"><span data-stu-id="5c862-278">Driver'Licence#</span></span>
- <span data-ttu-id="5c862-279">Driver ' Licences #</span><span class="sxs-lookup"><span data-stu-id="5c862-279">Driver'Licences#</span></span>
- <span data-ttu-id="5c862-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-280">Driver' Lic#</span></span>
- <span data-ttu-id="5c862-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-281">Driver' Lics#</span></span>
- <span data-ttu-id="5c862-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-282">Driver' Licence#</span></span>
- <span data-ttu-id="5c862-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-283">Driver' Licences#</span></span>
- <span data-ttu-id="5c862-284">дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="5c862-284">Driver'sLic#</span></span>
- <span data-ttu-id="5c862-285">дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-285">Driver'sLics#</span></span>
- <span data-ttu-id="5c862-286">дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="5c862-286">Driver'sLicence#</span></span>
- <span data-ttu-id="5c862-287">дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="5c862-287">Driver'sLicences#</span></span>
- <span data-ttu-id="5c862-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-288">Driver's Lic#</span></span>
- <span data-ttu-id="5c862-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-289">Driver's Lics#</span></span>
- <span data-ttu-id="5c862-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-290">Driver's Licence#</span></span>
- <span data-ttu-id="5c862-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="5c862-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="5c862-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="5c862-293">AAA</span><span class="sxs-lookup"><span data-stu-id="5c862-293">aaa</span></span>
- <span data-ttu-id="5c862-294">дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-294">DriverLicense</span></span>
- <span data-ttu-id="5c862-295">дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-295">DriverLicenses</span></span>
- <span data-ttu-id="5c862-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="5c862-296">Driver License</span></span>
- <span data-ttu-id="5c862-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-297">Driver Licenses</span></span>
- <span data-ttu-id="5c862-298">дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-298">DriversLicense</span></span>
- <span data-ttu-id="5c862-299">дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-299">DriversLicenses</span></span>
- <span data-ttu-id="5c862-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="5c862-300">Drivers License</span></span>
- <span data-ttu-id="5c862-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-301">Drivers Licenses</span></span>
- <span data-ttu-id="5c862-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="5c862-302">Driver'License</span></span>
- <span data-ttu-id="5c862-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-303">Driver'Licenses</span></span>
- <span data-ttu-id="5c862-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="5c862-304">Driver' License</span></span>
- <span data-ttu-id="5c862-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-305">Driver' Licenses</span></span>
- <span data-ttu-id="5c862-306">дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-306">Driver'sLicense</span></span>
- <span data-ttu-id="5c862-307">дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-307">Driver'sLicenses</span></span>
- <span data-ttu-id="5c862-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="5c862-308">Driver's License</span></span>
- <span data-ttu-id="5c862-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-309">Driver's Licenses</span></span>
- <span data-ttu-id="5c862-310">дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-310">DriverLicense#</span></span>
- <span data-ttu-id="5c862-311">дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-311">DriverLicenses#</span></span>
- <span data-ttu-id="5c862-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="5c862-312">Driver License#</span></span>
- <span data-ttu-id="5c862-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-313">Driver Licenses#</span></span>
- <span data-ttu-id="5c862-314">дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-314">DriversLicense#</span></span>
- <span data-ttu-id="5c862-315">дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-315">DriversLicenses#</span></span>
- <span data-ttu-id="5c862-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="5c862-316">Drivers License#</span></span>
- <span data-ttu-id="5c862-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-317">Drivers Licenses#</span></span>
- <span data-ttu-id="5c862-318">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="5c862-318">Driver'License#</span></span>
- <span data-ttu-id="5c862-319">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="5c862-319">Driver'Licenses#</span></span>
- <span data-ttu-id="5c862-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="5c862-320">Driver' License#</span></span>
- <span data-ttu-id="5c862-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-321">Driver' Licenses#</span></span>
- <span data-ttu-id="5c862-322">дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-322">Driver'sLicense#</span></span>
- <span data-ttu-id="5c862-323">дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="5c862-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="5c862-324">Driver's License#</span></span>
- <span data-ttu-id="5c862-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="5c862-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="5c862-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-327">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-327">Format</span></span>

<span data-ttu-id="5c862-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-329">Pattern</span></span>

<span data-ttu-id="5c862-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-330">10-11 digits:</span></span>
- <span data-ttu-id="5c862-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="5c862-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="5c862-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="5c862-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="5c862-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="5c862-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="5c862-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-335">Checksum</span></span>

<span data-ttu-id="5c862-336">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-337">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-337">Definition</span></span>

<span data-ttu-id="5c862-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="5c862-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="5c862-341">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-341">The checksum passes.</span></span>

<span data-ttu-id="5c862-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="5c862-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="5c862-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="5c862-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="5c862-347">bank account details</span></span>
- <span data-ttu-id="5c862-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="5c862-348">medicare payments</span></span>
- <span data-ttu-id="5c862-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="5c862-349">mortgage account</span></span>
- <span data-ttu-id="5c862-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="5c862-350">bank payments</span></span>
- <span data-ttu-id="5c862-351">information branch</span><span class="sxs-lookup"><span data-stu-id="5c862-351">information branch</span></span>
- <span data-ttu-id="5c862-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="5c862-352">credit card loan</span></span>
- <span data-ttu-id="5c862-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="5c862-353">department of human services</span></span>
- <span data-ttu-id="5c862-354">local service</span><span class="sxs-lookup"><span data-stu-id="5c862-354">local service</span></span>
- <span data-ttu-id="5c862-355">медикаре</span><span class="sxs-lookup"><span data-stu-id="5c862-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="5c862-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="5c862-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-357">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-357">Format</span></span>

<span data-ttu-id="5c862-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-359">Pattern</span></span>

<span data-ttu-id="5c862-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-361">Checksum</span></span>

<span data-ttu-id="5c862-362">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-363">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-363">Definition</span></span>

<span data-ttu-id="5c862-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-366">Найдено ключевое слово из Keyword_passport или Keyword_australia_passport_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="5c862-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-368">Keyword_passport</span></span>

- <span data-ttu-id="5c862-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="5c862-369">Passport Number</span></span>
- <span data-ttu-id="5c862-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="5c862-370">Passport No</span></span>
- <span data-ttu-id="5c862-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="5c862-371">Passport #</span></span>
- <span data-ttu-id="5c862-372">Службу #</span><span class="sxs-lookup"><span data-stu-id="5c862-372">Passport#</span></span>
- <span data-ttu-id="5c862-373">пасспортид</span><span class="sxs-lookup"><span data-stu-id="5c862-373">PassportID</span></span>
- <span data-ttu-id="5c862-374">пасспортно</span><span class="sxs-lookup"><span data-stu-id="5c862-374">Passportno</span></span>
- <span data-ttu-id="5c862-375">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-375">passportnumber</span></span>
- <span data-ttu-id="5c862-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="5c862-376">パスポート</span></span>
- <span data-ttu-id="5c862-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="5c862-377">パスポート番号</span></span>
- <span data-ttu-id="5c862-378">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="5c862-378">パスポートのNum</span></span>
- <span data-ttu-id="5c862-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="5c862-379">パスポート ＃</span></span> 
- <span data-ttu-id="5c862-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="5c862-380">Numéro de passeport</span></span>
- <span data-ttu-id="5c862-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="5c862-381">Passeport n °</span></span>
- <span data-ttu-id="5c862-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="5c862-382">Passeport Non</span></span>
- <span data-ttu-id="5c862-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="5c862-383">Passeport #</span></span>
- <span data-ttu-id="5c862-384">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="5c862-384">Passeport#</span></span>
- <span data-ttu-id="5c862-385">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="5c862-385">PasseportNon</span></span>
- <span data-ttu-id="5c862-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="5c862-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="5c862-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="5c862-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="5c862-388">службу</span><span class="sxs-lookup"><span data-stu-id="5c862-388">passport</span></span>
- <span data-ttu-id="5c862-389">passport details</span><span class="sxs-lookup"><span data-stu-id="5c862-389">passport details</span></span>
- <span data-ttu-id="5c862-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="5c862-390">immigration and citizenship</span></span>
- <span data-ttu-id="5c862-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="5c862-391">commonwealth of australia</span></span>
- <span data-ttu-id="5c862-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="5c862-392">department of immigration</span></span>
- <span data-ttu-id="5c862-393">residential address</span><span class="sxs-lookup"><span data-stu-id="5c862-393">residential address</span></span>
- <span data-ttu-id="5c862-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="5c862-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="5c862-395">Visa</span><span class="sxs-lookup"><span data-stu-id="5c862-395">visa</span></span>
- <span data-ttu-id="5c862-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="5c862-396">national identity card</span></span>
- <span data-ttu-id="5c862-397">passport number</span><span class="sxs-lookup"><span data-stu-id="5c862-397">passport number</span></span>
- <span data-ttu-id="5c862-398">travel document</span><span class="sxs-lookup"><span data-stu-id="5c862-398">travel document</span></span>
- <span data-ttu-id="5c862-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="5c862-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="5c862-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="5c862-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-401">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-401">Format</span></span>

<span data-ttu-id="5c862-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-403">Pattern</span></span>

<span data-ttu-id="5c862-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="5c862-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="5c862-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-405">Three digits</span></span> 
- <span data-ttu-id="5c862-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-406">An optional space</span></span> 
- <span data-ttu-id="5c862-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-407">Three digits</span></span> 
- <span data-ttu-id="5c862-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-408">An optional space</span></span> 
- <span data-ttu-id="5c862-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="5c862-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-410">Checksum</span></span>

<span data-ttu-id="5c862-411">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-412">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-412">Definition</span></span>

<span data-ttu-id="5c862-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="5c862-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="5c862-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-416">The checksum passes.</span></span>

```
   <!-- Australia Tax File Number -->
    <Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Match idRef="Keyword_Australia_Tax_File_Number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_number_exclusions" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="5c862-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="5c862-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="5c862-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="5c862-419">australian business number</span></span>
- <span data-ttu-id="5c862-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="5c862-420">marginal tax rate</span></span>
- <span data-ttu-id="5c862-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="5c862-421">medicare levy</span></span>
- <span data-ttu-id="5c862-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="5c862-422">portfolio number</span></span>
- <span data-ttu-id="5c862-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="5c862-423">service veterans</span></span>
- <span data-ttu-id="5c862-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="5c862-424">withholding tax</span></span>
- <span data-ttu-id="5c862-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="5c862-425">individual tax return</span></span>
- <span data-ttu-id="5c862-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="5c862-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="5c862-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="5c862-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="5c862-428">00000001</span><span class="sxs-lookup"><span data-stu-id="5c862-428">00000000</span></span>
- <span data-ttu-id="5c862-429">11111111</span><span class="sxs-lookup"><span data-stu-id="5c862-429">11111111</span></span>
- <span data-ttu-id="5c862-430">22222222</span><span class="sxs-lookup"><span data-stu-id="5c862-430">22222222</span></span>
- <span data-ttu-id="5c862-431">33333333</span><span class="sxs-lookup"><span data-stu-id="5c862-431">33333333</span></span>
- <span data-ttu-id="5c862-432">44444444</span><span class="sxs-lookup"><span data-stu-id="5c862-432">44444444</span></span>
- <span data-ttu-id="5c862-433">55555555</span><span class="sxs-lookup"><span data-stu-id="5c862-433">55555555</span></span>
- <span data-ttu-id="5c862-434">66666666</span><span class="sxs-lookup"><span data-stu-id="5c862-434">66666666</span></span>
- <span data-ttu-id="5c862-435">77777777</span><span class="sxs-lookup"><span data-stu-id="5c862-435">77777777</span></span>
- <span data-ttu-id="5c862-436">88888888</span><span class="sxs-lookup"><span data-stu-id="5c862-436">88888888</span></span>
- <span data-ttu-id="5c862-437">99999999</span><span class="sxs-lookup"><span data-stu-id="5c862-437">99999999</span></span>
- <span data-ttu-id="5c862-438">000000000</span><span class="sxs-lookup"><span data-stu-id="5c862-438">000000000</span></span>
- <span data-ttu-id="5c862-439">111111111</span><span class="sxs-lookup"><span data-stu-id="5c862-439">111111111</span></span>
- <span data-ttu-id="5c862-440">222222222</span><span class="sxs-lookup"><span data-stu-id="5c862-440">222222222</span></span>
- <span data-ttu-id="5c862-441">333333333</span><span class="sxs-lookup"><span data-stu-id="5c862-441">333333333</span></span>
- <span data-ttu-id="5c862-442">444444444</span><span class="sxs-lookup"><span data-stu-id="5c862-442">444444444</span></span>
- <span data-ttu-id="5c862-443">555555555</span><span class="sxs-lookup"><span data-stu-id="5c862-443">555555555</span></span>
- <span data-ttu-id="5c862-444">666666666</span><span class="sxs-lookup"><span data-stu-id="5c862-444">666666666</span></span>
- <span data-ttu-id="5c862-445">777777777</span><span class="sxs-lookup"><span data-stu-id="5c862-445">777777777</span></span>
- <span data-ttu-id="5c862-446">888888888</span><span class="sxs-lookup"><span data-stu-id="5c862-446">888888888</span></span>
- <span data-ttu-id="5c862-447">999999999</span><span class="sxs-lookup"><span data-stu-id="5c862-447">999999999</span></span>
- <span data-ttu-id="5c862-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="5c862-448">0000000000</span></span>
- <span data-ttu-id="5c862-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="5c862-449">1111111111</span></span>
- <span data-ttu-id="5c862-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="5c862-450">2222222222</span></span>
- <span data-ttu-id="5c862-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="5c862-451">3333333333</span></span>
- <span data-ttu-id="5c862-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="5c862-452">4444444444</span></span>
- <span data-ttu-id="5c862-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="5c862-453">5555555555</span></span>
- <span data-ttu-id="5c862-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="5c862-454">6666666666</span></span>
- <span data-ttu-id="5c862-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="5c862-455">7777777777</span></span>
- <span data-ttu-id="5c862-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="5c862-456">8888888888</span></span>
- <span data-ttu-id="5c862-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="5c862-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="5c862-458">Ключ проверки подлинности Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="5c862-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="5c862-459">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-459">Format</span></span>

<span data-ttu-id="5c862-460">Строка "DocumentDb", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="5c862-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-461">Pattern</span></span>

- <span data-ttu-id="5c862-462">Строка "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="5c862-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="5c862-463">Любая комбинация из 3-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-464">Символ "больше" (>), знак равенства (=), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="5c862-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="5c862-465">Любая комбинация 86 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="5c862-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="5c862-466">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="5c862-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-467">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-467">Checksum</span></span>

<span data-ttu-id="5c862-468">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-469">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-469">Definition</span></span>

<span data-ttu-id="5c862-470">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-471">Регулярное выражение CEP_Regex_AzureDocumentDBAuthKey находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-472">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-473">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-475">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-476">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-476">contoso</span></span>
- <span data-ttu-id="5c862-477">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-477">fabrikam</span></span>
- <span data-ttu-id="5c862-478">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-478">northwind</span></span>
- <span data-ttu-id="5c862-479">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-479">sandbox</span></span>
- <span data-ttu-id="5c862-480">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-480">onebox</span></span>
- <span data-ttu-id="5c862-481">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-481">localhost</span></span>
- <span data-ttu-id="5c862-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-482">127.0.0.1</span></span>
- <span data-ttu-id="5c862-483">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-484">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-484">com</span></span>
- <span data-ttu-id="5c862-485">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-486">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="5c862-487">Строка подключения к базе данных Azure IAAS и строка подключения к SQL Azure</span><span class="sxs-lookup"><span data-stu-id="5c862-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="5c862-488">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-488">Format</span></span>

<span data-ttu-id="5c862-489">Строка "Server", "Server" или "Data Source", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "клаудапп. Azure".</span><span class="sxs-lookup"><span data-stu-id="5c862-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-490">com "или" клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="5c862-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-491">NET "или" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="5c862-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-492">NET ", а также строку" Password "или" Password "или" pwd ".</span><span class="sxs-lookup"><span data-stu-id="5c862-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-493">Pattern</span></span>

- <span data-ttu-id="5c862-494">Строка "Server", "Server" или "Data Source"</span><span class="sxs-lookup"><span data-stu-id="5c862-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="5c862-495">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-496">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-496">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-497">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-498">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-499">Строка "клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="5c862-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-500">com "," клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="5c862-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-501">NET "или" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="5c862-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-502">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-502">net"</span></span>
- <span data-ttu-id="5c862-503">Любая комбинация из 1-300 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-504">Строка "Password", "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="5c862-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="5c862-505">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-506">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-506">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-507">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-508">Один или несколько символов, не отделяющая точку с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="5c862-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="5c862-509">Точка с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="5c862-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-510">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-510">Checksum</span></span>

<span data-ttu-id="5c862-511">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-512">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-512">Definition</span></span>

<span data-ttu-id="5c862-513">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-514">Регулярное выражение CEP_Regex_AzureConnectionString находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-515">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-516">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-518">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-519">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-519">contoso</span></span>
- <span data-ttu-id="5c862-520">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-520">fabrikam</span></span>
- <span data-ttu-id="5c862-521">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-521">northwind</span></span>
- <span data-ttu-id="5c862-522">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-522">sandbox</span></span>
- <span data-ttu-id="5c862-523">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-523">onebox</span></span>
- <span data-ttu-id="5c862-524">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-524">localhost</span></span>
- <span data-ttu-id="5c862-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-525">127.0.0.1</span></span>
- <span data-ttu-id="5c862-526">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-527">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-527">com</span></span>
- <span data-ttu-id="5c862-528">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-529">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="5c862-530">Строка подключения Azure IoT</span><span class="sxs-lookup"><span data-stu-id="5c862-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="5c862-531">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-531">Format</span></span>

<span data-ttu-id="5c862-532">Строка "HostName", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, включая строки "Azure — Devices.</span><span class="sxs-lookup"><span data-stu-id="5c862-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-533">NET "и" Шаредакцесскэй ".</span><span class="sxs-lookup"><span data-stu-id="5c862-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-534">Pattern</span></span>

- <span data-ttu-id="5c862-535">Строка "HostName"</span><span class="sxs-lookup"><span data-stu-id="5c862-535">The string "HostName"</span></span>
- <span data-ttu-id="5c862-536">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-537">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-537">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-538">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-539">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-540">Строка "Azure — Devices.</span><span class="sxs-lookup"><span data-stu-id="5c862-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-541">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-541">net"</span></span>
- <span data-ttu-id="5c862-542">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-543">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="5c862-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="5c862-544">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-545">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-545">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-546">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-547">Любая комбинация 43 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="5c862-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="5c862-548">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-549">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-549">Checksum</span></span>

<span data-ttu-id="5c862-550">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-551">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-551">Definition</span></span>

<span data-ttu-id="5c862-552">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-553">Регулярное выражение CEP_Regex_AzureIoTConnectionString находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-554">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-555">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-557">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-558">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-558">contoso</span></span>
- <span data-ttu-id="5c862-559">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-559">fabrikam</span></span>
- <span data-ttu-id="5c862-560">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-560">northwind</span></span>
- <span data-ttu-id="5c862-561">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-561">sandbox</span></span>
- <span data-ttu-id="5c862-562">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-562">onebox</span></span>
- <span data-ttu-id="5c862-563">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-563">localhost</span></span>
- <span data-ttu-id="5c862-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-564">127.0.0.1</span></span>
- <span data-ttu-id="5c862-565">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-566">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-566">com</span></span>
- <span data-ttu-id="5c862-567">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-568">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="5c862-569">Пароль для параметра публикации Azure</span><span class="sxs-lookup"><span data-stu-id="5c862-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="5c862-570">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-570">Format</span></span>

<span data-ttu-id="5c862-571">Строка "усерпвд =", за которой следует буквенно-цифровая строка.</span><span class="sxs-lookup"><span data-stu-id="5c862-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-572">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-572">Pattern</span></span>

- <span data-ttu-id="5c862-573">Строка "усерпвд ="</span><span class="sxs-lookup"><span data-stu-id="5c862-573">The string "userpwd="</span></span>
- <span data-ttu-id="5c862-574">Любая комбинация букв или цифр в нижнем регистре 60</span><span class="sxs-lookup"><span data-stu-id="5c862-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="5c862-575">Знак кавычек (")</span><span class="sxs-lookup"><span data-stu-id="5c862-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-576">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-576">Checksum</span></span>

<span data-ttu-id="5c862-577">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-578">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-578">Definition</span></span>

<span data-ttu-id="5c862-579">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-580">Регулярное выражение CEP_Regex_AzurePublishSettingPasswords находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-581">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="5c862-582">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-584">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-585">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-585">contoso</span></span>
- <span data-ttu-id="5c862-586">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-586">fabrikam</span></span>
- <span data-ttu-id="5c862-587">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-587">northwind</span></span>
- <span data-ttu-id="5c862-588">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-588">sandbox</span></span>
- <span data-ttu-id="5c862-589">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-589">onebox</span></span>
- <span data-ttu-id="5c862-590">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-590">localhost</span></span>
- <span data-ttu-id="5c862-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-591">127.0.0.1</span></span>
- <span data-ttu-id="5c862-592">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-593">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-593">com</span></span>
- <span data-ttu-id="5c862-594">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-595">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="5c862-596">Строка подключения к кэшу Azure Redis</span><span class="sxs-lookup"><span data-stu-id="5c862-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="5c862-597">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-597">Format</span></span>

<span data-ttu-id="5c862-598">Строка "Redis. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="5c862-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-599">NET, за которыми следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "Password" или "pwd".</span><span class="sxs-lookup"><span data-stu-id="5c862-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-600">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-600">Pattern</span></span>

- <span data-ttu-id="5c862-601">Строка "Redis. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="5c862-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-602">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-602">net"</span></span>
- <span data-ttu-id="5c862-603">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-604">Строка "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="5c862-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="5c862-605">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-606">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-606">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-607">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-608">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="5c862-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="5c862-609">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-610">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-610">Checksum</span></span>

<span data-ttu-id="5c862-611">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-612">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-612">Definition</span></span>

<span data-ttu-id="5c862-613">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-614">Регулярное выражение CEP_Regex_AzureRedisCacheConnectionString находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="5c862-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="5c862-615">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-616">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-618">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-619">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-619">contoso</span></span>
- <span data-ttu-id="5c862-620">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-620">fabrikam</span></span>
- <span data-ttu-id="5c862-621">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-621">northwind</span></span>
- <span data-ttu-id="5c862-622">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-622">sandbox</span></span>
- <span data-ttu-id="5c862-623">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-623">onebox</span></span>
- <span data-ttu-id="5c862-624">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-624">localhost</span></span>
- <span data-ttu-id="5c862-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-625">127.0.0.1</span></span>
- <span data-ttu-id="5c862-626">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-627">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-627">com</span></span>
- <span data-ttu-id="5c862-628">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-629">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="5c862-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="5c862-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="5c862-631">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-631">Format</span></span>

<span data-ttu-id="5c862-632">Строка "SIG", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="5c862-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-633">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-633">Pattern</span></span>

- <span data-ttu-id="5c862-634">Строка "SIG"</span><span class="sxs-lookup"><span data-stu-id="5c862-634">The string "sig"</span></span>
- <span data-ttu-id="5c862-635">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-636">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-636">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-637">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-638">Любое сочетание 43-53 символов, которые являются буквами нижнего или верхнего регистра, цифрами или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="5c862-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="5c862-639">Строка "% 3D"</span><span class="sxs-lookup"><span data-stu-id="5c862-639">The string "%3d"</span></span>
- <span data-ttu-id="5c862-640">Любой символ, который не является буквой нижнего или верхнего регистра, цифрой или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="5c862-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-641">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-641">Checksum</span></span>

<span data-ttu-id="5c862-642">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-643">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-643">Definition</span></span>

<span data-ttu-id="5c862-644">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-645">Регулярное выражение CEP_Regex_AzureSAS находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="5c862-646">Строка подключения к служебной шине Azure</span><span class="sxs-lookup"><span data-stu-id="5c862-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="5c862-647">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-647">Format</span></span>

<span data-ttu-id="5c862-648">Строка "EndPoint", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строки "сервицебус. Windows.</span><span class="sxs-lookup"><span data-stu-id="5c862-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-649">NET "и" Шаредакцескэй ".</span><span class="sxs-lookup"><span data-stu-id="5c862-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-650">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-650">Pattern</span></span>

- <span data-ttu-id="5c862-651">Строка "EndPoint"</span><span class="sxs-lookup"><span data-stu-id="5c862-651">The string "EndPoint"</span></span>
- <span data-ttu-id="5c862-652">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-653">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-653">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-654">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-655">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-656">Строка "сервицебус. Windows.</span><span class="sxs-lookup"><span data-stu-id="5c862-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-657">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-657">net"</span></span>
- <span data-ttu-id="5c862-658">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-659">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="5c862-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="5c862-660">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-661">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-661">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-662">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-663">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="5c862-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="5c862-664">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-665">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-665">Checksum</span></span>

<span data-ttu-id="5c862-666">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-667">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-667">Definition</span></span>

<span data-ttu-id="5c862-668">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-669">Регулярное выражение CEP_Regex_AzureServiceBusConnectionString находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="5c862-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="5c862-670">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-671">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-673">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-674">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-674">contoso</span></span>
- <span data-ttu-id="5c862-675">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-675">fabrikam</span></span>
- <span data-ttu-id="5c862-676">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-676">northwind</span></span>
- <span data-ttu-id="5c862-677">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-677">sandbox</span></span>
- <span data-ttu-id="5c862-678">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-678">onebox</span></span>
- <span data-ttu-id="5c862-679">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-679">localhost</span></span>
- <span data-ttu-id="5c862-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-680">127.0.0.1</span></span>
- <span data-ttu-id="5c862-681">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-682">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-682">com</span></span>
- <span data-ttu-id="5c862-683">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-684">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="5c862-685">Ключ учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="5c862-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="5c862-686">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-686">Format</span></span>

<span data-ttu-id="5c862-687">Строка "Дефаултендпоинтспротокол", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "AccountKey".</span><span class="sxs-lookup"><span data-stu-id="5c862-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-688">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-688">Pattern</span></span>

- <span data-ttu-id="5c862-689">Строка "Дефаултендпоинтспротокол"</span><span class="sxs-lookup"><span data-stu-id="5c862-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="5c862-690">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-691">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-691">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-692">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-693">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-694">Строка "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="5c862-694">The string "AccountKey"</span></span>
- <span data-ttu-id="5c862-695">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-696">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-696">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-697">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="5c862-698">Любое сочетание 86 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="5c862-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="5c862-699">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="5c862-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-700">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-700">Checksum</span></span>

<span data-ttu-id="5c862-701">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-702">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-702">Definition</span></span>

<span data-ttu-id="5c862-703">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-704">Регулярное выражение CEP_Regex_AzureStorageAccountKey находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-705">Регулярное выражение CEP_AzureEmulatorStorageAccountFilter не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-706">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-707">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="5c862-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="5c862-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="5c862-709">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/Кбхбексогмгв = =</span><span class="sxs-lookup"><span data-stu-id="5c862-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-712">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-713">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-713">contoso</span></span>
- <span data-ttu-id="5c862-714">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-714">fabrikam</span></span>
- <span data-ttu-id="5c862-715">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-715">northwind</span></span>
- <span data-ttu-id="5c862-716">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-716">sandbox</span></span>
- <span data-ttu-id="5c862-717">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-717">onebox</span></span>
- <span data-ttu-id="5c862-718">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-718">localhost</span></span>
- <span data-ttu-id="5c862-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-719">127.0.0.1</span></span>
- <span data-ttu-id="5c862-720">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-721">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-721">com</span></span>
- <span data-ttu-id="5c862-722">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-723">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="5c862-724">Ключ учетной записи хранилища Azure (общий)</span><span class="sxs-lookup"><span data-stu-id="5c862-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-725">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-725">Format</span></span>

<span data-ttu-id="5c862-726">Любая комбинация 86 строчных или прописных букв, цифр, знаков косой черты (/) или знака плюса (+) перед или за ними следуют символы, указанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="5c862-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-727">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-727">Pattern</span></span>

- <span data-ttu-id="5c862-728">0-1 из символа "больше" (>), апостроф ('), знак равенства (=), знак кавычек (") или решетка (#)</span><span class="sxs-lookup"><span data-stu-id="5c862-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="5c862-729">Любое сочетание 86 символов, которые представляют собой буквы в нижнем или верхнем регистре, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="5c862-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="5c862-730">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="5c862-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="5c862-731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-731">Checksum</span></span>

<span data-ttu-id="5c862-732">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-733">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-733">Definition</span></span>

<span data-ttu-id="5c862-734">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-735">Регулярное выражение CEP_Regex_AzureStorageAccountKeyGeneric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="5c862-736">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="5c862-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-737">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-737">Format</span></span>

<span data-ttu-id="5c862-738">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="5c862-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-739">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-739">Pattern</span></span>

<span data-ttu-id="5c862-740">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="5c862-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="5c862-741">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="5c862-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="5c862-742">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-742">A hyphen</span></span> 
- <span data-ttu-id="5c862-743">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="5c862-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="5c862-744">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-744">A period</span></span> 
- <span data-ttu-id="5c862-745">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-746">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-746">Checksum</span></span>

<span data-ttu-id="5c862-747">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-748">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-748">Definition</span></span>

<span data-ttu-id="5c862-749">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-750">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-751">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="5c862-752">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-752">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-753">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="5c862-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="5c862-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="5c862-755">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="5c862-755">Identity</span></span>
- <span data-ttu-id="5c862-756">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="5c862-756">Registration</span></span>
- <span data-ttu-id="5c862-757">Процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-757">Identification</span></span> 
- <span data-ttu-id="5c862-758">ID</span><span class="sxs-lookup"><span data-stu-id="5c862-758">ID</span></span> 
- <span data-ttu-id="5c862-759">идентитеитскаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-759">Identiteitskaart</span></span>
- <span data-ttu-id="5c862-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="5c862-760">Registratie nummer</span></span> 
- <span data-ttu-id="5c862-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="5c862-761">Identificatie nummer</span></span> 
- <span data-ttu-id="5c862-762">идентитеит</span><span class="sxs-lookup"><span data-stu-id="5c862-762">Identiteit</span></span>
- <span data-ttu-id="5c862-763">регистратие</span><span class="sxs-lookup"><span data-stu-id="5c862-763">Registratie</span></span>
- <span data-ttu-id="5c862-764">идентификатие</span><span class="sxs-lookup"><span data-stu-id="5c862-764">Identificatie</span></span> 
- <span data-ttu-id="5c862-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="5c862-765">Carte d’identité</span></span> 
- <span data-ttu-id="5c862-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="5c862-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="5c862-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="5c862-767">numéro d'identification</span></span>
- <span data-ttu-id="5c862-768">идентитé</span><span class="sxs-lookup"><span data-stu-id="5c862-768">identité</span></span> 
- <span data-ttu-id="5c862-769">инскриптион</span><span class="sxs-lookup"><span data-stu-id="5c862-769">inscription</span></span> 
- <span data-ttu-id="5c862-770">идентификатион</span><span class="sxs-lookup"><span data-stu-id="5c862-770">Identifikation</span></span>
- <span data-ttu-id="5c862-771">идентифизиерунг</span><span class="sxs-lookup"><span data-stu-id="5c862-771">Identifizierung</span></span>
- <span data-ttu-id="5c862-772">идентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-772">Identifikationsnummer</span></span>
- <span data-ttu-id="5c862-773">персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="5c862-773">Personalausweis</span></span>
- <span data-ttu-id="5c862-774">регистриерунг</span><span class="sxs-lookup"><span data-stu-id="5c862-774">Registrierung</span></span>
- <span data-ttu-id="5c862-775">регистратионснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="5c862-776">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="5c862-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-777">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-777">Format</span></span>

<span data-ttu-id="5c862-778">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="5c862-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-779">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-779">Pattern</span></span>

<span data-ttu-id="5c862-780">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="5c862-780">Formatted:</span></span>
- <span data-ttu-id="5c862-781">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-781">Three digits</span></span> 
- <span data-ttu-id="5c862-782">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-782">A period</span></span> 
- <span data-ttu-id="5c862-783">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-783">Three digits</span></span> 
- <span data-ttu-id="5c862-784">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-784">A period</span></span> 
- <span data-ttu-id="5c862-785">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-785">Three digits</span></span> 
- <span data-ttu-id="5c862-786">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-786">A hyphen</span></span> 
- <span data-ttu-id="5c862-787">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-787">Two digits which are check digits</span></span>

<span data-ttu-id="5c862-788">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="5c862-788">Unformatted:</span></span>
- <span data-ttu-id="5c862-789">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="5c862-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-790">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-790">Checksum</span></span>

<span data-ttu-id="5c862-791">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-792">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-792">Definition</span></span>

<span data-ttu-id="5c862-793">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-794">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-795">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="5c862-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="5c862-796">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-796">The checksum passes.</span></span>

<span data-ttu-id="5c862-797">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-798">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-799">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-799">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-800">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="5c862-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="5c862-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="5c862-802">CPF</span><span class="sxs-lookup"><span data-stu-id="5c862-802">CPF</span></span>
- <span data-ttu-id="5c862-803">Процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-803">Identification</span></span>
- <span data-ttu-id="5c862-804">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="5c862-804">Registration</span></span>
- <span data-ttu-id="5c862-805">Реализации</span><span class="sxs-lookup"><span data-stu-id="5c862-805">Revenue</span></span>
- <span data-ttu-id="5c862-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="5c862-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="5c862-807">импосто</span><span class="sxs-lookup"><span data-stu-id="5c862-807">Imposto</span></span> 
- <span data-ttu-id="5c862-808">идентификаçãо</span><span class="sxs-lookup"><span data-stu-id="5c862-808">Identificação</span></span> 
- <span data-ttu-id="5c862-809">инскриçãо</span><span class="sxs-lookup"><span data-stu-id="5c862-809">Inscrição</span></span> 
- <span data-ttu-id="5c862-810">рецеита</span><span class="sxs-lookup"><span data-stu-id="5c862-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="5c862-811">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="5c862-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-812">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-812">Format</span></span>

<span data-ttu-id="5c862-813">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="5c862-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-814">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-814">Pattern</span></span>
<span data-ttu-id="5c862-815">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="5c862-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="5c862-816">две цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-816">Two digits</span></span> 
- <span data-ttu-id="5c862-817">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-817">A period</span></span> 
- <span data-ttu-id="5c862-818">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-818">Three digits</span></span> 
- <span data-ttu-id="5c862-819">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-819">A period</span></span> 
- <span data-ttu-id="5c862-820">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="5c862-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="5c862-821">косая черта;</span><span class="sxs-lookup"><span data-stu-id="5c862-821">A forward slash</span></span> 
- <span data-ttu-id="5c862-822">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-822">Four-digit branch number</span></span> 
- <span data-ttu-id="5c862-823">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-823">A hyphen</span></span> 
- <span data-ttu-id="5c862-824">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-825">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-825">Checksum</span></span>

<span data-ttu-id="5c862-826">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-827">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-827">Definition</span></span>

<span data-ttu-id="5c862-828">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-829">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-830">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="5c862-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="5c862-831">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-831">The checksum passes.</span></span>

<span data-ttu-id="5c862-832">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-833">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-834">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-834">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-835">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="5c862-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="5c862-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="5c862-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="5c862-837">CNPJ</span></span> 
- <span data-ttu-id="5c862-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="5c862-838">CNPJ/MF</span></span> 
- <span data-ttu-id="5c862-839">CNPJ – MF</span><span class="sxs-lookup"><span data-stu-id="5c862-839">CNPJ-MF</span></span> 
- <span data-ttu-id="5c862-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="5c862-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="5c862-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="5c862-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="5c862-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="5c862-842">Legal entity</span></span> 
- <span data-ttu-id="5c862-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="5c862-843">Legal entities</span></span> 
- <span data-ttu-id="5c862-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="5c862-844">Registration Status</span></span> 
- <span data-ttu-id="5c862-845">Бизнес</span><span class="sxs-lookup"><span data-stu-id="5c862-845">Business</span></span> 
- <span data-ttu-id="5c862-846">Company</span><span class="sxs-lookup"><span data-stu-id="5c862-846">Company</span></span>
- <span data-ttu-id="5c862-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="5c862-847">CNPJ</span></span> 
- <span data-ttu-id="5c862-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="5c862-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="5c862-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="5c862-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="5c862-850">кгк</span><span class="sxs-lookup"><span data-stu-id="5c862-850">CGC</span></span> 
- <span data-ttu-id="5c862-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="5c862-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="5c862-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="5c862-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="5c862-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="5c862-853">Situação cadastral</span></span> 
- <span data-ttu-id="5c862-854">инскриçãо</span><span class="sxs-lookup"><span data-stu-id="5c862-854">Inscrição</span></span> 
- <span data-ttu-id="5c862-855">емпреса</span><span class="sxs-lookup"><span data-stu-id="5c862-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="5c862-856">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="5c862-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-857">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-857">Format</span></span>

<span data-ttu-id="5c862-858">Registro Geral (старый формат): девять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="5c862-859">Registro de identidade (RIC) (новый формат): 11 цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-860">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-860">Pattern</span></span>

<span data-ttu-id="5c862-861">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="5c862-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="5c862-862">две цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-862">Two digits</span></span> 
- <span data-ttu-id="5c862-863">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-863">A period</span></span> 
- <span data-ttu-id="5c862-864">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-864">Three digits</span></span> 
- <span data-ttu-id="5c862-865">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-865">A period</span></span> 
- <span data-ttu-id="5c862-866">три цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-866">Three digits</span></span> 
- <span data-ttu-id="5c862-867">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-867">A hyphen</span></span> 
- <span data-ttu-id="5c862-868">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-868">One digit which is a check digit</span></span>

<span data-ttu-id="5c862-869">Registro de identidade (RIC) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="5c862-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="5c862-870">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-870">10 digits</span></span> 
- <span data-ttu-id="5c862-871">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-871">A hyphen</span></span> 
- <span data-ttu-id="5c862-872">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-873">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-873">Checksum</span></span>

<span data-ttu-id="5c862-874">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-875">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-875">Definition</span></span>

<span data-ttu-id="5c862-876">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-877">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-878">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="5c862-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="5c862-879">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-879">The checksum passes.</span></span>

<span data-ttu-id="5c862-880">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-881">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-882">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-882">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-883">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="5c862-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="5c862-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="5c862-885">Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр).</span><span class="sxs-lookup"><span data-stu-id="5c862-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="5c862-886">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="5c862-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-887">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-887">Format</span></span>

<span data-ttu-id="5c862-888">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-889">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-889">Pattern</span></span>

<span data-ttu-id="5c862-890">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="5c862-891">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="5c862-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="5c862-892">пять цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-892">Five digits</span></span> 
- <span data-ttu-id="5c862-893">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-893">A hyphen</span></span> 
- <span data-ttu-id="5c862-894">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="5c862-894">Three digits OR</span></span>
- <span data-ttu-id="5c862-895">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="5c862-895">A zero "0"</span></span> 
- <span data-ttu-id="5c862-896">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-897">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-897">Checksum</span></span>

<span data-ttu-id="5c862-898">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-899">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-899">Definition</span></span>

<span data-ttu-id="5c862-900">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-901">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-902">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="5c862-903">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="5c862-904">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-905">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-906">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-907">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="5c862-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="5c862-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="5c862-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="5c862-909">canada savings bonds</span></span>
- <span data-ttu-id="5c862-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="5c862-910">canada revenue agency</span></span>
- <span data-ttu-id="5c862-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="5c862-911">canadian financial institution</span></span>
- <span data-ttu-id="5c862-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="5c862-912">direct deposit form</span></span>
- <span data-ttu-id="5c862-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="5c862-913">canadian citizen</span></span>
- <span data-ttu-id="5c862-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="5c862-914">legal representative</span></span>
- <span data-ttu-id="5c862-915">notary public</span><span class="sxs-lookup"><span data-stu-id="5c862-915">notary public</span></span>
- <span data-ttu-id="5c862-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="5c862-916">commissioner for oaths</span></span>
- <span data-ttu-id="5c862-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="5c862-917">child care benefit</span></span>
- <span data-ttu-id="5c862-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="5c862-918">universal child care</span></span>
- <span data-ttu-id="5c862-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="5c862-919">canada child tax benefit</span></span>
- <span data-ttu-id="5c862-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="5c862-920">income tax benefit</span></span>
- <span data-ttu-id="5c862-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="5c862-921">harmonized sales tax</span></span>
- <span data-ttu-id="5c862-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="5c862-922">social insurance number</span></span>
- <span data-ttu-id="5c862-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="5c862-923">income tax refund</span></span>
- <span data-ttu-id="5c862-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="5c862-924">child tax benefit</span></span>
- <span data-ttu-id="5c862-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="5c862-925">territorial payments</span></span>
- <span data-ttu-id="5c862-926">institution number</span><span class="sxs-lookup"><span data-stu-id="5c862-926">institution number</span></span>
- <span data-ttu-id="5c862-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="5c862-927">deposit request</span></span>
- <span data-ttu-id="5c862-928">banking information</span><span class="sxs-lookup"><span data-stu-id="5c862-928">banking information</span></span>
- <span data-ttu-id="5c862-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="5c862-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="5c862-930">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="5c862-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-931">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-931">Format</span></span>

<span data-ttu-id="5c862-932">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="5c862-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-933">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-933">Pattern</span></span>

<span data-ttu-id="5c862-934">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="5c862-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-935">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-935">Checksum</span></span>

<span data-ttu-id="5c862-936">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-937">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-937">Definition</span></span>

<span data-ttu-id="5c862-938">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-939">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-940">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="5c862-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="5c862-941">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="5c862-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-942">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="5c862-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="5c862-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="5c862-944">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="5c862-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="5c862-945">Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="5c862-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="5c862-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="5c862-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="5c862-947">DL</span><span class="sxs-lookup"><span data-stu-id="5c862-947">DL</span></span>
- <span data-ttu-id="5c862-948">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="5c862-948">DLS</span></span>
- <span data-ttu-id="5c862-949">кдл</span><span class="sxs-lookup"><span data-stu-id="5c862-949">CDL</span></span>
- <span data-ttu-id="5c862-950">кдлс</span><span class="sxs-lookup"><span data-stu-id="5c862-950">CDLS</span></span>
- <span data-ttu-id="5c862-951">дриверлик</span><span class="sxs-lookup"><span data-stu-id="5c862-951">DriverLic</span></span>
- <span data-ttu-id="5c862-952">дриверликс</span><span class="sxs-lookup"><span data-stu-id="5c862-952">DriverLics</span></span>
- <span data-ttu-id="5c862-953">дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-953">DriverLicense</span></span>
- <span data-ttu-id="5c862-954">дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-954">DriverLicenses</span></span>
- <span data-ttu-id="5c862-955">дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="5c862-955">DriverLicence</span></span>
- <span data-ttu-id="5c862-956">дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="5c862-956">DriverLicences</span></span>
- <span data-ttu-id="5c862-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-957">Driver Lic</span></span>
- <span data-ttu-id="5c862-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-958">Driver Lics</span></span>
- <span data-ttu-id="5c862-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="5c862-959">Driver License</span></span>
- <span data-ttu-id="5c862-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-960">Driver Licenses</span></span>
- <span data-ttu-id="5c862-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-961">Driver Licence</span></span>
- <span data-ttu-id="5c862-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-962">Driver Licences</span></span>
- <span data-ttu-id="5c862-963">дриверслик</span><span class="sxs-lookup"><span data-stu-id="5c862-963">DriversLic</span></span>
- <span data-ttu-id="5c862-964">дриверсликс</span><span class="sxs-lookup"><span data-stu-id="5c862-964">DriversLics</span></span>
- <span data-ttu-id="5c862-965">дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="5c862-965">DriversLicence</span></span>
- <span data-ttu-id="5c862-966">дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="5c862-966">DriversLicences</span></span>
- <span data-ttu-id="5c862-967">дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-967">DriversLicense</span></span>
- <span data-ttu-id="5c862-968">дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-968">DriversLicenses</span></span>
- <span data-ttu-id="5c862-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-969">Drivers Lic</span></span>
- <span data-ttu-id="5c862-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-970">Drivers Lics</span></span>
- <span data-ttu-id="5c862-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="5c862-971">Drivers License</span></span>
- <span data-ttu-id="5c862-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-972">Drivers Licenses</span></span>
- <span data-ttu-id="5c862-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-973">Drivers Licence</span></span>
- <span data-ttu-id="5c862-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-974">Drivers Licences</span></span>
- <span data-ttu-id="5c862-975">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="5c862-975">Driver'Lic</span></span>
- <span data-ttu-id="5c862-976">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="5c862-976">Driver'Lics</span></span>
- <span data-ttu-id="5c862-977">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="5c862-977">Driver'License</span></span>
- <span data-ttu-id="5c862-978">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-978">Driver'Licenses</span></span>
- <span data-ttu-id="5c862-979">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-979">Driver'Licence</span></span>
- <span data-ttu-id="5c862-980">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-980">Driver'Licences</span></span>
- <span data-ttu-id="5c862-981">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-981">Driver' Lic</span></span>
- <span data-ttu-id="5c862-982">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-982">Driver' Lics</span></span>
- <span data-ttu-id="5c862-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="5c862-983">Driver' License</span></span>
- <span data-ttu-id="5c862-984">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-984">Driver' Licenses</span></span>
- <span data-ttu-id="5c862-985">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-985">Driver' Licence</span></span>
- <span data-ttu-id="5c862-986">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-986">Driver' Licences</span></span>
- <span data-ttu-id="5c862-987">дривер'слик</span><span class="sxs-lookup"><span data-stu-id="5c862-987">Driver'sLic</span></span>
- <span data-ttu-id="5c862-988">дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="5c862-988">Driver'sLics</span></span>
- <span data-ttu-id="5c862-989">дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-989">Driver'sLicense</span></span>
- <span data-ttu-id="5c862-990">дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-990">Driver'sLicenses</span></span>
- <span data-ttu-id="5c862-991">дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="5c862-991">Driver'sLicence</span></span>
- <span data-ttu-id="5c862-992">дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="5c862-992">Driver'sLicences</span></span>
- <span data-ttu-id="5c862-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-993">Driver's Lic</span></span>
- <span data-ttu-id="5c862-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-994">Driver's Lics</span></span>
- <span data-ttu-id="5c862-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="5c862-995">Driver's License</span></span>
- <span data-ttu-id="5c862-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-996">Driver's Licenses</span></span>
- <span data-ttu-id="5c862-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-997">Driver's Licence</span></span>
- <span data-ttu-id="5c862-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-998">Driver's Licences</span></span>
- <span data-ttu-id="5c862-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="5c862-999">Permis de Conduire</span></span>
- <span data-ttu-id="5c862-1000">id</span><span class="sxs-lookup"><span data-stu-id="5c862-1000">id</span></span>
- <span data-ttu-id="5c862-1001">ids</span><span class="sxs-lookup"><span data-stu-id="5c862-1001">ids</span></span>
- <span data-ttu-id="5c862-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="5c862-1002">idcard number</span></span>
- <span data-ttu-id="5c862-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-1003">idcard numbers</span></span>
- <span data-ttu-id="5c862-1004">idcard#</span><span class="sxs-lookup"><span data-stu-id="5c862-1004">idcard #</span></span>
- <span data-ttu-id="5c862-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="5c862-1005">idcard #s</span></span>
- <span data-ttu-id="5c862-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="5c862-1006">idcard card</span></span>
- <span data-ttu-id="5c862-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1007">idcard cards</span></span>
- <span data-ttu-id="5c862-1008">идкард</span><span class="sxs-lookup"><span data-stu-id="5c862-1008">idcard</span></span>
- <span data-ttu-id="5c862-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-1009">identification number</span></span>
- <span data-ttu-id="5c862-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-1010">identification numbers</span></span>
- <span data-ttu-id="5c862-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="5c862-1011">identification #</span></span>
- <span data-ttu-id="5c862-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="5c862-1012">identification #s</span></span>
- <span data-ttu-id="5c862-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="5c862-1013">identification card</span></span>
- <span data-ttu-id="5c862-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1014">identification cards</span></span>
- <span data-ttu-id="5c862-1015">процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-1015">identification</span></span> 
- <span data-ttu-id="5c862-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="5c862-1016">DL#</span></span>
- <span data-ttu-id="5c862-1017">БИБЛИОТЕК #</span><span class="sxs-lookup"><span data-stu-id="5c862-1017">DLS#</span></span> 
- <span data-ttu-id="5c862-1018">кдл #</span><span class="sxs-lookup"><span data-stu-id="5c862-1018">CDL#</span></span> 
- <span data-ttu-id="5c862-1019">кдлс #</span><span class="sxs-lookup"><span data-stu-id="5c862-1019">CDLS#</span></span> 
- <span data-ttu-id="5c862-1020">дриверлик #</span><span class="sxs-lookup"><span data-stu-id="5c862-1020">DriverLic#</span></span> 
- <span data-ttu-id="5c862-1021">дриверликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-1021">DriverLics#</span></span> 
- <span data-ttu-id="5c862-1022">дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-1022">DriverLicense#</span></span> 
- <span data-ttu-id="5c862-1023">дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="5c862-1024">дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="5c862-1024">DriverLicence#</span></span> 
- <span data-ttu-id="5c862-1025">дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="5c862-1025">DriverLicences#</span></span> 
- <span data-ttu-id="5c862-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-1026">Driver Lic#</span></span>
- <span data-ttu-id="5c862-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-1027">Driver Lics#</span></span> 
- <span data-ttu-id="5c862-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="5c862-1028">Driver License#</span></span> 
- <span data-ttu-id="5c862-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="5c862-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="5c862-1030">Driver License#</span></span> 
- <span data-ttu-id="5c862-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-1031">Driver Licences#</span></span> 
- <span data-ttu-id="5c862-1032">дриверслик #</span><span class="sxs-lookup"><span data-stu-id="5c862-1032">DriversLic#</span></span> 
- <span data-ttu-id="5c862-1033">дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-1033">DriversLics#</span></span> 
- <span data-ttu-id="5c862-1034">дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-1034">DriversLicense#</span></span> 
- <span data-ttu-id="5c862-1035">дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="5c862-1036">дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="5c862-1036">DriversLicence#</span></span> 
- <span data-ttu-id="5c862-1037">дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="5c862-1037">DriversLicences#</span></span> 
- <span data-ttu-id="5c862-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="5c862-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="5c862-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="5c862-1040">Drivers License#</span></span> 
- <span data-ttu-id="5c862-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="5c862-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="5c862-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="5c862-1044">Driver ' LIC #</span><span class="sxs-lookup"><span data-stu-id="5c862-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="5c862-1045">Driver ' LICS #</span><span class="sxs-lookup"><span data-stu-id="5c862-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="5c862-1046">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="5c862-1046">Driver'License#</span></span> 
- <span data-ttu-id="5c862-1047">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="5c862-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="5c862-1048">Driver ' Licence #</span><span class="sxs-lookup"><span data-stu-id="5c862-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="5c862-1049">Driver ' Licences #</span><span class="sxs-lookup"><span data-stu-id="5c862-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="5c862-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="5c862-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="5c862-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="5c862-1052">Driver' License#</span></span> 
- <span data-ttu-id="5c862-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="5c862-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="5c862-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="5c862-1056">дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="5c862-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="5c862-1057">дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="5c862-1058">дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="5c862-1059">дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="5c862-1060">дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="5c862-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="5c862-1061">дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="5c862-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="5c862-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="5c862-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="5c862-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="5c862-1064">Driver's License#</span></span> 
- <span data-ttu-id="5c862-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="5c862-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="5c862-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="5c862-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="5c862-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="5c862-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="5c862-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="5c862-1069">кодов #</span><span class="sxs-lookup"><span data-stu-id="5c862-1069">id#</span></span> 
- <span data-ttu-id="5c862-1070">идентификаторы #</span><span class="sxs-lookup"><span data-stu-id="5c862-1070">ids#</span></span> 
- <span data-ttu-id="5c862-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="5c862-1071">idcard card#</span></span> 
- <span data-ttu-id="5c862-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="5c862-1072">idcard cards#</span></span> 
- <span data-ttu-id="5c862-1073">идкард #</span><span class="sxs-lookup"><span data-stu-id="5c862-1073">idcard#</span></span> 
- <span data-ttu-id="5c862-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="5c862-1074">identification card#</span></span> 
- <span data-ttu-id="5c862-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="5c862-1075">identification cards#</span></span> 
- <span data-ttu-id="5c862-1076">процедура #</span><span class="sxs-lookup"><span data-stu-id="5c862-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="5c862-1077">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="5c862-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1078">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1078">Format</span></span>

<span data-ttu-id="5c862-1079">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1080">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1080">Pattern</span></span>

<span data-ttu-id="5c862-1081">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1082">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1082">Checksum</span></span>

<span data-ttu-id="5c862-1083">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1084">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1084">Definition</span></span>

<span data-ttu-id="5c862-1085">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1086">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1087">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1088">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="5c862-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="5c862-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="5c862-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="5c862-1090">personal health number</span></span>
- <span data-ttu-id="5c862-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="5c862-1091">patient information</span></span>
- <span data-ttu-id="5c862-1092">health services</span><span class="sxs-lookup"><span data-stu-id="5c862-1092">health services</span></span>
- <span data-ttu-id="5c862-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="5c862-1093">speciality services</span></span>
- <span data-ttu-id="5c862-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="5c862-1094">automobile accident</span></span>
- <span data-ttu-id="5c862-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="5c862-1095">patient hospital</span></span>
- <span data-ttu-id="5c862-1096">псичиатрист</span><span class="sxs-lookup"><span data-stu-id="5c862-1096">psychiatrist</span></span>
- <span data-ttu-id="5c862-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="5c862-1097">workers compensation</span></span>
- <span data-ttu-id="5c862-1098">ограничен</span><span class="sxs-lookup"><span data-stu-id="5c862-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="5c862-1099">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="5c862-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1100">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1100">Format</span></span>

<span data-ttu-id="5c862-1101">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1102">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1102">Pattern</span></span>

<span data-ttu-id="5c862-1103">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1104">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1104">Checksum</span></span>

<span data-ttu-id="5c862-1105">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1106">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1106">Definition</span></span>

<span data-ttu-id="5c862-1107">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1108">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1109">Найдено ключевое слово из Keyword_canada_passport_number или Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="5c862-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1110">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="5c862-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="5c862-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="5c862-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="5c862-1112">canadian citizenship</span></span>
- <span data-ttu-id="5c862-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="5c862-1113">canadian passport</span></span>
- <span data-ttu-id="5c862-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="5c862-1114">passport application</span></span>
- <span data-ttu-id="5c862-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="5c862-1115">passport photos</span></span>
- <span data-ttu-id="5c862-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="5c862-1116">certified translator</span></span>
- <span data-ttu-id="5c862-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="5c862-1117">canadian citizens</span></span>
- <span data-ttu-id="5c862-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="5c862-1118">processing times</span></span>
- <span data-ttu-id="5c862-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="5c862-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="5c862-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-1120">Keyword_passport</span></span>

- <span data-ttu-id="5c862-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="5c862-1121">Passport Number</span></span>
- <span data-ttu-id="5c862-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="5c862-1122">Passport No</span></span>
- <span data-ttu-id="5c862-1123">Passport#</span><span class="sxs-lookup"><span data-stu-id="5c862-1123">Passport #</span></span>
- <span data-ttu-id="5c862-1124">Службу #</span><span class="sxs-lookup"><span data-stu-id="5c862-1124">Passport#</span></span>
- <span data-ttu-id="5c862-1125">пасспортид</span><span class="sxs-lookup"><span data-stu-id="5c862-1125">PassportID</span></span>
- <span data-ttu-id="5c862-1126">пасспортно</span><span class="sxs-lookup"><span data-stu-id="5c862-1126">Passportno</span></span>
- <span data-ttu-id="5c862-1127">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-1127">passportnumber</span></span>
- <span data-ttu-id="5c862-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="5c862-1128">パスポート</span></span>
- <span data-ttu-id="5c862-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="5c862-1129">パスポート番号</span></span>
- <span data-ttu-id="5c862-1130">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="5c862-1130">パスポートのNum</span></span>
- <span data-ttu-id="5c862-1131">パスポート #</span><span class="sxs-lookup"><span data-stu-id="5c862-1131">パスポート＃</span></span>
- <span data-ttu-id="5c862-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="5c862-1132">Numéro de passeport</span></span>
- <span data-ttu-id="5c862-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="5c862-1133">Passeport n °</span></span>
- <span data-ttu-id="5c862-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="5c862-1134">Passeport Non</span></span>
- <span data-ttu-id="5c862-1135">Passeport#</span><span class="sxs-lookup"><span data-stu-id="5c862-1135">Passeport #</span></span>
- <span data-ttu-id="5c862-1136">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="5c862-1136">Passeport#</span></span>
- <span data-ttu-id="5c862-1137">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="5c862-1137">PasseportNon</span></span>
- <span data-ttu-id="5c862-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="5c862-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="5c862-1139">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="5c862-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1140">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1140">Format</span></span>

<span data-ttu-id="5c862-1141">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1142">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1142">Pattern</span></span>

<span data-ttu-id="5c862-1143">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1144">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1144">Checksum</span></span>

<span data-ttu-id="5c862-1145">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1146">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1146">Definition</span></span>

<span data-ttu-id="5c862-1147">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Regex_canada_phin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-1148">Найдены по крайней мере два ключевых слова от Keyword_canada_phin или Keyword_canada_provinces.</span><span class="sxs-lookup"><span data-stu-id="5c862-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1149">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="5c862-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="5c862-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="5c862-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="5c862-1151">social insurance number</span></span>
- <span data-ttu-id="5c862-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="5c862-1152">health information act</span></span>
- <span data-ttu-id="5c862-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="5c862-1153">income tax information</span></span>
- <span data-ttu-id="5c862-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="5c862-1154">manitoba health</span></span>
- <span data-ttu-id="5c862-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="5c862-1155">health registration</span></span>
- <span data-ttu-id="5c862-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="5c862-1156">prescription purchases</span></span>
- <span data-ttu-id="5c862-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="5c862-1157">benefit eligibility</span></span>
- <span data-ttu-id="5c862-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="5c862-1158">personal health</span></span>
- <span data-ttu-id="5c862-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="5c862-1159">power of attorney</span></span>
- <span data-ttu-id="5c862-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="5c862-1160">registration number</span></span>
- <span data-ttu-id="5c862-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="5c862-1161">personal health number</span></span>
- <span data-ttu-id="5c862-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="5c862-1162">practitioner referral</span></span>
- <span data-ttu-id="5c862-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="5c862-1163">wellness professional</span></span>
- <span data-ttu-id="5c862-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="5c862-1164">patient referral</span></span>
- <span data-ttu-id="5c862-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="5c862-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="5c862-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="5c862-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="5c862-1167">нунавут</span><span class="sxs-lookup"><span data-stu-id="5c862-1167">Nunavut</span></span>
- <span data-ttu-id="5c862-1168">Квебека</span><span class="sxs-lookup"><span data-stu-id="5c862-1168">Quebec</span></span>
- <span data-ttu-id="5c862-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="5c862-1169">Northwest Territories</span></span>
- <span data-ttu-id="5c862-1170">Онтарио</span><span class="sxs-lookup"><span data-stu-id="5c862-1170">Ontario</span></span>
- <span data-ttu-id="5c862-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="5c862-1171">British Columbia</span></span>
- <span data-ttu-id="5c862-1172">Альберта</span><span class="sxs-lookup"><span data-stu-id="5c862-1172">Alberta</span></span>
- <span data-ttu-id="5c862-1173">Саскачеван</span><span class="sxs-lookup"><span data-stu-id="5c862-1173">Saskatchewan</span></span>
- <span data-ttu-id="5c862-1174">Манитоба</span><span class="sxs-lookup"><span data-stu-id="5c862-1174">Manitoba</span></span>
- <span data-ttu-id="5c862-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="5c862-1175">Yukon</span></span>
- <span data-ttu-id="5c862-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="5c862-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="5c862-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="5c862-1177">New Brunswick</span></span>
- <span data-ttu-id="5c862-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="5c862-1178">Nova Scotia</span></span>
- <span data-ttu-id="5c862-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="5c862-1179">Prince Edward Island</span></span>
- <span data-ttu-id="5c862-1180">Канада</span><span class="sxs-lookup"><span data-stu-id="5c862-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="5c862-1181">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="5c862-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1182">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1182">Format</span></span>

<span data-ttu-id="5c862-1183">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="5c862-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1184">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1184">Pattern</span></span>

<span data-ttu-id="5c862-1185">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="5c862-1185">Formatted:</span></span>
- <span data-ttu-id="5c862-1186">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-1186">Three digits</span></span> 
- <span data-ttu-id="5c862-1187">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-1187">A hyphen or space</span></span> 
- <span data-ttu-id="5c862-1188">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-1188">Three digits</span></span> 
- <span data-ttu-id="5c862-1189">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-1189">A hyphen or space</span></span> 
- <span data-ttu-id="5c862-1190">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-1190">Three digits</span></span>

<span data-ttu-id="5c862-1191">Неформатированные: девять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1192">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1192">Checksum</span></span>

<span data-ttu-id="5c862-1193">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1194">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1194">Definition</span></span>

<span data-ttu-id="5c862-1195">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1196">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1197">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="5c862-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="5c862-1198">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="5c862-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="5c862-1199">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="5c862-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="5c862-1200">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="5c862-1201">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1201">The checksum passes.</span></span>

<span data-ttu-id="5c862-1202">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1203">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1204">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="5c862-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="5c862-1205">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1205">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1206">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="5c862-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="5c862-1207">Keyword_sin</span></span>

- <span data-ttu-id="5c862-1208">sin</span><span class="sxs-lookup"><span data-stu-id="5c862-1208">sin</span></span> 
- <span data-ttu-id="5c862-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="5c862-1209">social insurance</span></span> 
- <span data-ttu-id="5c862-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="5c862-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="5c862-1211">грехов</span><span class="sxs-lookup"><span data-stu-id="5c862-1211">sins</span></span> 
- <span data-ttu-id="5c862-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="5c862-1212">ssn</span></span> 
- <span data-ttu-id="5c862-1213">ssNS</span><span class="sxs-lookup"><span data-stu-id="5c862-1213">ssns</span></span> 
- <span data-ttu-id="5c862-1214">social security</span><span class="sxs-lookup"><span data-stu-id="5c862-1214">social security</span></span> 
- <span data-ttu-id="5c862-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="5c862-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="5c862-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-1216">national identification number</span></span> 
- <span data-ttu-id="5c862-1217">national id</span><span class="sxs-lookup"><span data-stu-id="5c862-1217">national id</span></span> 
- <span data-ttu-id="5c862-1218">Синус #</span><span class="sxs-lookup"><span data-stu-id="5c862-1218">sin#</span></span> 
- <span data-ttu-id="5c862-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="5c862-1219">soc ins</span></span> 
- <span data-ttu-id="5c862-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="5c862-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="5c862-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="5c862-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="5c862-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="5c862-1222">driver's license</span></span> 
- <span data-ttu-id="5c862-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="5c862-1223">drivers license</span></span> 
- <span data-ttu-id="5c862-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="5c862-1224">driver's licence</span></span> 
- <span data-ttu-id="5c862-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="5c862-1225">drivers licence</span></span> 
- <span data-ttu-id="5c862-1226">доб</span><span class="sxs-lookup"><span data-stu-id="5c862-1226">DOB</span></span> 
- <span data-ttu-id="5c862-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="5c862-1227">Birthdate</span></span> 
- <span data-ttu-id="5c862-1228">День рождения </span><span class="sxs-lookup"><span data-stu-id="5c862-1228">Birthday</span></span> 
- <span data-ttu-id="5c862-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="5c862-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="5c862-1230">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="5c862-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1231">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1231">Format</span></span>

<span data-ttu-id="5c862-1232">7-8 цифр и разделители — контрольная цифра или буква</span><span class="sxs-lookup"><span data-stu-id="5c862-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1233">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1233">Pattern</span></span>

<span data-ttu-id="5c862-1234">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="5c862-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="5c862-1235">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-1235">1-2 digits</span></span> 
- <span data-ttu-id="5c862-1236">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-1236">A period</span></span> 
- <span data-ttu-id="5c862-1237">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-1237">Three digits</span></span> 
- <span data-ttu-id="5c862-1238">точка;</span><span class="sxs-lookup"><span data-stu-id="5c862-1238">A period</span></span> 
- <span data-ttu-id="5c862-1239">три цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-1239">Three digits</span></span> 
- <span data-ttu-id="5c862-1240">тире;</span><span class="sxs-lookup"><span data-stu-id="5c862-1240">A dash</span></span> 
- <span data-ttu-id="5c862-1241">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1242">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1242">Checksum</span></span>

<span data-ttu-id="5c862-1243">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1244">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1244">Definition</span></span>

<span data-ttu-id="5c862-1245">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1246">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1247">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="5c862-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="5c862-1248">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1248">The checksum passes.</span></span>

<span data-ttu-id="5c862-1249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1250">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1251">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1251">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1252">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="5c862-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="5c862-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="5c862-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="5c862-1254">National Identification Number</span></span> 
- <span data-ttu-id="5c862-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="5c862-1255">Identity card</span></span> 
- <span data-ttu-id="5c862-1256">ID</span><span class="sxs-lookup"><span data-stu-id="5c862-1256">ID</span></span> 
- <span data-ttu-id="5c862-1257">Процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-1257">Identification</span></span> 
- <span data-ttu-id="5c862-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="5c862-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="5c862-1259">ВЫПОЛНЯЕМ</span><span class="sxs-lookup"><span data-stu-id="5c862-1259">RUN</span></span> 
- <span data-ttu-id="5c862-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="5c862-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="5c862-1261">СНИЖАТЬСЯ</span><span class="sxs-lookup"><span data-stu-id="5c862-1261">RUT</span></span> 
- <span data-ttu-id="5c862-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="5c862-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="5c862-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="5c862-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="5c862-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="5c862-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="5c862-1265">идентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="5c862-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="5c862-1266">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="5c862-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1267">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1267">Format</span></span>

<span data-ttu-id="5c862-1268">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1269">Pattern</span></span>

<span data-ttu-id="5c862-1270">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-1270">18 digits:</span></span>
- <span data-ttu-id="5c862-1271">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="5c862-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="5c862-1272">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="5c862-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="5c862-1273">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="5c862-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="5c862-1274">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1275">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1275">Checksum</span></span>

<span data-ttu-id="5c862-1276">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1277">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1277">Definition</span></span>

<span data-ttu-id="5c862-1278">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1279">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1280">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="5c862-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="5c862-1281">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1281">The checksum passes.</span></span>

<span data-ttu-id="5c862-1282">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1283">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1284">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1284">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1285">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="5c862-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="5c862-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="5c862-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="5c862-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="5c862-1288">NO7</span><span class="sxs-lookup"><span data-stu-id="5c862-1288">PRC</span></span> 
- <span data-ttu-id="5c862-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="5c862-1289">National Identification Card</span></span> 
- <span data-ttu-id="5c862-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="5c862-1290">身份证</span></span> 
- <span data-ttu-id="5c862-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="5c862-1291">居民 身份证</span></span> 
- <span data-ttu-id="5c862-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="5c862-1292">居民身份证</span></span> 
- <span data-ttu-id="5c862-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="5c862-1293">鉴定</span></span> 
- <span data-ttu-id="5c862-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-1294">身分證</span></span> 
- <span data-ttu-id="5c862-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-1295">居民 身份證</span></span>
- <span data-ttu-id="5c862-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="5c862-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="5c862-1297">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="5c862-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1298">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1298">Format</span></span>

<span data-ttu-id="5c862-1299">16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.</span><span class="sxs-lookup"><span data-stu-id="5c862-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1300">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1300">Pattern</span></span>

<span data-ttu-id="5c862-1301">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="5c862-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1302">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1302">Checksum</span></span>

<span data-ttu-id="5c862-1303">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="5c862-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1304">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1304">Definition</span></span>

<span data-ttu-id="5c862-1305">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1306">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1307">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-1307">One of the following is true:</span></span>
    - <span data-ttu-id="5c862-1308">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="5c862-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="5c862-1309">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="5c862-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="5c862-1310">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="5c862-1311">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1311">The checksum passes.</span></span>

<span data-ttu-id="5c862-1312">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1313">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1314">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1314">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="5c862-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="5c862-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="5c862-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="5c862-1317">card verification</span></span>
- <span data-ttu-id="5c862-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-1318">card identification number</span></span>
- <span data-ttu-id="5c862-1319">квн</span><span class="sxs-lookup"><span data-stu-id="5c862-1319">cvn</span></span>
- <span data-ttu-id="5c862-1320">cid</span><span class="sxs-lookup"><span data-stu-id="5c862-1320">cid</span></span>
- <span data-ttu-id="5c862-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="5c862-1321">cvc2</span></span>
- <span data-ttu-id="5c862-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="5c862-1322">cvv2</span></span>
- <span data-ttu-id="5c862-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="5c862-1323">pin block</span></span>
- <span data-ttu-id="5c862-1324">security code</span><span class="sxs-lookup"><span data-stu-id="5c862-1324">security code</span></span>
- <span data-ttu-id="5c862-1325">security number</span><span class="sxs-lookup"><span data-stu-id="5c862-1325">security number</span></span>
- <span data-ttu-id="5c862-1326">security no</span><span class="sxs-lookup"><span data-stu-id="5c862-1326">security no</span></span>
- <span data-ttu-id="5c862-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="5c862-1327">issue number</span></span>
- <span data-ttu-id="5c862-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="5c862-1328">issue no</span></span>
- <span data-ttu-id="5c862-1329">криптограмме</span><span class="sxs-lookup"><span data-stu-id="5c862-1329">cryptogramme</span></span>
- <span data-ttu-id="5c862-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="5c862-1330">numéro de sécurité</span></span>
- <span data-ttu-id="5c862-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="5c862-1331">numero de securite</span></span>
- <span data-ttu-id="5c862-1332">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="5c862-1333">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="5c862-1334">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="5c862-1334">prüfziffer</span></span>
- <span data-ttu-id="5c862-1335">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="5c862-1335">prufziffer</span></span>
- <span data-ttu-id="5c862-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="5c862-1336">sicherheits Kode</span></span>
- <span data-ttu-id="5c862-1337">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="5c862-1337">sicherheitscode</span></span>
- <span data-ttu-id="5c862-1338">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="5c862-1339">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1339">verfalldatum</span></span>
- <span data-ttu-id="5c862-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="5c862-1340">codice di verifica</span></span>
- <span data-ttu-id="5c862-1341">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1341">cod.</span></span> <span data-ttu-id="5c862-1342">сикурезза</span><span class="sxs-lookup"><span data-stu-id="5c862-1342">sicurezza</span></span>
- <span data-ttu-id="5c862-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="5c862-1343">cod sicurezza</span></span>
- <span data-ttu-id="5c862-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5c862-1344">n autorizzazione</span></span>
- <span data-ttu-id="5c862-1345">кóдиго</span><span class="sxs-lookup"><span data-stu-id="5c862-1345">código</span></span>
- <span data-ttu-id="5c862-1346">кодиго</span><span class="sxs-lookup"><span data-stu-id="5c862-1346">codigo</span></span>
- <span data-ttu-id="5c862-1347">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1347">cod.</span></span> <span data-ttu-id="5c862-1348">сег</span><span class="sxs-lookup"><span data-stu-id="5c862-1348">seg</span></span>
- <span data-ttu-id="5c862-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="5c862-1349">cod seg</span></span>
- <span data-ttu-id="5c862-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1350">código de segurança</span></span>
- <span data-ttu-id="5c862-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1351">codigo de seguranca</span></span>
- <span data-ttu-id="5c862-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1352">codigo de segurança</span></span>
- <span data-ttu-id="5c862-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1353">código de seguranca</span></span>
- <span data-ttu-id="5c862-1354">кóд.</span><span class="sxs-lookup"><span data-stu-id="5c862-1354">cód.</span></span> <span data-ttu-id="5c862-1355">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="5c862-1355">segurança</span></span>
- <span data-ttu-id="5c862-1356">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1356">cod.</span></span> <span data-ttu-id="5c862-1357">сегуранка наложенный платеж.</span><span class="sxs-lookup"><span data-stu-id="5c862-1357">seguranca cod.</span></span> <span data-ttu-id="5c862-1358">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="5c862-1358">segurança</span></span>
- <span data-ttu-id="5c862-1359">кóд.</span><span class="sxs-lookup"><span data-stu-id="5c862-1359">cód.</span></span> <span data-ttu-id="5c862-1360">сегуранка</span><span class="sxs-lookup"><span data-stu-id="5c862-1360">seguranca</span></span>
- <span data-ttu-id="5c862-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1361">cód segurança</span></span>
- <span data-ttu-id="5c862-1362">наложенный на наложенный сегуранка сегуранçа</span><span class="sxs-lookup"><span data-stu-id="5c862-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="5c862-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1363">cód seguranca</span></span>
- <span data-ttu-id="5c862-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="5c862-1364">número de verificação</span></span>
- <span data-ttu-id="5c862-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="5c862-1365">numero de verificacao</span></span>
- <span data-ttu-id="5c862-1366">аблауф</span><span class="sxs-lookup"><span data-stu-id="5c862-1366">ablauf</span></span>
- <span data-ttu-id="5c862-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="5c862-1367">gültig bis</span></span>
- <span data-ttu-id="5c862-1368">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="5c862-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="5c862-1369">gultig bis</span></span>
- <span data-ttu-id="5c862-1370">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="5c862-1371">скаденза</span><span class="sxs-lookup"><span data-stu-id="5c862-1371">scadenza</span></span>
- <span data-ttu-id="5c862-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="5c862-1372">data scad</span></span>
- <span data-ttu-id="5c862-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="5c862-1373">fecha de expiracion</span></span>
- <span data-ttu-id="5c862-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="5c862-1374">fecha de venc</span></span>
- <span data-ttu-id="5c862-1375">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="5c862-1375">vencimiento</span></span>
- <span data-ttu-id="5c862-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="5c862-1376">válido hasta</span></span>
- <span data-ttu-id="5c862-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="5c862-1377">valido hasta</span></span>
- <span data-ttu-id="5c862-1378">вто</span><span class="sxs-lookup"><span data-stu-id="5c862-1378">vto</span></span>
- <span data-ttu-id="5c862-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="5c862-1379">data de expiração</span></span>
- <span data-ttu-id="5c862-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="5c862-1380">data de expiracao</span></span>
- <span data-ttu-id="5c862-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="5c862-1381">data em que expira</span></span>
- <span data-ttu-id="5c862-1382">валидаде</span><span class="sxs-lookup"><span data-stu-id="5c862-1382">validade</span></span>
- <span data-ttu-id="5c862-1383">валор</span><span class="sxs-lookup"><span data-stu-id="5c862-1383">valor</span></span>
- <span data-ttu-id="5c862-1384">венЦименто</span><span class="sxs-lookup"><span data-stu-id="5c862-1384">vencimento</span></span>
- <span data-ttu-id="5c862-1385">венк</span><span class="sxs-lookup"><span data-stu-id="5c862-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="5c862-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="5c862-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="5c862-1387">амекс</span><span class="sxs-lookup"><span data-stu-id="5c862-1387">amex</span></span>
- <span data-ttu-id="5c862-1388">american express</span><span class="sxs-lookup"><span data-stu-id="5c862-1388">american express</span></span>
- <span data-ttu-id="5c862-1389">американекспресс</span><span class="sxs-lookup"><span data-stu-id="5c862-1389">americanexpress</span></span>
- <span data-ttu-id="5c862-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="5c862-1390">Visa</span></span>
- <span data-ttu-id="5c862-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="5c862-1391">mastercard</span></span>
- <span data-ttu-id="5c862-1392">master card</span><span class="sxs-lookup"><span data-stu-id="5c862-1392">master card</span></span>
- <span data-ttu-id="5c862-1393">MC</span><span class="sxs-lookup"><span data-stu-id="5c862-1393">mc</span></span> 
- <span data-ttu-id="5c862-1394">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1394">mastercards</span></span>
- <span data-ttu-id="5c862-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1395">master cards</span></span>
- <span data-ttu-id="5c862-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="5c862-1396">diner's Club</span></span>
- <span data-ttu-id="5c862-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="5c862-1397">diners club</span></span>
- <span data-ttu-id="5c862-1398">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="5c862-1398">dinersclub</span></span>
- <span data-ttu-id="5c862-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="5c862-1399">discover card</span></span>
- <span data-ttu-id="5c862-1400">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="5c862-1400">discovercard</span></span>
- <span data-ttu-id="5c862-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1401">discover cards</span></span>
- <span data-ttu-id="5c862-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="5c862-1402">JCB</span></span>
- <span data-ttu-id="5c862-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="5c862-1403">japanese card bureau</span></span>
- <span data-ttu-id="5c862-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="5c862-1404">carte blanche</span></span>
- <span data-ttu-id="5c862-1405">картебланче</span><span class="sxs-lookup"><span data-stu-id="5c862-1405">carteblanche</span></span>
- <span data-ttu-id="5c862-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="5c862-1406">credit card</span></span>
- <span data-ttu-id="5c862-1407">Центральной #</span><span class="sxs-lookup"><span data-stu-id="5c862-1407">cc#</span></span>
- <span data-ttu-id="5c862-1408">CC #:</span><span class="sxs-lookup"><span data-stu-id="5c862-1408">cc#:</span></span>
- <span data-ttu-id="5c862-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="5c862-1409">expiration date</span></span>
- <span data-ttu-id="5c862-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="5c862-1410">exp date</span></span>
- <span data-ttu-id="5c862-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="5c862-1411">expiry date</span></span>
- <span data-ttu-id="5c862-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="5c862-1412">date d’expiration</span></span>
- <span data-ttu-id="5c862-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="5c862-1413">date d'exp</span></span>
- <span data-ttu-id="5c862-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="5c862-1414">date expiration</span></span>
- <span data-ttu-id="5c862-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="5c862-1415">bank card</span></span>
- <span data-ttu-id="5c862-1416">банккард</span><span class="sxs-lookup"><span data-stu-id="5c862-1416">bankcard</span></span>
- <span data-ttu-id="5c862-1417">card number</span><span class="sxs-lookup"><span data-stu-id="5c862-1417">card number</span></span>
- <span data-ttu-id="5c862-1418">card num</span><span class="sxs-lookup"><span data-stu-id="5c862-1418">card num</span></span>
- <span data-ttu-id="5c862-1419">карднумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-1419">cardnumber</span></span>
- <span data-ttu-id="5c862-1420">карднумберс</span><span class="sxs-lookup"><span data-stu-id="5c862-1420">cardnumbers</span></span>
- <span data-ttu-id="5c862-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-1421">card numbers</span></span>
- <span data-ttu-id="5c862-1422">кредиткард</span><span class="sxs-lookup"><span data-stu-id="5c862-1422">creditcard</span></span>
- <span data-ttu-id="5c862-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1423">credit cards</span></span>
- <span data-ttu-id="5c862-1424">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1424">creditcards</span></span>
- <span data-ttu-id="5c862-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="5c862-1425">ccn</span></span>
- <span data-ttu-id="5c862-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="5c862-1426">card holder</span></span>
- <span data-ttu-id="5c862-1427">банков</span><span class="sxs-lookup"><span data-stu-id="5c862-1427">cardholder</span></span>
- <span data-ttu-id="5c862-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="5c862-1428">card holders</span></span>
- <span data-ttu-id="5c862-1429">карты</span><span class="sxs-lookup"><span data-stu-id="5c862-1429">cardholders</span></span>
- <span data-ttu-id="5c862-1430">check card</span><span class="sxs-lookup"><span data-stu-id="5c862-1430">check card</span></span>
- <span data-ttu-id="5c862-1431">чекккард</span><span class="sxs-lookup"><span data-stu-id="5c862-1431">checkcard</span></span>
- <span data-ttu-id="5c862-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1432">check cards</span></span>
- <span data-ttu-id="5c862-1433">чекккардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1433">checkcards</span></span>
- <span data-ttu-id="5c862-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="5c862-1434">debit card</span></span>
- <span data-ttu-id="5c862-1435">дебиткард</span><span class="sxs-lookup"><span data-stu-id="5c862-1435">debitcard</span></span>
- <span data-ttu-id="5c862-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1436">debit cards</span></span>
- <span data-ttu-id="5c862-1437">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1437">debitcards</span></span>
- <span data-ttu-id="5c862-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="5c862-1438">atm card</span></span>
- <span data-ttu-id="5c862-1439">атмкард</span><span class="sxs-lookup"><span data-stu-id="5c862-1439">atmcard</span></span>
- <span data-ttu-id="5c862-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1440">atm cards</span></span>
- <span data-ttu-id="5c862-1441">атмкардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1441">atmcards</span></span>
- <span data-ttu-id="5c862-1442">енрауте</span><span class="sxs-lookup"><span data-stu-id="5c862-1442">enroute</span></span>
- <span data-ttu-id="5c862-1443">en route</span><span class="sxs-lookup"><span data-stu-id="5c862-1443">en route</span></span>
- <span data-ttu-id="5c862-1444">card type</span><span class="sxs-lookup"><span data-stu-id="5c862-1444">card type</span></span>
- <span data-ttu-id="5c862-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="5c862-1445">carte bancaire</span></span>
- <span data-ttu-id="5c862-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="5c862-1446">carte de crédit</span></span>
- <span data-ttu-id="5c862-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="5c862-1447">carte de credit</span></span>
- <span data-ttu-id="5c862-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1448">numéro de carte</span></span>
- <span data-ttu-id="5c862-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1449">numero de carte</span></span>
- <span data-ttu-id="5c862-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1450">nº de la carte</span></span>
- <span data-ttu-id="5c862-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1451">nº de carte</span></span>
- <span data-ttu-id="5c862-1452">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="5c862-1452">kreditkarte</span></span>
- <span data-ttu-id="5c862-1453">карте</span><span class="sxs-lookup"><span data-stu-id="5c862-1453">karte</span></span>
- <span data-ttu-id="5c862-1454">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="5c862-1454">karteninhaber</span></span>
- <span data-ttu-id="5c862-1455">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="5c862-1455">karteninhabers</span></span>
- <span data-ttu-id="5c862-1456">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="5c862-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="5c862-1457">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="5c862-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="5c862-1458">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="5c862-1458">kreditkartentyp</span></span>
- <span data-ttu-id="5c862-1459">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="5c862-1459">eigentümername</span></span>
- <span data-ttu-id="5c862-1460">картеннр</span><span class="sxs-lookup"><span data-stu-id="5c862-1460">kartennr</span></span> 
- <span data-ttu-id="5c862-1461">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1461">kartennummer</span></span>
- <span data-ttu-id="5c862-1462">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1462">kreditkartennummer</span></span>
- <span data-ttu-id="5c862-1463">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="5c862-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1464">carta di credito</span></span>
- <span data-ttu-id="5c862-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1465">carta credito</span></span>
- <span data-ttu-id="5c862-1466">Корзина "</span><span class="sxs-lookup"><span data-stu-id="5c862-1466">carta</span></span>
- <span data-ttu-id="5c862-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1467">n carta</span></span>
- <span data-ttu-id="5c862-1468">НР.</span><span class="sxs-lookup"><span data-stu-id="5c862-1468">nr.</span></span> <span data-ttu-id="5c862-1469">Корзина "</span><span class="sxs-lookup"><span data-stu-id="5c862-1469">carta</span></span>
- <span data-ttu-id="5c862-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1470">nr carta</span></span>
- <span data-ttu-id="5c862-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1471">numero carta</span></span>
- <span data-ttu-id="5c862-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1472">numero della carta</span></span>
- <span data-ttu-id="5c862-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1473">numero di carta</span></span>
- <span data-ttu-id="5c862-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1474">tarjeta credito</span></span>
- <span data-ttu-id="5c862-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1475">tarjeta de credito</span></span>
- <span data-ttu-id="5c862-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="5c862-1476">tarjeta crédito</span></span>
- <span data-ttu-id="5c862-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="5c862-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="5c862-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="5c862-1478">tarjeta de atm</span></span>
- <span data-ttu-id="5c862-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="5c862-1479">tarjeta atm</span></span>
- <span data-ttu-id="5c862-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1480">tarjeta debito</span></span>
- <span data-ttu-id="5c862-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1481">tarjeta de debito</span></span>
- <span data-ttu-id="5c862-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="5c862-1482">tarjeta débito</span></span>
- <span data-ttu-id="5c862-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="5c862-1483">tarjeta de débito</span></span>
- <span data-ttu-id="5c862-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1484">nº de tarjeta</span></span>
- <span data-ttu-id="5c862-1485">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1485">no.</span></span> <span data-ttu-id="5c862-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1486">de tarjeta</span></span>
- <span data-ttu-id="5c862-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1487">no de tarjeta</span></span>
- <span data-ttu-id="5c862-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1488">numero de tarjeta</span></span>
- <span data-ttu-id="5c862-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1489">número de tarjeta</span></span>
- <span data-ttu-id="5c862-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="5c862-1490">tarjeta no</span></span>
- <span data-ttu-id="5c862-1491">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="5c862-1491">tarjetahabiente</span></span>
- <span data-ttu-id="5c862-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="5c862-1492">cartão de crédito</span></span>
- <span data-ttu-id="5c862-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1493">cartão de credito</span></span>
- <span data-ttu-id="5c862-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="5c862-1494">cartao de crédito</span></span>
- <span data-ttu-id="5c862-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1495">cartao de credito</span></span>
- <span data-ttu-id="5c862-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="5c862-1496">cartão de débito</span></span>
- <span data-ttu-id="5c862-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="5c862-1497">cartao de débito</span></span>
- <span data-ttu-id="5c862-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1498">cartão de debito</span></span>
- <span data-ttu-id="5c862-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1499">cartao de debito</span></span>
- <span data-ttu-id="5c862-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="5c862-1500">débito automático</span></span>
- <span data-ttu-id="5c862-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="5c862-1501">debito automatico</span></span>
- <span data-ttu-id="5c862-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1502">número do cartão</span></span>
- <span data-ttu-id="5c862-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1503">numero do cartão</span></span> 
- <span data-ttu-id="5c862-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1504">número do cartao</span></span>
- <span data-ttu-id="5c862-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1505">numero do cartao</span></span>
- <span data-ttu-id="5c862-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1506">número de cartão</span></span>
- <span data-ttu-id="5c862-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1507">numero de cartão</span></span>
- <span data-ttu-id="5c862-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1508">número de cartao</span></span>
- <span data-ttu-id="5c862-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1509">numero de cartao</span></span>
- <span data-ttu-id="5c862-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1510">nº do cartão</span></span>
- <span data-ttu-id="5c862-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1511">nº do cartao</span></span>
- <span data-ttu-id="5c862-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="5c862-1512">nº.</span></span> <span data-ttu-id="5c862-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1513">do cartão</span></span>
- <span data-ttu-id="5c862-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1514">no do cartão</span></span>
- <span data-ttu-id="5c862-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1515">no do cartao</span></span>
- <span data-ttu-id="5c862-1516">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1516">no.</span></span> <span data-ttu-id="5c862-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1517">do cartão</span></span>
- <span data-ttu-id="5c862-1518">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1518">no.</span></span> <span data-ttu-id="5c862-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="5c862-1520">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="5c862-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1521">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1521">Format</span></span>

<span data-ttu-id="5c862-1522">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1523">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1523">Pattern</span></span>

<span data-ttu-id="5c862-1524">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1525">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1525">Checksum</span></span>

<span data-ttu-id="5c862-1526">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1527">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1527">Definition</span></span>

<span data-ttu-id="5c862-1528">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1529">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1530">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="5c862-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-1531">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="5c862-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="5c862-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="5c862-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="5c862-1533">Croatian identity card</span></span>
- <span data-ttu-id="5c862-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="5c862-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="5c862-1535">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="5c862-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1536">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1536">Format</span></span>

<span data-ttu-id="5c862-1537">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1538">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1538">Pattern</span></span>

<span data-ttu-id="5c862-1539">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-1539">11 digits:</span></span>
- <span data-ttu-id="5c862-1540">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1540">10 digits</span></span> 
- <span data-ttu-id="5c862-1541">Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1542">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1542">Checksum</span></span>

<span data-ttu-id="5c862-1543">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1544">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1544">Definition</span></span>

<span data-ttu-id="5c862-1545">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1546">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1547">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="5c862-1548">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1548">The checksum passes.</span></span>

<span data-ttu-id="5c862-1549">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1550">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1551">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1551">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1552">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="5c862-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="5c862-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="5c862-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="5c862-1554">Personal Identification Number</span></span>
- <span data-ttu-id="5c862-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="5c862-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="5c862-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="5c862-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="5c862-1557">Номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="5c862-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1558">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1558">Format</span></span>

<span data-ttu-id="5c862-1559">Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)</span><span class="sxs-lookup"><span data-stu-id="5c862-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1560">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1560">Pattern</span></span>

<span data-ttu-id="5c862-1561">Девять цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="5c862-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="5c862-1562">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1562">Nine digits</span></span>

<span data-ttu-id="5c862-1563">OR</span><span class="sxs-lookup"><span data-stu-id="5c862-1563">OR</span></span>

- <span data-ttu-id="5c862-1564">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="5c862-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="5c862-1565">косая черта;</span><span class="sxs-lookup"><span data-stu-id="5c862-1565">A forward slash</span></span>
- <span data-ttu-id="5c862-1566">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-1566">Three digits</span></span>

<span data-ttu-id="5c862-1567">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="5c862-1567">10 digits (new format):</span></span>
- <span data-ttu-id="5c862-1568">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1568">10 digits</span></span>

<span data-ttu-id="5c862-1569">OR</span><span class="sxs-lookup"><span data-stu-id="5c862-1569">OR</span></span>

- <span data-ttu-id="5c862-1570">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="5c862-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="5c862-1571">косая черта;</span><span class="sxs-lookup"><span data-stu-id="5c862-1571">A forward slash</span></span> 
- <span data-ttu-id="5c862-1572">Четыре цифры, где последняя цифра является контрольной цифрой</span><span class="sxs-lookup"><span data-stu-id="5c862-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1573">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1573">Checksum</span></span>

<span data-ttu-id="5c862-1574">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1575">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1575">Definition</span></span>

<span data-ttu-id="5c862-1576">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_czech_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-1577">находится ключевое слово из Keyword_czech_id_card;</span><span class="sxs-lookup"><span data-stu-id="5c862-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="5c862-1578">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1578">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="5c862-1579">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1579">Keywords</span></span>

- <span data-ttu-id="5c862-1580">номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="5c862-1580">czech personal identity number</span></span>
- <span data-ttu-id="5c862-1581">Роднé číсло</span><span class="sxs-lookup"><span data-stu-id="5c862-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="5c862-1582">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="5c862-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1583">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1583">Format</span></span>

<span data-ttu-id="5c862-1584">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="5c862-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1585">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1585">Pattern</span></span>

<span data-ttu-id="5c862-1586">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-1586">10 digits:</span></span>
- <span data-ttu-id="5c862-1587">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="5c862-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="5c862-1588">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-1588">A hyphen</span></span> 
- <span data-ttu-id="5c862-1589">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1590">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1590">Checksum</span></span>

<span data-ttu-id="5c862-1591">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1592">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1592">Definition</span></span>

<span data-ttu-id="5c862-1593">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Regex_denmark_id находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-1594">находится ключевое слово из Keyword_denmark_id;</span><span class="sxs-lookup"><span data-stu-id="5c862-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="5c862-1595">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1595">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-1596">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="5c862-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="5c862-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="5c862-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="5c862-1598">Personal Identification Number</span></span>
- <span data-ttu-id="5c862-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="5c862-1599">CPR</span></span>
- <span data-ttu-id="5c862-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="5c862-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="5c862-1601">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="5c862-1602">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="5c862-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1603">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1603">Format</span></span>

<span data-ttu-id="5c862-1604">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1605">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1605">Pattern</span></span>

<span data-ttu-id="5c862-1606">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="5c862-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="5c862-1607">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="5c862-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="5c862-1608">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="5c862-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="5c862-1609">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="5c862-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1610">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1610">Checksum</span></span>

<span data-ttu-id="5c862-1611">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1612">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1612">Definition</span></span>

<span data-ttu-id="5c862-1613">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1614">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1615">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1615">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-1616">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1616">Keywords</span></span>

<span data-ttu-id="5c862-1617">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="5c862-1618">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="5c862-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1619">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1619">Format</span></span>

<span data-ttu-id="5c862-1620">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1621">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1621">Pattern</span></span>

<span data-ttu-id="5c862-1622">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="5c862-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1623">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1623">Checksum</span></span>

<span data-ttu-id="5c862-1624">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1625">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1625">Definition</span></span>

<span data-ttu-id="5c862-1626">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1627">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1628">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="5c862-1629">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="5c862-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="5c862-1630">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="5c862-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="5c862-1631">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="5c862-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="5c862-1632">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="5c862-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="5c862-1633">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="5c862-1634">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1634">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1635">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="5c862-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="5c862-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="5c862-1637">account number</span><span class="sxs-lookup"><span data-stu-id="5c862-1637">account number</span></span> 
- <span data-ttu-id="5c862-1638">card number</span><span class="sxs-lookup"><span data-stu-id="5c862-1638">card number</span></span> 
- <span data-ttu-id="5c862-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="5c862-1639">card no.</span></span> 
- <span data-ttu-id="5c862-1640">security number</span><span class="sxs-lookup"><span data-stu-id="5c862-1640">security number</span></span> 
- <span data-ttu-id="5c862-1641">Центральной #</span><span class="sxs-lookup"><span data-stu-id="5c862-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="5c862-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="5c862-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="5c862-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="5c862-1643">acct nbr</span></span> 
- <span data-ttu-id="5c862-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="5c862-1644">acct num</span></span> 
- <span data-ttu-id="5c862-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="5c862-1645">acct no</span></span> 
- <span data-ttu-id="5c862-1646">american express</span><span class="sxs-lookup"><span data-stu-id="5c862-1646">american express</span></span> 
- <span data-ttu-id="5c862-1647">американекспресс</span><span class="sxs-lookup"><span data-stu-id="5c862-1647">americanexpress</span></span> 
- <span data-ttu-id="5c862-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="5c862-1648">americano espresso</span></span> 
- <span data-ttu-id="5c862-1649">амекс</span><span class="sxs-lookup"><span data-stu-id="5c862-1649">amex</span></span> 
- <span data-ttu-id="5c862-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="5c862-1650">atm card</span></span> 
- <span data-ttu-id="5c862-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1651">atm cards</span></span> 
- <span data-ttu-id="5c862-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="5c862-1652">atm kaart</span></span> 
- <span data-ttu-id="5c862-1653">атмкард</span><span class="sxs-lookup"><span data-stu-id="5c862-1653">atmcard</span></span> 
- <span data-ttu-id="5c862-1654">атмкардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1654">atmcards</span></span> 
- <span data-ttu-id="5c862-1655">атмкаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1655">atmkaart</span></span> 
- <span data-ttu-id="5c862-1656">атмкаартен</span><span class="sxs-lookup"><span data-stu-id="5c862-1656">atmkaarten</span></span> 
- <span data-ttu-id="5c862-1657">банконтакт</span><span class="sxs-lookup"><span data-stu-id="5c862-1657">bancontact</span></span> 
- <span data-ttu-id="5c862-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="5c862-1658">bank card</span></span> 
- <span data-ttu-id="5c862-1659">банккаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1659">bankkaart</span></span> 
- <span data-ttu-id="5c862-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="5c862-1660">card holder</span></span> 
- <span data-ttu-id="5c862-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="5c862-1661">card holders</span></span> 
- <span data-ttu-id="5c862-1662">card num</span><span class="sxs-lookup"><span data-stu-id="5c862-1662">card num</span></span> 
- <span data-ttu-id="5c862-1663">card number</span><span class="sxs-lookup"><span data-stu-id="5c862-1663">card number</span></span> 
- <span data-ttu-id="5c862-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-1664">card numbers</span></span> 
- <span data-ttu-id="5c862-1665">card type</span><span class="sxs-lookup"><span data-stu-id="5c862-1665">card type</span></span> 
- <span data-ttu-id="5c862-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="5c862-1666">cardano numerico</span></span> 
- <span data-ttu-id="5c862-1667">банков</span><span class="sxs-lookup"><span data-stu-id="5c862-1667">cardholder</span></span> 
- <span data-ttu-id="5c862-1668">карты</span><span class="sxs-lookup"><span data-stu-id="5c862-1668">cardholders</span></span> 
- <span data-ttu-id="5c862-1669">карднумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-1669">cardnumber</span></span> 
- <span data-ttu-id="5c862-1670">карднумберс</span><span class="sxs-lookup"><span data-stu-id="5c862-1670">cardnumbers</span></span> 
- <span data-ttu-id="5c862-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="5c862-1671">carta bianca</span></span> 
- <span data-ttu-id="5c862-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1672">carta credito</span></span> 
- <span data-ttu-id="5c862-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1673">carta di credito</span></span> 
- <span data-ttu-id="5c862-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1674">cartao de credito</span></span> 
- <span data-ttu-id="5c862-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="5c862-1675">cartao de crédito</span></span> 
- <span data-ttu-id="5c862-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1676">cartao de debito</span></span> 
- <span data-ttu-id="5c862-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="5c862-1677">cartao de débito</span></span> 
- <span data-ttu-id="5c862-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="5c862-1678">carte bancaire</span></span> 
- <span data-ttu-id="5c862-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="5c862-1679">carte blanche</span></span> 
- <span data-ttu-id="5c862-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="5c862-1680">carte bleue</span></span> 
- <span data-ttu-id="5c862-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="5c862-1681">carte de credit</span></span> 
- <span data-ttu-id="5c862-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="5c862-1682">carte de crédit</span></span> 
- <span data-ttu-id="5c862-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1683">carte di credito</span></span> 
- <span data-ttu-id="5c862-1684">картебланче</span><span class="sxs-lookup"><span data-stu-id="5c862-1684">carteblanche</span></span> 
- <span data-ttu-id="5c862-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1685">cartão de credito</span></span> 
- <span data-ttu-id="5c862-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="5c862-1686">cartão de crédito</span></span> 
- <span data-ttu-id="5c862-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1687">cartão de debito</span></span> 
- <span data-ttu-id="5c862-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="5c862-1688">cartão de débito</span></span> 
- <span data-ttu-id="5c862-1689">cb</span><span class="sxs-lookup"><span data-stu-id="5c862-1689">cb</span></span> 
- <span data-ttu-id="5c862-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="5c862-1690">ccn</span></span> 
- <span data-ttu-id="5c862-1691">check card</span><span class="sxs-lookup"><span data-stu-id="5c862-1691">check card</span></span> 
- <span data-ttu-id="5c862-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1692">check cards</span></span> 
- <span data-ttu-id="5c862-1693">чекккард</span><span class="sxs-lookup"><span data-stu-id="5c862-1693">checkcard</span></span>
- <span data-ttu-id="5c862-1694">чекккардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1694">checkcards</span></span> 
- <span data-ttu-id="5c862-1695">чекуекаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1695">chequekaart</span></span> 
- <span data-ttu-id="5c862-1696">Logic</span><span class="sxs-lookup"><span data-stu-id="5c862-1696">cirrus</span></span> 
- <span data-ttu-id="5c862-1697">Cirrus центр EDC — Маестро</span><span class="sxs-lookup"><span data-stu-id="5c862-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="5c862-1698">контролекаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1698">controlekaart</span></span> 
- <span data-ttu-id="5c862-1699">контролекаартен</span><span class="sxs-lookup"><span data-stu-id="5c862-1699">controlekaarten</span></span> 
- <span data-ttu-id="5c862-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="5c862-1700">credit card</span></span> 
- <span data-ttu-id="5c862-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1701">credit cards</span></span> 
- <span data-ttu-id="5c862-1702">кредиткард</span><span class="sxs-lookup"><span data-stu-id="5c862-1702">creditcard</span></span> 
- <span data-ttu-id="5c862-1703">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1703">creditcards</span></span> 
- <span data-ttu-id="5c862-1704">дебеткаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1704">debetkaart</span></span> 
- <span data-ttu-id="5c862-1705">дебеткаартен</span><span class="sxs-lookup"><span data-stu-id="5c862-1705">debetkaarten</span></span> 
- <span data-ttu-id="5c862-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="5c862-1706">debit card</span></span> 
- <span data-ttu-id="5c862-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1707">debit cards</span></span> 
- <span data-ttu-id="5c862-1708">дебиткард</span><span class="sxs-lookup"><span data-stu-id="5c862-1708">debitcard</span></span> 
- <span data-ttu-id="5c862-1709">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1709">debitcards</span></span> 
- <span data-ttu-id="5c862-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="5c862-1710">debito automatico</span></span> 
- <span data-ttu-id="5c862-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="5c862-1711">diners club</span></span> 
- <span data-ttu-id="5c862-1712">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="5c862-1712">dinersclub</span></span> 
- <span data-ttu-id="5c862-1713">Повтор</span><span class="sxs-lookup"><span data-stu-id="5c862-1713">discover</span></span> 
- <span data-ttu-id="5c862-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="5c862-1714">discover card</span></span> 
- <span data-ttu-id="5c862-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1715">discover cards</span></span> 
- <span data-ttu-id="5c862-1716">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="5c862-1716">discovercard</span></span> 
- <span data-ttu-id="5c862-1717">дисковеркардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1717">discovercards</span></span> 
- <span data-ttu-id="5c862-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="5c862-1718">débito automático</span></span>
- <span data-ttu-id="5c862-1719">центр EDC</span><span class="sxs-lookup"><span data-stu-id="5c862-1719">edc</span></span> 
- <span data-ttu-id="5c862-1720">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="5c862-1720">eigentümername</span></span> 
- <span data-ttu-id="5c862-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="5c862-1721">european debit card</span></span> 
- <span data-ttu-id="5c862-1722">хуфдкаарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1722">hoofdkaart</span></span> 
- <span data-ttu-id="5c862-1723">хуфдкаартен</span><span class="sxs-lookup"><span data-stu-id="5c862-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="5c862-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="5c862-1724">in viaggio</span></span> 
- <span data-ttu-id="5c862-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="5c862-1725">japanese card bureau</span></span> 
- <span data-ttu-id="5c862-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="5c862-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="5c862-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="5c862-1727">jcb</span></span> 
- <span data-ttu-id="5c862-1728">каарт</span><span class="sxs-lookup"><span data-stu-id="5c862-1728">kaart</span></span> 
- <span data-ttu-id="5c862-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="5c862-1729">kaart num</span></span> 
- <span data-ttu-id="5c862-1730">каартаантал</span><span class="sxs-lookup"><span data-stu-id="5c862-1730">kaartaantal</span></span> 
- <span data-ttu-id="5c862-1731">каартаанталлен</span><span class="sxs-lookup"><span data-stu-id="5c862-1731">kaartaantallen</span></span> 
- <span data-ttu-id="5c862-1732">каарсаудер</span><span class="sxs-lookup"><span data-stu-id="5c862-1732">kaarthouder</span></span> 
- <span data-ttu-id="5c862-1733">каарсаудерс</span><span class="sxs-lookup"><span data-stu-id="5c862-1733">kaarthouders</span></span> 
- <span data-ttu-id="5c862-1734">карте</span><span class="sxs-lookup"><span data-stu-id="5c862-1734">karte</span></span>  
- <span data-ttu-id="5c862-1735">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="5c862-1735">karteninhaber</span></span> 
- <span data-ttu-id="5c862-1736">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="5c862-1736">karteninhabers</span></span>
- <span data-ttu-id="5c862-1737">картеннр</span><span class="sxs-lookup"><span data-stu-id="5c862-1737">kartennr</span></span> 
- <span data-ttu-id="5c862-1738">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1738">kartennummer</span></span> 
- <span data-ttu-id="5c862-1739">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="5c862-1739">kreditkarte</span></span> 
- <span data-ttu-id="5c862-1740">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="5c862-1741">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="5c862-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="5c862-1742">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="5c862-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="5c862-1743">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="5c862-1744">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="5c862-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="5c862-1745">маестро</span><span class="sxs-lookup"><span data-stu-id="5c862-1745">maestro</span></span> 
- <span data-ttu-id="5c862-1746">master card</span><span class="sxs-lookup"><span data-stu-id="5c862-1746">master card</span></span> 
- <span data-ttu-id="5c862-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="5c862-1747">master cards</span></span> 
- <span data-ttu-id="5c862-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="5c862-1748">mastercard</span></span> 
- <span data-ttu-id="5c862-1749">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="5c862-1749">mastercards</span></span> 
- <span data-ttu-id="5c862-1750">MC</span><span class="sxs-lookup"><span data-stu-id="5c862-1750">mc</span></span> 
- <span data-ttu-id="5c862-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="5c862-1751">mister cash</span></span> 
- <span data-ttu-id="5c862-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1752">n carta</span></span> 
- <span data-ttu-id="5c862-1753">Корзина "</span><span class="sxs-lookup"><span data-stu-id="5c862-1753">carta</span></span> 
- <span data-ttu-id="5c862-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1754">no de tarjeta</span></span> 
- <span data-ttu-id="5c862-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1755">no do cartao</span></span> 
- <span data-ttu-id="5c862-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1756">no do cartão</span></span> 
- <span data-ttu-id="5c862-1757">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1757">no.</span></span> <span data-ttu-id="5c862-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1758">de tarjeta</span></span> 
- <span data-ttu-id="5c862-1759">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1759">no.</span></span> <span data-ttu-id="5c862-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1760">do cartao</span></span> 
- <span data-ttu-id="5c862-1761">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1761">no.</span></span> <span data-ttu-id="5c862-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1762">do cartão</span></span> 
- <span data-ttu-id="5c862-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1763">nr carta</span></span> 
- <span data-ttu-id="5c862-1764">НР.</span><span class="sxs-lookup"><span data-stu-id="5c862-1764">nr.</span></span> <span data-ttu-id="5c862-1765">Корзина "</span><span class="sxs-lookup"><span data-stu-id="5c862-1765">carta</span></span> 
- <span data-ttu-id="5c862-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="5c862-1766">numeri di scheda</span></span> 
- <span data-ttu-id="5c862-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1767">numero carta</span></span> 
- <span data-ttu-id="5c862-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1768">numero de cartao</span></span> 
- <span data-ttu-id="5c862-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1769">numero de carte</span></span> 
- <span data-ttu-id="5c862-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1770">numero de cartão</span></span> 
- <span data-ttu-id="5c862-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1771">numero de tarjeta</span></span>
- <span data-ttu-id="5c862-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1772">numero della carta</span></span> 
- <span data-ttu-id="5c862-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1773">numero di carta</span></span> 
- <span data-ttu-id="5c862-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="5c862-1774">numero di scheda</span></span> 
- <span data-ttu-id="5c862-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1775">numero do cartao</span></span> 
- <span data-ttu-id="5c862-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1776">numero do cartão</span></span> 
- <span data-ttu-id="5c862-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1777">numéro de carte</span></span> 
- <span data-ttu-id="5c862-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="5c862-1778">nº carta</span></span> 
- <span data-ttu-id="5c862-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1779">nº de carte</span></span> 
- <span data-ttu-id="5c862-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="5c862-1780">nº de la carte</span></span> 
- <span data-ttu-id="5c862-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="5c862-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1782">nº do cartao</span></span> 
- <span data-ttu-id="5c862-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1783">nº do cartão</span></span> 
- <span data-ttu-id="5c862-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="5c862-1784">nº.</span></span> <span data-ttu-id="5c862-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1785">do cartão</span></span> 
- <span data-ttu-id="5c862-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1786">número de cartao</span></span> 
- <span data-ttu-id="5c862-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="5c862-1787">número de cartão</span></span> 
- <span data-ttu-id="5c862-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="5c862-1788">número de tarjeta</span></span> 
- <span data-ttu-id="5c862-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="5c862-1789">número do cartao</span></span> 
- <span data-ttu-id="5c862-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="5c862-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="5c862-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="5c862-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="5c862-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="5c862-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="5c862-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="5c862-1793">scheda della banca</span></span> 
- <span data-ttu-id="5c862-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="5c862-1794">scheda di controllo</span></span> 
- <span data-ttu-id="5c862-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1795">scheda di debito</span></span> 
- <span data-ttu-id="5c862-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="5c862-1796">scheda matrice</span></span> 
- <span data-ttu-id="5c862-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="5c862-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="5c862-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="5c862-1798">schede di controllo</span></span> 
- <span data-ttu-id="5c862-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1799">schede di debito</span></span> 
- <span data-ttu-id="5c862-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="5c862-1800">schede matrici</span></span> 
- <span data-ttu-id="5c862-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="5c862-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="5c862-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="5c862-1802">scoprono le schede</span></span> 
- <span data-ttu-id="5c862-1803">ОС</span><span class="sxs-lookup"><span data-stu-id="5c862-1803">solo</span></span> 
- <span data-ttu-id="5c862-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="5c862-1804">supporti di scheda</span></span> 
- <span data-ttu-id="5c862-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="5c862-1805">supporto di scheda</span></span> 
- <span data-ttu-id="5c862-1806">отключен</span><span class="sxs-lookup"><span data-stu-id="5c862-1806">switch</span></span> 
- <span data-ttu-id="5c862-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="5c862-1807">tarjeta atm</span></span> 
- <span data-ttu-id="5c862-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1808">tarjeta credito</span></span> 
- <span data-ttu-id="5c862-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="5c862-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="5c862-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="5c862-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="5c862-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="5c862-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="5c862-1812">tarjeta debito</span></span> 
- <span data-ttu-id="5c862-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="5c862-1813">tarjeta no</span></span>
- <span data-ttu-id="5c862-1814">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="5c862-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="5c862-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="5c862-1815">tipo della scheda</span></span> 
- <span data-ttu-id="5c862-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="5c862-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="5c862-1817">счеда</span><span class="sxs-lookup"><span data-stu-id="5c862-1817">scheda</span></span> 
- <span data-ttu-id="5c862-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="5c862-1818">v pay</span></span> 
- <span data-ttu-id="5c862-1819">v — оплата</span><span class="sxs-lookup"><span data-stu-id="5c862-1819">v-pay</span></span> 
- <span data-ttu-id="5c862-1820">Visa</span><span class="sxs-lookup"><span data-stu-id="5c862-1820">visa</span></span> 
- <span data-ttu-id="5c862-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="5c862-1821">visa plus</span></span> 
- <span data-ttu-id="5c862-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="5c862-1822">visa electron</span></span> 
- <span data-ttu-id="5c862-1823">висто</span><span class="sxs-lookup"><span data-stu-id="5c862-1823">visto</span></span> 
- <span data-ttu-id="5c862-1824">висум</span><span class="sxs-lookup"><span data-stu-id="5c862-1824">visum</span></span> 
- <span data-ttu-id="5c862-1825">впай</span><span class="sxs-lookup"><span data-stu-id="5c862-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="5c862-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="5c862-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="5c862-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-1827">card identification number</span></span>
- <span data-ttu-id="5c862-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="5c862-1828">card verification</span></span> 
- <span data-ttu-id="5c862-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="5c862-1829">cardi la verifica</span></span> 
- <span data-ttu-id="5c862-1830">cid</span><span class="sxs-lookup"><span data-stu-id="5c862-1830">cid</span></span> 
- <span data-ttu-id="5c862-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="5c862-1831">cod seg</span></span> 
- <span data-ttu-id="5c862-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1832">cod seguranca</span></span> 
- <span data-ttu-id="5c862-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1833">cod segurança</span></span> 
- <span data-ttu-id="5c862-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="5c862-1834">cod sicurezza</span></span> 
- <span data-ttu-id="5c862-1835">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1835">cod.</span></span> <span data-ttu-id="5c862-1836">сег</span><span class="sxs-lookup"><span data-stu-id="5c862-1836">seg</span></span> 
- <span data-ttu-id="5c862-1837">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1837">cod.</span></span> <span data-ttu-id="5c862-1838">сегуранка</span><span class="sxs-lookup"><span data-stu-id="5c862-1838">seguranca</span></span> 
- <span data-ttu-id="5c862-1839">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1839">cod.</span></span> <span data-ttu-id="5c862-1840">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="5c862-1840">segurança</span></span> 
- <span data-ttu-id="5c862-1841">наложен.</span><span class="sxs-lookup"><span data-stu-id="5c862-1841">cod.</span></span> <span data-ttu-id="5c862-1842">сикурезза</span><span class="sxs-lookup"><span data-stu-id="5c862-1842">sicurezza</span></span> 
- <span data-ttu-id="5c862-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5c862-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="5c862-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="5c862-1844">codice di verifica</span></span> 
- <span data-ttu-id="5c862-1845">кодиго</span><span class="sxs-lookup"><span data-stu-id="5c862-1845">codigo</span></span> 
- <span data-ttu-id="5c862-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="5c862-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1847">codigo de segurança</span></span> 
- <span data-ttu-id="5c862-1848">криттограмма</span><span class="sxs-lookup"><span data-stu-id="5c862-1848">crittogramma</span></span> 
- <span data-ttu-id="5c862-1849">криптограм</span><span class="sxs-lookup"><span data-stu-id="5c862-1849">cryptogram</span></span> 
- <span data-ttu-id="5c862-1850">криптограмме</span><span class="sxs-lookup"><span data-stu-id="5c862-1850">cryptogramme</span></span> 
- <span data-ttu-id="5c862-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="5c862-1851">cv2</span></span> 
- <span data-ttu-id="5c862-1852">квк</span><span class="sxs-lookup"><span data-stu-id="5c862-1852">cvc</span></span> 
- <span data-ttu-id="5c862-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="5c862-1853">cvc2</span></span> 
- <span data-ttu-id="5c862-1854">квн</span><span class="sxs-lookup"><span data-stu-id="5c862-1854">cvn</span></span> 
- <span data-ttu-id="5c862-1855">квв</span><span class="sxs-lookup"><span data-stu-id="5c862-1855">cvv</span></span> 
- <span data-ttu-id="5c862-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="5c862-1856">cvv2</span></span> 
- <span data-ttu-id="5c862-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1857">cód seguranca</span></span> 
- <span data-ttu-id="5c862-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1858">cód segurança</span></span> 
- <span data-ttu-id="5c862-1859">кóд.</span><span class="sxs-lookup"><span data-stu-id="5c862-1859">cód.</span></span> <span data-ttu-id="5c862-1860">сегуранка</span><span class="sxs-lookup"><span data-stu-id="5c862-1860">seguranca</span></span> 
- <span data-ttu-id="5c862-1861">кóд.</span><span class="sxs-lookup"><span data-stu-id="5c862-1861">cód.</span></span> <span data-ttu-id="5c862-1862">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="5c862-1862">segurança</span></span> 
- <span data-ttu-id="5c862-1863">кóдиго</span><span class="sxs-lookup"><span data-stu-id="5c862-1863">código</span></span> 
- <span data-ttu-id="5c862-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="5c862-1864">código de seguranca</span></span> 
- <span data-ttu-id="5c862-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="5c862-1865">código de segurança</span></span> 
- <span data-ttu-id="5c862-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="5c862-1866">de kaart controle</span></span> 
- <span data-ttu-id="5c862-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="5c862-1867">geeft nr uit</span></span> 
- <span data-ttu-id="5c862-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="5c862-1868">issue no</span></span> 
- <span data-ttu-id="5c862-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="5c862-1869">issue number</span></span> 
- <span data-ttu-id="5c862-1870">каартидентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="5c862-1871">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="5c862-1872">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="5c862-1873">квестиеаантал</span><span class="sxs-lookup"><span data-stu-id="5c862-1873">kwestieaantal</span></span> 
- <span data-ttu-id="5c862-1874">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1874">no.</span></span> <span data-ttu-id="5c862-1875">делл'едизионе</span><span class="sxs-lookup"><span data-stu-id="5c862-1875">dell'edizione</span></span> 
- <span data-ttu-id="5c862-1876">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-1876">no.</span></span> <span data-ttu-id="5c862-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5c862-1877">di sicurezza</span></span> 
- <span data-ttu-id="5c862-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="5c862-1878">numero de securite</span></span> 
- <span data-ttu-id="5c862-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="5c862-1879">numero de verificacao</span></span> 
- <span data-ttu-id="5c862-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="5c862-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="5c862-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="5c862-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="5c862-1882">счеда</span><span class="sxs-lookup"><span data-stu-id="5c862-1882">scheda</span></span> 
- <span data-ttu-id="5c862-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="5c862-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="5c862-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="5c862-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="5c862-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="5c862-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="5c862-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5c862-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="5c862-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="5c862-1887">número de verificação</span></span> 
- <span data-ttu-id="5c862-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="5c862-1888">perno il blocco</span></span> 
- <span data-ttu-id="5c862-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="5c862-1889">pin block</span></span> 
- <span data-ttu-id="5c862-1890">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="5c862-1890">prufziffer</span></span> 
- <span data-ttu-id="5c862-1891">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="5c862-1891">prüfziffer</span></span> 
- <span data-ttu-id="5c862-1892">security code</span><span class="sxs-lookup"><span data-stu-id="5c862-1892">security code</span></span> 
- <span data-ttu-id="5c862-1893">security no</span><span class="sxs-lookup"><span data-stu-id="5c862-1893">security no</span></span> 
- <span data-ttu-id="5c862-1894">security number</span><span class="sxs-lookup"><span data-stu-id="5c862-1894">security number</span></span> 
- <span data-ttu-id="5c862-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="5c862-1895">sicherheits kode</span></span> 
- <span data-ttu-id="5c862-1896">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="5c862-1896">sicherheitscode</span></span> 
- <span data-ttu-id="5c862-1897">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="5c862-1898">спелдблок</span><span class="sxs-lookup"><span data-stu-id="5c862-1898">speldblok</span></span> 
- <span data-ttu-id="5c862-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="5c862-1899">veiligheid nr</span></span> 
- <span data-ttu-id="5c862-1900">веилигхеидсаантал</span><span class="sxs-lookup"><span data-stu-id="5c862-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="5c862-1901">веилигхеидскоде</span><span class="sxs-lookup"><span data-stu-id="5c862-1901">veiligheidscode</span></span> 
- <span data-ttu-id="5c862-1902">веилигхеидснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="5c862-1903">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="5c862-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="5c862-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="5c862-1905">аблауф</span><span class="sxs-lookup"><span data-stu-id="5c862-1905">ablauf</span></span> 
- <span data-ttu-id="5c862-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="5c862-1906">data de expiracao</span></span> 
- <span data-ttu-id="5c862-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="5c862-1907">data de expiração</span></span> 
- <span data-ttu-id="5c862-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="5c862-1908">data del exp</span></span> 
- <span data-ttu-id="5c862-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="5c862-1909">data di exp</span></span> 
- <span data-ttu-id="5c862-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="5c862-1910">data di scadenza</span></span> 
- <span data-ttu-id="5c862-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="5c862-1911">data em que expira</span></span> 
- <span data-ttu-id="5c862-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="5c862-1912">data scad</span></span> 
- <span data-ttu-id="5c862-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="5c862-1913">data scadenza</span></span> 
- <span data-ttu-id="5c862-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="5c862-1914">date de validité</span></span> 
- <span data-ttu-id="5c862-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="5c862-1915">datum afloop</span></span> 
- <span data-ttu-id="5c862-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="5c862-1916">datum van exp</span></span> 
- <span data-ttu-id="5c862-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="5c862-1917">de afloop</span></span> 
- <span data-ttu-id="5c862-1918">еспира</span><span class="sxs-lookup"><span data-stu-id="5c862-1918">espira</span></span> 
- <span data-ttu-id="5c862-1919">еспира</span><span class="sxs-lookup"><span data-stu-id="5c862-1919">espira</span></span> 
- <span data-ttu-id="5c862-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="5c862-1920">exp date</span></span> 
- <span data-ttu-id="5c862-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="5c862-1921">exp datum</span></span> 
- <span data-ttu-id="5c862-1922">срока действия</span><span class="sxs-lookup"><span data-stu-id="5c862-1922">expiration</span></span> 
- <span data-ttu-id="5c862-1923">истекает</span><span class="sxs-lookup"><span data-stu-id="5c862-1923">expire</span></span> 
- <span data-ttu-id="5c862-1924">истекает</span><span class="sxs-lookup"><span data-stu-id="5c862-1924">expires</span></span> 
- <span data-ttu-id="5c862-1925">окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="5c862-1925">expiry</span></span> 
- <span data-ttu-id="5c862-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="5c862-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="5c862-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="5c862-1927">fecha de venc</span></span> 
- <span data-ttu-id="5c862-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="5c862-1928">gultig bis</span></span> 
- <span data-ttu-id="5c862-1929">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="5c862-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="5c862-1930">gültig bis</span></span> 
- <span data-ttu-id="5c862-1931">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="5c862-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="5c862-1932">la scadenza</span></span> 
- <span data-ttu-id="5c862-1933">скаденза</span><span class="sxs-lookup"><span data-stu-id="5c862-1933">scadenza</span></span> 
- <span data-ttu-id="5c862-1934">валабле</span><span class="sxs-lookup"><span data-stu-id="5c862-1934">valable</span></span> 
- <span data-ttu-id="5c862-1935">валидаде</span><span class="sxs-lookup"><span data-stu-id="5c862-1935">validade</span></span> 
- <span data-ttu-id="5c862-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="5c862-1936">valido hasta</span></span> 
- <span data-ttu-id="5c862-1937">валор</span><span class="sxs-lookup"><span data-stu-id="5c862-1937">valor</span></span> 
- <span data-ttu-id="5c862-1938">венк</span><span class="sxs-lookup"><span data-stu-id="5c862-1938">venc</span></span> 
- <span data-ttu-id="5c862-1939">венЦименто</span><span class="sxs-lookup"><span data-stu-id="5c862-1939">vencimento</span></span> 
- <span data-ttu-id="5c862-1940">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="5c862-1940">vencimiento</span></span> 
- <span data-ttu-id="5c862-1941">верлупт</span><span class="sxs-lookup"><span data-stu-id="5c862-1941">verloopt</span></span> 
- <span data-ttu-id="5c862-1942">вервалдаг</span><span class="sxs-lookup"><span data-stu-id="5c862-1942">vervaldag</span></span> 
- <span data-ttu-id="5c862-1943">вервалдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-1943">vervaldatum</span></span> 
- <span data-ttu-id="5c862-1944">вто</span><span class="sxs-lookup"><span data-stu-id="5c862-1944">vto</span></span> 
- <span data-ttu-id="5c862-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="5c862-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="5c862-1946">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="5c862-1946">EU Driver's License Number</span></span>

<span data-ttu-id="5c862-1947">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="5c862-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="5c862-1948">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="5c862-1948">EU National Identification Number</span></span>

<span data-ttu-id="5c862-1949">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационного номера ЕС](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="5c862-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="5c862-1950">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="5c862-1950">EU Passport Number</span></span>

<span data-ttu-id="5c862-1951">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="5c862-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="5c862-1952">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="5c862-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="5c862-1953">Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="5c862-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="5c862-1954">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="5c862-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="5c862-1955">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогового кода ЕС](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="5c862-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="5c862-1956">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="5c862-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1957">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1957">Format</span></span>

<span data-ttu-id="5c862-1958">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="5c862-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1959">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1959">Pattern</span></span>

<span data-ttu-id="5c862-1960">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="5c862-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="5c862-1961">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="5c862-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="5c862-1962">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="5c862-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="5c862-1963">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="5c862-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="5c862-1964">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1965">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1965">Checksum</span></span>

<span data-ttu-id="5c862-1966">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1967">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1967">Definition</span></span>

<span data-ttu-id="5c862-1968">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1969">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1970">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="5c862-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="5c862-1971">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-1971">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-1972">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1972">Keywords</span></span>

- <span data-ttu-id="5c862-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="5c862-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="5c862-1974">сосиаалитурватуннус</span><span class="sxs-lookup"><span data-stu-id="5c862-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="5c862-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="5c862-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="5c862-1976">персонбетеккнинг</span><span class="sxs-lookup"><span data-stu-id="5c862-1976">Personbeteckning</span></span>
- <span data-ttu-id="5c862-1977">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="5c862-1978">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="5c862-1978">Finland Passport Number</span></span>

<span data-ttu-id="5c862-1979">Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Regex_finland_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-1980">находится ключевое слово из Keyword_finland_passport_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="5c862-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="5c862-1981"></span></span>
<span data-ttu-id="5c862-1982">Ключевые слова Keyword_finland_passport_number Passport Пасси</span><span class="sxs-lookup"><span data-stu-id="5c862-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="5c862-1983">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="5c862-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-1984">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-1984">Format</span></span>

<span data-ttu-id="5c862-1985">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-1986">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-1986">Pattern</span></span>

<span data-ttu-id="5c862-1987">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="5c862-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-1988">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-1988">Checksum</span></span>

<span data-ttu-id="5c862-1989">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-1990">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-1990">Definition</span></span>

<span data-ttu-id="5c862-1991">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-1992">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-1993">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="5c862-1994">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="5c862-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="5c862-1995">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-1995">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-1996">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="5c862-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="5c862-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="5c862-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="5c862-1998">drivers licence</span></span>
- <span data-ttu-id="5c862-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="5c862-1999">drivers license</span></span>
- <span data-ttu-id="5c862-2000">driving licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2000">driving licence</span></span>
- <span data-ttu-id="5c862-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="5c862-2001">driving license</span></span>
- <span data-ttu-id="5c862-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="5c862-2002">permis de conduire</span></span>
- <span data-ttu-id="5c862-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="5c862-2003">licence number</span></span>
- <span data-ttu-id="5c862-2004">license number</span><span class="sxs-lookup"><span data-stu-id="5c862-2004">license number</span></span>
- <span data-ttu-id="5c862-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-2005">licence numbers</span></span>
- <span data-ttu-id="5c862-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="5c862-2007">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="5c862-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2008">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2008">Format</span></span>

<span data-ttu-id="5c862-2009">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2010">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2010">Pattern</span></span>

<span data-ttu-id="5c862-2011">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2012">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2012">Checksum</span></span>

<span data-ttu-id="5c862-2013">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2014">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2014">Definition</span></span>

<span data-ttu-id="5c862-2015">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2016">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2017">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2017">Keywords</span></span>

<span data-ttu-id="5c862-2018">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="5c862-2019">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="5c862-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2020">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2020">Format</span></span>

<span data-ttu-id="5c862-2021">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="5c862-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2022">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2022">Pattern</span></span>

<span data-ttu-id="5c862-2023">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="5c862-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="5c862-2024">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2024">Two digits</span></span> 
- <span data-ttu-id="5c862-2025">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-2026">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2027">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2027">Checksum</span></span>

<span data-ttu-id="5c862-2028">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2029">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2029">Definition</span></span>

<span data-ttu-id="5c862-2030">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2031">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2032">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="5c862-2032">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2033">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="5c862-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-2034">Keyword_passport</span></span>

- <span data-ttu-id="5c862-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2035">Passport Number</span></span>
- <span data-ttu-id="5c862-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="5c862-2036">Passport No</span></span>
- <span data-ttu-id="5c862-2037">Passport#</span><span class="sxs-lookup"><span data-stu-id="5c862-2037">Passport #</span></span>
- <span data-ttu-id="5c862-2038">Службу #</span><span class="sxs-lookup"><span data-stu-id="5c862-2038">Passport#</span></span>
- <span data-ttu-id="5c862-2039">пасспортид</span><span class="sxs-lookup"><span data-stu-id="5c862-2039">PassportID</span></span>
- <span data-ttu-id="5c862-2040">пасспортно</span><span class="sxs-lookup"><span data-stu-id="5c862-2040">Passportno</span></span>
- <span data-ttu-id="5c862-2041">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-2041">passportnumber</span></span>
- <span data-ttu-id="5c862-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="5c862-2042">パスポート</span></span>
- <span data-ttu-id="5c862-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2043">パスポート番号</span></span>
- <span data-ttu-id="5c862-2044">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="5c862-2044">パスポートのNum</span></span>
- <span data-ttu-id="5c862-2045">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="5c862-2045">パスポート ＃</span></span> 
- <span data-ttu-id="5c862-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="5c862-2046">Numéro de passeport</span></span>
- <span data-ttu-id="5c862-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="5c862-2047">Passeport n °</span></span>
- <span data-ttu-id="5c862-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="5c862-2048">Passeport Non</span></span>
- <span data-ttu-id="5c862-2049">Passeport#</span><span class="sxs-lookup"><span data-stu-id="5c862-2049">Passeport #</span></span>
- <span data-ttu-id="5c862-2050">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="5c862-2050">Passeport#</span></span>
- <span data-ttu-id="5c862-2051">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="5c862-2051">PasseportNon</span></span>
- <span data-ttu-id="5c862-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="5c862-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="5c862-2053">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="5c862-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2054">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2054">Format</span></span>

<span data-ttu-id="5c862-2055">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2056">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2056">Pattern</span></span>

<span data-ttu-id="5c862-2057">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="5c862-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="5c862-2058">13 цифр, за которыми следует пробел, за которым следуют две цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="5c862-2059">или</span><span class="sxs-lookup"><span data-stu-id="5c862-2059">or</span></span>
- <span data-ttu-id="5c862-2060">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2061">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2061">Checksum</span></span>

<span data-ttu-id="5c862-2062">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2063">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2063">Definition</span></span>

<span data-ttu-id="5c862-2064">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2065">Функция Func_french_insee или Func_fr_insee находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2066">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="5c862-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="5c862-2067">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2067">The checksum passes.</span></span>

<span data-ttu-id="5c862-2068">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2069">Функция Func_french_insee или Func_fr_insee находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2070">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="5c862-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="5c862-2071">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2071">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2072">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="5c862-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="5c862-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="5c862-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="5c862-2074">insee</span></span>
- <span data-ttu-id="5c862-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="5c862-2075">securité sociale</span></span>
- <span data-ttu-id="5c862-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="5c862-2076">securite sociale</span></span>
- <span data-ttu-id="5c862-2077">national id</span><span class="sxs-lookup"><span data-stu-id="5c862-2077">national id</span></span>
- <span data-ttu-id="5c862-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="5c862-2078">national identification</span></span>
- <span data-ttu-id="5c862-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="5c862-2079">numéro d'identité</span></span>
- <span data-ttu-id="5c862-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="5c862-2080">no d'identité</span></span>
- <span data-ttu-id="5c862-2081">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-2081">no.</span></span> <span data-ttu-id="5c862-2082">д'идентитé</span><span class="sxs-lookup"><span data-stu-id="5c862-2082">d'identité</span></span>
- <span data-ttu-id="5c862-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="5c862-2083">numero d'identite</span></span>
- <span data-ttu-id="5c862-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="5c862-2084">no d'identite</span></span>
- <span data-ttu-id="5c862-2085">Нет.</span><span class="sxs-lookup"><span data-stu-id="5c862-2085">no.</span></span> <span data-ttu-id="5c862-2086">д'идентите</span><span class="sxs-lookup"><span data-stu-id="5c862-2086">d'identite</span></span>
- <span data-ttu-id="5c862-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="5c862-2087">social security number</span></span>
- <span data-ttu-id="5c862-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="5c862-2088">social security code</span></span>
- <span data-ttu-id="5c862-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="5c862-2089">social insurance number</span></span>
- <span data-ttu-id="5c862-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="5c862-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="5c862-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="5c862-2091">d'identité nationale</span></span>
- <span data-ttu-id="5c862-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="5c862-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="5c862-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="5c862-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="5c862-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="5c862-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="5c862-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="5c862-2095">numéro de sécu</span></span>
- <span data-ttu-id="5c862-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="5c862-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="5c862-2097">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="5c862-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2098">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2098">Format</span></span>

<span data-ttu-id="5c862-2099">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="5c862-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2100">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2100">Pattern</span></span>

<span data-ttu-id="5c862-2101">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="5c862-2102">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="5c862-2102">A digit or letter</span></span> 
- <span data-ttu-id="5c862-2103">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2103">Two digits</span></span> 
- <span data-ttu-id="5c862-2104">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="5c862-2104">Six digits or letters</span></span> 
- <span data-ttu-id="5c862-2105">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="5c862-2105">A digit</span></span> 
- <span data-ttu-id="5c862-2106">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="5c862-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2107">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2107">Checksum</span></span>

<span data-ttu-id="5c862-2108">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2109">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2109">Definition</span></span>

<span data-ttu-id="5c862-2110">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2111">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2112">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="5c862-2113">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="5c862-2114">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="5c862-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="5c862-2115">найдено ключевое слово из Keyword_german_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="5c862-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="5c862-2116">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2116">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2117">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="5c862-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="5c862-2119">фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2119">Führerschein</span></span>
- <span data-ttu-id="5c862-2120">фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2120">Fuhrerschein</span></span>
- <span data-ttu-id="5c862-2121">фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2121">Fuehrerschein</span></span>
- <span data-ttu-id="5c862-2122">фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="5c862-2123">фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="5c862-2124">фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="5c862-2125">Фüхрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="5c862-2125">Führerschein-</span></span> 
- <span data-ttu-id="5c862-2126">Фухрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="5c862-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="5c862-2127">Фуехрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="5c862-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="5c862-2128">фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="5c862-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="5c862-2129">фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="5c862-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="5c862-2130">фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="5c862-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="5c862-2131">фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="5c862-2132">фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="5c862-2133">фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="5c862-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="5c862-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="5c862-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="5c862-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="5c862-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="5c862-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="5c862-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="5c862-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="5c862-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="5c862-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="5c862-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="5c862-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="5c862-2140">фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="5c862-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="5c862-2141">фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="5c862-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="5c862-2142">фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="5c862-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="5c862-2143">фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="5c862-2144">фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="5c862-2145">фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="5c862-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="5c862-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="5c862-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="5c862-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="5c862-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="5c862-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="5c862-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="5c862-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="5c862-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="5c862-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="5c862-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="5c862-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="5c862-2152">DL</span><span class="sxs-lookup"><span data-stu-id="5c862-2152">DL</span></span> 
- <span data-ttu-id="5c862-2153">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="5c862-2153">DLS</span></span>
- <span data-ttu-id="5c862-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-2154">Driv Lic</span></span> 
- <span data-ttu-id="5c862-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="5c862-2155">Driv Licen</span></span> 
- <span data-ttu-id="5c862-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="5c862-2156">Driv License</span></span>
- <span data-ttu-id="5c862-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2157">Driv Licenses</span></span> 
- <span data-ttu-id="5c862-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2158">Driv Licence</span></span> 
- <span data-ttu-id="5c862-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-2159">Driv Licences</span></span> 
- <span data-ttu-id="5c862-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-2160">Driv Lic</span></span> 
- <span data-ttu-id="5c862-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="5c862-2161">Driver Licen</span></span> 
- <span data-ttu-id="5c862-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="5c862-2162">Driver License</span></span> 
- <span data-ttu-id="5c862-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2163">Driver Licenses</span></span> 
- <span data-ttu-id="5c862-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2164">Driver Licence</span></span> 
- <span data-ttu-id="5c862-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-2165">Driver Licences</span></span> 
- <span data-ttu-id="5c862-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-2166">Drivers Lic</span></span> 
- <span data-ttu-id="5c862-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="5c862-2167">Drivers Licen</span></span> 
- <span data-ttu-id="5c862-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="5c862-2168">Drivers License</span></span> 
- <span data-ttu-id="5c862-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="5c862-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2170">Drivers Licence</span></span> 
- <span data-ttu-id="5c862-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-2171">Drivers Licences</span></span> 
- <span data-ttu-id="5c862-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-2172">Driver's Lic</span></span> 
- <span data-ttu-id="5c862-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="5c862-2173">Driver's Licen</span></span> 
- <span data-ttu-id="5c862-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="5c862-2174">Driver's License</span></span> 
- <span data-ttu-id="5c862-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="5c862-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2176">Driver's Licence</span></span> 
- <span data-ttu-id="5c862-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-2177">Driver's Licences</span></span> 
- <span data-ttu-id="5c862-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-2178">Driving Lic</span></span> 
- <span data-ttu-id="5c862-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="5c862-2179">Driving Licen</span></span> 
- <span data-ttu-id="5c862-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="5c862-2180">Driving License</span></span> 
- <span data-ttu-id="5c862-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2181">Driving Licenses</span></span> 
- <span data-ttu-id="5c862-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2182">Driving Licence</span></span> 
- <span data-ttu-id="5c862-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="5c862-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="5c862-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="5c862-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="5c862-2185">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="5c862-2186">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="5c862-2187">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="5c862-2188">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2188">No-Führerschein</span></span> 
- <span data-ttu-id="5c862-2189">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="5c862-2190">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="5c862-2191">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2191">N-Führerschein</span></span> 
- <span data-ttu-id="5c862-2192">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="5c862-2193">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="5c862-2194">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="5c862-2195">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="5c862-2196">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="5c862-2197">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2197">No-Führerschein</span></span> 
- <span data-ttu-id="5c862-2198">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="5c862-2199">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="5c862-2200">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2200">N-Führerschein</span></span> 
- <span data-ttu-id="5c862-2201">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="5c862-2202">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="5c862-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="5c862-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="5c862-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="5c862-2204">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="5c862-2205">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="5c862-2205">ausstellungsort</span></span>
- <span data-ttu-id="5c862-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="5c862-2206">ausstellende behöde</span></span>
- <span data-ttu-id="5c862-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="5c862-2207">ausstellende behorde</span></span>
- <span data-ttu-id="5c862-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="5c862-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="5c862-2209">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="5c862-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2210">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2210">Format</span></span>

<span data-ttu-id="5c862-2211">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="5c862-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2212">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2212">Pattern</span></span>

<span data-ttu-id="5c862-2213">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="5c862-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="5c862-2214">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="5c862-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="5c862-2215">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2215">Three digits</span></span> 
- <span data-ttu-id="5c862-2216">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="5c862-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="5c862-2217">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="5c862-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2218">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2218">Checksum</span></span>

<span data-ttu-id="5c862-2219">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2220">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2220">Definition</span></span>

<span data-ttu-id="5c862-2221">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2222">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2223">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="5c862-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="5c862-2224">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2224">The checksum passes.</span></span>

<span data-ttu-id="5c862-2225">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2226">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2227">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="5c862-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="5c862-2228">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2228">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2229">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="5c862-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="5c862-2231">реисепасс</span><span class="sxs-lookup"><span data-stu-id="5c862-2231">reisepass</span></span>
- <span data-ttu-id="5c862-2232">реисепассе</span><span class="sxs-lookup"><span data-stu-id="5c862-2232">reisepasse</span></span>
- <span data-ttu-id="5c862-2233">реисепасснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2233">reisepassnummer</span></span>
- <span data-ttu-id="5c862-2234">службу</span><span class="sxs-lookup"><span data-stu-id="5c862-2234">passport</span></span>
- <span data-ttu-id="5c862-2235">паспорты</span><span class="sxs-lookup"><span data-stu-id="5c862-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="5c862-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="5c862-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="5c862-2237">жебуртсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-2237">geburtsdatum</span></span>
- <span data-ttu-id="5c862-2238">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="5c862-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="5c862-2239">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="5c862-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="5c862-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="5c862-2241">No — Реисепасс НР — Реисепасс</span><span class="sxs-lookup"><span data-stu-id="5c862-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="5c862-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="5c862-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="5c862-2243">Реисепасс — НР</span><span class="sxs-lookup"><span data-stu-id="5c862-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="5c862-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="5c862-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="5c862-2245">бнатионалит. t</span><span class="sxs-lookup"><span data-stu-id="5c862-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="5c862-2246">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="5c862-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2247">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2247">Format</span></span>

<span data-ttu-id="5c862-2248">С 1 ноября 2010: девять букв и цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="5c862-2249">От 1 апреля 1987 до 31 октября 2010:10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2250">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2250">Pattern</span></span>

<span data-ttu-id="5c862-2251">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="5c862-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="5c862-2252">одна буква (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-2253">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2253">Eight digits</span></span>

<span data-ttu-id="5c862-2254">От 1 апреля 1987 до 31 октября 2010:</span><span class="sxs-lookup"><span data-stu-id="5c862-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="5c862-2255">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2256">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2256">Checksum</span></span>

<span data-ttu-id="5c862-2257">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2258">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2258">Definition</span></span>

<span data-ttu-id="5c862-2259">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2260">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2261">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="5c862-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2262">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="5c862-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="5c862-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="5c862-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="5c862-2264">Identity Card</span></span>
- <span data-ttu-id="5c862-2265">ID</span><span class="sxs-lookup"><span data-stu-id="5c862-2265">ID</span></span>
- <span data-ttu-id="5c862-2266">Процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-2266">Identification</span></span>
- <span data-ttu-id="5c862-2267">персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="5c862-2267">Personalausweis</span></span>
- <span data-ttu-id="5c862-2268">идентифизиерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="5c862-2269">аусвеис</span><span class="sxs-lookup"><span data-stu-id="5c862-2269">Ausweis</span></span>
- <span data-ttu-id="5c862-2270">идентификатион</span><span class="sxs-lookup"><span data-stu-id="5c862-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="5c862-2271">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="5c862-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2272">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2272">Format</span></span>

<span data-ttu-id="5c862-2273">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="5c862-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2274">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2274">Pattern</span></span>

<span data-ttu-id="5c862-2275">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="5c862-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="5c862-2276">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="5c862-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="5c862-2277">тире;</span><span class="sxs-lookup"><span data-stu-id="5c862-2277">A dash</span></span> 
- <span data-ttu-id="5c862-2278">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2278">Six digits</span></span>

<span data-ttu-id="5c862-2279">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="5c862-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="5c862-2280">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="5c862-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="5c862-2281">тире;</span><span class="sxs-lookup"><span data-stu-id="5c862-2281">A dash</span></span> 
- <span data-ttu-id="5c862-2282">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2283">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2283">Checksum</span></span>

<span data-ttu-id="5c862-2284">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2285">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2285">Definition</span></span>

<span data-ttu-id="5c862-2286">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2287">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2288">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="5c862-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2289">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="5c862-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="5c862-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="5c862-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="5c862-2291">Greek identity Card</span></span>
- <span data-ttu-id="5c862-2292">таутотита</span><span class="sxs-lookup"><span data-stu-id="5c862-2292">Tautotita</span></span>
- <span data-ttu-id="5c862-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="5c862-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="5c862-2294">ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="5c862-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="5c862-2295">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="5c862-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2296">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2296">Format</span></span>

<span data-ttu-id="5c862-2297">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="5c862-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2298">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2298">Pattern</span></span>

<span data-ttu-id="5c862-2299">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="5c862-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="5c862-2300">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-2301">шесть цифр; </span><span class="sxs-lookup"><span data-stu-id="5c862-2301">Six digits</span></span> 
- <span data-ttu-id="5c862-2302">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="5c862-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2303">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2303">Checksum</span></span>

<span data-ttu-id="5c862-2304">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2305">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2305">Definition</span></span>

<span data-ttu-id="5c862-2306">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2307">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2308">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="5c862-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="5c862-2309">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2309">The checksum passes.</span></span>

<span data-ttu-id="5c862-2310">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2311">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2312">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2312">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2313">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="5c862-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="5c862-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="5c862-2315">идентификационная карточка Гонконг</span><span class="sxs-lookup"><span data-stu-id="5c862-2315">hong kong identity card</span></span>
- <span data-ttu-id="5c862-2316">хкидк</span><span class="sxs-lookup"><span data-stu-id="5c862-2316">HKIDC</span></span>
- <span data-ttu-id="5c862-2317">id card</span><span class="sxs-lookup"><span data-stu-id="5c862-2317">id card</span></span>
- <span data-ttu-id="5c862-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="5c862-2318">identity card</span></span>
- <span data-ttu-id="5c862-2319">идентификационная карточка HK</span><span class="sxs-lookup"><span data-stu-id="5c862-2319">hk identity card</span></span>
- <span data-ttu-id="5c862-2320">Идентификатор Гонконг</span><span class="sxs-lookup"><span data-stu-id="5c862-2320">hong kong id</span></span>
- <span data-ttu-id="5c862-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2321">香港身份證</span></span>
- <span data-ttu-id="5c862-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="5c862-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2323">身份證</span></span>
- <span data-ttu-id="5c862-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2324">身份証</span></span>
- <span data-ttu-id="5c862-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2325">身分證</span></span>
- <span data-ttu-id="5c862-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2326">身分証</span></span>
- <span data-ttu-id="5c862-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2327">香港身份証</span></span>
- <span data-ttu-id="5c862-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2328">香港身分證</span></span>
- <span data-ttu-id="5c862-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2329">香港身分証</span></span>
- <span data-ttu-id="5c862-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2330">香港身份證</span></span>
- <span data-ttu-id="5c862-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2331">香港居民身份證</span></span>
- <span data-ttu-id="5c862-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2332">香港居民身份証</span></span>
- <span data-ttu-id="5c862-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2333">香港居民身分證</span></span>
- <span data-ttu-id="5c862-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2334">香港居民身分証</span></span>
- <span data-ttu-id="5c862-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="5c862-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="5c862-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="5c862-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="5c862-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="5c862-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="5c862-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="5c862-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="5c862-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="5c862-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="5c862-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="5c862-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="5c862-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="5c862-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="5c862-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="5c862-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="5c862-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="5c862-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="5c862-2351">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="5c862-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2352">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2352">Format</span></span>

<span data-ttu-id="5c862-2353">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2354">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2354">Pattern</span></span>

<span data-ttu-id="5c862-2355">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2355">10 letters or digits:</span></span>
- <span data-ttu-id="5c862-2356">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-2357">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2357">Four digits</span></span> 
- <span data-ttu-id="5c862-2358">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="5c862-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2359">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2359">Checksum</span></span>

<span data-ttu-id="5c862-2360">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2361">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2361">Definition</span></span>

<span data-ttu-id="5c862-2362">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2363">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2364">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="5c862-2365">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2365">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2366">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="5c862-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="5c862-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="5c862-2369">ПАНОРАМИРОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c862-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="5c862-2370">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="5c862-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2371">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2371">Format</span></span>

<span data-ttu-id="5c862-2372">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="5c862-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2373">Pattern</span></span>

<span data-ttu-id="5c862-2374">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2374">12 digits:</span></span>
- <span data-ttu-id="5c862-2375">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-2375">Four digits</span></span> 
- <span data-ttu-id="5c862-2376">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="5c862-2376">An optional space or dash</span></span> 
- <span data-ttu-id="5c862-2377">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-2377">Four digits</span></span> 
- <span data-ttu-id="5c862-2378">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="5c862-2378">An optional space or dash</span></span> 
- <span data-ttu-id="5c862-2379">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="5c862-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2380">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2380">Checksum</span></span>

<span data-ttu-id="5c862-2381">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2382">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2382">Definition</span></span>

<span data-ttu-id="5c862-2383">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_india_aadhaar находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-2384">находится ключевое слово из Keyword_india_aadhar;</span><span class="sxs-lookup"><span data-stu-id="5c862-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="5c862-2385">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2385">The checksum passes.</span></span>
<span data-ttu-id="5c862-2386">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_india_aadhaar находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-2387">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2387">The checksum passes.</span></span>
<!-- India Unique Identification (Aadhaar) number -->
<span data-ttu-id="5c862-2388"><Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="5c862-2388"></span></span>

### <a name="keywords"></a><span data-ttu-id="5c862-2389">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2389">Keywords</span></span>
   
#### <a name="keyword_india_aadhar"></a><span data-ttu-id="5c862-2390">Keyword_india_aadhar</span><span class="sxs-lookup"><span data-stu-id="5c862-2390">Keyword_india_aadhar</span></span>
- <span data-ttu-id="5c862-2391">аадхар</span><span class="sxs-lookup"><span data-stu-id="5c862-2391">Aadhar</span></span>
- <span data-ttu-id="5c862-2392">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="5c862-2392">Aadhaar</span></span>
- <span data-ttu-id="5c862-2393">UID</span><span class="sxs-lookup"><span data-stu-id="5c862-2393">UID</span></span>
- <span data-ttu-id="5c862-2394">आधार</span><span class="sxs-lookup"><span data-stu-id="5c862-2394">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="5c862-2395">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="5c862-2395">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2396">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2396">Format</span></span>

<span data-ttu-id="5c862-2397">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="5c862-2397">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2398">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2398">Pattern</span></span>

<span data-ttu-id="5c862-2399">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2399">16 digits:</span></span>
- <span data-ttu-id="5c862-2400">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="5c862-2400">Two-digit province code</span></span> 
- <span data-ttu-id="5c862-2401">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="5c862-2401">A period (optional)</span></span> 
- <span data-ttu-id="5c862-2402">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="5c862-2402">Two-digit regency or city code</span></span> 
- <span data-ttu-id="5c862-2403">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="5c862-2403">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="5c862-2404">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="5c862-2404">A period (optional)</span></span> 
- <span data-ttu-id="5c862-2405">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="5c862-2405">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="5c862-2406">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="5c862-2406">A period (optional)</span></span> 
- <span data-ttu-id="5c862-2407">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-2407">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2408">Checksum</span></span>

<span data-ttu-id="5c862-2409">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2409">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2410">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2410">Definition</span></span>

<span data-ttu-id="5c862-2411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2412">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2412">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2413">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="5c862-2413">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="5c862-2414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2415">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2415">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2416">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2416">Keywords</span></span>
   
#### <a name="keyword_indonesia_id_card"></a><span data-ttu-id="5c862-2417">Keyword_indonesia_id_card</span><span class="sxs-lookup"><span data-stu-id="5c862-2417">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="5c862-2418">KTP</span><span class="sxs-lookup"><span data-stu-id="5c862-2418">KTP</span></span>
- <span data-ttu-id="5c862-2419">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="5c862-2419">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="5c862-2420">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="5c862-2420">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="5c862-2421">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="5c862-2421">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2422">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2422">Format</span></span>

<span data-ttu-id="5c862-2423">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="5c862-2423">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2424">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2424">Pattern</span></span>

<span data-ttu-id="5c862-2425">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="5c862-2425">Pattern must include all of the following:</span></span>

- <span data-ttu-id="5c862-2426">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="5c862-2426">Two-letter country code</span></span>
- <span data-ttu-id="5c862-2427">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="5c862-2427">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="5c862-2428">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="5c862-2428">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="5c862-2429">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2429">1-3 letters or digits</span></span>

<span data-ttu-id="5c862-p135">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="5c862-p135">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="5c862-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="5c862-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2433">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2433">Checksum</span></span>

<span data-ttu-id="5c862-2434">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2435">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2435">Definition</span></span>

<span data-ttu-id="5c862-2436">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2437">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2437">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2438">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2438">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2439">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2439">Keywords</span></span>

<span data-ttu-id="5c862-2440">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2440">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="5c862-2441">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="5c862-2441">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2442">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2442">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="5c862-2443">IPv4</span><span class="sxs-lookup"><span data-stu-id="5c862-2443">IPv4:</span></span>
<span data-ttu-id="5c862-2444">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="5c862-2444">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="5c862-2445">Поддерживающ</span><span class="sxs-lookup"><span data-stu-id="5c862-2445">IPv6:</span></span>
<span data-ttu-id="5c862-2446"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="5c862-2446">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2447">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2447">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2448">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2448">Checksum</span></span>

<span data-ttu-id="5c862-2449">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2449">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2450">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2450">Definition</span></span>

<span data-ttu-id="5c862-2451">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2451">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2452">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2452">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2453">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="5c862-2453">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="5c862-2454">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2454">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2455">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2455">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2456">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="5c862-2456">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="5c862-2457">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2457">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2458">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2458">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2459">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="5c862-2459">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2460">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="5c862-2461">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="5c862-2461">Keyword_ipaddress</span></span>

- <span data-ttu-id="5c862-2462">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-2462">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="5c862-2463">ip address</span><span class="sxs-lookup"><span data-stu-id="5c862-2463">ip address</span></span> 
- <span data-ttu-id="5c862-2464">ip addresses</span><span class="sxs-lookup"><span data-stu-id="5c862-2464">ip addresses</span></span>
- <span data-ttu-id="5c862-2465">internet protocol</span><span class="sxs-lookup"><span data-stu-id="5c862-2465">internet protocol</span></span>
- <span data-ttu-id="5c862-2466">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="5c862-2466">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="5c862-2467">Международная классификация Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="5c862-2467">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2468">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2468">Format</span></span>

<span data-ttu-id="5c862-2469">Dictionary</span><span class="sxs-lookup"><span data-stu-id="5c862-2469">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2470">Pattern</span></span>

<span data-ttu-id="5c862-2471">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="5c862-2471">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2472">Checksum</span></span>

<span data-ttu-id="5c862-2473">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2474">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2474">Definition</span></span>

<span data-ttu-id="5c862-2475">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2476">Найдено ключевое слово из Dictionary_icd_10_cm.</span><span class="sxs-lookup"><span data-stu-id="5c862-2476">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="5c862-2477">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2477">Keywords</span></span>

<span data-ttu-id="5c862-2478">Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятой редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="5c862-2478">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="5c862-2479">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="5c862-2479">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="5c862-2480">Международная классификация Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="5c862-2480">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2481">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2481">Format</span></span>

<span data-ttu-id="5c862-2482">Dictionary</span><span class="sxs-lookup"><span data-stu-id="5c862-2482">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2483">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2483">Pattern</span></span>

<span data-ttu-id="5c862-2484">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="5c862-2484">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2485">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2485">Checksum</span></span>

<span data-ttu-id="5c862-2486">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2486">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2487">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2487">Definition</span></span>

<span data-ttu-id="5c862-2488">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2488">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2489">Найдено ключевое слово из Dictionary_icd_9_cm.</span><span class="sxs-lookup"><span data-stu-id="5c862-2489">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2490">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2490">Keywords</span></span>

<span data-ttu-id="5c862-2491">Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятой редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="5c862-2491">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="5c862-2492">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="5c862-2492">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="5c862-2493">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="5c862-2493">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2494">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2494">Format</span></span>

<span data-ttu-id="5c862-2495">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="5c862-2495">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="5c862-2496">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="5c862-2496">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="5c862-2497">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="5c862-2497">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="5c862-2498">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="5c862-2498">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2499">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2499">Pattern</span></span>

<span data-ttu-id="5c862-2500">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="5c862-2500">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="5c862-2501">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-2501">Seven digits</span></span> 
- <span data-ttu-id="5c862-2502">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="5c862-2502">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="5c862-2503">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="5c862-2503">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="5c862-2504">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-2504">Seven digits</span></span> 
- <span data-ttu-id="5c862-2505">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="5c862-2505">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="5c862-2506">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="5c862-2506">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2507">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2507">Checksum</span></span>

<span data-ttu-id="5c862-2508">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2508">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2509">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2509">Definition</span></span>

<span data-ttu-id="5c862-2510">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2511">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2511">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2512">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-2512">One of the following is true:</span></span>
    - <span data-ttu-id="5c862-2513">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="5c862-2513">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="5c862-2514">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-2514">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="5c862-2515">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2515">The checksum passes.</span></span>

<span data-ttu-id="5c862-2516">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2516">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2517">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2517">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2518">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2518">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2519">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2519">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="5c862-2520">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="5c862-2520">Keyword_ireland_pps</span></span>

- <span data-ttu-id="5c862-2521">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2521">Personal Public Service Number</span></span> 
- <span data-ttu-id="5c862-2522">PPS Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2522">PPS Number</span></span> 
- <span data-ttu-id="5c862-2523">PPS Num</span><span class="sxs-lookup"><span data-stu-id="5c862-2523">PPS Num</span></span> 
- <span data-ttu-id="5c862-2524">PPS No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2524">PPS No.</span></span> 
- <span data-ttu-id="5c862-2525">PPS #</span><span class="sxs-lookup"><span data-stu-id="5c862-2525">PPS #</span></span> 
- <span data-ttu-id="5c862-2526">PPS #</span><span class="sxs-lookup"><span data-stu-id="5c862-2526">PPS#</span></span> 
- <span data-ttu-id="5c862-2527">ппсн</span><span class="sxs-lookup"><span data-stu-id="5c862-2527">PPSN</span></span> 
- <span data-ttu-id="5c862-2528">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="5c862-2528">Public Services Card</span></span> 
- <span data-ttu-id="5c862-2529">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="5c862-2529">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="5c862-2530">Уимх.</span><span class="sxs-lookup"><span data-stu-id="5c862-2530">Uimh.</span></span> <span data-ttu-id="5c862-2531">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="5c862-2531">PSP</span></span> 
- <span data-ttu-id="5c862-2532">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="5c862-2532">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="5c862-2533">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="5c862-2533">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2534">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2534">Format</span></span>

<span data-ttu-id="5c862-2535">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2535">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2536">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2536">Pattern</span></span>

<span data-ttu-id="5c862-2537">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="5c862-2537">Formatted:</span></span>
- <span data-ttu-id="5c862-2538">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2538">Two digits</span></span> 
- <span data-ttu-id="5c862-2539">Тире</span><span class="sxs-lookup"><span data-stu-id="5c862-2539">A dash</span></span> 
- <span data-ttu-id="5c862-2540">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2540">Three digits</span></span> 
- <span data-ttu-id="5c862-2541">Тире</span><span class="sxs-lookup"><span data-stu-id="5c862-2541">A dash</span></span> 
- <span data-ttu-id="5c862-2542">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-2542">Eight digits</span></span>

<span data-ttu-id="5c862-2543">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="5c862-2543">Unformatted:</span></span>
- <span data-ttu-id="5c862-2544">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2544">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2545">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2545">Checksum</span></span>

<span data-ttu-id="5c862-2546">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2546">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2547">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2547">Definition</span></span>

<span data-ttu-id="5c862-2548">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2548">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2549">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2549">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2550">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-2550">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2551">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2551">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="5c862-2552">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2552">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="5c862-2553">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2553">Bank Account Number</span></span> 
- <span data-ttu-id="5c862-2554">Bank Account</span><span class="sxs-lookup"><span data-stu-id="5c862-2554">Bank Account</span></span> 
- <span data-ttu-id="5c862-2555">Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2555">Account Number</span></span> 
- <span data-ttu-id="5c862-2556">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="5c862-2556">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="5c862-2557">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="5c862-2557">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2558">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2558">Format</span></span>

<span data-ttu-id="5c862-2559">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2559">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2560">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2560">Pattern</span></span>

<span data-ttu-id="5c862-2561">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2561">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2562">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2562">Checksum</span></span>

<span data-ttu-id="5c862-2563">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2563">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2564">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2564">Definition</span></span>

<span data-ttu-id="5c862-2565">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2565">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2566">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2566">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2567">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="5c862-2567">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="5c862-2568">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2568">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2569">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2569">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="5c862-2570">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="5c862-2570">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="5c862-2571">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="5c862-2571">מספר זהות</span></span> 
- <span data-ttu-id="5c862-2572">National ID Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2572">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="5c862-2573">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="5c862-2573">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2574">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2574">Format</span></span>

<span data-ttu-id="5c862-2575">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2575">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2576">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2576">Pattern</span></span>

- <span data-ttu-id="5c862-2577">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2577">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="5c862-2578">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-2578">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-2579">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-2579">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-2580">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="5c862-2580">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="5c862-2581">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-2581">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2582">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2582">Checksum</span></span>

<span data-ttu-id="5c862-2583">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2583">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2584">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2584">Definition</span></span>

<span data-ttu-id="5c862-2585">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2586">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2586">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2587">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-2587">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2588">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2588">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="5c862-2589">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2589">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="5c862-2590">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="5c862-2590">numero di patente di guida</span></span> 
- <span data-ttu-id="5c862-2591">patente di guida</span><span class="sxs-lookup"><span data-stu-id="5c862-2591">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="5c862-2592">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="5c862-2592">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2593">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2593">Format</span></span>

<span data-ttu-id="5c862-2594">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2594">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2595">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2595">Pattern</span></span>

<span data-ttu-id="5c862-2596">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="5c862-2596">Bank account number:</span></span>
- <span data-ttu-id="5c862-2597">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2597">Seven or eight digits</span></span>
- <span data-ttu-id="5c862-2598">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="5c862-2598">Bank account branch code:</span></span>
- <span data-ttu-id="5c862-2599">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2599">Four digits</span></span> 
- <span data-ttu-id="5c862-2600">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5c862-2600">A space or dash (optional)</span></span> 
- <span data-ttu-id="5c862-2601">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2601">Three digits</span></span>

<span data-ttu-id="5c862-2602">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2602">Checksum</span></span>

<span data-ttu-id="5c862-2603">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2603">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2604">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2604">Definition</span></span>

<span data-ttu-id="5c862-2605">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2605">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2606">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-2606">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2607">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="5c862-2607">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="5c862-2608">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-2608">One of the following is true:</span></span>
- <span data-ttu-id="5c862-2609">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2609">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2610">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="5c862-2610">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="5c862-2611">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2611">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2612">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2612">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2613">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="5c862-2613">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2614">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2614">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="5c862-2615">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="5c862-2615">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="5c862-2616">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2616">Checking Account Number</span></span> 
- <span data-ttu-id="5c862-2617">Checking Account</span><span class="sxs-lookup"><span data-stu-id="5c862-2617">Checking Account</span></span> 
- <span data-ttu-id="5c862-2618">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-2618">Checking Account #</span></span> 
- <span data-ttu-id="5c862-2619">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2619">Checking Acct Number</span></span> 
- <span data-ttu-id="5c862-2620">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-2620">Checking Acct #</span></span> 
- <span data-ttu-id="5c862-2621">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2621">Checking Acct No.</span></span> 
- <span data-ttu-id="5c862-2622">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2622">Checking Account No.</span></span> 
- <span data-ttu-id="5c862-2623">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2623">Bank Account Number</span></span> 
- <span data-ttu-id="5c862-2624">Bank Account</span><span class="sxs-lookup"><span data-stu-id="5c862-2624">Bank Account</span></span> 
- <span data-ttu-id="5c862-2625">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-2625">Bank Account #</span></span> 
- <span data-ttu-id="5c862-2626">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2626">Bank Acct Number</span></span> 
- <span data-ttu-id="5c862-2627">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-2627">Bank Acct #</span></span> 
- <span data-ttu-id="5c862-2628">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2628">Bank Acct No.</span></span> 
- <span data-ttu-id="5c862-2629">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2629">Bank Account No.</span></span> 
- <span data-ttu-id="5c862-2630">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2630">Savings Account Number</span></span> 
- <span data-ttu-id="5c862-2631">Savings Account</span><span class="sxs-lookup"><span data-stu-id="5c862-2631">Savings Account</span></span> 
- <span data-ttu-id="5c862-2632">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-2632">Savings Account #</span></span> 
- <span data-ttu-id="5c862-2633">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2633">Savings Acct Number</span></span> 
- <span data-ttu-id="5c862-2634">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-2634">Savings Acct #</span></span> 
- <span data-ttu-id="5c862-2635">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2635">Savings Acct No.</span></span> 
- <span data-ttu-id="5c862-2636">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2636">Savings Account No.</span></span> 
- <span data-ttu-id="5c862-2637">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2637">Debit Account Number</span></span> 
- <span data-ttu-id="5c862-2638">Debit Account</span><span class="sxs-lookup"><span data-stu-id="5c862-2638">Debit Account</span></span> 
- <span data-ttu-id="5c862-2639">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-2639">Debit Account #</span></span> 
- <span data-ttu-id="5c862-2640">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2640">Debit Acct Number</span></span> 
- <span data-ttu-id="5c862-2641">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-2641">Debit Acct #</span></span> 
- <span data-ttu-id="5c862-2642">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2642">Debit Acct No.</span></span> 
- <span data-ttu-id="5c862-2643">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2643">Debit Account No.</span></span> 
- <span data-ttu-id="5c862-2644">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="5c862-2644">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="5c862-2645">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="5c862-2645">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="5c862-2646">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="5c862-2646">＃勘定の確認</span></span> 
- <span data-ttu-id="5c862-2647">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="5c862-2647">勘定番号の確認</span></span> 
- <span data-ttu-id="5c862-2648">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="5c862-2648">口座番号の確認</span></span> 
- <span data-ttu-id="5c862-2649">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2649">銀行口座番号</span></span> 
- <span data-ttu-id="5c862-2650">銀行口座</span><span class="sxs-lookup"><span data-stu-id="5c862-2650">銀行口座</span></span> 
- <span data-ttu-id="5c862-2651">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="5c862-2651">銀行口座＃</span></span> 
- <span data-ttu-id="5c862-2652">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2652">銀行の勘定番号</span></span> 
- <span data-ttu-id="5c862-2653">銀行のаккт #</span><span class="sxs-lookup"><span data-stu-id="5c862-2653">銀行のacct＃</span></span> 
- <span data-ttu-id="5c862-2654">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="5c862-2654">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="5c862-2655">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2655">銀行口座番号</span></span>
- <span data-ttu-id="5c862-2656">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2656">普通預金口座番号</span></span> 
- <span data-ttu-id="5c862-2657">預金口座</span><span class="sxs-lookup"><span data-stu-id="5c862-2657">預金口座</span></span> 
- <span data-ttu-id="5c862-2658">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="5c862-2658">貯蓄口座＃</span></span> 
- <span data-ttu-id="5c862-2659">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="5c862-2659">貯蓄勘定の数</span></span> 
- <span data-ttu-id="5c862-2660">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="5c862-2660">貯蓄勘定＃</span></span> 
- <span data-ttu-id="5c862-2661">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2661">貯蓄勘定番号</span></span> 
- <span data-ttu-id="5c862-2662">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2662">普通預金口座番号</span></span> 
- <span data-ttu-id="5c862-2663">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2663">引き落とし口座番号</span></span> 
- <span data-ttu-id="5c862-2664">口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2664">口座番号</span></span> 
- <span data-ttu-id="5c862-2665">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="5c862-2665">口座番号＃</span></span> 
- <span data-ttu-id="5c862-2666">デビットのаккт番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2666">デビットのacct番号</span></span> 
- <span data-ttu-id="5c862-2667">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="5c862-2667">デビット勘定＃</span></span> 
- <span data-ttu-id="5c862-2668">デビットакктの番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2668">デビットACCTの番号</span></span> 
- <span data-ttu-id="5c862-2669">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2669">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="5c862-2670">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="5c862-2670">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="5c862-2671">отемачи</span><span class="sxs-lookup"><span data-stu-id="5c862-2671">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="5c862-2672">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="5c862-2672">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2673">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2673">Format</span></span>

<span data-ttu-id="5c862-2674">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2674">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2675">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2675">Pattern</span></span>

<span data-ttu-id="5c862-2676">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2676">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2677">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2677">Checksum</span></span>

<span data-ttu-id="5c862-2678">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2678">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2679">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2679">Definition</span></span>

<span data-ttu-id="5c862-2680">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2681">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2681">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2682">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-2682">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2683">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2683">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="5c862-2684">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2684">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="5c862-2685">DL #</span><span class="sxs-lookup"><span data-stu-id="5c862-2685">dl#</span></span> 
- <span data-ttu-id="5c862-2686">DL</span><span class="sxs-lookup"><span data-stu-id="5c862-2686">DL＃</span></span> 
- <span data-ttu-id="5c862-2687">библиотек #</span><span class="sxs-lookup"><span data-stu-id="5c862-2687">dls#</span></span> 
- <span data-ttu-id="5c862-2688">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="5c862-2688">DLS＃</span></span> 
- <span data-ttu-id="5c862-2689">driver license</span><span class="sxs-lookup"><span data-stu-id="5c862-2689">driver license</span></span> 
- <span data-ttu-id="5c862-2690">driver licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2690">driver licenses</span></span> 
- <span data-ttu-id="5c862-2691">drivers license</span><span class="sxs-lookup"><span data-stu-id="5c862-2691">drivers license</span></span> 
- <span data-ttu-id="5c862-2692">driver's license</span><span class="sxs-lookup"><span data-stu-id="5c862-2692">driver's license</span></span> 
- <span data-ttu-id="5c862-2693">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2693">drivers licenses</span></span> 
- <span data-ttu-id="5c862-2694">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-2694">driver's licenses</span></span> 
- <span data-ttu-id="5c862-2695">driving licence</span><span class="sxs-lookup"><span data-stu-id="5c862-2695">driving licence</span></span> 
- <span data-ttu-id="5c862-2696">лик #</span><span class="sxs-lookup"><span data-stu-id="5c862-2696">lic#</span></span> 
- <span data-ttu-id="5c862-2697">Лик #</span><span class="sxs-lookup"><span data-stu-id="5c862-2697">LIC＃</span></span> 
- <span data-ttu-id="5c862-2698">ликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-2698">lics#</span></span> 
- <span data-ttu-id="5c862-2699">state id</span><span class="sxs-lookup"><span data-stu-id="5c862-2699">state id</span></span> 
- <span data-ttu-id="5c862-2700">state identification</span><span class="sxs-lookup"><span data-stu-id="5c862-2700">state identification</span></span> 
- <span data-ttu-id="5c862-2701">state identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-2701">state identification number</span></span> 
- <span data-ttu-id="5c862-2702">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="5c862-2702">低所得国＃</span></span> 
- <span data-ttu-id="5c862-2703">免許証</span><span class="sxs-lookup"><span data-stu-id="5c862-2703">免許証</span></span> 
- <span data-ttu-id="5c862-2704">状態ид</span><span class="sxs-lookup"><span data-stu-id="5c862-2704">状態ID</span></span>
- <span data-ttu-id="5c862-2705">状態の識別</span><span class="sxs-lookup"><span data-stu-id="5c862-2705">状態の識別</span></span> 
- <span data-ttu-id="5c862-2706">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2706">状態の識別番号</span></span> 
- <span data-ttu-id="5c862-2707">運転免許</span><span class="sxs-lookup"><span data-stu-id="5c862-2707">運転免許</span></span> 
- <span data-ttu-id="5c862-2708">運転免許証</span><span class="sxs-lookup"><span data-stu-id="5c862-2708">運転免許証</span></span> 
- <span data-ttu-id="5c862-2709">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2709">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="5c862-2710">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="5c862-2710">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2711">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2711">Format</span></span>

<span data-ttu-id="5c862-2712">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2712">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2713">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2713">Pattern</span></span>

<span data-ttu-id="5c862-2714">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2714">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2715">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2715">Checksum</span></span>

<span data-ttu-id="5c862-2716">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2716">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2717">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2717">Definition</span></span>

<span data-ttu-id="5c862-2718">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2718">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2719">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2719">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2720">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="5c862-2720">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2721">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2721">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="5c862-2722">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-2722">Keyword_jp_passport</span></span>

- <span data-ttu-id="5c862-2723">パスポート</span><span class="sxs-lookup"><span data-stu-id="5c862-2723">パスポート</span></span> 
- <span data-ttu-id="5c862-2724">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2724">パスポート番号</span></span> 
- <span data-ttu-id="5c862-2725">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="5c862-2725">パスポートのNum</span></span> 
- <span data-ttu-id="5c862-2726">パスポート #</span><span class="sxs-lookup"><span data-stu-id="5c862-2726">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="5c862-2727">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="5c862-2727">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2728">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2728">Format</span></span>

<span data-ttu-id="5c862-2729">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2729">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2730">Pattern</span></span>

<span data-ttu-id="5c862-2731">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2731">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2732">Checksum</span></span>

<span data-ttu-id="5c862-2733">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2733">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2734">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2734">Definition</span></span>

<span data-ttu-id="5c862-2735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2736">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2736">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2737">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-2737">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2738">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2738">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="5c862-2739">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2739">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="5c862-2740">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2740">Resident Registration Number</span></span>
- <span data-ttu-id="5c862-2741">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2741">Resident Register Number</span></span> 
- <span data-ttu-id="5c862-2742">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2742">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="5c862-2743">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2743">Resident Registration No.</span></span> 
- <span data-ttu-id="5c862-2744">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2744">Resident Register No.</span></span> 
- <span data-ttu-id="5c862-2745">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2745">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="5c862-2746">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2746">Basic Resident Register No.</span></span> 
- <span data-ttu-id="5c862-2747">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="5c862-2747">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="5c862-2748">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2748">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="5c862-2749">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="5c862-2749">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="5c862-2750">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2750">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="5c862-2751">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="5c862-2751">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2752">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2752">Format</span></span>

<span data-ttu-id="5c862-2753">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2753">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2754">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2754">Pattern</span></span>

<span data-ttu-id="5c862-2755">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-2755">7-12 digits:</span></span>
- <span data-ttu-id="5c862-2756">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-2756">Four digits</span></span> 
- <span data-ttu-id="5c862-2757">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5c862-2757">A hyphen (optional)</span></span> 
- <span data-ttu-id="5c862-2758">Шесть цифр или</span><span class="sxs-lookup"><span data-stu-id="5c862-2758">Six digits OR</span></span>
- <span data-ttu-id="5c862-2759">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2759">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2760">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2760">Checksum</span></span>

<span data-ttu-id="5c862-2761">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2761">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2762">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2762">Definition</span></span>

<span data-ttu-id="5c862-2763">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2763">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2764">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2764">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2765">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="5c862-2765">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="5c862-2766">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2766">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2767">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2767">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2768">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="5c862-2768">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2769">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2769">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="5c862-2770">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="5c862-2770">Keyword_jp_sin</span></span>

- <span data-ttu-id="5c862-2771">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="5c862-2771">Social Insurance No.</span></span> 
- <span data-ttu-id="5c862-2772">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="5c862-2772">Social Insurance Num</span></span> 
- <span data-ttu-id="5c862-2773">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2773">Social Insurance Number</span></span> 
- <span data-ttu-id="5c862-2774">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="5c862-2774">社会保険のテンキー</span></span> 
- <span data-ttu-id="5c862-2775">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2775">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="5c862-2776">Номер карточки для японского языка</span><span class="sxs-lookup"><span data-stu-id="5c862-2776">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2777">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2777">Format</span></span>

<span data-ttu-id="5c862-2778">12 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-2778">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2779">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2779">Pattern</span></span>

<span data-ttu-id="5c862-2780">12 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2780">12 letters and digits:</span></span>
- <span data-ttu-id="5c862-2781">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-2781">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="5c862-2782">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2782">Eight digits</span></span> 
- <span data-ttu-id="5c862-2783">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-2783">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2784">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2784">Checksum</span></span>

<span data-ttu-id="5c862-2785">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2785">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2786">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2786">Definition</span></span>

<span data-ttu-id="5c862-2787">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2788">Регулярное выражение Regex_jp_residence_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2788">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2789">Найдено ключевое слово из Keyword_jp_residence_card_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-2789">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2790">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2790">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="5c862-2791">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2791">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="5c862-2792">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="5c862-2792">Residence card number</span></span>
- <span data-ttu-id="5c862-2793">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="5c862-2793">Residence card no</span></span>
- <span data-ttu-id="5c862-2794">Карточка проживания #</span><span class="sxs-lookup"><span data-stu-id="5c862-2794">Residence card #</span></span>
- <span data-ttu-id="5c862-2795">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="5c862-2795">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="5c862-2796">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="5c862-2796">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2797">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2797">Format</span></span>

<span data-ttu-id="5c862-2798">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="5c862-2798">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2799">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2799">Pattern</span></span>

<span data-ttu-id="5c862-2800">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2800">12 digits:</span></span>
- <span data-ttu-id="5c862-2801">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="5c862-2801">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="5c862-2802">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="5c862-2802">A dash (optional)</span></span> 
- <span data-ttu-id="5c862-2803">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="5c862-2803">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="5c862-2804">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="5c862-2804">A dash (optional)</span></span> 
- <span data-ttu-id="5c862-2805">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-2805">Three random digits</span></span> 
- <span data-ttu-id="5c862-2806">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-2806">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2807">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2807">Checksum</span></span>

<span data-ttu-id="5c862-2808">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2808">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2809">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2809">Definition</span></span>

<span data-ttu-id="5c862-2810">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2810">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2811">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2811">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2812">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="5c862-2812">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2813">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2813">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="5c862-2814">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2814">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="5c862-2815">карточка цифрового приложения</span><span class="sxs-lookup"><span data-stu-id="5c862-2815">digital application card</span></span>
- <span data-ttu-id="5c862-2816">i/c</span><span class="sxs-lookup"><span data-stu-id="5c862-2816">i/c</span></span>
- <span data-ttu-id="5c862-2817">i/c нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2817">i/c no</span></span>
- <span data-ttu-id="5c862-2818">внутренних</span><span class="sxs-lookup"><span data-stu-id="5c862-2818">ic</span></span>
- <span data-ttu-id="5c862-2819">МФ нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2819">ic no</span></span>
- <span data-ttu-id="5c862-2820">id card</span><span class="sxs-lookup"><span data-stu-id="5c862-2820">id card</span></span>
- <span data-ttu-id="5c862-2821">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="5c862-2821">identification Card</span></span>
- <span data-ttu-id="5c862-2822">identity card</span><span class="sxs-lookup"><span data-stu-id="5c862-2822">identity card</span></span>
- <span data-ttu-id="5c862-2823">k/p</span><span class="sxs-lookup"><span data-stu-id="5c862-2823">k/p</span></span>
- <span data-ttu-id="5c862-2824">k/p</span><span class="sxs-lookup"><span data-stu-id="5c862-2824">k/p no</span></span>
- <span data-ttu-id="5c862-2825">кад акуан Дири</span><span class="sxs-lookup"><span data-stu-id="5c862-2825">kad akuan diri</span></span>
- <span data-ttu-id="5c862-2826">кад апликаси Digital</span><span class="sxs-lookup"><span data-stu-id="5c862-2826">kad aplikasi digital</span></span>
- <span data-ttu-id="5c862-2827">кад пенженалан Малайзии</span><span class="sxs-lookup"><span data-stu-id="5c862-2827">kad pengenalan malaysia</span></span>
- <span data-ttu-id="5c862-2828">ключев</span><span class="sxs-lookup"><span data-stu-id="5c862-2828">kp</span></span>
- <span data-ttu-id="5c862-2829">ключевой номер</span><span class="sxs-lookup"><span data-stu-id="5c862-2829">kp no</span></span>
- <span data-ttu-id="5c862-2830">микад</span><span class="sxs-lookup"><span data-stu-id="5c862-2830">mykad</span></span>
- <span data-ttu-id="5c862-2831">микас</span><span class="sxs-lookup"><span data-stu-id="5c862-2831">mykas</span></span>
- <span data-ttu-id="5c862-2832">микид</span><span class="sxs-lookup"><span data-stu-id="5c862-2832">mykid</span></span>
- <span data-ttu-id="5c862-2833">мипр</span><span class="sxs-lookup"><span data-stu-id="5c862-2833">mypr</span></span>
- <span data-ttu-id="5c862-2834">митентера</span><span class="sxs-lookup"><span data-stu-id="5c862-2834">mytentera</span></span>
- <span data-ttu-id="5c862-2835">идентификационная карточка Малайзии</span><span class="sxs-lookup"><span data-stu-id="5c862-2835">malaysia identity card</span></span>
- <span data-ttu-id="5c862-2836">идентификационная карточка малайсиан</span><span class="sxs-lookup"><span data-stu-id="5c862-2836">malaysian identity card</span></span>
- <span data-ttu-id="5c862-2837">NRIC</span><span class="sxs-lookup"><span data-stu-id="5c862-2837">nric</span></span>
- <span data-ttu-id="5c862-2838">Личная идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="5c862-2838">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="5c862-2839">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="5c862-2839">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2840">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2840">Format</span></span>

<span data-ttu-id="5c862-2841">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="5c862-2841">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2842">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2842">Pattern</span></span>

<span data-ttu-id="5c862-2843">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2843">8-9 digits:</span></span>
- <span data-ttu-id="5c862-2844">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-2844">Three digits</span></span> 
- <span data-ttu-id="5c862-2845">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="5c862-2845">A space (optional)</span></span> 
- <span data-ttu-id="5c862-2846">три цифры; </span><span class="sxs-lookup"><span data-stu-id="5c862-2846">Three digits</span></span> 
- <span data-ttu-id="5c862-2847">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="5c862-2847">A space (optional)</span></span> 
- <span data-ttu-id="5c862-2848">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-2848">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2849">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2849">Checksum</span></span>

<span data-ttu-id="5c862-2850">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2850">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2851">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2851">Definition</span></span>

<span data-ttu-id="5c862-2852">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2852">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2853">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2853">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2854">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="5c862-2854">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="5c862-2855">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-2855">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="5c862-2856">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2857">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2857">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="5c862-2858">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="5c862-2858">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="5c862-2859">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="5c862-2859">Citizen service number</span></span> 
- <span data-ttu-id="5c862-2860">BSN</span><span class="sxs-lookup"><span data-stu-id="5c862-2860">BSN</span></span> 
- <span data-ttu-id="5c862-2861">буржерсервиценуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2861">Burgerservicenummer</span></span> 
- <span data-ttu-id="5c862-2862">софинуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2862">Sofinummer</span></span> 
- <span data-ttu-id="5c862-2863">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="5c862-2863">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="5c862-2864">персунснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2864">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="5c862-2865">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="5c862-2865">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2866">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2866">Format</span></span>

<span data-ttu-id="5c862-2867">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-2867">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2868">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2868">Pattern</span></span>

<span data-ttu-id="5c862-2869">Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2869">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2870">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2870">Checksum</span></span>

<span data-ttu-id="5c862-2871">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2871">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2872">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2872">Definition</span></span>

<span data-ttu-id="5c862-2873">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2873">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2874">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2874">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2875">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="5c862-2875">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="5c862-2876">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2876">The checksum passes.</span></span>

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

<span data-ttu-id="5c862-2877">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2877">Keywords</span></span>

<span data-ttu-id="5c862-2878">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="5c862-2878">Keyword_nz_terms</span></span>

- <span data-ttu-id="5c862-2879">нхи</span><span class="sxs-lookup"><span data-stu-id="5c862-2879">NHI</span></span> 
- <span data-ttu-id="5c862-2880">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="5c862-2880">New Zealand</span></span> 
- <span data-ttu-id="5c862-2881">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="5c862-2881">Health</span></span> 
- <span data-ttu-id="5c862-2882">обращения</span><span class="sxs-lookup"><span data-stu-id="5c862-2882">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="5c862-2883">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="5c862-2883">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2884">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2884">Format</span></span>

<span data-ttu-id="5c862-2885">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2885">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2886">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2886">Pattern</span></span>

<span data-ttu-id="5c862-2887">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2887">11 digits:</span></span>
- <span data-ttu-id="5c862-2888">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="5c862-2888">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="5c862-2889">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-2889">Three-digit individual number</span></span> 
- <span data-ttu-id="5c862-2890">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-2890">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2891">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2891">Checksum</span></span>

<span data-ttu-id="5c862-2892">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2892">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2893">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2893">Definition</span></span>

<span data-ttu-id="5c862-2894">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2894">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2895">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2895">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2896">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-2896">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="5c862-2897">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2897">The checksum passes.</span></span>
- <span data-ttu-id="5c862-2898">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2898">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2899">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2899">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2900">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2900">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2901">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2901">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="5c862-2902">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2902">Keyword_norway_id_number</span></span>

- <span data-ttu-id="5c862-2903">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-2903">Personal identification number</span></span>
- <span data-ttu-id="5c862-2904">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2904">Norwegian ID Number</span></span>
- <span data-ttu-id="5c862-2905">ID Number</span><span class="sxs-lookup"><span data-stu-id="5c862-2905">ID Number</span></span>
- <span data-ttu-id="5c862-2906">Процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-2906">Identification</span></span>
- <span data-ttu-id="5c862-2907">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2907">Personnummer</span></span>
- <span data-ttu-id="5c862-2908">фøдселснуммер</span><span class="sxs-lookup"><span data-stu-id="5c862-2908">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="5c862-2909">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="5c862-2909">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2910">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2910">Format</span></span>

<span data-ttu-id="5c862-2911">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="5c862-2911">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2912">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2912">Pattern</span></span>

<span data-ttu-id="5c862-2913">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-2913">12 digits:</span></span>
- <span data-ttu-id="5c862-2914">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-2914">Four digits</span></span> 
- <span data-ttu-id="5c862-2915">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-2915">A hyphen</span></span> 
- <span data-ttu-id="5c862-2916">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-2916">Seven digits</span></span> 
- <span data-ttu-id="5c862-2917">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-2917">A hyphen</span></span> 
- <span data-ttu-id="5c862-2918">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="5c862-2918">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2919">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2919">Checksum</span></span>

<span data-ttu-id="5c862-2920">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2920">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2921">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2921">Definition</span></span>

<span data-ttu-id="5c862-2922">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2922">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2923">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2923">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2924">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="5c862-2924">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2925">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2925">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="5c862-2926">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="5c862-2926">Keyword_philippines_id</span></span>

- <span data-ttu-id="5c862-2927">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="5c862-2927">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="5c862-2928">умид</span><span class="sxs-lookup"><span data-stu-id="5c862-2928">UMID</span></span> 
- <span data-ttu-id="5c862-2929">Identity Card</span><span class="sxs-lookup"><span data-stu-id="5c862-2929">Identity Card</span></span> 
- <span data-ttu-id="5c862-2930">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="5c862-2930">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="5c862-2931">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="5c862-2931">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2932">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2932">Format</span></span>

<span data-ttu-id="5c862-2933">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2933">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2934">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2934">Pattern</span></span>

<span data-ttu-id="5c862-2935">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2935">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2936">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2936">Checksum</span></span>

<span data-ttu-id="5c862-2937">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2937">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2938">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2938">Definition</span></span>

<span data-ttu-id="5c862-2939">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_polish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2939">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="5c862-2940">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-2940">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="5c862-2941">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2941">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2942">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2942">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="5c862-2943">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2943">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="5c862-2944">Довóд особисти</span><span class="sxs-lookup"><span data-stu-id="5c862-2944">Dowód osobisty</span></span>
- <span data-ttu-id="5c862-2945">Нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="5c862-2945">Numer dowodu osobistego</span></span>
- <span data-ttu-id="5c862-2946">Назва i нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="5c862-2946">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="5c862-2947">Назва i НР доводу особистего</span><span class="sxs-lookup"><span data-stu-id="5c862-2947">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="5c862-2948">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="5c862-2948">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="5c862-2949">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="5c862-2949">Dowód Tożsamości</span></span>
- <span data-ttu-id="5c862-2950">Dow.</span><span class="sxs-lookup"><span data-stu-id="5c862-2950">dow.</span></span> <span data-ttu-id="5c862-2951">совместим.</span><span class="sxs-lookup"><span data-stu-id="5c862-2951">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="5c862-2952">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="5c862-2952">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2953">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2953">Format</span></span>

<span data-ttu-id="5c862-2954">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2954">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2955">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2955">Pattern</span></span>

<span data-ttu-id="5c862-2956">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2956">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2957">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2957">Checksum</span></span>

<span data-ttu-id="5c862-2958">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2958">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2959">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2959">Definition</span></span>

<span data-ttu-id="5c862-2960">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2960">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2961">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2961">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2962">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-2962">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="5c862-2963">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2963">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2964">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2964">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="5c862-2965">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2965">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="5c862-2966">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="5c862-2966">Nr PESEL</span></span>
- <span data-ttu-id="5c862-2967">PESEL</span><span class="sxs-lookup"><span data-stu-id="5c862-2967">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="5c862-2968">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="5c862-2968">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2969">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2969">Format</span></span>

<span data-ttu-id="5c862-2970">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2970">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2971">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2971">Pattern</span></span>

<span data-ttu-id="5c862-2972">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2972">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2973">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2973">Checksum</span></span>

<span data-ttu-id="5c862-2974">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-2974">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2975">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2975">Definition</span></span>

<span data-ttu-id="5c862-2976">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2976">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2977">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2977">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2978">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-2978">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="5c862-2979">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-2979">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-2980">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2980">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="5c862-2981">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="5c862-2981">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="5c862-2982">Нумер пасзпорту</span><span class="sxs-lookup"><span data-stu-id="5c862-2982">Numer paszportu</span></span>
- <span data-ttu-id="5c862-2983">НР.</span><span class="sxs-lookup"><span data-stu-id="5c862-2983">Nr.</span></span> <span data-ttu-id="5c862-2984">пасзпорту</span><span class="sxs-lookup"><span data-stu-id="5c862-2984">Paszportu</span></span>
- <span data-ttu-id="5c862-2985">пасзпорт</span><span class="sxs-lookup"><span data-stu-id="5c862-2985">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="5c862-2986">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="5c862-2986">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-2987">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-2987">Format</span></span>

<span data-ttu-id="5c862-2988">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2988">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-2989">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-2989">Pattern</span></span>

<span data-ttu-id="5c862-2990">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-2990">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-2991">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-2991">Checksum</span></span>

<span data-ttu-id="5c862-2992">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-2992">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-2993">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-2993">Definition</span></span>

<span data-ttu-id="5c862-2994">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-2994">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-2995">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-2995">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-2996">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="5c862-2996">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-2997">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-2997">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="5c862-2998">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="5c862-2998">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="5c862-2999">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="5c862-2999">Citizen Card</span></span>
- <span data-ttu-id="5c862-3000">National ID Card</span><span class="sxs-lookup"><span data-stu-id="5c862-3000">National ID Card</span></span>
- <span data-ttu-id="5c862-3001">CC</span><span class="sxs-lookup"><span data-stu-id="5c862-3001">CC</span></span>
- <span data-ttu-id="5c862-3002">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="5c862-3002">Cartão de Cidadão</span></span>
- <span data-ttu-id="5c862-3003">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="5c862-3003">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="5c862-3004">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="5c862-3004">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3005">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3005">Format</span></span>

<span data-ttu-id="5c862-3006">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3006">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3007">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3007">Pattern</span></span>

<span data-ttu-id="5c862-3008">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3008">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3009">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3009">Checksum</span></span>

<span data-ttu-id="5c862-3010">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3010">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3011">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3011">Definition</span></span>

<span data-ttu-id="5c862-3012">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3012">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3013">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3013">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3014">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="5c862-3014">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3015">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3015">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="5c862-3016">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="5c862-3016">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="5c862-3017">Identification Card</span><span class="sxs-lookup"><span data-stu-id="5c862-3017">Identification Card</span></span> 
- <span data-ttu-id="5c862-3018">I card number</span><span class="sxs-lookup"><span data-stu-id="5c862-3018">I card number</span></span> 
- <span data-ttu-id="5c862-3019">ID number</span><span class="sxs-lookup"><span data-stu-id="5c862-3019">ID number</span></span> 
- <span data-ttu-id="5c862-3020">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="5c862-3020">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="5c862-3021">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="5c862-3021">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3022">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3022">Format</span></span>

<span data-ttu-id="5c862-3023">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3023">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3024">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3024">Pattern</span></span>

- <span data-ttu-id="5c862-3025">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-3025">Nine letters and digits:</span></span>
- <span data-ttu-id="5c862-3026">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-3026">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-3027">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-3027">Seven digits</span></span> 
- <span data-ttu-id="5c862-3028">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="5c862-3028">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3029">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3029">Checksum</span></span>

<span data-ttu-id="5c862-3030">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3030">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3031">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3031">Definition</span></span>

<span data-ttu-id="5c862-3032">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3032">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3033">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3033">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3034">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="5c862-3034">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="5c862-3035">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3035">The checksum passes.</span></span>

<span data-ttu-id="5c862-3036">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3036">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3037">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3037">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3038">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3038">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3039">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3039">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="5c862-3040">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="5c862-3040">Keyword_singapore_nric</span></span>

- <span data-ttu-id="5c862-3041">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="5c862-3041">National Registration Identity Card</span></span> 
- <span data-ttu-id="5c862-3042">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3042">Identity Card Number</span></span> 
- <span data-ttu-id="5c862-3043">NRIC</span><span class="sxs-lookup"><span data-stu-id="5c862-3043">NRIC</span></span> 
- <span data-ttu-id="5c862-3044">ВНУТРЕННИХ</span><span class="sxs-lookup"><span data-stu-id="5c862-3044">IC</span></span> 
- <span data-ttu-id="5c862-3045">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3045">Foreign Identification Number</span></span> 
- <span data-ttu-id="5c862-3046">ПРОЦЕНТ</span><span class="sxs-lookup"><span data-stu-id="5c862-3046">FIN</span></span> 
- <span data-ttu-id="5c862-3047">身份证</span><span class="sxs-lookup"><span data-stu-id="5c862-3047">身份证</span></span> 
- <span data-ttu-id="5c862-3048">身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-3048">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="5c862-3049">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="5c862-3049">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3050">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3050">Format</span></span>

<span data-ttu-id="5c862-3051">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="5c862-3051">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3052">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3052">Pattern</span></span>

<span data-ttu-id="5c862-3053">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-3053">13 digits:</span></span>
- <span data-ttu-id="5c862-3054">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="5c862-3054">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="5c862-3055">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-3055">Four digits</span></span> 
- <span data-ttu-id="5c862-3056">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="5c862-3056">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="5c862-3057">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="5c862-3057">The digit "8" or "9"</span></span> 
- <span data-ttu-id="5c862-3058">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="5c862-3058">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3059">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3059">Checksum</span></span>

<span data-ttu-id="5c862-3060">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3061">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3061">Definition</span></span>

<span data-ttu-id="5c862-3062">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3063">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3063">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3064">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-3064">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="5c862-3065">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3065">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3066">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3066">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="5c862-3067">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="5c862-3067">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="5c862-3068">Identity card</span><span class="sxs-lookup"><span data-stu-id="5c862-3068">Identity card</span></span>
- <span data-ttu-id="5c862-3069">ID</span><span class="sxs-lookup"><span data-stu-id="5c862-3069">ID</span></span>
- <span data-ttu-id="5c862-3070">Процедура</span><span class="sxs-lookup"><span data-stu-id="5c862-3070">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="5c862-3071">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="5c862-3071">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3072">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3072">Format</span></span>

<span data-ttu-id="5c862-3073">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="5c862-3073">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3074">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3074">Pattern</span></span>

<span data-ttu-id="5c862-3075">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-3075">13 digits:</span></span>
- <span data-ttu-id="5c862-3076">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="5c862-3076">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="5c862-3077">дефис;</span><span class="sxs-lookup"><span data-stu-id="5c862-3077">A hyphen</span></span> 
- <span data-ttu-id="5c862-3078">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="5c862-3078">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="5c862-3079">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="5c862-3079">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="5c862-3080">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="5c862-3080">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="5c862-3081">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="5c862-3081">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3082">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3082">Checksum</span></span>

<span data-ttu-id="5c862-3083">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3083">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3084">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3084">Definition</span></span>

<span data-ttu-id="5c862-3085">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3085">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3086">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3086">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3087">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-3087">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="5c862-3088">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3088">The checksum passes.</span></span>

<span data-ttu-id="5c862-3089">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3089">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3090">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3090">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3091">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3091">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3092">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3092">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="5c862-3093">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="5c862-3093">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="5c862-3094">National ID card</span><span class="sxs-lookup"><span data-stu-id="5c862-3094">National ID card</span></span> 
- <span data-ttu-id="5c862-3095">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3095">Citizen's Registration Number</span></span> 
- <span data-ttu-id="5c862-3096">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="5c862-3096">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="5c862-3097">ррн</span><span class="sxs-lookup"><span data-stu-id="5c862-3097">RRN</span></span> 
- <span data-ttu-id="5c862-3098">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="5c862-3098">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="5c862-3099">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="5c862-3099">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3100">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3100">Format</span></span>

<span data-ttu-id="5c862-3101">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3101">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3102">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3102">Pattern</span></span>

<span data-ttu-id="5c862-3103">11-12 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-3103">11-12 digits:</span></span>
- <span data-ttu-id="5c862-3104">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3104">Two digits</span></span> 
- <span data-ttu-id="5c862-3105">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5c862-3105">A forward slash (optional)</span></span> 
- <span data-ttu-id="5c862-3106">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3106">7-8 digits</span></span> 
- <span data-ttu-id="5c862-3107">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5c862-3107">A forward slash (optional)</span></span> 
- <span data-ttu-id="5c862-3108">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3108">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3109">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3109">Checksum</span></span>

<span data-ttu-id="5c862-3110">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3110">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3111">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3111">Definition</span></span>

<span data-ttu-id="5c862-3112">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3112">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3113">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3113">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3114">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3114">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3115">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3115">Keywords</span></span>

<span data-ttu-id="5c862-3116">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3116">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="5c862-3117">Строка подключения к SQL Server</span><span class="sxs-lookup"><span data-stu-id="5c862-3117">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3118">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3118">Format</span></span>

<span data-ttu-id="5c862-3119">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId", за которыми следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="5c862-3119">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3120">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3120">Pattern</span></span>

- <span data-ttu-id="5c862-3121">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId"</span><span class="sxs-lookup"><span data-stu-id="5c862-3121">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="5c862-3122">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="5c862-3122">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="5c862-3123">Строка "Password" или "pwd", где "pwd" не предшествует буква нижнего регистра</span><span class="sxs-lookup"><span data-stu-id="5c862-3123">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="5c862-3124">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="5c862-3124">An equal sign (=)</span></span>
- <span data-ttu-id="5c862-3125">Любой символ, не являющийся знаком доллара ($), символ процента (%), символ "больше" (>), символ "@", "символ" (@), знак кавычек ("), точка с запятой (;), левая фигурная скобка ([) или левая квадратная скобка ({)</span><span class="sxs-lookup"><span data-stu-id="5c862-3125">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="5c862-3126">Любая комбинация 7-128 символов, не отделяющая точку с запятой (;), косая черта (/) или кавычки (").</span><span class="sxs-lookup"><span data-stu-id="5c862-3126">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="5c862-3127">Точка с запятой (;) или кавычки (")</span><span class="sxs-lookup"><span data-stu-id="5c862-3127">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3128">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3128">Checksum</span></span>

<span data-ttu-id="5c862-3129">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3129">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3130">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3130">Definition</span></span>

<span data-ttu-id="5c862-3131">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3132">Регулярное выражение CEP_Regex_SQLServerConnectionString находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3132">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3133">**Не** найдено ключевое слово из CEP_GlobalFilter.</span><span class="sxs-lookup"><span data-stu-id="5c862-3133">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="5c862-3134">Регулярное выражение CEP_PasswordPlaceHolder не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3134">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3135">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3135">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3136">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3136">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="5c862-3137">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="5c862-3137">CEP_GlobalFilter</span></span>

- <span data-ttu-id="5c862-3138">Некоторые пароли</span><span class="sxs-lookup"><span data-stu-id="5c862-3138">some-password</span></span>
- <span data-ttu-id="5c862-3139">сомепассворд</span><span class="sxs-lookup"><span data-stu-id="5c862-3139">somepassword</span></span>
- <span data-ttu-id="5c862-3140">секретпассворд</span><span class="sxs-lookup"><span data-stu-id="5c862-3140">secretPassword</span></span>
- <span data-ttu-id="5c862-3141">примером</span><span class="sxs-lookup"><span data-stu-id="5c862-3141">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="5c862-3142">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="5c862-3142">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="5c862-3143">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-3143">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-3144">Пароль или pwd, за которым следует 0-2 пробелов, знак равенства (=), 0-2 пробелы и звездочка (\*)--или--</span><span class="sxs-lookup"><span data-stu-id="5c862-3144">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="5c862-3145">Пароль или pwd, а затем:</span><span class="sxs-lookup"><span data-stu-id="5c862-3145">Password or pwd followed by:</span></span>
    - <span data-ttu-id="5c862-3146">Знак равенства (=)</span><span class="sxs-lookup"><span data-stu-id="5c862-3146">Equal sign (=)</span></span>
    - <span data-ttu-id="5c862-3147">Символ "меньше" (<)</span><span class="sxs-lookup"><span data-stu-id="5c862-3147">Less than symbol (<)</span></span>
    - <span data-ttu-id="5c862-3148">Любое сочетание 1-200 символов, которые являются буквами верхнего или нижнего регистра, цифрами, звездочкой (\*), дефисом (-), подчеркиванием (_) или символом пробела</span><span class="sxs-lookup"><span data-stu-id="5c862-3148">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="5c862-3149">Символ "больше" (>)</span><span class="sxs-lookup"><span data-stu-id="5c862-3149">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="5c862-3150">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="5c862-3150">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="5c862-3151">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="5c862-3151">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="5c862-3152">компанией</span><span class="sxs-lookup"><span data-stu-id="5c862-3152">contoso</span></span>
- <span data-ttu-id="5c862-3153">компании</span><span class="sxs-lookup"><span data-stu-id="5c862-3153">fabrikam</span></span>
- <span data-ttu-id="5c862-3154">базу</span><span class="sxs-lookup"><span data-stu-id="5c862-3154">northwind</span></span>
- <span data-ttu-id="5c862-3155">песочниц</span><span class="sxs-lookup"><span data-stu-id="5c862-3155">sandbox</span></span>
- <span data-ttu-id="5c862-3156">онебокс</span><span class="sxs-lookup"><span data-stu-id="5c862-3156">onebox</span></span>
- <span data-ttu-id="5c862-3157">localhost</span><span class="sxs-lookup"><span data-stu-id="5c862-3157">localhost</span></span>
- <span data-ttu-id="5c862-3158">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="5c862-3158">127.0.0.1</span></span>
- <span data-ttu-id="5c862-3159">тестакс.</span><span class="sxs-lookup"><span data-stu-id="5c862-3159">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-3160">порта</span><span class="sxs-lookup"><span data-stu-id="5c862-3160">com</span></span>
- <span data-ttu-id="5c862-3161">s — int.</span><span class="sxs-lookup"><span data-stu-id="5c862-3161">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="5c862-3162">команде</span><span class="sxs-lookup"><span data-stu-id="5c862-3162">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="5c862-3163">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="5c862-3163">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3164">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3164">Format</span></span>

<span data-ttu-id="5c862-3165">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="5c862-3165">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3166">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3166">Pattern</span></span>

<span data-ttu-id="5c862-3167">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="5c862-3167">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="5c862-3168">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5c862-3168">2-4 digits (optional)</span></span> 
- <span data-ttu-id="5c862-3169">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="5c862-3169">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="5c862-3170">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5c862-3170">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="5c862-3171">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-3171">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3172">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3172">Checksum</span></span>

<span data-ttu-id="5c862-3173">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3173">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3174">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3174">Definition</span></span>

<span data-ttu-id="5c862-3175">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3175">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3176">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3176">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3177">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3177">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3178">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3178">Keywords</span></span>

<span data-ttu-id="5c862-3179">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3179">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="5c862-3180">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="5c862-3180">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3181">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3181">Format</span></span>

<span data-ttu-id="5c862-3182">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3182">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3183">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3183">Pattern</span></span>

<span data-ttu-id="5c862-3184">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3184">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3185">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3185">Checksum</span></span>

<span data-ttu-id="5c862-3186">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3186">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3187">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3187">Definition</span></span>

<span data-ttu-id="5c862-3188">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3188">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3189">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3189">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3190">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-3190">One of the following is true:</span></span>
    - <span data-ttu-id="5c862-3191">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="5c862-3191">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="5c862-3192">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="5c862-3192">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3193">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3193">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="5c862-3194">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-3194">Keyword_sweden_passport</span></span>

- <span data-ttu-id="5c862-3195">visa requirements</span><span class="sxs-lookup"><span data-stu-id="5c862-3195">visa requirements</span></span> 
- <span data-ttu-id="5c862-3196">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="5c862-3196">Alien Registration Card</span></span> 
- <span data-ttu-id="5c862-3197">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="5c862-3197">Schengen visas</span></span> 
- <span data-ttu-id="5c862-3198">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="5c862-3198">Schengen visa</span></span> 
- <span data-ttu-id="5c862-3199">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="5c862-3199">Visa Processing</span></span> 
- <span data-ttu-id="5c862-3200">Visa Type</span><span class="sxs-lookup"><span data-stu-id="5c862-3200">Visa Type</span></span> 
- <span data-ttu-id="5c862-3201">Single Entry</span><span class="sxs-lookup"><span data-stu-id="5c862-3201">Single Entry</span></span> 
- <span data-ttu-id="5c862-3202">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="5c862-3202">Multiple Entry</span></span> 
- <span data-ttu-id="5c862-3203">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="5c862-3203">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="5c862-3204">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-3204">Keyword_passport</span></span>

- <span data-ttu-id="5c862-3205">Passport Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3205">Passport Number</span></span> 
- <span data-ttu-id="5c862-3206">Passport No</span><span class="sxs-lookup"><span data-stu-id="5c862-3206">Passport No</span></span> 
- <span data-ttu-id="5c862-3207">Passport#</span><span class="sxs-lookup"><span data-stu-id="5c862-3207">Passport #</span></span> 
- <span data-ttu-id="5c862-3208">Службу #</span><span class="sxs-lookup"><span data-stu-id="5c862-3208">Passport#</span></span> 
- <span data-ttu-id="5c862-3209">пасспортид</span><span class="sxs-lookup"><span data-stu-id="5c862-3209">PassportID</span></span> 
- <span data-ttu-id="5c862-3210">пасспортно</span><span class="sxs-lookup"><span data-stu-id="5c862-3210">Passportno</span></span> 
- <span data-ttu-id="5c862-3211">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-3211">passportnumber</span></span> 
- <span data-ttu-id="5c862-3212">パスポート</span><span class="sxs-lookup"><span data-stu-id="5c862-3212">パスポート</span></span> 
- <span data-ttu-id="5c862-3213">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="5c862-3213">パスポート番号</span></span> 
- <span data-ttu-id="5c862-3214">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="5c862-3214">パスポートのNum</span></span> 
- <span data-ttu-id="5c862-3215">パスポート #</span><span class="sxs-lookup"><span data-stu-id="5c862-3215">パスポート＃</span></span> 
- <span data-ttu-id="5c862-3216">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="5c862-3216">Numéro de passeport</span></span> 
- <span data-ttu-id="5c862-3217">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="5c862-3217">Passeport n °</span></span> 
- <span data-ttu-id="5c862-3218">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="5c862-3218">Passeport Non</span></span> 
- <span data-ttu-id="5c862-3219">Passeport#</span><span class="sxs-lookup"><span data-stu-id="5c862-3219">Passeport #</span></span> 
- <span data-ttu-id="5c862-3220">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="5c862-3220">Passeport#</span></span> 
- <span data-ttu-id="5c862-3221">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="5c862-3221">PasseportNon</span></span> 
- <span data-ttu-id="5c862-3222">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="5c862-3222">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="5c862-3223">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="5c862-3223">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3224">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3224">Format</span></span>

<span data-ttu-id="5c862-3225">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-3225">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3226">Pattern</span></span>

<span data-ttu-id="5c862-3227">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3227">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="5c862-3228">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-3228">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-3229">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-3229">An optional space</span></span> 
- <span data-ttu-id="5c862-3230">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="5c862-3230">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="5c862-3231">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-3231">An optional space</span></span> 
- <span data-ttu-id="5c862-3232">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="5c862-3232">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3233">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3233">Checksum</span></span>

<span data-ttu-id="5c862-3234">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3234">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3235">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3235">Definition</span></span>

<span data-ttu-id="5c862-3236">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3236">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3237">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3237">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3238">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="5c862-3238">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3239">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3239">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="5c862-3240">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="5c862-3240">Keyword_swift</span></span>

- <span data-ttu-id="5c862-3241">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="5c862-3241">international organization for standardization 9362</span></span> 
- <span data-ttu-id="5c862-3242">iso 9362</span><span class="sxs-lookup"><span data-stu-id="5c862-3242">iso 9362</span></span> 
- <span data-ttu-id="5c862-3243">iso9362</span><span class="sxs-lookup"><span data-stu-id="5c862-3243">iso9362</span></span> 
- <span data-ttu-id="5c862-3244">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="5c862-3244">swift\#</span></span> 
- <span data-ttu-id="5c862-3245">свифткоде</span><span class="sxs-lookup"><span data-stu-id="5c862-3245">swiftcode</span></span> 
- <span data-ttu-id="5c862-3246">свифтнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-3246">swiftnumber</span></span> 
- <span data-ttu-id="5c862-3247">свифтраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-3247">swiftroutingnumber</span></span> 
- <span data-ttu-id="5c862-3248">swift code</span><span class="sxs-lookup"><span data-stu-id="5c862-3248">swift code</span></span> 
- <span data-ttu-id="5c862-3249">swift number #</span><span class="sxs-lookup"><span data-stu-id="5c862-3249">swift number #</span></span> 
- <span data-ttu-id="5c862-3250">swift routing number</span><span class="sxs-lookup"><span data-stu-id="5c862-3250">swift routing number</span></span> 
- <span data-ttu-id="5c862-3251">bic number</span><span class="sxs-lookup"><span data-stu-id="5c862-3251">bic number</span></span> 
- <span data-ttu-id="5c862-3252">bic code</span><span class="sxs-lookup"><span data-stu-id="5c862-3252">bic code</span></span> 
- <span data-ttu-id="5c862-3253">БИК\#</span><span class="sxs-lookup"><span data-stu-id="5c862-3253">bic \#</span></span> 
- <span data-ttu-id="5c862-3254">БИК\#</span><span class="sxs-lookup"><span data-stu-id="5c862-3254">bic\#</span></span> 
- <span data-ttu-id="5c862-3255">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="5c862-3255">bank identifier code</span></span> 
- <span data-ttu-id="5c862-3256">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="5c862-3256">標準化9362</span></span> 
- <span data-ttu-id="5c862-3257">迅速 #</span><span class="sxs-lookup"><span data-stu-id="5c862-3257">迅速＃</span></span> 
- <span data-ttu-id="5c862-3258">свифтコード</span><span class="sxs-lookup"><span data-stu-id="5c862-3258">SWIFTコード</span></span> 
- <span data-ttu-id="5c862-3259">свифт番号</span><span class="sxs-lookup"><span data-stu-id="5c862-3259">SWIFT番号</span></span> 
- <span data-ttu-id="5c862-3260">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="5c862-3260">迅速なルーティング番号</span></span> 
- <span data-ttu-id="5c862-3261">бик番号</span><span class="sxs-lookup"><span data-stu-id="5c862-3261">BIC番号</span></span> 
- <span data-ttu-id="5c862-3262">бикコード</span><span class="sxs-lookup"><span data-stu-id="5c862-3262">BICコード</span></span> 
- <span data-ttu-id="5c862-3263">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="5c862-3263">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="5c862-3264">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="5c862-3264">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="5c862-3265">Быстрая\#</span><span class="sxs-lookup"><span data-stu-id="5c862-3265">rapide \#</span></span> 
- <span data-ttu-id="5c862-3266">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="5c862-3266">code SWIFT</span></span> 
- <span data-ttu-id="5c862-3267">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="5c862-3267">le numéro de swift</span></span> 
- <span data-ttu-id="5c862-3268">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="5c862-3268">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="5c862-3269">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="5c862-3269">le numéro BIC</span></span> 
- <span data-ttu-id="5c862-3270">\#БИК</span><span class="sxs-lookup"><span data-stu-id="5c862-3270">\# BIC</span></span> 
- <span data-ttu-id="5c862-3271">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="5c862-3271">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="5c862-3272">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="5c862-3272">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3273">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3273">Format</span></span>

<span data-ttu-id="5c862-3274">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3274">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3275">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3275">Pattern</span></span>

<span data-ttu-id="5c862-3276">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3276">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="5c862-3277">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-3277">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="5c862-3278">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="5c862-3278">The digit "1" or "2"</span></span> 
- <span data-ttu-id="5c862-3279">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3279">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3280">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3280">Checksum</span></span>

<span data-ttu-id="5c862-3281">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3281">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3282">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3282">Definition</span></span>

<span data-ttu-id="5c862-3283">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3283">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3284">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3284">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3285">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="5c862-3285">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="5c862-3286">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3286">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3287">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3287">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="5c862-3288">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="5c862-3288">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="5c862-3289">身份證字號</span><span class="sxs-lookup"><span data-stu-id="5c862-3289">身份證字號</span></span> 
- <span data-ttu-id="5c862-3290">身份證</span><span class="sxs-lookup"><span data-stu-id="5c862-3290">身份證</span></span> 
- <span data-ttu-id="5c862-3291">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="5c862-3291">身份證號碼</span></span> 
- <span data-ttu-id="5c862-3292">身份證號</span><span class="sxs-lookup"><span data-stu-id="5c862-3292">身份證號</span></span> 
- <span data-ttu-id="5c862-3293">身分證字號</span><span class="sxs-lookup"><span data-stu-id="5c862-3293">身分證字號</span></span> 
- <span data-ttu-id="5c862-3294">身分證</span><span class="sxs-lookup"><span data-stu-id="5c862-3294">身分證</span></span> 
- <span data-ttu-id="5c862-3295">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="5c862-3295">身分證號碼</span></span> 
- <span data-ttu-id="5c862-3296">身份證號</span><span class="sxs-lookup"><span data-stu-id="5c862-3296">身份證號</span></span> 
- <span data-ttu-id="5c862-3297">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="5c862-3297">身分證統一編號</span></span> 
- <span data-ttu-id="5c862-3298">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="5c862-3298">國民身分證統一編號</span></span> 
- <span data-ttu-id="5c862-3299">簽名</span><span class="sxs-lookup"><span data-stu-id="5c862-3299">簽名</span></span> 
- <span data-ttu-id="5c862-3300">蓋章</span><span class="sxs-lookup"><span data-stu-id="5c862-3300">蓋章</span></span> 
- <span data-ttu-id="5c862-3301">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="5c862-3301">簽名或蓋章</span></span> 
- <span data-ttu-id="5c862-3302">簽章</span><span class="sxs-lookup"><span data-stu-id="5c862-3302">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="5c862-3303">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="5c862-3303">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3304">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3304">Format</span></span>

- <span data-ttu-id="5c862-3305">Номер биометрического паспорта: девять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3305">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="5c862-3306">Номер биометрической службы Passport: девять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3306">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3307">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3307">Pattern</span></span>
<span data-ttu-id="5c862-3308">Номер биометрического паспорта:</span><span class="sxs-lookup"><span data-stu-id="5c862-3308">Biometric passport number:</span></span>
- <span data-ttu-id="5c862-3309">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="5c862-3309">The digit "3"</span></span> 
- <span data-ttu-id="5c862-3310">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3310">Eight digits</span></span>

<span data-ttu-id="5c862-3311">Номер биометрической службы Passport:</span><span class="sxs-lookup"><span data-stu-id="5c862-3311">Non-biometric passport number:</span></span>
- <span data-ttu-id="5c862-3312">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3312">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3313">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3313">Checksum</span></span>

<span data-ttu-id="5c862-3314">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3314">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3315">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3315">Definition</span></span>

<span data-ttu-id="5c862-3316">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3317">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3317">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3318">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="5c862-3318">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3319">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3319">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="5c862-3320">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-3320">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="5c862-3321">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="5c862-3321">ROC passport number</span></span> 
- <span data-ttu-id="5c862-3322">Passport number</span><span class="sxs-lookup"><span data-stu-id="5c862-3322">Passport number</span></span> 
- <span data-ttu-id="5c862-3323">Passport no</span><span class="sxs-lookup"><span data-stu-id="5c862-3323">Passport no</span></span> 
- <span data-ttu-id="5c862-3324">Passport Num</span><span class="sxs-lookup"><span data-stu-id="5c862-3324">Passport Num</span></span> 
- <span data-ttu-id="5c862-3325">Passport #</span><span class="sxs-lookup"><span data-stu-id="5c862-3325">Passport #</span></span> 
- <span data-ttu-id="5c862-3326">护照</span><span class="sxs-lookup"><span data-stu-id="5c862-3326">护照</span></span> 
- <span data-ttu-id="5c862-3327">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="5c862-3327">中華民國護照</span></span> 
- <span data-ttu-id="5c862-3328">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="5c862-3328">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="5c862-3329">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="5c862-3329">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3330">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3330">Format</span></span>

<span data-ttu-id="5c862-3331">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3331">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3332">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3332">Pattern</span></span>

<span data-ttu-id="5c862-3333">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-3333">10 letters and digits:</span></span>
- <span data-ttu-id="5c862-3334">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="5c862-3334">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="5c862-3335">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3335">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3336">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3336">Checksum</span></span>

<span data-ttu-id="5c862-3337">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3337">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3338">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3338">Definition</span></span>

<span data-ttu-id="5c862-3339">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3340">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3340">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3341">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="5c862-3341">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3342">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3342">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="5c862-3343">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="5c862-3343">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="5c862-3344">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="5c862-3344">Resident Certificate</span></span> 
- <span data-ttu-id="5c862-3345">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="5c862-3345">Resident Cert</span></span> 
- <span data-ttu-id="5c862-3346">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="5c862-3346">Resident Cert.</span></span> 
- <span data-ttu-id="5c862-3347">Identification card</span><span class="sxs-lookup"><span data-stu-id="5c862-3347">Identification card</span></span> 
- <span data-ttu-id="5c862-3348">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="5c862-3348">Alien Resident Certificate</span></span> 
- <span data-ttu-id="5c862-3349">ГИПЕРБОЛ</span><span class="sxs-lookup"><span data-stu-id="5c862-3349">ARC</span></span> 
- <span data-ttu-id="5c862-3350">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="5c862-3350">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="5c862-3351">TARC</span><span class="sxs-lookup"><span data-stu-id="5c862-3351">TARC</span></span> 
- <span data-ttu-id="5c862-3352">居留證</span><span class="sxs-lookup"><span data-stu-id="5c862-3352">居留證</span></span> 
- <span data-ttu-id="5c862-3353">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="5c862-3353">外僑居留證</span></span> 
- <span data-ttu-id="5c862-3354">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="5c862-3354">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="5c862-3355">Код идентификации для тайского заполнения</span><span class="sxs-lookup"><span data-stu-id="5c862-3355">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3356">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3356">Format</span></span>

<span data-ttu-id="5c862-3357">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3357">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3358">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3358">Pattern</span></span>

<span data-ttu-id="5c862-3359">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="5c862-3359">13 digits:</span></span>
- <span data-ttu-id="5c862-3360">Первая цифра не равна 0 или 9</span><span class="sxs-lookup"><span data-stu-id="5c862-3360">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="5c862-3361">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3361">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3362">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3362">Checksum</span></span>

<span data-ttu-id="5c862-3363">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3363">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3364">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3364">Definition</span></span>

<span data-ttu-id="5c862-3365">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3365">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3366">Функция Func_Thai_Citizen_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3366">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3367">Найдено ключевое слово из Keyword_Thai_Citizen_Id.</span><span class="sxs-lookup"><span data-stu-id="5c862-3367">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="5c862-3368">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3368">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3369">Функция Func_Thai_Citizen_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3369">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3370">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3370">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="5c862-3371">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="5c862-3371">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="5c862-3372">ID Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3372">ID Number</span></span>
- <span data-ttu-id="5c862-3373">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="5c862-3373">Identification Number</span></span>
- <span data-ttu-id="5c862-3374">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="5c862-3374">บัตรประชาชน</span></span>
- <span data-ttu-id="5c862-3375">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="5c862-3375">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="5c862-3376">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="5c862-3376">บัตรประชาชน</span></span>
- <span data-ttu-id="5c862-3377">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="5c862-3377">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="5c862-3378">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="5c862-3378">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3379">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3379">Format</span></span>

<span data-ttu-id="5c862-3380">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3380">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3381">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3381">Pattern</span></span>

<span data-ttu-id="5c862-3382">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3382">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3383">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3383">Checksum</span></span>

<span data-ttu-id="5c862-3384">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3384">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3385">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3385">Definition</span></span>

<span data-ttu-id="5c862-3386">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3386">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3387">Функция Func_Turkish_National_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3387">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3388">Найдено ключевое слово из Keyword_Turkish_National_Id.</span><span class="sxs-lookup"><span data-stu-id="5c862-3388">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="5c862-3389">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3390">Функция Func_Turkish_National_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3390">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3391">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3391">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="5c862-3392">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="5c862-3392">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="5c862-3393">TC Кимлик No</span><span class="sxs-lookup"><span data-stu-id="5c862-3393">TC Kimlik No</span></span>
- <span data-ttu-id="5c862-3394">TC Кимлик нумарасı</span><span class="sxs-lookup"><span data-stu-id="5c862-3394">TC Kimlik numarası</span></span>
- <span data-ttu-id="5c862-3395">Ватандаşлıк нумарасı</span><span class="sxs-lookup"><span data-stu-id="5c862-3395">Vatandaşlık numarası</span></span>
- <span data-ttu-id="5c862-3396">Ватандаşлıк нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3396">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="5c862-p142">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="5c862-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3399">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3399">Format</span></span>

<span data-ttu-id="5c862-3400">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-3400">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3401">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3401">Pattern</span></span>

<span data-ttu-id="5c862-3402">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3402">18 letters and digits:</span></span>
- <span data-ttu-id="5c862-3403">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="5c862-3403">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="5c862-3404">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="5c862-3404">One digit</span></span> 
- <span data-ttu-id="5c862-3405">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="5c862-3405">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="5c862-3406">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="5c862-3406">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="5c862-3407">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3407">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3408">Checksum</span></span>

<span data-ttu-id="5c862-3409">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3409">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3410">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3410">Definition</span></span>

<span data-ttu-id="5c862-3411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3412">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3412">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3413">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="5c862-3413">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="5c862-3414">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3414">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3415">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3415">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="5c862-3416">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="5c862-3416">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="5c862-3417">двла</span><span class="sxs-lookup"><span data-stu-id="5c862-3417">DVLA</span></span> 
- <span data-ttu-id="5c862-3418">light vans</span><span class="sxs-lookup"><span data-stu-id="5c862-3418">light vans</span></span> 
- <span data-ttu-id="5c862-3419">куадбикес</span><span class="sxs-lookup"><span data-stu-id="5c862-3419">quadbikes</span></span> 
- <span data-ttu-id="5c862-3420">motor cars</span><span class="sxs-lookup"><span data-stu-id="5c862-3420">motor cars</span></span> 
- <span data-ttu-id="5c862-3421">125cc</span><span class="sxs-lookup"><span data-stu-id="5c862-3421">125cc</span></span> 
- <span data-ttu-id="5c862-3422">сидекар</span><span class="sxs-lookup"><span data-stu-id="5c862-3422">sidecar</span></span> 
- <span data-ttu-id="5c862-3423">трициклес</span><span class="sxs-lookup"><span data-stu-id="5c862-3423">tricycles</span></span> 
- <span data-ttu-id="5c862-3424">моторциклес</span><span class="sxs-lookup"><span data-stu-id="5c862-3424">motorcycles</span></span> 
- <span data-ttu-id="5c862-3425">photocard licence</span><span class="sxs-lookup"><span data-stu-id="5c862-3425">photocard licence</span></span> 
- <span data-ttu-id="5c862-3426">learner drivers</span><span class="sxs-lookup"><span data-stu-id="5c862-3426">learner drivers</span></span> 
- <span data-ttu-id="5c862-3427">licence holder</span><span class="sxs-lookup"><span data-stu-id="5c862-3427">licence holder</span></span> 
- <span data-ttu-id="5c862-3428">licence holders</span><span class="sxs-lookup"><span data-stu-id="5c862-3428">licence holders</span></span> 
- <span data-ttu-id="5c862-3429">driving licences</span><span class="sxs-lookup"><span data-stu-id="5c862-3429">driving licences</span></span> 
- <span data-ttu-id="5c862-3430">driving licence</span><span class="sxs-lookup"><span data-stu-id="5c862-3430">driving licence</span></span> 
- <span data-ttu-id="5c862-3431">dual control car</span><span class="sxs-lookup"><span data-stu-id="5c862-3431">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="5c862-p143">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="5c862-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3434">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3434">Format</span></span>

<span data-ttu-id="5c862-3435">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-3435">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3436">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3436">Pattern</span></span>

<span data-ttu-id="5c862-3437">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="5c862-3437">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3438">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3438">Checksum</span></span>

<span data-ttu-id="5c862-3439">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3439">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3440">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3440">Definition</span></span>

<span data-ttu-id="5c862-3441">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3441">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3442">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3442">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3443">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="5c862-3443">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3444">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3444">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="5c862-3445">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="5c862-3445">Keyword_uk_electoral</span></span>

- <span data-ttu-id="5c862-3446">council nomination</span><span class="sxs-lookup"><span data-stu-id="5c862-3446">council nomination</span></span> 
- <span data-ttu-id="5c862-3447">nomination form</span><span class="sxs-lookup"><span data-stu-id="5c862-3447">nomination form</span></span> 
- <span data-ttu-id="5c862-3448">electoral register</span><span class="sxs-lookup"><span data-stu-id="5c862-3448">electoral register</span></span> 
- <span data-ttu-id="5c862-3449">electoral roll</span><span class="sxs-lookup"><span data-stu-id="5c862-3449">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="5c862-p144">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="5c862-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3452">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3452">Format</span></span>

<span data-ttu-id="5c862-3453">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="5c862-3453">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3454">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3454">Pattern</span></span>

<span data-ttu-id="5c862-3455">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3455">10-17 digits:</span></span>
- <span data-ttu-id="5c862-3456">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3456">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="5c862-3457">Пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-3457">A space</span></span> 
- <span data-ttu-id="5c862-3458">Три цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3458">Three digits</span></span> 
- <span data-ttu-id="5c862-3459">Пробел</span><span class="sxs-lookup"><span data-stu-id="5c862-3459">A space</span></span> 
- <span data-ttu-id="5c862-3460">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3460">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3461">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3461">Checksum</span></span>

<span data-ttu-id="5c862-3462">Да</span><span class="sxs-lookup"><span data-stu-id="5c862-3462">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3463">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3463">Definition</span></span>

<span data-ttu-id="5c862-3464">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3464">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3465">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3465">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3466">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-3466">One of the following is true:</span></span>
    - <span data-ttu-id="5c862-3467">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="5c862-3467">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="5c862-3468">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="5c862-3468">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="5c862-3469">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="5c862-3469">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="5c862-3470">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="5c862-3470">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3471">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3471">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="5c862-3472">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="5c862-3472">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="5c862-3473">national health service</span><span class="sxs-lookup"><span data-stu-id="5c862-3473">national health service</span></span> 
- <span data-ttu-id="5c862-3474">NHS</span><span class="sxs-lookup"><span data-stu-id="5c862-3474">nhs</span></span> 
- <span data-ttu-id="5c862-3475">health services authority</span><span class="sxs-lookup"><span data-stu-id="5c862-3475">health services authority</span></span> 
- <span data-ttu-id="5c862-3476">health authority</span><span class="sxs-lookup"><span data-stu-id="5c862-3476">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="5c862-3477">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="5c862-3477">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="5c862-3478">patient id</span><span class="sxs-lookup"><span data-stu-id="5c862-3478">patient id</span></span> 
- <span data-ttu-id="5c862-3479">patient identification</span><span class="sxs-lookup"><span data-stu-id="5c862-3479">patient identification</span></span> 
- <span data-ttu-id="5c862-3480">patient no</span><span class="sxs-lookup"><span data-stu-id="5c862-3480">patient no</span></span> 
- <span data-ttu-id="5c862-3481">patient number</span><span class="sxs-lookup"><span data-stu-id="5c862-3481">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="5c862-3482">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="5c862-3482">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="5c862-3483">ГРУПП</span><span class="sxs-lookup"><span data-stu-id="5c862-3483">GP</span></span> 
- <span data-ttu-id="5c862-3484">доб</span><span class="sxs-lookup"><span data-stu-id="5c862-3484">DOB</span></span> 
- <span data-ttu-id="5c862-3485">D. O. B</span><span class="sxs-lookup"><span data-stu-id="5c862-3485">D.O.B</span></span> 
- <span data-ttu-id="5c862-3486">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="5c862-3486">Date of Birth</span></span> 
- <span data-ttu-id="5c862-3487">Birth Date</span><span class="sxs-lookup"><span data-stu-id="5c862-3487">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="5c862-p145">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="5c862-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3490">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3490">Format</span></span>

<span data-ttu-id="5c862-3491">7 символов или 9 символов, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3491">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3492">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3492">Pattern</span></span>

<span data-ttu-id="5c862-3493">Два возможных шаблона:</span><span class="sxs-lookup"><span data-stu-id="5c862-3493">Two possible patterns:</span></span>

- <span data-ttu-id="5c862-3494">Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-3494">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="5c862-3495">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3495">Six digits</span></span>
- <span data-ttu-id="5c862-3496">"A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="5c862-3496">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="5c862-3497">OR</span><span class="sxs-lookup"><span data-stu-id="5c862-3497">OR</span></span>

- <span data-ttu-id="5c862-3498">Две буквы</span><span class="sxs-lookup"><span data-stu-id="5c862-3498">Two letters</span></span>
- <span data-ttu-id="5c862-3499">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3499">A space or dash</span></span>
- <span data-ttu-id="5c862-3500">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3500">Two digits</span></span>
- <span data-ttu-id="5c862-3501">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3501">A space or dash</span></span>
- <span data-ttu-id="5c862-3502">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3502">Two digits</span></span>
- <span data-ttu-id="5c862-3503">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3503">A space or dash</span></span>
- <span data-ttu-id="5c862-3504">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3504">Two digits</span></span>
- <span data-ttu-id="5c862-3505">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3505">A space or dash</span></span>
- <span data-ttu-id="5c862-3506">Значение "A", "B", "C" или "'D"</span><span class="sxs-lookup"><span data-stu-id="5c862-3506">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3507">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3507">Checksum</span></span>

<span data-ttu-id="5c862-3508">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3508">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3509">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3509">Definition</span></span>

<span data-ttu-id="5c862-3510">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3511">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3511">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3512">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="5c862-3512">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="5c862-3513">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3513">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3514">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3514">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3515">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="5c862-3515">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3516">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3516">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="5c862-3517">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="5c862-3517">Keyword_uk_nino</span></span>

- <span data-ttu-id="5c862-3518">national insurance number</span><span class="sxs-lookup"><span data-stu-id="5c862-3518">national insurance number</span></span> 
- <span data-ttu-id="5c862-3519">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="5c862-3519">national insurance contributions</span></span> 
- <span data-ttu-id="5c862-3520">protection act</span><span class="sxs-lookup"><span data-stu-id="5c862-3520">protection act</span></span> 
- <span data-ttu-id="5c862-3521">страхования</span><span class="sxs-lookup"><span data-stu-id="5c862-3521">insurance</span></span> 
- <span data-ttu-id="5c862-3522">social security number</span><span class="sxs-lookup"><span data-stu-id="5c862-3522">social security number</span></span> 
- <span data-ttu-id="5c862-3523">insurance application</span><span class="sxs-lookup"><span data-stu-id="5c862-3523">insurance application</span></span> 
- <span data-ttu-id="5c862-3524">medical application</span><span class="sxs-lookup"><span data-stu-id="5c862-3524">medical application</span></span> 
- <span data-ttu-id="5c862-3525">social insurance</span><span class="sxs-lookup"><span data-stu-id="5c862-3525">social insurance</span></span> 
- <span data-ttu-id="5c862-3526">medical attention</span><span class="sxs-lookup"><span data-stu-id="5c862-3526">medical attention</span></span> 
- <span data-ttu-id="5c862-3527">social security</span><span class="sxs-lookup"><span data-stu-id="5c862-3527">social security</span></span> 
- <span data-ttu-id="5c862-3528">great britain</span><span class="sxs-lookup"><span data-stu-id="5c862-3528">great britain</span></span> 
- <span data-ttu-id="5c862-3529">страхования</span><span class="sxs-lookup"><span data-stu-id="5c862-3529">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="5c862-p146">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="5c862-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3532">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3532">Format</span></span>

<span data-ttu-id="5c862-3533">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3534">Pattern</span></span>

<span data-ttu-id="5c862-3535">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="5c862-3535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3536">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3536">Checksum</span></span>

<span data-ttu-id="5c862-3537">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3537">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3538">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3538">Definition</span></span>

<span data-ttu-id="5c862-3539">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3540">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3540">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3541">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="5c862-3541">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3542">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3542">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="5c862-3543">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="5c862-3543">Keyword_passport</span></span>

- <span data-ttu-id="5c862-3544">Passport Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3544">Passport Number</span></span> 
- <span data-ttu-id="5c862-3545">Passport No</span><span class="sxs-lookup"><span data-stu-id="5c862-3545">Passport No</span></span> 
- <span data-ttu-id="5c862-3546">Passport#</span><span class="sxs-lookup"><span data-stu-id="5c862-3546">Passport #</span></span> 
- <span data-ttu-id="5c862-3547">Службу #</span><span class="sxs-lookup"><span data-stu-id="5c862-3547">Passport#</span></span> 
- <span data-ttu-id="5c862-3548">пасспортид</span><span class="sxs-lookup"><span data-stu-id="5c862-3548">PassportID</span></span> 
- <span data-ttu-id="5c862-3549">пасспортно</span><span class="sxs-lookup"><span data-stu-id="5c862-3549">Passportno</span></span> 
- <span data-ttu-id="5c862-3550">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="5c862-3550">passportnumber</span></span> 
- <span data-ttu-id="5c862-3551">パスポート</span><span class="sxs-lookup"><span data-stu-id="5c862-3551">パスポート</span></span> 
- <span data-ttu-id="5c862-3552">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="5c862-3552">パスポート番号</span></span> 
- <span data-ttu-id="5c862-3553">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="5c862-3553">パスポートのNum</span></span> 
- <span data-ttu-id="5c862-3554">パスポート #</span><span class="sxs-lookup"><span data-stu-id="5c862-3554">パスポート＃</span></span> 
- <span data-ttu-id="5c862-3555">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="5c862-3555">Numéro de passeport</span></span> 
- <span data-ttu-id="5c862-3556">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="5c862-3556">Passeport n °</span></span> 
- <span data-ttu-id="5c862-3557">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="5c862-3557">Passeport Non</span></span> 
- <span data-ttu-id="5c862-3558">Passeport#</span><span class="sxs-lookup"><span data-stu-id="5c862-3558">Passeport #</span></span> 
- <span data-ttu-id="5c862-3559">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="5c862-3559">Passeport#</span></span> 
- <span data-ttu-id="5c862-3560">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="5c862-3560">PasseportNon</span></span> 
- <span data-ttu-id="5c862-3561">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="5c862-3561">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="5c862-3562">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="5c862-3562">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3563">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3563">Format</span></span>

<span data-ttu-id="5c862-3564">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3564">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3565">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3565">Pattern</span></span>

<span data-ttu-id="5c862-3566">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3566">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3567">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3567">Checksum</span></span>

<span data-ttu-id="5c862-3568">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3568">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3569">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3569">Definition</span></span>

<span data-ttu-id="5c862-3570">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3571">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3571">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3572">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="5c862-3572">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="5c862-3573">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3573">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="5c862-3574">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="5c862-3574">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="5c862-3575">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3575">Checking Account Number</span></span> 
- <span data-ttu-id="5c862-3576">Checking Account</span><span class="sxs-lookup"><span data-stu-id="5c862-3576">Checking Account</span></span> 
- <span data-ttu-id="5c862-3577">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-3577">Checking Account #</span></span> 
- <span data-ttu-id="5c862-3578">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3578">Checking Acct Number</span></span> 
- <span data-ttu-id="5c862-3579">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-3579">Checking Acct #</span></span> 
- <span data-ttu-id="5c862-3580">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3580">Checking Acct No.</span></span> 
- <span data-ttu-id="5c862-3581">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3581">Checking Account No.</span></span> 
- <span data-ttu-id="5c862-3582">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3582">Bank Account Number</span></span> 
- <span data-ttu-id="5c862-3583">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-3583">Bank Account #</span></span> 
- <span data-ttu-id="5c862-3584">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3584">Bank Acct Number</span></span> 
- <span data-ttu-id="5c862-3585">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-3585">Bank Acct #</span></span> 
- <span data-ttu-id="5c862-3586">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3586">Bank Acct No.</span></span> 
- <span data-ttu-id="5c862-3587">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3587">Bank Account No.</span></span> 
- <span data-ttu-id="5c862-3588">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3588">Savings Account Number</span></span> 
- <span data-ttu-id="5c862-3589">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="5c862-3589">Savings Account.</span></span> 
- <span data-ttu-id="5c862-3590">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-3590">Savings Account #</span></span> 
- <span data-ttu-id="5c862-3591">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3591">Savings Acct Number</span></span> 
- <span data-ttu-id="5c862-3592">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-3592">Savings Acct #</span></span> 
- <span data-ttu-id="5c862-3593">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3593">Savings Acct No.</span></span> 
- <span data-ttu-id="5c862-3594">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3594">Savings Account No.</span></span> 
- <span data-ttu-id="5c862-3595">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3595">Debit Account Number</span></span> 
- <span data-ttu-id="5c862-3596">Debit Account</span><span class="sxs-lookup"><span data-stu-id="5c862-3596">Debit Account</span></span> 
- <span data-ttu-id="5c862-3597">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="5c862-3597">Debit Account #</span></span> 
- <span data-ttu-id="5c862-3598">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="5c862-3598">Debit Acct Number</span></span> 
- <span data-ttu-id="5c862-3599">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="5c862-3599">Debit Acct #</span></span> 
- <span data-ttu-id="5c862-3600">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3600">Debit Acct No.</span></span> 
- <span data-ttu-id="5c862-3601">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="5c862-3601">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="5c862-3602">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="5c862-3602">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3603">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3603">Format</span></span>

<span data-ttu-id="5c862-3604">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="5c862-3604">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3605">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3605">Pattern</span></span>

<span data-ttu-id="5c862-3606">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="5c862-3606">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="5c862-3607">Девять цифр, отформатированных как DDD DDD DDD, будут совпадают.</span><span class="sxs-lookup"><span data-stu-id="5c862-3607">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="5c862-3608">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="5c862-3608">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3609">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3609">Checksum</span></span>

<span data-ttu-id="5c862-3610">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3610">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3611">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3611">Definition</span></span>

<span data-ttu-id="5c862-3612">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3612">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3613">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3613">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3614">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="5c862-3614">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="5c862-3615">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="5c862-3615">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="5c862-3616">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3616">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3617">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="5c862-3617">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3618">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="5c862-3618">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="5c862-3619">находится ключевое слово из Keyword_us_drivers_license_abbreviations.</span><span class="sxs-lookup"><span data-stu-id="5c862-3619">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="5c862-3620">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="5c862-3620">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3621">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3621">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="5c862-3622">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="5c862-3622">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="5c862-3623">DL</span><span class="sxs-lookup"><span data-stu-id="5c862-3623">DL</span></span> 
- <span data-ttu-id="5c862-3624">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="5c862-3624">DLS</span></span> 
- <span data-ttu-id="5c862-3625">кдл</span><span class="sxs-lookup"><span data-stu-id="5c862-3625">CDL</span></span> 
- <span data-ttu-id="5c862-3626">кдлс</span><span class="sxs-lookup"><span data-stu-id="5c862-3626">CDLS</span></span> 
- <span data-ttu-id="5c862-3627">ID</span><span class="sxs-lookup"><span data-stu-id="5c862-3627">ID</span></span> 
- <span data-ttu-id="5c862-3628">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="5c862-3628">IDs</span></span> 
- <span data-ttu-id="5c862-3629">DL #</span><span class="sxs-lookup"><span data-stu-id="5c862-3629">DL#</span></span> 
- <span data-ttu-id="5c862-3630">БИБЛИОТЕК #</span><span class="sxs-lookup"><span data-stu-id="5c862-3630">DLS#</span></span> 
- <span data-ttu-id="5c862-3631">кдл #</span><span class="sxs-lookup"><span data-stu-id="5c862-3631">CDL#</span></span> 
- <span data-ttu-id="5c862-3632">кдлс #</span><span class="sxs-lookup"><span data-stu-id="5c862-3632">CDLS#</span></span> 
- <span data-ttu-id="5c862-3633">КОДОВ #</span><span class="sxs-lookup"><span data-stu-id="5c862-3633">ID#</span></span>
- <span data-ttu-id="5c862-3634">Идентификаторы #</span><span class="sxs-lookup"><span data-stu-id="5c862-3634">IDs#</span></span> 
- <span data-ttu-id="5c862-3635">ID number</span><span class="sxs-lookup"><span data-stu-id="5c862-3635">ID number</span></span> 
- <span data-ttu-id="5c862-3636">ID numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-3636">ID numbers</span></span> 
- <span data-ttu-id="5c862-3637">лик</span><span class="sxs-lookup"><span data-stu-id="5c862-3637">LIC</span></span> 
- <span data-ttu-id="5c862-3638">лик #</span><span class="sxs-lookup"><span data-stu-id="5c862-3638">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="5c862-3639">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="5c862-3639">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="5c862-3640">дриверлик</span><span class="sxs-lookup"><span data-stu-id="5c862-3640">DriverLic</span></span> 
- <span data-ttu-id="5c862-3641">дриверликс</span><span class="sxs-lookup"><span data-stu-id="5c862-3641">DriverLics</span></span> 
- <span data-ttu-id="5c862-3642">дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-3642">DriverLicense</span></span> 
- <span data-ttu-id="5c862-3643">дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-3643">DriverLicenses</span></span> 
- <span data-ttu-id="5c862-3644">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-3644">Driver Lic</span></span> 
- <span data-ttu-id="5c862-3645">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-3645">Driver Lics</span></span> 
- <span data-ttu-id="5c862-3646">Driver License</span><span class="sxs-lookup"><span data-stu-id="5c862-3646">Driver License</span></span> 
- <span data-ttu-id="5c862-3647">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-3647">Driver Licenses</span></span> 
- <span data-ttu-id="5c862-3648">дриверслик</span><span class="sxs-lookup"><span data-stu-id="5c862-3648">DriversLic</span></span> 
- <span data-ttu-id="5c862-3649">дриверсликс</span><span class="sxs-lookup"><span data-stu-id="5c862-3649">DriversLics</span></span> 
- <span data-ttu-id="5c862-3650">дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-3650">DriversLicense</span></span> 
- <span data-ttu-id="5c862-3651">дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-3651">DriversLicenses</span></span> 
- <span data-ttu-id="5c862-3652">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-3652">Drivers Lic</span></span> 
- <span data-ttu-id="5c862-3653">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-3653">Drivers Lics</span></span> 
- <span data-ttu-id="5c862-3654">Drivers License</span><span class="sxs-lookup"><span data-stu-id="5c862-3654">Drivers License</span></span> 
- <span data-ttu-id="5c862-3655">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-3655">Drivers Licenses</span></span> 
- <span data-ttu-id="5c862-3656">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="5c862-3656">Driver'Lic</span></span> 
- <span data-ttu-id="5c862-3657">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="5c862-3657">Driver'Lics</span></span> 
- <span data-ttu-id="5c862-3658">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="5c862-3658">Driver'License</span></span> 
- <span data-ttu-id="5c862-3659">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-3659">Driver'Licenses</span></span> 
- <span data-ttu-id="5c862-3660">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-3660">Driver' Lic</span></span> 
- <span data-ttu-id="5c862-3661">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-3661">Driver' Lics</span></span> 
- <span data-ttu-id="5c862-3662">Driver' License</span><span class="sxs-lookup"><span data-stu-id="5c862-3662">Driver' License</span></span> 
- <span data-ttu-id="5c862-3663">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-3663">Driver' Licenses</span></span>
- <span data-ttu-id="5c862-3664">дривер'слик</span><span class="sxs-lookup"><span data-stu-id="5c862-3664">Driver'sLic</span></span> 
- <span data-ttu-id="5c862-3665">дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="5c862-3665">Driver'sLics</span></span> 
- <span data-ttu-id="5c862-3666">дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="5c862-3666">Driver'sLicense</span></span> 
- <span data-ttu-id="5c862-3667">дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="5c862-3667">Driver'sLicenses</span></span> 
- <span data-ttu-id="5c862-3668">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="5c862-3668">Driver's Lic</span></span> 
- <span data-ttu-id="5c862-3669">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="5c862-3669">Driver's Lics</span></span> 
- <span data-ttu-id="5c862-3670">Driver's License</span><span class="sxs-lookup"><span data-stu-id="5c862-3670">Driver's License</span></span> 
- <span data-ttu-id="5c862-3671">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="5c862-3671">Driver's Licenses</span></span> 
- <span data-ttu-id="5c862-3672">identification number</span><span class="sxs-lookup"><span data-stu-id="5c862-3672">identification number</span></span> 
- <span data-ttu-id="5c862-3673">identification numbers</span><span class="sxs-lookup"><span data-stu-id="5c862-3673">identification numbers</span></span> 
- <span data-ttu-id="5c862-3674">identification #</span><span class="sxs-lookup"><span data-stu-id="5c862-3674">identification #</span></span> 
- <span data-ttu-id="5c862-3675">id card</span><span class="sxs-lookup"><span data-stu-id="5c862-3675">id card</span></span> 
- <span data-ttu-id="5c862-3676">id cards</span><span class="sxs-lookup"><span data-stu-id="5c862-3676">id cards</span></span> 
- <span data-ttu-id="5c862-3677">identification card</span><span class="sxs-lookup"><span data-stu-id="5c862-3677">identification card</span></span> 
- <span data-ttu-id="5c862-3678">identification cards</span><span class="sxs-lookup"><span data-stu-id="5c862-3678">identification cards</span></span> 
- <span data-ttu-id="5c862-3679">дриверлик #</span><span class="sxs-lookup"><span data-stu-id="5c862-3679">DriverLic#</span></span> 
- <span data-ttu-id="5c862-3680">дриверликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-3680">DriverLics#</span></span> 
- <span data-ttu-id="5c862-3681">дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-3681">DriverLicense#</span></span> 
- <span data-ttu-id="5c862-3682">дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-3682">DriverLicenses#</span></span> 
- <span data-ttu-id="5c862-3683">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-3683">Driver Lic#</span></span> 
- <span data-ttu-id="5c862-3684">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-3684">Driver Lics#</span></span> 
- <span data-ttu-id="5c862-3685">Driver License#</span><span class="sxs-lookup"><span data-stu-id="5c862-3685">Driver License#</span></span> 
- <span data-ttu-id="5c862-3686">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-3686">Driver Licenses#</span></span> 
- <span data-ttu-id="5c862-3687">дриверслик #</span><span class="sxs-lookup"><span data-stu-id="5c862-3687">DriversLic#</span></span> 
- <span data-ttu-id="5c862-3688">дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-3688">DriversLics#</span></span> 
- <span data-ttu-id="5c862-3689">дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-3689">DriversLicense#</span></span> 
- <span data-ttu-id="5c862-3690">дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-3690">DriversLicenses#</span></span> 
- <span data-ttu-id="5c862-3691">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-3691">Drivers Lic#</span></span> 
- <span data-ttu-id="5c862-3692">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-3692">Drivers Lics#</span></span> 
- <span data-ttu-id="5c862-3693">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="5c862-3693">Drivers License#</span></span> 
- <span data-ttu-id="5c862-3694">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-3694">Drivers Licenses#</span></span> 
- <span data-ttu-id="5c862-3695">Driver ' LIC #</span><span class="sxs-lookup"><span data-stu-id="5c862-3695">Driver'Lic#</span></span> 
- <span data-ttu-id="5c862-3696">Driver ' LICS #</span><span class="sxs-lookup"><span data-stu-id="5c862-3696">Driver'Lics#</span></span> 
- <span data-ttu-id="5c862-3697">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="5c862-3697">Driver'License#</span></span> 
- <span data-ttu-id="5c862-3698">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="5c862-3698">Driver'Licenses#</span></span> 
- <span data-ttu-id="5c862-3699">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-3699">Driver' Lic#</span></span> 
- <span data-ttu-id="5c862-3700">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-3700">Driver' Lics#</span></span> 
- <span data-ttu-id="5c862-3701">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="5c862-3701">Driver' License#</span></span> 
- <span data-ttu-id="5c862-3702">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-3702">Driver' Licenses#</span></span> 
- <span data-ttu-id="5c862-3703">дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="5c862-3703">Driver'sLic#</span></span> 
- <span data-ttu-id="5c862-3704">дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="5c862-3704">Driver'sLics#</span></span> 
- <span data-ttu-id="5c862-3705">дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="5c862-3705">Driver'sLicense#</span></span> 
- <span data-ttu-id="5c862-3706">дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="5c862-3706">Driver'sLicenses#</span></span> 
- <span data-ttu-id="5c862-3707">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="5c862-3707">Driver's Lic#</span></span> 
- <span data-ttu-id="5c862-3708">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="5c862-3708">Driver's Lics#</span></span> 
- <span data-ttu-id="5c862-3709">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="5c862-3709">Driver's License#</span></span> 
- <span data-ttu-id="5c862-3710">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="5c862-3710">Driver's Licenses#</span></span> 
- <span data-ttu-id="5c862-3711">id card#</span><span class="sxs-lookup"><span data-stu-id="5c862-3711">id card#</span></span> 
- <span data-ttu-id="5c862-3712">id cards#</span><span class="sxs-lookup"><span data-stu-id="5c862-3712">id cards#</span></span> 
- <span data-ttu-id="5c862-3713">identification card#</span><span class="sxs-lookup"><span data-stu-id="5c862-3713">identification card#</span></span> 
- <span data-ttu-id="5c862-3714">identification cards#</span><span class="sxs-lookup"><span data-stu-id="5c862-3714">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="5c862-3715">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="5c862-3715">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="5c862-3716">Аббревиатура штата (например, NY)</span><span class="sxs-lookup"><span data-stu-id="5c862-3716">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="5c862-3717">Название штата (например, New York)</span><span class="sxs-lookup"><span data-stu-id="5c862-3717">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="5c862-3718">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="5c862-3718">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3719">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3719">Format</span></span>

<span data-ttu-id="5c862-3720">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="5c862-3720">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3721">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3721">Pattern</span></span>

<span data-ttu-id="5c862-3722">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="5c862-3722">Formatted:</span></span>
- <span data-ttu-id="5c862-3723">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="5c862-3723">The digit "9"</span></span> 
- <span data-ttu-id="5c862-3724">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3724">Two digits</span></span> 
- <span data-ttu-id="5c862-3725">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3725">A space or dash</span></span> 
- <span data-ttu-id="5c862-3726">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="5c862-3726">A "7" or "8"</span></span> 
- <span data-ttu-id="5c862-3727">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="5c862-3727">A digit</span></span> 
- <span data-ttu-id="5c862-3728">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="5c862-3728">A space, or dash</span></span> 
- <span data-ttu-id="5c862-3729">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3729">Four digits</span></span>

<span data-ttu-id="5c862-3730">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="5c862-3730">Unformatted:</span></span>
- <span data-ttu-id="5c862-3731">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="5c862-3731">The digit "9"</span></span> 
- <span data-ttu-id="5c862-3732">Две цифры</span><span class="sxs-lookup"><span data-stu-id="5c862-3732">Two digits</span></span> 
- <span data-ttu-id="5c862-3733">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="5c862-3733">A "7" or "8"</span></span> 
- <span data-ttu-id="5c862-3734">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="5c862-3734">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3735">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3735">Checksum</span></span>

<span data-ttu-id="5c862-3736">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3736">No</span></span>

### <a name="definition"></a><span data-ttu-id="5c862-3737">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3737">Definition</span></span>

<span data-ttu-id="5c862-3738">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3738">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3739">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3739">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3740">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-3740">At least one of the following is true:</span></span>
    - <span data-ttu-id="5c862-3741">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="5c862-3741">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="5c862-3742">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="5c862-3742">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="5c862-3743">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-3743">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="5c862-3744">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="5c862-3744">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="5c862-3745">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3745">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3746">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3746">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3747">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="5c862-3747">At least one of the following is true:</span></span>
    - <span data-ttu-id="5c862-3748">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="5c862-3748">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="5c862-3749">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="5c862-3749">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="5c862-3750">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="5c862-3750">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3751">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3751">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="5c862-3752">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="5c862-3752">Keyword_itin</span></span>

- <span data-ttu-id="5c862-3753">дубликат</span><span class="sxs-lookup"><span data-stu-id="5c862-3753">taxpayer</span></span> 
- <span data-ttu-id="5c862-3754">tax id</span><span class="sxs-lookup"><span data-stu-id="5c862-3754">tax id</span></span> 
- <span data-ttu-id="5c862-3755">tax identification</span><span class="sxs-lookup"><span data-stu-id="5c862-3755">tax identification</span></span> 
- <span data-ttu-id="5c862-3756">SharePointв</span><span class="sxs-lookup"><span data-stu-id="5c862-3756">itin</span></span> 
- <span data-ttu-id="5c862-3757">SSN</span><span class="sxs-lookup"><span data-stu-id="5c862-3757">ssn</span></span> 
- <span data-ttu-id="5c862-3758">ИНН</span><span class="sxs-lookup"><span data-stu-id="5c862-3758">tin</span></span> 
- <span data-ttu-id="5c862-3759">social security</span><span class="sxs-lookup"><span data-stu-id="5c862-3759">social security</span></span> 
- <span data-ttu-id="5c862-3760">tax payer</span><span class="sxs-lookup"><span data-stu-id="5c862-3760">tax payer</span></span> 
- <span data-ttu-id="5c862-3761">итинс</span><span class="sxs-lookup"><span data-stu-id="5c862-3761">itins</span></span> 
- <span data-ttu-id="5c862-3762">такси</span><span class="sxs-lookup"><span data-stu-id="5c862-3762">taxid</span></span> 
- <span data-ttu-id="5c862-3763">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="5c862-3763">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="5c862-3764">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="5c862-3764">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="5c862-3765">Лицензия</span><span class="sxs-lookup"><span data-stu-id="5c862-3765">License</span></span> 
- <span data-ttu-id="5c862-3766">DL</span><span class="sxs-lookup"><span data-stu-id="5c862-3766">DL</span></span> 
- <span data-ttu-id="5c862-3767">доб</span><span class="sxs-lookup"><span data-stu-id="5c862-3767">DOB</span></span> 
- <span data-ttu-id="5c862-3768">Birthdate</span><span class="sxs-lookup"><span data-stu-id="5c862-3768">Birthdate</span></span> 
- <span data-ttu-id="5c862-3769">День рождения </span><span class="sxs-lookup"><span data-stu-id="5c862-3769">Birthday</span></span> 
- <span data-ttu-id="5c862-3770">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="5c862-3770">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="5c862-3771">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="5c862-3771">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="5c862-3772">Format</span><span class="sxs-lookup"><span data-stu-id="5c862-3772">Format</span></span>

<span data-ttu-id="5c862-3773">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="5c862-3773">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="5c862-3774">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="5c862-3774">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="5c862-3775">Шаблон</span><span class="sxs-lookup"><span data-stu-id="5c862-3775">Pattern</span></span>

<span data-ttu-id="5c862-3776">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="5c862-3776">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="5c862-3777">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="5c862-3777">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="5c862-3778">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="5c862-3778">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="5c862-3779">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="5c862-3779">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="5c862-3780">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="5c862-3780">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="5c862-3781">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="5c862-3781">Checksum</span></span>

<span data-ttu-id="5c862-3782">Нет</span><span class="sxs-lookup"><span data-stu-id="5c862-3782">No</span></span>


### <a name="definition"></a><span data-ttu-id="5c862-3783">Определение</span><span class="sxs-lookup"><span data-stu-id="5c862-3783">Definition</span></span>

<span data-ttu-id="5c862-3784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3785">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3785">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3786">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="5c862-3786">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="5c862-3787">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3788">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3788">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3789">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="5c862-3789">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="5c862-3790">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3790">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3791">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3791">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3792">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="5c862-3792">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="5c862-3793">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3793">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="5c862-3794">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="5c862-3794">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="5c862-3795">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3795">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="5c862-3796">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="5c862-3796">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="5c862-3797">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="5c862-3797">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="5c862-3798">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="5c862-3798">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="5c862-3799">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="5c862-3799">Keyword_ssn</span></span>

- <span data-ttu-id="5c862-3800">Social Security</span><span class="sxs-lookup"><span data-stu-id="5c862-3800">Social Security</span></span> 
- <span data-ttu-id="5c862-3801">Social Security#</span><span class="sxs-lookup"><span data-stu-id="5c862-3801">Social Security#</span></span> 
- <span data-ttu-id="5c862-3802">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="5c862-3802">Soc Sec</span></span> 
- <span data-ttu-id="5c862-3803">SSN</span><span class="sxs-lookup"><span data-stu-id="5c862-3803">SSN</span></span> 
- <span data-ttu-id="5c862-3804">SSNS</span><span class="sxs-lookup"><span data-stu-id="5c862-3804">SSNS</span></span> 
- <span data-ttu-id="5c862-3805">SSN #</span><span class="sxs-lookup"><span data-stu-id="5c862-3805">SSN#</span></span> 
- <span data-ttu-id="5c862-3806">НН #</span><span class="sxs-lookup"><span data-stu-id="5c862-3806">SS#</span></span> 
- <span data-ttu-id="5c862-3807">SSID</span><span class="sxs-lookup"><span data-stu-id="5c862-3807">SSID</span></span> 
   

