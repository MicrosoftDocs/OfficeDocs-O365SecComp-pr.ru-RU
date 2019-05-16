---
title: Что позволяют искать типы конфиденциальной информации
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/29/2018
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
ms.openlocfilehash: dc2958af5b64f9e9318faab5d55ed340404f1857
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077555"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="14da3-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="14da3-104">What the sensitive information types look for</span></span>

<span data-ttu-id="14da3-105">Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="14da3-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="14da3-106">В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.</span><span class="sxs-lookup"><span data-stu-id="14da3-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="14da3-107">Тип конфиденциальной информации определяется шаблоном, который можно идентифицировать регулярным выражением или функцией.</span><span class="sxs-lookup"><span data-stu-id="14da3-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="14da3-108">Кроме того, для идентификации типа конфиденциальной информации могут использоваться подкрепляющие доказательства, такие как ключевые слова и контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="14da3-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="14da3-109">Уровень вероятности и расположение слов и знаков также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="14da3-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="14da3-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="14da3-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-111">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-111">Format</span></span>

<span data-ttu-id="14da3-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="14da3-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-113">Pattern</span></span>

<span data-ttu-id="14da3-114">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="14da3-114">Formatted:</span></span>
- <span data-ttu-id="14da3-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="14da3-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="14da3-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-116">A hyphen</span></span>
- <span data-ttu-id="14da3-117">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-117">Four digits</span></span>
- <span data-ttu-id="14da3-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-118">A hyphen</span></span>
- <span data-ttu-id="14da3-119">цифра.</span><span class="sxs-lookup"><span data-stu-id="14da3-119">A digit</span></span>

<span data-ttu-id="14da3-120">Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8.</span><span class="sxs-lookup"><span data-stu-id="14da3-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="14da3-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-121">Checksum</span></span>

<span data-ttu-id="14da3-122">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-123">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-123">Definition</span></span>

<span data-ttu-id="14da3-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="14da3-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="14da3-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="14da3-128">Кэйворд_аба_раутинг</span><span class="sxs-lookup"><span data-stu-id="14da3-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="14da3-129">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="14da3-129">aba</span></span>
- <span data-ttu-id="14da3-130">aba#</span><span class="sxs-lookup"><span data-stu-id="14da3-130">aba #</span></span>
- <span data-ttu-id="14da3-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="14da3-131">aba routing #</span></span>
- <span data-ttu-id="14da3-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="14da3-132">aba routing number</span></span>
- <span data-ttu-id="14da3-133">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="14da3-133">aba#</span></span>
- <span data-ttu-id="14da3-134">абараутинг #</span><span class="sxs-lookup"><span data-stu-id="14da3-134">abarouting#</span></span>
- <span data-ttu-id="14da3-135">aba number</span><span class="sxs-lookup"><span data-stu-id="14da3-135">aba number</span></span>
- <span data-ttu-id="14da3-136">абараутингнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-136">abaroutingnumber</span></span>
- <span data-ttu-id="14da3-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="14da3-137">american bank association routing #</span></span>
- <span data-ttu-id="14da3-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="14da3-138">american bank association routing number</span></span>
- <span data-ttu-id="14da3-139">американбанкассоЦиатионраутинг #</span><span class="sxs-lookup"><span data-stu-id="14da3-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="14da3-140">американбанкассоЦиатионраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="14da3-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="14da3-141">bank routing number</span></span>
- <span data-ttu-id="14da3-142">банкраутинг #</span><span class="sxs-lookup"><span data-stu-id="14da3-142">bankrouting#</span></span>
- <span data-ttu-id="14da3-143">банкраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-143">bankroutingnumber</span></span>
- <span data-ttu-id="14da3-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="14da3-144">routing transit number</span></span>
- <span data-ttu-id="14da3-145">РТН</span><span class="sxs-lookup"><span data-stu-id="14da3-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="14da3-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="14da3-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-147">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-147">Format</span></span>

<span data-ttu-id="14da3-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="14da3-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-149">Pattern</span></span>

<span data-ttu-id="14da3-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-150">Eight digits:</span></span>
- <span data-ttu-id="14da3-151">две цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-151">Two digits</span></span>
- <span data-ttu-id="14da3-152">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-152">A period</span></span>
- <span data-ttu-id="14da3-153">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-153">Three digits</span></span>
- <span data-ttu-id="14da3-154">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-154">A period</span></span>
- <span data-ttu-id="14da3-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-156">Checksum</span></span>

<span data-ttu-id="14da3-157">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-158">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-158">Definition</span></span>

<span data-ttu-id="14da3-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="14da3-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="14da3-163">Кэйворд_аржентина_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="14da3-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="14da3-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="14da3-165">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="14da3-165">Identity</span></span> 
- <span data-ttu-id="14da3-166">Идентификация национальной идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="14da3-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="14da3-167">DNI</span><span class="sxs-lookup"><span data-stu-id="14da3-167">DNI</span></span> 
- <span data-ttu-id="14da3-168">Национальная реестр пользователей NIC</span><span class="sxs-lookup"><span data-stu-id="14da3-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="14da3-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="14da3-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="14da3-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="14da3-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="14da3-171">ИДЕНТИДАД</span><span class="sxs-lookup"><span data-stu-id="14da3-171">Identidad</span></span> 
- <span data-ttu-id="14da3-172">ИдентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="14da3-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="14da3-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="14da3-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-174">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-174">Format</span></span>

<span data-ttu-id="14da3-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="14da3-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-176">Pattern</span></span>

<span data-ttu-id="14da3-177">Номер счета состоит из 6–10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="14da3-178">Номер филиала государственного банка Австралии</span><span class="sxs-lookup"><span data-stu-id="14da3-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="14da3-179">три цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-179">Three digits</span></span> 
- <span data-ttu-id="14da3-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-180">A hyphen</span></span> 
- <span data-ttu-id="14da3-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-182">Checksum</span></span>

<span data-ttu-id="14da3-183">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-184">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-184">Definition</span></span>

<span data-ttu-id="14da3-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="14da3-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="14da3-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="14da3-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="14da3-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="14da3-193">Кэйворд_аустралиа_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="14da3-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="14da3-194">swift bank code</span></span>
- <span data-ttu-id="14da3-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="14da3-195">correspondent bank</span></span>
- <span data-ttu-id="14da3-196">base currency</span><span class="sxs-lookup"><span data-stu-id="14da3-196">base currency</span></span>
- <span data-ttu-id="14da3-197">usa account</span><span class="sxs-lookup"><span data-stu-id="14da3-197">usa account</span></span>
- <span data-ttu-id="14da3-198">holder address</span><span class="sxs-lookup"><span data-stu-id="14da3-198">holder address</span></span>
- <span data-ttu-id="14da3-199">bank address</span><span class="sxs-lookup"><span data-stu-id="14da3-199">bank address</span></span>
- <span data-ttu-id="14da3-200">information account</span><span class="sxs-lookup"><span data-stu-id="14da3-200">information account</span></span>
- <span data-ttu-id="14da3-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="14da3-201">fund transfers</span></span>
- <span data-ttu-id="14da3-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="14da3-202">bank charges</span></span>
- <span data-ttu-id="14da3-203">bank details</span><span class="sxs-lookup"><span data-stu-id="14da3-203">bank details</span></span>
- <span data-ttu-id="14da3-204">banking information</span><span class="sxs-lookup"><span data-stu-id="14da3-204">banking information</span></span>
- <span data-ttu-id="14da3-205">full names</span><span class="sxs-lookup"><span data-stu-id="14da3-205">full names</span></span>
- <span data-ttu-id="14da3-206">иаеа</span><span class="sxs-lookup"><span data-stu-id="14da3-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="14da3-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="14da3-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-208">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-208">Format</span></span>

<span data-ttu-id="14da3-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-210">Pattern</span></span>

<span data-ttu-id="14da3-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="14da3-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-213">две цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-213">Two digits</span></span> 
- <span data-ttu-id="14da3-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="14da3-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="14da3-215">OR</span><span class="sxs-lookup"><span data-stu-id="14da3-215">OR</span></span>

- <span data-ttu-id="14da3-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-217">4-9 digits</span></span>

<span data-ttu-id="14da3-218">OR</span><span class="sxs-lookup"><span data-stu-id="14da3-218">OR</span></span>

- <span data-ttu-id="14da3-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="14da3-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-220">Checksum</span></span>

<span data-ttu-id="14da3-221">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-222">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-222">Definition</span></span>

<span data-ttu-id="14da3-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="14da3-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="14da3-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="14da3-228">Кэйворд_аустралиа_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="14da3-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="14da3-229">international driving permits</span></span>
- <span data-ttu-id="14da3-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="14da3-230">australian automobile association</span></span>
- <span data-ttu-id="14da3-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="14da3-231">international driving permit</span></span>
- <span data-ttu-id="14da3-232">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="14da3-232">DriverLicence</span></span>
- <span data-ttu-id="14da3-233">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="14da3-233">DriverLicences</span></span>
- <span data-ttu-id="14da3-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-234">Driver Lic</span></span>
- <span data-ttu-id="14da3-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-235">Driver Licence</span></span>
- <span data-ttu-id="14da3-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-236">Driver Licences</span></span>
- <span data-ttu-id="14da3-237">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="14da3-237">DriversLic</span></span>
- <span data-ttu-id="14da3-238">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="14da3-238">DriversLicence</span></span>
- <span data-ttu-id="14da3-239">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="14da3-239">DriversLicences</span></span>
- <span data-ttu-id="14da3-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-240">Drivers Lic</span></span>
- <span data-ttu-id="14da3-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-241">Drivers Lics</span></span>
- <span data-ttu-id="14da3-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-242">Drivers Licence</span></span>
- <span data-ttu-id="14da3-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-243">Drivers Licences</span></span>
- <span data-ttu-id="14da3-244">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="14da3-244">Driver'Lic</span></span>
- <span data-ttu-id="14da3-245">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="14da3-245">Driver'Lics</span></span>
- <span data-ttu-id="14da3-246">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-246">Driver'Licence</span></span>
- <span data-ttu-id="14da3-247">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-247">Driver'Licences</span></span>
- <span data-ttu-id="14da3-248">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-248">Driver' Lic</span></span>
- <span data-ttu-id="14da3-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-249">Driver' Lics</span></span>
- <span data-ttu-id="14da3-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-250">Driver' Licence</span></span>
- <span data-ttu-id="14da3-251">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-251">Driver' Licences</span></span>
- <span data-ttu-id="14da3-252">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="14da3-252">Driver'sLic</span></span>
- <span data-ttu-id="14da3-253">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="14da3-253">Driver'sLics</span></span>
- <span data-ttu-id="14da3-254">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="14da3-254">Driver'sLicence</span></span>
- <span data-ttu-id="14da3-255">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="14da3-255">Driver'sLicences</span></span>
- <span data-ttu-id="14da3-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-256">Driver's Lic</span></span>
- <span data-ttu-id="14da3-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-257">Driver's Lics</span></span>
- <span data-ttu-id="14da3-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-258">Driver's Licence</span></span>
- <span data-ttu-id="14da3-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-259">Driver's Licences</span></span>
- <span data-ttu-id="14da3-260">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="14da3-260">DriverLic#</span></span>
- <span data-ttu-id="14da3-261">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-261">DriverLics#</span></span>
- <span data-ttu-id="14da3-262">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="14da3-262">DriverLicence#</span></span>
- <span data-ttu-id="14da3-263">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="14da3-263">DriverLicences#</span></span>
- <span data-ttu-id="14da3-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-264">Driver Lic#</span></span>
- <span data-ttu-id="14da3-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-265">Driver Lics#</span></span>
- <span data-ttu-id="14da3-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-266">Driver Licence#</span></span>
- <span data-ttu-id="14da3-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-267">Driver Licences#</span></span>
- <span data-ttu-id="14da3-268">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="14da3-268">DriversLic#</span></span>
- <span data-ttu-id="14da3-269">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-269">DriversLics#</span></span>
- <span data-ttu-id="14da3-270">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="14da3-270">DriversLicence#</span></span>
- <span data-ttu-id="14da3-271">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="14da3-271">DriversLicences#</span></span>
- <span data-ttu-id="14da3-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-272">Drivers Lic#</span></span>
- <span data-ttu-id="14da3-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-273">Drivers Lics#</span></span>
- <span data-ttu-id="14da3-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-274">Drivers Licence#</span></span>
- <span data-ttu-id="14da3-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-275">Drivers Licences#</span></span>
- <span data-ttu-id="14da3-276">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="14da3-276">Driver'Lic#</span></span>
- <span data-ttu-id="14da3-277">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="14da3-277">Driver'Lics#</span></span>
- <span data-ttu-id="14da3-278">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-278">Driver'Licence#</span></span>
- <span data-ttu-id="14da3-279">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-279">Driver'Licences#</span></span>
- <span data-ttu-id="14da3-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-280">Driver' Lic#</span></span>
- <span data-ttu-id="14da3-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-281">Driver' Lics#</span></span>
- <span data-ttu-id="14da3-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-282">Driver' Licence#</span></span>
- <span data-ttu-id="14da3-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-283">Driver' Licences#</span></span>
- <span data-ttu-id="14da3-284">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="14da3-284">Driver'sLic#</span></span>
- <span data-ttu-id="14da3-285">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-285">Driver'sLics#</span></span>
- <span data-ttu-id="14da3-286">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="14da3-286">Driver'sLicence#</span></span>
- <span data-ttu-id="14da3-287">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="14da3-287">Driver'sLicences#</span></span>
- <span data-ttu-id="14da3-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-288">Driver's Lic#</span></span>
- <span data-ttu-id="14da3-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-289">Driver's Lics#</span></span>
- <span data-ttu-id="14da3-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-290">Driver's Licence#</span></span>
- <span data-ttu-id="14da3-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="14da3-292">Кэйворд_аустралиа_дриверс_лиценсе_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="14da3-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="14da3-293">AAA</span><span class="sxs-lookup"><span data-stu-id="14da3-293">aaa</span></span>
- <span data-ttu-id="14da3-294">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-294">DriverLicense</span></span>
- <span data-ttu-id="14da3-295">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-295">DriverLicenses</span></span>
- <span data-ttu-id="14da3-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="14da3-296">Driver License</span></span>
- <span data-ttu-id="14da3-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-297">Driver Licenses</span></span>
- <span data-ttu-id="14da3-298">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-298">DriversLicense</span></span>
- <span data-ttu-id="14da3-299">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-299">DriversLicenses</span></span>
- <span data-ttu-id="14da3-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="14da3-300">Drivers License</span></span>
- <span data-ttu-id="14da3-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-301">Drivers Licenses</span></span>
- <span data-ttu-id="14da3-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="14da3-302">Driver'License</span></span>
- <span data-ttu-id="14da3-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-303">Driver'Licenses</span></span>
- <span data-ttu-id="14da3-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="14da3-304">Driver' License</span></span>
- <span data-ttu-id="14da3-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-305">Driver' Licenses</span></span>
- <span data-ttu-id="14da3-306">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-306">Driver'sLicense</span></span>
- <span data-ttu-id="14da3-307">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-307">Driver'sLicenses</span></span>
- <span data-ttu-id="14da3-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="14da3-308">Driver's License</span></span>
- <span data-ttu-id="14da3-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-309">Driver's Licenses</span></span>
- <span data-ttu-id="14da3-310">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-310">DriverLicense#</span></span>
- <span data-ttu-id="14da3-311">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-311">DriverLicenses#</span></span>
- <span data-ttu-id="14da3-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="14da3-312">Driver License#</span></span>
- <span data-ttu-id="14da3-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-313">Driver Licenses#</span></span>
- <span data-ttu-id="14da3-314">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-314">DriversLicense#</span></span>
- <span data-ttu-id="14da3-315">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-315">DriversLicenses#</span></span>
- <span data-ttu-id="14da3-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="14da3-316">Drivers License#</span></span>
- <span data-ttu-id="14da3-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-317">Drivers Licenses#</span></span>
- <span data-ttu-id="14da3-318">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="14da3-318">Driver'License#</span></span>
- <span data-ttu-id="14da3-319">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-319">Driver'Licenses#</span></span>
- <span data-ttu-id="14da3-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="14da3-320">Driver' License#</span></span>
- <span data-ttu-id="14da3-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-321">Driver' Licenses#</span></span>
- <span data-ttu-id="14da3-322">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-322">Driver'sLicense#</span></span>
- <span data-ttu-id="14da3-323">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="14da3-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="14da3-324">Driver's License#</span></span>
- <span data-ttu-id="14da3-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="14da3-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="14da3-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-327">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-327">Format</span></span>

<span data-ttu-id="14da3-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-329">Pattern</span></span>

<span data-ttu-id="14da3-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-330">10-11 digits:</span></span>
- <span data-ttu-id="14da3-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="14da3-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="14da3-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="14da3-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="14da3-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="14da3-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="14da3-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-335">Checksum</span></span>

<span data-ttu-id="14da3-336">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-337">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-337">Definition</span></span>

<span data-ttu-id="14da3-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="14da3-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="14da3-341">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-341">The checksum passes.</span></span>

<span data-ttu-id="14da3-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="14da3-346">Кэйворд_аустралиа_медикал_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="14da3-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="14da3-347">bank account details</span></span>
- <span data-ttu-id="14da3-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="14da3-348">medicare payments</span></span>
- <span data-ttu-id="14da3-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="14da3-349">mortgage account</span></span>
- <span data-ttu-id="14da3-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="14da3-350">bank payments</span></span>
- <span data-ttu-id="14da3-351">information branch</span><span class="sxs-lookup"><span data-stu-id="14da3-351">information branch</span></span>
- <span data-ttu-id="14da3-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="14da3-352">credit card loan</span></span>
- <span data-ttu-id="14da3-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="14da3-353">department of human services</span></span>
- <span data-ttu-id="14da3-354">local service</span><span class="sxs-lookup"><span data-stu-id="14da3-354">local service</span></span>
- <span data-ttu-id="14da3-355">Медикаре</span><span class="sxs-lookup"><span data-stu-id="14da3-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="14da3-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="14da3-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-357">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-357">Format</span></span>

<span data-ttu-id="14da3-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-359">Pattern</span></span>

<span data-ttu-id="14da3-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-361">Checksum</span></span>

<span data-ttu-id="14da3-362">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-363">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-363">Definition</span></span>

<span data-ttu-id="14da3-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-366">Найдено ключевое слово из Кэйворд_пасспорт или Кэйворд_аустралиа_пасспорт_нумбер.</span><span class="sxs-lookup"><span data-stu-id="14da3-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="14da3-368">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-368">Keyword_passport</span></span>

- <span data-ttu-id="14da3-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="14da3-369">Passport Number</span></span>
- <span data-ttu-id="14da3-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="14da3-370">Passport No</span></span>
- <span data-ttu-id="14da3-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="14da3-371">Passport #</span></span>
- <span data-ttu-id="14da3-372">Службу</span><span class="sxs-lookup"><span data-stu-id="14da3-372">Passport#</span></span>
- <span data-ttu-id="14da3-373">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="14da3-373">PassportID</span></span>
- <span data-ttu-id="14da3-374">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="14da3-374">Passportno</span></span>
- <span data-ttu-id="14da3-375">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-375">passportnumber</span></span>
- <span data-ttu-id="14da3-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="14da3-376">パスポート</span></span>
- <span data-ttu-id="14da3-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="14da3-377">パスポート番号</span></span>
- <span data-ttu-id="14da3-378">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="14da3-378">パスポートのNum</span></span>
- <span data-ttu-id="14da3-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="14da3-379">パスポート ＃</span></span> 
- <span data-ttu-id="14da3-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="14da3-380">Numéro de passeport</span></span>
- <span data-ttu-id="14da3-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="14da3-381">Passeport n °</span></span>
- <span data-ttu-id="14da3-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="14da3-382">Passeport Non</span></span>
- <span data-ttu-id="14da3-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="14da3-383">Passeport #</span></span>
- <span data-ttu-id="14da3-384">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="14da3-384">Passeport#</span></span>
- <span data-ttu-id="14da3-385">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="14da3-385">PasseportNon</span></span>
- <span data-ttu-id="14da3-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="14da3-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="14da3-387">Кэйворд_аустралиа_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="14da3-388">службу</span><span class="sxs-lookup"><span data-stu-id="14da3-388">passport</span></span>
- <span data-ttu-id="14da3-389">passport details</span><span class="sxs-lookup"><span data-stu-id="14da3-389">passport details</span></span>
- <span data-ttu-id="14da3-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="14da3-390">immigration and citizenship</span></span>
- <span data-ttu-id="14da3-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="14da3-391">commonwealth of australia</span></span>
- <span data-ttu-id="14da3-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="14da3-392">department of immigration</span></span>
- <span data-ttu-id="14da3-393">residential address</span><span class="sxs-lookup"><span data-stu-id="14da3-393">residential address</span></span>
- <span data-ttu-id="14da3-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="14da3-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="14da3-395">Visa</span><span class="sxs-lookup"><span data-stu-id="14da3-395">visa</span></span>
- <span data-ttu-id="14da3-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="14da3-396">national identity card</span></span>
- <span data-ttu-id="14da3-397">passport number</span><span class="sxs-lookup"><span data-stu-id="14da3-397">passport number</span></span>
- <span data-ttu-id="14da3-398">travel document</span><span class="sxs-lookup"><span data-stu-id="14da3-398">travel document</span></span>
- <span data-ttu-id="14da3-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="14da3-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="14da3-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="14da3-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-401">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-401">Format</span></span>

<span data-ttu-id="14da3-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-403">Pattern</span></span>

<span data-ttu-id="14da3-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="14da3-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="14da3-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-405">Three digits</span></span> 
- <span data-ttu-id="14da3-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-406">An optional space</span></span> 
- <span data-ttu-id="14da3-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-407">Three digits</span></span> 
- <span data-ttu-id="14da3-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-408">An optional space</span></span> 
- <span data-ttu-id="14da3-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="14da3-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-410">Checksum</span></span>

<span data-ttu-id="14da3-411">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-412">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-412">Definition</span></span>

<span data-ttu-id="14da3-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="14da3-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="14da3-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="14da3-418">Кэйворд_аустралиа_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="14da3-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="14da3-419">australian business number</span></span>
- <span data-ttu-id="14da3-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="14da3-420">marginal tax rate</span></span>
- <span data-ttu-id="14da3-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="14da3-421">medicare levy</span></span>
- <span data-ttu-id="14da3-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="14da3-422">portfolio number</span></span>
- <span data-ttu-id="14da3-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="14da3-423">service veterans</span></span>
- <span data-ttu-id="14da3-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="14da3-424">withholding tax</span></span>
- <span data-ttu-id="14da3-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="14da3-425">individual tax return</span></span>
- <span data-ttu-id="14da3-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="14da3-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="14da3-427">Кэйворд_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="14da3-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="14da3-428">00000001</span><span class="sxs-lookup"><span data-stu-id="14da3-428">00000000</span></span>
- <span data-ttu-id="14da3-429">11111111</span><span class="sxs-lookup"><span data-stu-id="14da3-429">11111111</span></span>
- <span data-ttu-id="14da3-430">22222222</span><span class="sxs-lookup"><span data-stu-id="14da3-430">22222222</span></span>
- <span data-ttu-id="14da3-431">33333333</span><span class="sxs-lookup"><span data-stu-id="14da3-431">33333333</span></span>
- <span data-ttu-id="14da3-432">44444444</span><span class="sxs-lookup"><span data-stu-id="14da3-432">44444444</span></span>
- <span data-ttu-id="14da3-433">55555555</span><span class="sxs-lookup"><span data-stu-id="14da3-433">55555555</span></span>
- <span data-ttu-id="14da3-434">66666666</span><span class="sxs-lookup"><span data-stu-id="14da3-434">66666666</span></span>
- <span data-ttu-id="14da3-435">77777777</span><span class="sxs-lookup"><span data-stu-id="14da3-435">77777777</span></span>
- <span data-ttu-id="14da3-436">88888888</span><span class="sxs-lookup"><span data-stu-id="14da3-436">88888888</span></span>
- <span data-ttu-id="14da3-437">99999999</span><span class="sxs-lookup"><span data-stu-id="14da3-437">99999999</span></span>
- <span data-ttu-id="14da3-438">000000000</span><span class="sxs-lookup"><span data-stu-id="14da3-438">000000000</span></span>
- <span data-ttu-id="14da3-439">111111111</span><span class="sxs-lookup"><span data-stu-id="14da3-439">111111111</span></span>
- <span data-ttu-id="14da3-440">222222222</span><span class="sxs-lookup"><span data-stu-id="14da3-440">222222222</span></span>
- <span data-ttu-id="14da3-441">333333333</span><span class="sxs-lookup"><span data-stu-id="14da3-441">333333333</span></span>
- <span data-ttu-id="14da3-442">444444444</span><span class="sxs-lookup"><span data-stu-id="14da3-442">444444444</span></span>
- <span data-ttu-id="14da3-443">555555555</span><span class="sxs-lookup"><span data-stu-id="14da3-443">555555555</span></span>
- <span data-ttu-id="14da3-444">666666666</span><span class="sxs-lookup"><span data-stu-id="14da3-444">666666666</span></span>
- <span data-ttu-id="14da3-445">777777777</span><span class="sxs-lookup"><span data-stu-id="14da3-445">777777777</span></span>
- <span data-ttu-id="14da3-446">888888888</span><span class="sxs-lookup"><span data-stu-id="14da3-446">888888888</span></span>
- <span data-ttu-id="14da3-447">999999999</span><span class="sxs-lookup"><span data-stu-id="14da3-447">999999999</span></span>
- <span data-ttu-id="14da3-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="14da3-448">0000000000</span></span>
- <span data-ttu-id="14da3-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="14da3-449">1111111111</span></span>
- <span data-ttu-id="14da3-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="14da3-450">2222222222</span></span>
- <span data-ttu-id="14da3-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="14da3-451">3333333333</span></span>
- <span data-ttu-id="14da3-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="14da3-452">4444444444</span></span>
- <span data-ttu-id="14da3-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="14da3-453">5555555555</span></span>
- <span data-ttu-id="14da3-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="14da3-454">6666666666</span></span>
- <span data-ttu-id="14da3-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="14da3-455">7777777777</span></span>
- <span data-ttu-id="14da3-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="14da3-456">8888888888</span></span>
- <span data-ttu-id="14da3-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="14da3-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="14da3-458">Ключ проверки подлинности Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="14da3-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="14da3-459">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-459">Format</span></span>

<span data-ttu-id="14da3-460">Строка "DocumentDb", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="14da3-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-461">Pattern</span></span>

- <span data-ttu-id="14da3-462">Строка "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="14da3-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="14da3-463">Любая комбинация из 3-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-464">Символ "больше" (_Гт_), знак равенства (=), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="14da3-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="14da3-465">Любая комбинация 86 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="14da3-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="14da3-466">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="14da3-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-467">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-467">Checksum</span></span>

<span data-ttu-id="14da3-468">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-469">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-469">Definition</span></span>

<span data-ttu-id="14da3-470">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-471">Регулярное выражение Цеп_режекс_азуредокументдбаускэй находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-472">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-473">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-473">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-474">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-475">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-476">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-476">contoso</span></span>
- <span data-ttu-id="14da3-477">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-477">fabrikam</span></span>
- <span data-ttu-id="14da3-478">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-478">northwind</span></span>
- <span data-ttu-id="14da3-479">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-479">sandbox</span></span>
- <span data-ttu-id="14da3-480">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-480">onebox</span></span>
- <span data-ttu-id="14da3-481">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-481">localhost</span></span>
- <span data-ttu-id="14da3-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-482">127.0.0.1</span></span>
- <span data-ttu-id="14da3-483">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-484">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-484">com</span></span>
- <span data-ttu-id="14da3-485">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-486">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="14da3-487">Строка подключения к базе данных Azure IAAS и строка подключения к SQL Azure</span><span class="sxs-lookup"><span data-stu-id="14da3-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="14da3-488">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-488">Format</span></span>

<span data-ttu-id="14da3-489">Строка "Server", "Server" или "Data Source", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "клаудапп. Azure".</span><span class="sxs-lookup"><span data-stu-id="14da3-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-490">com "или" клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="14da3-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-491">NET "или" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="14da3-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-492">NET ", а также строку" Password "или" Password "или" pwd ".</span><span class="sxs-lookup"><span data-stu-id="14da3-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-493">Pattern</span></span>

- <span data-ttu-id="14da3-494">Строка "Server", "Server" или "Data Source"</span><span class="sxs-lookup"><span data-stu-id="14da3-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="14da3-495">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-496">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-496">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-497">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-498">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-499">Строка "клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="14da3-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-500">com "," клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="14da3-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-501">NET "или" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="14da3-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-502">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-502">net"</span></span>
- <span data-ttu-id="14da3-503">Любая комбинация из 1-300 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-504">Строка "Password", "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="14da3-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="14da3-505">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-506">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-506">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-507">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-508">Один или несколько символов, не отделяющая точку с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="14da3-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="14da3-509">Точка с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="14da3-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-510">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-510">Checksum</span></span>

<span data-ttu-id="14da3-511">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-512">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-512">Definition</span></span>

<span data-ttu-id="14da3-513">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-514">Регулярное выражение Цеп_режекс_азуреконнектионстринг находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-515">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-516">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-516">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-517">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-518">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-519">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-519">contoso</span></span>
- <span data-ttu-id="14da3-520">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-520">fabrikam</span></span>
- <span data-ttu-id="14da3-521">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-521">northwind</span></span>
- <span data-ttu-id="14da3-522">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-522">sandbox</span></span>
- <span data-ttu-id="14da3-523">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-523">onebox</span></span>
- <span data-ttu-id="14da3-524">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-524">localhost</span></span>
- <span data-ttu-id="14da3-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-525">127.0.0.1</span></span>
- <span data-ttu-id="14da3-526">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-527">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-527">com</span></span>
- <span data-ttu-id="14da3-528">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-529">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="14da3-530">Строка подключения Azure IoT</span><span class="sxs-lookup"><span data-stu-id="14da3-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="14da3-531">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-531">Format</span></span>

<span data-ttu-id="14da3-532">Строка "HostName", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, включая строки "Azure — Devices.</span><span class="sxs-lookup"><span data-stu-id="14da3-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-533">NET "и" Шаредакцесскэй ".</span><span class="sxs-lookup"><span data-stu-id="14da3-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-534">Pattern</span></span>

- <span data-ttu-id="14da3-535">Строка "HostName"</span><span class="sxs-lookup"><span data-stu-id="14da3-535">The string "HostName"</span></span>
- <span data-ttu-id="14da3-536">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-537">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-537">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-538">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-539">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-540">Строка "Azure — Devices.</span><span class="sxs-lookup"><span data-stu-id="14da3-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-541">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-541">net"</span></span>
- <span data-ttu-id="14da3-542">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-543">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="14da3-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="14da3-544">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-545">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-545">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-546">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-547">Любая комбинация 43 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="14da3-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="14da3-548">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-549">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-549">Checksum</span></span>

<span data-ttu-id="14da3-550">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-551">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-551">Definition</span></span>

<span data-ttu-id="14da3-552">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-553">Регулярное выражение Цеп_режекс_азуреиотконнектионстринг находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-554">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-555">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-555">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-556">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-557">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-558">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-558">contoso</span></span>
- <span data-ttu-id="14da3-559">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-559">fabrikam</span></span>
- <span data-ttu-id="14da3-560">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-560">northwind</span></span>
- <span data-ttu-id="14da3-561">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-561">sandbox</span></span>
- <span data-ttu-id="14da3-562">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-562">onebox</span></span>
- <span data-ttu-id="14da3-563">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-563">localhost</span></span>
- <span data-ttu-id="14da3-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-564">127.0.0.1</span></span>
- <span data-ttu-id="14da3-565">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-566">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-566">com</span></span>
- <span data-ttu-id="14da3-567">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-568">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="14da3-569">Пароль для параметра публикации Azure</span><span class="sxs-lookup"><span data-stu-id="14da3-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="14da3-570">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-570">Format</span></span>

<span data-ttu-id="14da3-571">Строка "усерпвд =", за которой следует буквенно-цифровая строка.</span><span class="sxs-lookup"><span data-stu-id="14da3-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-572">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-572">Pattern</span></span>

- <span data-ttu-id="14da3-573">Строка "усерпвд ="</span><span class="sxs-lookup"><span data-stu-id="14da3-573">The string "userpwd="</span></span>
- <span data-ttu-id="14da3-574">Любая комбинация букв или цифр в нижнем регистре 60</span><span class="sxs-lookup"><span data-stu-id="14da3-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="14da3-575">Знак кавычек (")</span><span class="sxs-lookup"><span data-stu-id="14da3-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-576">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-576">Checksum</span></span>

<span data-ttu-id="14da3-577">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-578">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-578">Definition</span></span>

<span data-ttu-id="14da3-579">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-580">Регулярное выражение Цеп_режекс_азурепублишсеттингпассвордс находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-581">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


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

### <a name="keywords"></a><span data-ttu-id="14da3-582">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-582">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-583">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-584">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-585">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-585">contoso</span></span>
- <span data-ttu-id="14da3-586">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-586">fabrikam</span></span>
- <span data-ttu-id="14da3-587">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-587">northwind</span></span>
- <span data-ttu-id="14da3-588">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-588">sandbox</span></span>
- <span data-ttu-id="14da3-589">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-589">onebox</span></span>
- <span data-ttu-id="14da3-590">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-590">localhost</span></span>
- <span data-ttu-id="14da3-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-591">127.0.0.1</span></span>
- <span data-ttu-id="14da3-592">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-593">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-593">com</span></span>
- <span data-ttu-id="14da3-594">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-595">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="14da3-596">Строка подключения к кэшу Azure Redis</span><span class="sxs-lookup"><span data-stu-id="14da3-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="14da3-597">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-597">Format</span></span>

<span data-ttu-id="14da3-598">Строка "Redis. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="14da3-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-599">NET, за которыми следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "Password" или "pwd".</span><span class="sxs-lookup"><span data-stu-id="14da3-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-600">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-600">Pattern</span></span>

- <span data-ttu-id="14da3-601">Строка "Redis. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="14da3-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-602">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-602">net"</span></span>
- <span data-ttu-id="14da3-603">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-604">Строка "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="14da3-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="14da3-605">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-606">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-606">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-607">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-608">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="14da3-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="14da3-609">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-610">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-610">Checksum</span></span>

<span data-ttu-id="14da3-611">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-612">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-612">Definition</span></span>

<span data-ttu-id="14da3-613">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-614">Регулярное выражение Цеп_режекс_азурередискачеконнектионстринг находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="14da3-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="14da3-615">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-616">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-616">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-617">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-618">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-619">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-619">contoso</span></span>
- <span data-ttu-id="14da3-620">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-620">fabrikam</span></span>
- <span data-ttu-id="14da3-621">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-621">northwind</span></span>
- <span data-ttu-id="14da3-622">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-622">sandbox</span></span>
- <span data-ttu-id="14da3-623">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-623">onebox</span></span>
- <span data-ttu-id="14da3-624">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-624">localhost</span></span>
- <span data-ttu-id="14da3-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-625">127.0.0.1</span></span>
- <span data-ttu-id="14da3-626">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-627">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-627">com</span></span>
- <span data-ttu-id="14da3-628">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-629">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="14da3-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="14da3-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="14da3-631">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-631">Format</span></span>

<span data-ttu-id="14da3-632">Строка "SIG", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="14da3-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-633">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-633">Pattern</span></span>

- <span data-ttu-id="14da3-634">Строка "SIG"</span><span class="sxs-lookup"><span data-stu-id="14da3-634">The string "sig"</span></span>
- <span data-ttu-id="14da3-635">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-636">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-636">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-637">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-638">Любое сочетание 43-53 символов, которые являются буквами нижнего или верхнего регистра, цифрами или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="14da3-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="14da3-639">Строка "% 3D"</span><span class="sxs-lookup"><span data-stu-id="14da3-639">The string "%3d"</span></span>
- <span data-ttu-id="14da3-640">Любой символ, который не является буквой нижнего или верхнего регистра, цифрой или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="14da3-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-641">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-641">Checksum</span></span>

<span data-ttu-id="14da3-642">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-643">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-643">Definition</span></span>

<span data-ttu-id="14da3-644">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-645">Регулярное выражение Цеп_режекс_азуресас находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="14da3-646">Строка подключения к служебной шине Azure</span><span class="sxs-lookup"><span data-stu-id="14da3-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="14da3-647">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-647">Format</span></span>

<span data-ttu-id="14da3-648">Строка "EndPoint", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строки "сервицебус. Windows.</span><span class="sxs-lookup"><span data-stu-id="14da3-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-649">NET "и" Шаредакцескэй ".</span><span class="sxs-lookup"><span data-stu-id="14da3-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-650">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-650">Pattern</span></span>

- <span data-ttu-id="14da3-651">Строка "EndPoint"</span><span class="sxs-lookup"><span data-stu-id="14da3-651">The string "EndPoint"</span></span>
- <span data-ttu-id="14da3-652">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-653">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-653">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-654">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-655">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-656">Строка "сервицебус. Windows.</span><span class="sxs-lookup"><span data-stu-id="14da3-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-657">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-657">net"</span></span>
- <span data-ttu-id="14da3-658">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-659">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="14da3-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="14da3-660">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-661">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-661">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-662">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-663">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="14da3-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="14da3-664">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-665">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-665">Checksum</span></span>

<span data-ttu-id="14da3-666">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-667">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-667">Definition</span></span>

<span data-ttu-id="14da3-668">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-669">Регулярное выражение Цеп_режекс_азуресервицебусконнектионстринг находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="14da3-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="14da3-670">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-671">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-671">Keywords</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-672">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-673">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-674">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-674">contoso</span></span>
- <span data-ttu-id="14da3-675">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-675">fabrikam</span></span>
- <span data-ttu-id="14da3-676">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-676">northwind</span></span>
- <span data-ttu-id="14da3-677">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-677">sandbox</span></span>
- <span data-ttu-id="14da3-678">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-678">onebox</span></span>
- <span data-ttu-id="14da3-679">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-679">localhost</span></span>
- <span data-ttu-id="14da3-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-680">127.0.0.1</span></span>
- <span data-ttu-id="14da3-681">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-682">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-682">com</span></span>
- <span data-ttu-id="14da3-683">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-684">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="14da3-685">Ключ учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="14da3-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="14da3-686">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-686">Format</span></span>

<span data-ttu-id="14da3-687">Строка "Дефаултендпоинтспротокол", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "AccountKey".</span><span class="sxs-lookup"><span data-stu-id="14da3-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-688">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-688">Pattern</span></span>

- <span data-ttu-id="14da3-689">Строка "Дефаултендпоинтспротокол"</span><span class="sxs-lookup"><span data-stu-id="14da3-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="14da3-690">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-691">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-691">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-692">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-693">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-694">Строка "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="14da3-694">The string "AccountKey"</span></span>
- <span data-ttu-id="14da3-695">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-696">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-696">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-697">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="14da3-698">Любое сочетание 86 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="14da3-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="14da3-699">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="14da3-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-700">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-700">Checksum</span></span>

<span data-ttu-id="14da3-701">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-702">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-702">Definition</span></span>

<span data-ttu-id="14da3-703">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-704">Регулярное выражение Цеп_режекс_азуресторажеаккаунткэй находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-705">Регулярное выражение Цеп_азуримулаторсторажеаккаунтфилтер не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-706">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-707">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-707">Keywords</span></span>

#### <a name="cepazureemulatorstorageaccountfilter"></a><span data-ttu-id="14da3-708">Цеп_азуримулаторсторажеаккаунтфилтер</span><span class="sxs-lookup"><span data-stu-id="14da3-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="14da3-709">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/Кбхбексогмгв = =</span><span class="sxs-lookup"><span data-stu-id="14da3-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-711">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-712">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-713">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-713">contoso</span></span>
- <span data-ttu-id="14da3-714">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-714">fabrikam</span></span>
- <span data-ttu-id="14da3-715">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-715">northwind</span></span>
- <span data-ttu-id="14da3-716">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-716">sandbox</span></span>
- <span data-ttu-id="14da3-717">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-717">onebox</span></span>
- <span data-ttu-id="14da3-718">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-718">localhost</span></span>
- <span data-ttu-id="14da3-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-719">127.0.0.1</span></span>
- <span data-ttu-id="14da3-720">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-721">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-721">com</span></span>
- <span data-ttu-id="14da3-722">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-723">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="14da3-724">Ключ учетной записи хранилища Azure (общий)</span><span class="sxs-lookup"><span data-stu-id="14da3-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-725">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-725">Format</span></span>

<span data-ttu-id="14da3-726">Любая комбинация 86 строчных или прописных букв, цифр, знаков косой черты (/) или знака плюса (+) перед или за ними следуют символы, указанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="14da3-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-727">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-727">Pattern</span></span>

- <span data-ttu-id="14da3-728">0-1 из символа "больше" (_Гт_), апостроф ('), знак равенства (=), знак кавычек (") или решетка (#)</span><span class="sxs-lookup"><span data-stu-id="14da3-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="14da3-729">Любое сочетание 86 символов, которые представляют собой буквы в нижнем или верхнем регистре, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="14da3-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="14da3-730">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="14da3-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="14da3-731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-731">Checksum</span></span>

<span data-ttu-id="14da3-732">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-733">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-733">Definition</span></span>

<span data-ttu-id="14da3-734">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-735">Регулярное выражение Цеп_режекс_азуресторажеаккаунткэйженерик находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="14da3-736">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="14da3-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-737">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-737">Format</span></span>

<span data-ttu-id="14da3-738">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="14da3-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-739">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-739">Pattern</span></span>

<span data-ttu-id="14da3-740">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="14da3-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="14da3-741">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="14da3-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="14da3-742">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-742">A hyphen</span></span> 
- <span data-ttu-id="14da3-743">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="14da3-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="14da3-744">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-744">A period</span></span> 
- <span data-ttu-id="14da3-745">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-746">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-746">Checksum</span></span>

<span data-ttu-id="14da3-747">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-748">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-748">Definition</span></span>

<span data-ttu-id="14da3-749">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-750">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-751">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="14da3-752">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-752">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-753">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-753">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="14da3-754">Кэйворд_белгиум_натионал_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="14da3-755">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="14da3-755">Identity</span></span>
- <span data-ttu-id="14da3-756">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="14da3-756">Registration</span></span>
- <span data-ttu-id="14da3-757">Процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-757">Identification</span></span> 
- <span data-ttu-id="14da3-758">ID</span><span class="sxs-lookup"><span data-stu-id="14da3-758">ID</span></span> 
- <span data-ttu-id="14da3-759">Идентитеитскаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-759">Identiteitskaart</span></span>
- <span data-ttu-id="14da3-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="14da3-760">Registratie nummer</span></span> 
- <span data-ttu-id="14da3-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="14da3-761">Identificatie nummer</span></span> 
- <span data-ttu-id="14da3-762">Идентитеит</span><span class="sxs-lookup"><span data-stu-id="14da3-762">Identiteit</span></span>
- <span data-ttu-id="14da3-763">Регистратие</span><span class="sxs-lookup"><span data-stu-id="14da3-763">Registratie</span></span>
- <span data-ttu-id="14da3-764">Идентификатие</span><span class="sxs-lookup"><span data-stu-id="14da3-764">Identificatie</span></span> 
- <span data-ttu-id="14da3-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="14da3-765">Carte d’identité</span></span> 
- <span data-ttu-id="14da3-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="14da3-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="14da3-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="14da3-767">numéro d'identification</span></span>
- <span data-ttu-id="14da3-768">идентитé</span><span class="sxs-lookup"><span data-stu-id="14da3-768">identité</span></span> 
- <span data-ttu-id="14da3-769">инскриптион</span><span class="sxs-lookup"><span data-stu-id="14da3-769">inscription</span></span> 
- <span data-ttu-id="14da3-770">Идентификатион</span><span class="sxs-lookup"><span data-stu-id="14da3-770">Identifikation</span></span>
- <span data-ttu-id="14da3-771">Идентифизиерунг</span><span class="sxs-lookup"><span data-stu-id="14da3-771">Identifizierung</span></span>
- <span data-ttu-id="14da3-772">Идентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-772">Identifikationsnummer</span></span>
- <span data-ttu-id="14da3-773">Персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="14da3-773">Personalausweis</span></span>
- <span data-ttu-id="14da3-774">Регистриерунг</span><span class="sxs-lookup"><span data-stu-id="14da3-774">Registrierung</span></span>
- <span data-ttu-id="14da3-775">Регистратионснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="14da3-776">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="14da3-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-777">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-777">Format</span></span>

<span data-ttu-id="14da3-778">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="14da3-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-779">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-779">Pattern</span></span>

<span data-ttu-id="14da3-780">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="14da3-780">Formatted:</span></span>
- <span data-ttu-id="14da3-781">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-781">Three digits</span></span> 
- <span data-ttu-id="14da3-782">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-782">A period</span></span> 
- <span data-ttu-id="14da3-783">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-783">Three digits</span></span> 
- <span data-ttu-id="14da3-784">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-784">A period</span></span> 
- <span data-ttu-id="14da3-785">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-785">Three digits</span></span> 
- <span data-ttu-id="14da3-786">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-786">A hyphen</span></span> 
- <span data-ttu-id="14da3-787">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-787">Two digits which are check digits</span></span>

<span data-ttu-id="14da3-788">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="14da3-788">Unformatted:</span></span>
- <span data-ttu-id="14da3-789">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="14da3-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-790">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-790">Checksum</span></span>

<span data-ttu-id="14da3-791">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-792">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-792">Definition</span></span>

<span data-ttu-id="14da3-793">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-794">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-795">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="14da3-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="14da3-796">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-796">The checksum passes.</span></span>

<span data-ttu-id="14da3-797">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-798">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-799">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-799">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-800">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-800">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="14da3-801">Кэйворд_бразил_кпф</span><span class="sxs-lookup"><span data-stu-id="14da3-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="14da3-802">CPF</span><span class="sxs-lookup"><span data-stu-id="14da3-802">CPF</span></span>
- <span data-ttu-id="14da3-803">Процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-803">Identification</span></span>
- <span data-ttu-id="14da3-804">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="14da3-804">Registration</span></span>
- <span data-ttu-id="14da3-805">Реализации</span><span class="sxs-lookup"><span data-stu-id="14da3-805">Revenue</span></span>
- <span data-ttu-id="14da3-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="14da3-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="14da3-807">Импосто</span><span class="sxs-lookup"><span data-stu-id="14da3-807">Imposto</span></span> 
- <span data-ttu-id="14da3-808">Идентификаçãо</span><span class="sxs-lookup"><span data-stu-id="14da3-808">Identificação</span></span> 
- <span data-ttu-id="14da3-809">Инскриçãо</span><span class="sxs-lookup"><span data-stu-id="14da3-809">Inscrição</span></span> 
- <span data-ttu-id="14da3-810">Рецеита</span><span class="sxs-lookup"><span data-stu-id="14da3-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="14da3-811">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="14da3-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-812">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-812">Format</span></span>

<span data-ttu-id="14da3-813">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="14da3-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-814">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-814">Pattern</span></span>
<span data-ttu-id="14da3-815">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="14da3-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="14da3-816">две цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-816">Two digits</span></span> 
- <span data-ttu-id="14da3-817">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-817">A period</span></span> 
- <span data-ttu-id="14da3-818">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-818">Three digits</span></span> 
- <span data-ttu-id="14da3-819">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-819">A period</span></span> 
- <span data-ttu-id="14da3-820">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="14da3-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="14da3-821">косая черта;</span><span class="sxs-lookup"><span data-stu-id="14da3-821">A forward slash</span></span> 
- <span data-ttu-id="14da3-822">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-822">Four-digit branch number</span></span> 
- <span data-ttu-id="14da3-823">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-823">A hyphen</span></span> 
- <span data-ttu-id="14da3-824">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-825">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-825">Checksum</span></span>

<span data-ttu-id="14da3-826">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-827">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-827">Definition</span></span>

<span data-ttu-id="14da3-828">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-829">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-830">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="14da3-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="14da3-831">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-831">The checksum passes.</span></span>

<span data-ttu-id="14da3-832">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-833">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-834">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-834">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-835">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-835">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="14da3-836">Кэйворд_бразил_кнпж</span><span class="sxs-lookup"><span data-stu-id="14da3-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="14da3-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="14da3-837">CNPJ</span></span> 
- <span data-ttu-id="14da3-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="14da3-838">CNPJ/MF</span></span> 
- <span data-ttu-id="14da3-839">CNPJ – MF</span><span class="sxs-lookup"><span data-stu-id="14da3-839">CNPJ-MF</span></span> 
- <span data-ttu-id="14da3-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="14da3-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="14da3-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="14da3-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="14da3-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="14da3-842">Legal entity</span></span> 
- <span data-ttu-id="14da3-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="14da3-843">Legal entities</span></span> 
- <span data-ttu-id="14da3-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="14da3-844">Registration Status</span></span> 
- <span data-ttu-id="14da3-845">Бизнес</span><span class="sxs-lookup"><span data-stu-id="14da3-845">Business</span></span> 
- <span data-ttu-id="14da3-846">Company</span><span class="sxs-lookup"><span data-stu-id="14da3-846">Company</span></span>
- <span data-ttu-id="14da3-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="14da3-847">CNPJ</span></span> 
- <span data-ttu-id="14da3-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="14da3-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="14da3-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="14da3-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="14da3-850">КГК</span><span class="sxs-lookup"><span data-stu-id="14da3-850">CGC</span></span> 
- <span data-ttu-id="14da3-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="14da3-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="14da3-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="14da3-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="14da3-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="14da3-853">Situação cadastral</span></span> 
- <span data-ttu-id="14da3-854">Инскриçãо</span><span class="sxs-lookup"><span data-stu-id="14da3-854">Inscrição</span></span> 
- <span data-ttu-id="14da3-855">Емпреса</span><span class="sxs-lookup"><span data-stu-id="14da3-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="14da3-856">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="14da3-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-857">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-857">Format</span></span>

<span data-ttu-id="14da3-858">Registro Geral (старый формат): девять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="14da3-859">Registro de identidade (RIC) (новый формат): 11 цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-860">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-860">Pattern</span></span>

<span data-ttu-id="14da3-861">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="14da3-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="14da3-862">две цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-862">Two digits</span></span> 
- <span data-ttu-id="14da3-863">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-863">A period</span></span> 
- <span data-ttu-id="14da3-864">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-864">Three digits</span></span> 
- <span data-ttu-id="14da3-865">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-865">A period</span></span> 
- <span data-ttu-id="14da3-866">три цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-866">Three digits</span></span> 
- <span data-ttu-id="14da3-867">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-867">A hyphen</span></span> 
- <span data-ttu-id="14da3-868">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-868">One digit which is a check digit</span></span>

<span data-ttu-id="14da3-869">Registro de identidade (RIC) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="14da3-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="14da3-870">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-870">10 digits</span></span> 
- <span data-ttu-id="14da3-871">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-871">A hyphen</span></span> 
- <span data-ttu-id="14da3-872">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-873">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-873">Checksum</span></span>

<span data-ttu-id="14da3-874">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-875">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-875">Definition</span></span>

<span data-ttu-id="14da3-876">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-877">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-878">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="14da3-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="14da3-879">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-879">The checksum passes.</span></span>

<span data-ttu-id="14da3-880">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-881">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-882">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-882">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-883">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-883">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="14da3-884">Кэйворд_бразил_рг</span><span class="sxs-lookup"><span data-stu-id="14da3-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="14da3-885">Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр).</span><span class="sxs-lookup"><span data-stu-id="14da3-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="14da3-886">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="14da3-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-887">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-887">Format</span></span>

<span data-ttu-id="14da3-888">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-889">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-889">Pattern</span></span>

<span data-ttu-id="14da3-890">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="14da3-891">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="14da3-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="14da3-892">пять цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-892">Five digits</span></span> 
- <span data-ttu-id="14da3-893">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-893">A hyphen</span></span> 
- <span data-ttu-id="14da3-894">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="14da3-894">Three digits OR</span></span>
- <span data-ttu-id="14da3-895">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="14da3-895">A zero "0"</span></span> 
- <span data-ttu-id="14da3-896">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-897">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-897">Checksum</span></span>

<span data-ttu-id="14da3-898">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-899">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-899">Definition</span></span>

<span data-ttu-id="14da3-900">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-901">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-902">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="14da3-903">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="14da3-904">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-905">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-906">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-907">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-907">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="14da3-908">Кэйворд_канада_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="14da3-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="14da3-909">canada savings bonds</span></span>
- <span data-ttu-id="14da3-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="14da3-910">canada revenue agency</span></span>
- <span data-ttu-id="14da3-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="14da3-911">canadian financial institution</span></span>
- <span data-ttu-id="14da3-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="14da3-912">direct deposit form</span></span>
- <span data-ttu-id="14da3-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="14da3-913">canadian citizen</span></span>
- <span data-ttu-id="14da3-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="14da3-914">legal representative</span></span>
- <span data-ttu-id="14da3-915">notary public</span><span class="sxs-lookup"><span data-stu-id="14da3-915">notary public</span></span>
- <span data-ttu-id="14da3-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="14da3-916">commissioner for oaths</span></span>
- <span data-ttu-id="14da3-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="14da3-917">child care benefit</span></span>
- <span data-ttu-id="14da3-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="14da3-918">universal child care</span></span>
- <span data-ttu-id="14da3-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="14da3-919">canada child tax benefit</span></span>
- <span data-ttu-id="14da3-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="14da3-920">income tax benefit</span></span>
- <span data-ttu-id="14da3-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="14da3-921">harmonized sales tax</span></span>
- <span data-ttu-id="14da3-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="14da3-922">social insurance number</span></span>
- <span data-ttu-id="14da3-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="14da3-923">income tax refund</span></span>
- <span data-ttu-id="14da3-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="14da3-924">child tax benefit</span></span>
- <span data-ttu-id="14da3-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="14da3-925">territorial payments</span></span>
- <span data-ttu-id="14da3-926">institution number</span><span class="sxs-lookup"><span data-stu-id="14da3-926">institution number</span></span>
- <span data-ttu-id="14da3-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="14da3-927">deposit request</span></span>
- <span data-ttu-id="14da3-928">banking information</span><span class="sxs-lookup"><span data-stu-id="14da3-928">banking information</span></span>
- <span data-ttu-id="14da3-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="14da3-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="14da3-930">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="14da3-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-931">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-931">Format</span></span>

<span data-ttu-id="14da3-932">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="14da3-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-933">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-933">Pattern</span></span>

<span data-ttu-id="14da3-934">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="14da3-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-935">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-935">Checksum</span></span>

<span data-ttu-id="14da3-936">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-937">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-937">Definition</span></span>

<span data-ttu-id="14da3-938">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-939">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-940">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="14da3-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="14da3-941">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="14da3-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-942">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-942">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="14da3-943">Кэйворд_ [провинце_наме] _дриверс_лиценсе_наме</span><span class="sxs-lookup"><span data-stu-id="14da3-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="14da3-944">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="14da3-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="14da3-945">Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="14da3-945">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="14da3-946">Кэйворд_канада_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="14da3-947">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-947">DL</span></span>
- <span data-ttu-id="14da3-948">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="14da3-948">DLS</span></span>
- <span data-ttu-id="14da3-949">КДЛ</span><span class="sxs-lookup"><span data-stu-id="14da3-949">CDL</span></span>
- <span data-ttu-id="14da3-950">КДЛС</span><span class="sxs-lookup"><span data-stu-id="14da3-950">CDLS</span></span>
- <span data-ttu-id="14da3-951">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="14da3-951">DriverLic</span></span>
- <span data-ttu-id="14da3-952">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="14da3-952">DriverLics</span></span>
- <span data-ttu-id="14da3-953">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-953">DriverLicense</span></span>
- <span data-ttu-id="14da3-954">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-954">DriverLicenses</span></span>
- <span data-ttu-id="14da3-955">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="14da3-955">DriverLicence</span></span>
- <span data-ttu-id="14da3-956">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="14da3-956">DriverLicences</span></span>
- <span data-ttu-id="14da3-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-957">Driver Lic</span></span>
- <span data-ttu-id="14da3-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-958">Driver Lics</span></span>
- <span data-ttu-id="14da3-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="14da3-959">Driver License</span></span>
- <span data-ttu-id="14da3-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-960">Driver Licenses</span></span>
- <span data-ttu-id="14da3-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-961">Driver Licence</span></span>
- <span data-ttu-id="14da3-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-962">Driver Licences</span></span>
- <span data-ttu-id="14da3-963">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="14da3-963">DriversLic</span></span>
- <span data-ttu-id="14da3-964">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="14da3-964">DriversLics</span></span>
- <span data-ttu-id="14da3-965">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="14da3-965">DriversLicence</span></span>
- <span data-ttu-id="14da3-966">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="14da3-966">DriversLicences</span></span>
- <span data-ttu-id="14da3-967">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-967">DriversLicense</span></span>
- <span data-ttu-id="14da3-968">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-968">DriversLicenses</span></span>
- <span data-ttu-id="14da3-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-969">Drivers Lic</span></span>
- <span data-ttu-id="14da3-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-970">Drivers Lics</span></span>
- <span data-ttu-id="14da3-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="14da3-971">Drivers License</span></span>
- <span data-ttu-id="14da3-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-972">Drivers Licenses</span></span>
- <span data-ttu-id="14da3-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-973">Drivers Licence</span></span>
- <span data-ttu-id="14da3-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-974">Drivers Licences</span></span>
- <span data-ttu-id="14da3-975">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="14da3-975">Driver'Lic</span></span>
- <span data-ttu-id="14da3-976">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="14da3-976">Driver'Lics</span></span>
- <span data-ttu-id="14da3-977">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="14da3-977">Driver'License</span></span>
- <span data-ttu-id="14da3-978">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-978">Driver'Licenses</span></span>
- <span data-ttu-id="14da3-979">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-979">Driver'Licence</span></span>
- <span data-ttu-id="14da3-980">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-980">Driver'Licences</span></span>
- <span data-ttu-id="14da3-981">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-981">Driver' Lic</span></span>
- <span data-ttu-id="14da3-982">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-982">Driver' Lics</span></span>
- <span data-ttu-id="14da3-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="14da3-983">Driver' License</span></span>
- <span data-ttu-id="14da3-984">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-984">Driver' Licenses</span></span>
- <span data-ttu-id="14da3-985">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-985">Driver' Licence</span></span>
- <span data-ttu-id="14da3-986">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-986">Driver' Licences</span></span>
- <span data-ttu-id="14da3-987">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="14da3-987">Driver'sLic</span></span>
- <span data-ttu-id="14da3-988">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="14da3-988">Driver'sLics</span></span>
- <span data-ttu-id="14da3-989">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-989">Driver'sLicense</span></span>
- <span data-ttu-id="14da3-990">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-990">Driver'sLicenses</span></span>
- <span data-ttu-id="14da3-991">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="14da3-991">Driver'sLicence</span></span>
- <span data-ttu-id="14da3-992">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="14da3-992">Driver'sLicences</span></span>
- <span data-ttu-id="14da3-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-993">Driver's Lic</span></span>
- <span data-ttu-id="14da3-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-994">Driver's Lics</span></span>
- <span data-ttu-id="14da3-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="14da3-995">Driver's License</span></span>
- <span data-ttu-id="14da3-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-996">Driver's Licenses</span></span>
- <span data-ttu-id="14da3-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-997">Driver's Licence</span></span>
- <span data-ttu-id="14da3-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-998">Driver's Licences</span></span>
- <span data-ttu-id="14da3-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="14da3-999">Permis de Conduire</span></span>
- <span data-ttu-id="14da3-1000">id</span><span class="sxs-lookup"><span data-stu-id="14da3-1000">id</span></span>
- <span data-ttu-id="14da3-1001">ids</span><span class="sxs-lookup"><span data-stu-id="14da3-1001">ids</span></span>
- <span data-ttu-id="14da3-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="14da3-1002">idcard number</span></span>
- <span data-ttu-id="14da3-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-1003">idcard numbers</span></span>
- <span data-ttu-id="14da3-1004">idcard#</span><span class="sxs-lookup"><span data-stu-id="14da3-1004">idcard #</span></span>
- <span data-ttu-id="14da3-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="14da3-1005">idcard #s</span></span>
- <span data-ttu-id="14da3-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="14da3-1006">idcard card</span></span>
- <span data-ttu-id="14da3-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1007">idcard cards</span></span>
- <span data-ttu-id="14da3-1008">идкард</span><span class="sxs-lookup"><span data-stu-id="14da3-1008">idcard</span></span>
- <span data-ttu-id="14da3-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-1009">identification number</span></span>
- <span data-ttu-id="14da3-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-1010">identification numbers</span></span>
- <span data-ttu-id="14da3-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="14da3-1011">identification #</span></span>
- <span data-ttu-id="14da3-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="14da3-1012">identification #s</span></span>
- <span data-ttu-id="14da3-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="14da3-1013">identification card</span></span>
- <span data-ttu-id="14da3-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1014">identification cards</span></span>
- <span data-ttu-id="14da3-1015">процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-1015">identification</span></span> 
- <span data-ttu-id="14da3-1016">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-1016">DL#</span></span>
- <span data-ttu-id="14da3-1017">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="14da3-1017">DLS#</span></span> 
- <span data-ttu-id="14da3-1018">КДЛ #</span><span class="sxs-lookup"><span data-stu-id="14da3-1018">CDL#</span></span> 
- <span data-ttu-id="14da3-1019">КДЛС #</span><span class="sxs-lookup"><span data-stu-id="14da3-1019">CDLS#</span></span> 
- <span data-ttu-id="14da3-1020">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="14da3-1020">DriverLic#</span></span> 
- <span data-ttu-id="14da3-1021">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-1021">DriverLics#</span></span> 
- <span data-ttu-id="14da3-1022">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-1022">DriverLicense#</span></span> 
- <span data-ttu-id="14da3-1023">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="14da3-1024">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="14da3-1024">DriverLicence#</span></span> 
- <span data-ttu-id="14da3-1025">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="14da3-1025">DriverLicences#</span></span> 
- <span data-ttu-id="14da3-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-1026">Driver Lic#</span></span>
- <span data-ttu-id="14da3-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-1027">Driver Lics#</span></span> 
- <span data-ttu-id="14da3-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="14da3-1028">Driver License#</span></span> 
- <span data-ttu-id="14da3-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="14da3-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="14da3-1030">Driver License#</span></span> 
- <span data-ttu-id="14da3-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-1031">Driver Licences#</span></span> 
- <span data-ttu-id="14da3-1032">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="14da3-1032">DriversLic#</span></span> 
- <span data-ttu-id="14da3-1033">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-1033">DriversLics#</span></span> 
- <span data-ttu-id="14da3-1034">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-1034">DriversLicense#</span></span> 
- <span data-ttu-id="14da3-1035">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="14da3-1036">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="14da3-1036">DriversLicence#</span></span> 
- <span data-ttu-id="14da3-1037">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="14da3-1037">DriversLicences#</span></span> 
- <span data-ttu-id="14da3-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="14da3-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="14da3-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="14da3-1040">Drivers License#</span></span> 
- <span data-ttu-id="14da3-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="14da3-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="14da3-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="14da3-1044">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="14da3-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="14da3-1045">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="14da3-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="14da3-1046">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="14da3-1046">Driver'License#</span></span> 
- <span data-ttu-id="14da3-1047">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="14da3-1048">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="14da3-1049">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="14da3-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="14da3-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="14da3-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="14da3-1052">Driver' License#</span></span> 
- <span data-ttu-id="14da3-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="14da3-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="14da3-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="14da3-1056">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="14da3-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="14da3-1057">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="14da3-1058">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="14da3-1059">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="14da3-1060">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="14da3-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="14da3-1061">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="14da3-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="14da3-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="14da3-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="14da3-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="14da3-1064">Driver's License#</span></span> 
- <span data-ttu-id="14da3-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="14da3-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="14da3-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="14da3-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="14da3-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="14da3-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="14da3-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="14da3-1069">кодов</span><span class="sxs-lookup"><span data-stu-id="14da3-1069">id#</span></span> 
- <span data-ttu-id="14da3-1070">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="14da3-1070">ids#</span></span> 
- <span data-ttu-id="14da3-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="14da3-1071">idcard card#</span></span> 
- <span data-ttu-id="14da3-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="14da3-1072">idcard cards#</span></span> 
- <span data-ttu-id="14da3-1073">идкард #</span><span class="sxs-lookup"><span data-stu-id="14da3-1073">idcard#</span></span> 
- <span data-ttu-id="14da3-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="14da3-1074">identification card#</span></span> 
- <span data-ttu-id="14da3-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="14da3-1075">identification cards#</span></span> 
- <span data-ttu-id="14da3-1076">процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="14da3-1077">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="14da3-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1078">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1078">Format</span></span>

<span data-ttu-id="14da3-1079">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1080">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1080">Pattern</span></span>

<span data-ttu-id="14da3-1081">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1082">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1082">Checksum</span></span>

<span data-ttu-id="14da3-1083">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1084">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1084">Definition</span></span>

<span data-ttu-id="14da3-1085">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1086">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1087">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1088">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1088">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="14da3-1089">Кэйворд_канада_хеалс_сервице_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="14da3-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="14da3-1090">personal health number</span></span>
- <span data-ttu-id="14da3-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="14da3-1091">patient information</span></span>
- <span data-ttu-id="14da3-1092">health services</span><span class="sxs-lookup"><span data-stu-id="14da3-1092">health services</span></span>
- <span data-ttu-id="14da3-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="14da3-1093">speciality services</span></span>
- <span data-ttu-id="14da3-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="14da3-1094">automobile accident</span></span>
- <span data-ttu-id="14da3-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="14da3-1095">patient hospital</span></span>
- <span data-ttu-id="14da3-1096">псичиатрист</span><span class="sxs-lookup"><span data-stu-id="14da3-1096">psychiatrist</span></span>
- <span data-ttu-id="14da3-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="14da3-1097">workers compensation</span></span>
- <span data-ttu-id="14da3-1098">ограничен</span><span class="sxs-lookup"><span data-stu-id="14da3-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="14da3-1099">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="14da3-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1100">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1100">Format</span></span>

<span data-ttu-id="14da3-1101">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1102">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1102">Pattern</span></span>

<span data-ttu-id="14da3-1103">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1104">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1104">Checksum</span></span>

<span data-ttu-id="14da3-1105">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1106">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1106">Definition</span></span>

<span data-ttu-id="14da3-1107">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1108">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1109">Найдено ключевое слово из Кэйворд_канада_пасспорт_нумбер или Кэйворд_пасспорт.</span><span class="sxs-lookup"><span data-stu-id="14da3-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1110">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1110">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="14da3-1111">Кэйворд_канада_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="14da3-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="14da3-1112">canadian citizenship</span></span>
- <span data-ttu-id="14da3-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="14da3-1113">canadian passport</span></span>
- <span data-ttu-id="14da3-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="14da3-1114">passport application</span></span>
- <span data-ttu-id="14da3-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="14da3-1115">passport photos</span></span>
- <span data-ttu-id="14da3-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="14da3-1116">certified translator</span></span>
- <span data-ttu-id="14da3-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="14da3-1117">canadian citizens</span></span>
- <span data-ttu-id="14da3-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="14da3-1118">processing times</span></span>
- <span data-ttu-id="14da3-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="14da3-1119">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="14da3-1120">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-1120">Keyword_passport</span></span>

- <span data-ttu-id="14da3-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="14da3-1121">Passport Number</span></span>
- <span data-ttu-id="14da3-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="14da3-1122">Passport No</span></span>
- <span data-ttu-id="14da3-1123">Passport#</span><span class="sxs-lookup"><span data-stu-id="14da3-1123">Passport #</span></span>
- <span data-ttu-id="14da3-1124">Службу</span><span class="sxs-lookup"><span data-stu-id="14da3-1124">Passport#</span></span>
- <span data-ttu-id="14da3-1125">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="14da3-1125">PassportID</span></span>
- <span data-ttu-id="14da3-1126">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="14da3-1126">Passportno</span></span>
- <span data-ttu-id="14da3-1127">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-1127">passportnumber</span></span>
- <span data-ttu-id="14da3-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="14da3-1128">パスポート</span></span>
- <span data-ttu-id="14da3-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="14da3-1129">パスポート番号</span></span>
- <span data-ttu-id="14da3-1130">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="14da3-1130">パスポートのNum</span></span>
- <span data-ttu-id="14da3-1131">パスポート #</span><span class="sxs-lookup"><span data-stu-id="14da3-1131">パスポート＃</span></span>
- <span data-ttu-id="14da3-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="14da3-1132">Numéro de passeport</span></span>
- <span data-ttu-id="14da3-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="14da3-1133">Passeport n °</span></span>
- <span data-ttu-id="14da3-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="14da3-1134">Passeport Non</span></span>
- <span data-ttu-id="14da3-1135">Passeport#</span><span class="sxs-lookup"><span data-stu-id="14da3-1135">Passeport #</span></span>
- <span data-ttu-id="14da3-1136">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="14da3-1136">Passeport#</span></span>
- <span data-ttu-id="14da3-1137">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="14da3-1137">PasseportNon</span></span>
- <span data-ttu-id="14da3-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="14da3-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="14da3-1139">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="14da3-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1140">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1140">Format</span></span>

<span data-ttu-id="14da3-1141">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1142">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1142">Pattern</span></span>

<span data-ttu-id="14da3-1143">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1144">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1144">Checksum</span></span>

<span data-ttu-id="14da3-1145">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1146">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1146">Definition</span></span>

<span data-ttu-id="14da3-1147">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_канада_фин находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-1148">Найдены по крайней мере два ключевых слова от Кэйворд_канада_фин или Кэйворд_канада_провинцес.</span><span class="sxs-lookup"><span data-stu-id="14da3-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1149">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1149">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="14da3-1150">Кэйворд_канада_фин</span><span class="sxs-lookup"><span data-stu-id="14da3-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="14da3-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="14da3-1151">social insurance number</span></span>
- <span data-ttu-id="14da3-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="14da3-1152">health information act</span></span>
- <span data-ttu-id="14da3-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="14da3-1153">income tax information</span></span>
- <span data-ttu-id="14da3-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="14da3-1154">manitoba health</span></span>
- <span data-ttu-id="14da3-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="14da3-1155">health registration</span></span>
- <span data-ttu-id="14da3-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="14da3-1156">prescription purchases</span></span>
- <span data-ttu-id="14da3-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="14da3-1157">benefit eligibility</span></span>
- <span data-ttu-id="14da3-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="14da3-1158">personal health</span></span>
- <span data-ttu-id="14da3-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="14da3-1159">power of attorney</span></span>
- <span data-ttu-id="14da3-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="14da3-1160">registration number</span></span>
- <span data-ttu-id="14da3-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="14da3-1161">personal health number</span></span>
- <span data-ttu-id="14da3-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="14da3-1162">practitioner referral</span></span>
- <span data-ttu-id="14da3-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="14da3-1163">wellness professional</span></span>
- <span data-ttu-id="14da3-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="14da3-1164">patient referral</span></span>
- <span data-ttu-id="14da3-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="14da3-1165">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="14da3-1166">Кэйворд_канада_провинцес</span><span class="sxs-lookup"><span data-stu-id="14da3-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="14da3-1167">Нунавут</span><span class="sxs-lookup"><span data-stu-id="14da3-1167">Nunavut</span></span>
- <span data-ttu-id="14da3-1168">Квебека</span><span class="sxs-lookup"><span data-stu-id="14da3-1168">Quebec</span></span>
- <span data-ttu-id="14da3-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="14da3-1169">Northwest Territories</span></span>
- <span data-ttu-id="14da3-1170">Онтарио</span><span class="sxs-lookup"><span data-stu-id="14da3-1170">Ontario</span></span>
- <span data-ttu-id="14da3-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="14da3-1171">British Columbia</span></span>
- <span data-ttu-id="14da3-1172">Альберта</span><span class="sxs-lookup"><span data-stu-id="14da3-1172">Alberta</span></span>
- <span data-ttu-id="14da3-1173">Саскачеван</span><span class="sxs-lookup"><span data-stu-id="14da3-1173">Saskatchewan</span></span>
- <span data-ttu-id="14da3-1174">Манитоба</span><span class="sxs-lookup"><span data-stu-id="14da3-1174">Manitoba</span></span>
- <span data-ttu-id="14da3-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="14da3-1175">Yukon</span></span>
- <span data-ttu-id="14da3-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="14da3-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="14da3-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="14da3-1177">New Brunswick</span></span>
- <span data-ttu-id="14da3-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="14da3-1178">Nova Scotia</span></span>
- <span data-ttu-id="14da3-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="14da3-1179">Prince Edward Island</span></span>
- <span data-ttu-id="14da3-1180">Канада</span><span class="sxs-lookup"><span data-stu-id="14da3-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="14da3-1181">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="14da3-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1182">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1182">Format</span></span>

<span data-ttu-id="14da3-1183">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="14da3-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1184">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1184">Pattern</span></span>

<span data-ttu-id="14da3-1185">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="14da3-1185">Formatted:</span></span>
- <span data-ttu-id="14da3-1186">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-1186">Three digits</span></span> 
- <span data-ttu-id="14da3-1187">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-1187">A hyphen or space</span></span> 
- <span data-ttu-id="14da3-1188">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-1188">Three digits</span></span> 
- <span data-ttu-id="14da3-1189">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-1189">A hyphen or space</span></span> 
- <span data-ttu-id="14da3-1190">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-1190">Three digits</span></span>

<span data-ttu-id="14da3-1191">Неформатированные: девять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1192">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1192">Checksum</span></span>

<span data-ttu-id="14da3-1193">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1194">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1194">Definition</span></span>

<span data-ttu-id="14da3-1195">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1196">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1197">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="14da3-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="14da3-1198">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="14da3-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="14da3-1199">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="14da3-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="14da3-1200">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="14da3-1201">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1201">The checksum passes.</span></span>

<span data-ttu-id="14da3-1202">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1203">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1204">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="14da3-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="14da3-1205">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1205">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1206">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1206">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="14da3-1207">Кэйворд_син</span><span class="sxs-lookup"><span data-stu-id="14da3-1207">Keyword_sin</span></span>

- <span data-ttu-id="14da3-1208">sin</span><span class="sxs-lookup"><span data-stu-id="14da3-1208">sin</span></span> 
- <span data-ttu-id="14da3-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="14da3-1209">social insurance</span></span> 
- <span data-ttu-id="14da3-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="14da3-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="14da3-1211">грехов</span><span class="sxs-lookup"><span data-stu-id="14da3-1211">sins</span></span> 
- <span data-ttu-id="14da3-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="14da3-1212">ssn</span></span> 
- <span data-ttu-id="14da3-1213">ssNS</span><span class="sxs-lookup"><span data-stu-id="14da3-1213">ssns</span></span> 
- <span data-ttu-id="14da3-1214">social security</span><span class="sxs-lookup"><span data-stu-id="14da3-1214">social security</span></span> 
- <span data-ttu-id="14da3-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="14da3-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="14da3-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-1216">national identification number</span></span> 
- <span data-ttu-id="14da3-1217">national id</span><span class="sxs-lookup"><span data-stu-id="14da3-1217">national id</span></span> 
- <span data-ttu-id="14da3-1218">Синус</span><span class="sxs-lookup"><span data-stu-id="14da3-1218">sin#</span></span> 
- <span data-ttu-id="14da3-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="14da3-1219">soc ins</span></span> 
- <span data-ttu-id="14da3-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="14da3-1220">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="14da3-1221">Кэйворд_син_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="14da3-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="14da3-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="14da3-1222">driver's license</span></span> 
- <span data-ttu-id="14da3-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="14da3-1223">drivers license</span></span> 
- <span data-ttu-id="14da3-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="14da3-1224">driver's licence</span></span> 
- <span data-ttu-id="14da3-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="14da3-1225">drivers licence</span></span> 
- <span data-ttu-id="14da3-1226">ДОБ</span><span class="sxs-lookup"><span data-stu-id="14da3-1226">DOB</span></span> 
- <span data-ttu-id="14da3-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="14da3-1227">Birthdate</span></span> 
- <span data-ttu-id="14da3-1228">День рождения </span><span class="sxs-lookup"><span data-stu-id="14da3-1228">Birthday</span></span> 
- <span data-ttu-id="14da3-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="14da3-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="14da3-1230">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="14da3-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1231">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1231">Format</span></span>

<span data-ttu-id="14da3-1232">7-8 цифр и разделители — контрольная цифра или буква</span><span class="sxs-lookup"><span data-stu-id="14da3-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1233">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1233">Pattern</span></span>

<span data-ttu-id="14da3-1234">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="14da3-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="14da3-1235">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-1235">1-2 digits</span></span> 
- <span data-ttu-id="14da3-1236">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-1236">A period</span></span> 
- <span data-ttu-id="14da3-1237">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-1237">Three digits</span></span> 
- <span data-ttu-id="14da3-1238">точка;</span><span class="sxs-lookup"><span data-stu-id="14da3-1238">A period</span></span> 
- <span data-ttu-id="14da3-1239">три цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-1239">Three digits</span></span> 
- <span data-ttu-id="14da3-1240">тире;</span><span class="sxs-lookup"><span data-stu-id="14da3-1240">A dash</span></span> 
- <span data-ttu-id="14da3-1241">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1242">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1242">Checksum</span></span>

<span data-ttu-id="14da3-1243">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1244">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1244">Definition</span></span>

<span data-ttu-id="14da3-1245">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1246">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1247">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="14da3-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="14da3-1248">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1248">The checksum passes.</span></span>

<span data-ttu-id="14da3-1249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1250">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1251">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1251">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1252">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1252">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="14da3-1253">Кэйворд_чиле_ид_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="14da3-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="14da3-1254">National Identification Number</span></span> 
- <span data-ttu-id="14da3-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="14da3-1255">Identity card</span></span> 
- <span data-ttu-id="14da3-1256">ID</span><span class="sxs-lookup"><span data-stu-id="14da3-1256">ID</span></span> 
- <span data-ttu-id="14da3-1257">Процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-1257">Identification</span></span> 
- <span data-ttu-id="14da3-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="14da3-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="14da3-1259">ВЫПОЛНЯЕМ</span><span class="sxs-lookup"><span data-stu-id="14da3-1259">RUN</span></span> 
- <span data-ttu-id="14da3-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="14da3-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="14da3-1261">СНИЖАТЬСЯ</span><span class="sxs-lookup"><span data-stu-id="14da3-1261">RUT</span></span> 
- <span data-ttu-id="14da3-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="14da3-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="14da3-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="14da3-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="14da3-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="14da3-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="14da3-1265">ИдентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="14da3-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="14da3-1266">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="14da3-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1267">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1267">Format</span></span>

<span data-ttu-id="14da3-1268">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1269">Pattern</span></span>

<span data-ttu-id="14da3-1270">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-1270">18 digits:</span></span>
- <span data-ttu-id="14da3-1271">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="14da3-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="14da3-1272">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="14da3-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="14da3-1273">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="14da3-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="14da3-1274">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1275">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1275">Checksum</span></span>

<span data-ttu-id="14da3-1276">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1277">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1277">Definition</span></span>

<span data-ttu-id="14da3-1278">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1279">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1280">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="14da3-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="14da3-1281">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1281">The checksum passes.</span></span>

<span data-ttu-id="14da3-1282">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1283">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1284">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1284">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1285">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1285">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="14da3-1286">Кэйворд_чина_ресидент_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="14da3-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="14da3-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="14da3-1288">NO7</span><span class="sxs-lookup"><span data-stu-id="14da3-1288">PRC</span></span> 
- <span data-ttu-id="14da3-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="14da3-1289">National Identification Card</span></span> 
- <span data-ttu-id="14da3-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="14da3-1290">身份证</span></span> 
- <span data-ttu-id="14da3-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="14da3-1291">居民 身份证</span></span> 
- <span data-ttu-id="14da3-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="14da3-1292">居民身份证</span></span> 
- <span data-ttu-id="14da3-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="14da3-1293">鉴定</span></span> 
- <span data-ttu-id="14da3-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-1294">身分證</span></span> 
- <span data-ttu-id="14da3-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-1295">居民 身份證</span></span>
- <span data-ttu-id="14da3-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="14da3-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="14da3-1297">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="14da3-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1298">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1298">Format</span></span>

<span data-ttu-id="14da3-1299">16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.</span><span class="sxs-lookup"><span data-stu-id="14da3-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1300">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1300">Pattern</span></span>

<span data-ttu-id="14da3-1301">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="14da3-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1302">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1302">Checksum</span></span>

<span data-ttu-id="14da3-1303">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="14da3-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1304">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1304">Definition</span></span>

<span data-ttu-id="14da3-1305">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1306">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1307">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-1307">One of the following is true:</span></span>
    - <span data-ttu-id="14da3-1308">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="14da3-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="14da3-1309">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="14da3-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="14da3-1310">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="14da3-1311">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1311">The checksum passes.</span></span>

<span data-ttu-id="14da3-1312">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1313">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1314">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1314">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1315">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="14da3-1316">Кэйворд_кк_верификатион</span><span class="sxs-lookup"><span data-stu-id="14da3-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="14da3-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="14da3-1317">card verification</span></span>
- <span data-ttu-id="14da3-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-1318">card identification number</span></span>
- <span data-ttu-id="14da3-1319">КВН</span><span class="sxs-lookup"><span data-stu-id="14da3-1319">cvn</span></span>
- <span data-ttu-id="14da3-1320">cid</span><span class="sxs-lookup"><span data-stu-id="14da3-1320">cid</span></span>
- <span data-ttu-id="14da3-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="14da3-1321">cvc2</span></span>
- <span data-ttu-id="14da3-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="14da3-1322">cvv2</span></span>
- <span data-ttu-id="14da3-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="14da3-1323">pin block</span></span>
- <span data-ttu-id="14da3-1324">security code</span><span class="sxs-lookup"><span data-stu-id="14da3-1324">security code</span></span>
- <span data-ttu-id="14da3-1325">security number</span><span class="sxs-lookup"><span data-stu-id="14da3-1325">security number</span></span>
- <span data-ttu-id="14da3-1326">security no</span><span class="sxs-lookup"><span data-stu-id="14da3-1326">security no</span></span>
- <span data-ttu-id="14da3-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="14da3-1327">issue number</span></span>
- <span data-ttu-id="14da3-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="14da3-1328">issue no</span></span>
- <span data-ttu-id="14da3-1329">криптограмме</span><span class="sxs-lookup"><span data-stu-id="14da3-1329">cryptogramme</span></span>
- <span data-ttu-id="14da3-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="14da3-1330">numéro de sécurité</span></span>
- <span data-ttu-id="14da3-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="14da3-1331">numero de securite</span></span>
- <span data-ttu-id="14da3-1332">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="14da3-1333">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="14da3-1334">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="14da3-1334">prüfziffer</span></span>
- <span data-ttu-id="14da3-1335">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="14da3-1335">prufziffer</span></span>
- <span data-ttu-id="14da3-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="14da3-1336">sicherheits Kode</span></span>
- <span data-ttu-id="14da3-1337">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="14da3-1337">sicherheitscode</span></span>
- <span data-ttu-id="14da3-1338">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="14da3-1339">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1339">verfalldatum</span></span>
- <span data-ttu-id="14da3-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="14da3-1340">codice di verifica</span></span>
- <span data-ttu-id="14da3-1341">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1341">cod.</span></span> <span data-ttu-id="14da3-1342">сикурезза</span><span class="sxs-lookup"><span data-stu-id="14da3-1342">sicurezza</span></span>
- <span data-ttu-id="14da3-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="14da3-1343">cod sicurezza</span></span>
- <span data-ttu-id="14da3-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="14da3-1344">n autorizzazione</span></span>
- <span data-ttu-id="14da3-1345">кóдиго</span><span class="sxs-lookup"><span data-stu-id="14da3-1345">código</span></span>
- <span data-ttu-id="14da3-1346">кодиго</span><span class="sxs-lookup"><span data-stu-id="14da3-1346">codigo</span></span>
- <span data-ttu-id="14da3-1347">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1347">cod.</span></span> <span data-ttu-id="14da3-1348">СЕГ</span><span class="sxs-lookup"><span data-stu-id="14da3-1348">seg</span></span>
- <span data-ttu-id="14da3-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="14da3-1349">cod seg</span></span>
- <span data-ttu-id="14da3-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1350">código de segurança</span></span>
- <span data-ttu-id="14da3-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1351">codigo de seguranca</span></span>
- <span data-ttu-id="14da3-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1352">codigo de segurança</span></span>
- <span data-ttu-id="14da3-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1353">código de seguranca</span></span>
- <span data-ttu-id="14da3-1354">кóд.</span><span class="sxs-lookup"><span data-stu-id="14da3-1354">cód.</span></span> <span data-ttu-id="14da3-1355">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="14da3-1355">segurança</span></span>
- <span data-ttu-id="14da3-1356">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1356">cod.</span></span> <span data-ttu-id="14da3-1357">сегуранка наложенный платеж.</span><span class="sxs-lookup"><span data-stu-id="14da3-1357">seguranca cod.</span></span> <span data-ttu-id="14da3-1358">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="14da3-1358">segurança</span></span>
- <span data-ttu-id="14da3-1359">кóд.</span><span class="sxs-lookup"><span data-stu-id="14da3-1359">cód.</span></span> <span data-ttu-id="14da3-1360">сегуранка</span><span class="sxs-lookup"><span data-stu-id="14da3-1360">seguranca</span></span>
- <span data-ttu-id="14da3-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1361">cód segurança</span></span>
- <span data-ttu-id="14da3-1362">наложенный на наложенный сегуранка сегуранçа</span><span class="sxs-lookup"><span data-stu-id="14da3-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="14da3-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1363">cód seguranca</span></span>
- <span data-ttu-id="14da3-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="14da3-1364">número de verificação</span></span>
- <span data-ttu-id="14da3-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="14da3-1365">numero de verificacao</span></span>
- <span data-ttu-id="14da3-1366">аблауф</span><span class="sxs-lookup"><span data-stu-id="14da3-1366">ablauf</span></span>
- <span data-ttu-id="14da3-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="14da3-1367">gültig bis</span></span>
- <span data-ttu-id="14da3-1368">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="14da3-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="14da3-1369">gultig bis</span></span>
- <span data-ttu-id="14da3-1370">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="14da3-1371">скаденза</span><span class="sxs-lookup"><span data-stu-id="14da3-1371">scadenza</span></span>
- <span data-ttu-id="14da3-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="14da3-1372">data scad</span></span>
- <span data-ttu-id="14da3-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="14da3-1373">fecha de expiracion</span></span>
- <span data-ttu-id="14da3-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="14da3-1374">fecha de venc</span></span>
- <span data-ttu-id="14da3-1375">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="14da3-1375">vencimiento</span></span>
- <span data-ttu-id="14da3-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="14da3-1376">válido hasta</span></span>
- <span data-ttu-id="14da3-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="14da3-1377">valido hasta</span></span>
- <span data-ttu-id="14da3-1378">ВТО</span><span class="sxs-lookup"><span data-stu-id="14da3-1378">vto</span></span>
- <span data-ttu-id="14da3-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="14da3-1379">data de expiração</span></span>
- <span data-ttu-id="14da3-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="14da3-1380">data de expiracao</span></span>
- <span data-ttu-id="14da3-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="14da3-1381">data em que expira</span></span>
- <span data-ttu-id="14da3-1382">валидаде</span><span class="sxs-lookup"><span data-stu-id="14da3-1382">validade</span></span>
- <span data-ttu-id="14da3-1383">Валор</span><span class="sxs-lookup"><span data-stu-id="14da3-1383">valor</span></span>
- <span data-ttu-id="14da3-1384">венЦименто</span><span class="sxs-lookup"><span data-stu-id="14da3-1384">vencimento</span></span>
- <span data-ttu-id="14da3-1385">Венк</span><span class="sxs-lookup"><span data-stu-id="14da3-1385">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="14da3-1386">Кэйворд_кк_наме</span><span class="sxs-lookup"><span data-stu-id="14da3-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="14da3-1387">АМЕКС</span><span class="sxs-lookup"><span data-stu-id="14da3-1387">amex</span></span>
- <span data-ttu-id="14da3-1388">american express</span><span class="sxs-lookup"><span data-stu-id="14da3-1388">american express</span></span>
- <span data-ttu-id="14da3-1389">американекспресс</span><span class="sxs-lookup"><span data-stu-id="14da3-1389">americanexpress</span></span>
- <span data-ttu-id="14da3-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="14da3-1390">Visa</span></span>
- <span data-ttu-id="14da3-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="14da3-1391">mastercard</span></span>
- <span data-ttu-id="14da3-1392">master card</span><span class="sxs-lookup"><span data-stu-id="14da3-1392">master card</span></span>
- <span data-ttu-id="14da3-1393">MC</span><span class="sxs-lookup"><span data-stu-id="14da3-1393">mc</span></span> 
- <span data-ttu-id="14da3-1394">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1394">mastercards</span></span>
- <span data-ttu-id="14da3-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1395">master cards</span></span>
- <span data-ttu-id="14da3-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="14da3-1396">diner's Club</span></span>
- <span data-ttu-id="14da3-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="14da3-1397">diners club</span></span>
- <span data-ttu-id="14da3-1398">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="14da3-1398">dinersclub</span></span>
- <span data-ttu-id="14da3-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="14da3-1399">discover card</span></span>
- <span data-ttu-id="14da3-1400">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="14da3-1400">discovercard</span></span>
- <span data-ttu-id="14da3-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1401">discover cards</span></span>
- <span data-ttu-id="14da3-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="14da3-1402">JCB</span></span>
- <span data-ttu-id="14da3-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="14da3-1403">japanese card bureau</span></span>
- <span data-ttu-id="14da3-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="14da3-1404">carte blanche</span></span>
- <span data-ttu-id="14da3-1405">картебланче</span><span class="sxs-lookup"><span data-stu-id="14da3-1405">carteblanche</span></span>
- <span data-ttu-id="14da3-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="14da3-1406">credit card</span></span>
- <span data-ttu-id="14da3-1407">Центральной</span><span class="sxs-lookup"><span data-stu-id="14da3-1407">cc#</span></span>
- <span data-ttu-id="14da3-1408">CC #:</span><span class="sxs-lookup"><span data-stu-id="14da3-1408">cc#:</span></span>
- <span data-ttu-id="14da3-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="14da3-1409">expiration date</span></span>
- <span data-ttu-id="14da3-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="14da3-1410">exp date</span></span>
- <span data-ttu-id="14da3-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="14da3-1411">expiry date</span></span>
- <span data-ttu-id="14da3-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="14da3-1412">date d’expiration</span></span>
- <span data-ttu-id="14da3-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="14da3-1413">date d'exp</span></span>
- <span data-ttu-id="14da3-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="14da3-1414">date expiration</span></span>
- <span data-ttu-id="14da3-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="14da3-1415">bank card</span></span>
- <span data-ttu-id="14da3-1416">банккард</span><span class="sxs-lookup"><span data-stu-id="14da3-1416">bankcard</span></span>
- <span data-ttu-id="14da3-1417">card number</span><span class="sxs-lookup"><span data-stu-id="14da3-1417">card number</span></span>
- <span data-ttu-id="14da3-1418">card num</span><span class="sxs-lookup"><span data-stu-id="14da3-1418">card num</span></span>
- <span data-ttu-id="14da3-1419">карднумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-1419">cardnumber</span></span>
- <span data-ttu-id="14da3-1420">карднумберс</span><span class="sxs-lookup"><span data-stu-id="14da3-1420">cardnumbers</span></span>
- <span data-ttu-id="14da3-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-1421">card numbers</span></span>
- <span data-ttu-id="14da3-1422">кредиткард</span><span class="sxs-lookup"><span data-stu-id="14da3-1422">creditcard</span></span>
- <span data-ttu-id="14da3-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1423">credit cards</span></span>
- <span data-ttu-id="14da3-1424">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1424">creditcards</span></span>
- <span data-ttu-id="14da3-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="14da3-1425">ccn</span></span>
- <span data-ttu-id="14da3-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="14da3-1426">card holder</span></span>
- <span data-ttu-id="14da3-1427">банков</span><span class="sxs-lookup"><span data-stu-id="14da3-1427">cardholder</span></span>
- <span data-ttu-id="14da3-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="14da3-1428">card holders</span></span>
- <span data-ttu-id="14da3-1429">карты</span><span class="sxs-lookup"><span data-stu-id="14da3-1429">cardholders</span></span>
- <span data-ttu-id="14da3-1430">check card</span><span class="sxs-lookup"><span data-stu-id="14da3-1430">check card</span></span>
- <span data-ttu-id="14da3-1431">чекккард</span><span class="sxs-lookup"><span data-stu-id="14da3-1431">checkcard</span></span>
- <span data-ttu-id="14da3-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1432">check cards</span></span>
- <span data-ttu-id="14da3-1433">чекккардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1433">checkcards</span></span>
- <span data-ttu-id="14da3-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="14da3-1434">debit card</span></span>
- <span data-ttu-id="14da3-1435">дебиткард</span><span class="sxs-lookup"><span data-stu-id="14da3-1435">debitcard</span></span>
- <span data-ttu-id="14da3-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1436">debit cards</span></span>
- <span data-ttu-id="14da3-1437">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1437">debitcards</span></span>
- <span data-ttu-id="14da3-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="14da3-1438">atm card</span></span>
- <span data-ttu-id="14da3-1439">атмкард</span><span class="sxs-lookup"><span data-stu-id="14da3-1439">atmcard</span></span>
- <span data-ttu-id="14da3-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1440">atm cards</span></span>
- <span data-ttu-id="14da3-1441">атмкардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1441">atmcards</span></span>
- <span data-ttu-id="14da3-1442">енрауте</span><span class="sxs-lookup"><span data-stu-id="14da3-1442">enroute</span></span>
- <span data-ttu-id="14da3-1443">en route</span><span class="sxs-lookup"><span data-stu-id="14da3-1443">en route</span></span>
- <span data-ttu-id="14da3-1444">card type</span><span class="sxs-lookup"><span data-stu-id="14da3-1444">card type</span></span>
- <span data-ttu-id="14da3-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="14da3-1445">carte bancaire</span></span>
- <span data-ttu-id="14da3-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="14da3-1446">carte de crédit</span></span>
- <span data-ttu-id="14da3-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="14da3-1447">carte de credit</span></span>
- <span data-ttu-id="14da3-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1448">numéro de carte</span></span>
- <span data-ttu-id="14da3-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1449">numero de carte</span></span>
- <span data-ttu-id="14da3-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1450">nº de la carte</span></span>
- <span data-ttu-id="14da3-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1451">nº de carte</span></span>
- <span data-ttu-id="14da3-1452">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="14da3-1452">kreditkarte</span></span>
- <span data-ttu-id="14da3-1453">карте</span><span class="sxs-lookup"><span data-stu-id="14da3-1453">karte</span></span>
- <span data-ttu-id="14da3-1454">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="14da3-1454">karteninhaber</span></span>
- <span data-ttu-id="14da3-1455">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="14da3-1455">karteninhabers</span></span>
- <span data-ttu-id="14da3-1456">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="14da3-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="14da3-1457">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="14da3-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="14da3-1458">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="14da3-1458">kreditkartentyp</span></span>
- <span data-ttu-id="14da3-1459">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="14da3-1459">eigentümername</span></span>
- <span data-ttu-id="14da3-1460">картеннр</span><span class="sxs-lookup"><span data-stu-id="14da3-1460">kartennr</span></span> 
- <span data-ttu-id="14da3-1461">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1461">kartennummer</span></span>
- <span data-ttu-id="14da3-1462">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1462">kreditkartennummer</span></span>
- <span data-ttu-id="14da3-1463">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="14da3-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1464">carta di credito</span></span>
- <span data-ttu-id="14da3-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1465">carta credito</span></span>
- <span data-ttu-id="14da3-1466">Корзина "</span><span class="sxs-lookup"><span data-stu-id="14da3-1466">carta</span></span>
- <span data-ttu-id="14da3-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1467">n carta</span></span>
- <span data-ttu-id="14da3-1468">НР.</span><span class="sxs-lookup"><span data-stu-id="14da3-1468">nr.</span></span> <span data-ttu-id="14da3-1469">Корзина "</span><span class="sxs-lookup"><span data-stu-id="14da3-1469">carta</span></span>
- <span data-ttu-id="14da3-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1470">nr carta</span></span>
- <span data-ttu-id="14da3-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1471">numero carta</span></span>
- <span data-ttu-id="14da3-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1472">numero della carta</span></span>
- <span data-ttu-id="14da3-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1473">numero di carta</span></span>
- <span data-ttu-id="14da3-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1474">tarjeta credito</span></span>
- <span data-ttu-id="14da3-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1475">tarjeta de credito</span></span>
- <span data-ttu-id="14da3-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="14da3-1476">tarjeta crédito</span></span>
- <span data-ttu-id="14da3-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="14da3-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="14da3-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="14da3-1478">tarjeta de atm</span></span>
- <span data-ttu-id="14da3-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="14da3-1479">tarjeta atm</span></span>
- <span data-ttu-id="14da3-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1480">tarjeta debito</span></span>
- <span data-ttu-id="14da3-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1481">tarjeta de debito</span></span>
- <span data-ttu-id="14da3-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="14da3-1482">tarjeta débito</span></span>
- <span data-ttu-id="14da3-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="14da3-1483">tarjeta de débito</span></span>
- <span data-ttu-id="14da3-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1484">nº de tarjeta</span></span>
- <span data-ttu-id="14da3-1485">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1485">no.</span></span> <span data-ttu-id="14da3-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1486">de tarjeta</span></span>
- <span data-ttu-id="14da3-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1487">no de tarjeta</span></span>
- <span data-ttu-id="14da3-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1488">numero de tarjeta</span></span>
- <span data-ttu-id="14da3-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1489">número de tarjeta</span></span>
- <span data-ttu-id="14da3-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="14da3-1490">tarjeta no</span></span>
- <span data-ttu-id="14da3-1491">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="14da3-1491">tarjetahabiente</span></span>
- <span data-ttu-id="14da3-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="14da3-1492">cartão de crédito</span></span>
- <span data-ttu-id="14da3-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1493">cartão de credito</span></span>
- <span data-ttu-id="14da3-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="14da3-1494">cartao de crédito</span></span>
- <span data-ttu-id="14da3-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1495">cartao de credito</span></span>
- <span data-ttu-id="14da3-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="14da3-1496">cartão de débito</span></span>
- <span data-ttu-id="14da3-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="14da3-1497">cartao de débito</span></span>
- <span data-ttu-id="14da3-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1498">cartão de debito</span></span>
- <span data-ttu-id="14da3-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1499">cartao de debito</span></span>
- <span data-ttu-id="14da3-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="14da3-1500">débito automático</span></span>
- <span data-ttu-id="14da3-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="14da3-1501">debito automatico</span></span>
- <span data-ttu-id="14da3-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1502">número do cartão</span></span>
- <span data-ttu-id="14da3-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1503">numero do cartão</span></span> 
- <span data-ttu-id="14da3-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1504">número do cartao</span></span>
- <span data-ttu-id="14da3-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1505">numero do cartao</span></span>
- <span data-ttu-id="14da3-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1506">número de cartão</span></span>
- <span data-ttu-id="14da3-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1507">numero de cartão</span></span>
- <span data-ttu-id="14da3-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1508">número de cartao</span></span>
- <span data-ttu-id="14da3-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1509">numero de cartao</span></span>
- <span data-ttu-id="14da3-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1510">nº do cartão</span></span>
- <span data-ttu-id="14da3-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1511">nº do cartao</span></span>
- <span data-ttu-id="14da3-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="14da3-1512">nº.</span></span> <span data-ttu-id="14da3-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1513">do cartão</span></span>
- <span data-ttu-id="14da3-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1514">no do cartão</span></span>
- <span data-ttu-id="14da3-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1515">no do cartao</span></span>
- <span data-ttu-id="14da3-1516">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1516">no.</span></span> <span data-ttu-id="14da3-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1517">do cartão</span></span>
- <span data-ttu-id="14da3-1518">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1518">no.</span></span> <span data-ttu-id="14da3-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="14da3-1520">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="14da3-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1521">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1521">Format</span></span>

<span data-ttu-id="14da3-1522">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1523">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1523">Pattern</span></span>

<span data-ttu-id="14da3-1524">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1525">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1525">Checksum</span></span>

<span data-ttu-id="14da3-1526">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1527">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1527">Definition</span></span>

<span data-ttu-id="14da3-1528">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1529">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1530">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="14da3-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-1531">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1531">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="14da3-1532">Кэйворд_кроатиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="14da3-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="14da3-1533">Croatian identity card</span></span>
- <span data-ttu-id="14da3-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="14da3-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="14da3-1535">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="14da3-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1536">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1536">Format</span></span>

<span data-ttu-id="14da3-1537">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1538">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1538">Pattern</span></span>

<span data-ttu-id="14da3-1539">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-1539">11 digits:</span></span>
- <span data-ttu-id="14da3-1540">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1540">10 digits</span></span> 
- <span data-ttu-id="14da3-1541">Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1542">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1542">Checksum</span></span>

<span data-ttu-id="14da3-1543">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1544">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1544">Definition</span></span>

<span data-ttu-id="14da3-1545">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1546">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1547">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="14da3-1548">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1548">The checksum passes.</span></span>

<span data-ttu-id="14da3-1549">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1550">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1551">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1551">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1552">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1552">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="14da3-1553">Кэйворд_кроатиа_оиб_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="14da3-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="14da3-1554">Personal Identification Number</span></span>
- <span data-ttu-id="14da3-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="14da3-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="14da3-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="14da3-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="14da3-1557">Номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="14da3-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1558">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1558">Format</span></span>

<span data-ttu-id="14da3-1559">Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)</span><span class="sxs-lookup"><span data-stu-id="14da3-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1560">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1560">Pattern</span></span>

<span data-ttu-id="14da3-1561">Девять цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="14da3-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="14da3-1562">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1562">Nine digits</span></span>

<span data-ttu-id="14da3-1563">OR</span><span class="sxs-lookup"><span data-stu-id="14da3-1563">OR</span></span>

- <span data-ttu-id="14da3-1564">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="14da3-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="14da3-1565">косая черта;</span><span class="sxs-lookup"><span data-stu-id="14da3-1565">A forward slash</span></span>
- <span data-ttu-id="14da3-1566">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-1566">Three digits</span></span>

<span data-ttu-id="14da3-1567">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="14da3-1567">10 digits (new format):</span></span>
- <span data-ttu-id="14da3-1568">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1568">10 digits</span></span>

<span data-ttu-id="14da3-1569">OR</span><span class="sxs-lookup"><span data-stu-id="14da3-1569">OR</span></span>

- <span data-ttu-id="14da3-1570">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="14da3-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="14da3-1571">косая черта;</span><span class="sxs-lookup"><span data-stu-id="14da3-1571">A forward slash</span></span> 
- <span data-ttu-id="14da3-1572">Четыре цифры, где последняя цифра является контрольной цифрой</span><span class="sxs-lookup"><span data-stu-id="14da3-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1573">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1573">Checksum</span></span>

<span data-ttu-id="14da3-1574">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1575">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1575">Definition</span></span>

<span data-ttu-id="14da3-1576">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_кзеч_ид_кард находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-1577">находится ключевое слово из Keyword_czech_id_card;</span><span class="sxs-lookup"><span data-stu-id="14da3-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="14da3-1578">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1578">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="14da3-1579">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1579">Keywords</span></span>

- <span data-ttu-id="14da3-1580">номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="14da3-1580">czech personal identity number</span></span>
- <span data-ttu-id="14da3-1581">Роднé číсло</span><span class="sxs-lookup"><span data-stu-id="14da3-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="14da3-1582">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="14da3-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1583">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1583">Format</span></span>

<span data-ttu-id="14da3-1584">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="14da3-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1585">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1585">Pattern</span></span>

<span data-ttu-id="14da3-1586">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-1586">10 digits:</span></span>
- <span data-ttu-id="14da3-1587">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="14da3-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="14da3-1588">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-1588">A hyphen</span></span> 
- <span data-ttu-id="14da3-1589">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1590">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1590">Checksum</span></span>

<span data-ttu-id="14da3-1591">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1592">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1592">Definition</span></span>

<span data-ttu-id="14da3-1593">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_денмарк_ид находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-1594">находится ключевое слово из Keyword_denmark_id;</span><span class="sxs-lookup"><span data-stu-id="14da3-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="14da3-1595">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1595">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-1596">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1596">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="14da3-1597">Кэйворд_денмарк_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="14da3-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="14da3-1598">Personal Identification Number</span></span>
- <span data-ttu-id="14da3-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="14da3-1599">CPR</span></span>
- <span data-ttu-id="14da3-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="14da3-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="14da3-1601">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="14da3-1602">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="14da3-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1603">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1603">Format</span></span>

<span data-ttu-id="14da3-1604">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1605">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1605">Pattern</span></span>

<span data-ttu-id="14da3-1606">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="14da3-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="14da3-1607">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="14da3-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="14da3-1608">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="14da3-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="14da3-1609">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="14da3-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1610">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1610">Checksum</span></span>

<span data-ttu-id="14da3-1611">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1612">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1612">Definition</span></span>

<span data-ttu-id="14da3-1613">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1614">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1615">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1615">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-1616">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1616">Keywords</span></span>

<span data-ttu-id="14da3-1617">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="14da3-1618">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="14da3-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1619">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1619">Format</span></span>

<span data-ttu-id="14da3-1620">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1621">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1621">Pattern</span></span>

<span data-ttu-id="14da3-1622">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="14da3-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1623">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1623">Checksum</span></span>

<span data-ttu-id="14da3-1624">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1625">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1625">Definition</span></span>

<span data-ttu-id="14da3-1626">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1627">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1628">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="14da3-1629">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="14da3-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="14da3-1630">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="14da3-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="14da3-1631">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="14da3-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="14da3-1632">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="14da3-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="14da3-1633">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="14da3-1634">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1634">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1635">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1635">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="14da3-1636">Кэйворд_еу_дебит_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="14da3-1637">account number</span><span class="sxs-lookup"><span data-stu-id="14da3-1637">account number</span></span> 
- <span data-ttu-id="14da3-1638">card number</span><span class="sxs-lookup"><span data-stu-id="14da3-1638">card number</span></span> 
- <span data-ttu-id="14da3-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="14da3-1639">card no.</span></span> 
- <span data-ttu-id="14da3-1640">security number</span><span class="sxs-lookup"><span data-stu-id="14da3-1640">security number</span></span> 
- <span data-ttu-id="14da3-1641">Центральной</span><span class="sxs-lookup"><span data-stu-id="14da3-1641">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="14da3-1642">Кэйворд_кард_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="14da3-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="14da3-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="14da3-1643">acct nbr</span></span> 
- <span data-ttu-id="14da3-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="14da3-1644">acct num</span></span> 
- <span data-ttu-id="14da3-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="14da3-1645">acct no</span></span> 
- <span data-ttu-id="14da3-1646">american express</span><span class="sxs-lookup"><span data-stu-id="14da3-1646">american express</span></span> 
- <span data-ttu-id="14da3-1647">американекспресс</span><span class="sxs-lookup"><span data-stu-id="14da3-1647">americanexpress</span></span> 
- <span data-ttu-id="14da3-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="14da3-1648">americano espresso</span></span> 
- <span data-ttu-id="14da3-1649">АМЕКС</span><span class="sxs-lookup"><span data-stu-id="14da3-1649">amex</span></span> 
- <span data-ttu-id="14da3-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="14da3-1650">atm card</span></span> 
- <span data-ttu-id="14da3-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1651">atm cards</span></span> 
- <span data-ttu-id="14da3-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="14da3-1652">atm kaart</span></span> 
- <span data-ttu-id="14da3-1653">атмкард</span><span class="sxs-lookup"><span data-stu-id="14da3-1653">atmcard</span></span> 
- <span data-ttu-id="14da3-1654">атмкардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1654">atmcards</span></span> 
- <span data-ttu-id="14da3-1655">атмкаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1655">atmkaart</span></span> 
- <span data-ttu-id="14da3-1656">атмкаартен</span><span class="sxs-lookup"><span data-stu-id="14da3-1656">atmkaarten</span></span> 
- <span data-ttu-id="14da3-1657">банконтакт</span><span class="sxs-lookup"><span data-stu-id="14da3-1657">bancontact</span></span> 
- <span data-ttu-id="14da3-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="14da3-1658">bank card</span></span> 
- <span data-ttu-id="14da3-1659">банккаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1659">bankkaart</span></span> 
- <span data-ttu-id="14da3-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="14da3-1660">card holder</span></span> 
- <span data-ttu-id="14da3-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="14da3-1661">card holders</span></span> 
- <span data-ttu-id="14da3-1662">card num</span><span class="sxs-lookup"><span data-stu-id="14da3-1662">card num</span></span> 
- <span data-ttu-id="14da3-1663">card number</span><span class="sxs-lookup"><span data-stu-id="14da3-1663">card number</span></span> 
- <span data-ttu-id="14da3-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-1664">card numbers</span></span> 
- <span data-ttu-id="14da3-1665">card type</span><span class="sxs-lookup"><span data-stu-id="14da3-1665">card type</span></span> 
- <span data-ttu-id="14da3-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="14da3-1666">cardano numerico</span></span> 
- <span data-ttu-id="14da3-1667">банков</span><span class="sxs-lookup"><span data-stu-id="14da3-1667">cardholder</span></span> 
- <span data-ttu-id="14da3-1668">карты</span><span class="sxs-lookup"><span data-stu-id="14da3-1668">cardholders</span></span> 
- <span data-ttu-id="14da3-1669">карднумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-1669">cardnumber</span></span> 
- <span data-ttu-id="14da3-1670">карднумберс</span><span class="sxs-lookup"><span data-stu-id="14da3-1670">cardnumbers</span></span> 
- <span data-ttu-id="14da3-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="14da3-1671">carta bianca</span></span> 
- <span data-ttu-id="14da3-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1672">carta credito</span></span> 
- <span data-ttu-id="14da3-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1673">carta di credito</span></span> 
- <span data-ttu-id="14da3-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1674">cartao de credito</span></span> 
- <span data-ttu-id="14da3-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="14da3-1675">cartao de crédito</span></span> 
- <span data-ttu-id="14da3-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1676">cartao de debito</span></span> 
- <span data-ttu-id="14da3-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="14da3-1677">cartao de débito</span></span> 
- <span data-ttu-id="14da3-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="14da3-1678">carte bancaire</span></span> 
- <span data-ttu-id="14da3-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="14da3-1679">carte blanche</span></span> 
- <span data-ttu-id="14da3-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="14da3-1680">carte bleue</span></span> 
- <span data-ttu-id="14da3-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="14da3-1681">carte de credit</span></span> 
- <span data-ttu-id="14da3-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="14da3-1682">carte de crédit</span></span> 
- <span data-ttu-id="14da3-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1683">carte di credito</span></span> 
- <span data-ttu-id="14da3-1684">картебланче</span><span class="sxs-lookup"><span data-stu-id="14da3-1684">carteblanche</span></span> 
- <span data-ttu-id="14da3-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1685">cartão de credito</span></span> 
- <span data-ttu-id="14da3-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="14da3-1686">cartão de crédito</span></span> 
- <span data-ttu-id="14da3-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1687">cartão de debito</span></span> 
- <span data-ttu-id="14da3-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="14da3-1688">cartão de débito</span></span> 
- <span data-ttu-id="14da3-1689">cb</span><span class="sxs-lookup"><span data-stu-id="14da3-1689">cb</span></span> 
- <span data-ttu-id="14da3-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="14da3-1690">ccn</span></span> 
- <span data-ttu-id="14da3-1691">check card</span><span class="sxs-lookup"><span data-stu-id="14da3-1691">check card</span></span> 
- <span data-ttu-id="14da3-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1692">check cards</span></span> 
- <span data-ttu-id="14da3-1693">чекккард</span><span class="sxs-lookup"><span data-stu-id="14da3-1693">checkcard</span></span>
- <span data-ttu-id="14da3-1694">чекккардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1694">checkcards</span></span> 
- <span data-ttu-id="14da3-1695">чекуекаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1695">chequekaart</span></span> 
- <span data-ttu-id="14da3-1696">Logic</span><span class="sxs-lookup"><span data-stu-id="14da3-1696">cirrus</span></span> 
- <span data-ttu-id="14da3-1697">Cirrus центр EDC — Маестро</span><span class="sxs-lookup"><span data-stu-id="14da3-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="14da3-1698">контролекаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1698">controlekaart</span></span> 
- <span data-ttu-id="14da3-1699">контролекаартен</span><span class="sxs-lookup"><span data-stu-id="14da3-1699">controlekaarten</span></span> 
- <span data-ttu-id="14da3-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="14da3-1700">credit card</span></span> 
- <span data-ttu-id="14da3-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1701">credit cards</span></span> 
- <span data-ttu-id="14da3-1702">кредиткард</span><span class="sxs-lookup"><span data-stu-id="14da3-1702">creditcard</span></span> 
- <span data-ttu-id="14da3-1703">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1703">creditcards</span></span> 
- <span data-ttu-id="14da3-1704">дебеткаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1704">debetkaart</span></span> 
- <span data-ttu-id="14da3-1705">дебеткаартен</span><span class="sxs-lookup"><span data-stu-id="14da3-1705">debetkaarten</span></span> 
- <span data-ttu-id="14da3-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="14da3-1706">debit card</span></span> 
- <span data-ttu-id="14da3-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1707">debit cards</span></span> 
- <span data-ttu-id="14da3-1708">дебиткард</span><span class="sxs-lookup"><span data-stu-id="14da3-1708">debitcard</span></span> 
- <span data-ttu-id="14da3-1709">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1709">debitcards</span></span> 
- <span data-ttu-id="14da3-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="14da3-1710">debito automatico</span></span> 
- <span data-ttu-id="14da3-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="14da3-1711">diners club</span></span> 
- <span data-ttu-id="14da3-1712">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="14da3-1712">dinersclub</span></span> 
- <span data-ttu-id="14da3-1713">Повтор</span><span class="sxs-lookup"><span data-stu-id="14da3-1713">discover</span></span> 
- <span data-ttu-id="14da3-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="14da3-1714">discover card</span></span> 
- <span data-ttu-id="14da3-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1715">discover cards</span></span> 
- <span data-ttu-id="14da3-1716">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="14da3-1716">discovercard</span></span> 
- <span data-ttu-id="14da3-1717">дисковеркардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1717">discovercards</span></span> 
- <span data-ttu-id="14da3-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="14da3-1718">débito automático</span></span>
- <span data-ttu-id="14da3-1719">центр EDC</span><span class="sxs-lookup"><span data-stu-id="14da3-1719">edc</span></span> 
- <span data-ttu-id="14da3-1720">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="14da3-1720">eigentümername</span></span> 
- <span data-ttu-id="14da3-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="14da3-1721">european debit card</span></span> 
- <span data-ttu-id="14da3-1722">хуфдкаарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1722">hoofdkaart</span></span> 
- <span data-ttu-id="14da3-1723">хуфдкаартен</span><span class="sxs-lookup"><span data-stu-id="14da3-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="14da3-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="14da3-1724">in viaggio</span></span> 
- <span data-ttu-id="14da3-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="14da3-1725">japanese card bureau</span></span> 
- <span data-ttu-id="14da3-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="14da3-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="14da3-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="14da3-1727">jcb</span></span> 
- <span data-ttu-id="14da3-1728">каарт</span><span class="sxs-lookup"><span data-stu-id="14da3-1728">kaart</span></span> 
- <span data-ttu-id="14da3-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="14da3-1729">kaart num</span></span> 
- <span data-ttu-id="14da3-1730">каартаантал</span><span class="sxs-lookup"><span data-stu-id="14da3-1730">kaartaantal</span></span> 
- <span data-ttu-id="14da3-1731">каартаанталлен</span><span class="sxs-lookup"><span data-stu-id="14da3-1731">kaartaantallen</span></span> 
- <span data-ttu-id="14da3-1732">каарсаудер</span><span class="sxs-lookup"><span data-stu-id="14da3-1732">kaarthouder</span></span> 
- <span data-ttu-id="14da3-1733">каарсаудерс</span><span class="sxs-lookup"><span data-stu-id="14da3-1733">kaarthouders</span></span> 
- <span data-ttu-id="14da3-1734">карте</span><span class="sxs-lookup"><span data-stu-id="14da3-1734">karte</span></span>  
- <span data-ttu-id="14da3-1735">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="14da3-1735">karteninhaber</span></span> 
- <span data-ttu-id="14da3-1736">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="14da3-1736">karteninhabers</span></span>
- <span data-ttu-id="14da3-1737">картеннр</span><span class="sxs-lookup"><span data-stu-id="14da3-1737">kartennr</span></span> 
- <span data-ttu-id="14da3-1738">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1738">kartennummer</span></span> 
- <span data-ttu-id="14da3-1739">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="14da3-1739">kreditkarte</span></span> 
- <span data-ttu-id="14da3-1740">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="14da3-1741">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="14da3-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="14da3-1742">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="14da3-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="14da3-1743">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="14da3-1744">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="14da3-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="14da3-1745">Маестро</span><span class="sxs-lookup"><span data-stu-id="14da3-1745">maestro</span></span> 
- <span data-ttu-id="14da3-1746">master card</span><span class="sxs-lookup"><span data-stu-id="14da3-1746">master card</span></span> 
- <span data-ttu-id="14da3-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="14da3-1747">master cards</span></span> 
- <span data-ttu-id="14da3-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="14da3-1748">mastercard</span></span> 
- <span data-ttu-id="14da3-1749">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="14da3-1749">mastercards</span></span> 
- <span data-ttu-id="14da3-1750">MC</span><span class="sxs-lookup"><span data-stu-id="14da3-1750">mc</span></span> 
- <span data-ttu-id="14da3-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="14da3-1751">mister cash</span></span> 
- <span data-ttu-id="14da3-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1752">n carta</span></span> 
- <span data-ttu-id="14da3-1753">Корзина "</span><span class="sxs-lookup"><span data-stu-id="14da3-1753">carta</span></span> 
- <span data-ttu-id="14da3-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1754">no de tarjeta</span></span> 
- <span data-ttu-id="14da3-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1755">no do cartao</span></span> 
- <span data-ttu-id="14da3-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1756">no do cartão</span></span> 
- <span data-ttu-id="14da3-1757">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1757">no.</span></span> <span data-ttu-id="14da3-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1758">de tarjeta</span></span> 
- <span data-ttu-id="14da3-1759">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1759">no.</span></span> <span data-ttu-id="14da3-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1760">do cartao</span></span> 
- <span data-ttu-id="14da3-1761">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1761">no.</span></span> <span data-ttu-id="14da3-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1762">do cartão</span></span> 
- <span data-ttu-id="14da3-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1763">nr carta</span></span> 
- <span data-ttu-id="14da3-1764">НР.</span><span class="sxs-lookup"><span data-stu-id="14da3-1764">nr.</span></span> <span data-ttu-id="14da3-1765">Корзина "</span><span class="sxs-lookup"><span data-stu-id="14da3-1765">carta</span></span> 
- <span data-ttu-id="14da3-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="14da3-1766">numeri di scheda</span></span> 
- <span data-ttu-id="14da3-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1767">numero carta</span></span> 
- <span data-ttu-id="14da3-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1768">numero de cartao</span></span> 
- <span data-ttu-id="14da3-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1769">numero de carte</span></span> 
- <span data-ttu-id="14da3-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1770">numero de cartão</span></span> 
- <span data-ttu-id="14da3-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1771">numero de tarjeta</span></span>
- <span data-ttu-id="14da3-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1772">numero della carta</span></span> 
- <span data-ttu-id="14da3-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1773">numero di carta</span></span> 
- <span data-ttu-id="14da3-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="14da3-1774">numero di scheda</span></span> 
- <span data-ttu-id="14da3-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1775">numero do cartao</span></span> 
- <span data-ttu-id="14da3-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1776">numero do cartão</span></span> 
- <span data-ttu-id="14da3-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1777">numéro de carte</span></span> 
- <span data-ttu-id="14da3-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="14da3-1778">nº carta</span></span> 
- <span data-ttu-id="14da3-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1779">nº de carte</span></span> 
- <span data-ttu-id="14da3-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="14da3-1780">nº de la carte</span></span> 
- <span data-ttu-id="14da3-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="14da3-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1782">nº do cartao</span></span> 
- <span data-ttu-id="14da3-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1783">nº do cartão</span></span> 
- <span data-ttu-id="14da3-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="14da3-1784">nº.</span></span> <span data-ttu-id="14da3-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1785">do cartão</span></span> 
- <span data-ttu-id="14da3-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1786">número de cartao</span></span> 
- <span data-ttu-id="14da3-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="14da3-1787">número de cartão</span></span> 
- <span data-ttu-id="14da3-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="14da3-1788">número de tarjeta</span></span> 
- <span data-ttu-id="14da3-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="14da3-1789">número do cartao</span></span> 
- <span data-ttu-id="14da3-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="14da3-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="14da3-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="14da3-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="14da3-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="14da3-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="14da3-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="14da3-1793">scheda della banca</span></span> 
- <span data-ttu-id="14da3-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="14da3-1794">scheda di controllo</span></span> 
- <span data-ttu-id="14da3-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1795">scheda di debito</span></span> 
- <span data-ttu-id="14da3-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="14da3-1796">scheda matrice</span></span> 
- <span data-ttu-id="14da3-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="14da3-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="14da3-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="14da3-1798">schede di controllo</span></span> 
- <span data-ttu-id="14da3-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1799">schede di debito</span></span> 
- <span data-ttu-id="14da3-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="14da3-1800">schede matrici</span></span> 
- <span data-ttu-id="14da3-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="14da3-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="14da3-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="14da3-1802">scoprono le schede</span></span> 
- <span data-ttu-id="14da3-1803">ОС</span><span class="sxs-lookup"><span data-stu-id="14da3-1803">solo</span></span> 
- <span data-ttu-id="14da3-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="14da3-1804">supporti di scheda</span></span> 
- <span data-ttu-id="14da3-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="14da3-1805">supporto di scheda</span></span> 
- <span data-ttu-id="14da3-1806">отключен</span><span class="sxs-lookup"><span data-stu-id="14da3-1806">switch</span></span> 
- <span data-ttu-id="14da3-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="14da3-1807">tarjeta atm</span></span> 
- <span data-ttu-id="14da3-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1808">tarjeta credito</span></span> 
- <span data-ttu-id="14da3-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="14da3-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="14da3-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="14da3-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="14da3-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="14da3-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="14da3-1812">tarjeta debito</span></span> 
- <span data-ttu-id="14da3-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="14da3-1813">tarjeta no</span></span>
- <span data-ttu-id="14da3-1814">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="14da3-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="14da3-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="14da3-1815">tipo della scheda</span></span> 
- <span data-ttu-id="14da3-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="14da3-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="14da3-1817">счеда</span><span class="sxs-lookup"><span data-stu-id="14da3-1817">scheda</span></span> 
- <span data-ttu-id="14da3-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="14da3-1818">v pay</span></span> 
- <span data-ttu-id="14da3-1819">v — оплата</span><span class="sxs-lookup"><span data-stu-id="14da3-1819">v-pay</span></span> 
- <span data-ttu-id="14da3-1820">Visa</span><span class="sxs-lookup"><span data-stu-id="14da3-1820">visa</span></span> 
- <span data-ttu-id="14da3-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="14da3-1821">visa plus</span></span> 
- <span data-ttu-id="14da3-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="14da3-1822">visa electron</span></span> 
- <span data-ttu-id="14da3-1823">висто</span><span class="sxs-lookup"><span data-stu-id="14da3-1823">visto</span></span> 
- <span data-ttu-id="14da3-1824">висум</span><span class="sxs-lookup"><span data-stu-id="14da3-1824">visum</span></span> 
- <span data-ttu-id="14da3-1825">впай</span><span class="sxs-lookup"><span data-stu-id="14da3-1825">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="14da3-1826">Кэйворд_кард_секурити_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="14da3-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="14da3-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-1827">card identification number</span></span>
- <span data-ttu-id="14da3-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="14da3-1828">card verification</span></span> 
- <span data-ttu-id="14da3-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="14da3-1829">cardi la verifica</span></span> 
- <span data-ttu-id="14da3-1830">cid</span><span class="sxs-lookup"><span data-stu-id="14da3-1830">cid</span></span> 
- <span data-ttu-id="14da3-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="14da3-1831">cod seg</span></span> 
- <span data-ttu-id="14da3-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1832">cod seguranca</span></span> 
- <span data-ttu-id="14da3-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1833">cod segurança</span></span> 
- <span data-ttu-id="14da3-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="14da3-1834">cod sicurezza</span></span> 
- <span data-ttu-id="14da3-1835">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1835">cod.</span></span> <span data-ttu-id="14da3-1836">СЕГ</span><span class="sxs-lookup"><span data-stu-id="14da3-1836">seg</span></span> 
- <span data-ttu-id="14da3-1837">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1837">cod.</span></span> <span data-ttu-id="14da3-1838">сегуранка</span><span class="sxs-lookup"><span data-stu-id="14da3-1838">seguranca</span></span> 
- <span data-ttu-id="14da3-1839">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1839">cod.</span></span> <span data-ttu-id="14da3-1840">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="14da3-1840">segurança</span></span> 
- <span data-ttu-id="14da3-1841">наложен.</span><span class="sxs-lookup"><span data-stu-id="14da3-1841">cod.</span></span> <span data-ttu-id="14da3-1842">сикурезза</span><span class="sxs-lookup"><span data-stu-id="14da3-1842">sicurezza</span></span> 
- <span data-ttu-id="14da3-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="14da3-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="14da3-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="14da3-1844">codice di verifica</span></span> 
- <span data-ttu-id="14da3-1845">кодиго</span><span class="sxs-lookup"><span data-stu-id="14da3-1845">codigo</span></span> 
- <span data-ttu-id="14da3-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="14da3-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1847">codigo de segurança</span></span> 
- <span data-ttu-id="14da3-1848">криттограмма</span><span class="sxs-lookup"><span data-stu-id="14da3-1848">crittogramma</span></span> 
- <span data-ttu-id="14da3-1849">криптограм</span><span class="sxs-lookup"><span data-stu-id="14da3-1849">cryptogram</span></span> 
- <span data-ttu-id="14da3-1850">криптограмме</span><span class="sxs-lookup"><span data-stu-id="14da3-1850">cryptogramme</span></span> 
- <span data-ttu-id="14da3-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="14da3-1851">cv2</span></span> 
- <span data-ttu-id="14da3-1852">КВК</span><span class="sxs-lookup"><span data-stu-id="14da3-1852">cvc</span></span> 
- <span data-ttu-id="14da3-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="14da3-1853">cvc2</span></span> 
- <span data-ttu-id="14da3-1854">КВН</span><span class="sxs-lookup"><span data-stu-id="14da3-1854">cvn</span></span> 
- <span data-ttu-id="14da3-1855">КВВ</span><span class="sxs-lookup"><span data-stu-id="14da3-1855">cvv</span></span> 
- <span data-ttu-id="14da3-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="14da3-1856">cvv2</span></span> 
- <span data-ttu-id="14da3-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1857">cód seguranca</span></span> 
- <span data-ttu-id="14da3-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1858">cód segurança</span></span> 
- <span data-ttu-id="14da3-1859">кóд.</span><span class="sxs-lookup"><span data-stu-id="14da3-1859">cód.</span></span> <span data-ttu-id="14da3-1860">сегуранка</span><span class="sxs-lookup"><span data-stu-id="14da3-1860">seguranca</span></span> 
- <span data-ttu-id="14da3-1861">кóд.</span><span class="sxs-lookup"><span data-stu-id="14da3-1861">cód.</span></span> <span data-ttu-id="14da3-1862">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="14da3-1862">segurança</span></span> 
- <span data-ttu-id="14da3-1863">кóдиго</span><span class="sxs-lookup"><span data-stu-id="14da3-1863">código</span></span> 
- <span data-ttu-id="14da3-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="14da3-1864">código de seguranca</span></span> 
- <span data-ttu-id="14da3-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="14da3-1865">código de segurança</span></span> 
- <span data-ttu-id="14da3-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="14da3-1866">de kaart controle</span></span> 
- <span data-ttu-id="14da3-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="14da3-1867">geeft nr uit</span></span> 
- <span data-ttu-id="14da3-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="14da3-1868">issue no</span></span> 
- <span data-ttu-id="14da3-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="14da3-1869">issue number</span></span> 
- <span data-ttu-id="14da3-1870">каартидентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="14da3-1871">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="14da3-1872">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="14da3-1873">квестиеаантал</span><span class="sxs-lookup"><span data-stu-id="14da3-1873">kwestieaantal</span></span> 
- <span data-ttu-id="14da3-1874">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1874">no.</span></span> <span data-ttu-id="14da3-1875">делл'едизионе</span><span class="sxs-lookup"><span data-stu-id="14da3-1875">dell'edizione</span></span> 
- <span data-ttu-id="14da3-1876">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-1876">no.</span></span> <span data-ttu-id="14da3-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="14da3-1877">di sicurezza</span></span> 
- <span data-ttu-id="14da3-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="14da3-1878">numero de securite</span></span> 
- <span data-ttu-id="14da3-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="14da3-1879">numero de verificacao</span></span> 
- <span data-ttu-id="14da3-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="14da3-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="14da3-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="14da3-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="14da3-1882">счеда</span><span class="sxs-lookup"><span data-stu-id="14da3-1882">scheda</span></span> 
- <span data-ttu-id="14da3-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="14da3-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="14da3-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="14da3-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="14da3-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="14da3-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="14da3-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="14da3-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="14da3-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="14da3-1887">número de verificação</span></span> 
- <span data-ttu-id="14da3-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="14da3-1888">perno il blocco</span></span> 
- <span data-ttu-id="14da3-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="14da3-1889">pin block</span></span> 
- <span data-ttu-id="14da3-1890">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="14da3-1890">prufziffer</span></span> 
- <span data-ttu-id="14da3-1891">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="14da3-1891">prüfziffer</span></span> 
- <span data-ttu-id="14da3-1892">security code</span><span class="sxs-lookup"><span data-stu-id="14da3-1892">security code</span></span> 
- <span data-ttu-id="14da3-1893">security no</span><span class="sxs-lookup"><span data-stu-id="14da3-1893">security no</span></span> 
- <span data-ttu-id="14da3-1894">security number</span><span class="sxs-lookup"><span data-stu-id="14da3-1894">security number</span></span> 
- <span data-ttu-id="14da3-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="14da3-1895">sicherheits kode</span></span> 
- <span data-ttu-id="14da3-1896">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="14da3-1896">sicherheitscode</span></span> 
- <span data-ttu-id="14da3-1897">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="14da3-1898">спелдблок</span><span class="sxs-lookup"><span data-stu-id="14da3-1898">speldblok</span></span> 
- <span data-ttu-id="14da3-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="14da3-1899">veiligheid nr</span></span> 
- <span data-ttu-id="14da3-1900">веилигхеидсаантал</span><span class="sxs-lookup"><span data-stu-id="14da3-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="14da3-1901">веилигхеидскоде</span><span class="sxs-lookup"><span data-stu-id="14da3-1901">veiligheidscode</span></span> 
- <span data-ttu-id="14da3-1902">веилигхеидснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="14da3-1903">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1903">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="14da3-1904">Кэйворд_кард_експиратион_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="14da3-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="14da3-1905">аблауф</span><span class="sxs-lookup"><span data-stu-id="14da3-1905">ablauf</span></span> 
- <span data-ttu-id="14da3-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="14da3-1906">data de expiracao</span></span> 
- <span data-ttu-id="14da3-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="14da3-1907">data de expiração</span></span> 
- <span data-ttu-id="14da3-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="14da3-1908">data del exp</span></span> 
- <span data-ttu-id="14da3-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="14da3-1909">data di exp</span></span> 
- <span data-ttu-id="14da3-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="14da3-1910">data di scadenza</span></span> 
- <span data-ttu-id="14da3-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="14da3-1911">data em que expira</span></span> 
- <span data-ttu-id="14da3-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="14da3-1912">data scad</span></span> 
- <span data-ttu-id="14da3-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="14da3-1913">data scadenza</span></span> 
- <span data-ttu-id="14da3-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="14da3-1914">date de validité</span></span> 
- <span data-ttu-id="14da3-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="14da3-1915">datum afloop</span></span> 
- <span data-ttu-id="14da3-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="14da3-1916">datum van exp</span></span> 
- <span data-ttu-id="14da3-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="14da3-1917">de afloop</span></span> 
- <span data-ttu-id="14da3-1918">еспира</span><span class="sxs-lookup"><span data-stu-id="14da3-1918">espira</span></span> 
- <span data-ttu-id="14da3-1919">еспира</span><span class="sxs-lookup"><span data-stu-id="14da3-1919">espira</span></span> 
- <span data-ttu-id="14da3-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="14da3-1920">exp date</span></span> 
- <span data-ttu-id="14da3-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="14da3-1921">exp datum</span></span> 
- <span data-ttu-id="14da3-1922">срока действия</span><span class="sxs-lookup"><span data-stu-id="14da3-1922">expiration</span></span> 
- <span data-ttu-id="14da3-1923">истекает</span><span class="sxs-lookup"><span data-stu-id="14da3-1923">expire</span></span> 
- <span data-ttu-id="14da3-1924">истекает</span><span class="sxs-lookup"><span data-stu-id="14da3-1924">expires</span></span> 
- <span data-ttu-id="14da3-1925">окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="14da3-1925">expiry</span></span> 
- <span data-ttu-id="14da3-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="14da3-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="14da3-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="14da3-1927">fecha de venc</span></span> 
- <span data-ttu-id="14da3-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="14da3-1928">gultig bis</span></span> 
- <span data-ttu-id="14da3-1929">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="14da3-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="14da3-1930">gültig bis</span></span> 
- <span data-ttu-id="14da3-1931">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="14da3-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="14da3-1932">la scadenza</span></span> 
- <span data-ttu-id="14da3-1933">скаденза</span><span class="sxs-lookup"><span data-stu-id="14da3-1933">scadenza</span></span> 
- <span data-ttu-id="14da3-1934">валабле</span><span class="sxs-lookup"><span data-stu-id="14da3-1934">valable</span></span> 
- <span data-ttu-id="14da3-1935">валидаде</span><span class="sxs-lookup"><span data-stu-id="14da3-1935">validade</span></span> 
- <span data-ttu-id="14da3-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="14da3-1936">valido hasta</span></span> 
- <span data-ttu-id="14da3-1937">Валор</span><span class="sxs-lookup"><span data-stu-id="14da3-1937">valor</span></span> 
- <span data-ttu-id="14da3-1938">Венк</span><span class="sxs-lookup"><span data-stu-id="14da3-1938">venc</span></span> 
- <span data-ttu-id="14da3-1939">венЦименто</span><span class="sxs-lookup"><span data-stu-id="14da3-1939">vencimento</span></span> 
- <span data-ttu-id="14da3-1940">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="14da3-1940">vencimiento</span></span> 
- <span data-ttu-id="14da3-1941">верлупт</span><span class="sxs-lookup"><span data-stu-id="14da3-1941">verloopt</span></span> 
- <span data-ttu-id="14da3-1942">вервалдаг</span><span class="sxs-lookup"><span data-stu-id="14da3-1942">vervaldag</span></span> 
- <span data-ttu-id="14da3-1943">вервалдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-1943">vervaldatum</span></span> 
- <span data-ttu-id="14da3-1944">ВТО</span><span class="sxs-lookup"><span data-stu-id="14da3-1944">vto</span></span> 
- <span data-ttu-id="14da3-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="14da3-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="14da3-1946">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="14da3-1946">EU Driver's License Number</span></span>

<span data-ttu-id="14da3-1947">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="14da3-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="14da3-1948">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="14da3-1948">EU National Identification Number</span></span>

<span data-ttu-id="14da3-1949">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационного номера ЕС](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="14da3-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="14da3-1950">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="14da3-1950">EU Passport Number</span></span>

<span data-ttu-id="14da3-1951">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="14da3-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="14da3-1952">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="14da3-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="14da3-1953">Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="14da3-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="14da3-1954">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="14da3-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="14da3-1955">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогового кода ЕС](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="14da3-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="14da3-1956">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="14da3-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1957">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1957">Format</span></span>

<span data-ttu-id="14da3-1958">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="14da3-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1959">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1959">Pattern</span></span>

<span data-ttu-id="14da3-1960">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="14da3-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="14da3-1961">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="14da3-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="14da3-1962">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="14da3-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="14da3-1963">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="14da3-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="14da3-1964">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1965">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1965">Checksum</span></span>

<span data-ttu-id="14da3-1966">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1967">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1967">Definition</span></span>

<span data-ttu-id="14da3-1968">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1969">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1970">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="14da3-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="14da3-1971">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-1971">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-1972">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1972">Keywords</span></span>

- <span data-ttu-id="14da3-1973">Кэйворд_финниш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="14da3-1974">Сосиаалитурватуннус</span><span class="sxs-lookup"><span data-stu-id="14da3-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="14da3-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="14da3-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="14da3-1976">Персонбетеккнинг</span><span class="sxs-lookup"><span data-stu-id="14da3-1976">Personbeteckning</span></span>
- <span data-ttu-id="14da3-1977">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="14da3-1978">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="14da3-1978">Finland Passport Number</span></span>

<span data-ttu-id="14da3-1979">Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Режекс_финланд_пасспорт_нумбер находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-1980">находится ключевое слово из Keyword_finland_passport_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="14da3-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="14da3-1981"></span></span>
<span data-ttu-id="14da3-1982">Ключевые слова Кэйворд_финланд_пасспорт_нумбер Passport Пасси</span><span class="sxs-lookup"><span data-stu-id="14da3-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="14da3-1983">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="14da3-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-1984">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-1984">Format</span></span>

<span data-ttu-id="14da3-1985">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-1986">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-1986">Pattern</span></span>

<span data-ttu-id="14da3-1987">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="14da3-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-1988">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-1988">Checksum</span></span>

<span data-ttu-id="14da3-1989">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-1990">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-1990">Definition</span></span>

<span data-ttu-id="14da3-1991">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-1992">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-1993">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="14da3-1994">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="14da3-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="14da3-1995">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-1995">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-1996">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-1996">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="14da3-1997">Кэйворд_френч_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="14da3-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="14da3-1998">drivers licence</span></span>
- <span data-ttu-id="14da3-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="14da3-1999">drivers license</span></span>
- <span data-ttu-id="14da3-2000">driving licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2000">driving licence</span></span>
- <span data-ttu-id="14da3-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="14da3-2001">driving license</span></span>
- <span data-ttu-id="14da3-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="14da3-2002">permis de conduire</span></span>
- <span data-ttu-id="14da3-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="14da3-2003">licence number</span></span>
- <span data-ttu-id="14da3-2004">license number</span><span class="sxs-lookup"><span data-stu-id="14da3-2004">license number</span></span>
- <span data-ttu-id="14da3-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-2005">licence numbers</span></span>
- <span data-ttu-id="14da3-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="14da3-2007">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="14da3-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2008">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2008">Format</span></span>

<span data-ttu-id="14da3-2009">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2010">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2010">Pattern</span></span>

<span data-ttu-id="14da3-2011">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2012">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2012">Checksum</span></span>

<span data-ttu-id="14da3-2013">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2014">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2014">Definition</span></span>

<span data-ttu-id="14da3-2015">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2016">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2017">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2017">Keywords</span></span>

<span data-ttu-id="14da3-2018">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="14da3-2019">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="14da3-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2020">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2020">Format</span></span>

<span data-ttu-id="14da3-2021">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="14da3-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2022">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2022">Pattern</span></span>

<span data-ttu-id="14da3-2023">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="14da3-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="14da3-2024">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2024">Two digits</span></span> 
- <span data-ttu-id="14da3-2025">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-2026">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2027">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2027">Checksum</span></span>

<span data-ttu-id="14da3-2028">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2029">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2029">Definition</span></span>

<span data-ttu-id="14da3-2030">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2031">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2032">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="14da3-2032">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2033">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2033">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="14da3-2034">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-2034">Keyword_passport</span></span>

- <span data-ttu-id="14da3-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2035">Passport Number</span></span>
- <span data-ttu-id="14da3-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="14da3-2036">Passport No</span></span>
- <span data-ttu-id="14da3-2037">Passport#</span><span class="sxs-lookup"><span data-stu-id="14da3-2037">Passport #</span></span>
- <span data-ttu-id="14da3-2038">Службу</span><span class="sxs-lookup"><span data-stu-id="14da3-2038">Passport#</span></span>
- <span data-ttu-id="14da3-2039">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="14da3-2039">PassportID</span></span>
- <span data-ttu-id="14da3-2040">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="14da3-2040">Passportno</span></span>
- <span data-ttu-id="14da3-2041">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2041">passportnumber</span></span>
- <span data-ttu-id="14da3-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="14da3-2042">パスポート</span></span>
- <span data-ttu-id="14da3-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2043">パスポート番号</span></span>
- <span data-ttu-id="14da3-2044">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="14da3-2044">パスポートのNum</span></span>
- <span data-ttu-id="14da3-2045">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="14da3-2045">パスポート ＃</span></span> 
- <span data-ttu-id="14da3-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="14da3-2046">Numéro de passeport</span></span>
- <span data-ttu-id="14da3-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="14da3-2047">Passeport n °</span></span>
- <span data-ttu-id="14da3-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="14da3-2048">Passeport Non</span></span>
- <span data-ttu-id="14da3-2049">Passeport#</span><span class="sxs-lookup"><span data-stu-id="14da3-2049">Passeport #</span></span>
- <span data-ttu-id="14da3-2050">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="14da3-2050">Passeport#</span></span>
- <span data-ttu-id="14da3-2051">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="14da3-2051">PasseportNon</span></span>
- <span data-ttu-id="14da3-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="14da3-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="14da3-2053">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="14da3-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2054">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2054">Format</span></span>

<span data-ttu-id="14da3-2055">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2056">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2056">Pattern</span></span>

<span data-ttu-id="14da3-2057">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="14da3-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="14da3-2058">13 цифр, за которыми следует пробел, за которым следуют две цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="14da3-2059">или</span><span class="sxs-lookup"><span data-stu-id="14da3-2059">or</span></span>
- <span data-ttu-id="14da3-2060">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2061">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2061">Checksum</span></span>

<span data-ttu-id="14da3-2062">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2063">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2063">Definition</span></span>

<span data-ttu-id="14da3-2064">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2065">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2066">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="14da3-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="14da3-2067">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2067">The checksum passes.</span></span>

<span data-ttu-id="14da3-2068">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2069">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2070">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="14da3-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="14da3-2071">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2071">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2072">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2072">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="14da3-2073">Кэйворд_фр_инси</span><span class="sxs-lookup"><span data-stu-id="14da3-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="14da3-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="14da3-2074">insee</span></span>
- <span data-ttu-id="14da3-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="14da3-2075">securité sociale</span></span>
- <span data-ttu-id="14da3-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="14da3-2076">securite sociale</span></span>
- <span data-ttu-id="14da3-2077">national id</span><span class="sxs-lookup"><span data-stu-id="14da3-2077">national id</span></span>
- <span data-ttu-id="14da3-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="14da3-2078">national identification</span></span>
- <span data-ttu-id="14da3-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="14da3-2079">numéro d'identité</span></span>
- <span data-ttu-id="14da3-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="14da3-2080">no d'identité</span></span>
- <span data-ttu-id="14da3-2081">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-2081">no.</span></span> <span data-ttu-id="14da3-2082">д'идентитé</span><span class="sxs-lookup"><span data-stu-id="14da3-2082">d'identité</span></span>
- <span data-ttu-id="14da3-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="14da3-2083">numero d'identite</span></span>
- <span data-ttu-id="14da3-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="14da3-2084">no d'identite</span></span>
- <span data-ttu-id="14da3-2085">Нет.</span><span class="sxs-lookup"><span data-stu-id="14da3-2085">no.</span></span> <span data-ttu-id="14da3-2086">д'идентите</span><span class="sxs-lookup"><span data-stu-id="14da3-2086">d'identite</span></span>
- <span data-ttu-id="14da3-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="14da3-2087">social security number</span></span>
- <span data-ttu-id="14da3-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="14da3-2088">social security code</span></span>
- <span data-ttu-id="14da3-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="14da3-2089">social insurance number</span></span>
- <span data-ttu-id="14da3-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="14da3-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="14da3-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="14da3-2091">d'identité nationale</span></span>
- <span data-ttu-id="14da3-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="14da3-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="14da3-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="14da3-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="14da3-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="14da3-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="14da3-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="14da3-2095">numéro de sécu</span></span>
- <span data-ttu-id="14da3-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="14da3-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="14da3-2097">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="14da3-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2098">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2098">Format</span></span>

<span data-ttu-id="14da3-2099">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="14da3-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2100">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2100">Pattern</span></span>

<span data-ttu-id="14da3-2101">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="14da3-2102">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="14da3-2102">A digit or letter</span></span> 
- <span data-ttu-id="14da3-2103">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2103">Two digits</span></span> 
- <span data-ttu-id="14da3-2104">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="14da3-2104">Six digits or letters</span></span> 
- <span data-ttu-id="14da3-2105">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="14da3-2105">A digit</span></span> 
- <span data-ttu-id="14da3-2106">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="14da3-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2107">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2107">Checksum</span></span>

<span data-ttu-id="14da3-2108">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2109">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2109">Definition</span></span>

<span data-ttu-id="14da3-2110">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2111">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2112">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="14da3-2113">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="14da3-2114">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="14da3-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="14da3-2115">найдено ключевое слово из Keyword_german_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="14da3-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="14da3-2116">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2116">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2117">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2117">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="14da3-2118">Кэйворд_жерман_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="14da3-2119">Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2119">Führerschein</span></span>
- <span data-ttu-id="14da3-2120">Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2120">Fuhrerschein</span></span>
- <span data-ttu-id="14da3-2121">Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2121">Fuehrerschein</span></span>
- <span data-ttu-id="14da3-2122">Фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="14da3-2123">Фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="14da3-2124">Фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="14da3-2125">Фüхрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="14da3-2125">Führerschein-</span></span> 
- <span data-ttu-id="14da3-2126">Фухрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="14da3-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="14da3-2127">Фуехрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="14da3-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="14da3-2128">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="14da3-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="14da3-2129">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="14da3-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="14da3-2130">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="14da3-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="14da3-2131">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="14da3-2132">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="14da3-2133">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="14da3-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="14da3-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="14da3-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="14da3-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="14da3-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="14da3-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="14da3-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="14da3-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="14da3-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="14da3-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="14da3-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="14da3-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="14da3-2140">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="14da3-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="14da3-2141">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="14da3-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="14da3-2142">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="14da3-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="14da3-2143">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="14da3-2144">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="14da3-2145">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="14da3-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="14da3-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="14da3-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="14da3-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="14da3-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="14da3-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="14da3-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="14da3-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="14da3-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="14da3-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="14da3-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="14da3-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="14da3-2152">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-2152">DL</span></span> 
- <span data-ttu-id="14da3-2153">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="14da3-2153">DLS</span></span>
- <span data-ttu-id="14da3-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-2154">Driv Lic</span></span> 
- <span data-ttu-id="14da3-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="14da3-2155">Driv Licen</span></span> 
- <span data-ttu-id="14da3-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="14da3-2156">Driv License</span></span>
- <span data-ttu-id="14da3-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2157">Driv Licenses</span></span> 
- <span data-ttu-id="14da3-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2158">Driv Licence</span></span> 
- <span data-ttu-id="14da3-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-2159">Driv Licences</span></span> 
- <span data-ttu-id="14da3-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-2160">Driv Lic</span></span> 
- <span data-ttu-id="14da3-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="14da3-2161">Driver Licen</span></span> 
- <span data-ttu-id="14da3-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="14da3-2162">Driver License</span></span> 
- <span data-ttu-id="14da3-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2163">Driver Licenses</span></span> 
- <span data-ttu-id="14da3-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2164">Driver Licence</span></span> 
- <span data-ttu-id="14da3-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-2165">Driver Licences</span></span> 
- <span data-ttu-id="14da3-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-2166">Drivers Lic</span></span> 
- <span data-ttu-id="14da3-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="14da3-2167">Drivers Licen</span></span> 
- <span data-ttu-id="14da3-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="14da3-2168">Drivers License</span></span> 
- <span data-ttu-id="14da3-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="14da3-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2170">Drivers Licence</span></span> 
- <span data-ttu-id="14da3-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-2171">Drivers Licences</span></span> 
- <span data-ttu-id="14da3-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-2172">Driver's Lic</span></span> 
- <span data-ttu-id="14da3-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="14da3-2173">Driver's Licen</span></span> 
- <span data-ttu-id="14da3-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="14da3-2174">Driver's License</span></span> 
- <span data-ttu-id="14da3-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="14da3-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2176">Driver's Licence</span></span> 
- <span data-ttu-id="14da3-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-2177">Driver's Licences</span></span> 
- <span data-ttu-id="14da3-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-2178">Driving Lic</span></span> 
- <span data-ttu-id="14da3-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="14da3-2179">Driving Licen</span></span> 
- <span data-ttu-id="14da3-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="14da3-2180">Driving License</span></span> 
- <span data-ttu-id="14da3-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2181">Driving Licenses</span></span> 
- <span data-ttu-id="14da3-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2182">Driving Licence</span></span> 
- <span data-ttu-id="14da3-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="14da3-2183">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="14da3-2184">Кэйворд_жерман_дриверс_лиценсе_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="14da3-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="14da3-2185">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="14da3-2186">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="14da3-2187">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="14da3-2188">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2188">No-Führerschein</span></span> 
- <span data-ttu-id="14da3-2189">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="14da3-2190">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="14da3-2191">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2191">N-Führerschein</span></span> 
- <span data-ttu-id="14da3-2192">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="14da3-2193">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="14da3-2194">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="14da3-2195">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="14da3-2196">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="14da3-2197">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2197">No-Führerschein</span></span> 
- <span data-ttu-id="14da3-2198">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="14da3-2199">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="14da3-2200">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2200">N-Führerschein</span></span> 
- <span data-ttu-id="14da3-2201">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="14da3-2202">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="14da3-2202">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="14da3-2203">Кэйворд_жерман_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="14da3-2204">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="14da3-2205">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="14da3-2205">ausstellungsort</span></span>
- <span data-ttu-id="14da3-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="14da3-2206">ausstellende behöde</span></span>
- <span data-ttu-id="14da3-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="14da3-2207">ausstellende behorde</span></span>
- <span data-ttu-id="14da3-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="14da3-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="14da3-2209">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="14da3-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2210">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2210">Format</span></span>

<span data-ttu-id="14da3-2211">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="14da3-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2212">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2212">Pattern</span></span>

<span data-ttu-id="14da3-2213">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="14da3-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="14da3-2214">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="14da3-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="14da3-2215">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2215">Three digits</span></span> 
- <span data-ttu-id="14da3-2216">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="14da3-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="14da3-2217">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="14da3-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2218">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2218">Checksum</span></span>

<span data-ttu-id="14da3-2219">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2220">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2220">Definition</span></span>

<span data-ttu-id="14da3-2221">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2222">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2223">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="14da3-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="14da3-2224">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2224">The checksum passes.</span></span>

<span data-ttu-id="14da3-2225">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2226">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2227">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="14da3-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="14da3-2228">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2228">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2229">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2229">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="14da3-2230">Кэйворд_жерман_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="14da3-2231">реисепасс</span><span class="sxs-lookup"><span data-stu-id="14da3-2231">reisepass</span></span>
- <span data-ttu-id="14da3-2232">реисепассе</span><span class="sxs-lookup"><span data-stu-id="14da3-2232">reisepasse</span></span>
- <span data-ttu-id="14da3-2233">реисепасснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2233">reisepassnummer</span></span>
- <span data-ttu-id="14da3-2234">службу</span><span class="sxs-lookup"><span data-stu-id="14da3-2234">passport</span></span>
- <span data-ttu-id="14da3-2235">паспорты</span><span class="sxs-lookup"><span data-stu-id="14da3-2235">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="14da3-2236">Кэйворд_жерман_пасспорт_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="14da3-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="14da3-2237">жебуртсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-2237">geburtsdatum</span></span>
- <span data-ttu-id="14da3-2238">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="14da3-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="14da3-2239">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="14da3-2239">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="14da3-2240">Кэйворд_жерман_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="14da3-2241">No — Реисепасс НР — Реисепасс</span><span class="sxs-lookup"><span data-stu-id="14da3-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="14da3-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="14da3-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="14da3-2243">Реисепасс — НР</span><span class="sxs-lookup"><span data-stu-id="14da3-2243">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="14da3-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="14da3-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="14da3-2245">бнатионалит. t</span><span class="sxs-lookup"><span data-stu-id="14da3-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="14da3-2246">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="14da3-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2247">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2247">Format</span></span>

<span data-ttu-id="14da3-2248">С 1 ноября 2010: девять букв и цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="14da3-2249">От 1 апреля 1987 до 31 октября 2010:10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2250">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2250">Pattern</span></span>

<span data-ttu-id="14da3-2251">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="14da3-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="14da3-2252">одна буква (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-2253">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2253">Eight digits</span></span>

<span data-ttu-id="14da3-2254">От 1 апреля 1987 до 31 октября 2010:</span><span class="sxs-lookup"><span data-stu-id="14da3-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="14da3-2255">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2256">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2256">Checksum</span></span>

<span data-ttu-id="14da3-2257">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2258">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2258">Definition</span></span>

<span data-ttu-id="14da3-2259">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2260">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2261">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="14da3-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2262">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2262">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="14da3-2263">Кэйворд_жермани_ид_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="14da3-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="14da3-2264">Identity Card</span></span>
- <span data-ttu-id="14da3-2265">ID</span><span class="sxs-lookup"><span data-stu-id="14da3-2265">ID</span></span>
- <span data-ttu-id="14da3-2266">Процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-2266">Identification</span></span>
- <span data-ttu-id="14da3-2267">Персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="14da3-2267">Personalausweis</span></span>
- <span data-ttu-id="14da3-2268">Идентифизиерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="14da3-2269">Аусвеис</span><span class="sxs-lookup"><span data-stu-id="14da3-2269">Ausweis</span></span>
- <span data-ttu-id="14da3-2270">Идентификатион</span><span class="sxs-lookup"><span data-stu-id="14da3-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="14da3-2271">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="14da3-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2272">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2272">Format</span></span>

<span data-ttu-id="14da3-2273">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="14da3-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2274">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2274">Pattern</span></span>

<span data-ttu-id="14da3-2275">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="14da3-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="14da3-2276">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="14da3-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="14da3-2277">тире;</span><span class="sxs-lookup"><span data-stu-id="14da3-2277">A dash</span></span> 
- <span data-ttu-id="14da3-2278">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2278">Six digits</span></span>

<span data-ttu-id="14da3-2279">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="14da3-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="14da3-2280">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="14da3-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="14da3-2281">тире;</span><span class="sxs-lookup"><span data-stu-id="14da3-2281">A dash</span></span> 
- <span data-ttu-id="14da3-2282">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2283">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2283">Checksum</span></span>

<span data-ttu-id="14da3-2284">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2285">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2285">Definition</span></span>

<span data-ttu-id="14da3-2286">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2287">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2288">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="14da3-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2289">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2289">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="14da3-2290">Кэйворд_грице_ид_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="14da3-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="14da3-2291">Greek identity Card</span></span>
- <span data-ttu-id="14da3-2292">Таутотита</span><span class="sxs-lookup"><span data-stu-id="14da3-2292">Tautotita</span></span>
- <span data-ttu-id="14da3-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="14da3-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="14da3-2294">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="14da3-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="14da3-2295">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="14da3-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2296">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2296">Format</span></span>

<span data-ttu-id="14da3-2297">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="14da3-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2298">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2298">Pattern</span></span>

<span data-ttu-id="14da3-2299">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="14da3-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="14da3-2300">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-2301">шесть цифр; </span><span class="sxs-lookup"><span data-stu-id="14da3-2301">Six digits</span></span> 
- <span data-ttu-id="14da3-2302">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="14da3-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2303">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2303">Checksum</span></span>

<span data-ttu-id="14da3-2304">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2305">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2305">Definition</span></span>

<span data-ttu-id="14da3-2306">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2307">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2308">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="14da3-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="14da3-2309">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2309">The checksum passes.</span></span>

<span data-ttu-id="14da3-2310">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2311">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2312">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2312">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2313">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2313">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="14da3-2314">Кэйворд_хонг_конг_ид_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="14da3-2315">идентификационная карточка Гонконг</span><span class="sxs-lookup"><span data-stu-id="14da3-2315">hong kong identity card</span></span>
- <span data-ttu-id="14da3-2316">ХКИДК</span><span class="sxs-lookup"><span data-stu-id="14da3-2316">HKIDC</span></span>
- <span data-ttu-id="14da3-2317">id card</span><span class="sxs-lookup"><span data-stu-id="14da3-2317">id card</span></span>
- <span data-ttu-id="14da3-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="14da3-2318">identity card</span></span>
- <span data-ttu-id="14da3-2319">идентификационная карточка HK</span><span class="sxs-lookup"><span data-stu-id="14da3-2319">hk identity card</span></span>
- <span data-ttu-id="14da3-2320">Идентификатор Гонконг</span><span class="sxs-lookup"><span data-stu-id="14da3-2320">hong kong id</span></span>
- <span data-ttu-id="14da3-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2321">香港身份證</span></span>
- <span data-ttu-id="14da3-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="14da3-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2323">身份證</span></span>
- <span data-ttu-id="14da3-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2324">身份証</span></span>
- <span data-ttu-id="14da3-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2325">身分證</span></span>
- <span data-ttu-id="14da3-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2326">身分証</span></span>
- <span data-ttu-id="14da3-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2327">香港身份証</span></span>
- <span data-ttu-id="14da3-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2328">香港身分證</span></span>
- <span data-ttu-id="14da3-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2329">香港身分証</span></span>
- <span data-ttu-id="14da3-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2330">香港身份證</span></span>
- <span data-ttu-id="14da3-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2331">香港居民身份證</span></span>
- <span data-ttu-id="14da3-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2332">香港居民身份証</span></span>
- <span data-ttu-id="14da3-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2333">香港居民身分證</span></span>
- <span data-ttu-id="14da3-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2334">香港居民身分証</span></span>
- <span data-ttu-id="14da3-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="14da3-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="14da3-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="14da3-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="14da3-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="14da3-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="14da3-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="14da3-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="14da3-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="14da3-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="14da3-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="14da3-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="14da3-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="14da3-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="14da3-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="14da3-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="14da3-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="14da3-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="14da3-2351">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="14da3-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2352">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2352">Format</span></span>

<span data-ttu-id="14da3-2353">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2354">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2354">Pattern</span></span>

<span data-ttu-id="14da3-2355">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2355">10 letters or digits:</span></span>
- <span data-ttu-id="14da3-2356">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-2357">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2357">Four digits</span></span> 
- <span data-ttu-id="14da3-2358">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="14da3-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2359">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2359">Checksum</span></span>

<span data-ttu-id="14da3-2360">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2361">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2361">Definition</span></span>

<span data-ttu-id="14da3-2362">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2363">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2364">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="14da3-2365">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2365">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2366">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2366">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="14da3-2367">Кэйворд_индиа_перманент_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="14da3-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="14da3-2369">ПАНОРАМИРОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14da3-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="14da3-2370">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="14da3-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2371">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2371">Format</span></span>

<span data-ttu-id="14da3-2372">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="14da3-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2373">Pattern</span></span>

<span data-ttu-id="14da3-2374">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2374">12 digits:</span></span>
- <span data-ttu-id="14da3-2375">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-2375">Four digits</span></span> 
- <span data-ttu-id="14da3-2376">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="14da3-2376">An optional space or dash</span></span> 
- <span data-ttu-id="14da3-2377">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-2377">Four digits</span></span> 
- <span data-ttu-id="14da3-2378">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="14da3-2378">An optional space or dash</span></span> 
- <span data-ttu-id="14da3-2379">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="14da3-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2380">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2380">Checksum</span></span>

<span data-ttu-id="14da3-2381">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2382">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2382">Definition</span></span>

<span data-ttu-id="14da3-2383">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-2384">находится ключевое слово из Keyword_india_aadhar;</span><span class="sxs-lookup"><span data-stu-id="14da3-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="14da3-2385">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2385">The checksum passes.</span></span>
<span data-ttu-id="14da3-2386">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-2387">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2387">The checksum passes.</span></span>
<!-- India Unique Identification (Aadhaar) number -->
<span data-ttu-id="14da3-2388"><Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="14da3-2388"></span></span>

### <a name="keywords"></a><span data-ttu-id="14da3-2389">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2389">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="14da3-2390">Кэйворд_индиа_аадхар</span><span class="sxs-lookup"><span data-stu-id="14da3-2390">Keyword_india_aadhar</span></span>
- <span data-ttu-id="14da3-2391">Аадхар</span><span class="sxs-lookup"><span data-stu-id="14da3-2391">Aadhar</span></span>
- <span data-ttu-id="14da3-2392">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="14da3-2392">Aadhaar</span></span>
- <span data-ttu-id="14da3-2393">UID</span><span class="sxs-lookup"><span data-stu-id="14da3-2393">UID</span></span>
- <span data-ttu-id="14da3-2394">आधार</span><span class="sxs-lookup"><span data-stu-id="14da3-2394">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="14da3-2395">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="14da3-2395">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2396">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2396">Format</span></span>

<span data-ttu-id="14da3-2397">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="14da3-2397">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2398">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2398">Pattern</span></span>

<span data-ttu-id="14da3-2399">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2399">16 digits:</span></span>
- <span data-ttu-id="14da3-2400">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="14da3-2400">Two-digit province code</span></span> 
- <span data-ttu-id="14da3-2401">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="14da3-2401">A period (optional)</span></span> 
- <span data-ttu-id="14da3-2402">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="14da3-2402">Two-digit regency or city code</span></span> 
- <span data-ttu-id="14da3-2403">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="14da3-2403">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="14da3-2404">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="14da3-2404">A period (optional)</span></span> 
- <span data-ttu-id="14da3-2405">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="14da3-2405">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="14da3-2406">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="14da3-2406">A period (optional)</span></span> 
- <span data-ttu-id="14da3-2407">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-2407">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2408">Checksum</span></span>

<span data-ttu-id="14da3-2409">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2409">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2410">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2410">Definition</span></span>

<span data-ttu-id="14da3-2411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2412">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2412">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2413">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="14da3-2413">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="14da3-2414">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2415">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2415">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2416">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2416">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="14da3-2417">Кэйворд_индонесиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-2417">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="14da3-2418">KTP</span><span class="sxs-lookup"><span data-stu-id="14da3-2418">KTP</span></span>
- <span data-ttu-id="14da3-2419">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="14da3-2419">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="14da3-2420">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="14da3-2420">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="14da3-2421">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="14da3-2421">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2422">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2422">Format</span></span>

<span data-ttu-id="14da3-2423">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="14da3-2423">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2424">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2424">Pattern</span></span>

<span data-ttu-id="14da3-2425">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="14da3-2425">Pattern must include all of the following:</span></span>

- <span data-ttu-id="14da3-2426">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="14da3-2426">Two-letter country code</span></span>
- <span data-ttu-id="14da3-2427">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="14da3-2427">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="14da3-2428">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="14da3-2428">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="14da3-2429">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2429">1-3 letters or digits</span></span>

<span data-ttu-id="14da3-p135">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="14da3-p135">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="14da3-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="14da3-2432">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2433">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2433">Checksum</span></span>

<span data-ttu-id="14da3-2434">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2434">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2435">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2435">Definition</span></span>

<span data-ttu-id="14da3-2436">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2436">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2437">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2437">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2438">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2438">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2439">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2439">Keywords</span></span>

<span data-ttu-id="14da3-2440">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2440">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="14da3-2441">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="14da3-2441">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2442">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2442">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="14da3-2443">IPv4</span><span class="sxs-lookup"><span data-stu-id="14da3-2443">IPv4:</span></span>
<span data-ttu-id="14da3-2444">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="14da3-2444">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="14da3-2445">Поддерживающ</span><span class="sxs-lookup"><span data-stu-id="14da3-2445">IPv6:</span></span>
<span data-ttu-id="14da3-2446"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="14da3-2446">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2447">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2447">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2448">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2448">Checksum</span></span>

<span data-ttu-id="14da3-2449">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2449">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2450">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2450">Definition</span></span>

<span data-ttu-id="14da3-2451">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2451">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2452">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2452">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2453">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="14da3-2453">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="14da3-2454">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2454">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2455">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2455">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2456">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="14da3-2456">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="14da3-2457">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2457">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2458">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2458">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2459">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="14da3-2459">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2460">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="14da3-2461">Кэйворд_ипаддресс</span><span class="sxs-lookup"><span data-stu-id="14da3-2461">Keyword_ipaddress</span></span>

- <span data-ttu-id="14da3-2462">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-2462">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="14da3-2463">ip address</span><span class="sxs-lookup"><span data-stu-id="14da3-2463">ip address</span></span> 
- <span data-ttu-id="14da3-2464">ip addresses</span><span class="sxs-lookup"><span data-stu-id="14da3-2464">ip addresses</span></span>
- <span data-ttu-id="14da3-2465">internet protocol</span><span class="sxs-lookup"><span data-stu-id="14da3-2465">internet protocol</span></span>
- <span data-ttu-id="14da3-2466">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="14da3-2466">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="14da3-2467">Международная классификация Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="14da3-2467">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2468">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2468">Format</span></span>

<span data-ttu-id="14da3-2469">Dictionary</span><span class="sxs-lookup"><span data-stu-id="14da3-2469">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2470">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2470">Pattern</span></span>

<span data-ttu-id="14da3-2471">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="14da3-2471">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2472">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2472">Checksum</span></span>

<span data-ttu-id="14da3-2473">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2473">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2474">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2474">Definition</span></span>

<span data-ttu-id="14da3-2475">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2475">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2476">Найдено ключевое слово из Dictionary_icd_10_cm.</span><span class="sxs-lookup"><span data-stu-id="14da3-2476">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="14da3-2477">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2477">Keywords</span></span>

<span data-ttu-id="14da3-2478">Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятой редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="14da3-2478">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="14da3-2479">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="14da3-2479">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="14da3-2480">Международная классификация Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="14da3-2480">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2481">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2481">Format</span></span>

<span data-ttu-id="14da3-2482">Dictionary</span><span class="sxs-lookup"><span data-stu-id="14da3-2482">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2483">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2483">Pattern</span></span>

<span data-ttu-id="14da3-2484">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="14da3-2484">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2485">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2485">Checksum</span></span>

<span data-ttu-id="14da3-2486">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2486">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2487">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2487">Definition</span></span>

<span data-ttu-id="14da3-2488">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2488">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2489">Найдено ключевое слово из Dictionary_icd_9_cm.</span><span class="sxs-lookup"><span data-stu-id="14da3-2489">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2490">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2490">Keywords</span></span>

<span data-ttu-id="14da3-2491">Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятой редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="14da3-2491">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="14da3-2492">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="14da3-2492">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="14da3-2493">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="14da3-2493">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2494">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2494">Format</span></span>

<span data-ttu-id="14da3-2495">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="14da3-2495">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="14da3-2496">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="14da3-2496">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="14da3-2497">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="14da3-2497">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="14da3-2498">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="14da3-2498">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2499">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2499">Pattern</span></span>

<span data-ttu-id="14da3-2500">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="14da3-2500">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="14da3-2501">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-2501">Seven digits</span></span> 
- <span data-ttu-id="14da3-2502">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="14da3-2502">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="14da3-2503">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="14da3-2503">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="14da3-2504">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-2504">Seven digits</span></span> 
- <span data-ttu-id="14da3-2505">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="14da3-2505">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="14da3-2506">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="14da3-2506">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2507">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2507">Checksum</span></span>

<span data-ttu-id="14da3-2508">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2508">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2509">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2509">Definition</span></span>

<span data-ttu-id="14da3-2510">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2511">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2511">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2512">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-2512">One of the following is true:</span></span>
    - <span data-ttu-id="14da3-2513">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="14da3-2513">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="14da3-2514">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-2514">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="14da3-2515">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2515">The checksum passes.</span></span>

<span data-ttu-id="14da3-2516">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2516">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2517">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2517">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2518">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2518">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2519">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2519">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="14da3-2520">Кэйворд_иреланд_ппс</span><span class="sxs-lookup"><span data-stu-id="14da3-2520">Keyword_ireland_pps</span></span>

- <span data-ttu-id="14da3-2521">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2521">Personal Public Service Number</span></span> 
- <span data-ttu-id="14da3-2522">PPS Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2522">PPS Number</span></span> 
- <span data-ttu-id="14da3-2523">PPS Num</span><span class="sxs-lookup"><span data-stu-id="14da3-2523">PPS Num</span></span> 
- <span data-ttu-id="14da3-2524">PPS No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2524">PPS No.</span></span> 
- <span data-ttu-id="14da3-2525">PPS #</span><span class="sxs-lookup"><span data-stu-id="14da3-2525">PPS #</span></span> 
- <span data-ttu-id="14da3-2526">PPS</span><span class="sxs-lookup"><span data-stu-id="14da3-2526">PPS#</span></span> 
- <span data-ttu-id="14da3-2527">ППСН</span><span class="sxs-lookup"><span data-stu-id="14da3-2527">PPSN</span></span> 
- <span data-ttu-id="14da3-2528">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="14da3-2528">Public Services Card</span></span> 
- <span data-ttu-id="14da3-2529">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="14da3-2529">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="14da3-2530">Уимх.</span><span class="sxs-lookup"><span data-stu-id="14da3-2530">Uimh.</span></span> <span data-ttu-id="14da3-2531">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="14da3-2531">PSP</span></span> 
- <span data-ttu-id="14da3-2532">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="14da3-2532">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="14da3-2533">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="14da3-2533">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2534">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2534">Format</span></span>

<span data-ttu-id="14da3-2535">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2535">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2536">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2536">Pattern</span></span>

<span data-ttu-id="14da3-2537">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="14da3-2537">Formatted:</span></span>
- <span data-ttu-id="14da3-2538">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2538">Two digits</span></span> 
- <span data-ttu-id="14da3-2539">Тире</span><span class="sxs-lookup"><span data-stu-id="14da3-2539">A dash</span></span> 
- <span data-ttu-id="14da3-2540">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2540">Three digits</span></span> 
- <span data-ttu-id="14da3-2541">Тире</span><span class="sxs-lookup"><span data-stu-id="14da3-2541">A dash</span></span> 
- <span data-ttu-id="14da3-2542">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-2542">Eight digits</span></span>

<span data-ttu-id="14da3-2543">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="14da3-2543">Unformatted:</span></span>
- <span data-ttu-id="14da3-2544">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2544">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2545">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2545">Checksum</span></span>

<span data-ttu-id="14da3-2546">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2546">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2547">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2547">Definition</span></span>

<span data-ttu-id="14da3-2548">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2548">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2549">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2549">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2550">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-2550">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2551">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2551">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="14da3-2552">Кэйворд_исраел_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2552">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="14da3-2553">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2553">Bank Account Number</span></span> 
- <span data-ttu-id="14da3-2554">Bank Account</span><span class="sxs-lookup"><span data-stu-id="14da3-2554">Bank Account</span></span> 
- <span data-ttu-id="14da3-2555">Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2555">Account Number</span></span> 
- <span data-ttu-id="14da3-2556">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="14da3-2556">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="14da3-2557">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="14da3-2557">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2558">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2558">Format</span></span>

<span data-ttu-id="14da3-2559">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2559">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2560">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2560">Pattern</span></span>

<span data-ttu-id="14da3-2561">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2561">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2562">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2562">Checksum</span></span>

<span data-ttu-id="14da3-2563">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2563">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2564">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2564">Definition</span></span>

<span data-ttu-id="14da3-2565">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2565">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2566">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2566">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2567">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="14da3-2567">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="14da3-2568">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2568">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2569">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2569">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="14da3-2570">Кэйворд_исраел_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-2570">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="14da3-2571">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="14da3-2571">מספר זהות</span></span> 
- <span data-ttu-id="14da3-2572">National ID Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2572">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="14da3-2573">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="14da3-2573">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2574">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2574">Format</span></span>

<span data-ttu-id="14da3-2575">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2575">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2576">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2576">Pattern</span></span>

- <span data-ttu-id="14da3-2577">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2577">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="14da3-2578">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-2578">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-2579">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-2579">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-2580">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="14da3-2580">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="14da3-2581">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-2581">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2582">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2582">Checksum</span></span>

<span data-ttu-id="14da3-2583">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2583">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2584">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2584">Definition</span></span>

<span data-ttu-id="14da3-2585">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2585">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2586">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2586">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2587">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-2587">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2588">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2588">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="14da3-2589">Кэйворд_итали_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2589">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="14da3-2590">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="14da3-2590">numero di patente di guida</span></span> 
- <span data-ttu-id="14da3-2591">patente di guida</span><span class="sxs-lookup"><span data-stu-id="14da3-2591">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="14da3-2592">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="14da3-2592">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2593">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2593">Format</span></span>

<span data-ttu-id="14da3-2594">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2594">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2595">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2595">Pattern</span></span>

<span data-ttu-id="14da3-2596">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="14da3-2596">Bank account number:</span></span>
- <span data-ttu-id="14da3-2597">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2597">Seven or eight digits</span></span>
- <span data-ttu-id="14da3-2598">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="14da3-2598">Bank account branch code:</span></span>
- <span data-ttu-id="14da3-2599">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2599">Four digits</span></span> 
- <span data-ttu-id="14da3-2600">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14da3-2600">A space or dash (optional)</span></span> 
- <span data-ttu-id="14da3-2601">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2601">Three digits</span></span>

<span data-ttu-id="14da3-2602">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2602">Checksum</span></span>

<span data-ttu-id="14da3-2603">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2603">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2604">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2604">Definition</span></span>

<span data-ttu-id="14da3-2605">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2605">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2606">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-2606">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2607">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="14da3-2607">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="14da3-2608">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-2608">One of the following is true:</span></span>
- <span data-ttu-id="14da3-2609">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2609">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2610">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="14da3-2610">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="14da3-2611">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2611">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2612">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2612">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2613">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="14da3-2613">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2614">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2614">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="14da3-2615">Кэйворд_жп_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="14da3-2615">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="14da3-2616">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2616">Checking Account Number</span></span> 
- <span data-ttu-id="14da3-2617">Checking Account</span><span class="sxs-lookup"><span data-stu-id="14da3-2617">Checking Account</span></span> 
- <span data-ttu-id="14da3-2618">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-2618">Checking Account #</span></span> 
- <span data-ttu-id="14da3-2619">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2619">Checking Acct Number</span></span> 
- <span data-ttu-id="14da3-2620">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-2620">Checking Acct #</span></span> 
- <span data-ttu-id="14da3-2621">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2621">Checking Acct No.</span></span> 
- <span data-ttu-id="14da3-2622">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2622">Checking Account No.</span></span> 
- <span data-ttu-id="14da3-2623">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2623">Bank Account Number</span></span> 
- <span data-ttu-id="14da3-2624">Bank Account</span><span class="sxs-lookup"><span data-stu-id="14da3-2624">Bank Account</span></span> 
- <span data-ttu-id="14da3-2625">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-2625">Bank Account #</span></span> 
- <span data-ttu-id="14da3-2626">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2626">Bank Acct Number</span></span> 
- <span data-ttu-id="14da3-2627">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-2627">Bank Acct #</span></span> 
- <span data-ttu-id="14da3-2628">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2628">Bank Acct No.</span></span> 
- <span data-ttu-id="14da3-2629">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2629">Bank Account No.</span></span> 
- <span data-ttu-id="14da3-2630">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2630">Savings Account Number</span></span> 
- <span data-ttu-id="14da3-2631">Savings Account</span><span class="sxs-lookup"><span data-stu-id="14da3-2631">Savings Account</span></span> 
- <span data-ttu-id="14da3-2632">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-2632">Savings Account #</span></span> 
- <span data-ttu-id="14da3-2633">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2633">Savings Acct Number</span></span> 
- <span data-ttu-id="14da3-2634">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-2634">Savings Acct #</span></span> 
- <span data-ttu-id="14da3-2635">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2635">Savings Acct No.</span></span> 
- <span data-ttu-id="14da3-2636">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2636">Savings Account No.</span></span> 
- <span data-ttu-id="14da3-2637">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2637">Debit Account Number</span></span> 
- <span data-ttu-id="14da3-2638">Debit Account</span><span class="sxs-lookup"><span data-stu-id="14da3-2638">Debit Account</span></span> 
- <span data-ttu-id="14da3-2639">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-2639">Debit Account #</span></span> 
- <span data-ttu-id="14da3-2640">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2640">Debit Acct Number</span></span> 
- <span data-ttu-id="14da3-2641">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-2641">Debit Acct #</span></span> 
- <span data-ttu-id="14da3-2642">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2642">Debit Acct No.</span></span> 
- <span data-ttu-id="14da3-2643">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2643">Debit Account No.</span></span> 
- <span data-ttu-id="14da3-2644">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="14da3-2644">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="14da3-2645">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="14da3-2645">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="14da3-2646">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="14da3-2646">＃勘定の確認</span></span> 
- <span data-ttu-id="14da3-2647">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="14da3-2647">勘定番号の確認</span></span> 
- <span data-ttu-id="14da3-2648">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="14da3-2648">口座番号の確認</span></span> 
- <span data-ttu-id="14da3-2649">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2649">銀行口座番号</span></span> 
- <span data-ttu-id="14da3-2650">銀行口座</span><span class="sxs-lookup"><span data-stu-id="14da3-2650">銀行口座</span></span> 
- <span data-ttu-id="14da3-2651">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="14da3-2651">銀行口座＃</span></span> 
- <span data-ttu-id="14da3-2652">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2652">銀行の勘定番号</span></span> 
- <span data-ttu-id="14da3-2653">銀行のаккт #</span><span class="sxs-lookup"><span data-stu-id="14da3-2653">銀行のacct＃</span></span> 
- <span data-ttu-id="14da3-2654">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="14da3-2654">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="14da3-2655">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2655">銀行口座番号</span></span>
- <span data-ttu-id="14da3-2656">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2656">普通預金口座番号</span></span> 
- <span data-ttu-id="14da3-2657">預金口座</span><span class="sxs-lookup"><span data-stu-id="14da3-2657">預金口座</span></span> 
- <span data-ttu-id="14da3-2658">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="14da3-2658">貯蓄口座＃</span></span> 
- <span data-ttu-id="14da3-2659">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="14da3-2659">貯蓄勘定の数</span></span> 
- <span data-ttu-id="14da3-2660">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="14da3-2660">貯蓄勘定＃</span></span> 
- <span data-ttu-id="14da3-2661">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2661">貯蓄勘定番号</span></span> 
- <span data-ttu-id="14da3-2662">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2662">普通預金口座番号</span></span> 
- <span data-ttu-id="14da3-2663">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2663">引き落とし口座番号</span></span> 
- <span data-ttu-id="14da3-2664">口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2664">口座番号</span></span> 
- <span data-ttu-id="14da3-2665">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="14da3-2665">口座番号＃</span></span> 
- <span data-ttu-id="14da3-2666">デビットのаккт番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2666">デビットのacct番号</span></span> 
- <span data-ttu-id="14da3-2667">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="14da3-2667">デビット勘定＃</span></span> 
- <span data-ttu-id="14da3-2668">デビットакктの番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2668">デビットACCTの番号</span></span> 
- <span data-ttu-id="14da3-2669">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2669">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="14da3-2670">Кэйворд_жп_банк_бранч_коде</span><span class="sxs-lookup"><span data-stu-id="14da3-2670">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="14da3-2671">Отемачи</span><span class="sxs-lookup"><span data-stu-id="14da3-2671">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="14da3-2672">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="14da3-2672">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2673">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2673">Format</span></span>

<span data-ttu-id="14da3-2674">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2674">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2675">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2675">Pattern</span></span>

<span data-ttu-id="14da3-2676">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2676">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2677">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2677">Checksum</span></span>

<span data-ttu-id="14da3-2678">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2678">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2679">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2679">Definition</span></span>

<span data-ttu-id="14da3-2680">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2680">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2681">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2681">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2682">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-2682">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2683">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2683">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="14da3-2684">Кэйворд_жп_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2684">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="14da3-2685">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-2685">dl#</span></span> 
- <span data-ttu-id="14da3-2686">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-2686">DL＃</span></span> 
- <span data-ttu-id="14da3-2687">библиотек</span><span class="sxs-lookup"><span data-stu-id="14da3-2687">dls#</span></span> 
- <span data-ttu-id="14da3-2688">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="14da3-2688">DLS＃</span></span> 
- <span data-ttu-id="14da3-2689">driver license</span><span class="sxs-lookup"><span data-stu-id="14da3-2689">driver license</span></span> 
- <span data-ttu-id="14da3-2690">driver licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2690">driver licenses</span></span> 
- <span data-ttu-id="14da3-2691">drivers license</span><span class="sxs-lookup"><span data-stu-id="14da3-2691">drivers license</span></span> 
- <span data-ttu-id="14da3-2692">driver's license</span><span class="sxs-lookup"><span data-stu-id="14da3-2692">driver's license</span></span> 
- <span data-ttu-id="14da3-2693">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2693">drivers licenses</span></span> 
- <span data-ttu-id="14da3-2694">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-2694">driver's licenses</span></span> 
- <span data-ttu-id="14da3-2695">driving licence</span><span class="sxs-lookup"><span data-stu-id="14da3-2695">driving licence</span></span> 
- <span data-ttu-id="14da3-2696">Лик #</span><span class="sxs-lookup"><span data-stu-id="14da3-2696">lic#</span></span> 
- <span data-ttu-id="14da3-2697">Лик #</span><span class="sxs-lookup"><span data-stu-id="14da3-2697">LIC＃</span></span> 
- <span data-ttu-id="14da3-2698">ликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-2698">lics#</span></span> 
- <span data-ttu-id="14da3-2699">state id</span><span class="sxs-lookup"><span data-stu-id="14da3-2699">state id</span></span> 
- <span data-ttu-id="14da3-2700">state identification</span><span class="sxs-lookup"><span data-stu-id="14da3-2700">state identification</span></span> 
- <span data-ttu-id="14da3-2701">state identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-2701">state identification number</span></span> 
- <span data-ttu-id="14da3-2702">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="14da3-2702">低所得国＃</span></span> 
- <span data-ttu-id="14da3-2703">免許証</span><span class="sxs-lookup"><span data-stu-id="14da3-2703">免許証</span></span> 
- <span data-ttu-id="14da3-2704">状態ид</span><span class="sxs-lookup"><span data-stu-id="14da3-2704">状態ID</span></span>
- <span data-ttu-id="14da3-2705">状態の識別</span><span class="sxs-lookup"><span data-stu-id="14da3-2705">状態の識別</span></span> 
- <span data-ttu-id="14da3-2706">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2706">状態の識別番号</span></span> 
- <span data-ttu-id="14da3-2707">運転免許</span><span class="sxs-lookup"><span data-stu-id="14da3-2707">運転免許</span></span> 
- <span data-ttu-id="14da3-2708">運転免許証</span><span class="sxs-lookup"><span data-stu-id="14da3-2708">運転免許証</span></span> 
- <span data-ttu-id="14da3-2709">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2709">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="14da3-2710">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="14da3-2710">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2711">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2711">Format</span></span>

<span data-ttu-id="14da3-2712">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2712">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2713">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2713">Pattern</span></span>

<span data-ttu-id="14da3-2714">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2714">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2715">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2715">Checksum</span></span>

<span data-ttu-id="14da3-2716">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2716">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2717">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2717">Definition</span></span>

<span data-ttu-id="14da3-2718">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2718">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2719">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2719">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2720">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="14da3-2720">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2721">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2721">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="14da3-2722">Кэйворд_жп_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-2722">Keyword_jp_passport</span></span>

- <span data-ttu-id="14da3-2723">パスポート</span><span class="sxs-lookup"><span data-stu-id="14da3-2723">パスポート</span></span> 
- <span data-ttu-id="14da3-2724">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2724">パスポート番号</span></span> 
- <span data-ttu-id="14da3-2725">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="14da3-2725">パスポートのNum</span></span> 
- <span data-ttu-id="14da3-2726">パスポート #</span><span class="sxs-lookup"><span data-stu-id="14da3-2726">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="14da3-2727">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="14da3-2727">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2728">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2728">Format</span></span>

<span data-ttu-id="14da3-2729">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2729">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2730">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2730">Pattern</span></span>

<span data-ttu-id="14da3-2731">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2731">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2732">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2732">Checksum</span></span>

<span data-ttu-id="14da3-2733">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2733">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2734">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2734">Definition</span></span>

<span data-ttu-id="14da3-2735">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2736">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2736">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2737">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-2737">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2738">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2738">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="14da3-2739">Кэйворд_жп_ресидент_регистратион_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2739">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="14da3-2740">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2740">Resident Registration Number</span></span>
- <span data-ttu-id="14da3-2741">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2741">Resident Register Number</span></span> 
- <span data-ttu-id="14da3-2742">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2742">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="14da3-2743">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2743">Resident Registration No.</span></span> 
- <span data-ttu-id="14da3-2744">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2744">Resident Register No.</span></span> 
- <span data-ttu-id="14da3-2745">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2745">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="14da3-2746">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2746">Basic Resident Register No.</span></span> 
- <span data-ttu-id="14da3-2747">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="14da3-2747">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="14da3-2748">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2748">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="14da3-2749">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="14da3-2749">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="14da3-2750">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2750">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="14da3-2751">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="14da3-2751">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2752">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2752">Format</span></span>

<span data-ttu-id="14da3-2753">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2753">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2754">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2754">Pattern</span></span>

<span data-ttu-id="14da3-2755">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-2755">7-12 digits:</span></span>
- <span data-ttu-id="14da3-2756">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-2756">Four digits</span></span> 
- <span data-ttu-id="14da3-2757">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14da3-2757">A hyphen (optional)</span></span> 
- <span data-ttu-id="14da3-2758">Шесть цифр или</span><span class="sxs-lookup"><span data-stu-id="14da3-2758">Six digits OR</span></span>
- <span data-ttu-id="14da3-2759">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2759">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2760">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2760">Checksum</span></span>

<span data-ttu-id="14da3-2761">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2761">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2762">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2762">Definition</span></span>

<span data-ttu-id="14da3-2763">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2763">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2764">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2764">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2765">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="14da3-2765">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="14da3-2766">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2766">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2767">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2767">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2768">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="14da3-2768">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2769">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2769">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="14da3-2770">Кэйворд_жп_син</span><span class="sxs-lookup"><span data-stu-id="14da3-2770">Keyword_jp_sin</span></span>

- <span data-ttu-id="14da3-2771">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="14da3-2771">Social Insurance No.</span></span> 
- <span data-ttu-id="14da3-2772">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="14da3-2772">Social Insurance Num</span></span> 
- <span data-ttu-id="14da3-2773">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2773">Social Insurance Number</span></span> 
- <span data-ttu-id="14da3-2774">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="14da3-2774">社会保険のテンキー</span></span> 
- <span data-ttu-id="14da3-2775">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2775">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="14da3-2776">Номер карточки для японского языка</span><span class="sxs-lookup"><span data-stu-id="14da3-2776">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2777">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2777">Format</span></span>

<span data-ttu-id="14da3-2778">12 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-2778">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2779">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2779">Pattern</span></span>

<span data-ttu-id="14da3-2780">12 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2780">12 letters and digits:</span></span>
- <span data-ttu-id="14da3-2781">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-2781">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="14da3-2782">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2782">Eight digits</span></span> 
- <span data-ttu-id="14da3-2783">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-2783">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2784">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2784">Checksum</span></span>

<span data-ttu-id="14da3-2785">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2785">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2786">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2786">Definition</span></span>

<span data-ttu-id="14da3-2787">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2788">Регулярное выражение Режекс_жп_ресиденце_кард_нумбер находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2788">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2789">Найдено ключевое слово из Кэйворд_жп_ресиденце_кард_нумбер.</span><span class="sxs-lookup"><span data-stu-id="14da3-2789">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2790">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2790">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="14da3-2791">Кэйворд_жп_ресиденце_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2791">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="14da3-2792">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="14da3-2792">Residence card number</span></span>
- <span data-ttu-id="14da3-2793">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="14da3-2793">Residence card no</span></span>
- <span data-ttu-id="14da3-2794">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="14da3-2794">Residence card #</span></span>
- <span data-ttu-id="14da3-2795">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="14da3-2795">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="14da3-2796">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="14da3-2796">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2797">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2797">Format</span></span>

<span data-ttu-id="14da3-2798">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="14da3-2798">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2799">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2799">Pattern</span></span>

<span data-ttu-id="14da3-2800">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2800">12 digits:</span></span>
- <span data-ttu-id="14da3-2801">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="14da3-2801">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="14da3-2802">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="14da3-2802">A dash (optional)</span></span> 
- <span data-ttu-id="14da3-2803">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="14da3-2803">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="14da3-2804">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="14da3-2804">A dash (optional)</span></span> 
- <span data-ttu-id="14da3-2805">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-2805">Three random digits</span></span> 
- <span data-ttu-id="14da3-2806">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-2806">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2807">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2807">Checksum</span></span>

<span data-ttu-id="14da3-2808">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2808">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2809">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2809">Definition</span></span>

<span data-ttu-id="14da3-2810">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2810">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2811">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2811">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2812">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="14da3-2812">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2813">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2813">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="14da3-2814">Кэйворд_малайсиа_ид_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2814">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="14da3-2815">карточка цифрового приложения</span><span class="sxs-lookup"><span data-stu-id="14da3-2815">digital application card</span></span>
- <span data-ttu-id="14da3-2816">i/c</span><span class="sxs-lookup"><span data-stu-id="14da3-2816">i/c</span></span>
- <span data-ttu-id="14da3-2817">i/c нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2817">i/c no</span></span>
- <span data-ttu-id="14da3-2818">внутренних</span><span class="sxs-lookup"><span data-stu-id="14da3-2818">ic</span></span>
- <span data-ttu-id="14da3-2819">МФ нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2819">ic no</span></span>
- <span data-ttu-id="14da3-2820">id card</span><span class="sxs-lookup"><span data-stu-id="14da3-2820">id card</span></span>
- <span data-ttu-id="14da3-2821">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="14da3-2821">identification Card</span></span>
- <span data-ttu-id="14da3-2822">identity card</span><span class="sxs-lookup"><span data-stu-id="14da3-2822">identity card</span></span>
- <span data-ttu-id="14da3-2823">k/p</span><span class="sxs-lookup"><span data-stu-id="14da3-2823">k/p</span></span>
- <span data-ttu-id="14da3-2824">k/p</span><span class="sxs-lookup"><span data-stu-id="14da3-2824">k/p no</span></span>
- <span data-ttu-id="14da3-2825">кад акуан Дири</span><span class="sxs-lookup"><span data-stu-id="14da3-2825">kad akuan diri</span></span>
- <span data-ttu-id="14da3-2826">кад апликаси Digital</span><span class="sxs-lookup"><span data-stu-id="14da3-2826">kad aplikasi digital</span></span>
- <span data-ttu-id="14da3-2827">кад пенженалан Малайзии</span><span class="sxs-lookup"><span data-stu-id="14da3-2827">kad pengenalan malaysia</span></span>
- <span data-ttu-id="14da3-2828">ключев</span><span class="sxs-lookup"><span data-stu-id="14da3-2828">kp</span></span>
- <span data-ttu-id="14da3-2829">ключевой номер</span><span class="sxs-lookup"><span data-stu-id="14da3-2829">kp no</span></span>
- <span data-ttu-id="14da3-2830">микад</span><span class="sxs-lookup"><span data-stu-id="14da3-2830">mykad</span></span>
- <span data-ttu-id="14da3-2831">Микас</span><span class="sxs-lookup"><span data-stu-id="14da3-2831">mykas</span></span>
- <span data-ttu-id="14da3-2832">микид</span><span class="sxs-lookup"><span data-stu-id="14da3-2832">mykid</span></span>
- <span data-ttu-id="14da3-2833">МИПР</span><span class="sxs-lookup"><span data-stu-id="14da3-2833">mypr</span></span>
- <span data-ttu-id="14da3-2834">митентера</span><span class="sxs-lookup"><span data-stu-id="14da3-2834">mytentera</span></span>
- <span data-ttu-id="14da3-2835">идентификационная карточка Малайзии</span><span class="sxs-lookup"><span data-stu-id="14da3-2835">malaysia identity card</span></span>
- <span data-ttu-id="14da3-2836">идентификационная карточка малайсиан</span><span class="sxs-lookup"><span data-stu-id="14da3-2836">malaysian identity card</span></span>
- <span data-ttu-id="14da3-2837">NRIC</span><span class="sxs-lookup"><span data-stu-id="14da3-2837">nric</span></span>
- <span data-ttu-id="14da3-2838">Личная идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="14da3-2838">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="14da3-2839">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="14da3-2839">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2840">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2840">Format</span></span>

<span data-ttu-id="14da3-2841">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="14da3-2841">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2842">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2842">Pattern</span></span>

<span data-ttu-id="14da3-2843">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2843">8-9 digits:</span></span>
- <span data-ttu-id="14da3-2844">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-2844">Three digits</span></span> 
- <span data-ttu-id="14da3-2845">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="14da3-2845">A space (optional)</span></span> 
- <span data-ttu-id="14da3-2846">три цифры; </span><span class="sxs-lookup"><span data-stu-id="14da3-2846">Three digits</span></span> 
- <span data-ttu-id="14da3-2847">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="14da3-2847">A space (optional)</span></span> 
- <span data-ttu-id="14da3-2848">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-2848">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2849">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2849">Checksum</span></span>

<span data-ttu-id="14da3-2850">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2850">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2851">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2851">Definition</span></span>

<span data-ttu-id="14da3-2852">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2852">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2853">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2853">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2854">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="14da3-2854">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="14da3-2855">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-2855">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="14da3-2856">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2856">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2857">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2857">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="14da3-2858">Кэйворд_несерландс_бсн</span><span class="sxs-lookup"><span data-stu-id="14da3-2858">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="14da3-2859">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="14da3-2859">Citizen service number</span></span> 
- <span data-ttu-id="14da3-2860">BSN</span><span class="sxs-lookup"><span data-stu-id="14da3-2860">BSN</span></span> 
- <span data-ttu-id="14da3-2861">Буржерсервиценуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2861">Burgerservicenummer</span></span> 
- <span data-ttu-id="14da3-2862">Софинуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2862">Sofinummer</span></span> 
- <span data-ttu-id="14da3-2863">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="14da3-2863">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="14da3-2864">Персунснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2864">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="14da3-2865">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="14da3-2865">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2866">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2866">Format</span></span>

<span data-ttu-id="14da3-2867">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-2867">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2868">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2868">Pattern</span></span>

<span data-ttu-id="14da3-2869">Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2869">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2870">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2870">Checksum</span></span>

<span data-ttu-id="14da3-2871">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2871">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2872">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2872">Definition</span></span>

<span data-ttu-id="14da3-2873">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2873">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2874">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2874">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2875">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="14da3-2875">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="14da3-2876">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2876">The checksum passes.</span></span>

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

<span data-ttu-id="14da3-2877">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2877">Keywords</span></span>

<span data-ttu-id="14da3-2878">Кэйворд_нз_термс</span><span class="sxs-lookup"><span data-stu-id="14da3-2878">Keyword_nz_terms</span></span>

- <span data-ttu-id="14da3-2879">НХИ</span><span class="sxs-lookup"><span data-stu-id="14da3-2879">NHI</span></span> 
- <span data-ttu-id="14da3-2880">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="14da3-2880">New Zealand</span></span> 
- <span data-ttu-id="14da3-2881">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="14da3-2881">Health</span></span> 
- <span data-ttu-id="14da3-2882">обращения</span><span class="sxs-lookup"><span data-stu-id="14da3-2882">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="14da3-2883">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="14da3-2883">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2884">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2884">Format</span></span>

<span data-ttu-id="14da3-2885">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2885">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2886">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2886">Pattern</span></span>

<span data-ttu-id="14da3-2887">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2887">11 digits:</span></span>
- <span data-ttu-id="14da3-2888">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="14da3-2888">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="14da3-2889">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-2889">Three-digit individual number</span></span> 
- <span data-ttu-id="14da3-2890">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-2890">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2891">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2891">Checksum</span></span>

<span data-ttu-id="14da3-2892">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2892">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2893">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2893">Definition</span></span>

<span data-ttu-id="14da3-2894">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2894">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2895">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2895">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2896">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-2896">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="14da3-2897">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2897">The checksum passes.</span></span>
- <span data-ttu-id="14da3-2898">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2898">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2899">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2899">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2900">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2900">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2901">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2901">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="14da3-2902">Кэйворд_норвай_ид_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2902">Keyword_norway_id_number</span></span>

- <span data-ttu-id="14da3-2903">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-2903">Personal identification number</span></span>
- <span data-ttu-id="14da3-2904">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2904">Norwegian ID Number</span></span>
- <span data-ttu-id="14da3-2905">ID Number</span><span class="sxs-lookup"><span data-stu-id="14da3-2905">ID Number</span></span>
- <span data-ttu-id="14da3-2906">Процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-2906">Identification</span></span>
- <span data-ttu-id="14da3-2907">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2907">Personnummer</span></span>
- <span data-ttu-id="14da3-2908">Фøдселснуммер</span><span class="sxs-lookup"><span data-stu-id="14da3-2908">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="14da3-2909">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="14da3-2909">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2910">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2910">Format</span></span>

<span data-ttu-id="14da3-2911">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="14da3-2911">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2912">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2912">Pattern</span></span>

<span data-ttu-id="14da3-2913">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-2913">12 digits:</span></span>
- <span data-ttu-id="14da3-2914">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-2914">Four digits</span></span> 
- <span data-ttu-id="14da3-2915">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-2915">A hyphen</span></span> 
- <span data-ttu-id="14da3-2916">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-2916">Seven digits</span></span> 
- <span data-ttu-id="14da3-2917">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-2917">A hyphen</span></span> 
- <span data-ttu-id="14da3-2918">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="14da3-2918">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2919">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2919">Checksum</span></span>

<span data-ttu-id="14da3-2920">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2920">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2921">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2921">Definition</span></span>

<span data-ttu-id="14da3-2922">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2922">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2923">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2923">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2924">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="14da3-2924">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2925">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2925">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="14da3-2926">Кэйворд_филиппинес_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-2926">Keyword_philippines_id</span></span>

- <span data-ttu-id="14da3-2927">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="14da3-2927">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="14da3-2928">Умид</span><span class="sxs-lookup"><span data-stu-id="14da3-2928">UMID</span></span> 
- <span data-ttu-id="14da3-2929">Identity Card</span><span class="sxs-lookup"><span data-stu-id="14da3-2929">Identity Card</span></span> 
- <span data-ttu-id="14da3-2930">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="14da3-2930">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="14da3-2931">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="14da3-2931">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2932">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2932">Format</span></span>

<span data-ttu-id="14da3-2933">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2933">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2934">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2934">Pattern</span></span>

<span data-ttu-id="14da3-2935">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2935">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2936">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2936">Checksum</span></span>

<span data-ttu-id="14da3-2937">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2937">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2938">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2938">Definition</span></span>

<span data-ttu-id="14da3-2939">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_полиш_натионал_ид находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2939">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="14da3-2940">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-2940">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="14da3-2941">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2941">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2942">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2942">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="14da3-2943">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2943">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="14da3-2944">Довóд особисти</span><span class="sxs-lookup"><span data-stu-id="14da3-2944">Dowód osobisty</span></span>
- <span data-ttu-id="14da3-2945">Нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="14da3-2945">Numer dowodu osobistego</span></span>
- <span data-ttu-id="14da3-2946">Назва i нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="14da3-2946">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="14da3-2947">Назва i НР доводу особистего</span><span class="sxs-lookup"><span data-stu-id="14da3-2947">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="14da3-2948">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="14da3-2948">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="14da3-2949">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="14da3-2949">Dowód Tożsamości</span></span>
- <span data-ttu-id="14da3-2950">Dow.</span><span class="sxs-lookup"><span data-stu-id="14da3-2950">dow.</span></span> <span data-ttu-id="14da3-2951">совместим.</span><span class="sxs-lookup"><span data-stu-id="14da3-2951">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="14da3-2952">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="14da3-2952">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2953">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2953">Format</span></span>

<span data-ttu-id="14da3-2954">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2954">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2955">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2955">Pattern</span></span>

<span data-ttu-id="14da3-2956">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2956">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2957">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2957">Checksum</span></span>

<span data-ttu-id="14da3-2958">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2958">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2959">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2959">Definition</span></span>

<span data-ttu-id="14da3-2960">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2960">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2961">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2961">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2962">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-2962">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="14da3-2963">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2963">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2964">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2964">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="14da3-2965">Кэйворд_песел_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2965">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="14da3-2966">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="14da3-2966">Nr PESEL</span></span>
- <span data-ttu-id="14da3-2967">PESEL</span><span class="sxs-lookup"><span data-stu-id="14da3-2967">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="14da3-2968">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="14da3-2968">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2969">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2969">Format</span></span>

<span data-ttu-id="14da3-2970">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2970">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2971">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2971">Pattern</span></span>

<span data-ttu-id="14da3-2972">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2972">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2973">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2973">Checksum</span></span>

<span data-ttu-id="14da3-2974">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-2974">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2975">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2975">Definition</span></span>

<span data-ttu-id="14da3-2976">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2976">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2977">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2977">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2978">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-2978">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="14da3-2979">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-2979">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-2980">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2980">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="14da3-2981">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-2981">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="14da3-2982">Нумер пасзпорту</span><span class="sxs-lookup"><span data-stu-id="14da3-2982">Numer paszportu</span></span>
- <span data-ttu-id="14da3-2983">НР.</span><span class="sxs-lookup"><span data-stu-id="14da3-2983">Nr.</span></span> <span data-ttu-id="14da3-2984">Пасзпорту</span><span class="sxs-lookup"><span data-stu-id="14da3-2984">Paszportu</span></span>
- <span data-ttu-id="14da3-2985">Пасзпорт</span><span class="sxs-lookup"><span data-stu-id="14da3-2985">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="14da3-2986">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="14da3-2986">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-2987">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-2987">Format</span></span>

<span data-ttu-id="14da3-2988">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2988">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-2989">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-2989">Pattern</span></span>

<span data-ttu-id="14da3-2990">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-2990">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-2991">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-2991">Checksum</span></span>

<span data-ttu-id="14da3-2992">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-2992">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-2993">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-2993">Definition</span></span>

<span data-ttu-id="14da3-2994">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-2994">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-2995">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-2995">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-2996">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="14da3-2996">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-2997">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-2997">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="14da3-2998">Кэйворд_португал_Цитизен_кард</span><span class="sxs-lookup"><span data-stu-id="14da3-2998">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="14da3-2999">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="14da3-2999">Citizen Card</span></span>
- <span data-ttu-id="14da3-3000">National ID Card</span><span class="sxs-lookup"><span data-stu-id="14da3-3000">National ID Card</span></span>
- <span data-ttu-id="14da3-3001">CC</span><span class="sxs-lookup"><span data-stu-id="14da3-3001">CC</span></span>
- <span data-ttu-id="14da3-3002">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="14da3-3002">Cartão de Cidadão</span></span>
- <span data-ttu-id="14da3-3003">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="14da3-3003">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="14da3-3004">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="14da3-3004">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3005">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3005">Format</span></span>

<span data-ttu-id="14da3-3006">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3006">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3007">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3007">Pattern</span></span>

<span data-ttu-id="14da3-3008">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3008">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3009">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3009">Checksum</span></span>

<span data-ttu-id="14da3-3010">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3010">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3011">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3011">Definition</span></span>

<span data-ttu-id="14da3-3012">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3012">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3013">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3013">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3014">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="14da3-3014">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3015">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3015">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="14da3-3016">Кэйворд_сауди_арабиа_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-3016">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="14da3-3017">Identification Card</span><span class="sxs-lookup"><span data-stu-id="14da3-3017">Identification Card</span></span> 
- <span data-ttu-id="14da3-3018">I card number</span><span class="sxs-lookup"><span data-stu-id="14da3-3018">I card number</span></span> 
- <span data-ttu-id="14da3-3019">ID number</span><span class="sxs-lookup"><span data-stu-id="14da3-3019">ID number</span></span> 
- <span data-ttu-id="14da3-3020">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="14da3-3020">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="14da3-3021">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="14da3-3021">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3022">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3022">Format</span></span>

<span data-ttu-id="14da3-3023">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3023">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3024">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3024">Pattern</span></span>

- <span data-ttu-id="14da3-3025">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-3025">Nine letters and digits:</span></span>
- <span data-ttu-id="14da3-3026">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-3026">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-3027">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-3027">Seven digits</span></span> 
- <span data-ttu-id="14da3-3028">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="14da3-3028">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3029">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3029">Checksum</span></span>

<span data-ttu-id="14da3-3030">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3030">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3031">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3031">Definition</span></span>

<span data-ttu-id="14da3-3032">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3032">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3033">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3033">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3034">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="14da3-3034">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="14da3-3035">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3035">The checksum passes.</span></span>

<span data-ttu-id="14da3-3036">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3036">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3037">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3037">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3038">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3038">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3039">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3039">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="14da3-3040">Кэйворд_сингапоре_нрик</span><span class="sxs-lookup"><span data-stu-id="14da3-3040">Keyword_singapore_nric</span></span>

- <span data-ttu-id="14da3-3041">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="14da3-3041">National Registration Identity Card</span></span> 
- <span data-ttu-id="14da3-3042">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3042">Identity Card Number</span></span> 
- <span data-ttu-id="14da3-3043">NRIC</span><span class="sxs-lookup"><span data-stu-id="14da3-3043">NRIC</span></span> 
- <span data-ttu-id="14da3-3044">ВНУТРЕННИХ</span><span class="sxs-lookup"><span data-stu-id="14da3-3044">IC</span></span> 
- <span data-ttu-id="14da3-3045">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3045">Foreign Identification Number</span></span> 
- <span data-ttu-id="14da3-3046">ПРОЦЕНТ</span><span class="sxs-lookup"><span data-stu-id="14da3-3046">FIN</span></span> 
- <span data-ttu-id="14da3-3047">身份证</span><span class="sxs-lookup"><span data-stu-id="14da3-3047">身份证</span></span> 
- <span data-ttu-id="14da3-3048">身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-3048">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="14da3-3049">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="14da3-3049">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3050">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3050">Format</span></span>

<span data-ttu-id="14da3-3051">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="14da3-3051">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3052">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3052">Pattern</span></span>

<span data-ttu-id="14da3-3053">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-3053">13 digits:</span></span>
- <span data-ttu-id="14da3-3054">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="14da3-3054">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="14da3-3055">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-3055">Four digits</span></span> 
- <span data-ttu-id="14da3-3056">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="14da3-3056">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="14da3-3057">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="14da3-3057">The digit "8" or "9"</span></span> 
- <span data-ttu-id="14da3-3058">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="14da3-3058">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3059">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3059">Checksum</span></span>

<span data-ttu-id="14da3-3060">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3061">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3061">Definition</span></span>

<span data-ttu-id="14da3-3062">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3063">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3063">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3064">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-3064">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="14da3-3065">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3065">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3066">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3066">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="14da3-3067">Кэйворд_саус_африка_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3067">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="14da3-3068">Identity card</span><span class="sxs-lookup"><span data-stu-id="14da3-3068">Identity card</span></span>
- <span data-ttu-id="14da3-3069">ID</span><span class="sxs-lookup"><span data-stu-id="14da3-3069">ID</span></span>
- <span data-ttu-id="14da3-3070">Процедура</span><span class="sxs-lookup"><span data-stu-id="14da3-3070">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="14da3-3071">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="14da3-3071">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3072">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3072">Format</span></span>

<span data-ttu-id="14da3-3073">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="14da3-3073">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3074">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3074">Pattern</span></span>

<span data-ttu-id="14da3-3075">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-3075">13 digits:</span></span>
- <span data-ttu-id="14da3-3076">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="14da3-3076">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="14da3-3077">дефис;</span><span class="sxs-lookup"><span data-stu-id="14da3-3077">A hyphen</span></span> 
- <span data-ttu-id="14da3-3078">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="14da3-3078">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="14da3-3079">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="14da3-3079">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="14da3-3080">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="14da3-3080">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="14da3-3081">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="14da3-3081">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3082">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3082">Checksum</span></span>

<span data-ttu-id="14da3-3083">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3083">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3084">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3084">Definition</span></span>

<span data-ttu-id="14da3-3085">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3085">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3086">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3086">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3087">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-3087">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="14da3-3088">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3088">The checksum passes.</span></span>

<span data-ttu-id="14da3-3089">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3089">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3090">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3090">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3091">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3091">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3092">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3092">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="14da3-3093">Кэйворд_саус_кореа_ресидент_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3093">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="14da3-3094">National ID card</span><span class="sxs-lookup"><span data-stu-id="14da3-3094">National ID card</span></span> 
- <span data-ttu-id="14da3-3095">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3095">Citizen's Registration Number</span></span> 
- <span data-ttu-id="14da3-3096">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="14da3-3096">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="14da3-3097">РРН</span><span class="sxs-lookup"><span data-stu-id="14da3-3097">RRN</span></span> 
- <span data-ttu-id="14da3-3098">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="14da3-3098">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="14da3-3099">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="14da3-3099">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3100">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3100">Format</span></span>

<span data-ttu-id="14da3-3101">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3101">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3102">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3102">Pattern</span></span>

<span data-ttu-id="14da3-3103">11-12 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-3103">11-12 digits:</span></span>
- <span data-ttu-id="14da3-3104">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3104">Two digits</span></span> 
- <span data-ttu-id="14da3-3105">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14da3-3105">A forward slash (optional)</span></span> 
- <span data-ttu-id="14da3-3106">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3106">7-8 digits</span></span> 
- <span data-ttu-id="14da3-3107">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14da3-3107">A forward slash (optional)</span></span> 
- <span data-ttu-id="14da3-3108">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3108">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3109">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3109">Checksum</span></span>

<span data-ttu-id="14da3-3110">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3110">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3111">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3111">Definition</span></span>

<span data-ttu-id="14da3-3112">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3112">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3113">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3113">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3114">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3114">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3115">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3115">Keywords</span></span>

<span data-ttu-id="14da3-3116">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3116">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="14da3-3117">Строка подключения к SQL Server</span><span class="sxs-lookup"><span data-stu-id="14da3-3117">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3118">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3118">Format</span></span>

<span data-ttu-id="14da3-3119">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId", за которыми следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="14da3-3119">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3120">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3120">Pattern</span></span>

- <span data-ttu-id="14da3-3121">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId"</span><span class="sxs-lookup"><span data-stu-id="14da3-3121">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="14da3-3122">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="14da3-3122">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="14da3-3123">Строка "Password" или "pwd", где "pwd" не предшествует буква нижнего регистра</span><span class="sxs-lookup"><span data-stu-id="14da3-3123">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="14da3-3124">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="14da3-3124">An equal sign (=)</span></span>
- <span data-ttu-id="14da3-3125">Любой символ, не являющийся знаком доллара ($), символ процента (%), больше символа (_Гт_), символ "@", символ "@", знак кавычек ("), точка с запятой (;), левая фигурная скобка ([) или левая квадратная скобка ({)</span><span class="sxs-lookup"><span data-stu-id="14da3-3125">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="14da3-3126">Любая комбинация 7-128 символов, не отделяющая точку с запятой (;), косая черта (/) или кавычки (").</span><span class="sxs-lookup"><span data-stu-id="14da3-3126">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="14da3-3127">Точка с запятой (;) или кавычки (")</span><span class="sxs-lookup"><span data-stu-id="14da3-3127">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3128">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3128">Checksum</span></span>

<span data-ttu-id="14da3-3129">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3129">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3130">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3130">Definition</span></span>

<span data-ttu-id="14da3-3131">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3131">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3132">Регулярное выражение Цеп_режекс_склсерверконнектионстринг находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3132">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3133">**Не** найдено ключевое слово из цеп_глобалфилтер.</span><span class="sxs-lookup"><span data-stu-id="14da3-3133">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="14da3-3134">Регулярное выражение Цеп_пассвордплацехолдер не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3134">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3135">Регулярное выражение Цеп_коммонексамплекэйвордс не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3135">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3136">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3136">Keywords</span></span>

#### <a name="cepglobalfilter"></a><span data-ttu-id="14da3-3137">Цеп_глобалфилтер</span><span class="sxs-lookup"><span data-stu-id="14da3-3137">CEP_GlobalFilter</span></span>

- <span data-ttu-id="14da3-3138">Некоторые пароли</span><span class="sxs-lookup"><span data-stu-id="14da3-3138">some-password</span></span>
- <span data-ttu-id="14da3-3139">сомепассворд</span><span class="sxs-lookup"><span data-stu-id="14da3-3139">somepassword</span></span>
- <span data-ttu-id="14da3-3140">Секретпассворд</span><span class="sxs-lookup"><span data-stu-id="14da3-3140">secretPassword</span></span>
- <span data-ttu-id="14da3-3141">примером</span><span class="sxs-lookup"><span data-stu-id="14da3-3141">sample</span></span>

#### <a name="ceppasswordplaceholder"></a><span data-ttu-id="14da3-3142">Цеп_пассвордплацехолдер</span><span class="sxs-lookup"><span data-stu-id="14da3-3142">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="14da3-3143">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-3143">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-3144">Пароль или pwd, за которым следует 0-2 пробелов, знак равенства (=), 0-2 пробелы и звездочка (\*)--или--</span><span class="sxs-lookup"><span data-stu-id="14da3-3144">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="14da3-3145">Пароль или pwd, а затем:</span><span class="sxs-lookup"><span data-stu-id="14da3-3145">Password or pwd followed by:</span></span>
    - <span data-ttu-id="14da3-3146">Знак равенства (=)</span><span class="sxs-lookup"><span data-stu-id="14da3-3146">Equal sign (=)</span></span>
    - <span data-ttu-id="14da3-3147">Символ "меньше" (_Лт_)</span><span class="sxs-lookup"><span data-stu-id="14da3-3147">Less than symbol (<)</span></span>
    - <span data-ttu-id="14da3-3148">Любое сочетание 1-200 символов, которые являются буквами верхнего или нижнего регистра, цифрами, звездочкой (\*), дефисом (-), подчеркиванием (_) или символом пробела</span><span class="sxs-lookup"><span data-stu-id="14da3-3148">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="14da3-3149">Символ "больше" (_Гт_)</span><span class="sxs-lookup"><span data-stu-id="14da3-3149">Greater than symbol (>)</span></span>

#### <a name="cepcommonexamplekeywords"></a><span data-ttu-id="14da3-3150">Цеп_коммонексамплекэйвордс</span><span class="sxs-lookup"><span data-stu-id="14da3-3150">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="14da3-3151">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="14da3-3151">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="14da3-3152">компанией</span><span class="sxs-lookup"><span data-stu-id="14da3-3152">contoso</span></span>
- <span data-ttu-id="14da3-3153">компании</span><span class="sxs-lookup"><span data-stu-id="14da3-3153">fabrikam</span></span>
- <span data-ttu-id="14da3-3154">базу</span><span class="sxs-lookup"><span data-stu-id="14da3-3154">northwind</span></span>
- <span data-ttu-id="14da3-3155">песочниц</span><span class="sxs-lookup"><span data-stu-id="14da3-3155">sandbox</span></span>
- <span data-ttu-id="14da3-3156">онебокс</span><span class="sxs-lookup"><span data-stu-id="14da3-3156">onebox</span></span>
- <span data-ttu-id="14da3-3157">localhost</span><span class="sxs-lookup"><span data-stu-id="14da3-3157">localhost</span></span>
- <span data-ttu-id="14da3-3158">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="14da3-3158">127.0.0.1</span></span>
- <span data-ttu-id="14da3-3159">тестакс.</span><span class="sxs-lookup"><span data-stu-id="14da3-3159">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-3160">порта</span><span class="sxs-lookup"><span data-stu-id="14da3-3160">com</span></span>
- <span data-ttu-id="14da3-3161">s — int.</span><span class="sxs-lookup"><span data-stu-id="14da3-3161">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="14da3-3162">команде</span><span class="sxs-lookup"><span data-stu-id="14da3-3162">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="14da3-3163">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="14da3-3163">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3164">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3164">Format</span></span>

<span data-ttu-id="14da3-3165">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="14da3-3165">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3166">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3166">Pattern</span></span>

<span data-ttu-id="14da3-3167">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="14da3-3167">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="14da3-3168">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14da3-3168">2-4 digits (optional)</span></span> 
- <span data-ttu-id="14da3-3169">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="14da3-3169">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="14da3-3170">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="14da3-3170">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="14da3-3171">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-3171">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3172">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3172">Checksum</span></span>

<span data-ttu-id="14da3-3173">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3173">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3174">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3174">Definition</span></span>

<span data-ttu-id="14da3-3175">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3175">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3176">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3176">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3177">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3177">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3178">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3178">Keywords</span></span>

<span data-ttu-id="14da3-3179">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3179">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="14da3-3180">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="14da3-3180">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3181">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3181">Format</span></span>

<span data-ttu-id="14da3-3182">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3182">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3183">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3183">Pattern</span></span>

<span data-ttu-id="14da3-3184">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3184">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3185">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3185">Checksum</span></span>

<span data-ttu-id="14da3-3186">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3186">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3187">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3187">Definition</span></span>

<span data-ttu-id="14da3-3188">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3188">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3189">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3189">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3190">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-3190">One of the following is true:</span></span>
    - <span data-ttu-id="14da3-3191">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="14da3-3191">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="14da3-3192">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="14da3-3192">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3193">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3193">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="14da3-3194">Кэйворд_сведен_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-3194">Keyword_sweden_passport</span></span>

- <span data-ttu-id="14da3-3195">visa requirements</span><span class="sxs-lookup"><span data-stu-id="14da3-3195">visa requirements</span></span> 
- <span data-ttu-id="14da3-3196">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="14da3-3196">Alien Registration Card</span></span> 
- <span data-ttu-id="14da3-3197">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="14da3-3197">Schengen visas</span></span> 
- <span data-ttu-id="14da3-3198">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="14da3-3198">Schengen visa</span></span> 
- <span data-ttu-id="14da3-3199">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="14da3-3199">Visa Processing</span></span> 
- <span data-ttu-id="14da3-3200">Visa Type</span><span class="sxs-lookup"><span data-stu-id="14da3-3200">Visa Type</span></span> 
- <span data-ttu-id="14da3-3201">Single Entry</span><span class="sxs-lookup"><span data-stu-id="14da3-3201">Single Entry</span></span> 
- <span data-ttu-id="14da3-3202">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="14da3-3202">Multiple Entry</span></span> 
- <span data-ttu-id="14da3-3203">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="14da3-3203">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="14da3-3204">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-3204">Keyword_passport</span></span>

- <span data-ttu-id="14da3-3205">Passport Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3205">Passport Number</span></span> 
- <span data-ttu-id="14da3-3206">Passport No</span><span class="sxs-lookup"><span data-stu-id="14da3-3206">Passport No</span></span> 
- <span data-ttu-id="14da3-3207">Passport#</span><span class="sxs-lookup"><span data-stu-id="14da3-3207">Passport #</span></span> 
- <span data-ttu-id="14da3-3208">Службу</span><span class="sxs-lookup"><span data-stu-id="14da3-3208">Passport#</span></span> 
- <span data-ttu-id="14da3-3209">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="14da3-3209">PassportID</span></span> 
- <span data-ttu-id="14da3-3210">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="14da3-3210">Passportno</span></span> 
- <span data-ttu-id="14da3-3211">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3211">passportnumber</span></span> 
- <span data-ttu-id="14da3-3212">パスポート</span><span class="sxs-lookup"><span data-stu-id="14da3-3212">パスポート</span></span> 
- <span data-ttu-id="14da3-3213">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="14da3-3213">パスポート番号</span></span> 
- <span data-ttu-id="14da3-3214">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="14da3-3214">パスポートのNum</span></span> 
- <span data-ttu-id="14da3-3215">パスポート #</span><span class="sxs-lookup"><span data-stu-id="14da3-3215">パスポート＃</span></span> 
- <span data-ttu-id="14da3-3216">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="14da3-3216">Numéro de passeport</span></span> 
- <span data-ttu-id="14da3-3217">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="14da3-3217">Passeport n °</span></span> 
- <span data-ttu-id="14da3-3218">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="14da3-3218">Passeport Non</span></span> 
- <span data-ttu-id="14da3-3219">Passeport#</span><span class="sxs-lookup"><span data-stu-id="14da3-3219">Passeport #</span></span> 
- <span data-ttu-id="14da3-3220">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="14da3-3220">Passeport#</span></span> 
- <span data-ttu-id="14da3-3221">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="14da3-3221">PasseportNon</span></span> 
- <span data-ttu-id="14da3-3222">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="14da3-3222">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="14da3-3223">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="14da3-3223">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3224">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3224">Format</span></span>

<span data-ttu-id="14da3-3225">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-3225">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3226">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3226">Pattern</span></span>

<span data-ttu-id="14da3-3227">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3227">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="14da3-3228">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-3228">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-3229">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-3229">An optional space</span></span> 
- <span data-ttu-id="14da3-3230">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="14da3-3230">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="14da3-3231">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-3231">An optional space</span></span> 
- <span data-ttu-id="14da3-3232">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="14da3-3232">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3233">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3233">Checksum</span></span>

<span data-ttu-id="14da3-3234">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3234">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3235">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3235">Definition</span></span>

<span data-ttu-id="14da3-3236">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3236">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3237">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3237">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3238">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="14da3-3238">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3239">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3239">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="14da3-3240">Кэйворд_свифт</span><span class="sxs-lookup"><span data-stu-id="14da3-3240">Keyword_swift</span></span>

- <span data-ttu-id="14da3-3241">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="14da3-3241">international organization for standardization 9362</span></span> 
- <span data-ttu-id="14da3-3242">iso 9362</span><span class="sxs-lookup"><span data-stu-id="14da3-3242">iso 9362</span></span> 
- <span data-ttu-id="14da3-3243">iso9362</span><span class="sxs-lookup"><span data-stu-id="14da3-3243">iso9362</span></span> 
- <span data-ttu-id="14da3-3244">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="14da3-3244">swift\#</span></span> 
- <span data-ttu-id="14da3-3245">свифткоде</span><span class="sxs-lookup"><span data-stu-id="14da3-3245">swiftcode</span></span> 
- <span data-ttu-id="14da3-3246">свифтнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3246">swiftnumber</span></span> 
- <span data-ttu-id="14da3-3247">свифтраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3247">swiftroutingnumber</span></span> 
- <span data-ttu-id="14da3-3248">swift code</span><span class="sxs-lookup"><span data-stu-id="14da3-3248">swift code</span></span> 
- <span data-ttu-id="14da3-3249">swift number #</span><span class="sxs-lookup"><span data-stu-id="14da3-3249">swift number #</span></span> 
- <span data-ttu-id="14da3-3250">swift routing number</span><span class="sxs-lookup"><span data-stu-id="14da3-3250">swift routing number</span></span> 
- <span data-ttu-id="14da3-3251">bic number</span><span class="sxs-lookup"><span data-stu-id="14da3-3251">bic number</span></span> 
- <span data-ttu-id="14da3-3252">bic code</span><span class="sxs-lookup"><span data-stu-id="14da3-3252">bic code</span></span> 
- <span data-ttu-id="14da3-3253">БИК\#</span><span class="sxs-lookup"><span data-stu-id="14da3-3253">bic \#</span></span> 
- <span data-ttu-id="14da3-3254">БИК\#</span><span class="sxs-lookup"><span data-stu-id="14da3-3254">bic\#</span></span> 
- <span data-ttu-id="14da3-3255">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="14da3-3255">bank identifier code</span></span> 
- <span data-ttu-id="14da3-3256">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="14da3-3256">標準化9362</span></span> 
- <span data-ttu-id="14da3-3257">迅速 #</span><span class="sxs-lookup"><span data-stu-id="14da3-3257">迅速＃</span></span> 
- <span data-ttu-id="14da3-3258">Свифтコード</span><span class="sxs-lookup"><span data-stu-id="14da3-3258">SWIFTコード</span></span> 
- <span data-ttu-id="14da3-3259">Свифт番号</span><span class="sxs-lookup"><span data-stu-id="14da3-3259">SWIFT番号</span></span> 
- <span data-ttu-id="14da3-3260">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="14da3-3260">迅速なルーティング番号</span></span> 
- <span data-ttu-id="14da3-3261">Бик番号</span><span class="sxs-lookup"><span data-stu-id="14da3-3261">BIC番号</span></span> 
- <span data-ttu-id="14da3-3262">Бикコード</span><span class="sxs-lookup"><span data-stu-id="14da3-3262">BICコード</span></span> 
- <span data-ttu-id="14da3-3263">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="14da3-3263">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="14da3-3264">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="14da3-3264">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="14da3-3265">Быстрая\#</span><span class="sxs-lookup"><span data-stu-id="14da3-3265">rapide \#</span></span> 
- <span data-ttu-id="14da3-3266">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="14da3-3266">code SWIFT</span></span> 
- <span data-ttu-id="14da3-3267">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="14da3-3267">le numéro de swift</span></span> 
- <span data-ttu-id="14da3-3268">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="14da3-3268">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="14da3-3269">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="14da3-3269">le numéro BIC</span></span> 
- <span data-ttu-id="14da3-3270">\#БИК</span><span class="sxs-lookup"><span data-stu-id="14da3-3270">\# BIC</span></span> 
- <span data-ttu-id="14da3-3271">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="14da3-3271">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="14da3-3272">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="14da3-3272">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3273">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3273">Format</span></span>

<span data-ttu-id="14da3-3274">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3274">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3275">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3275">Pattern</span></span>

<span data-ttu-id="14da3-3276">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3276">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="14da3-3277">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-3277">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="14da3-3278">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="14da3-3278">The digit "1" or "2"</span></span> 
- <span data-ttu-id="14da3-3279">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3279">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3280">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3280">Checksum</span></span>

<span data-ttu-id="14da3-3281">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3281">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3282">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3282">Definition</span></span>

<span data-ttu-id="14da3-3283">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3283">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3284">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3284">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3285">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="14da3-3285">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="14da3-3286">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3286">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3287">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3287">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="14da3-3288">Кэйворд_таиванесе_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-3288">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="14da3-3289">身份證字號</span><span class="sxs-lookup"><span data-stu-id="14da3-3289">身份證字號</span></span> 
- <span data-ttu-id="14da3-3290">身份證</span><span class="sxs-lookup"><span data-stu-id="14da3-3290">身份證</span></span> 
- <span data-ttu-id="14da3-3291">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="14da3-3291">身份證號碼</span></span> 
- <span data-ttu-id="14da3-3292">身份證號</span><span class="sxs-lookup"><span data-stu-id="14da3-3292">身份證號</span></span> 
- <span data-ttu-id="14da3-3293">身分證字號</span><span class="sxs-lookup"><span data-stu-id="14da3-3293">身分證字號</span></span> 
- <span data-ttu-id="14da3-3294">身分證</span><span class="sxs-lookup"><span data-stu-id="14da3-3294">身分證</span></span> 
- <span data-ttu-id="14da3-3295">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="14da3-3295">身分證號碼</span></span> 
- <span data-ttu-id="14da3-3296">身份證號</span><span class="sxs-lookup"><span data-stu-id="14da3-3296">身份證號</span></span> 
- <span data-ttu-id="14da3-3297">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="14da3-3297">身分證統一編號</span></span> 
- <span data-ttu-id="14da3-3298">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="14da3-3298">國民身分證統一編號</span></span> 
- <span data-ttu-id="14da3-3299">簽名</span><span class="sxs-lookup"><span data-stu-id="14da3-3299">簽名</span></span> 
- <span data-ttu-id="14da3-3300">蓋章</span><span class="sxs-lookup"><span data-stu-id="14da3-3300">蓋章</span></span> 
- <span data-ttu-id="14da3-3301">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="14da3-3301">簽名或蓋章</span></span> 
- <span data-ttu-id="14da3-3302">簽章</span><span class="sxs-lookup"><span data-stu-id="14da3-3302">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="14da3-3303">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="14da3-3303">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3304">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3304">Format</span></span>

- <span data-ttu-id="14da3-3305">Номер биометрического паспорта: девять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3305">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="14da3-3306">Номер биометрической службы Passport: девять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3306">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3307">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3307">Pattern</span></span>
<span data-ttu-id="14da3-3308">Номер биометрического паспорта:</span><span class="sxs-lookup"><span data-stu-id="14da3-3308">Biometric passport number:</span></span>
- <span data-ttu-id="14da3-3309">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="14da3-3309">The digit "3"</span></span> 
- <span data-ttu-id="14da3-3310">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3310">Eight digits</span></span>

<span data-ttu-id="14da3-3311">Номер биометрической службы Passport:</span><span class="sxs-lookup"><span data-stu-id="14da3-3311">Non-biometric passport number:</span></span>
- <span data-ttu-id="14da3-3312">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3312">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3313">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3313">Checksum</span></span>

<span data-ttu-id="14da3-3314">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3314">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3315">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3315">Definition</span></span>

<span data-ttu-id="14da3-3316">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3316">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3317">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3317">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3318">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="14da3-3318">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3319">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3319">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="14da3-3320">Кэйворд_таиван_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-3320">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="14da3-3321">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="14da3-3321">ROC passport number</span></span> 
- <span data-ttu-id="14da3-3322">Passport number</span><span class="sxs-lookup"><span data-stu-id="14da3-3322">Passport number</span></span> 
- <span data-ttu-id="14da3-3323">Passport no</span><span class="sxs-lookup"><span data-stu-id="14da3-3323">Passport no</span></span> 
- <span data-ttu-id="14da3-3324">Passport Num</span><span class="sxs-lookup"><span data-stu-id="14da3-3324">Passport Num</span></span> 
- <span data-ttu-id="14da3-3325">Passport #</span><span class="sxs-lookup"><span data-stu-id="14da3-3325">Passport #</span></span> 
- <span data-ttu-id="14da3-3326">护照</span><span class="sxs-lookup"><span data-stu-id="14da3-3326">护照</span></span> 
- <span data-ttu-id="14da3-3327">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="14da3-3327">中華民國護照</span></span> 
- <span data-ttu-id="14da3-3328">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="14da3-3328">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="14da3-3329">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="14da3-3329">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3330">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3330">Format</span></span>

<span data-ttu-id="14da3-3331">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3331">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3332">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3332">Pattern</span></span>

<span data-ttu-id="14da3-3333">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-3333">10 letters and digits:</span></span>
- <span data-ttu-id="14da3-3334">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="14da3-3334">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="14da3-3335">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3335">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3336">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3336">Checksum</span></span>

<span data-ttu-id="14da3-3337">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3337">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3338">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3338">Definition</span></span>

<span data-ttu-id="14da3-3339">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3340">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3340">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3341">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="14da3-3341">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3342">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3342">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="14da3-3343">Кэйворд_таиван_ресидент_цертификате</span><span class="sxs-lookup"><span data-stu-id="14da3-3343">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="14da3-3344">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="14da3-3344">Resident Certificate</span></span> 
- <span data-ttu-id="14da3-3345">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="14da3-3345">Resident Cert</span></span> 
- <span data-ttu-id="14da3-3346">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="14da3-3346">Resident Cert.</span></span> 
- <span data-ttu-id="14da3-3347">Identification card</span><span class="sxs-lookup"><span data-stu-id="14da3-3347">Identification card</span></span> 
- <span data-ttu-id="14da3-3348">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="14da3-3348">Alien Resident Certificate</span></span> 
- <span data-ttu-id="14da3-3349">ГИПЕРБОЛ</span><span class="sxs-lookup"><span data-stu-id="14da3-3349">ARC</span></span> 
- <span data-ttu-id="14da3-3350">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="14da3-3350">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="14da3-3351">TARC</span><span class="sxs-lookup"><span data-stu-id="14da3-3351">TARC</span></span> 
- <span data-ttu-id="14da3-3352">居留證</span><span class="sxs-lookup"><span data-stu-id="14da3-3352">居留證</span></span> 
- <span data-ttu-id="14da3-3353">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="14da3-3353">外僑居留證</span></span> 
- <span data-ttu-id="14da3-3354">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="14da3-3354">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="14da3-3355">Код идентификации для тайского заполнения</span><span class="sxs-lookup"><span data-stu-id="14da3-3355">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3356">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3356">Format</span></span>

<span data-ttu-id="14da3-3357">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3357">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3358">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3358">Pattern</span></span>

<span data-ttu-id="14da3-3359">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="14da3-3359">13 digits:</span></span>
- <span data-ttu-id="14da3-3360">Первая цифра не равна 0 или 9</span><span class="sxs-lookup"><span data-stu-id="14da3-3360">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="14da3-3361">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3361">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3362">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3362">Checksum</span></span>

<span data-ttu-id="14da3-3363">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3363">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3364">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3364">Definition</span></span>

<span data-ttu-id="14da3-3365">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3365">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3366">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3366">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3367">Найдено ключевое слово из Кэйворд_саи_Цитизен_ид.</span><span class="sxs-lookup"><span data-stu-id="14da3-3367">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="14da3-3368">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3368">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3369">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3369">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3370">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3370">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="14da3-3371">Кэйворд_саи_Цитизен_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-3371">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="14da3-3372">ID Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3372">ID Number</span></span>
- <span data-ttu-id="14da3-3373">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="14da3-3373">Identification Number</span></span>
- <span data-ttu-id="14da3-3374">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="14da3-3374">บัตรประชาชน</span></span>
- <span data-ttu-id="14da3-3375">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="14da3-3375">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="14da3-3376">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="14da3-3376">บัตรประชาชน</span></span>
- <span data-ttu-id="14da3-3377">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="14da3-3377">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="14da3-3378">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="14da3-3378">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3379">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3379">Format</span></span>

<span data-ttu-id="14da3-3380">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3380">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3381">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3381">Pattern</span></span>

<span data-ttu-id="14da3-3382">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3382">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3383">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3383">Checksum</span></span>

<span data-ttu-id="14da3-3384">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3384">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3385">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3385">Definition</span></span>

<span data-ttu-id="14da3-3386">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3386">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3387">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3387">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3388">Найдено ключевое слово из Кэйворд_туркиш_натионал_ид.</span><span class="sxs-lookup"><span data-stu-id="14da3-3388">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="14da3-3389">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3389">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3390">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3390">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3391">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3391">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="14da3-3392">Кэйворд_туркиш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="14da3-3392">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="14da3-3393">TC Кимлик No</span><span class="sxs-lookup"><span data-stu-id="14da3-3393">TC Kimlik No</span></span>
- <span data-ttu-id="14da3-3394">TC Кимлик нумарасı</span><span class="sxs-lookup"><span data-stu-id="14da3-3394">TC Kimlik numarası</span></span>
- <span data-ttu-id="14da3-3395">Ватандаşлıк нумарасı</span><span class="sxs-lookup"><span data-stu-id="14da3-3395">Vatandaşlık numarası</span></span>
- <span data-ttu-id="14da3-3396">Ватандаşлıк нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3396">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="14da3-p142">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="14da3-p142">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3399">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3399">Format</span></span>

<span data-ttu-id="14da3-3400">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-3400">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3401">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3401">Pattern</span></span>

<span data-ttu-id="14da3-3402">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3402">18 letters and digits:</span></span>
- <span data-ttu-id="14da3-3403">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="14da3-3403">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="14da3-3404">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="14da3-3404">One digit</span></span> 
- <span data-ttu-id="14da3-3405">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="14da3-3405">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="14da3-3406">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="14da3-3406">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="14da3-3407">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3407">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3408">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3408">Checksum</span></span>

<span data-ttu-id="14da3-3409">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3409">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3410">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3410">Definition</span></span>

<span data-ttu-id="14da3-3411">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3412">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3412">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3413">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="14da3-3413">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="14da3-3414">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3414">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3415">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3415">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="14da3-3416">Кэйворд_ук_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-3416">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="14da3-3417">ДВЛА</span><span class="sxs-lookup"><span data-stu-id="14da3-3417">DVLA</span></span> 
- <span data-ttu-id="14da3-3418">light vans</span><span class="sxs-lookup"><span data-stu-id="14da3-3418">light vans</span></span> 
- <span data-ttu-id="14da3-3419">куадбикес</span><span class="sxs-lookup"><span data-stu-id="14da3-3419">quadbikes</span></span> 
- <span data-ttu-id="14da3-3420">motor cars</span><span class="sxs-lookup"><span data-stu-id="14da3-3420">motor cars</span></span> 
- <span data-ttu-id="14da3-3421">125cc</span><span class="sxs-lookup"><span data-stu-id="14da3-3421">125cc</span></span> 
- <span data-ttu-id="14da3-3422">сидекар</span><span class="sxs-lookup"><span data-stu-id="14da3-3422">sidecar</span></span> 
- <span data-ttu-id="14da3-3423">трициклес</span><span class="sxs-lookup"><span data-stu-id="14da3-3423">tricycles</span></span> 
- <span data-ttu-id="14da3-3424">моторциклес</span><span class="sxs-lookup"><span data-stu-id="14da3-3424">motorcycles</span></span> 
- <span data-ttu-id="14da3-3425">photocard licence</span><span class="sxs-lookup"><span data-stu-id="14da3-3425">photocard licence</span></span> 
- <span data-ttu-id="14da3-3426">learner drivers</span><span class="sxs-lookup"><span data-stu-id="14da3-3426">learner drivers</span></span> 
- <span data-ttu-id="14da3-3427">licence holder</span><span class="sxs-lookup"><span data-stu-id="14da3-3427">licence holder</span></span> 
- <span data-ttu-id="14da3-3428">licence holders</span><span class="sxs-lookup"><span data-stu-id="14da3-3428">licence holders</span></span> 
- <span data-ttu-id="14da3-3429">driving licences</span><span class="sxs-lookup"><span data-stu-id="14da3-3429">driving licences</span></span> 
- <span data-ttu-id="14da3-3430">driving licence</span><span class="sxs-lookup"><span data-stu-id="14da3-3430">driving licence</span></span> 
- <span data-ttu-id="14da3-3431">dual control car</span><span class="sxs-lookup"><span data-stu-id="14da3-3431">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="14da3-p143">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="14da3-p143">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3434">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3434">Format</span></span>

<span data-ttu-id="14da3-3435">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-3435">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3436">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3436">Pattern</span></span>

<span data-ttu-id="14da3-3437">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="14da3-3437">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3438">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3438">Checksum</span></span>

<span data-ttu-id="14da3-3439">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3439">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3440">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3440">Definition</span></span>

<span data-ttu-id="14da3-3441">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3441">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3442">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3442">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3443">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="14da3-3443">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3444">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3444">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="14da3-3445">Кэйворд_ук_електорал</span><span class="sxs-lookup"><span data-stu-id="14da3-3445">Keyword_uk_electoral</span></span>

- <span data-ttu-id="14da3-3446">council nomination</span><span class="sxs-lookup"><span data-stu-id="14da3-3446">council nomination</span></span> 
- <span data-ttu-id="14da3-3447">nomination form</span><span class="sxs-lookup"><span data-stu-id="14da3-3447">nomination form</span></span> 
- <span data-ttu-id="14da3-3448">electoral register</span><span class="sxs-lookup"><span data-stu-id="14da3-3448">electoral register</span></span> 
- <span data-ttu-id="14da3-3449">electoral roll</span><span class="sxs-lookup"><span data-stu-id="14da3-3449">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="14da3-p144">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="14da3-p144">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3452">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3452">Format</span></span>

<span data-ttu-id="14da3-3453">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="14da3-3453">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3454">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3454">Pattern</span></span>

<span data-ttu-id="14da3-3455">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3455">10-17 digits:</span></span>
- <span data-ttu-id="14da3-3456">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3456">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="14da3-3457">Пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-3457">A space</span></span> 
- <span data-ttu-id="14da3-3458">Три цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3458">Three digits</span></span> 
- <span data-ttu-id="14da3-3459">Пробел</span><span class="sxs-lookup"><span data-stu-id="14da3-3459">A space</span></span> 
- <span data-ttu-id="14da3-3460">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3460">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3461">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3461">Checksum</span></span>

<span data-ttu-id="14da3-3462">Да</span><span class="sxs-lookup"><span data-stu-id="14da3-3462">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3463">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3463">Definition</span></span>

<span data-ttu-id="14da3-3464">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3464">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3465">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3465">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3466">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-3466">One of the following is true:</span></span>
    - <span data-ttu-id="14da3-3467">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="14da3-3467">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="14da3-3468">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="14da3-3468">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="14da3-3469">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="14da3-3469">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="14da3-3470">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="14da3-3470">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3471">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3471">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="14da3-3472">Кэйворд_ук_нхс_нумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3472">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="14da3-3473">national health service</span><span class="sxs-lookup"><span data-stu-id="14da3-3473">national health service</span></span> 
- <span data-ttu-id="14da3-3474">NHS</span><span class="sxs-lookup"><span data-stu-id="14da3-3474">nhs</span></span> 
- <span data-ttu-id="14da3-3475">health services authority</span><span class="sxs-lookup"><span data-stu-id="14da3-3475">health services authority</span></span> 
- <span data-ttu-id="14da3-3476">health authority</span><span class="sxs-lookup"><span data-stu-id="14da3-3476">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="14da3-3477">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="14da3-3477">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="14da3-3478">patient id</span><span class="sxs-lookup"><span data-stu-id="14da3-3478">patient id</span></span> 
- <span data-ttu-id="14da3-3479">patient identification</span><span class="sxs-lookup"><span data-stu-id="14da3-3479">patient identification</span></span> 
- <span data-ttu-id="14da3-3480">patient no</span><span class="sxs-lookup"><span data-stu-id="14da3-3480">patient no</span></span> 
- <span data-ttu-id="14da3-3481">patient number</span><span class="sxs-lookup"><span data-stu-id="14da3-3481">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="14da3-3482">Кэйворд_ук_нхс_нумбер_доб</span><span class="sxs-lookup"><span data-stu-id="14da3-3482">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="14da3-3483">ГРУПП</span><span class="sxs-lookup"><span data-stu-id="14da3-3483">GP</span></span> 
- <span data-ttu-id="14da3-3484">ДОБ</span><span class="sxs-lookup"><span data-stu-id="14da3-3484">DOB</span></span> 
- <span data-ttu-id="14da3-3485">D. O. B</span><span class="sxs-lookup"><span data-stu-id="14da3-3485">D.O.B</span></span> 
- <span data-ttu-id="14da3-3486">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="14da3-3486">Date of Birth</span></span> 
- <span data-ttu-id="14da3-3487">Birth Date</span><span class="sxs-lookup"><span data-stu-id="14da3-3487">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="14da3-p145">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="14da3-p145">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3490">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3490">Format</span></span>

<span data-ttu-id="14da3-3491">7 символов или 9 символов, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3491">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3492">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3492">Pattern</span></span>

<span data-ttu-id="14da3-3493">Два возможных шаблона:</span><span class="sxs-lookup"><span data-stu-id="14da3-3493">Two possible patterns:</span></span>

- <span data-ttu-id="14da3-3494">Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-3494">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="14da3-3495">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3495">Six digits</span></span>
- <span data-ttu-id="14da3-3496">"A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="14da3-3496">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="14da3-3497">OR</span><span class="sxs-lookup"><span data-stu-id="14da3-3497">OR</span></span>

- <span data-ttu-id="14da3-3498">Две буквы</span><span class="sxs-lookup"><span data-stu-id="14da3-3498">Two letters</span></span>
- <span data-ttu-id="14da3-3499">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3499">A space or dash</span></span>
- <span data-ttu-id="14da3-3500">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3500">Two digits</span></span>
- <span data-ttu-id="14da3-3501">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3501">A space or dash</span></span>
- <span data-ttu-id="14da3-3502">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3502">Two digits</span></span>
- <span data-ttu-id="14da3-3503">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3503">A space or dash</span></span>
- <span data-ttu-id="14da3-3504">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3504">Two digits</span></span>
- <span data-ttu-id="14da3-3505">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3505">A space or dash</span></span>
- <span data-ttu-id="14da3-3506">Значение "A", "B", "C" или "'D"</span><span class="sxs-lookup"><span data-stu-id="14da3-3506">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3507">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3507">Checksum</span></span>

<span data-ttu-id="14da3-3508">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3508">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3509">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3509">Definition</span></span>

<span data-ttu-id="14da3-3510">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3510">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3511">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3511">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3512">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="14da3-3512">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="14da3-3513">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3513">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3514">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3514">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3515">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="14da3-3515">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3516">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3516">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="14da3-3517">Кэйворд_ук_нино</span><span class="sxs-lookup"><span data-stu-id="14da3-3517">Keyword_uk_nino</span></span>

- <span data-ttu-id="14da3-3518">national insurance number</span><span class="sxs-lookup"><span data-stu-id="14da3-3518">national insurance number</span></span> 
- <span data-ttu-id="14da3-3519">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="14da3-3519">national insurance contributions</span></span> 
- <span data-ttu-id="14da3-3520">protection act</span><span class="sxs-lookup"><span data-stu-id="14da3-3520">protection act</span></span> 
- <span data-ttu-id="14da3-3521">страхования</span><span class="sxs-lookup"><span data-stu-id="14da3-3521">insurance</span></span> 
- <span data-ttu-id="14da3-3522">social security number</span><span class="sxs-lookup"><span data-stu-id="14da3-3522">social security number</span></span> 
- <span data-ttu-id="14da3-3523">insurance application</span><span class="sxs-lookup"><span data-stu-id="14da3-3523">insurance application</span></span> 
- <span data-ttu-id="14da3-3524">medical application</span><span class="sxs-lookup"><span data-stu-id="14da3-3524">medical application</span></span> 
- <span data-ttu-id="14da3-3525">social insurance</span><span class="sxs-lookup"><span data-stu-id="14da3-3525">social insurance</span></span> 
- <span data-ttu-id="14da3-3526">medical attention</span><span class="sxs-lookup"><span data-stu-id="14da3-3526">medical attention</span></span> 
- <span data-ttu-id="14da3-3527">social security</span><span class="sxs-lookup"><span data-stu-id="14da3-3527">social security</span></span> 
- <span data-ttu-id="14da3-3528">great britain</span><span class="sxs-lookup"><span data-stu-id="14da3-3528">great britain</span></span> 
- <span data-ttu-id="14da3-3529">страхования</span><span class="sxs-lookup"><span data-stu-id="14da3-3529">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="14da3-p146">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="14da3-p146">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3532">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3532">Format</span></span>

<span data-ttu-id="14da3-3533">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3533">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3534">Pattern</span></span>

<span data-ttu-id="14da3-3535">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="14da3-3535">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3536">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3536">Checksum</span></span>

<span data-ttu-id="14da3-3537">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3537">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3538">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3538">Definition</span></span>

<span data-ttu-id="14da3-3539">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3539">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3540">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3540">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3541">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="14da3-3541">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3542">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3542">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="14da3-3543">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="14da3-3543">Keyword_passport</span></span>

- <span data-ttu-id="14da3-3544">Passport Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3544">Passport Number</span></span> 
- <span data-ttu-id="14da3-3545">Passport No</span><span class="sxs-lookup"><span data-stu-id="14da3-3545">Passport No</span></span> 
- <span data-ttu-id="14da3-3546">Passport#</span><span class="sxs-lookup"><span data-stu-id="14da3-3546">Passport #</span></span> 
- <span data-ttu-id="14da3-3547">Службу</span><span class="sxs-lookup"><span data-stu-id="14da3-3547">Passport#</span></span> 
- <span data-ttu-id="14da3-3548">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="14da3-3548">PassportID</span></span> 
- <span data-ttu-id="14da3-3549">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="14da3-3549">Passportno</span></span> 
- <span data-ttu-id="14da3-3550">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="14da3-3550">passportnumber</span></span> 
- <span data-ttu-id="14da3-3551">パスポート</span><span class="sxs-lookup"><span data-stu-id="14da3-3551">パスポート</span></span> 
- <span data-ttu-id="14da3-3552">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="14da3-3552">パスポート番号</span></span> 
- <span data-ttu-id="14da3-3553">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="14da3-3553">パスポートのNum</span></span> 
- <span data-ttu-id="14da3-3554">パスポート #</span><span class="sxs-lookup"><span data-stu-id="14da3-3554">パスポート＃</span></span> 
- <span data-ttu-id="14da3-3555">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="14da3-3555">Numéro de passeport</span></span> 
- <span data-ttu-id="14da3-3556">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="14da3-3556">Passeport n °</span></span> 
- <span data-ttu-id="14da3-3557">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="14da3-3557">Passeport Non</span></span> 
- <span data-ttu-id="14da3-3558">Passeport#</span><span class="sxs-lookup"><span data-stu-id="14da3-3558">Passeport #</span></span> 
- <span data-ttu-id="14da3-3559">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="14da3-3559">Passeport#</span></span> 
- <span data-ttu-id="14da3-3560">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="14da3-3560">PasseportNon</span></span> 
- <span data-ttu-id="14da3-3561">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="14da3-3561">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="14da3-3562">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="14da3-3562">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3563">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3563">Format</span></span>

<span data-ttu-id="14da3-3564">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3564">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3565">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3565">Pattern</span></span>

<span data-ttu-id="14da3-3566">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3566">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3567">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3567">Checksum</span></span>

<span data-ttu-id="14da3-3568">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3568">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3569">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3569">Definition</span></span>

<span data-ttu-id="14da3-3570">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3570">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3571">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3571">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3572">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="14da3-3572">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="14da3-3573">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3573">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="14da3-3574">Кэйворд_уса_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="14da3-3574">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="14da3-3575">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3575">Checking Account Number</span></span> 
- <span data-ttu-id="14da3-3576">Checking Account</span><span class="sxs-lookup"><span data-stu-id="14da3-3576">Checking Account</span></span> 
- <span data-ttu-id="14da3-3577">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-3577">Checking Account #</span></span> 
- <span data-ttu-id="14da3-3578">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3578">Checking Acct Number</span></span> 
- <span data-ttu-id="14da3-3579">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-3579">Checking Acct #</span></span> 
- <span data-ttu-id="14da3-3580">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3580">Checking Acct No.</span></span> 
- <span data-ttu-id="14da3-3581">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3581">Checking Account No.</span></span> 
- <span data-ttu-id="14da3-3582">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3582">Bank Account Number</span></span> 
- <span data-ttu-id="14da3-3583">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-3583">Bank Account #</span></span> 
- <span data-ttu-id="14da3-3584">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3584">Bank Acct Number</span></span> 
- <span data-ttu-id="14da3-3585">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-3585">Bank Acct #</span></span> 
- <span data-ttu-id="14da3-3586">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3586">Bank Acct No.</span></span> 
- <span data-ttu-id="14da3-3587">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3587">Bank Account No.</span></span> 
- <span data-ttu-id="14da3-3588">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3588">Savings Account Number</span></span> 
- <span data-ttu-id="14da3-3589">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="14da3-3589">Savings Account.</span></span> 
- <span data-ttu-id="14da3-3590">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-3590">Savings Account #</span></span> 
- <span data-ttu-id="14da3-3591">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3591">Savings Acct Number</span></span> 
- <span data-ttu-id="14da3-3592">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-3592">Savings Acct #</span></span> 
- <span data-ttu-id="14da3-3593">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3593">Savings Acct No.</span></span> 
- <span data-ttu-id="14da3-3594">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3594">Savings Account No.</span></span> 
- <span data-ttu-id="14da3-3595">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3595">Debit Account Number</span></span> 
- <span data-ttu-id="14da3-3596">Debit Account</span><span class="sxs-lookup"><span data-stu-id="14da3-3596">Debit Account</span></span> 
- <span data-ttu-id="14da3-3597">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="14da3-3597">Debit Account #</span></span> 
- <span data-ttu-id="14da3-3598">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="14da3-3598">Debit Acct Number</span></span> 
- <span data-ttu-id="14da3-3599">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="14da3-3599">Debit Acct #</span></span> 
- <span data-ttu-id="14da3-3600">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3600">Debit Acct No.</span></span> 
- <span data-ttu-id="14da3-3601">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="14da3-3601">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="14da3-3602">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="14da3-3602">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3603">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3603">Format</span></span>

<span data-ttu-id="14da3-3604">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="14da3-3604">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3605">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3605">Pattern</span></span>

<span data-ttu-id="14da3-3606">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="14da3-3606">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="14da3-3607">Девять цифр, отформатированных как DDD DDD DDD, будут совпадают.</span><span class="sxs-lookup"><span data-stu-id="14da3-3607">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="14da3-3608">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="14da3-3608">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3609">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3609">Checksum</span></span>

<span data-ttu-id="14da3-3610">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3610">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3611">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3611">Definition</span></span>

<span data-ttu-id="14da3-3612">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3612">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3613">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3613">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3614">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="14da3-3614">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="14da3-3615">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="14da3-3615">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="14da3-3616">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3616">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3617">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="14da3-3617">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3618">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="14da3-3618">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="14da3-3619">находится ключевое слово из Keyword_us_drivers_license_abbreviations.</span><span class="sxs-lookup"><span data-stu-id="14da3-3619">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="14da3-3620">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="14da3-3620">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3621">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3621">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="14da3-3622">Кэйворд_ус_дриверс_лиценсе_аббревиатионс</span><span class="sxs-lookup"><span data-stu-id="14da3-3622">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="14da3-3623">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-3623">DL</span></span> 
- <span data-ttu-id="14da3-3624">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="14da3-3624">DLS</span></span> 
- <span data-ttu-id="14da3-3625">КДЛ</span><span class="sxs-lookup"><span data-stu-id="14da3-3625">CDL</span></span> 
- <span data-ttu-id="14da3-3626">КДЛС</span><span class="sxs-lookup"><span data-stu-id="14da3-3626">CDLS</span></span> 
- <span data-ttu-id="14da3-3627">ID</span><span class="sxs-lookup"><span data-stu-id="14da3-3627">ID</span></span> 
- <span data-ttu-id="14da3-3628">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="14da3-3628">IDs</span></span> 
- <span data-ttu-id="14da3-3629">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-3629">DL#</span></span> 
- <span data-ttu-id="14da3-3630">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="14da3-3630">DLS#</span></span> 
- <span data-ttu-id="14da3-3631">КДЛ #</span><span class="sxs-lookup"><span data-stu-id="14da3-3631">CDL#</span></span> 
- <span data-ttu-id="14da3-3632">КДЛС #</span><span class="sxs-lookup"><span data-stu-id="14da3-3632">CDLS#</span></span> 
- <span data-ttu-id="14da3-3633">КОДОВ</span><span class="sxs-lookup"><span data-stu-id="14da3-3633">ID#</span></span>
- <span data-ttu-id="14da3-3634">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="14da3-3634">IDs#</span></span> 
- <span data-ttu-id="14da3-3635">ID number</span><span class="sxs-lookup"><span data-stu-id="14da3-3635">ID number</span></span> 
- <span data-ttu-id="14da3-3636">ID numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-3636">ID numbers</span></span> 
- <span data-ttu-id="14da3-3637">Лик</span><span class="sxs-lookup"><span data-stu-id="14da3-3637">LIC</span></span> 
- <span data-ttu-id="14da3-3638">Лик #</span><span class="sxs-lookup"><span data-stu-id="14da3-3638">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="14da3-3639">Кэйворд_ус_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-3639">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="14da3-3640">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="14da3-3640">DriverLic</span></span> 
- <span data-ttu-id="14da3-3641">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="14da3-3641">DriverLics</span></span> 
- <span data-ttu-id="14da3-3642">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-3642">DriverLicense</span></span> 
- <span data-ttu-id="14da3-3643">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-3643">DriverLicenses</span></span> 
- <span data-ttu-id="14da3-3644">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-3644">Driver Lic</span></span> 
- <span data-ttu-id="14da3-3645">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-3645">Driver Lics</span></span> 
- <span data-ttu-id="14da3-3646">Driver License</span><span class="sxs-lookup"><span data-stu-id="14da3-3646">Driver License</span></span> 
- <span data-ttu-id="14da3-3647">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-3647">Driver Licenses</span></span> 
- <span data-ttu-id="14da3-3648">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="14da3-3648">DriversLic</span></span> 
- <span data-ttu-id="14da3-3649">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="14da3-3649">DriversLics</span></span> 
- <span data-ttu-id="14da3-3650">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-3650">DriversLicense</span></span> 
- <span data-ttu-id="14da3-3651">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-3651">DriversLicenses</span></span> 
- <span data-ttu-id="14da3-3652">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-3652">Drivers Lic</span></span> 
- <span data-ttu-id="14da3-3653">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-3653">Drivers Lics</span></span> 
- <span data-ttu-id="14da3-3654">Drivers License</span><span class="sxs-lookup"><span data-stu-id="14da3-3654">Drivers License</span></span> 
- <span data-ttu-id="14da3-3655">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-3655">Drivers Licenses</span></span> 
- <span data-ttu-id="14da3-3656">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="14da3-3656">Driver'Lic</span></span> 
- <span data-ttu-id="14da3-3657">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="14da3-3657">Driver'Lics</span></span> 
- <span data-ttu-id="14da3-3658">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="14da3-3658">Driver'License</span></span> 
- <span data-ttu-id="14da3-3659">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-3659">Driver'Licenses</span></span> 
- <span data-ttu-id="14da3-3660">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-3660">Driver' Lic</span></span> 
- <span data-ttu-id="14da3-3661">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-3661">Driver' Lics</span></span> 
- <span data-ttu-id="14da3-3662">Driver' License</span><span class="sxs-lookup"><span data-stu-id="14da3-3662">Driver' License</span></span> 
- <span data-ttu-id="14da3-3663">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-3663">Driver' Licenses</span></span>
- <span data-ttu-id="14da3-3664">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="14da3-3664">Driver'sLic</span></span> 
- <span data-ttu-id="14da3-3665">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="14da3-3665">Driver'sLics</span></span> 
- <span data-ttu-id="14da3-3666">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="14da3-3666">Driver'sLicense</span></span> 
- <span data-ttu-id="14da3-3667">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="14da3-3667">Driver'sLicenses</span></span> 
- <span data-ttu-id="14da3-3668">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="14da3-3668">Driver's Lic</span></span> 
- <span data-ttu-id="14da3-3669">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="14da3-3669">Driver's Lics</span></span> 
- <span data-ttu-id="14da3-3670">Driver's License</span><span class="sxs-lookup"><span data-stu-id="14da3-3670">Driver's License</span></span> 
- <span data-ttu-id="14da3-3671">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-3671">Driver's Licenses</span></span> 
- <span data-ttu-id="14da3-3672">identification number</span><span class="sxs-lookup"><span data-stu-id="14da3-3672">identification number</span></span> 
- <span data-ttu-id="14da3-3673">identification numbers</span><span class="sxs-lookup"><span data-stu-id="14da3-3673">identification numbers</span></span> 
- <span data-ttu-id="14da3-3674">identification #</span><span class="sxs-lookup"><span data-stu-id="14da3-3674">identification #</span></span> 
- <span data-ttu-id="14da3-3675">id card</span><span class="sxs-lookup"><span data-stu-id="14da3-3675">id card</span></span> 
- <span data-ttu-id="14da3-3676">id cards</span><span class="sxs-lookup"><span data-stu-id="14da3-3676">id cards</span></span> 
- <span data-ttu-id="14da3-3677">identification card</span><span class="sxs-lookup"><span data-stu-id="14da3-3677">identification card</span></span> 
- <span data-ttu-id="14da3-3678">identification cards</span><span class="sxs-lookup"><span data-stu-id="14da3-3678">identification cards</span></span> 
- <span data-ttu-id="14da3-3679">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="14da3-3679">DriverLic#</span></span> 
- <span data-ttu-id="14da3-3680">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-3680">DriverLics#</span></span> 
- <span data-ttu-id="14da3-3681">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-3681">DriverLicense#</span></span> 
- <span data-ttu-id="14da3-3682">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-3682">DriverLicenses#</span></span> 
- <span data-ttu-id="14da3-3683">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-3683">Driver Lic#</span></span> 
- <span data-ttu-id="14da3-3684">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-3684">Driver Lics#</span></span> 
- <span data-ttu-id="14da3-3685">Driver License#</span><span class="sxs-lookup"><span data-stu-id="14da3-3685">Driver License#</span></span> 
- <span data-ttu-id="14da3-3686">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-3686">Driver Licenses#</span></span> 
- <span data-ttu-id="14da3-3687">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="14da3-3687">DriversLic#</span></span> 
- <span data-ttu-id="14da3-3688">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-3688">DriversLics#</span></span> 
- <span data-ttu-id="14da3-3689">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-3689">DriversLicense#</span></span> 
- <span data-ttu-id="14da3-3690">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-3690">DriversLicenses#</span></span> 
- <span data-ttu-id="14da3-3691">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-3691">Drivers Lic#</span></span> 
- <span data-ttu-id="14da3-3692">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-3692">Drivers Lics#</span></span> 
- <span data-ttu-id="14da3-3693">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="14da3-3693">Drivers License#</span></span> 
- <span data-ttu-id="14da3-3694">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-3694">Drivers Licenses#</span></span> 
- <span data-ttu-id="14da3-3695">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="14da3-3695">Driver'Lic#</span></span> 
- <span data-ttu-id="14da3-3696">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="14da3-3696">Driver'Lics#</span></span> 
- <span data-ttu-id="14da3-3697">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="14da3-3697">Driver'License#</span></span> 
- <span data-ttu-id="14da3-3698">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="14da3-3698">Driver'Licenses#</span></span> 
- <span data-ttu-id="14da3-3699">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-3699">Driver' Lic#</span></span> 
- <span data-ttu-id="14da3-3700">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-3700">Driver' Lics#</span></span> 
- <span data-ttu-id="14da3-3701">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="14da3-3701">Driver' License#</span></span> 
- <span data-ttu-id="14da3-3702">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-3702">Driver' Licenses#</span></span> 
- <span data-ttu-id="14da3-3703">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="14da3-3703">Driver'sLic#</span></span> 
- <span data-ttu-id="14da3-3704">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="14da3-3704">Driver'sLics#</span></span> 
- <span data-ttu-id="14da3-3705">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="14da3-3705">Driver'sLicense#</span></span> 
- <span data-ttu-id="14da3-3706">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="14da3-3706">Driver'sLicenses#</span></span> 
- <span data-ttu-id="14da3-3707">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="14da3-3707">Driver's Lic#</span></span> 
- <span data-ttu-id="14da3-3708">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="14da3-3708">Driver's Lics#</span></span> 
- <span data-ttu-id="14da3-3709">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="14da3-3709">Driver's License#</span></span> 
- <span data-ttu-id="14da3-3710">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="14da3-3710">Driver's Licenses#</span></span> 
- <span data-ttu-id="14da3-3711">id card#</span><span class="sxs-lookup"><span data-stu-id="14da3-3711">id card#</span></span> 
- <span data-ttu-id="14da3-3712">id cards#</span><span class="sxs-lookup"><span data-stu-id="14da3-3712">id cards#</span></span> 
- <span data-ttu-id="14da3-3713">identification card#</span><span class="sxs-lookup"><span data-stu-id="14da3-3713">identification card#</span></span> 
- <span data-ttu-id="14da3-3714">identification cards#</span><span class="sxs-lookup"><span data-stu-id="14da3-3714">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="14da3-3715">Кэйворд_ [стате_наме] _дриверс_лиценсе_наме</span><span class="sxs-lookup"><span data-stu-id="14da3-3715">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="14da3-3716">Аббревиатура штата (например, NY)</span><span class="sxs-lookup"><span data-stu-id="14da3-3716">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="14da3-3717">Название штата (например, New York)</span><span class="sxs-lookup"><span data-stu-id="14da3-3717">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="14da3-3718">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="14da3-3718">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3719">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3719">Format</span></span>

<span data-ttu-id="14da3-3720">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="14da3-3720">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3721">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3721">Pattern</span></span>

<span data-ttu-id="14da3-3722">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="14da3-3722">Formatted:</span></span>
- <span data-ttu-id="14da3-3723">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="14da3-3723">The digit "9"</span></span> 
- <span data-ttu-id="14da3-3724">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3724">Two digits</span></span> 
- <span data-ttu-id="14da3-3725">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3725">A space or dash</span></span> 
- <span data-ttu-id="14da3-3726">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="14da3-3726">A "7" or "8"</span></span> 
- <span data-ttu-id="14da3-3727">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="14da3-3727">A digit</span></span> 
- <span data-ttu-id="14da3-3728">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="14da3-3728">A space, or dash</span></span> 
- <span data-ttu-id="14da3-3729">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3729">Four digits</span></span>

<span data-ttu-id="14da3-3730">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="14da3-3730">Unformatted:</span></span>
- <span data-ttu-id="14da3-3731">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="14da3-3731">The digit "9"</span></span> 
- <span data-ttu-id="14da3-3732">Две цифры</span><span class="sxs-lookup"><span data-stu-id="14da3-3732">Two digits</span></span> 
- <span data-ttu-id="14da3-3733">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="14da3-3733">A "7" or "8"</span></span> 
- <span data-ttu-id="14da3-3734">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="14da3-3734">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3735">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3735">Checksum</span></span>

<span data-ttu-id="14da3-3736">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3736">No</span></span>

### <a name="definition"></a><span data-ttu-id="14da3-3737">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3737">Definition</span></span>

<span data-ttu-id="14da3-3738">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3738">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3739">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3739">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3740">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-3740">At least one of the following is true:</span></span>
    - <span data-ttu-id="14da3-3741">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="14da3-3741">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="14da3-3742">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="14da3-3742">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="14da3-3743">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-3743">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="14da3-3744">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="14da3-3744">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="14da3-3745">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3745">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3746">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3746">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3747">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="14da3-3747">At least one of the following is true:</span></span>
    - <span data-ttu-id="14da3-3748">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="14da3-3748">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="14da3-3749">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="14da3-3749">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="14da3-3750">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="14da3-3750">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3751">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3751">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="14da3-3752">Кэйворд_итин</span><span class="sxs-lookup"><span data-stu-id="14da3-3752">Keyword_itin</span></span>

- <span data-ttu-id="14da3-3753">дубликат</span><span class="sxs-lookup"><span data-stu-id="14da3-3753">taxpayer</span></span> 
- <span data-ttu-id="14da3-3754">tax id</span><span class="sxs-lookup"><span data-stu-id="14da3-3754">tax id</span></span> 
- <span data-ttu-id="14da3-3755">tax identification</span><span class="sxs-lookup"><span data-stu-id="14da3-3755">tax identification</span></span> 
- <span data-ttu-id="14da3-3756">SharePointв</span><span class="sxs-lookup"><span data-stu-id="14da3-3756">itin</span></span> 
- <span data-ttu-id="14da3-3757">SSN</span><span class="sxs-lookup"><span data-stu-id="14da3-3757">ssn</span></span> 
- <span data-ttu-id="14da3-3758">ИНН</span><span class="sxs-lookup"><span data-stu-id="14da3-3758">tin</span></span> 
- <span data-ttu-id="14da3-3759">social security</span><span class="sxs-lookup"><span data-stu-id="14da3-3759">social security</span></span> 
- <span data-ttu-id="14da3-3760">tax payer</span><span class="sxs-lookup"><span data-stu-id="14da3-3760">tax payer</span></span> 
- <span data-ttu-id="14da3-3761">итинс</span><span class="sxs-lookup"><span data-stu-id="14da3-3761">itins</span></span> 
- <span data-ttu-id="14da3-3762">такси</span><span class="sxs-lookup"><span data-stu-id="14da3-3762">taxid</span></span> 
- <span data-ttu-id="14da3-3763">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="14da3-3763">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="14da3-3764">Кэйворд_итин_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="14da3-3764">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="14da3-3765">Лицензия</span><span class="sxs-lookup"><span data-stu-id="14da3-3765">License</span></span> 
- <span data-ttu-id="14da3-3766">DL</span><span class="sxs-lookup"><span data-stu-id="14da3-3766">DL</span></span> 
- <span data-ttu-id="14da3-3767">ДОБ</span><span class="sxs-lookup"><span data-stu-id="14da3-3767">DOB</span></span> 
- <span data-ttu-id="14da3-3768">Birthdate</span><span class="sxs-lookup"><span data-stu-id="14da3-3768">Birthdate</span></span> 
- <span data-ttu-id="14da3-3769">День рождения </span><span class="sxs-lookup"><span data-stu-id="14da3-3769">Birthday</span></span> 
- <span data-ttu-id="14da3-3770">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="14da3-3770">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="14da3-3771">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="14da3-3771">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="14da3-3772">Format</span><span class="sxs-lookup"><span data-stu-id="14da3-3772">Format</span></span>

<span data-ttu-id="14da3-3773">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="14da3-3773">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="14da3-3774">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="14da3-3774">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="14da3-3775">Шаблон</span><span class="sxs-lookup"><span data-stu-id="14da3-3775">Pattern</span></span>

<span data-ttu-id="14da3-3776">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="14da3-3776">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="14da3-3777">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="14da3-3777">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="14da3-3778">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="14da3-3778">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="14da3-3779">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="14da3-3779">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="14da3-3780">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="14da3-3780">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="14da3-3781">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="14da3-3781">Checksum</span></span>

<span data-ttu-id="14da3-3782">Нет</span><span class="sxs-lookup"><span data-stu-id="14da3-3782">No</span></span>


### <a name="definition"></a><span data-ttu-id="14da3-3783">Определение</span><span class="sxs-lookup"><span data-stu-id="14da3-3783">Definition</span></span>

<span data-ttu-id="14da3-3784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3785">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3785">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3786">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="14da3-3786">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="14da3-3787">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3787">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3788">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3788">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3789">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="14da3-3789">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="14da3-3790">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3790">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3791">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3791">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3792">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="14da3-3792">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="14da3-3793">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3793">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="14da3-3794">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="14da3-3794">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="14da3-3795">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3795">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="14da3-3796">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="14da3-3796">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="14da3-3797">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="14da3-3797">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="14da3-3798">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="14da3-3798">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="14da3-3799">Кэйворд_ссн</span><span class="sxs-lookup"><span data-stu-id="14da3-3799">Keyword_ssn</span></span>

- <span data-ttu-id="14da3-3800">Social Security</span><span class="sxs-lookup"><span data-stu-id="14da3-3800">Social Security</span></span> 
- <span data-ttu-id="14da3-3801">Social Security#</span><span class="sxs-lookup"><span data-stu-id="14da3-3801">Social Security#</span></span> 
- <span data-ttu-id="14da3-3802">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="14da3-3802">Soc Sec</span></span> 
- <span data-ttu-id="14da3-3803">SSN</span><span class="sxs-lookup"><span data-stu-id="14da3-3803">SSN</span></span> 
- <span data-ttu-id="14da3-3804">SSNS</span><span class="sxs-lookup"><span data-stu-id="14da3-3804">SSNS</span></span> 
- <span data-ttu-id="14da3-3805">SSN</span><span class="sxs-lookup"><span data-stu-id="14da3-3805">SSN#</span></span> 
- <span data-ttu-id="14da3-3806">НН</span><span class="sxs-lookup"><span data-stu-id="14da3-3806">SS#</span></span> 
- <span data-ttu-id="14da3-3807">SSID</span><span class="sxs-lookup"><span data-stu-id="14da3-3807">SSID</span></span> 
   

