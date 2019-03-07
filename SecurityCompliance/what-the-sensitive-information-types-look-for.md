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
ms.openlocfilehash: 55fa8b6855a9a5bf2c84f6555dd8c8227a2ad9cf
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455271"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="504cd-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="504cd-104">What the sensitive information types look for</span></span>

<span data-ttu-id="504cd-105">Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="504cd-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="504cd-106">В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.</span><span class="sxs-lookup"><span data-stu-id="504cd-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="504cd-107">Тип конфиденциальной информации определяется шаблоном, который можно идентифицировать регулярным выражением или функцией.</span><span class="sxs-lookup"><span data-stu-id="504cd-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="504cd-108">Кроме того, для идентификации типа конфиденциальной информации могут использоваться подкрепляющие доказательства, такие как ключевые слова и контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="504cd-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="504cd-109">Уровень вероятности и расположение слов и знаков также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="504cd-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="504cd-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="504cd-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-111">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-111">Format</span></span>

<span data-ttu-id="504cd-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="504cd-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-113">Pattern</span></span>

<span data-ttu-id="504cd-114">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="504cd-114">Formatted:</span></span>
- <span data-ttu-id="504cd-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="504cd-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="504cd-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-116">A hyphen</span></span>
- <span data-ttu-id="504cd-117">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-117">Four digits</span></span>
- <span data-ttu-id="504cd-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-118">A hyphen</span></span>
- <span data-ttu-id="504cd-119">цифра.</span><span class="sxs-lookup"><span data-stu-id="504cd-119">A digit</span></span>

<span data-ttu-id="504cd-120">Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8.</span><span class="sxs-lookup"><span data-stu-id="504cd-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="504cd-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-121">Checksum</span></span>

<span data-ttu-id="504cd-122">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-123">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-123">Definition</span></span>

<span data-ttu-id="504cd-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="504cd-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="504cd-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-127">Keywords</span></span>

#### <a name="keywordabarouting"></a><span data-ttu-id="504cd-128">Кэйворд_аба_раутинг</span><span class="sxs-lookup"><span data-stu-id="504cd-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="504cd-129">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="504cd-129">aba</span></span>
- <span data-ttu-id="504cd-130">aba#</span><span class="sxs-lookup"><span data-stu-id="504cd-130">aba #</span></span>
- <span data-ttu-id="504cd-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="504cd-131">aba routing #</span></span>
- <span data-ttu-id="504cd-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="504cd-132">aba routing number</span></span>
- <span data-ttu-id="504cd-133">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="504cd-133">aba#</span></span>
- <span data-ttu-id="504cd-134">абараутинг #</span><span class="sxs-lookup"><span data-stu-id="504cd-134">abarouting#</span></span>
- <span data-ttu-id="504cd-135">aba number</span><span class="sxs-lookup"><span data-stu-id="504cd-135">aba number</span></span>
- <span data-ttu-id="504cd-136">абараутингнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-136">abaroutingnumber</span></span>
- <span data-ttu-id="504cd-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="504cd-137">american bank association routing #</span></span>
- <span data-ttu-id="504cd-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="504cd-138">american bank association routing number</span></span>
- <span data-ttu-id="504cd-139">американбанкассоЦиатионраутинг #</span><span class="sxs-lookup"><span data-stu-id="504cd-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="504cd-140">американбанкассоЦиатионраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="504cd-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="504cd-141">bank routing number</span></span>
- <span data-ttu-id="504cd-142">банкраутинг #</span><span class="sxs-lookup"><span data-stu-id="504cd-142">bankrouting#</span></span>
- <span data-ttu-id="504cd-143">банкраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-143">bankroutingnumber</span></span>
- <span data-ttu-id="504cd-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="504cd-144">routing transit number</span></span>
- <span data-ttu-id="504cd-145">РТН</span><span class="sxs-lookup"><span data-stu-id="504cd-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="504cd-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="504cd-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-147">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-147">Format</span></span>

<span data-ttu-id="504cd-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="504cd-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-149">Pattern</span></span>

<span data-ttu-id="504cd-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-150">Eight digits:</span></span>
- <span data-ttu-id="504cd-151">две цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-151">Two digits</span></span>
- <span data-ttu-id="504cd-152">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-152">A period</span></span>
- <span data-ttu-id="504cd-153">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-153">Three digits</span></span>
- <span data-ttu-id="504cd-154">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-154">A period</span></span>
- <span data-ttu-id="504cd-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-156">Checksum</span></span>

<span data-ttu-id="504cd-157">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-158">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-158">Definition</span></span>

<span data-ttu-id="504cd-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="504cd-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-162">Keywords</span></span>

#### <a name="keywordargentinanationalid"></a><span data-ttu-id="504cd-163">Кэйворд_аржентина_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="504cd-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="504cd-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="504cd-165">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="504cd-165">Identity</span></span> 
- <span data-ttu-id="504cd-166">Идентификация национальной идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="504cd-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="504cd-167">DNI</span><span class="sxs-lookup"><span data-stu-id="504cd-167">DNI</span></span> 
- <span data-ttu-id="504cd-168">Национальная реестр пользователей NIC</span><span class="sxs-lookup"><span data-stu-id="504cd-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="504cd-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="504cd-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="504cd-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="504cd-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="504cd-171">ИДЕНТИДАД</span><span class="sxs-lookup"><span data-stu-id="504cd-171">Identidad</span></span> 
- <span data-ttu-id="504cd-172">ИдентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="504cd-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="504cd-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="504cd-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-174">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-174">Format</span></span>

<span data-ttu-id="504cd-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="504cd-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-176">Pattern</span></span>

<span data-ttu-id="504cd-177">Номер счета состоит из 6–10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="504cd-178">Номер филиала государственного банка Австралии</span><span class="sxs-lookup"><span data-stu-id="504cd-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="504cd-179">три цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-179">Three digits</span></span> 
- <span data-ttu-id="504cd-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-180">A hyphen</span></span> 
- <span data-ttu-id="504cd-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-182">Checksum</span></span>

<span data-ttu-id="504cd-183">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-184">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-184">Definition</span></span>

<span data-ttu-id="504cd-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="504cd-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="504cd-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="504cd-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="504cd-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-192">Keywords</span></span>

#### <a name="keywordaustraliabankaccountnumber"></a><span data-ttu-id="504cd-193">Кэйворд_аустралиа_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="504cd-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="504cd-194">swift bank code</span></span>
- <span data-ttu-id="504cd-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="504cd-195">correspondent bank</span></span>
- <span data-ttu-id="504cd-196">base currency</span><span class="sxs-lookup"><span data-stu-id="504cd-196">base currency</span></span>
- <span data-ttu-id="504cd-197">usa account</span><span class="sxs-lookup"><span data-stu-id="504cd-197">usa account</span></span>
- <span data-ttu-id="504cd-198">holder address</span><span class="sxs-lookup"><span data-stu-id="504cd-198">holder address</span></span>
- <span data-ttu-id="504cd-199">bank address</span><span class="sxs-lookup"><span data-stu-id="504cd-199">bank address</span></span>
- <span data-ttu-id="504cd-200">information account</span><span class="sxs-lookup"><span data-stu-id="504cd-200">information account</span></span>
- <span data-ttu-id="504cd-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="504cd-201">fund transfers</span></span>
- <span data-ttu-id="504cd-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="504cd-202">bank charges</span></span>
- <span data-ttu-id="504cd-203">bank details</span><span class="sxs-lookup"><span data-stu-id="504cd-203">bank details</span></span>
- <span data-ttu-id="504cd-204">banking information</span><span class="sxs-lookup"><span data-stu-id="504cd-204">banking information</span></span>
- <span data-ttu-id="504cd-205">full names</span><span class="sxs-lookup"><span data-stu-id="504cd-205">full names</span></span>
- <span data-ttu-id="504cd-206">иаеа</span><span class="sxs-lookup"><span data-stu-id="504cd-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="504cd-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="504cd-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-208">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-208">Format</span></span>

<span data-ttu-id="504cd-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-210">Pattern</span></span>

<span data-ttu-id="504cd-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="504cd-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-213">две цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-213">Two digits</span></span> 
- <span data-ttu-id="504cd-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="504cd-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="504cd-215">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="504cd-215">OR</span></span>

- <span data-ttu-id="504cd-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-217">4-9 digits</span></span>

<span data-ttu-id="504cd-218">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="504cd-218">OR</span></span>

- <span data-ttu-id="504cd-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="504cd-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-220">Checksum</span></span>

<span data-ttu-id="504cd-221">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-222">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-222">Definition</span></span>

<span data-ttu-id="504cd-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="504cd-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="504cd-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-227">Keywords</span></span>

#### <a name="keywordaustraliadriverslicensenumber"></a><span data-ttu-id="504cd-228">Кэйворд_аустралиа_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="504cd-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="504cd-229">international driving permits</span></span>
- <span data-ttu-id="504cd-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="504cd-230">australian automobile association</span></span>
- <span data-ttu-id="504cd-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="504cd-231">international driving permit</span></span>
- <span data-ttu-id="504cd-232">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="504cd-232">DriverLicence</span></span>
- <span data-ttu-id="504cd-233">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="504cd-233">DriverLicences</span></span>
- <span data-ttu-id="504cd-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-234">Driver Lic</span></span>
- <span data-ttu-id="504cd-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-235">Driver Licence</span></span>
- <span data-ttu-id="504cd-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-236">Driver Licences</span></span>
- <span data-ttu-id="504cd-237">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="504cd-237">DriversLic</span></span>
- <span data-ttu-id="504cd-238">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="504cd-238">DriversLicence</span></span>
- <span data-ttu-id="504cd-239">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="504cd-239">DriversLicences</span></span>
- <span data-ttu-id="504cd-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-240">Drivers Lic</span></span>
- <span data-ttu-id="504cd-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-241">Drivers Lics</span></span>
- <span data-ttu-id="504cd-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-242">Drivers Licence</span></span>
- <span data-ttu-id="504cd-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-243">Drivers Licences</span></span>
- <span data-ttu-id="504cd-244">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="504cd-244">Driver'Lic</span></span>
- <span data-ttu-id="504cd-245">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="504cd-245">Driver'Lics</span></span>
- <span data-ttu-id="504cd-246">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-246">Driver'Licence</span></span>
- <span data-ttu-id="504cd-247">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-247">Driver'Licences</span></span>
- <span data-ttu-id="504cd-248">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-248">Driver' Lic</span></span>
- <span data-ttu-id="504cd-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-249">Driver' Lics</span></span>
- <span data-ttu-id="504cd-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-250">Driver' Licence</span></span>
- <span data-ttu-id="504cd-251">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-251">Driver' Licences</span></span>
- <span data-ttu-id="504cd-252">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="504cd-252">Driver'sLic</span></span>
- <span data-ttu-id="504cd-253">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="504cd-253">Driver'sLics</span></span>
- <span data-ttu-id="504cd-254">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="504cd-254">Driver'sLicence</span></span>
- <span data-ttu-id="504cd-255">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="504cd-255">Driver'sLicences</span></span>
- <span data-ttu-id="504cd-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-256">Driver's Lic</span></span>
- <span data-ttu-id="504cd-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-257">Driver's Lics</span></span>
- <span data-ttu-id="504cd-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-258">Driver's Licence</span></span>
- <span data-ttu-id="504cd-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-259">Driver's Licences</span></span>
- <span data-ttu-id="504cd-260">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="504cd-260">DriverLic#</span></span>
- <span data-ttu-id="504cd-261">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-261">DriverLics#</span></span>
- <span data-ttu-id="504cd-262">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="504cd-262">DriverLicence#</span></span>
- <span data-ttu-id="504cd-263">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="504cd-263">DriverLicences#</span></span>
- <span data-ttu-id="504cd-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-264">Driver Lic#</span></span>
- <span data-ttu-id="504cd-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-265">Driver Lics#</span></span>
- <span data-ttu-id="504cd-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-266">Driver Licence#</span></span>
- <span data-ttu-id="504cd-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-267">Driver Licences#</span></span>
- <span data-ttu-id="504cd-268">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="504cd-268">DriversLic#</span></span>
- <span data-ttu-id="504cd-269">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-269">DriversLics#</span></span>
- <span data-ttu-id="504cd-270">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="504cd-270">DriversLicence#</span></span>
- <span data-ttu-id="504cd-271">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="504cd-271">DriversLicences#</span></span>
- <span data-ttu-id="504cd-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-272">Drivers Lic#</span></span>
- <span data-ttu-id="504cd-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-273">Drivers Lics#</span></span>
- <span data-ttu-id="504cd-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-274">Drivers Licence#</span></span>
- <span data-ttu-id="504cd-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-275">Drivers Licences#</span></span>
- <span data-ttu-id="504cd-276">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="504cd-276">Driver'Lic#</span></span>
- <span data-ttu-id="504cd-277">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="504cd-277">Driver'Lics#</span></span>
- <span data-ttu-id="504cd-278">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-278">Driver'Licence#</span></span>
- <span data-ttu-id="504cd-279">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-279">Driver'Licences#</span></span>
- <span data-ttu-id="504cd-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-280">Driver' Lic#</span></span>
- <span data-ttu-id="504cd-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-281">Driver' Lics#</span></span>
- <span data-ttu-id="504cd-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-282">Driver' Licence#</span></span>
- <span data-ttu-id="504cd-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-283">Driver' Licences#</span></span>
- <span data-ttu-id="504cd-284">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="504cd-284">Driver'sLic#</span></span>
- <span data-ttu-id="504cd-285">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-285">Driver'sLics#</span></span>
- <span data-ttu-id="504cd-286">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="504cd-286">Driver'sLicence#</span></span>
- <span data-ttu-id="504cd-287">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="504cd-287">Driver'sLicences#</span></span>
- <span data-ttu-id="504cd-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-288">Driver's Lic#</span></span>
- <span data-ttu-id="504cd-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-289">Driver's Lics#</span></span>
- <span data-ttu-id="504cd-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-290">Driver's Licence#</span></span>
- <span data-ttu-id="504cd-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-291">Driver's Licences#</span></span> 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a><span data-ttu-id="504cd-292">Кэйворд_аустралиа_дриверс_лиценсе_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="504cd-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="504cd-293">AAA</span><span class="sxs-lookup"><span data-stu-id="504cd-293">aaa</span></span>
- <span data-ttu-id="504cd-294">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-294">DriverLicense</span></span>
- <span data-ttu-id="504cd-295">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-295">DriverLicenses</span></span>
- <span data-ttu-id="504cd-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="504cd-296">Driver License</span></span>
- <span data-ttu-id="504cd-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-297">Driver Licenses</span></span>
- <span data-ttu-id="504cd-298">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-298">DriversLicense</span></span>
- <span data-ttu-id="504cd-299">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-299">DriversLicenses</span></span>
- <span data-ttu-id="504cd-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="504cd-300">Drivers License</span></span>
- <span data-ttu-id="504cd-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-301">Drivers Licenses</span></span>
- <span data-ttu-id="504cd-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="504cd-302">Driver'License</span></span>
- <span data-ttu-id="504cd-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-303">Driver'Licenses</span></span>
- <span data-ttu-id="504cd-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="504cd-304">Driver' License</span></span>
- <span data-ttu-id="504cd-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-305">Driver' Licenses</span></span>
- <span data-ttu-id="504cd-306">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-306">Driver'sLicense</span></span>
- <span data-ttu-id="504cd-307">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-307">Driver'sLicenses</span></span>
- <span data-ttu-id="504cd-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="504cd-308">Driver's License</span></span>
- <span data-ttu-id="504cd-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-309">Driver's Licenses</span></span>
- <span data-ttu-id="504cd-310">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-310">DriverLicense#</span></span>
- <span data-ttu-id="504cd-311">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-311">DriverLicenses#</span></span>
- <span data-ttu-id="504cd-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="504cd-312">Driver License#</span></span>
- <span data-ttu-id="504cd-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-313">Driver Licenses#</span></span>
- <span data-ttu-id="504cd-314">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-314">DriversLicense#</span></span>
- <span data-ttu-id="504cd-315">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-315">DriversLicenses#</span></span>
- <span data-ttu-id="504cd-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="504cd-316">Drivers License#</span></span>
- <span data-ttu-id="504cd-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-317">Drivers Licenses#</span></span>
- <span data-ttu-id="504cd-318">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="504cd-318">Driver'License#</span></span>
- <span data-ttu-id="504cd-319">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-319">Driver'Licenses#</span></span>
- <span data-ttu-id="504cd-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="504cd-320">Driver' License#</span></span>
- <span data-ttu-id="504cd-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-321">Driver' Licenses#</span></span>
- <span data-ttu-id="504cd-322">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-322">Driver'sLicense#</span></span>
- <span data-ttu-id="504cd-323">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="504cd-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="504cd-324">Driver's License#</span></span>
- <span data-ttu-id="504cd-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="504cd-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="504cd-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-327">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-327">Format</span></span>

<span data-ttu-id="504cd-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-329">Pattern</span></span>

<span data-ttu-id="504cd-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-330">10-11 digits:</span></span>
- <span data-ttu-id="504cd-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="504cd-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="504cd-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="504cd-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="504cd-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="504cd-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="504cd-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-335">Checksum</span></span>

<span data-ttu-id="504cd-336">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-337">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-337">Definition</span></span>

<span data-ttu-id="504cd-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="504cd-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="504cd-341">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-341">The checksum passes.</span></span>

<span data-ttu-id="504cd-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-344">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-345">Keywords</span></span>

#### <a name="keywordaustraliamedicalaccountnumber"></a><span data-ttu-id="504cd-346">Кэйворд_аустралиа_медикал_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="504cd-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="504cd-347">bank account details</span></span>
- <span data-ttu-id="504cd-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="504cd-348">medicare payments</span></span>
- <span data-ttu-id="504cd-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="504cd-349">mortgage account</span></span>
- <span data-ttu-id="504cd-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="504cd-350">bank payments</span></span>
- <span data-ttu-id="504cd-351">information branch</span><span class="sxs-lookup"><span data-stu-id="504cd-351">information branch</span></span>
- <span data-ttu-id="504cd-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="504cd-352">credit card loan</span></span>
- <span data-ttu-id="504cd-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="504cd-353">department of human services</span></span>
- <span data-ttu-id="504cd-354">local service</span><span class="sxs-lookup"><span data-stu-id="504cd-354">local service</span></span>
- <span data-ttu-id="504cd-355">Медикаре</span><span class="sxs-lookup"><span data-stu-id="504cd-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="504cd-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="504cd-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-357">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-357">Format</span></span>

<span data-ttu-id="504cd-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-359">Pattern</span></span>

<span data-ttu-id="504cd-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-361">Checksum</span></span>

<span data-ttu-id="504cd-362">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-363">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-363">Definition</span></span>

<span data-ttu-id="504cd-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-366">Найдено ключевое слово из Кэйворд_пасспорт или Кэйворд_аустралиа_пасспорт_нумбер.</span><span class="sxs-lookup"><span data-stu-id="504cd-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-367">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="504cd-368">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-368">Keyword_passport</span></span>

- <span data-ttu-id="504cd-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="504cd-369">Passport Number</span></span>
- <span data-ttu-id="504cd-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="504cd-370">Passport No</span></span>
- <span data-ttu-id="504cd-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="504cd-371">Passport #</span></span>
- <span data-ttu-id="504cd-372">Службу</span><span class="sxs-lookup"><span data-stu-id="504cd-372">Passport#</span></span>
- <span data-ttu-id="504cd-373">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="504cd-373">PassportID</span></span>
- <span data-ttu-id="504cd-374">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="504cd-374">Passportno</span></span>
- <span data-ttu-id="504cd-375">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-375">passportnumber</span></span>
- <span data-ttu-id="504cd-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="504cd-376">パスポート</span></span>
- <span data-ttu-id="504cd-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="504cd-377">パスポート番号</span></span>
- <span data-ttu-id="504cd-378">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="504cd-378">パスポートのNum</span></span>
- <span data-ttu-id="504cd-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="504cd-379">パスポート ＃</span></span> 
- <span data-ttu-id="504cd-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="504cd-380">Numéro de passeport</span></span>
- <span data-ttu-id="504cd-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="504cd-381">Passeport n °</span></span>
- <span data-ttu-id="504cd-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="504cd-382">Passeport Non</span></span>
- <span data-ttu-id="504cd-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="504cd-383">Passeport #</span></span>
- <span data-ttu-id="504cd-384">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="504cd-384">Passeport#</span></span>
- <span data-ttu-id="504cd-385">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="504cd-385">PasseportNon</span></span>
- <span data-ttu-id="504cd-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="504cd-386">Passeportn °</span></span>

#### <a name="keywordaustraliapassportnumber"></a><span data-ttu-id="504cd-387">Кэйворд_аустралиа_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="504cd-388">службу</span><span class="sxs-lookup"><span data-stu-id="504cd-388">passport</span></span>
- <span data-ttu-id="504cd-389">passport details</span><span class="sxs-lookup"><span data-stu-id="504cd-389">passport details</span></span>
- <span data-ttu-id="504cd-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="504cd-390">immigration and citizenship</span></span>
- <span data-ttu-id="504cd-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="504cd-391">commonwealth of australia</span></span>
- <span data-ttu-id="504cd-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="504cd-392">department of immigration</span></span>
- <span data-ttu-id="504cd-393">residential address</span><span class="sxs-lookup"><span data-stu-id="504cd-393">residential address</span></span>
- <span data-ttu-id="504cd-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="504cd-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="504cd-395">Visa</span><span class="sxs-lookup"><span data-stu-id="504cd-395">visa</span></span>
- <span data-ttu-id="504cd-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="504cd-396">national identity card</span></span>
- <span data-ttu-id="504cd-397">passport number</span><span class="sxs-lookup"><span data-stu-id="504cd-397">passport number</span></span>
- <span data-ttu-id="504cd-398">travel document</span><span class="sxs-lookup"><span data-stu-id="504cd-398">travel document</span></span>
- <span data-ttu-id="504cd-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="504cd-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="504cd-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="504cd-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-401">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-401">Format</span></span>

<span data-ttu-id="504cd-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-403">Pattern</span></span>

<span data-ttu-id="504cd-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="504cd-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="504cd-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-405">Three digits</span></span> 
- <span data-ttu-id="504cd-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-406">An optional space</span></span> 
- <span data-ttu-id="504cd-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-407">Three digits</span></span> 
- <span data-ttu-id="504cd-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-408">An optional space</span></span> 
- <span data-ttu-id="504cd-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="504cd-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-410">Checksum</span></span>

<span data-ttu-id="504cd-411">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-412">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-412">Definition</span></span>

<span data-ttu-id="504cd-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="504cd-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="504cd-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-416">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-417">Keywords</span></span>

#### <a name="keywordaustraliataxfilenumber"></a><span data-ttu-id="504cd-418">Кэйворд_аустралиа_такс_филе_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="504cd-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="504cd-419">australian business number</span></span>
- <span data-ttu-id="504cd-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="504cd-420">marginal tax rate</span></span>
- <span data-ttu-id="504cd-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="504cd-421">medicare levy</span></span>
- <span data-ttu-id="504cd-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="504cd-422">portfolio number</span></span>
- <span data-ttu-id="504cd-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="504cd-423">service veterans</span></span>
- <span data-ttu-id="504cd-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="504cd-424">withholding tax</span></span>
- <span data-ttu-id="504cd-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="504cd-425">individual tax return</span></span>
- <span data-ttu-id="504cd-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="504cd-426">tax file number</span></span>

#### <a name="keywordnumberexclusions"></a><span data-ttu-id="504cd-427">Кэйворд_нумбер_ексклусионс</span><span class="sxs-lookup"><span data-stu-id="504cd-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="504cd-428">00000001</span><span class="sxs-lookup"><span data-stu-id="504cd-428">00000000</span></span>
- <span data-ttu-id="504cd-429">11111111</span><span class="sxs-lookup"><span data-stu-id="504cd-429">11111111</span></span>
- <span data-ttu-id="504cd-430">22222222</span><span class="sxs-lookup"><span data-stu-id="504cd-430">22222222</span></span>
- <span data-ttu-id="504cd-431">33333333</span><span class="sxs-lookup"><span data-stu-id="504cd-431">33333333</span></span>
- <span data-ttu-id="504cd-432">44444444</span><span class="sxs-lookup"><span data-stu-id="504cd-432">44444444</span></span>
- <span data-ttu-id="504cd-433">55555555</span><span class="sxs-lookup"><span data-stu-id="504cd-433">55555555</span></span>
- <span data-ttu-id="504cd-434">66666666</span><span class="sxs-lookup"><span data-stu-id="504cd-434">66666666</span></span>
- <span data-ttu-id="504cd-435">77777777</span><span class="sxs-lookup"><span data-stu-id="504cd-435">77777777</span></span>
- <span data-ttu-id="504cd-436">88888888</span><span class="sxs-lookup"><span data-stu-id="504cd-436">88888888</span></span>
- <span data-ttu-id="504cd-437">99999999</span><span class="sxs-lookup"><span data-stu-id="504cd-437">99999999</span></span>
- <span data-ttu-id="504cd-438">000000000</span><span class="sxs-lookup"><span data-stu-id="504cd-438">000000000</span></span>
- <span data-ttu-id="504cd-439">111111111</span><span class="sxs-lookup"><span data-stu-id="504cd-439">111111111</span></span>
- <span data-ttu-id="504cd-440">222222222</span><span class="sxs-lookup"><span data-stu-id="504cd-440">222222222</span></span>
- <span data-ttu-id="504cd-441">333333333</span><span class="sxs-lookup"><span data-stu-id="504cd-441">333333333</span></span>
- <span data-ttu-id="504cd-442">444444444</span><span class="sxs-lookup"><span data-stu-id="504cd-442">444444444</span></span>
- <span data-ttu-id="504cd-443">555555555</span><span class="sxs-lookup"><span data-stu-id="504cd-443">555555555</span></span>
- <span data-ttu-id="504cd-444">666666666</span><span class="sxs-lookup"><span data-stu-id="504cd-444">666666666</span></span>
- <span data-ttu-id="504cd-445">777777777</span><span class="sxs-lookup"><span data-stu-id="504cd-445">777777777</span></span>
- <span data-ttu-id="504cd-446">888888888</span><span class="sxs-lookup"><span data-stu-id="504cd-446">888888888</span></span>
- <span data-ttu-id="504cd-447">999999999</span><span class="sxs-lookup"><span data-stu-id="504cd-447">999999999</span></span>
- <span data-ttu-id="504cd-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="504cd-448">0000000000</span></span>
- <span data-ttu-id="504cd-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="504cd-449">1111111111</span></span>
- <span data-ttu-id="504cd-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="504cd-450">2222222222</span></span>
- <span data-ttu-id="504cd-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="504cd-451">3333333333</span></span>
- <span data-ttu-id="504cd-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="504cd-452">4444444444</span></span>
- <span data-ttu-id="504cd-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="504cd-453">5555555555</span></span>
- <span data-ttu-id="504cd-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="504cd-454">6666666666</span></span>
- <span data-ttu-id="504cd-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="504cd-455">7777777777</span></span>
- <span data-ttu-id="504cd-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="504cd-456">8888888888</span></span>
- <span data-ttu-id="504cd-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="504cd-457">9999999999</span></span>
   
## <a name="belgium-national-number"></a><span data-ttu-id="504cd-458">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="504cd-458">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-459">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-459">Format</span></span>

<span data-ttu-id="504cd-460">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="504cd-460">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-461">Pattern</span></span>

<span data-ttu-id="504cd-462">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="504cd-462">11 digits plus delimiters:</span></span>
- <span data-ttu-id="504cd-463">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="504cd-463">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="504cd-464">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-464">A hyphen</span></span> 
- <span data-ttu-id="504cd-465">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="504cd-465">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="504cd-466">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-466">A period</span></span> 
- <span data-ttu-id="504cd-467">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-467">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-468">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-468">Checksum</span></span>

<span data-ttu-id="504cd-469">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-469">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-470">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-470">Definition</span></span>

<span data-ttu-id="504cd-471">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-472">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-472">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-473">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-473">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="504cd-474">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-474">The checksum passes.</span></span>

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-475">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-475">Keywords</span></span>

#### <a name="keywordbelgiumnationalnumber"></a><span data-ttu-id="504cd-476">Кэйворд_белгиум_натионал_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-476">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="504cd-477">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="504cd-477">Identity</span></span>
- <span data-ttu-id="504cd-478">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="504cd-478">Registration</span></span>
- <span data-ttu-id="504cd-479">Процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-479">Identification</span></span> 
- <span data-ttu-id="504cd-480">ИД</span><span class="sxs-lookup"><span data-stu-id="504cd-480">ID</span></span> 
- <span data-ttu-id="504cd-481">Идентитеитскаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-481">Identiteitskaart</span></span>
- <span data-ttu-id="504cd-482">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="504cd-482">Registratie nummer</span></span> 
- <span data-ttu-id="504cd-483">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="504cd-483">Identificatie nummer</span></span> 
- <span data-ttu-id="504cd-484">Идентитеит</span><span class="sxs-lookup"><span data-stu-id="504cd-484">Identiteit</span></span>
- <span data-ttu-id="504cd-485">Регистратие</span><span class="sxs-lookup"><span data-stu-id="504cd-485">Registratie</span></span>
- <span data-ttu-id="504cd-486">Идентификатие</span><span class="sxs-lookup"><span data-stu-id="504cd-486">Identificatie</span></span> 
- <span data-ttu-id="504cd-487">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="504cd-487">Carte d’identité</span></span> 
- <span data-ttu-id="504cd-488">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="504cd-488">numéro d'immatriculation</span></span>
- <span data-ttu-id="504cd-489">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="504cd-489">numéro d'identification</span></span>
- <span data-ttu-id="504cd-490">идентитé</span><span class="sxs-lookup"><span data-stu-id="504cd-490">identité</span></span> 
- <span data-ttu-id="504cd-491">инскриптион</span><span class="sxs-lookup"><span data-stu-id="504cd-491">inscription</span></span> 
- <span data-ttu-id="504cd-492">Идентификатион</span><span class="sxs-lookup"><span data-stu-id="504cd-492">Identifikation</span></span>
- <span data-ttu-id="504cd-493">Идентифизиерунг</span><span class="sxs-lookup"><span data-stu-id="504cd-493">Identifizierung</span></span>
- <span data-ttu-id="504cd-494">Идентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-494">Identifikationsnummer</span></span>
- <span data-ttu-id="504cd-495">Персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="504cd-495">Personalausweis</span></span>
- <span data-ttu-id="504cd-496">Регистриерунг</span><span class="sxs-lookup"><span data-stu-id="504cd-496">Registrierung</span></span>
- <span data-ttu-id="504cd-497">Регистратионснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-497">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="504cd-498">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="504cd-498">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-499">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-499">Format</span></span>

<span data-ttu-id="504cd-500">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="504cd-500">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-501">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-501">Pattern</span></span>

<span data-ttu-id="504cd-502">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="504cd-502">Formatted:</span></span>
- <span data-ttu-id="504cd-503">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-503">Three digits</span></span> 
- <span data-ttu-id="504cd-504">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-504">A period</span></span> 
- <span data-ttu-id="504cd-505">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-505">Three digits</span></span> 
- <span data-ttu-id="504cd-506">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-506">A period</span></span> 
- <span data-ttu-id="504cd-507">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-507">Three digits</span></span> 
- <span data-ttu-id="504cd-508">Дефис</span><span class="sxs-lookup"><span data-stu-id="504cd-508">A hyphen</span></span> 
- <span data-ttu-id="504cd-509">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-509">Two digits which are check digits</span></span>

<span data-ttu-id="504cd-510">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="504cd-510">Unformatted:</span></span>
- <span data-ttu-id="504cd-511">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="504cd-511">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-512">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-512">Checksum</span></span>

<span data-ttu-id="504cd-513">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-514">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-514">Definition</span></span>

<span data-ttu-id="504cd-515">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-515">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-516">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-516">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-517">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="504cd-517">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="504cd-518">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-518">The checksum passes.</span></span>

<span data-ttu-id="504cd-519">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-519">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-520">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-520">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-521">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-521">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-522">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-522">Keywords</span></span>

#### <a name="keywordbrazilcpf"></a><span data-ttu-id="504cd-523">Кэйворд_бразил_кпф</span><span class="sxs-lookup"><span data-stu-id="504cd-523">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="504cd-524">CPF</span><span class="sxs-lookup"><span data-stu-id="504cd-524">CPF</span></span>
- <span data-ttu-id="504cd-525">Процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-525">Identification</span></span>
- <span data-ttu-id="504cd-526">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="504cd-526">Registration</span></span>
- <span data-ttu-id="504cd-527">Реализации</span><span class="sxs-lookup"><span data-stu-id="504cd-527">Revenue</span></span>
- <span data-ttu-id="504cd-528">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="504cd-528">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="504cd-529">Импосто</span><span class="sxs-lookup"><span data-stu-id="504cd-529">Imposto</span></span> 
- <span data-ttu-id="504cd-530">Идентификаçãо</span><span class="sxs-lookup"><span data-stu-id="504cd-530">Identificação</span></span> 
- <span data-ttu-id="504cd-531">Инскриçãо</span><span class="sxs-lookup"><span data-stu-id="504cd-531">Inscrição</span></span> 
- <span data-ttu-id="504cd-532">Рецеита</span><span class="sxs-lookup"><span data-stu-id="504cd-532">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="504cd-533">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="504cd-533">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-534">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-534">Format</span></span>

<span data-ttu-id="504cd-535">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="504cd-535">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-536">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-536">Pattern</span></span>
<span data-ttu-id="504cd-537">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="504cd-537">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="504cd-538">две цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-538">Two digits</span></span> 
- <span data-ttu-id="504cd-539">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-539">A period</span></span> 
- <span data-ttu-id="504cd-540">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-540">Three digits</span></span> 
- <span data-ttu-id="504cd-541">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-541">A period</span></span> 
- <span data-ttu-id="504cd-542">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="504cd-542">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="504cd-543">косая черта;</span><span class="sxs-lookup"><span data-stu-id="504cd-543">A forward slash</span></span> 
- <span data-ttu-id="504cd-544">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-544">Four-digit branch number</span></span> 
- <span data-ttu-id="504cd-545">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-545">A hyphen</span></span> 
- <span data-ttu-id="504cd-546">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-546">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-547">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-547">Checksum</span></span>

<span data-ttu-id="504cd-548">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-548">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-549">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-549">Definition</span></span>

<span data-ttu-id="504cd-550">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-550">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-551">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-551">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-552">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="504cd-552">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="504cd-553">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-553">The checksum passes.</span></span>

<span data-ttu-id="504cd-554">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-554">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-555">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-555">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-556">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-556">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-557">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-557">Keywords</span></span>

#### <a name="keywordbrazilcnpj"></a><span data-ttu-id="504cd-558">Кэйворд_бразил_кнпж</span><span class="sxs-lookup"><span data-stu-id="504cd-558">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="504cd-559">CNPJ</span><span class="sxs-lookup"><span data-stu-id="504cd-559">CNPJ</span></span> 
- <span data-ttu-id="504cd-560">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="504cd-560">CNPJ/MF</span></span> 
- <span data-ttu-id="504cd-561">CNPJ – MF</span><span class="sxs-lookup"><span data-stu-id="504cd-561">CNPJ-MF</span></span> 
- <span data-ttu-id="504cd-562">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="504cd-562">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="504cd-563">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="504cd-563">Taxpayers Registry</span></span> 
- <span data-ttu-id="504cd-564">Legal entity</span><span class="sxs-lookup"><span data-stu-id="504cd-564">Legal entity</span></span> 
- <span data-ttu-id="504cd-565">Legal entities</span><span class="sxs-lookup"><span data-stu-id="504cd-565">Legal entities</span></span> 
- <span data-ttu-id="504cd-566">Registration Status</span><span class="sxs-lookup"><span data-stu-id="504cd-566">Registration Status</span></span> 
- <span data-ttu-id="504cd-567">Бизнес</span><span class="sxs-lookup"><span data-stu-id="504cd-567">Business</span></span> 
- <span data-ttu-id="504cd-568">Company</span><span class="sxs-lookup"><span data-stu-id="504cd-568">Company</span></span>
- <span data-ttu-id="504cd-569">CNPJ</span><span class="sxs-lookup"><span data-stu-id="504cd-569">CNPJ</span></span> 
- <span data-ttu-id="504cd-570">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="504cd-570">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="504cd-571">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="504cd-571">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="504cd-572">КГК</span><span class="sxs-lookup"><span data-stu-id="504cd-572">CGC</span></span> 
- <span data-ttu-id="504cd-573">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="504cd-573">Pessoa jurídica</span></span> 
- <span data-ttu-id="504cd-574">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="504cd-574">Pessoas jurídicas</span></span> 
- <span data-ttu-id="504cd-575">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="504cd-575">Situação cadastral</span></span> 
- <span data-ttu-id="504cd-576">Инскриçãо</span><span class="sxs-lookup"><span data-stu-id="504cd-576">Inscrição</span></span> 
- <span data-ttu-id="504cd-577">Емпреса</span><span class="sxs-lookup"><span data-stu-id="504cd-577">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="504cd-578">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="504cd-578">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-579">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-579">Format</span></span>

<span data-ttu-id="504cd-580">Registro Geral (старый формат): девять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-580">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="504cd-581">Registro de identidade (RIC) (новый формат): 11 цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-581">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-582">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-582">Pattern</span></span>

<span data-ttu-id="504cd-583">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="504cd-583">Registro Geral (old format):</span></span>
- <span data-ttu-id="504cd-584">две цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-584">Two digits</span></span> 
- <span data-ttu-id="504cd-585">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-585">A period</span></span> 
- <span data-ttu-id="504cd-586">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-586">Three digits</span></span> 
- <span data-ttu-id="504cd-587">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-587">A period</span></span> 
- <span data-ttu-id="504cd-588">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-588">Three digits</span></span> 
- <span data-ttu-id="504cd-589">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-589">A hyphen</span></span> 
- <span data-ttu-id="504cd-590">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-590">One digit which is a check digit</span></span>

<span data-ttu-id="504cd-591">Registro de identidade (RIC) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="504cd-591">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="504cd-592">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-592">10 digits</span></span> 
- <span data-ttu-id="504cd-593">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-593">A hyphen</span></span> 
- <span data-ttu-id="504cd-594">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-594">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-595">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-595">Checksum</span></span>

<span data-ttu-id="504cd-596">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-596">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-597">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-597">Definition</span></span>

<span data-ttu-id="504cd-598">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-598">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-599">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-599">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-600">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="504cd-600">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="504cd-601">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-601">The checksum passes.</span></span>

<span data-ttu-id="504cd-602">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-602">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-603">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-603">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-604">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-604">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-605">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-605">Keywords</span></span>

#### <a name="keywordbrazilrg"></a><span data-ttu-id="504cd-606">Кэйворд_бразил_рг</span><span class="sxs-lookup"><span data-stu-id="504cd-606">Keyword_brazil_rg</span></span>

<span data-ttu-id="504cd-607">Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр).</span><span class="sxs-lookup"><span data-stu-id="504cd-607">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="504cd-608">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="504cd-608">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-609">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-609">Format</span></span>

<span data-ttu-id="504cd-610">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-610">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-611">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-611">Pattern</span></span>

<span data-ttu-id="504cd-612">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-612">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="504cd-613">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="504cd-613">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="504cd-614">пять цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-614">Five digits</span></span> 
- <span data-ttu-id="504cd-615">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-615">A hyphen</span></span> 
- <span data-ttu-id="504cd-616">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="504cd-616">Three digits OR</span></span>
- <span data-ttu-id="504cd-617">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="504cd-617">A zero "0"</span></span> 
- <span data-ttu-id="504cd-618">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-618">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-619">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-619">Checksum</span></span>

<span data-ttu-id="504cd-620">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-620">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-621">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-621">Definition</span></span>

<span data-ttu-id="504cd-622">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-622">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-623">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-623">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-624">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-624">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="504cd-625">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-625">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="504cd-626">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-627">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-627">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-628">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-628">A keyword from Keyword_canada_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-629">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-629">Keywords</span></span>

#### <a name="keywordcanadabankaccountnumber"></a><span data-ttu-id="504cd-630">Кэйворд_канада_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-630">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="504cd-631">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="504cd-631">canada savings bonds</span></span>
- <span data-ttu-id="504cd-632">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="504cd-632">canada revenue agency</span></span>
- <span data-ttu-id="504cd-633">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="504cd-633">canadian financial institution</span></span>
- <span data-ttu-id="504cd-634">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="504cd-634">direct deposit form</span></span>
- <span data-ttu-id="504cd-635">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="504cd-635">canadian citizen</span></span>
- <span data-ttu-id="504cd-636">legal representative</span><span class="sxs-lookup"><span data-stu-id="504cd-636">legal representative</span></span>
- <span data-ttu-id="504cd-637">notary public</span><span class="sxs-lookup"><span data-stu-id="504cd-637">notary public</span></span>
- <span data-ttu-id="504cd-638">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="504cd-638">commissioner for oaths</span></span>
- <span data-ttu-id="504cd-639">child care benefit</span><span class="sxs-lookup"><span data-stu-id="504cd-639">child care benefit</span></span>
- <span data-ttu-id="504cd-640">universal child care</span><span class="sxs-lookup"><span data-stu-id="504cd-640">universal child care</span></span>
- <span data-ttu-id="504cd-641">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="504cd-641">canada child tax benefit</span></span>
- <span data-ttu-id="504cd-642">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="504cd-642">income tax benefit</span></span>
- <span data-ttu-id="504cd-643">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="504cd-643">harmonized sales tax</span></span>
- <span data-ttu-id="504cd-644">social insurance number</span><span class="sxs-lookup"><span data-stu-id="504cd-644">social insurance number</span></span>
- <span data-ttu-id="504cd-645">income tax refund</span><span class="sxs-lookup"><span data-stu-id="504cd-645">income tax refund</span></span>
- <span data-ttu-id="504cd-646">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="504cd-646">child tax benefit</span></span>
- <span data-ttu-id="504cd-647">territorial payments</span><span class="sxs-lookup"><span data-stu-id="504cd-647">territorial payments</span></span>
- <span data-ttu-id="504cd-648">institution number</span><span class="sxs-lookup"><span data-stu-id="504cd-648">institution number</span></span>
- <span data-ttu-id="504cd-649">deposit request</span><span class="sxs-lookup"><span data-stu-id="504cd-649">deposit request</span></span>
- <span data-ttu-id="504cd-650">banking information</span><span class="sxs-lookup"><span data-stu-id="504cd-650">banking information</span></span>
- <span data-ttu-id="504cd-651">direct deposit</span><span class="sxs-lookup"><span data-stu-id="504cd-651">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="504cd-652">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="504cd-652">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-653">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-653">Format</span></span>

<span data-ttu-id="504cd-654">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="504cd-654">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-655">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-655">Pattern</span></span>

<span data-ttu-id="504cd-656">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="504cd-656">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-657">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-657">Checksum</span></span>

<span data-ttu-id="504cd-658">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-658">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-659">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-659">Definition</span></span>

<span data-ttu-id="504cd-660">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-660">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-661">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-661">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-662">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="504cd-662">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="504cd-663">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="504cd-663">A keyword from Keyword_canada_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-664">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-664">Keywords</span></span>

#### <a name="keywordprovincenamedriverslicensename"></a><span data-ttu-id="504cd-665">Кэйворд_ [провинце_наме] _дриверс_лиценсе_наме</span><span class="sxs-lookup"><span data-stu-id="504cd-665">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="504cd-666">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="504cd-666">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="504cd-667">Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="504cd-667">The province name, for example Alberta</span></span>

#### <a name="keywordcanadadriverslicense"></a><span data-ttu-id="504cd-668">Кэйворд_канада_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-668">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="504cd-669">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-669">DL</span></span>
- <span data-ttu-id="504cd-670">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="504cd-670">DLS</span></span>
- <span data-ttu-id="504cd-671">КДЛ</span><span class="sxs-lookup"><span data-stu-id="504cd-671">CDL</span></span>
- <span data-ttu-id="504cd-672">КДЛС</span><span class="sxs-lookup"><span data-stu-id="504cd-672">CDLS</span></span>
- <span data-ttu-id="504cd-673">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="504cd-673">DriverLic</span></span>
- <span data-ttu-id="504cd-674">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="504cd-674">DriverLics</span></span>
- <span data-ttu-id="504cd-675">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-675">DriverLicense</span></span>
- <span data-ttu-id="504cd-676">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-676">DriverLicenses</span></span>
- <span data-ttu-id="504cd-677">Дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="504cd-677">DriverLicence</span></span>
- <span data-ttu-id="504cd-678">Дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="504cd-678">DriverLicences</span></span>
- <span data-ttu-id="504cd-679">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-679">Driver Lic</span></span>
- <span data-ttu-id="504cd-680">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-680">Driver Lics</span></span>
- <span data-ttu-id="504cd-681">Driver License</span><span class="sxs-lookup"><span data-stu-id="504cd-681">Driver License</span></span>
- <span data-ttu-id="504cd-682">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-682">Driver Licenses</span></span>
- <span data-ttu-id="504cd-683">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-683">Driver Licence</span></span>
- <span data-ttu-id="504cd-684">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-684">Driver Licences</span></span>
- <span data-ttu-id="504cd-685">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="504cd-685">DriversLic</span></span>
- <span data-ttu-id="504cd-686">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="504cd-686">DriversLics</span></span>
- <span data-ttu-id="504cd-687">Дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="504cd-687">DriversLicence</span></span>
- <span data-ttu-id="504cd-688">Дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="504cd-688">DriversLicences</span></span>
- <span data-ttu-id="504cd-689">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-689">DriversLicense</span></span>
- <span data-ttu-id="504cd-690">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-690">DriversLicenses</span></span>
- <span data-ttu-id="504cd-691">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-691">Drivers Lic</span></span>
- <span data-ttu-id="504cd-692">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-692">Drivers Lics</span></span>
- <span data-ttu-id="504cd-693">Drivers License</span><span class="sxs-lookup"><span data-stu-id="504cd-693">Drivers License</span></span>
- <span data-ttu-id="504cd-694">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-694">Drivers Licenses</span></span>
- <span data-ttu-id="504cd-695">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-695">Drivers Licence</span></span>
- <span data-ttu-id="504cd-696">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-696">Drivers Licences</span></span>
- <span data-ttu-id="504cd-697">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="504cd-697">Driver'Lic</span></span>
- <span data-ttu-id="504cd-698">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="504cd-698">Driver'Lics</span></span>
- <span data-ttu-id="504cd-699">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="504cd-699">Driver'License</span></span>
- <span data-ttu-id="504cd-700">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-700">Driver'Licenses</span></span>
- <span data-ttu-id="504cd-701">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-701">Driver'Licence</span></span>
- <span data-ttu-id="504cd-702">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-702">Driver'Licences</span></span>
- <span data-ttu-id="504cd-703">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-703">Driver' Lic</span></span>
- <span data-ttu-id="504cd-704">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-704">Driver' Lics</span></span>
- <span data-ttu-id="504cd-705">Driver' License</span><span class="sxs-lookup"><span data-stu-id="504cd-705">Driver' License</span></span>
- <span data-ttu-id="504cd-706">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-706">Driver' Licenses</span></span>
- <span data-ttu-id="504cd-707">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-707">Driver' Licence</span></span>
- <span data-ttu-id="504cd-708">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-708">Driver' Licences</span></span>
- <span data-ttu-id="504cd-709">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="504cd-709">Driver'sLic</span></span>
- <span data-ttu-id="504cd-710">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="504cd-710">Driver'sLics</span></span>
- <span data-ttu-id="504cd-711">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-711">Driver'sLicense</span></span>
- <span data-ttu-id="504cd-712">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-712">Driver'sLicenses</span></span>
- <span data-ttu-id="504cd-713">Дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="504cd-713">Driver'sLicence</span></span>
- <span data-ttu-id="504cd-714">Дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="504cd-714">Driver'sLicences</span></span>
- <span data-ttu-id="504cd-715">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-715">Driver's Lic</span></span>
- <span data-ttu-id="504cd-716">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-716">Driver's Lics</span></span>
- <span data-ttu-id="504cd-717">Driver's License</span><span class="sxs-lookup"><span data-stu-id="504cd-717">Driver's License</span></span>
- <span data-ttu-id="504cd-718">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-718">Driver's Licenses</span></span>
- <span data-ttu-id="504cd-719">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-719">Driver's Licence</span></span>
- <span data-ttu-id="504cd-720">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-720">Driver's Licences</span></span>
- <span data-ttu-id="504cd-721">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="504cd-721">Permis de Conduire</span></span>
- <span data-ttu-id="504cd-722">id</span><span class="sxs-lookup"><span data-stu-id="504cd-722">id</span></span>
- <span data-ttu-id="504cd-723">ids</span><span class="sxs-lookup"><span data-stu-id="504cd-723">ids</span></span>
- <span data-ttu-id="504cd-724">idcard number</span><span class="sxs-lookup"><span data-stu-id="504cd-724">idcard number</span></span>
- <span data-ttu-id="504cd-725">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-725">idcard numbers</span></span>
- <span data-ttu-id="504cd-726">idcard#</span><span class="sxs-lookup"><span data-stu-id="504cd-726">idcard #</span></span>
- <span data-ttu-id="504cd-727">idcard #s</span><span class="sxs-lookup"><span data-stu-id="504cd-727">idcard #s</span></span>
- <span data-ttu-id="504cd-728">idcard card</span><span class="sxs-lookup"><span data-stu-id="504cd-728">idcard card</span></span>
- <span data-ttu-id="504cd-729">idcard cards</span><span class="sxs-lookup"><span data-stu-id="504cd-729">idcard cards</span></span>
- <span data-ttu-id="504cd-730">идкард</span><span class="sxs-lookup"><span data-stu-id="504cd-730">idcard</span></span>
- <span data-ttu-id="504cd-731">identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-731">identification number</span></span>
- <span data-ttu-id="504cd-732">identification numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-732">identification numbers</span></span>
- <span data-ttu-id="504cd-733">identification #</span><span class="sxs-lookup"><span data-stu-id="504cd-733">identification #</span></span>
- <span data-ttu-id="504cd-734">identification #s</span><span class="sxs-lookup"><span data-stu-id="504cd-734">identification #s</span></span>
- <span data-ttu-id="504cd-735">identification card</span><span class="sxs-lookup"><span data-stu-id="504cd-735">identification card</span></span>
- <span data-ttu-id="504cd-736">identification cards</span><span class="sxs-lookup"><span data-stu-id="504cd-736">identification cards</span></span>
- <span data-ttu-id="504cd-737">процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-737">identification</span></span> 
- <span data-ttu-id="504cd-738">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-738">DL#</span></span>
- <span data-ttu-id="504cd-739">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="504cd-739">DLS#</span></span> 
- <span data-ttu-id="504cd-740">КДЛ #</span><span class="sxs-lookup"><span data-stu-id="504cd-740">CDL#</span></span> 
- <span data-ttu-id="504cd-741">КДЛС #</span><span class="sxs-lookup"><span data-stu-id="504cd-741">CDLS#</span></span> 
- <span data-ttu-id="504cd-742">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="504cd-742">DriverLic#</span></span> 
- <span data-ttu-id="504cd-743">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-743">DriverLics#</span></span> 
- <span data-ttu-id="504cd-744">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-744">DriverLicense#</span></span> 
- <span data-ttu-id="504cd-745">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-745">DriverLicenses#</span></span> 
- <span data-ttu-id="504cd-746">Дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="504cd-746">DriverLicence#</span></span> 
- <span data-ttu-id="504cd-747">Дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="504cd-747">DriverLicences#</span></span> 
- <span data-ttu-id="504cd-748">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-748">Driver Lic#</span></span>
- <span data-ttu-id="504cd-749">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-749">Driver Lics#</span></span> 
- <span data-ttu-id="504cd-750">Driver License#</span><span class="sxs-lookup"><span data-stu-id="504cd-750">Driver License#</span></span> 
- <span data-ttu-id="504cd-751">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-751">Driver Licenses#</span></span> 
- <span data-ttu-id="504cd-752">Driver License#</span><span class="sxs-lookup"><span data-stu-id="504cd-752">Driver License#</span></span> 
- <span data-ttu-id="504cd-753">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-753">Driver Licences#</span></span> 
- <span data-ttu-id="504cd-754">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="504cd-754">DriversLic#</span></span> 
- <span data-ttu-id="504cd-755">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-755">DriversLics#</span></span> 
- <span data-ttu-id="504cd-756">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-756">DriversLicense#</span></span> 
- <span data-ttu-id="504cd-757">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-757">DriversLicenses#</span></span> 
- <span data-ttu-id="504cd-758">Дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="504cd-758">DriversLicence#</span></span> 
- <span data-ttu-id="504cd-759">Дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="504cd-759">DriversLicences#</span></span> 
- <span data-ttu-id="504cd-760">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-760">Drivers Lic#</span></span> 
- <span data-ttu-id="504cd-761">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-761">Drivers Lics#</span></span> 
- <span data-ttu-id="504cd-762">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="504cd-762">Drivers License#</span></span> 
- <span data-ttu-id="504cd-763">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-763">Drivers Licenses#</span></span> 
- <span data-ttu-id="504cd-764">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-764">Drivers Licence#</span></span> 
- <span data-ttu-id="504cd-765">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-765">Drivers Licences#</span></span> 
- <span data-ttu-id="504cd-766">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="504cd-766">Driver'Lic#</span></span> 
- <span data-ttu-id="504cd-767">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="504cd-767">Driver'Lics#</span></span> 
- <span data-ttu-id="504cd-768">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="504cd-768">Driver'License#</span></span> 
- <span data-ttu-id="504cd-769">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-769">Driver'Licenses#</span></span> 
- <span data-ttu-id="504cd-770">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-770">Driver'Licence#</span></span> 
- <span data-ttu-id="504cd-771">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-771">Driver'Licences#</span></span> 
- <span data-ttu-id="504cd-772">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-772">Driver' Lic#</span></span> 
- <span data-ttu-id="504cd-773">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-773">Driver' Lics#</span></span> 
- <span data-ttu-id="504cd-774">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="504cd-774">Driver' License#</span></span> 
- <span data-ttu-id="504cd-775">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-775">Driver' Licenses#</span></span> 
- <span data-ttu-id="504cd-776">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-776">Driver' Licence#</span></span> 
- <span data-ttu-id="504cd-777">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-777">Driver' Licences#</span></span> 
- <span data-ttu-id="504cd-778">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="504cd-778">Driver'sLic#</span></span> 
- <span data-ttu-id="504cd-779">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-779">Driver'sLics#</span></span> 
- <span data-ttu-id="504cd-780">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-780">Driver'sLicense#</span></span> 
- <span data-ttu-id="504cd-781">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-781">Driver'sLicenses#</span></span> 
- <span data-ttu-id="504cd-782">Дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="504cd-782">Driver'sLicence#</span></span> 
- <span data-ttu-id="504cd-783">Дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="504cd-783">Driver'sLicences#</span></span> 
- <span data-ttu-id="504cd-784">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-784">Driver's Lic#</span></span> 
- <span data-ttu-id="504cd-785">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-785">Driver's Lics#</span></span> 
- <span data-ttu-id="504cd-786">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="504cd-786">Driver's License#</span></span> 
- <span data-ttu-id="504cd-787">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-787">Driver's Licenses#</span></span> 
- <span data-ttu-id="504cd-788">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="504cd-788">Driver's Licence#</span></span> 
- <span data-ttu-id="504cd-789">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="504cd-789">Driver's Licences#</span></span> 
- <span data-ttu-id="504cd-790">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="504cd-790">Permis de Conduire#</span></span> 
- <span data-ttu-id="504cd-791">кодов</span><span class="sxs-lookup"><span data-stu-id="504cd-791">id#</span></span> 
- <span data-ttu-id="504cd-792">идентификаторы</span><span class="sxs-lookup"><span data-stu-id="504cd-792">ids#</span></span> 
- <span data-ttu-id="504cd-793">idcard card#</span><span class="sxs-lookup"><span data-stu-id="504cd-793">idcard card#</span></span> 
- <span data-ttu-id="504cd-794">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="504cd-794">idcard cards#</span></span> 
- <span data-ttu-id="504cd-795">идкард #</span><span class="sxs-lookup"><span data-stu-id="504cd-795">idcard#</span></span> 
- <span data-ttu-id="504cd-796">identification card#</span><span class="sxs-lookup"><span data-stu-id="504cd-796">identification card#</span></span> 
- <span data-ttu-id="504cd-797">identification cards#</span><span class="sxs-lookup"><span data-stu-id="504cd-797">identification cards#</span></span> 
- <span data-ttu-id="504cd-798">процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-798">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="504cd-799">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="504cd-799">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-800">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-800">Format</span></span>

<span data-ttu-id="504cd-801">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-801">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-802">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-802">Pattern</span></span>

<span data-ttu-id="504cd-803">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-803">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-804">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-804">Checksum</span></span>

<span data-ttu-id="504cd-805">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-805">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-806">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-806">Definition</span></span>

<span data-ttu-id="504cd-807">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-807">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-808">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-808">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-809">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-809">A keyword from Keyword_canada_health_service_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-810">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-810">Keywords</span></span>

#### <a name="keywordcanadahealthservicenumber"></a><span data-ttu-id="504cd-811">Кэйворд_канада_хеалс_сервице_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-811">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="504cd-812">personal health number</span><span class="sxs-lookup"><span data-stu-id="504cd-812">personal health number</span></span>
- <span data-ttu-id="504cd-813">patient information</span><span class="sxs-lookup"><span data-stu-id="504cd-813">patient information</span></span>
- <span data-ttu-id="504cd-814">health services</span><span class="sxs-lookup"><span data-stu-id="504cd-814">health services</span></span>
- <span data-ttu-id="504cd-815">speciality services</span><span class="sxs-lookup"><span data-stu-id="504cd-815">speciality services</span></span>
- <span data-ttu-id="504cd-816">automobile accident</span><span class="sxs-lookup"><span data-stu-id="504cd-816">automobile accident</span></span>
- <span data-ttu-id="504cd-817">patient hospital</span><span class="sxs-lookup"><span data-stu-id="504cd-817">patient hospital</span></span>
- <span data-ttu-id="504cd-818">псичиатрист</span><span class="sxs-lookup"><span data-stu-id="504cd-818">psychiatrist</span></span>
- <span data-ttu-id="504cd-819">workers compensation</span><span class="sxs-lookup"><span data-stu-id="504cd-819">workers compensation</span></span>
- <span data-ttu-id="504cd-820">ограничен</span><span class="sxs-lookup"><span data-stu-id="504cd-820">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="504cd-821">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="504cd-821">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-822">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-822">Format</span></span>

<span data-ttu-id="504cd-823">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-823">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-824">Pattern</span></span>

<span data-ttu-id="504cd-825">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-825">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-826">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-826">Checksum</span></span>

<span data-ttu-id="504cd-827">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-827">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-828">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-828">Definition</span></span>

<span data-ttu-id="504cd-829">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-829">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-830">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-830">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-831">Найдено ключевое слово из Кэйворд_канада_пасспорт_нумбер или Кэйворд_пасспорт.</span><span class="sxs-lookup"><span data-stu-id="504cd-831">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-832">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-832">Keywords</span></span>

#### <a name="keywordcanadapassportnumber"></a><span data-ttu-id="504cd-833">Кэйворд_канада_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-833">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="504cd-834">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="504cd-834">canadian citizenship</span></span>
- <span data-ttu-id="504cd-835">canadian passport</span><span class="sxs-lookup"><span data-stu-id="504cd-835">canadian passport</span></span>
- <span data-ttu-id="504cd-836">passport application</span><span class="sxs-lookup"><span data-stu-id="504cd-836">passport application</span></span>
- <span data-ttu-id="504cd-837">passport photos</span><span class="sxs-lookup"><span data-stu-id="504cd-837">passport photos</span></span>
- <span data-ttu-id="504cd-838">certified translator</span><span class="sxs-lookup"><span data-stu-id="504cd-838">certified translator</span></span>
- <span data-ttu-id="504cd-839">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="504cd-839">canadian citizens</span></span>
- <span data-ttu-id="504cd-840">processing times</span><span class="sxs-lookup"><span data-stu-id="504cd-840">processing times</span></span>
- <span data-ttu-id="504cd-841">renewal application</span><span class="sxs-lookup"><span data-stu-id="504cd-841">renewal application</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="504cd-842">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-842">Keyword_passport</span></span>

- <span data-ttu-id="504cd-843">Passport Number</span><span class="sxs-lookup"><span data-stu-id="504cd-843">Passport Number</span></span>
- <span data-ttu-id="504cd-844">Passport No</span><span class="sxs-lookup"><span data-stu-id="504cd-844">Passport No</span></span>
- <span data-ttu-id="504cd-845">Passport#</span><span class="sxs-lookup"><span data-stu-id="504cd-845">Passport #</span></span>
- <span data-ttu-id="504cd-846">Службу</span><span class="sxs-lookup"><span data-stu-id="504cd-846">Passport#</span></span>
- <span data-ttu-id="504cd-847">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="504cd-847">PassportID</span></span>
- <span data-ttu-id="504cd-848">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="504cd-848">Passportno</span></span>
- <span data-ttu-id="504cd-849">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-849">passportnumber</span></span>
- <span data-ttu-id="504cd-850">パスポート</span><span class="sxs-lookup"><span data-stu-id="504cd-850">パスポート</span></span>
- <span data-ttu-id="504cd-851">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="504cd-851">パスポート番号</span></span>
- <span data-ttu-id="504cd-852">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="504cd-852">パスポートのNum</span></span>
- <span data-ttu-id="504cd-853">パスポート #</span><span class="sxs-lookup"><span data-stu-id="504cd-853">パスポート＃</span></span>
- <span data-ttu-id="504cd-854">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="504cd-854">Numéro de passeport</span></span>
- <span data-ttu-id="504cd-855">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="504cd-855">Passeport n °</span></span>
- <span data-ttu-id="504cd-856">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="504cd-856">Passeport Non</span></span>
- <span data-ttu-id="504cd-857">Passeport#</span><span class="sxs-lookup"><span data-stu-id="504cd-857">Passeport #</span></span>
- <span data-ttu-id="504cd-858">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="504cd-858">Passeport#</span></span>
- <span data-ttu-id="504cd-859">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="504cd-859">PasseportNon</span></span>
- <span data-ttu-id="504cd-860">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="504cd-860">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="504cd-861">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="504cd-861">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-862">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-862">Format</span></span>

<span data-ttu-id="504cd-863">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-863">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-864">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-864">Pattern</span></span>

<span data-ttu-id="504cd-865">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-865">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-866">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-866">Checksum</span></span>

<span data-ttu-id="504cd-867">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-867">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-868">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-868">Definition</span></span>

<span data-ttu-id="504cd-869">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_канада_фин находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-869">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-870">Найдены по крайней мере два ключевых слова от Кэйворд_канада_фин или Кэйворд_канада_провинцес.</span><span class="sxs-lookup"><span data-stu-id="504cd-870">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-871">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-871">Keywords</span></span>

#### <a name="keywordcanadaphin"></a><span data-ttu-id="504cd-872">Кэйворд_канада_фин</span><span class="sxs-lookup"><span data-stu-id="504cd-872">Keyword_canada_phin</span></span>

- <span data-ttu-id="504cd-873">social insurance number</span><span class="sxs-lookup"><span data-stu-id="504cd-873">social insurance number</span></span>
- <span data-ttu-id="504cd-874">health information act</span><span class="sxs-lookup"><span data-stu-id="504cd-874">health information act</span></span>
- <span data-ttu-id="504cd-875">income tax information</span><span class="sxs-lookup"><span data-stu-id="504cd-875">income tax information</span></span>
- <span data-ttu-id="504cd-876">manitoba health</span><span class="sxs-lookup"><span data-stu-id="504cd-876">manitoba health</span></span>
- <span data-ttu-id="504cd-877">health registration</span><span class="sxs-lookup"><span data-stu-id="504cd-877">health registration</span></span>
- <span data-ttu-id="504cd-878">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="504cd-878">prescription purchases</span></span>
- <span data-ttu-id="504cd-879">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="504cd-879">benefit eligibility</span></span>
- <span data-ttu-id="504cd-880">personal health</span><span class="sxs-lookup"><span data-stu-id="504cd-880">personal health</span></span>
- <span data-ttu-id="504cd-881">power of attorney</span><span class="sxs-lookup"><span data-stu-id="504cd-881">power of attorney</span></span>
- <span data-ttu-id="504cd-882">registration number</span><span class="sxs-lookup"><span data-stu-id="504cd-882">registration number</span></span>
- <span data-ttu-id="504cd-883">personal health number</span><span class="sxs-lookup"><span data-stu-id="504cd-883">personal health number</span></span>
- <span data-ttu-id="504cd-884">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="504cd-884">practitioner referral</span></span>
- <span data-ttu-id="504cd-885">wellness professional</span><span class="sxs-lookup"><span data-stu-id="504cd-885">wellness professional</span></span>
- <span data-ttu-id="504cd-886">patient referral</span><span class="sxs-lookup"><span data-stu-id="504cd-886">patient referral</span></span>
- <span data-ttu-id="504cd-887">health and wellness</span><span class="sxs-lookup"><span data-stu-id="504cd-887">health and wellness</span></span>

#### <a name="keywordcanadaprovinces"></a><span data-ttu-id="504cd-888">Кэйворд_канада_провинцес</span><span class="sxs-lookup"><span data-stu-id="504cd-888">Keyword_canada_provinces</span></span>

- <span data-ttu-id="504cd-889">Нунавут</span><span class="sxs-lookup"><span data-stu-id="504cd-889">Nunavut</span></span>
- <span data-ttu-id="504cd-890">Квебека</span><span class="sxs-lookup"><span data-stu-id="504cd-890">Quebec</span></span>
- <span data-ttu-id="504cd-891">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="504cd-891">Northwest Territories</span></span>
- <span data-ttu-id="504cd-892">Онтарио</span><span class="sxs-lookup"><span data-stu-id="504cd-892">Ontario</span></span>
- <span data-ttu-id="504cd-893">British Columbia</span><span class="sxs-lookup"><span data-stu-id="504cd-893">British Columbia</span></span>
- <span data-ttu-id="504cd-894">Альберта</span><span class="sxs-lookup"><span data-stu-id="504cd-894">Alberta</span></span>
- <span data-ttu-id="504cd-895">Саскачеван</span><span class="sxs-lookup"><span data-stu-id="504cd-895">Saskatchewan</span></span>
- <span data-ttu-id="504cd-896">Манитоба</span><span class="sxs-lookup"><span data-stu-id="504cd-896">Manitoba</span></span>
- <span data-ttu-id="504cd-897">Yukon</span><span class="sxs-lookup"><span data-stu-id="504cd-897">Yukon</span></span>
- <span data-ttu-id="504cd-898">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="504cd-898">Newfoundland and Labrador</span></span>
- <span data-ttu-id="504cd-899">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="504cd-899">New Brunswick</span></span>
- <span data-ttu-id="504cd-900">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="504cd-900">Nova Scotia</span></span>
- <span data-ttu-id="504cd-901">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="504cd-901">Prince Edward Island</span></span>
- <span data-ttu-id="504cd-902">Канада</span><span class="sxs-lookup"><span data-stu-id="504cd-902">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="504cd-903">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="504cd-903">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-904">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-904">Format</span></span>

<span data-ttu-id="504cd-905">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="504cd-905">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-906">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-906">Pattern</span></span>

<span data-ttu-id="504cd-907">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="504cd-907">Formatted:</span></span>
- <span data-ttu-id="504cd-908">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-908">Three digits</span></span> 
- <span data-ttu-id="504cd-909">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-909">A hyphen or space</span></span> 
- <span data-ttu-id="504cd-910">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-910">Three digits</span></span> 
- <span data-ttu-id="504cd-911">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-911">A hyphen or space</span></span> 
- <span data-ttu-id="504cd-912">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-912">Three digits</span></span>

<span data-ttu-id="504cd-913">Неформатированные: девять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-913">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-914">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-914">Checksum</span></span>

<span data-ttu-id="504cd-915">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-915">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-916">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-916">Definition</span></span>

<span data-ttu-id="504cd-917">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-917">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-918">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-918">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-919">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="504cd-919">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="504cd-920">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="504cd-920">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="504cd-921">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="504cd-921">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="504cd-922">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-922">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="504cd-923">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-923">The checksum passes.</span></span>

<span data-ttu-id="504cd-924">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-924">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-925">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-925">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-926">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="504cd-926">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="504cd-927">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-927">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-928">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-928">Keywords</span></span>

#### <a name="keywordsin"></a><span data-ttu-id="504cd-929">Кэйворд_син</span><span class="sxs-lookup"><span data-stu-id="504cd-929">Keyword_sin</span></span>

- <span data-ttu-id="504cd-930">sin</span><span class="sxs-lookup"><span data-stu-id="504cd-930">sin</span></span> 
- <span data-ttu-id="504cd-931">social insurance</span><span class="sxs-lookup"><span data-stu-id="504cd-931">social insurance</span></span> 
- <span data-ttu-id="504cd-932">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="504cd-932">numero d'assurance sociale</span></span> 
- <span data-ttu-id="504cd-933">грехов</span><span class="sxs-lookup"><span data-stu-id="504cd-933">sins</span></span> 
- <span data-ttu-id="504cd-934">SSN</span><span class="sxs-lookup"><span data-stu-id="504cd-934">ssn</span></span> 
- <span data-ttu-id="504cd-935">ssNS</span><span class="sxs-lookup"><span data-stu-id="504cd-935">ssns</span></span> 
- <span data-ttu-id="504cd-936">social security</span><span class="sxs-lookup"><span data-stu-id="504cd-936">social security</span></span> 
- <span data-ttu-id="504cd-937">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="504cd-937">numero d'assurance social</span></span> 
- <span data-ttu-id="504cd-938">national identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-938">national identification number</span></span> 
- <span data-ttu-id="504cd-939">national id</span><span class="sxs-lookup"><span data-stu-id="504cd-939">national id</span></span> 
- <span data-ttu-id="504cd-940">Синус</span><span class="sxs-lookup"><span data-stu-id="504cd-940">sin#</span></span> 
- <span data-ttu-id="504cd-941">soc ins</span><span class="sxs-lookup"><span data-stu-id="504cd-941">soc ins</span></span> 
- <span data-ttu-id="504cd-942">social ins</span><span class="sxs-lookup"><span data-stu-id="504cd-942">social ins</span></span> 

#### <a name="keywordsincollaborative"></a><span data-ttu-id="504cd-943">Кэйворд_син_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="504cd-943">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="504cd-944">driver's license</span><span class="sxs-lookup"><span data-stu-id="504cd-944">driver's license</span></span> 
- <span data-ttu-id="504cd-945">drivers license</span><span class="sxs-lookup"><span data-stu-id="504cd-945">drivers license</span></span> 
- <span data-ttu-id="504cd-946">driver's licence</span><span class="sxs-lookup"><span data-stu-id="504cd-946">driver's licence</span></span> 
- <span data-ttu-id="504cd-947">drivers licence</span><span class="sxs-lookup"><span data-stu-id="504cd-947">drivers licence</span></span> 
- <span data-ttu-id="504cd-948">ДОБ</span><span class="sxs-lookup"><span data-stu-id="504cd-948">DOB</span></span> 
- <span data-ttu-id="504cd-949">Birthdate</span><span class="sxs-lookup"><span data-stu-id="504cd-949">Birthdate</span></span> 
- <span data-ttu-id="504cd-950">День рождения</span><span class="sxs-lookup"><span data-stu-id="504cd-950">Birthday</span></span> 
- <span data-ttu-id="504cd-951">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="504cd-951">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="504cd-952">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="504cd-952">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-953">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-953">Format</span></span>

<span data-ttu-id="504cd-954">7-8 цифр и разделители — контрольная цифра или буква</span><span class="sxs-lookup"><span data-stu-id="504cd-954">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-955">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-955">Pattern</span></span>

<span data-ttu-id="504cd-956">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="504cd-956">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="504cd-957">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-957">1-2 digits</span></span> 
- <span data-ttu-id="504cd-958">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-958">A period</span></span> 
- <span data-ttu-id="504cd-959">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-959">Three digits</span></span> 
- <span data-ttu-id="504cd-960">точка;</span><span class="sxs-lookup"><span data-stu-id="504cd-960">A period</span></span> 
- <span data-ttu-id="504cd-961">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-961">Three digits</span></span> 
- <span data-ttu-id="504cd-962">тире;</span><span class="sxs-lookup"><span data-stu-id="504cd-962">A dash</span></span> 
- <span data-ttu-id="504cd-963">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-963">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-964">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-964">Checksum</span></span>

<span data-ttu-id="504cd-965">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-965">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-966">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-966">Definition</span></span>

<span data-ttu-id="504cd-967">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-967">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-968">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-968">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-969">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="504cd-969">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="504cd-970">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-970">The checksum passes.</span></span>

<span data-ttu-id="504cd-971">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-971">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-972">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-972">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-973">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-973">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-974">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-974">Keywords</span></span>

#### <a name="keywordchileidcard"></a><span data-ttu-id="504cd-975">Кэйворд_чиле_ид_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-975">Keyword_chile_id_card</span></span>

- <span data-ttu-id="504cd-976">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="504cd-976">National Identification Number</span></span> 
- <span data-ttu-id="504cd-977">Identity card</span><span class="sxs-lookup"><span data-stu-id="504cd-977">Identity card</span></span> 
- <span data-ttu-id="504cd-978">ИД</span><span class="sxs-lookup"><span data-stu-id="504cd-978">ID</span></span> 
- <span data-ttu-id="504cd-979">Процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-979">Identification</span></span> 
- <span data-ttu-id="504cd-980">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="504cd-980">Rol Único Nacional</span></span> 
- <span data-ttu-id="504cd-981">ВЫПОЛНЯЕМ</span><span class="sxs-lookup"><span data-stu-id="504cd-981">RUN</span></span> 
- <span data-ttu-id="504cd-982">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="504cd-982">Rol Único Tributario</span></span> 
- <span data-ttu-id="504cd-983">СНИЖАТЬСЯ</span><span class="sxs-lookup"><span data-stu-id="504cd-983">RUT</span></span> 
- <span data-ttu-id="504cd-984">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="504cd-984">Cédula de Identidad</span></span> 
- <span data-ttu-id="504cd-985">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="504cd-985">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="504cd-986">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="504cd-986">Tarjeta de identificación</span></span> 
- <span data-ttu-id="504cd-987">ИдентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="504cd-987">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="504cd-988">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="504cd-988">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-989">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-989">Format</span></span>

<span data-ttu-id="504cd-990">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-990">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-991">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-991">Pattern</span></span>

<span data-ttu-id="504cd-992">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-992">18 digits:</span></span>
- <span data-ttu-id="504cd-993">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="504cd-993">Six digits which are an address code</span></span> 
- <span data-ttu-id="504cd-994">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="504cd-994">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="504cd-995">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="504cd-995">Three digits which are an order code</span></span> 
- <span data-ttu-id="504cd-996">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-996">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-997">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-997">Checksum</span></span>

<span data-ttu-id="504cd-998">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-998">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-999">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-999">Definition</span></span>

<span data-ttu-id="504cd-1000">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1000">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1001">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1001">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1002">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="504cd-1002">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="504cd-1003">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1003">The checksum passes.</span></span>

<span data-ttu-id="504cd-1004">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1004">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1005">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1005">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1006">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1006">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1007">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1007">Keywords</span></span>

### <a name="keywordchinaresidentid"></a><span data-ttu-id="504cd-1008">Кэйворд_чина_ресидент_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-1008">Keyword_china_resident_id</span></span>

- <span data-ttu-id="504cd-1009">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="504cd-1009">Resident Identity Card</span></span> 
- <span data-ttu-id="504cd-1010">NO7</span><span class="sxs-lookup"><span data-stu-id="504cd-1010">PRC</span></span> 
- <span data-ttu-id="504cd-1011">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="504cd-1011">National Identification Card</span></span> 
- <span data-ttu-id="504cd-1012">身份证</span><span class="sxs-lookup"><span data-stu-id="504cd-1012">身份证</span></span> 
- <span data-ttu-id="504cd-1013">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="504cd-1013">居民 身份证</span></span> 
- <span data-ttu-id="504cd-1014">居民身份证</span><span class="sxs-lookup"><span data-stu-id="504cd-1014">居民身份证</span></span> 
- <span data-ttu-id="504cd-1015">鉴定</span><span class="sxs-lookup"><span data-stu-id="504cd-1015">鉴定</span></span> 
- <span data-ttu-id="504cd-1016">身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-1016">身分證</span></span> 
- <span data-ttu-id="504cd-1017">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-1017">居民 身份證</span></span>
- <span data-ttu-id="504cd-1018">鑑定</span><span class="sxs-lookup"><span data-stu-id="504cd-1018">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="504cd-1019">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="504cd-1019">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1020">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1020">Format</span></span>

<span data-ttu-id="504cd-1021">16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.</span><span class="sxs-lookup"><span data-stu-id="504cd-1021">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1022">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1022">Pattern</span></span>

<span data-ttu-id="504cd-1023">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="504cd-1023">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1024">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1024">Checksum</span></span>

<span data-ttu-id="504cd-1025">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="504cd-1025">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1026">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1026">Definition</span></span>

<span data-ttu-id="504cd-1027">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1027">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1028">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1028">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1029">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-1029">One of the following is true:</span></span>
    - <span data-ttu-id="504cd-1030">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="504cd-1030">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="504cd-1031">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="504cd-1031">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="504cd-1032">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-1032">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="504cd-1033">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1033">The checksum passes.</span></span>

<span data-ttu-id="504cd-1034">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1034">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1035">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1035">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1036">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1036">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1037">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1037">Keywords</span></span>

#### <a name="keywordccverification"></a><span data-ttu-id="504cd-1038">Кэйворд_кк_верификатион</span><span class="sxs-lookup"><span data-stu-id="504cd-1038">Keyword_cc_verification</span></span>

- <span data-ttu-id="504cd-1039">card verification</span><span class="sxs-lookup"><span data-stu-id="504cd-1039">card verification</span></span>
- <span data-ttu-id="504cd-1040">card identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-1040">card identification number</span></span>
- <span data-ttu-id="504cd-1041">КВН</span><span class="sxs-lookup"><span data-stu-id="504cd-1041">cvn</span></span>
- <span data-ttu-id="504cd-1042">cid</span><span class="sxs-lookup"><span data-stu-id="504cd-1042">cid</span></span>
- <span data-ttu-id="504cd-1043">CVC2</span><span class="sxs-lookup"><span data-stu-id="504cd-1043">cvc2</span></span>
- <span data-ttu-id="504cd-1044">CVV2</span><span class="sxs-lookup"><span data-stu-id="504cd-1044">cvv2</span></span>
- <span data-ttu-id="504cd-1045">pin block</span><span class="sxs-lookup"><span data-stu-id="504cd-1045">pin block</span></span>
- <span data-ttu-id="504cd-1046">security code</span><span class="sxs-lookup"><span data-stu-id="504cd-1046">security code</span></span>
- <span data-ttu-id="504cd-1047">security number</span><span class="sxs-lookup"><span data-stu-id="504cd-1047">security number</span></span>
- <span data-ttu-id="504cd-1048">security no</span><span class="sxs-lookup"><span data-stu-id="504cd-1048">security no</span></span>
- <span data-ttu-id="504cd-1049">issue number</span><span class="sxs-lookup"><span data-stu-id="504cd-1049">issue number</span></span>
- <span data-ttu-id="504cd-1050">issue no</span><span class="sxs-lookup"><span data-stu-id="504cd-1050">issue no</span></span>
- <span data-ttu-id="504cd-1051">криптограмме</span><span class="sxs-lookup"><span data-stu-id="504cd-1051">cryptogramme</span></span>
- <span data-ttu-id="504cd-1052">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="504cd-1052">numéro de sécurité</span></span>
- <span data-ttu-id="504cd-1053">numero de securite</span><span class="sxs-lookup"><span data-stu-id="504cd-1053">numero de securite</span></span>
- <span data-ttu-id="504cd-1054">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1054">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="504cd-1055">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1055">kreditkartenprufnummer</span></span>
- <span data-ttu-id="504cd-1056">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="504cd-1056">prüfziffer</span></span>
- <span data-ttu-id="504cd-1057">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="504cd-1057">prufziffer</span></span>
- <span data-ttu-id="504cd-1058">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="504cd-1058">sicherheits Kode</span></span>
- <span data-ttu-id="504cd-1059">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="504cd-1059">sicherheitscode</span></span>
- <span data-ttu-id="504cd-1060">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1060">sicherheitsnummer</span></span>
- <span data-ttu-id="504cd-1061">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1061">verfalldatum</span></span>
- <span data-ttu-id="504cd-1062">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="504cd-1062">codice di verifica</span></span>
- <span data-ttu-id="504cd-1063">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1063">cod.</span></span> <span data-ttu-id="504cd-1064">сикурезза</span><span class="sxs-lookup"><span data-stu-id="504cd-1064">sicurezza</span></span>
- <span data-ttu-id="504cd-1065">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="504cd-1065">cod sicurezza</span></span>
- <span data-ttu-id="504cd-1066">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="504cd-1066">n autorizzazione</span></span>
- <span data-ttu-id="504cd-1067">кóдиго</span><span class="sxs-lookup"><span data-stu-id="504cd-1067">código</span></span>
- <span data-ttu-id="504cd-1068">кодиго</span><span class="sxs-lookup"><span data-stu-id="504cd-1068">codigo</span></span>
- <span data-ttu-id="504cd-1069">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1069">cod.</span></span> <span data-ttu-id="504cd-1070">СЕГ</span><span class="sxs-lookup"><span data-stu-id="504cd-1070">seg</span></span>
- <span data-ttu-id="504cd-1071">cod seg</span><span class="sxs-lookup"><span data-stu-id="504cd-1071">cod seg</span></span>
- <span data-ttu-id="504cd-1072">código de segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1072">código de segurança</span></span>
- <span data-ttu-id="504cd-1073">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1073">codigo de seguranca</span></span>
- <span data-ttu-id="504cd-1074">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1074">codigo de segurança</span></span>
- <span data-ttu-id="504cd-1075">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1075">código de seguranca</span></span>
- <span data-ttu-id="504cd-1076">кóд.</span><span class="sxs-lookup"><span data-stu-id="504cd-1076">cód.</span></span> <span data-ttu-id="504cd-1077">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="504cd-1077">segurança</span></span>
- <span data-ttu-id="504cd-1078">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1078">cod.</span></span> <span data-ttu-id="504cd-1079">сегуранка наложенный платеж.</span><span class="sxs-lookup"><span data-stu-id="504cd-1079">seguranca cod.</span></span> <span data-ttu-id="504cd-1080">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="504cd-1080">segurança</span></span>
- <span data-ttu-id="504cd-1081">кóд.</span><span class="sxs-lookup"><span data-stu-id="504cd-1081">cód.</span></span> <span data-ttu-id="504cd-1082">сегуранка</span><span class="sxs-lookup"><span data-stu-id="504cd-1082">seguranca</span></span>
- <span data-ttu-id="504cd-1083">cód segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1083">cód segurança</span></span>
- <span data-ttu-id="504cd-1084">наложенный на наложенный сегуранка сегуранçа</span><span class="sxs-lookup"><span data-stu-id="504cd-1084">cod seguranca cod segurança</span></span>
- <span data-ttu-id="504cd-1085">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1085">cód seguranca</span></span>
- <span data-ttu-id="504cd-1086">número de verificação</span><span class="sxs-lookup"><span data-stu-id="504cd-1086">número de verificação</span></span>
- <span data-ttu-id="504cd-1087">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="504cd-1087">numero de verificacao</span></span>
- <span data-ttu-id="504cd-1088">аблауф</span><span class="sxs-lookup"><span data-stu-id="504cd-1088">ablauf</span></span>
- <span data-ttu-id="504cd-1089">gültig bis</span><span class="sxs-lookup"><span data-stu-id="504cd-1089">gültig bis</span></span>
- <span data-ttu-id="504cd-1090">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1090">gültigkeitsdatum</span></span>
- <span data-ttu-id="504cd-1091">gultig bis</span><span class="sxs-lookup"><span data-stu-id="504cd-1091">gultig bis</span></span>
- <span data-ttu-id="504cd-1092">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1092">gultigkeitsdatum</span></span>
- <span data-ttu-id="504cd-1093">скаденза</span><span class="sxs-lookup"><span data-stu-id="504cd-1093">scadenza</span></span>
- <span data-ttu-id="504cd-1094">data scad</span><span class="sxs-lookup"><span data-stu-id="504cd-1094">data scad</span></span>
- <span data-ttu-id="504cd-1095">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="504cd-1095">fecha de expiracion</span></span>
- <span data-ttu-id="504cd-1096">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="504cd-1096">fecha de venc</span></span>
- <span data-ttu-id="504cd-1097">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="504cd-1097">vencimiento</span></span>
- <span data-ttu-id="504cd-1098">válido hasta</span><span class="sxs-lookup"><span data-stu-id="504cd-1098">válido hasta</span></span>
- <span data-ttu-id="504cd-1099">valido hasta</span><span class="sxs-lookup"><span data-stu-id="504cd-1099">valido hasta</span></span>
- <span data-ttu-id="504cd-1100">ВТО</span><span class="sxs-lookup"><span data-stu-id="504cd-1100">vto</span></span>
- <span data-ttu-id="504cd-1101">data de expiração</span><span class="sxs-lookup"><span data-stu-id="504cd-1101">data de expiração</span></span>
- <span data-ttu-id="504cd-1102">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="504cd-1102">data de expiracao</span></span>
- <span data-ttu-id="504cd-1103">data em que expira</span><span class="sxs-lookup"><span data-stu-id="504cd-1103">data em que expira</span></span>
- <span data-ttu-id="504cd-1104">валидаде</span><span class="sxs-lookup"><span data-stu-id="504cd-1104">validade</span></span>
- <span data-ttu-id="504cd-1105">Валор</span><span class="sxs-lookup"><span data-stu-id="504cd-1105">valor</span></span>
- <span data-ttu-id="504cd-1106">венЦименто</span><span class="sxs-lookup"><span data-stu-id="504cd-1106">vencimento</span></span>
- <span data-ttu-id="504cd-1107">Венк</span><span class="sxs-lookup"><span data-stu-id="504cd-1107">Venc</span></span> 

#### <a name="keywordccname"></a><span data-ttu-id="504cd-1108">Кэйворд_кк_наме</span><span class="sxs-lookup"><span data-stu-id="504cd-1108">Keyword_cc_name</span></span>

- <span data-ttu-id="504cd-1109">АМЕКС</span><span class="sxs-lookup"><span data-stu-id="504cd-1109">amex</span></span>
- <span data-ttu-id="504cd-1110">american express</span><span class="sxs-lookup"><span data-stu-id="504cd-1110">american express</span></span>
- <span data-ttu-id="504cd-1111">американекспресс</span><span class="sxs-lookup"><span data-stu-id="504cd-1111">americanexpress</span></span>
- <span data-ttu-id="504cd-1112">Visa</span><span class="sxs-lookup"><span data-stu-id="504cd-1112">Visa</span></span>
- <span data-ttu-id="504cd-1113">MasterCard</span><span class="sxs-lookup"><span data-stu-id="504cd-1113">mastercard</span></span>
- <span data-ttu-id="504cd-1114">master card</span><span class="sxs-lookup"><span data-stu-id="504cd-1114">master card</span></span>
- <span data-ttu-id="504cd-1115">MC</span><span class="sxs-lookup"><span data-stu-id="504cd-1115">mc</span></span> 
- <span data-ttu-id="504cd-1116">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1116">mastercards</span></span>
- <span data-ttu-id="504cd-1117">master cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1117">master cards</span></span>
- <span data-ttu-id="504cd-1118">diner's Club</span><span class="sxs-lookup"><span data-stu-id="504cd-1118">diner's Club</span></span>
- <span data-ttu-id="504cd-1119">diners club</span><span class="sxs-lookup"><span data-stu-id="504cd-1119">diners club</span></span>
- <span data-ttu-id="504cd-1120">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="504cd-1120">dinersclub</span></span>
- <span data-ttu-id="504cd-1121">discover card</span><span class="sxs-lookup"><span data-stu-id="504cd-1121">discover card</span></span>
- <span data-ttu-id="504cd-1122">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="504cd-1122">discovercard</span></span>
- <span data-ttu-id="504cd-1123">discover cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1123">discover cards</span></span>
- <span data-ttu-id="504cd-1124">JCB</span><span class="sxs-lookup"><span data-stu-id="504cd-1124">JCB</span></span>
- <span data-ttu-id="504cd-1125">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="504cd-1125">japanese card bureau</span></span>
- <span data-ttu-id="504cd-1126">carte blanche</span><span class="sxs-lookup"><span data-stu-id="504cd-1126">carte blanche</span></span>
- <span data-ttu-id="504cd-1127">картебланче</span><span class="sxs-lookup"><span data-stu-id="504cd-1127">carteblanche</span></span>
- <span data-ttu-id="504cd-1128">credit card</span><span class="sxs-lookup"><span data-stu-id="504cd-1128">credit card</span></span>
- <span data-ttu-id="504cd-1129">Центральной</span><span class="sxs-lookup"><span data-stu-id="504cd-1129">cc#</span></span>
- <span data-ttu-id="504cd-1130">CC #:</span><span class="sxs-lookup"><span data-stu-id="504cd-1130">cc#:</span></span>
- <span data-ttu-id="504cd-1131">expiration date</span><span class="sxs-lookup"><span data-stu-id="504cd-1131">expiration date</span></span>
- <span data-ttu-id="504cd-1132">exp date</span><span class="sxs-lookup"><span data-stu-id="504cd-1132">exp date</span></span>
- <span data-ttu-id="504cd-1133">expiry date</span><span class="sxs-lookup"><span data-stu-id="504cd-1133">expiry date</span></span>
- <span data-ttu-id="504cd-1134">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="504cd-1134">date d’expiration</span></span>
- <span data-ttu-id="504cd-1135">date d'exp</span><span class="sxs-lookup"><span data-stu-id="504cd-1135">date d'exp</span></span>
- <span data-ttu-id="504cd-1136">date expiration</span><span class="sxs-lookup"><span data-stu-id="504cd-1136">date expiration</span></span>
- <span data-ttu-id="504cd-1137">bank card</span><span class="sxs-lookup"><span data-stu-id="504cd-1137">bank card</span></span>
- <span data-ttu-id="504cd-1138">банккард</span><span class="sxs-lookup"><span data-stu-id="504cd-1138">bankcard</span></span>
- <span data-ttu-id="504cd-1139">card number</span><span class="sxs-lookup"><span data-stu-id="504cd-1139">card number</span></span>
- <span data-ttu-id="504cd-1140">card num</span><span class="sxs-lookup"><span data-stu-id="504cd-1140">card num</span></span>
- <span data-ttu-id="504cd-1141">карднумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-1141">cardnumber</span></span>
- <span data-ttu-id="504cd-1142">карднумберс</span><span class="sxs-lookup"><span data-stu-id="504cd-1142">cardnumbers</span></span>
- <span data-ttu-id="504cd-1143">card numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-1143">card numbers</span></span>
- <span data-ttu-id="504cd-1144">кредиткард</span><span class="sxs-lookup"><span data-stu-id="504cd-1144">creditcard</span></span>
- <span data-ttu-id="504cd-1145">credit cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1145">credit cards</span></span>
- <span data-ttu-id="504cd-1146">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1146">creditcards</span></span>
- <span data-ttu-id="504cd-1147">CCN</span><span class="sxs-lookup"><span data-stu-id="504cd-1147">ccn</span></span>
- <span data-ttu-id="504cd-1148">card holder</span><span class="sxs-lookup"><span data-stu-id="504cd-1148">card holder</span></span>
- <span data-ttu-id="504cd-1149">банков</span><span class="sxs-lookup"><span data-stu-id="504cd-1149">cardholder</span></span>
- <span data-ttu-id="504cd-1150">card holders</span><span class="sxs-lookup"><span data-stu-id="504cd-1150">card holders</span></span>
- <span data-ttu-id="504cd-1151">карты</span><span class="sxs-lookup"><span data-stu-id="504cd-1151">cardholders</span></span>
- <span data-ttu-id="504cd-1152">check card</span><span class="sxs-lookup"><span data-stu-id="504cd-1152">check card</span></span>
- <span data-ttu-id="504cd-1153">чекккард</span><span class="sxs-lookup"><span data-stu-id="504cd-1153">checkcard</span></span>
- <span data-ttu-id="504cd-1154">check cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1154">check cards</span></span>
- <span data-ttu-id="504cd-1155">чекккардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1155">checkcards</span></span>
- <span data-ttu-id="504cd-1156">debit card</span><span class="sxs-lookup"><span data-stu-id="504cd-1156">debit card</span></span>
- <span data-ttu-id="504cd-1157">дебиткард</span><span class="sxs-lookup"><span data-stu-id="504cd-1157">debitcard</span></span>
- <span data-ttu-id="504cd-1158">debit cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1158">debit cards</span></span>
- <span data-ttu-id="504cd-1159">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1159">debitcards</span></span>
- <span data-ttu-id="504cd-1160">atm card</span><span class="sxs-lookup"><span data-stu-id="504cd-1160">atm card</span></span>
- <span data-ttu-id="504cd-1161">атмкард</span><span class="sxs-lookup"><span data-stu-id="504cd-1161">atmcard</span></span>
- <span data-ttu-id="504cd-1162">atm cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1162">atm cards</span></span>
- <span data-ttu-id="504cd-1163">атмкардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1163">atmcards</span></span>
- <span data-ttu-id="504cd-1164">енрауте</span><span class="sxs-lookup"><span data-stu-id="504cd-1164">enroute</span></span>
- <span data-ttu-id="504cd-1165">en route</span><span class="sxs-lookup"><span data-stu-id="504cd-1165">en route</span></span>
- <span data-ttu-id="504cd-1166">card type</span><span class="sxs-lookup"><span data-stu-id="504cd-1166">card type</span></span>
- <span data-ttu-id="504cd-1167">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="504cd-1167">carte bancaire</span></span>
- <span data-ttu-id="504cd-1168">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="504cd-1168">carte de crédit</span></span>
- <span data-ttu-id="504cd-1169">carte de credit</span><span class="sxs-lookup"><span data-stu-id="504cd-1169">carte de credit</span></span>
- <span data-ttu-id="504cd-1170">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1170">numéro de carte</span></span>
- <span data-ttu-id="504cd-1171">numero de carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1171">numero de carte</span></span>
- <span data-ttu-id="504cd-1172">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1172">nº de la carte</span></span>
- <span data-ttu-id="504cd-1173">nº de carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1173">nº de carte</span></span>
- <span data-ttu-id="504cd-1174">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="504cd-1174">kreditkarte</span></span>
- <span data-ttu-id="504cd-1175">карте</span><span class="sxs-lookup"><span data-stu-id="504cd-1175">karte</span></span>
- <span data-ttu-id="504cd-1176">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="504cd-1176">karteninhaber</span></span>
- <span data-ttu-id="504cd-1177">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="504cd-1177">karteninhabers</span></span>
- <span data-ttu-id="504cd-1178">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="504cd-1178">kreditkarteninhaber</span></span>
- <span data-ttu-id="504cd-1179">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="504cd-1179">kreditkarteninstitut</span></span>
- <span data-ttu-id="504cd-1180">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="504cd-1180">kreditkartentyp</span></span>
- <span data-ttu-id="504cd-1181">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="504cd-1181">eigentümername</span></span>
- <span data-ttu-id="504cd-1182">картеннр</span><span class="sxs-lookup"><span data-stu-id="504cd-1182">kartennr</span></span> 
- <span data-ttu-id="504cd-1183">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1183">kartennummer</span></span>
- <span data-ttu-id="504cd-1184">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1184">kreditkartennummer</span></span>
- <span data-ttu-id="504cd-1185">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1185">kreditkarten-nummer</span></span>
- <span data-ttu-id="504cd-1186">carta di credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1186">carta di credito</span></span>
- <span data-ttu-id="504cd-1187">carta credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1187">carta credito</span></span>
- <span data-ttu-id="504cd-1188">Корзина "</span><span class="sxs-lookup"><span data-stu-id="504cd-1188">carta</span></span>
- <span data-ttu-id="504cd-1189">n carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1189">n carta</span></span>
- <span data-ttu-id="504cd-1190">НР.</span><span class="sxs-lookup"><span data-stu-id="504cd-1190">nr.</span></span> <span data-ttu-id="504cd-1191">Корзина "</span><span class="sxs-lookup"><span data-stu-id="504cd-1191">carta</span></span>
- <span data-ttu-id="504cd-1192">nr carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1192">nr carta</span></span>
- <span data-ttu-id="504cd-1193">numero carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1193">numero carta</span></span>
- <span data-ttu-id="504cd-1194">numero della carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1194">numero della carta</span></span>
- <span data-ttu-id="504cd-1195">numero di carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1195">numero di carta</span></span>
- <span data-ttu-id="504cd-1196">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1196">tarjeta credito</span></span>
- <span data-ttu-id="504cd-1197">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1197">tarjeta de credito</span></span>
- <span data-ttu-id="504cd-1198">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="504cd-1198">tarjeta crédito</span></span>
- <span data-ttu-id="504cd-1199">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="504cd-1199">tarjeta de crédito</span></span>
- <span data-ttu-id="504cd-1200">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="504cd-1200">tarjeta de atm</span></span>
- <span data-ttu-id="504cd-1201">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="504cd-1201">tarjeta atm</span></span>
- <span data-ttu-id="504cd-1202">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1202">tarjeta debito</span></span>
- <span data-ttu-id="504cd-1203">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1203">tarjeta de debito</span></span>
- <span data-ttu-id="504cd-1204">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="504cd-1204">tarjeta débito</span></span>
- <span data-ttu-id="504cd-1205">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="504cd-1205">tarjeta de débito</span></span>
- <span data-ttu-id="504cd-1206">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1206">nº de tarjeta</span></span>
- <span data-ttu-id="504cd-1207">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1207">no.</span></span> <span data-ttu-id="504cd-1208">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1208">de tarjeta</span></span>
- <span data-ttu-id="504cd-1209">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1209">no de tarjeta</span></span>
- <span data-ttu-id="504cd-1210">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1210">numero de tarjeta</span></span>
- <span data-ttu-id="504cd-1211">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1211">número de tarjeta</span></span>
- <span data-ttu-id="504cd-1212">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="504cd-1212">tarjeta no</span></span>
- <span data-ttu-id="504cd-1213">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="504cd-1213">tarjetahabiente</span></span>
- <span data-ttu-id="504cd-1214">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="504cd-1214">cartão de crédito</span></span>
- <span data-ttu-id="504cd-1215">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1215">cartão de credito</span></span>
- <span data-ttu-id="504cd-1216">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="504cd-1216">cartao de crédito</span></span>
- <span data-ttu-id="504cd-1217">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1217">cartao de credito</span></span>
- <span data-ttu-id="504cd-1218">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="504cd-1218">cartão de débito</span></span>
- <span data-ttu-id="504cd-1219">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="504cd-1219">cartao de débito</span></span>
- <span data-ttu-id="504cd-1220">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1220">cartão de debito</span></span>
- <span data-ttu-id="504cd-1221">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1221">cartao de debito</span></span>
- <span data-ttu-id="504cd-1222">débito automático</span><span class="sxs-lookup"><span data-stu-id="504cd-1222">débito automático</span></span>
- <span data-ttu-id="504cd-1223">debito automatico</span><span class="sxs-lookup"><span data-stu-id="504cd-1223">debito automatico</span></span>
- <span data-ttu-id="504cd-1224">número do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1224">número do cartão</span></span>
- <span data-ttu-id="504cd-1225">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1225">numero do cartão</span></span> 
- <span data-ttu-id="504cd-1226">número do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1226">número do cartao</span></span>
- <span data-ttu-id="504cd-1227">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1227">numero do cartao</span></span>
- <span data-ttu-id="504cd-1228">número de cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1228">número de cartão</span></span>
- <span data-ttu-id="504cd-1229">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1229">numero de cartão</span></span>
- <span data-ttu-id="504cd-1230">número de cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1230">número de cartao</span></span>
- <span data-ttu-id="504cd-1231">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1231">numero de cartao</span></span>
- <span data-ttu-id="504cd-1232">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1232">nº do cartão</span></span>
- <span data-ttu-id="504cd-1233">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1233">nº do cartao</span></span>
- <span data-ttu-id="504cd-1234">n º.</span><span class="sxs-lookup"><span data-stu-id="504cd-1234">nº.</span></span> <span data-ttu-id="504cd-1235">do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1235">do cartão</span></span>
- <span data-ttu-id="504cd-1236">no do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1236">no do cartão</span></span>
- <span data-ttu-id="504cd-1237">no do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1237">no do cartao</span></span>
- <span data-ttu-id="504cd-1238">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1238">no.</span></span> <span data-ttu-id="504cd-1239">do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1239">do cartão</span></span>
- <span data-ttu-id="504cd-1240">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1240">no.</span></span> <span data-ttu-id="504cd-1241">do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1241">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="504cd-1242">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="504cd-1242">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1243">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1243">Format</span></span>

<span data-ttu-id="504cd-1244">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1244">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1245">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1245">Pattern</span></span>

<span data-ttu-id="504cd-1246">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1246">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1247">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1247">Checksum</span></span>

<span data-ttu-id="504cd-1248">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1248">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1249">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1249">Definition</span></span>

<span data-ttu-id="504cd-1250">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1251">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1251">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1252">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="504cd-1252">A keyword from Keyword_croatia_id_card is found.</span></span>

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1253">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1253">Keywords</span></span>

#### <a name="keywordcroatiaidcard"></a><span data-ttu-id="504cd-1254">Кэйворд_кроатиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-1254">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="504cd-1255">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="504cd-1255">Croatian identity card</span></span>
- <span data-ttu-id="504cd-1256">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="504cd-1256">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="504cd-1257">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="504cd-1257">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1258">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1258">Format</span></span>

<span data-ttu-id="504cd-1259">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1259">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1260">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1260">Pattern</span></span>

<span data-ttu-id="504cd-1261">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-1261">11 digits:</span></span>
- <span data-ttu-id="504cd-1262">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1262">10 digits</span></span> 
- <span data-ttu-id="504cd-1263">Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1263">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1264">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1264">Checksum</span></span>

<span data-ttu-id="504cd-1265">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1265">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1266">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1266">Definition</span></span>

<span data-ttu-id="504cd-1267">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1267">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1268">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1268">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1269">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-1269">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="504cd-1270">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1270">The checksum passes.</span></span>

<span data-ttu-id="504cd-1271">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1271">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1272">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1272">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1273">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1273">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1274">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1274">Keywords</span></span>

#### <a name="keywordcroatiaoibnumber"></a><span data-ttu-id="504cd-1275">Кэйворд_кроатиа_оиб_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-1275">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="504cd-1276">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="504cd-1276">Personal Identification Number</span></span>
- <span data-ttu-id="504cd-1277">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="504cd-1277">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="504cd-1278">OIB</span><span class="sxs-lookup"><span data-stu-id="504cd-1278">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="504cd-1279">Номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="504cd-1279">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1280">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1280">Format</span></span>

<span data-ttu-id="504cd-1281">Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)</span><span class="sxs-lookup"><span data-stu-id="504cd-1281">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1282">Pattern</span></span>

<span data-ttu-id="504cd-1283">Девять цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="504cd-1283">Nine digits (old format):</span></span>
- <span data-ttu-id="504cd-1284">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1284">Nine digits</span></span>

<span data-ttu-id="504cd-1285">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="504cd-1285">OR</span></span>

- <span data-ttu-id="504cd-1286">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="504cd-1286">Six digits that represent date of birth</span></span>
- <span data-ttu-id="504cd-1287">косая черта;</span><span class="sxs-lookup"><span data-stu-id="504cd-1287">A forward slash</span></span>
- <span data-ttu-id="504cd-1288">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-1288">Three digits</span></span>

<span data-ttu-id="504cd-1289">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="504cd-1289">10 digits (new format):</span></span>
- <span data-ttu-id="504cd-1290">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1290">10 digits</span></span>

<span data-ttu-id="504cd-1291">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="504cd-1291">OR</span></span>

- <span data-ttu-id="504cd-1292">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="504cd-1292">Six digits that represent date of birth</span></span>
- <span data-ttu-id="504cd-1293">косая черта;</span><span class="sxs-lookup"><span data-stu-id="504cd-1293">A forward slash</span></span> 
- <span data-ttu-id="504cd-1294">Четыре цифры, где последняя цифра является контрольной цифрой</span><span class="sxs-lookup"><span data-stu-id="504cd-1294">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1295">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1295">Checksum</span></span>

<span data-ttu-id="504cd-1296">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1296">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1297">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1297">Definition</span></span>

<span data-ttu-id="504cd-1298">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_кзеч_ид_кард находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1298">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-1299">находится ключевое слово из Keyword_czech_id_card;</span><span class="sxs-lookup"><span data-stu-id="504cd-1299">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="504cd-1300">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1300">The checksum passes.</span></span>

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="504cd-1301">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1301">Keywords</span></span>

- <span data-ttu-id="504cd-1302">номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="504cd-1302">czech personal identity number</span></span>
- <span data-ttu-id="504cd-1303">Роднé číсло</span><span class="sxs-lookup"><span data-stu-id="504cd-1303">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="504cd-1304">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="504cd-1304">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1305">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1305">Format</span></span>

<span data-ttu-id="504cd-1306">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="504cd-1306">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1307">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1307">Pattern</span></span>

<span data-ttu-id="504cd-1308">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-1308">10 digits:</span></span>
- <span data-ttu-id="504cd-1309">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="504cd-1309">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="504cd-1310">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-1310">A hyphen</span></span> 
- <span data-ttu-id="504cd-1311">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-1311">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1312">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1312">Checksum</span></span>

<span data-ttu-id="504cd-1313">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1314">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1314">Definition</span></span>

<span data-ttu-id="504cd-1315">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_денмарк_ид находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1315">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-1316">находится ключевое слово из Keyword_denmark_id;</span><span class="sxs-lookup"><span data-stu-id="504cd-1316">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="504cd-1317">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1317">The checksum passes.</span></span>

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1318">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1318">Keywords</span></span>

#### <a name="keyworddenmarkid"></a><span data-ttu-id="504cd-1319">Кэйворд_денмарк_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-1319">Keyword_denmark_id</span></span>

- <span data-ttu-id="504cd-1320">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="504cd-1320">Personal Identification Number</span></span>
- <span data-ttu-id="504cd-1321">CPR</span><span class="sxs-lookup"><span data-stu-id="504cd-1321">CPR</span></span>
- <span data-ttu-id="504cd-1322">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="504cd-1322">Det Centrale Personregister</span></span>
- <span data-ttu-id="504cd-1323">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1323">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="504cd-1324">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="504cd-1324">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1325">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1325">Format</span></span>

<span data-ttu-id="504cd-1326">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1326">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1327">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1327">Pattern</span></span>

<span data-ttu-id="504cd-1328">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="504cd-1328">Pattern must include all of the following:</span></span>
- <span data-ttu-id="504cd-1329">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="504cd-1329">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="504cd-1330">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="504cd-1330">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="504cd-1331">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="504cd-1331">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1332">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1332">Checksum</span></span>

<span data-ttu-id="504cd-1333">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1333">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1334">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1334">Definition</span></span>

<span data-ttu-id="504cd-1335">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1335">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1336">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1336">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1337">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1337">The checksum passes.</span></span>

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1338">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1338">Keywords</span></span>

<span data-ttu-id="504cd-1339">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1339">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="504cd-1340">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="504cd-1340">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1341">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1341">Format</span></span>

<span data-ttu-id="504cd-1342">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1342">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1343">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1343">Pattern</span></span>

<span data-ttu-id="504cd-1344">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="504cd-1344">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1345">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1345">Checksum</span></span>

<span data-ttu-id="504cd-1346">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1346">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1347">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1347">Definition</span></span>

<span data-ttu-id="504cd-1348">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1348">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1349">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1349">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1350">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-1350">At least one of the following is true:</span></span>
    - <span data-ttu-id="504cd-1351">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="504cd-1351">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="504cd-1352">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="504cd-1352">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="504cd-1353">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="504cd-1353">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="504cd-1354">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="504cd-1354">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="504cd-1355">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-1355">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="504cd-1356">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1356">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1357">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1357">Keywords</span></span>

#### <a name="keywordeudebitcard"></a><span data-ttu-id="504cd-1358">Кэйворд_еу_дебит_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-1358">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="504cd-1359">account number</span><span class="sxs-lookup"><span data-stu-id="504cd-1359">account number</span></span> 
- <span data-ttu-id="504cd-1360">card number</span><span class="sxs-lookup"><span data-stu-id="504cd-1360">card number</span></span> 
- <span data-ttu-id="504cd-1361">card no.</span><span class="sxs-lookup"><span data-stu-id="504cd-1361">card no.</span></span> 
- <span data-ttu-id="504cd-1362">security number</span><span class="sxs-lookup"><span data-stu-id="504cd-1362">security number</span></span> 
- <span data-ttu-id="504cd-1363">Центральной</span><span class="sxs-lookup"><span data-stu-id="504cd-1363">cc#</span></span> 

#### <a name="keywordcardtermsdict"></a><span data-ttu-id="504cd-1364">Кэйворд_кард_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="504cd-1364">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="504cd-1365">acct nbr</span><span class="sxs-lookup"><span data-stu-id="504cd-1365">acct nbr</span></span> 
- <span data-ttu-id="504cd-1366">acct num</span><span class="sxs-lookup"><span data-stu-id="504cd-1366">acct num</span></span> 
- <span data-ttu-id="504cd-1367">acct no</span><span class="sxs-lookup"><span data-stu-id="504cd-1367">acct no</span></span> 
- <span data-ttu-id="504cd-1368">american express</span><span class="sxs-lookup"><span data-stu-id="504cd-1368">american express</span></span> 
- <span data-ttu-id="504cd-1369">американекспресс</span><span class="sxs-lookup"><span data-stu-id="504cd-1369">americanexpress</span></span> 
- <span data-ttu-id="504cd-1370">americano espresso</span><span class="sxs-lookup"><span data-stu-id="504cd-1370">americano espresso</span></span> 
- <span data-ttu-id="504cd-1371">АМЕКС</span><span class="sxs-lookup"><span data-stu-id="504cd-1371">amex</span></span> 
- <span data-ttu-id="504cd-1372">atm card</span><span class="sxs-lookup"><span data-stu-id="504cd-1372">atm card</span></span> 
- <span data-ttu-id="504cd-1373">atm cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1373">atm cards</span></span> 
- <span data-ttu-id="504cd-1374">atm kaart</span><span class="sxs-lookup"><span data-stu-id="504cd-1374">atm kaart</span></span> 
- <span data-ttu-id="504cd-1375">атмкард</span><span class="sxs-lookup"><span data-stu-id="504cd-1375">atmcard</span></span> 
- <span data-ttu-id="504cd-1376">атмкардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1376">atmcards</span></span> 
- <span data-ttu-id="504cd-1377">атмкаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1377">atmkaart</span></span> 
- <span data-ttu-id="504cd-1378">атмкаартен</span><span class="sxs-lookup"><span data-stu-id="504cd-1378">atmkaarten</span></span> 
- <span data-ttu-id="504cd-1379">банконтакт</span><span class="sxs-lookup"><span data-stu-id="504cd-1379">bancontact</span></span> 
- <span data-ttu-id="504cd-1380">bank card</span><span class="sxs-lookup"><span data-stu-id="504cd-1380">bank card</span></span> 
- <span data-ttu-id="504cd-1381">банккаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1381">bankkaart</span></span> 
- <span data-ttu-id="504cd-1382">card holder</span><span class="sxs-lookup"><span data-stu-id="504cd-1382">card holder</span></span> 
- <span data-ttu-id="504cd-1383">card holders</span><span class="sxs-lookup"><span data-stu-id="504cd-1383">card holders</span></span> 
- <span data-ttu-id="504cd-1384">card num</span><span class="sxs-lookup"><span data-stu-id="504cd-1384">card num</span></span> 
- <span data-ttu-id="504cd-1385">card number</span><span class="sxs-lookup"><span data-stu-id="504cd-1385">card number</span></span> 
- <span data-ttu-id="504cd-1386">card numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-1386">card numbers</span></span> 
- <span data-ttu-id="504cd-1387">card type</span><span class="sxs-lookup"><span data-stu-id="504cd-1387">card type</span></span> 
- <span data-ttu-id="504cd-1388">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="504cd-1388">cardano numerico</span></span> 
- <span data-ttu-id="504cd-1389">банков</span><span class="sxs-lookup"><span data-stu-id="504cd-1389">cardholder</span></span> 
- <span data-ttu-id="504cd-1390">карты</span><span class="sxs-lookup"><span data-stu-id="504cd-1390">cardholders</span></span> 
- <span data-ttu-id="504cd-1391">карднумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-1391">cardnumber</span></span> 
- <span data-ttu-id="504cd-1392">карднумберс</span><span class="sxs-lookup"><span data-stu-id="504cd-1392">cardnumbers</span></span> 
- <span data-ttu-id="504cd-1393">carta bianca</span><span class="sxs-lookup"><span data-stu-id="504cd-1393">carta bianca</span></span> 
- <span data-ttu-id="504cd-1394">carta credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1394">carta credito</span></span> 
- <span data-ttu-id="504cd-1395">carta di credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1395">carta di credito</span></span> 
- <span data-ttu-id="504cd-1396">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1396">cartao de credito</span></span> 
- <span data-ttu-id="504cd-1397">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="504cd-1397">cartao de crédito</span></span> 
- <span data-ttu-id="504cd-1398">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1398">cartao de debito</span></span> 
- <span data-ttu-id="504cd-1399">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="504cd-1399">cartao de débito</span></span> 
- <span data-ttu-id="504cd-1400">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="504cd-1400">carte bancaire</span></span> 
- <span data-ttu-id="504cd-1401">carte blanche</span><span class="sxs-lookup"><span data-stu-id="504cd-1401">carte blanche</span></span> 
- <span data-ttu-id="504cd-1402">carte bleue</span><span class="sxs-lookup"><span data-stu-id="504cd-1402">carte bleue</span></span> 
- <span data-ttu-id="504cd-1403">carte de credit</span><span class="sxs-lookup"><span data-stu-id="504cd-1403">carte de credit</span></span> 
- <span data-ttu-id="504cd-1404">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="504cd-1404">carte de crédit</span></span> 
- <span data-ttu-id="504cd-1405">carte di credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1405">carte di credito</span></span> 
- <span data-ttu-id="504cd-1406">картебланче</span><span class="sxs-lookup"><span data-stu-id="504cd-1406">carteblanche</span></span> 
- <span data-ttu-id="504cd-1407">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1407">cartão de credito</span></span> 
- <span data-ttu-id="504cd-1408">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="504cd-1408">cartão de crédito</span></span> 
- <span data-ttu-id="504cd-1409">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1409">cartão de debito</span></span> 
- <span data-ttu-id="504cd-1410">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="504cd-1410">cartão de débito</span></span> 
- <span data-ttu-id="504cd-1411">cb</span><span class="sxs-lookup"><span data-stu-id="504cd-1411">cb</span></span> 
- <span data-ttu-id="504cd-1412">CCN</span><span class="sxs-lookup"><span data-stu-id="504cd-1412">ccn</span></span> 
- <span data-ttu-id="504cd-1413">check card</span><span class="sxs-lookup"><span data-stu-id="504cd-1413">check card</span></span> 
- <span data-ttu-id="504cd-1414">check cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1414">check cards</span></span> 
- <span data-ttu-id="504cd-1415">чекккард</span><span class="sxs-lookup"><span data-stu-id="504cd-1415">checkcard</span></span>
- <span data-ttu-id="504cd-1416">чекккардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1416">checkcards</span></span> 
- <span data-ttu-id="504cd-1417">чекуекаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1417">chequekaart</span></span> 
- <span data-ttu-id="504cd-1418">Logic</span><span class="sxs-lookup"><span data-stu-id="504cd-1418">cirrus</span></span> 
- <span data-ttu-id="504cd-1419">Cirrus центр EDC — Маестро</span><span class="sxs-lookup"><span data-stu-id="504cd-1419">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="504cd-1420">контролекаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1420">controlekaart</span></span> 
- <span data-ttu-id="504cd-1421">контролекаартен</span><span class="sxs-lookup"><span data-stu-id="504cd-1421">controlekaarten</span></span> 
- <span data-ttu-id="504cd-1422">credit card</span><span class="sxs-lookup"><span data-stu-id="504cd-1422">credit card</span></span> 
- <span data-ttu-id="504cd-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1423">credit cards</span></span> 
- <span data-ttu-id="504cd-1424">кредиткард</span><span class="sxs-lookup"><span data-stu-id="504cd-1424">creditcard</span></span> 
- <span data-ttu-id="504cd-1425">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1425">creditcards</span></span> 
- <span data-ttu-id="504cd-1426">дебеткаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1426">debetkaart</span></span> 
- <span data-ttu-id="504cd-1427">дебеткаартен</span><span class="sxs-lookup"><span data-stu-id="504cd-1427">debetkaarten</span></span> 
- <span data-ttu-id="504cd-1428">debit card</span><span class="sxs-lookup"><span data-stu-id="504cd-1428">debit card</span></span> 
- <span data-ttu-id="504cd-1429">debit cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1429">debit cards</span></span> 
- <span data-ttu-id="504cd-1430">дебиткард</span><span class="sxs-lookup"><span data-stu-id="504cd-1430">debitcard</span></span> 
- <span data-ttu-id="504cd-1431">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1431">debitcards</span></span> 
- <span data-ttu-id="504cd-1432">debito automatico</span><span class="sxs-lookup"><span data-stu-id="504cd-1432">debito automatico</span></span> 
- <span data-ttu-id="504cd-1433">diners club</span><span class="sxs-lookup"><span data-stu-id="504cd-1433">diners club</span></span> 
- <span data-ttu-id="504cd-1434">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="504cd-1434">dinersclub</span></span> 
- <span data-ttu-id="504cd-1435">Повтор</span><span class="sxs-lookup"><span data-stu-id="504cd-1435">discover</span></span> 
- <span data-ttu-id="504cd-1436">discover card</span><span class="sxs-lookup"><span data-stu-id="504cd-1436">discover card</span></span> 
- <span data-ttu-id="504cd-1437">discover cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1437">discover cards</span></span> 
- <span data-ttu-id="504cd-1438">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="504cd-1438">discovercard</span></span> 
- <span data-ttu-id="504cd-1439">дисковеркардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1439">discovercards</span></span> 
- <span data-ttu-id="504cd-1440">débito automático</span><span class="sxs-lookup"><span data-stu-id="504cd-1440">débito automático</span></span>
- <span data-ttu-id="504cd-1441">центр EDC</span><span class="sxs-lookup"><span data-stu-id="504cd-1441">edc</span></span> 
- <span data-ttu-id="504cd-1442">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="504cd-1442">eigentümername</span></span> 
- <span data-ttu-id="504cd-1443">european debit card</span><span class="sxs-lookup"><span data-stu-id="504cd-1443">european debit card</span></span> 
- <span data-ttu-id="504cd-1444">хуфдкаарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1444">hoofdkaart</span></span> 
- <span data-ttu-id="504cd-1445">хуфдкаартен</span><span class="sxs-lookup"><span data-stu-id="504cd-1445">hoofdkaarten</span></span> 
- <span data-ttu-id="504cd-1446">in viaggio</span><span class="sxs-lookup"><span data-stu-id="504cd-1446">in viaggio</span></span> 
- <span data-ttu-id="504cd-1447">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="504cd-1447">japanese card bureau</span></span> 
- <span data-ttu-id="504cd-1448">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="504cd-1448">japanse kaartdienst</span></span> 
- <span data-ttu-id="504cd-1449">JCB</span><span class="sxs-lookup"><span data-stu-id="504cd-1449">jcb</span></span> 
- <span data-ttu-id="504cd-1450">каарт</span><span class="sxs-lookup"><span data-stu-id="504cd-1450">kaart</span></span> 
- <span data-ttu-id="504cd-1451">kaart num</span><span class="sxs-lookup"><span data-stu-id="504cd-1451">kaart num</span></span> 
- <span data-ttu-id="504cd-1452">каартаантал</span><span class="sxs-lookup"><span data-stu-id="504cd-1452">kaartaantal</span></span> 
- <span data-ttu-id="504cd-1453">каартаанталлен</span><span class="sxs-lookup"><span data-stu-id="504cd-1453">kaartaantallen</span></span> 
- <span data-ttu-id="504cd-1454">каарсаудер</span><span class="sxs-lookup"><span data-stu-id="504cd-1454">kaarthouder</span></span> 
- <span data-ttu-id="504cd-1455">каарсаудерс</span><span class="sxs-lookup"><span data-stu-id="504cd-1455">kaarthouders</span></span> 
- <span data-ttu-id="504cd-1456">карте</span><span class="sxs-lookup"><span data-stu-id="504cd-1456">karte</span></span>  
- <span data-ttu-id="504cd-1457">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="504cd-1457">karteninhaber</span></span> 
- <span data-ttu-id="504cd-1458">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="504cd-1458">karteninhabers</span></span>
- <span data-ttu-id="504cd-1459">картеннр</span><span class="sxs-lookup"><span data-stu-id="504cd-1459">kartennr</span></span> 
- <span data-ttu-id="504cd-1460">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1460">kartennummer</span></span> 
- <span data-ttu-id="504cd-1461">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="504cd-1461">kreditkarte</span></span> 
- <span data-ttu-id="504cd-1462">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1462">kreditkarten-nummer</span></span> 
- <span data-ttu-id="504cd-1463">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="504cd-1463">kreditkarteninhaber</span></span> 
- <span data-ttu-id="504cd-1464">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="504cd-1464">kreditkarteninstitut</span></span> 
- <span data-ttu-id="504cd-1465">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1465">kreditkartennummer</span></span> 
- <span data-ttu-id="504cd-1466">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="504cd-1466">kreditkartentyp</span></span> 
- <span data-ttu-id="504cd-1467">Маестро</span><span class="sxs-lookup"><span data-stu-id="504cd-1467">maestro</span></span> 
- <span data-ttu-id="504cd-1468">master card</span><span class="sxs-lookup"><span data-stu-id="504cd-1468">master card</span></span> 
- <span data-ttu-id="504cd-1469">master cards</span><span class="sxs-lookup"><span data-stu-id="504cd-1469">master cards</span></span> 
- <span data-ttu-id="504cd-1470">MasterCard</span><span class="sxs-lookup"><span data-stu-id="504cd-1470">mastercard</span></span> 
- <span data-ttu-id="504cd-1471">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="504cd-1471">mastercards</span></span> 
- <span data-ttu-id="504cd-1472">MC</span><span class="sxs-lookup"><span data-stu-id="504cd-1472">mc</span></span> 
- <span data-ttu-id="504cd-1473">mister cash</span><span class="sxs-lookup"><span data-stu-id="504cd-1473">mister cash</span></span> 
- <span data-ttu-id="504cd-1474">n carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1474">n carta</span></span> 
- <span data-ttu-id="504cd-1475">Корзина "</span><span class="sxs-lookup"><span data-stu-id="504cd-1475">carta</span></span> 
- <span data-ttu-id="504cd-1476">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1476">no de tarjeta</span></span> 
- <span data-ttu-id="504cd-1477">no do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1477">no do cartao</span></span> 
- <span data-ttu-id="504cd-1478">no do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1478">no do cartão</span></span> 
- <span data-ttu-id="504cd-1479">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1479">no.</span></span> <span data-ttu-id="504cd-1480">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1480">de tarjeta</span></span> 
- <span data-ttu-id="504cd-1481">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1481">no.</span></span> <span data-ttu-id="504cd-1482">do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1482">do cartao</span></span> 
- <span data-ttu-id="504cd-1483">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1483">no.</span></span> <span data-ttu-id="504cd-1484">do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1484">do cartão</span></span> 
- <span data-ttu-id="504cd-1485">nr carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1485">nr carta</span></span> 
- <span data-ttu-id="504cd-1486">НР.</span><span class="sxs-lookup"><span data-stu-id="504cd-1486">nr.</span></span> <span data-ttu-id="504cd-1487">Корзина "</span><span class="sxs-lookup"><span data-stu-id="504cd-1487">carta</span></span> 
- <span data-ttu-id="504cd-1488">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="504cd-1488">numeri di scheda</span></span> 
- <span data-ttu-id="504cd-1489">numero carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1489">numero carta</span></span> 
- <span data-ttu-id="504cd-1490">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1490">numero de cartao</span></span> 
- <span data-ttu-id="504cd-1491">numero de carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1491">numero de carte</span></span> 
- <span data-ttu-id="504cd-1492">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1492">numero de cartão</span></span> 
- <span data-ttu-id="504cd-1493">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1493">numero de tarjeta</span></span>
- <span data-ttu-id="504cd-1494">numero della carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1494">numero della carta</span></span> 
- <span data-ttu-id="504cd-1495">numero di carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1495">numero di carta</span></span> 
- <span data-ttu-id="504cd-1496">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="504cd-1496">numero di scheda</span></span> 
- <span data-ttu-id="504cd-1497">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1497">numero do cartao</span></span> 
- <span data-ttu-id="504cd-1498">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1498">numero do cartão</span></span> 
- <span data-ttu-id="504cd-1499">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1499">numéro de carte</span></span> 
- <span data-ttu-id="504cd-1500">nº carta</span><span class="sxs-lookup"><span data-stu-id="504cd-1500">nº carta</span></span> 
- <span data-ttu-id="504cd-1501">nº de carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1501">nº de carte</span></span> 
- <span data-ttu-id="504cd-1502">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="504cd-1502">nº de la carte</span></span> 
- <span data-ttu-id="504cd-1503">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1503">nº de tarjeta</span></span> 
- <span data-ttu-id="504cd-1504">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1504">nº do cartao</span></span> 
- <span data-ttu-id="504cd-1505">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1505">nº do cartão</span></span> 
- <span data-ttu-id="504cd-1506">n º.</span><span class="sxs-lookup"><span data-stu-id="504cd-1506">nº.</span></span> <span data-ttu-id="504cd-1507">do cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1507">do cartão</span></span> 
- <span data-ttu-id="504cd-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1508">número de cartao</span></span> 
- <span data-ttu-id="504cd-1509">número de cartão</span><span class="sxs-lookup"><span data-stu-id="504cd-1509">número de cartão</span></span> 
- <span data-ttu-id="504cd-1510">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="504cd-1510">número de tarjeta</span></span> 
- <span data-ttu-id="504cd-1511">número do cartao</span><span class="sxs-lookup"><span data-stu-id="504cd-1511">número do cartao</span></span> 
- <span data-ttu-id="504cd-1512">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="504cd-1512">scheda dell'assegno</span></span> 
- <span data-ttu-id="504cd-1513">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="504cd-1513">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="504cd-1514">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="504cd-1514">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="504cd-1515">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="504cd-1515">scheda della banca</span></span> 
- <span data-ttu-id="504cd-1516">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="504cd-1516">scheda di controllo</span></span> 
- <span data-ttu-id="504cd-1517">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1517">scheda di debito</span></span> 
- <span data-ttu-id="504cd-1518">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="504cd-1518">scheda matrice</span></span> 
- <span data-ttu-id="504cd-1519">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="504cd-1519">schede dell'atmosfera</span></span> 
- <span data-ttu-id="504cd-1520">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="504cd-1520">schede di controllo</span></span> 
- <span data-ttu-id="504cd-1521">schede di debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1521">schede di debito</span></span> 
- <span data-ttu-id="504cd-1522">schede matrici</span><span class="sxs-lookup"><span data-stu-id="504cd-1522">schede matrici</span></span> 
- <span data-ttu-id="504cd-1523">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="504cd-1523">scoprono la scheda</span></span> 
- <span data-ttu-id="504cd-1524">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="504cd-1524">scoprono le schede</span></span> 
- <span data-ttu-id="504cd-1525">ОС</span><span class="sxs-lookup"><span data-stu-id="504cd-1525">solo</span></span> 
- <span data-ttu-id="504cd-1526">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="504cd-1526">supporti di scheda</span></span> 
- <span data-ttu-id="504cd-1527">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="504cd-1527">supporto di scheda</span></span> 
- <span data-ttu-id="504cd-1528">отключен</span><span class="sxs-lookup"><span data-stu-id="504cd-1528">switch</span></span> 
- <span data-ttu-id="504cd-1529">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="504cd-1529">tarjeta atm</span></span> 
- <span data-ttu-id="504cd-1530">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1530">tarjeta credito</span></span> 
- <span data-ttu-id="504cd-1531">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="504cd-1531">tarjeta de atm</span></span> 
- <span data-ttu-id="504cd-1532">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="504cd-1532">tarjeta de credito</span></span> 
- <span data-ttu-id="504cd-1533">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1533">tarjeta de debito</span></span> 
- <span data-ttu-id="504cd-1534">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="504cd-1534">tarjeta debito</span></span> 
- <span data-ttu-id="504cd-1535">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="504cd-1535">tarjeta no</span></span>
- <span data-ttu-id="504cd-1536">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="504cd-1536">tarjetahabiente</span></span> 
- <span data-ttu-id="504cd-1537">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="504cd-1537">tipo della scheda</span></span> 
- <span data-ttu-id="504cd-1538">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="504cd-1538">ufficio giapponese della</span></span> 
- <span data-ttu-id="504cd-1539">счеда</span><span class="sxs-lookup"><span data-stu-id="504cd-1539">scheda</span></span> 
- <span data-ttu-id="504cd-1540">v pay</span><span class="sxs-lookup"><span data-stu-id="504cd-1540">v pay</span></span> 
- <span data-ttu-id="504cd-1541">v — оплата</span><span class="sxs-lookup"><span data-stu-id="504cd-1541">v-pay</span></span> 
- <span data-ttu-id="504cd-1542">Visa</span><span class="sxs-lookup"><span data-stu-id="504cd-1542">visa</span></span> 
- <span data-ttu-id="504cd-1543">visa plus</span><span class="sxs-lookup"><span data-stu-id="504cd-1543">visa plus</span></span> 
- <span data-ttu-id="504cd-1544">visa electron</span><span class="sxs-lookup"><span data-stu-id="504cd-1544">visa electron</span></span> 
- <span data-ttu-id="504cd-1545">висто</span><span class="sxs-lookup"><span data-stu-id="504cd-1545">visto</span></span> 
- <span data-ttu-id="504cd-1546">висум</span><span class="sxs-lookup"><span data-stu-id="504cd-1546">visum</span></span> 
- <span data-ttu-id="504cd-1547">впай</span><span class="sxs-lookup"><span data-stu-id="504cd-1547">vpay</span></span>   

#### <a name="keywordcardsecuritytermsdict"></a><span data-ttu-id="504cd-1548">Кэйворд_кард_секурити_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="504cd-1548">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="504cd-1549">card identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-1549">card identification number</span></span>
- <span data-ttu-id="504cd-1550">card verification</span><span class="sxs-lookup"><span data-stu-id="504cd-1550">card verification</span></span> 
- <span data-ttu-id="504cd-1551">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="504cd-1551">cardi la verifica</span></span> 
- <span data-ttu-id="504cd-1552">cid</span><span class="sxs-lookup"><span data-stu-id="504cd-1552">cid</span></span> 
- <span data-ttu-id="504cd-1553">cod seg</span><span class="sxs-lookup"><span data-stu-id="504cd-1553">cod seg</span></span> 
- <span data-ttu-id="504cd-1554">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1554">cod seguranca</span></span> 
- <span data-ttu-id="504cd-1555">cod segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1555">cod segurança</span></span> 
- <span data-ttu-id="504cd-1556">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="504cd-1556">cod sicurezza</span></span> 
- <span data-ttu-id="504cd-1557">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1557">cod.</span></span> <span data-ttu-id="504cd-1558">СЕГ</span><span class="sxs-lookup"><span data-stu-id="504cd-1558">seg</span></span> 
- <span data-ttu-id="504cd-1559">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1559">cod.</span></span> <span data-ttu-id="504cd-1560">сегуранка</span><span class="sxs-lookup"><span data-stu-id="504cd-1560">seguranca</span></span> 
- <span data-ttu-id="504cd-1561">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1561">cod.</span></span> <span data-ttu-id="504cd-1562">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="504cd-1562">segurança</span></span> 
- <span data-ttu-id="504cd-1563">наложен.</span><span class="sxs-lookup"><span data-stu-id="504cd-1563">cod.</span></span> <span data-ttu-id="504cd-1564">сикурезза</span><span class="sxs-lookup"><span data-stu-id="504cd-1564">sicurezza</span></span> 
- <span data-ttu-id="504cd-1565">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="504cd-1565">codice di sicurezza</span></span> 
- <span data-ttu-id="504cd-1566">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="504cd-1566">codice di verifica</span></span> 
- <span data-ttu-id="504cd-1567">кодиго</span><span class="sxs-lookup"><span data-stu-id="504cd-1567">codigo</span></span> 
- <span data-ttu-id="504cd-1568">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1568">codigo de seguranca</span></span> 
- <span data-ttu-id="504cd-1569">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1569">codigo de segurança</span></span> 
- <span data-ttu-id="504cd-1570">криттограмма</span><span class="sxs-lookup"><span data-stu-id="504cd-1570">crittogramma</span></span> 
- <span data-ttu-id="504cd-1571">криптограм</span><span class="sxs-lookup"><span data-stu-id="504cd-1571">cryptogram</span></span> 
- <span data-ttu-id="504cd-1572">криптограмме</span><span class="sxs-lookup"><span data-stu-id="504cd-1572">cryptogramme</span></span> 
- <span data-ttu-id="504cd-1573">CV2</span><span class="sxs-lookup"><span data-stu-id="504cd-1573">cv2</span></span> 
- <span data-ttu-id="504cd-1574">КВК</span><span class="sxs-lookup"><span data-stu-id="504cd-1574">cvc</span></span> 
- <span data-ttu-id="504cd-1575">CVC2</span><span class="sxs-lookup"><span data-stu-id="504cd-1575">cvc2</span></span> 
- <span data-ttu-id="504cd-1576">КВН</span><span class="sxs-lookup"><span data-stu-id="504cd-1576">cvn</span></span> 
- <span data-ttu-id="504cd-1577">КВВ</span><span class="sxs-lookup"><span data-stu-id="504cd-1577">cvv</span></span> 
- <span data-ttu-id="504cd-1578">CVV2</span><span class="sxs-lookup"><span data-stu-id="504cd-1578">cvv2</span></span> 
- <span data-ttu-id="504cd-1579">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1579">cód seguranca</span></span> 
- <span data-ttu-id="504cd-1580">cód segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1580">cód segurança</span></span> 
- <span data-ttu-id="504cd-1581">кóд.</span><span class="sxs-lookup"><span data-stu-id="504cd-1581">cód.</span></span> <span data-ttu-id="504cd-1582">сегуранка</span><span class="sxs-lookup"><span data-stu-id="504cd-1582">seguranca</span></span> 
- <span data-ttu-id="504cd-1583">кóд.</span><span class="sxs-lookup"><span data-stu-id="504cd-1583">cód.</span></span> <span data-ttu-id="504cd-1584">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="504cd-1584">segurança</span></span> 
- <span data-ttu-id="504cd-1585">кóдиго</span><span class="sxs-lookup"><span data-stu-id="504cd-1585">código</span></span> 
- <span data-ttu-id="504cd-1586">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="504cd-1586">código de seguranca</span></span> 
- <span data-ttu-id="504cd-1587">código de segurança</span><span class="sxs-lookup"><span data-stu-id="504cd-1587">código de segurança</span></span> 
- <span data-ttu-id="504cd-1588">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="504cd-1588">de kaart controle</span></span> 
- <span data-ttu-id="504cd-1589">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="504cd-1589">geeft nr uit</span></span> 
- <span data-ttu-id="504cd-1590">issue no</span><span class="sxs-lookup"><span data-stu-id="504cd-1590">issue no</span></span> 
- <span data-ttu-id="504cd-1591">issue number</span><span class="sxs-lookup"><span data-stu-id="504cd-1591">issue number</span></span> 
- <span data-ttu-id="504cd-1592">каартидентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1592">kaartidentificatienummer</span></span> 
- <span data-ttu-id="504cd-1593">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1593">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="504cd-1594">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1594">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="504cd-1595">квестиеаантал</span><span class="sxs-lookup"><span data-stu-id="504cd-1595">kwestieaantal</span></span> 
- <span data-ttu-id="504cd-1596">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1596">no.</span></span> <span data-ttu-id="504cd-1597">делл'едизионе</span><span class="sxs-lookup"><span data-stu-id="504cd-1597">dell'edizione</span></span> 
- <span data-ttu-id="504cd-1598">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1598">no.</span></span> <span data-ttu-id="504cd-1599">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="504cd-1599">di sicurezza</span></span> 
- <span data-ttu-id="504cd-1600">numero de securite</span><span class="sxs-lookup"><span data-stu-id="504cd-1600">numero de securite</span></span> 
- <span data-ttu-id="504cd-1601">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="504cd-1601">numero de verificacao</span></span> 
- <span data-ttu-id="504cd-1602">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="504cd-1602">numero dell'edizione</span></span> 
- <span data-ttu-id="504cd-1603">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="504cd-1603">numero di identificazione della</span></span> 
- <span data-ttu-id="504cd-1604">счеда</span><span class="sxs-lookup"><span data-stu-id="504cd-1604">scheda</span></span> 
- <span data-ttu-id="504cd-1605">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="504cd-1605">numero di sicurezza</span></span> 
- <span data-ttu-id="504cd-1606">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="504cd-1606">numero van veiligheid</span></span> 
- <span data-ttu-id="504cd-1607">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="504cd-1607">numéro de sécurité</span></span> 
- <span data-ttu-id="504cd-1608">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="504cd-1608">nº autorizzazione</span></span> 
- <span data-ttu-id="504cd-1609">número de verificação</span><span class="sxs-lookup"><span data-stu-id="504cd-1609">número de verificação</span></span> 
- <span data-ttu-id="504cd-1610">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="504cd-1610">perno il blocco</span></span> 
- <span data-ttu-id="504cd-1611">pin block</span><span class="sxs-lookup"><span data-stu-id="504cd-1611">pin block</span></span> 
- <span data-ttu-id="504cd-1612">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="504cd-1612">prufziffer</span></span> 
- <span data-ttu-id="504cd-1613">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="504cd-1613">prüfziffer</span></span> 
- <span data-ttu-id="504cd-1614">security code</span><span class="sxs-lookup"><span data-stu-id="504cd-1614">security code</span></span> 
- <span data-ttu-id="504cd-1615">security no</span><span class="sxs-lookup"><span data-stu-id="504cd-1615">security no</span></span> 
- <span data-ttu-id="504cd-1616">security number</span><span class="sxs-lookup"><span data-stu-id="504cd-1616">security number</span></span> 
- <span data-ttu-id="504cd-1617">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="504cd-1617">sicherheits kode</span></span> 
- <span data-ttu-id="504cd-1618">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="504cd-1618">sicherheitscode</span></span> 
- <span data-ttu-id="504cd-1619">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1619">sicherheitsnummer</span></span> 
- <span data-ttu-id="504cd-1620">спелдблок</span><span class="sxs-lookup"><span data-stu-id="504cd-1620">speldblok</span></span> 
- <span data-ttu-id="504cd-1621">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1621">veiligheid nr</span></span> 
- <span data-ttu-id="504cd-1622">веилигхеидсаантал</span><span class="sxs-lookup"><span data-stu-id="504cd-1622">veiligheidsaantal</span></span> 
- <span data-ttu-id="504cd-1623">веилигхеидскоде</span><span class="sxs-lookup"><span data-stu-id="504cd-1623">veiligheidscode</span></span> 
- <span data-ttu-id="504cd-1624">веилигхеидснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1624">veiligheidsnummer</span></span> 
- <span data-ttu-id="504cd-1625">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1625">verfalldatum</span></span> 

#### <a name="keywordcardexpirationtermsdict"></a><span data-ttu-id="504cd-1626">Кэйворд_кард_експиратион_термс_дикт</span><span class="sxs-lookup"><span data-stu-id="504cd-1626">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="504cd-1627">аблауф</span><span class="sxs-lookup"><span data-stu-id="504cd-1627">ablauf</span></span> 
- <span data-ttu-id="504cd-1628">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="504cd-1628">data de expiracao</span></span> 
- <span data-ttu-id="504cd-1629">data de expiração</span><span class="sxs-lookup"><span data-stu-id="504cd-1629">data de expiração</span></span> 
- <span data-ttu-id="504cd-1630">data del exp</span><span class="sxs-lookup"><span data-stu-id="504cd-1630">data del exp</span></span> 
- <span data-ttu-id="504cd-1631">data di exp</span><span class="sxs-lookup"><span data-stu-id="504cd-1631">data di exp</span></span> 
- <span data-ttu-id="504cd-1632">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="504cd-1632">data di scadenza</span></span> 
- <span data-ttu-id="504cd-1633">data em que expira</span><span class="sxs-lookup"><span data-stu-id="504cd-1633">data em que expira</span></span> 
- <span data-ttu-id="504cd-1634">data scad</span><span class="sxs-lookup"><span data-stu-id="504cd-1634">data scad</span></span> 
- <span data-ttu-id="504cd-1635">data scadenza</span><span class="sxs-lookup"><span data-stu-id="504cd-1635">data scadenza</span></span> 
- <span data-ttu-id="504cd-1636">date de validité</span><span class="sxs-lookup"><span data-stu-id="504cd-1636">date de validité</span></span> 
- <span data-ttu-id="504cd-1637">datum afloop</span><span class="sxs-lookup"><span data-stu-id="504cd-1637">datum afloop</span></span> 
- <span data-ttu-id="504cd-1638">datum van exp</span><span class="sxs-lookup"><span data-stu-id="504cd-1638">datum van exp</span></span> 
- <span data-ttu-id="504cd-1639">de afloop</span><span class="sxs-lookup"><span data-stu-id="504cd-1639">de afloop</span></span> 
- <span data-ttu-id="504cd-1640">еспира</span><span class="sxs-lookup"><span data-stu-id="504cd-1640">espira</span></span> 
- <span data-ttu-id="504cd-1641">еспира</span><span class="sxs-lookup"><span data-stu-id="504cd-1641">espira</span></span> 
- <span data-ttu-id="504cd-1642">exp date</span><span class="sxs-lookup"><span data-stu-id="504cd-1642">exp date</span></span> 
- <span data-ttu-id="504cd-1643">exp datum</span><span class="sxs-lookup"><span data-stu-id="504cd-1643">exp datum</span></span> 
- <span data-ttu-id="504cd-1644">срока действия</span><span class="sxs-lookup"><span data-stu-id="504cd-1644">expiration</span></span> 
- <span data-ttu-id="504cd-1645">истекает</span><span class="sxs-lookup"><span data-stu-id="504cd-1645">expire</span></span> 
- <span data-ttu-id="504cd-1646">истекает</span><span class="sxs-lookup"><span data-stu-id="504cd-1646">expires</span></span> 
- <span data-ttu-id="504cd-1647">окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="504cd-1647">expiry</span></span> 
- <span data-ttu-id="504cd-1648">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="504cd-1648">fecha de expiracion</span></span> 
- <span data-ttu-id="504cd-1649">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="504cd-1649">fecha de venc</span></span> 
- <span data-ttu-id="504cd-1650">gultig bis</span><span class="sxs-lookup"><span data-stu-id="504cd-1650">gultig bis</span></span> 
- <span data-ttu-id="504cd-1651">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1651">gultigkeitsdatum</span></span> 
- <span data-ttu-id="504cd-1652">gültig bis</span><span class="sxs-lookup"><span data-stu-id="504cd-1652">gültig bis</span></span> 
- <span data-ttu-id="504cd-1653">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1653">gültigkeitsdatum</span></span> 
- <span data-ttu-id="504cd-1654">la scadenza</span><span class="sxs-lookup"><span data-stu-id="504cd-1654">la scadenza</span></span> 
- <span data-ttu-id="504cd-1655">скаденза</span><span class="sxs-lookup"><span data-stu-id="504cd-1655">scadenza</span></span> 
- <span data-ttu-id="504cd-1656">валабле</span><span class="sxs-lookup"><span data-stu-id="504cd-1656">valable</span></span> 
- <span data-ttu-id="504cd-1657">валидаде</span><span class="sxs-lookup"><span data-stu-id="504cd-1657">validade</span></span> 
- <span data-ttu-id="504cd-1658">valido hasta</span><span class="sxs-lookup"><span data-stu-id="504cd-1658">valido hasta</span></span> 
- <span data-ttu-id="504cd-1659">Валор</span><span class="sxs-lookup"><span data-stu-id="504cd-1659">valor</span></span> 
- <span data-ttu-id="504cd-1660">Венк</span><span class="sxs-lookup"><span data-stu-id="504cd-1660">venc</span></span> 
- <span data-ttu-id="504cd-1661">венЦименто</span><span class="sxs-lookup"><span data-stu-id="504cd-1661">vencimento</span></span> 
- <span data-ttu-id="504cd-1662">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="504cd-1662">vencimiento</span></span> 
- <span data-ttu-id="504cd-1663">верлупт</span><span class="sxs-lookup"><span data-stu-id="504cd-1663">verloopt</span></span> 
- <span data-ttu-id="504cd-1664">вервалдаг</span><span class="sxs-lookup"><span data-stu-id="504cd-1664">vervaldag</span></span> 
- <span data-ttu-id="504cd-1665">вервалдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1665">vervaldatum</span></span> 
- <span data-ttu-id="504cd-1666">ВТО</span><span class="sxs-lookup"><span data-stu-id="504cd-1666">vto</span></span> 
- <span data-ttu-id="504cd-1667">válido hasta</span><span class="sxs-lookup"><span data-stu-id="504cd-1667">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="504cd-1668">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="504cd-1668">EU Driver's License Number</span></span>

<span data-ttu-id="504cd-1669">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="504cd-1669">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="504cd-1670">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="504cd-1670">EU National Identification Number</span></span>

<span data-ttu-id="504cd-1671">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационНого номера ЕС](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="504cd-1671">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="504cd-1672">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="504cd-1672">EU Passport Number</span></span>

<span data-ttu-id="504cd-1673">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="504cd-1673">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="504cd-1674">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="504cd-1674">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="504cd-1675">Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="504cd-1675">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="504cd-1676">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="504cd-1676">EU Tax Identification Number</span></span>

<span data-ttu-id="504cd-1677">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогОвого кода ЕС](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="504cd-1677">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="504cd-1678">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="504cd-1678">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1679">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1679">Format</span></span>

<span data-ttu-id="504cd-1680">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="504cd-1680">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1681">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1681">Pattern</span></span>

<span data-ttu-id="504cd-1682">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="504cd-1682">Pattern must include all of the following:</span></span>
- <span data-ttu-id="504cd-1683">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="504cd-1683">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="504cd-1684">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="504cd-1684">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="504cd-1685">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="504cd-1685">Three-digit personal identification number</span></span> 
- <span data-ttu-id="504cd-1686">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-1686">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1687">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1687">Checksum</span></span>

<span data-ttu-id="504cd-1688">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1688">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1689">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1689">Definition</span></span>

<span data-ttu-id="504cd-1690">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1690">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1691">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1691">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1692">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="504cd-1692">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="504cd-1693">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1693">The checksum passes.</span></span>

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1694">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1694">Keywords</span></span>

- <span data-ttu-id="504cd-1695">Кэйворд_финниш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-1695">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="504cd-1696">Сосиаалитурватуннус</span><span class="sxs-lookup"><span data-stu-id="504cd-1696">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="504cd-1697">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="504cd-1697">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="504cd-1698">Персонбетеккнинг</span><span class="sxs-lookup"><span data-stu-id="504cd-1698">Personbeteckning</span></span>
- <span data-ttu-id="504cd-1699">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1699">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="504cd-1700">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="504cd-1700">Finland Passport Number</span></span>

<span data-ttu-id="504cd-1701">Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Режекс_финланд_пасспорт_нумбер находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1701">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-1702">находится ключевое слово из Keyword_finland_passport_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-1702">A keyword from Keyword_finland_passport_number is found.</span></span>
<span data-ttu-id="504cd-1703"><!-- Finland Passport Number -->
<Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="504cd-1703"></span></span>
<span data-ttu-id="504cd-1704">Ключевые слова Кэйворд_финланд_пасспорт_нумбер Passport Пасси</span><span class="sxs-lookup"><span data-stu-id="504cd-1704">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="504cd-1705">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="504cd-1705">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1706">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1706">Format</span></span>

<span data-ttu-id="504cd-1707">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1707">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1708">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1708">Pattern</span></span>

<span data-ttu-id="504cd-1709">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="504cd-1709">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1710">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1710">Checksum</span></span>

<span data-ttu-id="504cd-1711">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1711">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1712">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1712">Definition</span></span>

<span data-ttu-id="504cd-1713">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1713">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1714">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1714">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1715">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-1715">At least one of the following is true:</span></span>
- <span data-ttu-id="504cd-1716">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="504cd-1716">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="504cd-1717">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-1717">The function Func_eu_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1718">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1718">Keywords</span></span>

#### <a name="keywordfrenchdriverslicense"></a><span data-ttu-id="504cd-1719">Кэйворд_френч_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-1719">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="504cd-1720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1720">drivers licence</span></span>
- <span data-ttu-id="504cd-1721">drivers license</span><span class="sxs-lookup"><span data-stu-id="504cd-1721">drivers license</span></span>
- <span data-ttu-id="504cd-1722">driving licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1722">driving licence</span></span>
- <span data-ttu-id="504cd-1723">driving license</span><span class="sxs-lookup"><span data-stu-id="504cd-1723">driving license</span></span>
- <span data-ttu-id="504cd-1724">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="504cd-1724">permis de conduire</span></span>
- <span data-ttu-id="504cd-1725">licence number</span><span class="sxs-lookup"><span data-stu-id="504cd-1725">licence number</span></span>
- <span data-ttu-id="504cd-1726">license number</span><span class="sxs-lookup"><span data-stu-id="504cd-1726">license number</span></span>
- <span data-ttu-id="504cd-1727">licence numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-1727">licence numbers</span></span>
- <span data-ttu-id="504cd-1728">license numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-1728">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="504cd-1729">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="504cd-1729">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1730">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1730">Format</span></span>

<span data-ttu-id="504cd-1731">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1731">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1732">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1732">Pattern</span></span>

<span data-ttu-id="504cd-1733">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1733">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1734">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1734">Checksum</span></span>

<span data-ttu-id="504cd-1735">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1735">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1736">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1736">Definition</span></span>

<span data-ttu-id="504cd-1737">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1737">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1738">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1738">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1739">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1739">Keywords</span></span>

<span data-ttu-id="504cd-1740">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1740">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="504cd-1741">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="504cd-1741">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1742">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1742">Format</span></span>

<span data-ttu-id="504cd-1743">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="504cd-1743">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1744">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1744">Pattern</span></span>

<span data-ttu-id="504cd-1745">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="504cd-1745">Nine digits and letters:</span></span>
- <span data-ttu-id="504cd-1746">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-1746">Two digits</span></span> 
- <span data-ttu-id="504cd-1747">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-1747">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-1748">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-1748">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1749">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1749">Checksum</span></span>

<span data-ttu-id="504cd-1750">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1750">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1751">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1751">Definition</span></span>

<span data-ttu-id="504cd-1752">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1752">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1753">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1753">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1754">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="504cd-1754">A keyword from Keyword_passport is found.</span></span>

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1755">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1755">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="504cd-1756">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-1756">Keyword_passport</span></span>

- <span data-ttu-id="504cd-1757">Passport Number</span><span class="sxs-lookup"><span data-stu-id="504cd-1757">Passport Number</span></span>
- <span data-ttu-id="504cd-1758">Passport No</span><span class="sxs-lookup"><span data-stu-id="504cd-1758">Passport No</span></span>
- <span data-ttu-id="504cd-1759">Passport#</span><span class="sxs-lookup"><span data-stu-id="504cd-1759">Passport #</span></span>
- <span data-ttu-id="504cd-1760">Службу</span><span class="sxs-lookup"><span data-stu-id="504cd-1760">Passport#</span></span>
- <span data-ttu-id="504cd-1761">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="504cd-1761">PassportID</span></span>
- <span data-ttu-id="504cd-1762">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="504cd-1762">Passportno</span></span>
- <span data-ttu-id="504cd-1763">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-1763">passportnumber</span></span>
- <span data-ttu-id="504cd-1764">パスポート</span><span class="sxs-lookup"><span data-stu-id="504cd-1764">パスポート</span></span>
- <span data-ttu-id="504cd-1765">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="504cd-1765">パスポート番号</span></span>
- <span data-ttu-id="504cd-1766">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="504cd-1766">パスポートのNum</span></span>
- <span data-ttu-id="504cd-1767">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="504cd-1767">パスポート ＃</span></span> 
- <span data-ttu-id="504cd-1768">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="504cd-1768">Numéro de passeport</span></span>
- <span data-ttu-id="504cd-1769">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="504cd-1769">Passeport n °</span></span>
- <span data-ttu-id="504cd-1770">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="504cd-1770">Passeport Non</span></span>
- <span data-ttu-id="504cd-1771">Passeport#</span><span class="sxs-lookup"><span data-stu-id="504cd-1771">Passeport #</span></span>
- <span data-ttu-id="504cd-1772">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="504cd-1772">Passeport#</span></span>
- <span data-ttu-id="504cd-1773">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="504cd-1773">PasseportNon</span></span>
- <span data-ttu-id="504cd-1774">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="504cd-1774">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="504cd-1775">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="504cd-1775">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1776">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1776">Format</span></span>

<span data-ttu-id="504cd-1777">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1777">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1778">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1778">Pattern</span></span>

<span data-ttu-id="504cd-1779">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="504cd-1779">Must match one of two patterns:</span></span>
- <span data-ttu-id="504cd-1780">13 цифр, за которыми следует пробел, за которым следуют две цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-1780">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="504cd-1781">или</span><span class="sxs-lookup"><span data-stu-id="504cd-1781">or</span></span>
- <span data-ttu-id="504cd-1782">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1782">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1783">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1783">Checksum</span></span>

<span data-ttu-id="504cd-1784">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1784">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1785">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1785">Definition</span></span>

<span data-ttu-id="504cd-1786">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1786">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1787">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1787">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1788">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="504cd-1788">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="504cd-1789">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1789">The checksum passes.</span></span>

<span data-ttu-id="504cd-1790">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1790">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1791">Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-1791">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1792">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="504cd-1792">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="504cd-1793">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1793">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1794">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1794">Keywords</span></span>

#### <a name="keywordfrinsee"></a><span data-ttu-id="504cd-1795">Кэйворд_фр_инси</span><span class="sxs-lookup"><span data-stu-id="504cd-1795">Keyword_fr_insee</span></span>

- <span data-ttu-id="504cd-1796">INSEE</span><span class="sxs-lookup"><span data-stu-id="504cd-1796">insee</span></span>
- <span data-ttu-id="504cd-1797">securité sociale</span><span class="sxs-lookup"><span data-stu-id="504cd-1797">securité sociale</span></span>
- <span data-ttu-id="504cd-1798">securite sociale</span><span class="sxs-lookup"><span data-stu-id="504cd-1798">securite sociale</span></span>
- <span data-ttu-id="504cd-1799">national id</span><span class="sxs-lookup"><span data-stu-id="504cd-1799">national id</span></span>
- <span data-ttu-id="504cd-1800">national identification</span><span class="sxs-lookup"><span data-stu-id="504cd-1800">national identification</span></span>
- <span data-ttu-id="504cd-1801">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="504cd-1801">numéro d'identité</span></span>
- <span data-ttu-id="504cd-1802">no d'identité</span><span class="sxs-lookup"><span data-stu-id="504cd-1802">no d'identité</span></span>
- <span data-ttu-id="504cd-1803">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1803">no.</span></span> <span data-ttu-id="504cd-1804">д'идентитé</span><span class="sxs-lookup"><span data-stu-id="504cd-1804">d'identité</span></span>
- <span data-ttu-id="504cd-1805">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="504cd-1805">numero d'identite</span></span>
- <span data-ttu-id="504cd-1806">no d'identite</span><span class="sxs-lookup"><span data-stu-id="504cd-1806">no d'identite</span></span>
- <span data-ttu-id="504cd-1807">Нет.</span><span class="sxs-lookup"><span data-stu-id="504cd-1807">no.</span></span> <span data-ttu-id="504cd-1808">д'идентите</span><span class="sxs-lookup"><span data-stu-id="504cd-1808">d'identite</span></span>
- <span data-ttu-id="504cd-1809">social security number</span><span class="sxs-lookup"><span data-stu-id="504cd-1809">social security number</span></span>
- <span data-ttu-id="504cd-1810">social security code</span><span class="sxs-lookup"><span data-stu-id="504cd-1810">social security code</span></span>
- <span data-ttu-id="504cd-1811">social insurance number</span><span class="sxs-lookup"><span data-stu-id="504cd-1811">social insurance number</span></span>
- <span data-ttu-id="504cd-1812">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="504cd-1812">le numéro d'identification nationale</span></span>
- <span data-ttu-id="504cd-1813">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="504cd-1813">d'identité nationale</span></span>
- <span data-ttu-id="504cd-1814">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="504cd-1814">numéro de sécurité sociale</span></span>
- <span data-ttu-id="504cd-1815">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="504cd-1815">le code de la sécurité sociale</span></span>
- <span data-ttu-id="504cd-1816">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="504cd-1816">numéro d'assurance sociale</span></span>
- <span data-ttu-id="504cd-1817">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="504cd-1817">numéro de sécu</span></span>
- <span data-ttu-id="504cd-1818">code sécu</span><span class="sxs-lookup"><span data-stu-id="504cd-1818">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="504cd-1819">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="504cd-1819">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1820">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1820">Format</span></span>

<span data-ttu-id="504cd-1821">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="504cd-1821">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1822">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1822">Pattern</span></span>

<span data-ttu-id="504cd-1823">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-1823">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="504cd-1824">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="504cd-1824">A digit or letter</span></span> 
- <span data-ttu-id="504cd-1825">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-1825">Two digits</span></span> 
- <span data-ttu-id="504cd-1826">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="504cd-1826">Six digits or letters</span></span> 
- <span data-ttu-id="504cd-1827">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="504cd-1827">A digit</span></span> 
- <span data-ttu-id="504cd-1828">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="504cd-1828">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1829">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1829">Checksum</span></span>

<span data-ttu-id="504cd-1830">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1830">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1831">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1831">Definition</span></span>

<span data-ttu-id="504cd-1832">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1833">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1833">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1834">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-1834">At least one of the following is true:</span></span>
    - <span data-ttu-id="504cd-1835">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-1835">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="504cd-1836">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="504cd-1836">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="504cd-1837">найдено ключевое слово из Keyword_german_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="504cd-1837">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="504cd-1838">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1838">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1839">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1839">Keywords</span></span>

#### <a name="keywordgermandriverslicensenumber"></a><span data-ttu-id="504cd-1840">Кэйворд_жерман_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-1840">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="504cd-1841">Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1841">Führerschein</span></span>
- <span data-ttu-id="504cd-1842">Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1842">Fuhrerschein</span></span>
- <span data-ttu-id="504cd-1843">Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1843">Fuehrerschein</span></span>
- <span data-ttu-id="504cd-1844">Фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1844">Führerscheinnummer</span></span>
- <span data-ttu-id="504cd-1845">Фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1845">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="504cd-1846">Фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1846">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="504cd-1847">Фüхрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="504cd-1847">Führerschein-</span></span> 
- <span data-ttu-id="504cd-1848">Фухрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="504cd-1848">Fuhrerschein-</span></span> 
- <span data-ttu-id="504cd-1849">Фуехрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="504cd-1849">Fuehrerschein-</span></span> 
- <span data-ttu-id="504cd-1850">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="504cd-1850">FührerscheinnummerNr</span></span>
- <span data-ttu-id="504cd-1851">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="504cd-1851">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="504cd-1852">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="504cd-1852">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="504cd-1853">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1853">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="504cd-1854">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1854">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="504cd-1855">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1855">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="504cd-1856">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1856">Führerschein- Nr</span></span>
- <span data-ttu-id="504cd-1857">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1857">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="504cd-1858">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1858">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="504cd-1859">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="504cd-1859">Führerschein- Klasse</span></span> 
- <span data-ttu-id="504cd-1860">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="504cd-1860">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="504cd-1861">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="504cd-1861">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="504cd-1862">Фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="504cd-1862">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="504cd-1863">Фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="504cd-1863">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="504cd-1864">Фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="504cd-1864">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="504cd-1865">Фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1865">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="504cd-1866">Фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1866">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="504cd-1867">Фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1867">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="504cd-1868">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1868">Führerschein- Nr</span></span> 
- <span data-ttu-id="504cd-1869">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1869">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="504cd-1870">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="504cd-1870">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="504cd-1871">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="504cd-1871">Führerschein- Klasse</span></span> 
- <span data-ttu-id="504cd-1872">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="504cd-1872">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="504cd-1873">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="504cd-1873">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="504cd-1874">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-1874">DL</span></span> 
- <span data-ttu-id="504cd-1875">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="504cd-1875">DLS</span></span>
- <span data-ttu-id="504cd-1876">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-1876">Driv Lic</span></span> 
- <span data-ttu-id="504cd-1877">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="504cd-1877">Driv Licen</span></span> 
- <span data-ttu-id="504cd-1878">Driv License</span><span class="sxs-lookup"><span data-stu-id="504cd-1878">Driv License</span></span>
- <span data-ttu-id="504cd-1879">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-1879">Driv Licenses</span></span> 
- <span data-ttu-id="504cd-1880">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1880">Driv Licence</span></span> 
- <span data-ttu-id="504cd-1881">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-1881">Driv Licences</span></span> 
- <span data-ttu-id="504cd-1882">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-1882">Driv Lic</span></span> 
- <span data-ttu-id="504cd-1883">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="504cd-1883">Driver Licen</span></span> 
- <span data-ttu-id="504cd-1884">Driver License</span><span class="sxs-lookup"><span data-stu-id="504cd-1884">Driver License</span></span> 
- <span data-ttu-id="504cd-1885">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-1885">Driver Licenses</span></span> 
- <span data-ttu-id="504cd-1886">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1886">Driver Licence</span></span> 
- <span data-ttu-id="504cd-1887">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-1887">Driver Licences</span></span> 
- <span data-ttu-id="504cd-1888">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-1888">Drivers Lic</span></span> 
- <span data-ttu-id="504cd-1889">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="504cd-1889">Drivers Licen</span></span> 
- <span data-ttu-id="504cd-1890">Drivers License</span><span class="sxs-lookup"><span data-stu-id="504cd-1890">Drivers License</span></span> 
- <span data-ttu-id="504cd-1891">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-1891">Drivers Licenses</span></span> 
- <span data-ttu-id="504cd-1892">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1892">Drivers Licence</span></span> 
- <span data-ttu-id="504cd-1893">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-1893">Drivers Licences</span></span> 
- <span data-ttu-id="504cd-1894">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-1894">Driver's Lic</span></span> 
- <span data-ttu-id="504cd-1895">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="504cd-1895">Driver's Licen</span></span> 
- <span data-ttu-id="504cd-1896">Driver's License</span><span class="sxs-lookup"><span data-stu-id="504cd-1896">Driver's License</span></span> 
- <span data-ttu-id="504cd-1897">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-1897">Driver's Licenses</span></span> 
- <span data-ttu-id="504cd-1898">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1898">Driver's Licence</span></span> 
- <span data-ttu-id="504cd-1899">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-1899">Driver's Licences</span></span> 
- <span data-ttu-id="504cd-1900">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-1900">Driving Lic</span></span> 
- <span data-ttu-id="504cd-1901">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="504cd-1901">Driving Licen</span></span> 
- <span data-ttu-id="504cd-1902">Driving License</span><span class="sxs-lookup"><span data-stu-id="504cd-1902">Driving License</span></span> 
- <span data-ttu-id="504cd-1903">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-1903">Driving Licenses</span></span> 
- <span data-ttu-id="504cd-1904">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="504cd-1904">Driving Licence</span></span> 
- <span data-ttu-id="504cd-1905">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="504cd-1905">Driving Licences</span></span>

#### <a name="keywordgermandriverslicensecollaborative"></a><span data-ttu-id="504cd-1906">Кэйворд_жерман_дриверс_лиценсе_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="504cd-1906">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="504cd-1907">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1907">Nr-Führerschein</span></span> 
- <span data-ttu-id="504cd-1908">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1908">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="504cd-1909">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1909">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="504cd-1910">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1910">No-Führerschein</span></span> 
- <span data-ttu-id="504cd-1911">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1911">No-Fuhrerschein</span></span> 
- <span data-ttu-id="504cd-1912">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1912">No-Fuehrerschein</span></span> 
- <span data-ttu-id="504cd-1913">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1913">N-Führerschein</span></span> 
- <span data-ttu-id="504cd-1914">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1914">N-Fuhrerschein</span></span> 
- <span data-ttu-id="504cd-1915">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1915">N-Fuehrerschein</span></span>
- <span data-ttu-id="504cd-1916">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1916">Nr-Führerschein</span></span> 
- <span data-ttu-id="504cd-1917">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1917">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="504cd-1918">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1918">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="504cd-1919">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1919">No-Führerschein</span></span> 
- <span data-ttu-id="504cd-1920">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1920">No-Fuhrerschein</span></span> 
- <span data-ttu-id="504cd-1921">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1921">No-Fuehrerschein</span></span> 
- <span data-ttu-id="504cd-1922">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1922">N-Führerschein</span></span> 
- <span data-ttu-id="504cd-1923">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1923">N-Fuhrerschein</span></span> 
- <span data-ttu-id="504cd-1924">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="504cd-1924">N-Fuehrerschein</span></span> 

#### <a name="keywordgermandriverslicense"></a><span data-ttu-id="504cd-1925">Кэйворд_жерман_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-1925">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="504cd-1926">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1926">ausstellungsdatum</span></span>
- <span data-ttu-id="504cd-1927">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="504cd-1927">ausstellungsort</span></span>
- <span data-ttu-id="504cd-1928">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="504cd-1928">ausstellende behöde</span></span>
- <span data-ttu-id="504cd-1929">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="504cd-1929">ausstellende behorde</span></span>
- <span data-ttu-id="504cd-1930">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="504cd-1930">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="504cd-1931">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="504cd-1931">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1932">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1932">Format</span></span>

<span data-ttu-id="504cd-1933">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="504cd-1933">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1934">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1934">Pattern</span></span>

<span data-ttu-id="504cd-1935">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="504cd-1935">Pattern must include all of the following:</span></span>
- <span data-ttu-id="504cd-1936">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="504cd-1936">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="504cd-1937">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-1937">Three digits</span></span> 
- <span data-ttu-id="504cd-1938">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="504cd-1938">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="504cd-1939">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="504cd-1939">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1940">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1940">Checksum</span></span>

<span data-ttu-id="504cd-1941">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-1941">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1942">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1942">Definition</span></span>

<span data-ttu-id="504cd-1943">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1943">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1944">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1944">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1945">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="504cd-1945">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="504cd-1946">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1946">The checksum passes.</span></span>

<span data-ttu-id="504cd-1947">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1947">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1948">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1948">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1949">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="504cd-1949">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="504cd-1950">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-1950">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-1951">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1951">Keywords</span></span>

#### <a name="keywordgermanpassport"></a><span data-ttu-id="504cd-1952">Кэйворд_жерман_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-1952">Keyword_german_passport</span></span>

- <span data-ttu-id="504cd-1953">реисепасс</span><span class="sxs-lookup"><span data-stu-id="504cd-1953">reisepass</span></span>
- <span data-ttu-id="504cd-1954">реисепассе</span><span class="sxs-lookup"><span data-stu-id="504cd-1954">reisepasse</span></span>
- <span data-ttu-id="504cd-1955">реисепасснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1955">reisepassnummer</span></span>
- <span data-ttu-id="504cd-1956">службу</span><span class="sxs-lookup"><span data-stu-id="504cd-1956">passport</span></span>
- <span data-ttu-id="504cd-1957">паспорты</span><span class="sxs-lookup"><span data-stu-id="504cd-1957">passports</span></span>

#### <a name="keywordgermanpassportcollaborative"></a><span data-ttu-id="504cd-1958">Кэйворд_жерман_пасспорт_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="504cd-1958">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="504cd-1959">жебуртсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1959">geburtsdatum</span></span>
- <span data-ttu-id="504cd-1960">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="504cd-1960">ausstellungsdatum</span></span>
- <span data-ttu-id="504cd-1961">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="504cd-1961">ausstellungsort</span></span>

#### <a name="keywordgermanpassportnumber"></a><span data-ttu-id="504cd-1962">Кэйворд_жерман_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-1962">Keyword_german_passport_number</span></span>

<span data-ttu-id="504cd-1963">No — Реисепасс НР — Реисепасс</span><span class="sxs-lookup"><span data-stu-id="504cd-1963">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keywordgermanpassport1"></a><span data-ttu-id="504cd-1964">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="504cd-1964">Keyword_german_passport1</span></span>

<span data-ttu-id="504cd-1965">Реисепасс — НР</span><span class="sxs-lookup"><span data-stu-id="504cd-1965">Reisepass-Nr</span></span>

#### <a name="keywordgermanpassport2"></a><span data-ttu-id="504cd-1966">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="504cd-1966">Keyword_german_passport2</span></span>

<span data-ttu-id="504cd-1967">бнатионалит. t</span><span class="sxs-lookup"><span data-stu-id="504cd-1967">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="504cd-1968">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="504cd-1968">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1969">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1969">Format</span></span>

<span data-ttu-id="504cd-1970">С 1 ноября 2010: девять букв и цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-1970">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="504cd-1971">От 1 апреля 1987 до 31 октября 2010:10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1971">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1972">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1972">Pattern</span></span>

<span data-ttu-id="504cd-1973">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="504cd-1973">Since 1 November 2010:</span></span>
- <span data-ttu-id="504cd-1974">одна буква (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-1974">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-1975">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1975">Eight digits</span></span>

<span data-ttu-id="504cd-1976">От 1 апреля 1987 до 31 октября 2010:</span><span class="sxs-lookup"><span data-stu-id="504cd-1976">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="504cd-1977">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-1977">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-1978">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-1978">Checksum</span></span>

<span data-ttu-id="504cd-1979">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-1979">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-1980">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-1980">Definition</span></span>

<span data-ttu-id="504cd-1981">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-1981">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-1982">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-1982">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-1983">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="504cd-1983">A keyword from Keyword_germany_id_card is found.</span></span>

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-1984">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-1984">Keywords</span></span>

#### <a name="keywordgermanyidcard"></a><span data-ttu-id="504cd-1985">Кэйворд_жермани_ид_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-1985">Keyword_germany_id_card</span></span>

- <span data-ttu-id="504cd-1986">Identity Card</span><span class="sxs-lookup"><span data-stu-id="504cd-1986">Identity Card</span></span>
- <span data-ttu-id="504cd-1987">ИД</span><span class="sxs-lookup"><span data-stu-id="504cd-1987">ID</span></span>
- <span data-ttu-id="504cd-1988">Процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-1988">Identification</span></span>
- <span data-ttu-id="504cd-1989">Персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="504cd-1989">Personalausweis</span></span>
- <span data-ttu-id="504cd-1990">Идентифизиерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-1990">Identifizierungsnummer</span></span>
- <span data-ttu-id="504cd-1991">Аусвеис</span><span class="sxs-lookup"><span data-stu-id="504cd-1991">Ausweis</span></span>
- <span data-ttu-id="504cd-1992">Идентификатион</span><span class="sxs-lookup"><span data-stu-id="504cd-1992">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="504cd-1993">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="504cd-1993">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="504cd-1994">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-1994">Format</span></span>

<span data-ttu-id="504cd-1995">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="504cd-1995">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-1996">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-1996">Pattern</span></span>

<span data-ttu-id="504cd-1997">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="504cd-1997">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="504cd-1998">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="504cd-1998">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="504cd-1999">тире;</span><span class="sxs-lookup"><span data-stu-id="504cd-1999">A dash</span></span> 
- <span data-ttu-id="504cd-2000">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2000">Six digits</span></span>

<span data-ttu-id="504cd-2001">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="504cd-2001">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="504cd-2002">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="504cd-2002">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="504cd-2003">тире;</span><span class="sxs-lookup"><span data-stu-id="504cd-2003">A dash</span></span> 
- <span data-ttu-id="504cd-2004">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2004">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2005">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2005">Checksum</span></span>

<span data-ttu-id="504cd-2006">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2006">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2007">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2007">Definition</span></span>

<span data-ttu-id="504cd-2008">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2008">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2009">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2009">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2010">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="504cd-2010">A keyword from Keyword_greece_id_card is found.</span></span>

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2011">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2011">Keywords</span></span>

#### <a name="keywordgreeceidcard"></a><span data-ttu-id="504cd-2012">Кэйворд_грице_ид_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-2012">Keyword_greece_id_card</span></span>

- <span data-ttu-id="504cd-2013">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2013">Greek identity Card</span></span>
- <span data-ttu-id="504cd-2014">Таутотита</span><span class="sxs-lookup"><span data-stu-id="504cd-2014">Tautotita</span></span>
- <span data-ttu-id="504cd-2015">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="504cd-2015">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="504cd-2016">Ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="504cd-2016">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="504cd-2017">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="504cd-2017">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2018">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2018">Format</span></span>

<span data-ttu-id="504cd-2019">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="504cd-2019">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2020">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2020">Pattern</span></span>

<span data-ttu-id="504cd-2021">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="504cd-2021">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="504cd-2022">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-2022">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2023">шесть цифр; </span><span class="sxs-lookup"><span data-stu-id="504cd-2023">Six digits</span></span> 
- <span data-ttu-id="504cd-2024">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="504cd-2024">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2025">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2025">Checksum</span></span>

<span data-ttu-id="504cd-2026">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2026">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2027">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2027">Definition</span></span>

<span data-ttu-id="504cd-2028">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2028">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2029">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2029">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2030">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="504cd-2030">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="504cd-2031">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2031">The checksum passes.</span></span>

<span data-ttu-id="504cd-2032">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2032">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2033">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2033">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2034">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2034">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2035">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2035">Keywords</span></span>

#### <a name="keywordhongkongidcard"></a><span data-ttu-id="504cd-2036">Кэйворд_хонг_конг_ид_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-2036">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="504cd-2037">идентификационная карточка Гонконг</span><span class="sxs-lookup"><span data-stu-id="504cd-2037">hong kong identity card</span></span>
- <span data-ttu-id="504cd-2038">ХКИДК</span><span class="sxs-lookup"><span data-stu-id="504cd-2038">HKIDC</span></span>
- <span data-ttu-id="504cd-2039">id card</span><span class="sxs-lookup"><span data-stu-id="504cd-2039">id card</span></span>
- <span data-ttu-id="504cd-2040">identity card</span><span class="sxs-lookup"><span data-stu-id="504cd-2040">identity card</span></span>
- <span data-ttu-id="504cd-2041">идентификационная карточка HK</span><span class="sxs-lookup"><span data-stu-id="504cd-2041">hk identity card</span></span>
- <span data-ttu-id="504cd-2042">Идентификатор Гонконг</span><span class="sxs-lookup"><span data-stu-id="504cd-2042">hong kong id</span></span>
- <span data-ttu-id="504cd-2043">香港身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2043">香港身份證</span></span>
- <span data-ttu-id="504cd-2044">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2044">香港永久性居民身份證</span></span>
- <span data-ttu-id="504cd-2045">身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2045">身份證</span></span>
- <span data-ttu-id="504cd-2046">身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2046">身份証</span></span>
- <span data-ttu-id="504cd-2047">身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2047">身分證</span></span>
- <span data-ttu-id="504cd-2048">身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2048">身分証</span></span>
- <span data-ttu-id="504cd-2049">香港身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2049">香港身份証</span></span>
- <span data-ttu-id="504cd-2050">香港身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2050">香港身分證</span></span>
- <span data-ttu-id="504cd-2051">香港身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2051">香港身分証</span></span>
- <span data-ttu-id="504cd-2052">香港身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2052">香港身份證</span></span>
- <span data-ttu-id="504cd-2053">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2053">香港居民身份證</span></span>
- <span data-ttu-id="504cd-2054">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2054">香港居民身份証</span></span>
- <span data-ttu-id="504cd-2055">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2055">香港居民身分證</span></span>
- <span data-ttu-id="504cd-2056">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2056">香港居民身分証</span></span>
- <span data-ttu-id="504cd-2057">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2057">香港永久性居民身份証</span></span>
- <span data-ttu-id="504cd-2058">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2058">香港永久性居民身分證</span></span>
- <span data-ttu-id="504cd-2059">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2059">香港永久性居民身分証</span></span>
- <span data-ttu-id="504cd-2060">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2060">香港永久性居民身份證</span></span>
- <span data-ttu-id="504cd-2061">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2061">香港非永久性居民身份證</span></span>
- <span data-ttu-id="504cd-2062">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2062">香港非永久性居民身份証</span></span>
- <span data-ttu-id="504cd-2063">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2063">香港非永久性居民身分證</span></span>
- <span data-ttu-id="504cd-2064">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2064">香港非永久性居民身分証</span></span>
- <span data-ttu-id="504cd-2065">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2065">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="504cd-2066">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2066">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="504cd-2067">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2067">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="504cd-2068">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2068">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="504cd-2069">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2069">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="504cd-2070">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="504cd-2070">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="504cd-2071">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2071">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="504cd-2072">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="504cd-2072">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="504cd-2073">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2073">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2074">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2074">Format</span></span>

<span data-ttu-id="504cd-2075">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2075">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2076">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2076">Pattern</span></span>

<span data-ttu-id="504cd-2077">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2077">10 letters or digits:</span></span>
- <span data-ttu-id="504cd-2078">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-2078">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2079">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2079">Four digits</span></span> 
- <span data-ttu-id="504cd-2080">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="504cd-2080">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2081">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2081">Checksum</span></span>

<span data-ttu-id="504cd-2082">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2082">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2083">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2083">Definition</span></span>

<span data-ttu-id="504cd-2084">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2084">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2085">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2085">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2086">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2086">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="504cd-2087">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2087">The checksum passes.</span></span>

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2088">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2088">Keywords</span></span>

#### <a name="keywordindiapermanentaccountnumber"></a><span data-ttu-id="504cd-2089">Кэйворд_индиа_перманент_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2089">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="504cd-2090">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2090">Permanent Account Number</span></span> 
- <span data-ttu-id="504cd-2091">ПАНОРАМИРОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="504cd-2091">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="504cd-2092">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="504cd-2092">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2093">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2093">Format</span></span>

<span data-ttu-id="504cd-2094">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="504cd-2094">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2095">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2095">Pattern</span></span>

<span data-ttu-id="504cd-2096">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2096">12 digits:</span></span>
- <span data-ttu-id="504cd-2097">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-2097">Four digits</span></span> 
- <span data-ttu-id="504cd-2098">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="504cd-2098">An optional space or dash</span></span> 
- <span data-ttu-id="504cd-2099">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-2099">Four digits</span></span> 
- <span data-ttu-id="504cd-2100">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="504cd-2100">An optional space or dash</span></span> 
- <span data-ttu-id="504cd-2101">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="504cd-2101">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2102">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2102">Checksum</span></span>

<span data-ttu-id="504cd-2103">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2103">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2104">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2104">Definition</span></span>

<span data-ttu-id="504cd-2105">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2105">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-2106">находится ключевое слово из Keyword_india_aadhar;</span><span class="sxs-lookup"><span data-stu-id="504cd-2106">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="504cd-2107">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2107">The checksum passes.</span></span>
<span data-ttu-id="504cd-2108">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2108">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-2109">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2109">The checksum passes.</span></span>
<span data-ttu-id="504cd-2110"><!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="504cd-2110"></span></span>

### <a name="keywords"></a><span data-ttu-id="504cd-2111">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2111">Keywords</span></span>
   
#### <a name="keywordindiaaadhar"></a><span data-ttu-id="504cd-2112">Кэйворд_индиа_аадхар</span><span class="sxs-lookup"><span data-stu-id="504cd-2112">Keyword_india_aadhar</span></span>
- <span data-ttu-id="504cd-2113">Аадхар</span><span class="sxs-lookup"><span data-stu-id="504cd-2113">Aadhar</span></span>
- <span data-ttu-id="504cd-2114">Aadhaar</span><span class="sxs-lookup"><span data-stu-id="504cd-2114">Aadhaar</span></span>
- <span data-ttu-id="504cd-2115">UID</span><span class="sxs-lookup"><span data-stu-id="504cd-2115">UID</span></span>
- <span data-ttu-id="504cd-2116">आधार</span><span class="sxs-lookup"><span data-stu-id="504cd-2116">आधार</span></span>
   
## <a name="indonesia-identity-card-ktp-number"></a><span data-ttu-id="504cd-2117">Номер удостоверения личности (KTP) для Индонезии</span><span class="sxs-lookup"><span data-stu-id="504cd-2117">Indonesia Identity Card (KTP) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2118">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2118">Format</span></span>

<span data-ttu-id="504cd-2119">16 цифр, содержащих необязательные точки.</span><span class="sxs-lookup"><span data-stu-id="504cd-2119">16 digits containing optional periods</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2120">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2120">Pattern</span></span>

<span data-ttu-id="504cd-2121">16 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2121">16 digits:</span></span>
- <span data-ttu-id="504cd-2122">две цифры (код провинции);</span><span class="sxs-lookup"><span data-stu-id="504cd-2122">Two-digit province code</span></span> 
- <span data-ttu-id="504cd-2123">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="504cd-2123">A period (optional)</span></span> 
- <span data-ttu-id="504cd-2124">две цифры (код округа или города);</span><span class="sxs-lookup"><span data-stu-id="504cd-2124">Two-digit regency or city code</span></span> 
- <span data-ttu-id="504cd-2125">две цифры (код района);</span><span class="sxs-lookup"><span data-stu-id="504cd-2125">Two-digit subdistrict code</span></span> 
- <span data-ttu-id="504cd-2126">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="504cd-2126">A period (optional)</span></span> 
- <span data-ttu-id="504cd-2127">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="504cd-2127">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="504cd-2128">точка (необязательно);</span><span class="sxs-lookup"><span data-stu-id="504cd-2128">A period (optional)</span></span> 
- <span data-ttu-id="504cd-2129">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2129">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2130">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2130">Checksum</span></span>

<span data-ttu-id="504cd-2131">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2131">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2132">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2132">Definition</span></span>

<span data-ttu-id="504cd-2133">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2133">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2134">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-2134">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2135">находится ключевое слово из Keyword_indonesia_id_card.</span><span class="sxs-lookup"><span data-stu-id="504cd-2135">A keyword from Keyword_indonesia_id_card is found.</span></span>

<span data-ttu-id="504cd-2136">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2136">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2137">регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-2137">The regular expression Regex_indonesia_id_card finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2138">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2138">Keywords</span></span>
   
#### <a name="keywordindonesiaidcard"></a><span data-ttu-id="504cd-2139">Кэйворд_индонесиа_ид_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-2139">Keyword_indonesia_id_card</span></span>

- <span data-ttu-id="504cd-2140">KTP</span><span class="sxs-lookup"><span data-stu-id="504cd-2140">KTP</span></span>
- <span data-ttu-id="504cd-2141">Kartu Tanda Penduduk</span><span class="sxs-lookup"><span data-stu-id="504cd-2141">Kartu Tanda Penduduk</span></span> 
- <span data-ttu-id="504cd-2142">Nomor Induk Kependudukan</span><span class="sxs-lookup"><span data-stu-id="504cd-2142">Nomor Induk Kependudukan</span></span> 
   
## <a name="international-banking-account-number-iban"></a><span data-ttu-id="504cd-2143">Международный номер банковского счета (IBAN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2143">International Banking Account Number (IBAN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2144">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2144">Format</span></span>

<span data-ttu-id="504cd-2145">Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)</span><span class="sxs-lookup"><span data-stu-id="504cd-2145">Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2146">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2146">Pattern</span></span>

<span data-ttu-id="504cd-2147">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="504cd-2147">Pattern must include all of the following:</span></span>

- <span data-ttu-id="504cd-2148">Двухбуквенный код страны</span><span class="sxs-lookup"><span data-stu-id="504cd-2148">Two-letter country code</span></span>
- <span data-ttu-id="504cd-2149">Две проверочные цифры (после которых может следовать пробел) </span><span class="sxs-lookup"><span data-stu-id="504cd-2149">Two check digits (followed by an optional space)</span></span> 
- <span data-ttu-id="504cd-2150">1–7 групп из четырех букв или цифр (могут разделяться пробелами)</span><span class="sxs-lookup"><span data-stu-id="504cd-2150">1-7 groups of four letters or digits (can be separated by spaces)</span></span>
- <span data-ttu-id="504cd-2151">1–3 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2151">1-3 letters or digits</span></span>

<span data-ttu-id="504cd-p134">Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:</span><span class="sxs-lookup"><span data-stu-id="504cd-p134">The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:</span></span>

<span data-ttu-id="504cd-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span><span class="sxs-lookup"><span data-stu-id="504cd-2154">ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2155">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2155">Checksum</span></span>

<span data-ttu-id="504cd-2156">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2156">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2157">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2157">Definition</span></span>

<span data-ttu-id="504cd-2158">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2158">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2159">функция Func_iban находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2159">The function Func_iban finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2160">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2160">The checksum passes.</span></span>

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2161">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2161">Keywords</span></span>

<span data-ttu-id="504cd-2162">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2162">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="504cd-2163">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="504cd-2163">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2164">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2164">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="504cd-2165">IPv4</span><span class="sxs-lookup"><span data-stu-id="504cd-2165">IPv4:</span></span>
<span data-ttu-id="504cd-2166">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="504cd-2166">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="504cd-2167">Поддерживающ</span><span class="sxs-lookup"><span data-stu-id="504cd-2167">IPv6:</span></span>
<span data-ttu-id="504cd-2168"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="504cd-2168">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2169">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2169">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2170">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2170">Checksum</span></span>

<span data-ttu-id="504cd-2171">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2171">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2172">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2172">Definition</span></span>

<span data-ttu-id="504cd-2173">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2173">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2174">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2174">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2175">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="504cd-2175">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="504cd-2176">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2176">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2177">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2177">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2178">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="504cd-2178">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="504cd-2179">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2179">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2180">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2180">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2181">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="504cd-2181">No keyword from Keyword_ipaddress is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2182">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2182">Keywords</span></span>

#### <a name="keywordipaddress"></a><span data-ttu-id="504cd-2183">Кэйворд_ипаддресс</span><span class="sxs-lookup"><span data-stu-id="504cd-2183">Keyword_ipaddress</span></span>

- <span data-ttu-id="504cd-2184">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-2184">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="504cd-2185">ip address</span><span class="sxs-lookup"><span data-stu-id="504cd-2185">ip address</span></span> 
- <span data-ttu-id="504cd-2186">ip addresses</span><span class="sxs-lookup"><span data-stu-id="504cd-2186">ip addresses</span></span>
- <span data-ttu-id="504cd-2187">internet protocol</span><span class="sxs-lookup"><span data-stu-id="504cd-2187">internet protocol</span></span>
- <span data-ttu-id="504cd-2188">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="504cd-2188">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="504cd-2189">Международная классификация Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="504cd-2189">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2190">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2190">Format</span></span>

<span data-ttu-id="504cd-2191">Dictionary</span><span class="sxs-lookup"><span data-stu-id="504cd-2191">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2192">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2192">Pattern</span></span>

<span data-ttu-id="504cd-2193">Недопустим</span><span class="sxs-lookup"><span data-stu-id="504cd-2193">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2194">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2194">Checksum</span></span>

<span data-ttu-id="504cd-2195">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2195">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2196">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2196">Definition</span></span>

<span data-ttu-id="504cd-2197">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2197">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2198">Найдено ключевое слово из Dictionary_icd_10_cm.</span><span class="sxs-lookup"><span data-stu-id="504cd-2198">A keyword from Dictionary_icd_10_cm is found.</span></span>

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="504cd-2199">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2199">Keywords</span></span>

<span data-ttu-id="504cd-2200">Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятОй редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="504cd-2200">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="504cd-2201">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="504cd-2201">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="504cd-2202">Международная классификация Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="504cd-2202">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2203">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2203">Format</span></span>

<span data-ttu-id="504cd-2204">Dictionary</span><span class="sxs-lookup"><span data-stu-id="504cd-2204">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2205">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2205">Pattern</span></span>

<span data-ttu-id="504cd-2206">Недопустим</span><span class="sxs-lookup"><span data-stu-id="504cd-2206">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2207">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2207">Checksum</span></span>

<span data-ttu-id="504cd-2208">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2208">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2209">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2209">Definition</span></span>

<span data-ttu-id="504cd-2210">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2210">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2211">Найдено ключевое слово из Dictionary_icd_9_cm.</span><span class="sxs-lookup"><span data-stu-id="504cd-2211">A keyword from Dictionary_icd_9_cm is found.</span></span>

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2212">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2212">Keywords</span></span>

<span data-ttu-id="504cd-2213">Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятОй редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="504cd-2213">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="504cd-2214">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="504cd-2214">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="504cd-2215">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="504cd-2215">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2216">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2216">Format</span></span>

<span data-ttu-id="504cd-2217">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="504cd-2217">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="504cd-2218">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="504cd-2218">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="504cd-2219">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="504cd-2219">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="504cd-2220">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="504cd-2220">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2221">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2221">Pattern</span></span>

<span data-ttu-id="504cd-2222">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="504cd-2222">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="504cd-2223">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-2223">Seven digits</span></span> 
- <span data-ttu-id="504cd-2224">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="504cd-2224">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="504cd-2225">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="504cd-2225">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="504cd-2226">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-2226">Seven digits</span></span> 
- <span data-ttu-id="504cd-2227">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="504cd-2227">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="504cd-2228">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="504cd-2228">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2229">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2229">Checksum</span></span>

<span data-ttu-id="504cd-2230">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2230">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2231">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2231">Definition</span></span>

<span data-ttu-id="504cd-2232">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2232">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2233">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-2233">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2234">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-2234">One of the following is true:</span></span>
    - <span data-ttu-id="504cd-2235">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="504cd-2235">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="504cd-2236">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-2236">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="504cd-2237">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2237">The checksum passes.</span></span>

<span data-ttu-id="504cd-2238">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2238">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2239">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2239">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2240">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2240">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2241">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2241">Keywords</span></span>

#### <a name="keywordirelandpps"></a><span data-ttu-id="504cd-2242">Кэйворд_иреланд_ппс</span><span class="sxs-lookup"><span data-stu-id="504cd-2242">Keyword_ireland_pps</span></span>

- <span data-ttu-id="504cd-2243">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2243">Personal Public Service Number</span></span> 
- <span data-ttu-id="504cd-2244">PPS Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2244">PPS Number</span></span> 
- <span data-ttu-id="504cd-2245">PPS Num</span><span class="sxs-lookup"><span data-stu-id="504cd-2245">PPS Num</span></span> 
- <span data-ttu-id="504cd-2246">PPS No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2246">PPS No.</span></span> 
- <span data-ttu-id="504cd-2247">PPS #</span><span class="sxs-lookup"><span data-stu-id="504cd-2247">PPS #</span></span> 
- <span data-ttu-id="504cd-2248">PPS</span><span class="sxs-lookup"><span data-stu-id="504cd-2248">PPS#</span></span> 
- <span data-ttu-id="504cd-2249">ППСН</span><span class="sxs-lookup"><span data-stu-id="504cd-2249">PPSN</span></span> 
- <span data-ttu-id="504cd-2250">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2250">Public Services Card</span></span> 
- <span data-ttu-id="504cd-2251">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="504cd-2251">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="504cd-2252">Уимх.</span><span class="sxs-lookup"><span data-stu-id="504cd-2252">Uimh.</span></span> <span data-ttu-id="504cd-2253">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="504cd-2253">PSP</span></span> 
- <span data-ttu-id="504cd-2254">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="504cd-2254">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="504cd-2255">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="504cd-2255">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2256">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2256">Format</span></span>

<span data-ttu-id="504cd-2257">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2257">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2258">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2258">Pattern</span></span>

<span data-ttu-id="504cd-2259">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="504cd-2259">Formatted:</span></span>
- <span data-ttu-id="504cd-2260">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2260">Two digits</span></span> 
- <span data-ttu-id="504cd-2261">Тире</span><span class="sxs-lookup"><span data-stu-id="504cd-2261">A dash</span></span> 
- <span data-ttu-id="504cd-2262">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2262">Three digits</span></span> 
- <span data-ttu-id="504cd-2263">Тире</span><span class="sxs-lookup"><span data-stu-id="504cd-2263">A dash</span></span> 
- <span data-ttu-id="504cd-2264">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2264">Eight digits</span></span>

<span data-ttu-id="504cd-2265">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="504cd-2265">Unformatted:</span></span>
- <span data-ttu-id="504cd-2266">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2266">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2267">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2267">Checksum</span></span>

<span data-ttu-id="504cd-2268">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2268">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2269">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2269">Definition</span></span>

<span data-ttu-id="504cd-2270">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2270">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2271">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2271">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2272">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-2272">A keyword from Keyword_israel_bank_account_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2273">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2273">Keywords</span></span>

#### <a name="keywordisraelbankaccountnumber"></a><span data-ttu-id="504cd-2274">Кэйворд_исраел_банк_аккаунт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2274">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="504cd-2275">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2275">Bank Account Number</span></span> 
- <span data-ttu-id="504cd-2276">Bank Account</span><span class="sxs-lookup"><span data-stu-id="504cd-2276">Bank Account</span></span> 
- <span data-ttu-id="504cd-2277">Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2277">Account Number</span></span> 
- <span data-ttu-id="504cd-2278">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="504cd-2278">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="504cd-2279">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="504cd-2279">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2280">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2280">Format</span></span>

<span data-ttu-id="504cd-2281">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2281">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2282">Pattern</span></span>

<span data-ttu-id="504cd-2283">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2283">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2284">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2284">Checksum</span></span>

<span data-ttu-id="504cd-2285">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2285">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2286">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2286">Definition</span></span>

<span data-ttu-id="504cd-2287">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2287">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2288">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2288">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2289">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="504cd-2289">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="504cd-2290">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2290">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2291">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2291">Keywords</span></span>

#### <a name="keywordisraelnationalid"></a><span data-ttu-id="504cd-2292">Кэйворд_исраел_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-2292">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="504cd-2293">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="504cd-2293">מספר זהות</span></span> 
- <span data-ttu-id="504cd-2294">National ID Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2294">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="504cd-2295">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="504cd-2295">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2296">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2296">Format</span></span>

<span data-ttu-id="504cd-2297">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2297">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2298">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2298">Pattern</span></span>

- <span data-ttu-id="504cd-2299">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2299">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="504cd-2300">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-2300">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2301">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-2301">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2302">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="504cd-2302">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="504cd-2303">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-2303">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2304">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2304">Checksum</span></span>

<span data-ttu-id="504cd-2305">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2305">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2306">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2306">Definition</span></span>

<span data-ttu-id="504cd-2307">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2307">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2308">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2308">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2309">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-2309">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2310">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2310">Keywords</span></span>

#### <a name="keyworditalydriverslicensenumber"></a><span data-ttu-id="504cd-2311">Кэйворд_итали_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2311">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="504cd-2312">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="504cd-2312">numero di patente di guida</span></span> 
- <span data-ttu-id="504cd-2313">patente di guida</span><span class="sxs-lookup"><span data-stu-id="504cd-2313">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="504cd-2314">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="504cd-2314">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2315">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2315">Format</span></span>

<span data-ttu-id="504cd-2316">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2316">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2317">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2317">Pattern</span></span>

<span data-ttu-id="504cd-2318">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="504cd-2318">Bank account number:</span></span>
- <span data-ttu-id="504cd-2319">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2319">Seven or eight digits</span></span>
- <span data-ttu-id="504cd-2320">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="504cd-2320">Bank account branch code:</span></span>
- <span data-ttu-id="504cd-2321">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2321">Four digits</span></span> 
- <span data-ttu-id="504cd-2322">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="504cd-2322">A space or dash (optional)</span></span> 
- <span data-ttu-id="504cd-2323">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2323">Three digits</span></span>

<span data-ttu-id="504cd-2324">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2324">Checksum</span></span>

<span data-ttu-id="504cd-2325">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2325">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2326">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2326">Definition</span></span>

<span data-ttu-id="504cd-2327">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2327">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2328">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-2328">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2329">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="504cd-2329">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="504cd-2330">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-2330">One of the following is true:</span></span>
- <span data-ttu-id="504cd-2331">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2331">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2332">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="504cd-2332">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="504cd-2333">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2333">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2334">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2334">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2335">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="504cd-2335">A keyword from Keyword_jp_bank_account is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2336">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2336">Keywords</span></span>

#### <a name="keywordjpbankaccount"></a><span data-ttu-id="504cd-2337">Кэйворд_жп_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="504cd-2337">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="504cd-2338">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2338">Checking Account Number</span></span> 
- <span data-ttu-id="504cd-2339">Checking Account</span><span class="sxs-lookup"><span data-stu-id="504cd-2339">Checking Account</span></span> 
- <span data-ttu-id="504cd-2340">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-2340">Checking Account #</span></span> 
- <span data-ttu-id="504cd-2341">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2341">Checking Acct Number</span></span> 
- <span data-ttu-id="504cd-2342">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-2342">Checking Acct #</span></span> 
- <span data-ttu-id="504cd-2343">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2343">Checking Acct No.</span></span> 
- <span data-ttu-id="504cd-2344">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2344">Checking Account No.</span></span> 
- <span data-ttu-id="504cd-2345">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2345">Bank Account Number</span></span> 
- <span data-ttu-id="504cd-2346">Bank Account</span><span class="sxs-lookup"><span data-stu-id="504cd-2346">Bank Account</span></span> 
- <span data-ttu-id="504cd-2347">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-2347">Bank Account #</span></span> 
- <span data-ttu-id="504cd-2348">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2348">Bank Acct Number</span></span> 
- <span data-ttu-id="504cd-2349">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-2349">Bank Acct #</span></span> 
- <span data-ttu-id="504cd-2350">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2350">Bank Acct No.</span></span> 
- <span data-ttu-id="504cd-2351">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2351">Bank Account No.</span></span> 
- <span data-ttu-id="504cd-2352">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2352">Savings Account Number</span></span> 
- <span data-ttu-id="504cd-2353">Savings Account</span><span class="sxs-lookup"><span data-stu-id="504cd-2353">Savings Account</span></span> 
- <span data-ttu-id="504cd-2354">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-2354">Savings Account #</span></span> 
- <span data-ttu-id="504cd-2355">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2355">Savings Acct Number</span></span> 
- <span data-ttu-id="504cd-2356">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-2356">Savings Acct #</span></span> 
- <span data-ttu-id="504cd-2357">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2357">Savings Acct No.</span></span> 
- <span data-ttu-id="504cd-2358">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2358">Savings Account No.</span></span> 
- <span data-ttu-id="504cd-2359">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2359">Debit Account Number</span></span> 
- <span data-ttu-id="504cd-2360">Debit Account</span><span class="sxs-lookup"><span data-stu-id="504cd-2360">Debit Account</span></span> 
- <span data-ttu-id="504cd-2361">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-2361">Debit Account #</span></span> 
- <span data-ttu-id="504cd-2362">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2362">Debit Acct Number</span></span> 
- <span data-ttu-id="504cd-2363">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-2363">Debit Acct #</span></span> 
- <span data-ttu-id="504cd-2364">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2364">Debit Acct No.</span></span> 
- <span data-ttu-id="504cd-2365">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2365">Debit Account No.</span></span> 
- <span data-ttu-id="504cd-2366">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="504cd-2366">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="504cd-2367">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="504cd-2367">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="504cd-2368">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="504cd-2368">＃勘定の確認</span></span> 
- <span data-ttu-id="504cd-2369">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="504cd-2369">勘定番号の確認</span></span> 
- <span data-ttu-id="504cd-2370">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="504cd-2370">口座番号の確認</span></span> 
- <span data-ttu-id="504cd-2371">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2371">銀行口座番号</span></span> 
- <span data-ttu-id="504cd-2372">銀行口座</span><span class="sxs-lookup"><span data-stu-id="504cd-2372">銀行口座</span></span> 
- <span data-ttu-id="504cd-2373">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2373">銀行口座＃</span></span> 
- <span data-ttu-id="504cd-2374">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2374">銀行の勘定番号</span></span> 
- <span data-ttu-id="504cd-2375">銀行のаккт #</span><span class="sxs-lookup"><span data-stu-id="504cd-2375">銀行のacct＃</span></span> 
- <span data-ttu-id="504cd-2376">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="504cd-2376">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="504cd-2377">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2377">銀行口座番号</span></span>
- <span data-ttu-id="504cd-2378">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2378">普通預金口座番号</span></span> 
- <span data-ttu-id="504cd-2379">預金口座</span><span class="sxs-lookup"><span data-stu-id="504cd-2379">預金口座</span></span> 
- <span data-ttu-id="504cd-2380">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2380">貯蓄口座＃</span></span> 
- <span data-ttu-id="504cd-2381">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="504cd-2381">貯蓄勘定の数</span></span> 
- <span data-ttu-id="504cd-2382">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2382">貯蓄勘定＃</span></span> 
- <span data-ttu-id="504cd-2383">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2383">貯蓄勘定番号</span></span> 
- <span data-ttu-id="504cd-2384">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2384">普通預金口座番号</span></span> 
- <span data-ttu-id="504cd-2385">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2385">引き落とし口座番号</span></span> 
- <span data-ttu-id="504cd-2386">口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2386">口座番号</span></span> 
- <span data-ttu-id="504cd-2387">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2387">口座番号＃</span></span> 
- <span data-ttu-id="504cd-2388">デビットのаккт番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2388">デビットのacct番号</span></span> 
- <span data-ttu-id="504cd-2389">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2389">デビット勘定＃</span></span> 
- <span data-ttu-id="504cd-2390">デビットакктの番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2390">デビットACCTの番号</span></span> 
- <span data-ttu-id="504cd-2391">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2391">デビット口座番号</span></span> 

#### <a name="keywordjpbankbranchcode"></a><span data-ttu-id="504cd-2392">Кэйворд_жп_банк_бранч_коде</span><span class="sxs-lookup"><span data-stu-id="504cd-2392">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="504cd-2393">Отемачи</span><span class="sxs-lookup"><span data-stu-id="504cd-2393">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="504cd-2394">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="504cd-2394">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2395">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2395">Format</span></span>

<span data-ttu-id="504cd-2396">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2396">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2397">Pattern</span></span>

<span data-ttu-id="504cd-2398">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2398">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2399">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2399">Checksum</span></span>

<span data-ttu-id="504cd-2400">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2400">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2401">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2401">Definition</span></span>

<span data-ttu-id="504cd-2402">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2402">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2403">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2403">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2404">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-2404">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2405">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2405">Keywords</span></span>

#### <a name="keywordjpdriverslicensenumber"></a><span data-ttu-id="504cd-2406">Кэйворд_жп_дриверс_лиценсе_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2406">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="504cd-2407">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-2407">dl#</span></span> 
- <span data-ttu-id="504cd-2408">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-2408">DL＃</span></span> 
- <span data-ttu-id="504cd-2409">библиотек</span><span class="sxs-lookup"><span data-stu-id="504cd-2409">dls#</span></span> 
- <span data-ttu-id="504cd-2410">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="504cd-2410">DLS＃</span></span> 
- <span data-ttu-id="504cd-2411">driver license</span><span class="sxs-lookup"><span data-stu-id="504cd-2411">driver license</span></span> 
- <span data-ttu-id="504cd-2412">driver licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-2412">driver licenses</span></span> 
- <span data-ttu-id="504cd-2413">drivers license</span><span class="sxs-lookup"><span data-stu-id="504cd-2413">drivers license</span></span> 
- <span data-ttu-id="504cd-2414">driver's license</span><span class="sxs-lookup"><span data-stu-id="504cd-2414">driver's license</span></span> 
- <span data-ttu-id="504cd-2415">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-2415">drivers licenses</span></span> 
- <span data-ttu-id="504cd-2416">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-2416">driver's licenses</span></span> 
- <span data-ttu-id="504cd-2417">driving licence</span><span class="sxs-lookup"><span data-stu-id="504cd-2417">driving licence</span></span> 
- <span data-ttu-id="504cd-2418">Лик #</span><span class="sxs-lookup"><span data-stu-id="504cd-2418">lic#</span></span> 
- <span data-ttu-id="504cd-2419">Лик #</span><span class="sxs-lookup"><span data-stu-id="504cd-2419">LIC＃</span></span> 
- <span data-ttu-id="504cd-2420">ликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-2420">lics#</span></span> 
- <span data-ttu-id="504cd-2421">state id</span><span class="sxs-lookup"><span data-stu-id="504cd-2421">state id</span></span> 
- <span data-ttu-id="504cd-2422">state identification</span><span class="sxs-lookup"><span data-stu-id="504cd-2422">state identification</span></span> 
- <span data-ttu-id="504cd-2423">state identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-2423">state identification number</span></span> 
- <span data-ttu-id="504cd-2424">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2424">低所得国＃</span></span> 
- <span data-ttu-id="504cd-2425">免許証</span><span class="sxs-lookup"><span data-stu-id="504cd-2425">免許証</span></span> 
- <span data-ttu-id="504cd-2426">状態ид</span><span class="sxs-lookup"><span data-stu-id="504cd-2426">状態ID</span></span>
- <span data-ttu-id="504cd-2427">状態の識別</span><span class="sxs-lookup"><span data-stu-id="504cd-2427">状態の識別</span></span> 
- <span data-ttu-id="504cd-2428">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2428">状態の識別番号</span></span> 
- <span data-ttu-id="504cd-2429">運転免許</span><span class="sxs-lookup"><span data-stu-id="504cd-2429">運転免許</span></span> 
- <span data-ttu-id="504cd-2430">運転免許証</span><span class="sxs-lookup"><span data-stu-id="504cd-2430">運転免許証</span></span> 
- <span data-ttu-id="504cd-2431">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2431">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="504cd-2432">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="504cd-2432">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2433">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2433">Format</span></span>

<span data-ttu-id="504cd-2434">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2434">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2435">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2435">Pattern</span></span>

<span data-ttu-id="504cd-2436">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2436">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2437">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2437">Checksum</span></span>

<span data-ttu-id="504cd-2438">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2438">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2439">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2439">Definition</span></span>

<span data-ttu-id="504cd-2440">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2441">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2441">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2442">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="504cd-2442">A keyword from Keyword_jp_passport is found.</span></span>

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2443">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2443">Keywords</span></span>

#### <a name="keywordjppassport"></a><span data-ttu-id="504cd-2444">Кэйворд_жп_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-2444">Keyword_jp_passport</span></span>

- <span data-ttu-id="504cd-2445">パスポート</span><span class="sxs-lookup"><span data-stu-id="504cd-2445">パスポート</span></span> 
- <span data-ttu-id="504cd-2446">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2446">パスポート番号</span></span> 
- <span data-ttu-id="504cd-2447">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="504cd-2447">パスポートのNum</span></span> 
- <span data-ttu-id="504cd-2448">パスポート #</span><span class="sxs-lookup"><span data-stu-id="504cd-2448">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="504cd-2449">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="504cd-2449">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2450">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2450">Format</span></span>

<span data-ttu-id="504cd-2451">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2451">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2452">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2452">Pattern</span></span>

<span data-ttu-id="504cd-2453">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2453">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2454">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2454">Checksum</span></span>

<span data-ttu-id="504cd-2455">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2455">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2456">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2456">Definition</span></span>

<span data-ttu-id="504cd-2457">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2458">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2458">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2459">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-2459">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2460">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2460">Keywords</span></span>

#### <a name="keywordjpresidentregistrationnumber"></a><span data-ttu-id="504cd-2461">Кэйворд_жп_ресидент_регистратион_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2461">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="504cd-2462">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2462">Resident Registration Number</span></span>
- <span data-ttu-id="504cd-2463">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2463">Resident Register Number</span></span> 
- <span data-ttu-id="504cd-2464">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2464">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="504cd-2465">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2465">Resident Registration No.</span></span> 
- <span data-ttu-id="504cd-2466">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2466">Resident Register No.</span></span> 
- <span data-ttu-id="504cd-2467">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2467">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="504cd-2468">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2468">Basic Resident Register No.</span></span> 
- <span data-ttu-id="504cd-2469">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="504cd-2469">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="504cd-2470">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2470">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="504cd-2471">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="504cd-2471">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="504cd-2472">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2472">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="504cd-2473">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2473">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2474">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2474">Format</span></span>

<span data-ttu-id="504cd-2475">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2475">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2476">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2476">Pattern</span></span>

<span data-ttu-id="504cd-2477">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2477">7-12 digits:</span></span>
- <span data-ttu-id="504cd-2478">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2478">Four digits</span></span> 
- <span data-ttu-id="504cd-2479">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="504cd-2479">A hyphen (optional)</span></span> 
- <span data-ttu-id="504cd-2480">Шесть цифр или</span><span class="sxs-lookup"><span data-stu-id="504cd-2480">Six digits OR</span></span>
- <span data-ttu-id="504cd-2481">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2481">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2482">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2482">Checksum</span></span>

<span data-ttu-id="504cd-2483">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2483">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2484">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2484">Definition</span></span>

<span data-ttu-id="504cd-2485">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2485">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2486">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2486">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2487">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="504cd-2487">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="504cd-2488">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2488">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2489">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2489">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2490">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="504cd-2490">A keyword from Keyword_jp_sin is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2491">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2491">Keywords</span></span>

#### <a name="keywordjpsin"></a><span data-ttu-id="504cd-2492">Кэйворд_жп_син</span><span class="sxs-lookup"><span data-stu-id="504cd-2492">Keyword_jp_sin</span></span>

- <span data-ttu-id="504cd-2493">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="504cd-2493">Social Insurance No.</span></span> 
- <span data-ttu-id="504cd-2494">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="504cd-2494">Social Insurance Num</span></span> 
- <span data-ttu-id="504cd-2495">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2495">Social Insurance Number</span></span> 
- <span data-ttu-id="504cd-2496">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="504cd-2496">社会保険のテンキー</span></span> 
- <span data-ttu-id="504cd-2497">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2497">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="504cd-2498">Номер карточки для японского языка</span><span class="sxs-lookup"><span data-stu-id="504cd-2498">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2499">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2499">Format</span></span>

<span data-ttu-id="504cd-2500">12 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2500">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2501">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2501">Pattern</span></span>

<span data-ttu-id="504cd-2502">12 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2502">12 letters and digits:</span></span>
- <span data-ttu-id="504cd-2503">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-2503">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="504cd-2504">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2504">Eight digits</span></span> 
- <span data-ttu-id="504cd-2505">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-2505">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2506">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2506">Checksum</span></span>

<span data-ttu-id="504cd-2507">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2507">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2508">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2508">Definition</span></span>

<span data-ttu-id="504cd-2509">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2509">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2510">Регулярное выражение Режекс_жп_ресиденце_кард_нумбер находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2510">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2511">Найдено ключевое слово из Кэйворд_жп_ресиденце_кард_нумбер.</span><span class="sxs-lookup"><span data-stu-id="504cd-2511">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2512">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2512">Keywords</span></span>

#### <a name="keywordjpresidencecardnumber"></a><span data-ttu-id="504cd-2513">Кэйворд_жп_ресиденце_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2513">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="504cd-2514">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="504cd-2514">Residence card number</span></span>
- <span data-ttu-id="504cd-2515">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="504cd-2515">Residence card no</span></span>
- <span data-ttu-id="504cd-2516">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="504cd-2516">Residence card #</span></span>
- <span data-ttu-id="504cd-2517">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2517">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="504cd-2518">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="504cd-2518">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2519">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2519">Format</span></span>

<span data-ttu-id="504cd-2520">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="504cd-2520">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2521">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2521">Pattern</span></span>

<span data-ttu-id="504cd-2522">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2522">12 digits:</span></span>
- <span data-ttu-id="504cd-2523">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="504cd-2523">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="504cd-2524">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="504cd-2524">A dash (optional)</span></span> 
- <span data-ttu-id="504cd-2525">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="504cd-2525">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="504cd-2526">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="504cd-2526">A dash (optional)</span></span> 
- <span data-ttu-id="504cd-2527">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-2527">Three random digits</span></span> 
- <span data-ttu-id="504cd-2528">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2528">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2529">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2529">Checksum</span></span>

<span data-ttu-id="504cd-2530">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2530">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2531">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2531">Definition</span></span>

<span data-ttu-id="504cd-2532">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2532">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2533">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2533">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2534">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="504cd-2534">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2535">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2535">Keywords</span></span>
   
#### <a name="keywordmalaysiaidcardnumber"></a><span data-ttu-id="504cd-2536">Кэйворд_малайсиа_ид_кард_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2536">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="504cd-2537">карточка цифрового приложения</span><span class="sxs-lookup"><span data-stu-id="504cd-2537">digital application card</span></span>
- <span data-ttu-id="504cd-2538">i/c</span><span class="sxs-lookup"><span data-stu-id="504cd-2538">i/c</span></span>
- <span data-ttu-id="504cd-2539">i/c нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2539">i/c no</span></span>
- <span data-ttu-id="504cd-2540">внутренних</span><span class="sxs-lookup"><span data-stu-id="504cd-2540">ic</span></span>
- <span data-ttu-id="504cd-2541">МФ нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2541">ic no</span></span>
- <span data-ttu-id="504cd-2542">id card</span><span class="sxs-lookup"><span data-stu-id="504cd-2542">id card</span></span>
- <span data-ttu-id="504cd-2543">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="504cd-2543">identification Card</span></span>
- <span data-ttu-id="504cd-2544">identity card</span><span class="sxs-lookup"><span data-stu-id="504cd-2544">identity card</span></span>
- <span data-ttu-id="504cd-2545">k/p</span><span class="sxs-lookup"><span data-stu-id="504cd-2545">k/p</span></span>
- <span data-ttu-id="504cd-2546">k/p</span><span class="sxs-lookup"><span data-stu-id="504cd-2546">k/p no</span></span>
- <span data-ttu-id="504cd-2547">кад акуан Дири</span><span class="sxs-lookup"><span data-stu-id="504cd-2547">kad akuan diri</span></span>
- <span data-ttu-id="504cd-2548">кад апликаси Digital</span><span class="sxs-lookup"><span data-stu-id="504cd-2548">kad aplikasi digital</span></span>
- <span data-ttu-id="504cd-2549">кад пенженалан Малайзии</span><span class="sxs-lookup"><span data-stu-id="504cd-2549">kad pengenalan malaysia</span></span>
- <span data-ttu-id="504cd-2550">ключев</span><span class="sxs-lookup"><span data-stu-id="504cd-2550">kp</span></span>
- <span data-ttu-id="504cd-2551">ключевой номер</span><span class="sxs-lookup"><span data-stu-id="504cd-2551">kp no</span></span>
- <span data-ttu-id="504cd-2552">микад</span><span class="sxs-lookup"><span data-stu-id="504cd-2552">mykad</span></span>
- <span data-ttu-id="504cd-2553">Микас</span><span class="sxs-lookup"><span data-stu-id="504cd-2553">mykas</span></span>
- <span data-ttu-id="504cd-2554">микид</span><span class="sxs-lookup"><span data-stu-id="504cd-2554">mykid</span></span>
- <span data-ttu-id="504cd-2555">МИПР</span><span class="sxs-lookup"><span data-stu-id="504cd-2555">mypr</span></span>
- <span data-ttu-id="504cd-2556">митентера</span><span class="sxs-lookup"><span data-stu-id="504cd-2556">mytentera</span></span>
- <span data-ttu-id="504cd-2557">идентификационная карточка Малайзии</span><span class="sxs-lookup"><span data-stu-id="504cd-2557">malaysia identity card</span></span>
- <span data-ttu-id="504cd-2558">идентификационная карточка малайсиан</span><span class="sxs-lookup"><span data-stu-id="504cd-2558">malaysian identity card</span></span>
- <span data-ttu-id="504cd-2559">NRIC</span><span class="sxs-lookup"><span data-stu-id="504cd-2559">nric</span></span>
- <span data-ttu-id="504cd-2560">Личная идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="504cd-2560">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="504cd-2561">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2561">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2562">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2562">Format</span></span>

<span data-ttu-id="504cd-2563">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="504cd-2563">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2564">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2564">Pattern</span></span>

<span data-ttu-id="504cd-2565">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2565">8-9 digits:</span></span>
- <span data-ttu-id="504cd-2566">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-2566">Three digits</span></span> 
- <span data-ttu-id="504cd-2567">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="504cd-2567">A space (optional)</span></span> 
- <span data-ttu-id="504cd-2568">три цифры; </span><span class="sxs-lookup"><span data-stu-id="504cd-2568">Three digits</span></span> 
- <span data-ttu-id="504cd-2569">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="504cd-2569">A space (optional)</span></span> 
- <span data-ttu-id="504cd-2570">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2570">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2571">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2571">Checksum</span></span>

<span data-ttu-id="504cd-2572">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2572">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2573">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2573">Definition</span></span>

<span data-ttu-id="504cd-2574">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2574">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2575">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2575">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2576">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="504cd-2576">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="504cd-2577">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-2577">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="504cd-2578">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2578">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2579">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2579">Keywords</span></span>

#### <a name="keywordnetherlandsbsn"></a><span data-ttu-id="504cd-2580">Кэйворд_несерландс_бсн</span><span class="sxs-lookup"><span data-stu-id="504cd-2580">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="504cd-2581">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="504cd-2581">Citizen service number</span></span> 
- <span data-ttu-id="504cd-2582">BSN</span><span class="sxs-lookup"><span data-stu-id="504cd-2582">BSN</span></span> 
- <span data-ttu-id="504cd-2583">Буржерсервиценуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-2583">Burgerservicenummer</span></span> 
- <span data-ttu-id="504cd-2584">Софинуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-2584">Sofinummer</span></span> 
- <span data-ttu-id="504cd-2585">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="504cd-2585">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="504cd-2586">Персунснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-2586">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="504cd-2587">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="504cd-2587">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2588">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2588">Format</span></span>

<span data-ttu-id="504cd-2589">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2589">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2590">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2590">Pattern</span></span>

<span data-ttu-id="504cd-2591">Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2591">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2592">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2592">Checksum</span></span>

<span data-ttu-id="504cd-2593">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2593">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2594">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2594">Definition</span></span>

<span data-ttu-id="504cd-2595">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2595">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2596">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2596">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2597">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="504cd-2597">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="504cd-2598">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2598">The checksum passes.</span></span>

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

<span data-ttu-id="504cd-2599">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2599">Keywords</span></span>

<span data-ttu-id="504cd-2600">Кэйворд_нз_термс</span><span class="sxs-lookup"><span data-stu-id="504cd-2600">Keyword_nz_terms</span></span>

- <span data-ttu-id="504cd-2601">НХИ</span><span class="sxs-lookup"><span data-stu-id="504cd-2601">NHI</span></span> 
- <span data-ttu-id="504cd-2602">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="504cd-2602">New Zealand</span></span> 
- <span data-ttu-id="504cd-2603">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="504cd-2603">Health</span></span> 
- <span data-ttu-id="504cd-2604">обращения</span><span class="sxs-lookup"><span data-stu-id="504cd-2604">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="504cd-2605">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="504cd-2605">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2606">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2606">Format</span></span>

<span data-ttu-id="504cd-2607">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2607">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2608">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2608">Pattern</span></span>

<span data-ttu-id="504cd-2609">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2609">11 digits:</span></span>
- <span data-ttu-id="504cd-2610">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="504cd-2610">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="504cd-2611">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-2611">Three-digit individual number</span></span> 
- <span data-ttu-id="504cd-2612">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2612">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2613">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2613">Checksum</span></span>

<span data-ttu-id="504cd-2614">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2614">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2615">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2615">Definition</span></span>

<span data-ttu-id="504cd-2616">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2616">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2617">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2617">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2618">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2618">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="504cd-2619">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2619">The checksum passes.</span></span>
- <span data-ttu-id="504cd-2620">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2620">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2621">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2621">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2622">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2622">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2623">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2623">Keywords</span></span>

#### <a name="keywordnorwayidnumber"></a><span data-ttu-id="504cd-2624">Кэйворд_норвай_ид_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2624">Keyword_norway_id_number</span></span>

- <span data-ttu-id="504cd-2625">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-2625">Personal identification number</span></span>
- <span data-ttu-id="504cd-2626">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2626">Norwegian ID Number</span></span>
- <span data-ttu-id="504cd-2627">ID Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2627">ID Number</span></span>
- <span data-ttu-id="504cd-2628">Процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-2628">Identification</span></span>
- <span data-ttu-id="504cd-2629">Персоннуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-2629">Personnummer</span></span>
- <span data-ttu-id="504cd-2630">Фøдселснуммер</span><span class="sxs-lookup"><span data-stu-id="504cd-2630">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="504cd-2631">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="504cd-2631">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2632">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2632">Format</span></span>

<span data-ttu-id="504cd-2633">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="504cd-2633">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2634">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2634">Pattern</span></span>

<span data-ttu-id="504cd-2635">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2635">12 digits:</span></span>
- <span data-ttu-id="504cd-2636">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-2636">Four digits</span></span> 
- <span data-ttu-id="504cd-2637">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-2637">A hyphen</span></span> 
- <span data-ttu-id="504cd-2638">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-2638">Seven digits</span></span> 
- <span data-ttu-id="504cd-2639">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-2639">A hyphen</span></span> 
- <span data-ttu-id="504cd-2640">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="504cd-2640">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2641">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2641">Checksum</span></span>

<span data-ttu-id="504cd-2642">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2642">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2643">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2643">Definition</span></span>

<span data-ttu-id="504cd-2644">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2644">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2645">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2645">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2646">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="504cd-2646">A keyword from Keyword_philippines_id is found.</span></span>

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2647">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2647">Keywords</span></span>
   
#### <a name="keywordphilippinesid"></a><span data-ttu-id="504cd-2648">Кэйворд_филиппинес_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-2648">Keyword_philippines_id</span></span>

- <span data-ttu-id="504cd-2649">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="504cd-2649">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="504cd-2650">Умид</span><span class="sxs-lookup"><span data-stu-id="504cd-2650">UMID</span></span> 
- <span data-ttu-id="504cd-2651">Identity Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2651">Identity Card</span></span> 
- <span data-ttu-id="504cd-2652">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="504cd-2652">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="504cd-2653">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="504cd-2653">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2654">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2654">Format</span></span>

<span data-ttu-id="504cd-2655">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2655">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2656">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2656">Pattern</span></span>

<span data-ttu-id="504cd-2657">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2657">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2658">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2658">Checksum</span></span>

<span data-ttu-id="504cd-2659">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2659">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2660">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2660">Definition</span></span>

<span data-ttu-id="504cd-2661">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_полиш_натионал_ид находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2661">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="504cd-2662">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2662">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="504cd-2663">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2663">The checksum passes.</span></span>

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2664">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2664">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="504cd-2665">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2665">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="504cd-2666">Довóд особисти</span><span class="sxs-lookup"><span data-stu-id="504cd-2666">Dowód osobisty</span></span>
- <span data-ttu-id="504cd-2667">Нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="504cd-2667">Numer dowodu osobistego</span></span>
- <span data-ttu-id="504cd-2668">Назва i нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="504cd-2668">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="504cd-2669">Назва i НР доводу особистего</span><span class="sxs-lookup"><span data-stu-id="504cd-2669">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="504cd-2670">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="504cd-2670">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="504cd-2671">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="504cd-2671">Dowód Tożsamości</span></span>
- <span data-ttu-id="504cd-2672">Dow.</span><span class="sxs-lookup"><span data-stu-id="504cd-2672">dow.</span></span> <span data-ttu-id="504cd-2673">совместим.</span><span class="sxs-lookup"><span data-stu-id="504cd-2673">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="504cd-2674">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="504cd-2674">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2675">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2675">Format</span></span>

<span data-ttu-id="504cd-2676">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2676">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2677">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2677">Pattern</span></span>

<span data-ttu-id="504cd-2678">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2678">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2679">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2679">Checksum</span></span>

<span data-ttu-id="504cd-2680">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2680">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2681">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2681">Definition</span></span>

<span data-ttu-id="504cd-2682">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2682">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2683">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2683">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2684">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2684">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="504cd-2685">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2685">The checksum passes.</span></span>

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2686">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2686">Keywords</span></span>

#### <a name="keywordpeselidentificationnumber"></a><span data-ttu-id="504cd-2687">Кэйворд_песел_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2687">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="504cd-2688">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="504cd-2688">Nr PESEL</span></span>
- <span data-ttu-id="504cd-2689">PESEL</span><span class="sxs-lookup"><span data-stu-id="504cd-2689">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="504cd-2690">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="504cd-2690">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2691">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2691">Format</span></span>

<span data-ttu-id="504cd-2692">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2692">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2693">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2693">Pattern</span></span>

<span data-ttu-id="504cd-2694">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2694">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2695">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2695">Checksum</span></span>

<span data-ttu-id="504cd-2696">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2696">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2697">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2697">Definition</span></span>

<span data-ttu-id="504cd-2698">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2698">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2699">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2699">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2700">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2700">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="504cd-2701">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2701">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2702">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2702">Keywords</span></span>

#### <a name="keywordpolishnationalidpassportnumber"></a><span data-ttu-id="504cd-2703">Кэйворд_полиш_натионал_ид_пасспорт_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2703">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="504cd-2704">Нумер пасзпорту</span><span class="sxs-lookup"><span data-stu-id="504cd-2704">Numer paszportu</span></span>
- <span data-ttu-id="504cd-2705">НР.</span><span class="sxs-lookup"><span data-stu-id="504cd-2705">Nr.</span></span> <span data-ttu-id="504cd-2706">Пасзпорту</span><span class="sxs-lookup"><span data-stu-id="504cd-2706">Paszportu</span></span>
- <span data-ttu-id="504cd-2707">Пасзпорт</span><span class="sxs-lookup"><span data-stu-id="504cd-2707">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="504cd-2708">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="504cd-2708">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2709">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2709">Format</span></span>

<span data-ttu-id="504cd-2710">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2710">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2711">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2711">Pattern</span></span>

<span data-ttu-id="504cd-2712">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2712">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2713">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2713">Checksum</span></span>

<span data-ttu-id="504cd-2714">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2714">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2715">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2715">Definition</span></span>

<span data-ttu-id="504cd-2716">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2716">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2717">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2717">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2718">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="504cd-2718">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2719">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2719">Keywords</span></span>

#### <a name="keywordportugalcitizencard"></a><span data-ttu-id="504cd-2720">Кэйворд_португал_Цитизен_кард</span><span class="sxs-lookup"><span data-stu-id="504cd-2720">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="504cd-2721">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2721">Citizen Card</span></span>
- <span data-ttu-id="504cd-2722">National ID Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2722">National ID Card</span></span>
- <span data-ttu-id="504cd-2723">CC</span><span class="sxs-lookup"><span data-stu-id="504cd-2723">CC</span></span>
- <span data-ttu-id="504cd-2724">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="504cd-2724">Cartão de Cidadão</span></span>
- <span data-ttu-id="504cd-2725">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="504cd-2725">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="504cd-2726">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="504cd-2726">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2727">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2727">Format</span></span>

<span data-ttu-id="504cd-2728">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2728">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2729">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2729">Pattern</span></span>

<span data-ttu-id="504cd-2730">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2730">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2731">Checksum</span></span>

<span data-ttu-id="504cd-2732">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2732">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2733">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2733">Definition</span></span>

<span data-ttu-id="504cd-2734">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2734">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2735">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2735">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2736">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="504cd-2736">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2737">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2737">Keywords</span></span>

#### <a name="keywordsaudiarabianationalid"></a><span data-ttu-id="504cd-2738">Кэйворд_сауди_арабиа_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-2738">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="504cd-2739">Identification Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2739">Identification Card</span></span> 
- <span data-ttu-id="504cd-2740">I card number</span><span class="sxs-lookup"><span data-stu-id="504cd-2740">I card number</span></span> 
- <span data-ttu-id="504cd-2741">ID number</span><span class="sxs-lookup"><span data-stu-id="504cd-2741">ID number</span></span> 
- <span data-ttu-id="504cd-2742">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="504cd-2742">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="504cd-2743">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="504cd-2743">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2744">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2744">Format</span></span>

<span data-ttu-id="504cd-2745">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2745">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2746">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2746">Pattern</span></span>

- <span data-ttu-id="504cd-2747">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2747">Nine letters and digits:</span></span>
- <span data-ttu-id="504cd-2748">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-2748">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2749">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-2749">Seven digits</span></span> 
- <span data-ttu-id="504cd-2750">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="504cd-2750">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2751">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2751">Checksum</span></span>

<span data-ttu-id="504cd-2752">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2752">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2753">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2753">Definition</span></span>

<span data-ttu-id="504cd-2754">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2754">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2755">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2755">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2756">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="504cd-2756">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="504cd-2757">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2757">The checksum passes.</span></span>

<span data-ttu-id="504cd-2758">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2758">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2759">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2759">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2760">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2760">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2761">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2761">Keywords</span></span>
   
#### <a name="keywordsingaporenric"></a><span data-ttu-id="504cd-2762">Кэйворд_сингапоре_нрик</span><span class="sxs-lookup"><span data-stu-id="504cd-2762">Keyword_singapore_nric</span></span>

- <span data-ttu-id="504cd-2763">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2763">National Registration Identity Card</span></span> 
- <span data-ttu-id="504cd-2764">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2764">Identity Card Number</span></span> 
- <span data-ttu-id="504cd-2765">NRIC</span><span class="sxs-lookup"><span data-stu-id="504cd-2765">NRIC</span></span> 
- <span data-ttu-id="504cd-2766">ВНУТРЕННИХ</span><span class="sxs-lookup"><span data-stu-id="504cd-2766">IC</span></span> 
- <span data-ttu-id="504cd-2767">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2767">Foreign Identification Number</span></span> 
- <span data-ttu-id="504cd-2768">ПРОЦЕНТ</span><span class="sxs-lookup"><span data-stu-id="504cd-2768">FIN</span></span> 
- <span data-ttu-id="504cd-2769">身份证</span><span class="sxs-lookup"><span data-stu-id="504cd-2769">身份证</span></span> 
- <span data-ttu-id="504cd-2770">身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2770">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="504cd-2771">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="504cd-2771">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2772">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2772">Format</span></span>

<span data-ttu-id="504cd-2773">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="504cd-2773">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2774">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2774">Pattern</span></span>

<span data-ttu-id="504cd-2775">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2775">13 digits:</span></span>
- <span data-ttu-id="504cd-2776">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="504cd-2776">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="504cd-2777">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-2777">Four digits</span></span> 
- <span data-ttu-id="504cd-2778">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="504cd-2778">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="504cd-2779">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="504cd-2779">The digit "8" or "9"</span></span> 
- <span data-ttu-id="504cd-2780">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="504cd-2780">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2781">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2781">Checksum</span></span>

<span data-ttu-id="504cd-2782">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2782">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2783">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2783">Definition</span></span>

<span data-ttu-id="504cd-2784">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2784">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2785">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2785">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2786">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2786">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="504cd-2787">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2787">The checksum passes.</span></span>

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2788">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2788">Keywords</span></span>
   
#### <a name="keywordsouthafricaidentificationnumber"></a><span data-ttu-id="504cd-2789">Кэйворд_саус_африка_идентификатион_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2789">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="504cd-2790">Identity card</span><span class="sxs-lookup"><span data-stu-id="504cd-2790">Identity card</span></span>
- <span data-ttu-id="504cd-2791">ИД</span><span class="sxs-lookup"><span data-stu-id="504cd-2791">ID</span></span>
- <span data-ttu-id="504cd-2792">Процедура</span><span class="sxs-lookup"><span data-stu-id="504cd-2792">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="504cd-2793">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="504cd-2793">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2794">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2794">Format</span></span>

<span data-ttu-id="504cd-2795">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="504cd-2795">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2796">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2796">Pattern</span></span>

<span data-ttu-id="504cd-2797">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2797">13 digits:</span></span>
- <span data-ttu-id="504cd-2798">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="504cd-2798">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="504cd-2799">дефис;</span><span class="sxs-lookup"><span data-stu-id="504cd-2799">A hyphen</span></span> 
- <span data-ttu-id="504cd-2800">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="504cd-2800">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="504cd-2801">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="504cd-2801">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="504cd-2802">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="504cd-2802">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="504cd-2803">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="504cd-2803">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2804">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2804">Checksum</span></span>

<span data-ttu-id="504cd-2805">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2805">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2806">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2806">Definition</span></span>

<span data-ttu-id="504cd-2807">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2807">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2808">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2808">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2809">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-2809">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="504cd-2810">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2810">The checksum passes.</span></span>

<span data-ttu-id="504cd-2811">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2811">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2812">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2812">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2813">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2813">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2814">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2814">Keywords</span></span>
   
#### <a name="keywordsouthkorearesidentnumber"></a><span data-ttu-id="504cd-2815">Кэйворд_саус_кореа_ресидент_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2815">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="504cd-2816">National ID card</span><span class="sxs-lookup"><span data-stu-id="504cd-2816">National ID card</span></span> 
- <span data-ttu-id="504cd-2817">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2817">Citizen's Registration Number</span></span> 
- <span data-ttu-id="504cd-2818">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="504cd-2818">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="504cd-2819">РРН</span><span class="sxs-lookup"><span data-stu-id="504cd-2819">RRN</span></span> 
- <span data-ttu-id="504cd-2820">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="504cd-2820">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="504cd-2821">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2821">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2822">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2822">Format</span></span>

<span data-ttu-id="504cd-2823">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2823">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2824">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2824">Pattern</span></span>

<span data-ttu-id="504cd-2825">11-12 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-2825">11-12 digits:</span></span>
- <span data-ttu-id="504cd-2826">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2826">Two digits</span></span> 
- <span data-ttu-id="504cd-2827">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="504cd-2827">A forward slash (optional)</span></span> 
- <span data-ttu-id="504cd-2828">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2828">7-8 digits</span></span> 
- <span data-ttu-id="504cd-2829">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="504cd-2829">A forward slash (optional)</span></span> 
- <span data-ttu-id="504cd-2830">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2830">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2831">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2831">Checksum</span></span>

<span data-ttu-id="504cd-2832">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2832">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2833">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2833">Definition</span></span>

<span data-ttu-id="504cd-2834">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2834">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2835">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2835">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2836">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2836">The checksum passes.</span></span>

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2837">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2837">Keywords</span></span>

<span data-ttu-id="504cd-2838">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2838">None</span></span>
   
## <a name="sweden-national-id"></a><span data-ttu-id="504cd-2839">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="504cd-2839">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2840">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2840">Format</span></span>

<span data-ttu-id="504cd-2841">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="504cd-2841">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2842">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2842">Pattern</span></span>

<span data-ttu-id="504cd-2843">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="504cd-2843">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="504cd-2844">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="504cd-2844">2-4 digits (optional)</span></span> 
- <span data-ttu-id="504cd-2845">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="504cd-2845">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="504cd-2846">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="504cd-2846">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="504cd-2847">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2847">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2848">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2848">Checksum</span></span>

<span data-ttu-id="504cd-2849">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2849">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2850">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2850">Definition</span></span>

<span data-ttu-id="504cd-2851">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2851">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2852">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2852">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2853">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2853">The checksum passes.</span></span>

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2854">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2854">Keywords</span></span>

<span data-ttu-id="504cd-2855">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2855">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="504cd-2856">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="504cd-2856">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2857">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2857">Format</span></span>

<span data-ttu-id="504cd-2858">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2858">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2859">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2859">Pattern</span></span>

<span data-ttu-id="504cd-2860">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2860">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2861">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2861">Checksum</span></span>

<span data-ttu-id="504cd-2862">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2862">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2863">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2863">Definition</span></span>

<span data-ttu-id="504cd-2864">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2864">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2865">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-2865">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2866">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-2866">One of the following is true:</span></span>
    - <span data-ttu-id="504cd-2867">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="504cd-2867">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="504cd-2868">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="504cd-2868">A keyword from Keyword_sweden_passport is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-2869">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2869">Keywords</span></span>
   
#### <a name="keywordswedenpassport"></a><span data-ttu-id="504cd-2870">Кэйворд_сведен_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-2870">Keyword_sweden_passport</span></span>

- <span data-ttu-id="504cd-2871">visa requirements</span><span class="sxs-lookup"><span data-stu-id="504cd-2871">visa requirements</span></span> 
- <span data-ttu-id="504cd-2872">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="504cd-2872">Alien Registration Card</span></span> 
- <span data-ttu-id="504cd-2873">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="504cd-2873">Schengen visas</span></span> 
- <span data-ttu-id="504cd-2874">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="504cd-2874">Schengen visa</span></span> 
- <span data-ttu-id="504cd-2875">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="504cd-2875">Visa Processing</span></span> 
- <span data-ttu-id="504cd-2876">Visa Type</span><span class="sxs-lookup"><span data-stu-id="504cd-2876">Visa Type</span></span> 
- <span data-ttu-id="504cd-2877">Single Entry</span><span class="sxs-lookup"><span data-stu-id="504cd-2877">Single Entry</span></span> 
- <span data-ttu-id="504cd-2878">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="504cd-2878">Multiple Entry</span></span> 
- <span data-ttu-id="504cd-2879">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="504cd-2879">G3 Processing Fees</span></span> 

#### <a name="keywordpassport"></a><span data-ttu-id="504cd-2880">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-2880">Keyword_passport</span></span>

- <span data-ttu-id="504cd-2881">Passport Number</span><span class="sxs-lookup"><span data-stu-id="504cd-2881">Passport Number</span></span> 
- <span data-ttu-id="504cd-2882">Passport No</span><span class="sxs-lookup"><span data-stu-id="504cd-2882">Passport No</span></span> 
- <span data-ttu-id="504cd-2883">Passport#</span><span class="sxs-lookup"><span data-stu-id="504cd-2883">Passport #</span></span> 
- <span data-ttu-id="504cd-2884">Службу</span><span class="sxs-lookup"><span data-stu-id="504cd-2884">Passport#</span></span> 
- <span data-ttu-id="504cd-2885">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="504cd-2885">PassportID</span></span> 
- <span data-ttu-id="504cd-2886">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="504cd-2886">Passportno</span></span> 
- <span data-ttu-id="504cd-2887">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2887">passportnumber</span></span> 
- <span data-ttu-id="504cd-2888">パスポート</span><span class="sxs-lookup"><span data-stu-id="504cd-2888">パスポート</span></span> 
- <span data-ttu-id="504cd-2889">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2889">パスポート番号</span></span> 
- <span data-ttu-id="504cd-2890">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="504cd-2890">パスポートのNum</span></span> 
- <span data-ttu-id="504cd-2891">パスポート #</span><span class="sxs-lookup"><span data-stu-id="504cd-2891">パスポート＃</span></span> 
- <span data-ttu-id="504cd-2892">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="504cd-2892">Numéro de passeport</span></span> 
- <span data-ttu-id="504cd-2893">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="504cd-2893">Passeport n °</span></span> 
- <span data-ttu-id="504cd-2894">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="504cd-2894">Passeport Non</span></span> 
- <span data-ttu-id="504cd-2895">Passeport#</span><span class="sxs-lookup"><span data-stu-id="504cd-2895">Passeport #</span></span> 
- <span data-ttu-id="504cd-2896">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="504cd-2896">Passeport#</span></span> 
- <span data-ttu-id="504cd-2897">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="504cd-2897">PasseportNon</span></span> 
- <span data-ttu-id="504cd-2898">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="504cd-2898">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="504cd-2899">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="504cd-2899">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2900">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2900">Format</span></span>

<span data-ttu-id="504cd-2901">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-2901">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2902">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2902">Pattern</span></span>

<span data-ttu-id="504cd-2903">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-2903">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="504cd-2904">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-2904">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2905">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-2905">An optional space</span></span> 
- <span data-ttu-id="504cd-2906">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2906">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="504cd-2907">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-2907">An optional space</span></span> 
- <span data-ttu-id="504cd-2908">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="504cd-2908">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2909">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2909">Checksum</span></span>

<span data-ttu-id="504cd-2910">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2910">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2911">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2911">Definition</span></span>

<span data-ttu-id="504cd-2912">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2912">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2913">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2913">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2914">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="504cd-2914">A keyword from Keyword_swift is found.</span></span>

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2915">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2915">Keywords</span></span>
   
#### <a name="keywordswift"></a><span data-ttu-id="504cd-2916">Кэйворд_свифт</span><span class="sxs-lookup"><span data-stu-id="504cd-2916">Keyword_swift</span></span>

- <span data-ttu-id="504cd-2917">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="504cd-2917">international organization for standardization 9362</span></span> 
- <span data-ttu-id="504cd-2918">iso 9362</span><span class="sxs-lookup"><span data-stu-id="504cd-2918">iso 9362</span></span> 
- <span data-ttu-id="504cd-2919">iso9362</span><span class="sxs-lookup"><span data-stu-id="504cd-2919">iso9362</span></span> 
- <span data-ttu-id="504cd-2920">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="504cd-2920">swift\#</span></span> 
- <span data-ttu-id="504cd-2921">свифткоде</span><span class="sxs-lookup"><span data-stu-id="504cd-2921">swiftcode</span></span> 
- <span data-ttu-id="504cd-2922">свифтнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2922">swiftnumber</span></span> 
- <span data-ttu-id="504cd-2923">свифтраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-2923">swiftroutingnumber</span></span> 
- <span data-ttu-id="504cd-2924">swift code</span><span class="sxs-lookup"><span data-stu-id="504cd-2924">swift code</span></span> 
- <span data-ttu-id="504cd-2925">swift number #</span><span class="sxs-lookup"><span data-stu-id="504cd-2925">swift number #</span></span> 
- <span data-ttu-id="504cd-2926">swift routing number</span><span class="sxs-lookup"><span data-stu-id="504cd-2926">swift routing number</span></span> 
- <span data-ttu-id="504cd-2927">bic number</span><span class="sxs-lookup"><span data-stu-id="504cd-2927">bic number</span></span> 
- <span data-ttu-id="504cd-2928">bic code</span><span class="sxs-lookup"><span data-stu-id="504cd-2928">bic code</span></span> 
- <span data-ttu-id="504cd-2929">БИК\#</span><span class="sxs-lookup"><span data-stu-id="504cd-2929">bic \#</span></span> 
- <span data-ttu-id="504cd-2930">БИК\#</span><span class="sxs-lookup"><span data-stu-id="504cd-2930">bic\#</span></span> 
- <span data-ttu-id="504cd-2931">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="504cd-2931">bank identifier code</span></span> 
- <span data-ttu-id="504cd-2932">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="504cd-2932">標準化9362</span></span> 
- <span data-ttu-id="504cd-2933">迅速 #</span><span class="sxs-lookup"><span data-stu-id="504cd-2933">迅速＃</span></span> 
- <span data-ttu-id="504cd-2934">Свифтコード</span><span class="sxs-lookup"><span data-stu-id="504cd-2934">SWIFTコード</span></span> 
- <span data-ttu-id="504cd-2935">Свифт番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2935">SWIFT番号</span></span> 
- <span data-ttu-id="504cd-2936">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2936">迅速なルーティング番号</span></span> 
- <span data-ttu-id="504cd-2937">Бик番号</span><span class="sxs-lookup"><span data-stu-id="504cd-2937">BIC番号</span></span> 
- <span data-ttu-id="504cd-2938">Бикコード</span><span class="sxs-lookup"><span data-stu-id="504cd-2938">BICコード</span></span> 
- <span data-ttu-id="504cd-2939">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="504cd-2939">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="504cd-2940">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="504cd-2940">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="504cd-2941">Быстрая\#</span><span class="sxs-lookup"><span data-stu-id="504cd-2941">rapide \#</span></span> 
- <span data-ttu-id="504cd-2942">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="504cd-2942">code SWIFT</span></span> 
- <span data-ttu-id="504cd-2943">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="504cd-2943">le numéro de swift</span></span> 
- <span data-ttu-id="504cd-2944">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="504cd-2944">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="504cd-2945">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="504cd-2945">le numéro BIC</span></span> 
- <span data-ttu-id="504cd-2946">\#БИК</span><span class="sxs-lookup"><span data-stu-id="504cd-2946">\# BIC</span></span> 
- <span data-ttu-id="504cd-2947">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="504cd-2947">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="504cd-2948">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="504cd-2948">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2949">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2949">Format</span></span>

<span data-ttu-id="504cd-2950">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2950">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2951">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2951">Pattern</span></span>

<span data-ttu-id="504cd-2952">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2952">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="504cd-2953">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-2953">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="504cd-2954">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="504cd-2954">The digit "1" or "2"</span></span> 
- <span data-ttu-id="504cd-2955">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2955">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2956">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2956">Checksum</span></span>

<span data-ttu-id="504cd-2957">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-2957">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2958">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2958">Definition</span></span>

<span data-ttu-id="504cd-2959">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2959">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2960">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2960">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2961">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="504cd-2961">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="504cd-2962">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-2962">The checksum passes.</span></span>

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2963">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2963">Keywords</span></span>

#### <a name="keywordtaiwanesenationalid"></a><span data-ttu-id="504cd-2964">Кэйворд_таиванесе_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-2964">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="504cd-2965">身份證字號</span><span class="sxs-lookup"><span data-stu-id="504cd-2965">身份證字號</span></span> 
- <span data-ttu-id="504cd-2966">身份證</span><span class="sxs-lookup"><span data-stu-id="504cd-2966">身份證</span></span> 
- <span data-ttu-id="504cd-2967">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="504cd-2967">身份證號碼</span></span> 
- <span data-ttu-id="504cd-2968">身份證號</span><span class="sxs-lookup"><span data-stu-id="504cd-2968">身份證號</span></span> 
- <span data-ttu-id="504cd-2969">身分證字號</span><span class="sxs-lookup"><span data-stu-id="504cd-2969">身分證字號</span></span> 
- <span data-ttu-id="504cd-2970">身分證</span><span class="sxs-lookup"><span data-stu-id="504cd-2970">身分證</span></span> 
- <span data-ttu-id="504cd-2971">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="504cd-2971">身分證號碼</span></span> 
- <span data-ttu-id="504cd-2972">身份證號</span><span class="sxs-lookup"><span data-stu-id="504cd-2972">身份證號</span></span> 
- <span data-ttu-id="504cd-2973">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="504cd-2973">身分證統一編號</span></span> 
- <span data-ttu-id="504cd-2974">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="504cd-2974">國民身分證統一編號</span></span> 
- <span data-ttu-id="504cd-2975">簽名</span><span class="sxs-lookup"><span data-stu-id="504cd-2975">簽名</span></span> 
- <span data-ttu-id="504cd-2976">蓋章</span><span class="sxs-lookup"><span data-stu-id="504cd-2976">蓋章</span></span> 
- <span data-ttu-id="504cd-2977">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="504cd-2977">簽名或蓋章</span></span> 
- <span data-ttu-id="504cd-2978">簽章</span><span class="sxs-lookup"><span data-stu-id="504cd-2978">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="504cd-2979">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="504cd-2979">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-2980">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-2980">Format</span></span>

- <span data-ttu-id="504cd-2981">Номер биометрического паспорта: девять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2981">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="504cd-2982">Номер биометрической службы Passport: девять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-2982">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-2983">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-2983">Pattern</span></span>
<span data-ttu-id="504cd-2984">Номер биометрического паспорта:</span><span class="sxs-lookup"><span data-stu-id="504cd-2984">Biometric passport number:</span></span>
- <span data-ttu-id="504cd-2985">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="504cd-2985">The digit "3"</span></span> 
- <span data-ttu-id="504cd-2986">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2986">Eight digits</span></span>

<span data-ttu-id="504cd-2987">Номер биометрической службы Passport:</span><span class="sxs-lookup"><span data-stu-id="504cd-2987">Non-biometric passport number:</span></span>
- <span data-ttu-id="504cd-2988">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-2988">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-2989">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-2989">Checksum</span></span>

<span data-ttu-id="504cd-2990">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-2990">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-2991">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-2991">Definition</span></span>

<span data-ttu-id="504cd-2992">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-2992">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-2993">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-2993">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-2994">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="504cd-2994">A keyword from Keyword_taiwan_passport is found.</span></span>

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-2995">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-2995">Keywords</span></span>

#### <a name="keywordtaiwanpassport"></a><span data-ttu-id="504cd-2996">Кэйворд_таиван_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-2996">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="504cd-2997">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="504cd-2997">ROC passport number</span></span> 
- <span data-ttu-id="504cd-2998">Passport number</span><span class="sxs-lookup"><span data-stu-id="504cd-2998">Passport number</span></span> 
- <span data-ttu-id="504cd-2999">Passport no</span><span class="sxs-lookup"><span data-stu-id="504cd-2999">Passport no</span></span> 
- <span data-ttu-id="504cd-3000">Passport Num</span><span class="sxs-lookup"><span data-stu-id="504cd-3000">Passport Num</span></span> 
- <span data-ttu-id="504cd-3001">Passport #</span><span class="sxs-lookup"><span data-stu-id="504cd-3001">Passport #</span></span> 
- <span data-ttu-id="504cd-3002">护照</span><span class="sxs-lookup"><span data-stu-id="504cd-3002">护照</span></span> 
- <span data-ttu-id="504cd-3003">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="504cd-3003">中華民國護照</span></span> 
- <span data-ttu-id="504cd-3004">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="504cd-3004">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="504cd-3005">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="504cd-3005">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3006">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3006">Format</span></span>

<span data-ttu-id="504cd-3007">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3007">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3008">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3008">Pattern</span></span>

<span data-ttu-id="504cd-3009">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-3009">10 letters and digits:</span></span>
- <span data-ttu-id="504cd-3010">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="504cd-3010">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="504cd-3011">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3011">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3012">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3012">Checksum</span></span>

<span data-ttu-id="504cd-3013">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3013">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3014">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3014">Definition</span></span>

<span data-ttu-id="504cd-3015">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3015">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3016">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3016">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3017">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="504cd-3017">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-3018">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3018">Keywords</span></span>

#### <a name="keywordtaiwanresidentcertificate"></a><span data-ttu-id="504cd-3019">Кэйворд_таиван_ресидент_цертификате</span><span class="sxs-lookup"><span data-stu-id="504cd-3019">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="504cd-3020">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="504cd-3020">Resident Certificate</span></span> 
- <span data-ttu-id="504cd-3021">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="504cd-3021">Resident Cert</span></span> 
- <span data-ttu-id="504cd-3022">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="504cd-3022">Resident Cert.</span></span> 
- <span data-ttu-id="504cd-3023">Identification card</span><span class="sxs-lookup"><span data-stu-id="504cd-3023">Identification card</span></span> 
- <span data-ttu-id="504cd-3024">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="504cd-3024">Alien Resident Certificate</span></span> 
- <span data-ttu-id="504cd-3025">ГИПЕРБОЛ</span><span class="sxs-lookup"><span data-stu-id="504cd-3025">ARC</span></span> 
- <span data-ttu-id="504cd-3026">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="504cd-3026">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="504cd-3027">TARC</span><span class="sxs-lookup"><span data-stu-id="504cd-3027">TARC</span></span> 
- <span data-ttu-id="504cd-3028">居留證</span><span class="sxs-lookup"><span data-stu-id="504cd-3028">居留證</span></span> 
- <span data-ttu-id="504cd-3029">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="504cd-3029">外僑居留證</span></span> 
- <span data-ttu-id="504cd-3030">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="504cd-3030">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="504cd-3031">Код идентификации для тайского заполнения</span><span class="sxs-lookup"><span data-stu-id="504cd-3031">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3032">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3032">Format</span></span>

<span data-ttu-id="504cd-3033">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3033">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3034">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3034">Pattern</span></span>

<span data-ttu-id="504cd-3035">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="504cd-3035">13 digits:</span></span>
- <span data-ttu-id="504cd-3036">Первая цифра не равна 0 или 9</span><span class="sxs-lookup"><span data-stu-id="504cd-3036">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="504cd-3037">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3037">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3038">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3038">Checksum</span></span>

<span data-ttu-id="504cd-3039">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-3039">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3040">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3040">Definition</span></span>

<span data-ttu-id="504cd-3041">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3041">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3042">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3042">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3043">Найдено ключевое слово из Кэйворд_саи_Цитизен_ид.</span><span class="sxs-lookup"><span data-stu-id="504cd-3043">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="504cd-3044">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3044">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3045">Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3045">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3046">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3046">Keywords</span></span>

#### <a name="keywordthaicitizenid"></a><span data-ttu-id="504cd-3047">Кэйворд_саи_Цитизен_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-3047">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="504cd-3048">ID Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3048">ID Number</span></span>
- <span data-ttu-id="504cd-3049">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="504cd-3049">Identification Number</span></span>
- <span data-ttu-id="504cd-3050">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="504cd-3050">บัตรประชาชน</span></span>
- <span data-ttu-id="504cd-3051">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="504cd-3051">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="504cd-3052">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="504cd-3052">บัตรประชาชน</span></span>
- <span data-ttu-id="504cd-3053">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="504cd-3053">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="504cd-3054">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="504cd-3054">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3055">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3055">Format</span></span>

<span data-ttu-id="504cd-3056">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3056">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3057">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3057">Pattern</span></span>

<span data-ttu-id="504cd-3058">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3058">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3059">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3059">Checksum</span></span>

<span data-ttu-id="504cd-3060">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3061">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3061">Definition</span></span>

<span data-ttu-id="504cd-3062">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3063">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3063">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3064">Найдено ключевое слово из Кэйворд_туркиш_натионал_ид.</span><span class="sxs-lookup"><span data-stu-id="504cd-3064">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="504cd-3065">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3065">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3066">Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3066">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3067">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3067">Keywords</span></span>

#### <a name="keywordturkishnationalid"></a><span data-ttu-id="504cd-3068">Кэйворд_туркиш_натионал_ид</span><span class="sxs-lookup"><span data-stu-id="504cd-3068">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="504cd-3069">TC Кимлик No</span><span class="sxs-lookup"><span data-stu-id="504cd-3069">TC Kimlik No</span></span>
- <span data-ttu-id="504cd-3070">TC Кимлик нумарасı</span><span class="sxs-lookup"><span data-stu-id="504cd-3070">TC Kimlik numarası</span></span>
- <span data-ttu-id="504cd-3071">Ватандаşлıк нумарасı</span><span class="sxs-lookup"><span data-stu-id="504cd-3071">Vatandaşlık numarası</span></span>
- <span data-ttu-id="504cd-3072">Ватандаşлıк нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3072">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="504cd-p141">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="504cd-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3075">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3075">Format</span></span>

<span data-ttu-id="504cd-3076">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-3076">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3077">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3077">Pattern</span></span>

<span data-ttu-id="504cd-3078">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3078">18 letters and digits:</span></span>
- <span data-ttu-id="504cd-3079">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="504cd-3079">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="504cd-3080">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="504cd-3080">One digit</span></span> 
- <span data-ttu-id="504cd-3081">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="504cd-3081">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="504cd-3082">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="504cd-3082">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="504cd-3083">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3083">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3084">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3084">Checksum</span></span>

<span data-ttu-id="504cd-3085">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-3085">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3086">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3086">Definition</span></span>

<span data-ttu-id="504cd-3087">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3087">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3088">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3088">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3089">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="504cd-3089">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="504cd-3090">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-3090">The checksum passes.</span></span>

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-3091">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3091">Keywords</span></span>

#### <a name="keywordukdriverslicense"></a><span data-ttu-id="504cd-3092">Кэйворд_ук_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-3092">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="504cd-3093">ДВЛА</span><span class="sxs-lookup"><span data-stu-id="504cd-3093">DVLA</span></span> 
- <span data-ttu-id="504cd-3094">light vans</span><span class="sxs-lookup"><span data-stu-id="504cd-3094">light vans</span></span> 
- <span data-ttu-id="504cd-3095">куадбикес</span><span class="sxs-lookup"><span data-stu-id="504cd-3095">quadbikes</span></span> 
- <span data-ttu-id="504cd-3096">motor cars</span><span class="sxs-lookup"><span data-stu-id="504cd-3096">motor cars</span></span> 
- <span data-ttu-id="504cd-3097">125cc</span><span class="sxs-lookup"><span data-stu-id="504cd-3097">125cc</span></span> 
- <span data-ttu-id="504cd-3098">сидекар</span><span class="sxs-lookup"><span data-stu-id="504cd-3098">sidecar</span></span> 
- <span data-ttu-id="504cd-3099">трициклес</span><span class="sxs-lookup"><span data-stu-id="504cd-3099">tricycles</span></span> 
- <span data-ttu-id="504cd-3100">моторциклес</span><span class="sxs-lookup"><span data-stu-id="504cd-3100">motorcycles</span></span> 
- <span data-ttu-id="504cd-3101">photocard licence</span><span class="sxs-lookup"><span data-stu-id="504cd-3101">photocard licence</span></span> 
- <span data-ttu-id="504cd-3102">learner drivers</span><span class="sxs-lookup"><span data-stu-id="504cd-3102">learner drivers</span></span> 
- <span data-ttu-id="504cd-3103">licence holder</span><span class="sxs-lookup"><span data-stu-id="504cd-3103">licence holder</span></span> 
- <span data-ttu-id="504cd-3104">licence holders</span><span class="sxs-lookup"><span data-stu-id="504cd-3104">licence holders</span></span> 
- <span data-ttu-id="504cd-3105">driving licences</span><span class="sxs-lookup"><span data-stu-id="504cd-3105">driving licences</span></span> 
- <span data-ttu-id="504cd-3106">driving licence</span><span class="sxs-lookup"><span data-stu-id="504cd-3106">driving licence</span></span> 
- <span data-ttu-id="504cd-3107">dual control car</span><span class="sxs-lookup"><span data-stu-id="504cd-3107">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="504cd-p142">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="504cd-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3110">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3110">Format</span></span>

<span data-ttu-id="504cd-3111">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-3111">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3112">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3112">Pattern</span></span>

<span data-ttu-id="504cd-3113">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="504cd-3113">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3114">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3114">Checksum</span></span>

<span data-ttu-id="504cd-3115">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3115">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3116">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3116">Definition</span></span>

<span data-ttu-id="504cd-3117">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3118">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3118">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3119">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="504cd-3119">A keyword from Keyword_uk_electoral is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3120">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3120">Keywords</span></span>

#### <a name="keywordukelectoral"></a><span data-ttu-id="504cd-3121">Кэйворд_ук_електорал</span><span class="sxs-lookup"><span data-stu-id="504cd-3121">Keyword_uk_electoral</span></span>

- <span data-ttu-id="504cd-3122">council nomination</span><span class="sxs-lookup"><span data-stu-id="504cd-3122">council nomination</span></span> 
- <span data-ttu-id="504cd-3123">nomination form</span><span class="sxs-lookup"><span data-stu-id="504cd-3123">nomination form</span></span> 
- <span data-ttu-id="504cd-3124">electoral register</span><span class="sxs-lookup"><span data-stu-id="504cd-3124">electoral register</span></span> 
- <span data-ttu-id="504cd-3125">electoral roll</span><span class="sxs-lookup"><span data-stu-id="504cd-3125">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="504cd-p143">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="504cd-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3128">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3128">Format</span></span>

<span data-ttu-id="504cd-3129">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="504cd-3129">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3130">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3130">Pattern</span></span>

<span data-ttu-id="504cd-3131">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3131">10-17 digits:</span></span>
- <span data-ttu-id="504cd-3132">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3132">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="504cd-3133">Пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-3133">A space</span></span> 
- <span data-ttu-id="504cd-3134">Три цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3134">Three digits</span></span> 
- <span data-ttu-id="504cd-3135">Пробел</span><span class="sxs-lookup"><span data-stu-id="504cd-3135">A space</span></span> 
- <span data-ttu-id="504cd-3136">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3136">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3137">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3137">Checksum</span></span>

<span data-ttu-id="504cd-3138">Да</span><span class="sxs-lookup"><span data-stu-id="504cd-3138">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3139">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3139">Definition</span></span>

<span data-ttu-id="504cd-3140">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3140">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3141">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3141">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3142">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-3142">One of the following is true:</span></span>
    - <span data-ttu-id="504cd-3143">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="504cd-3143">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="504cd-3144">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="504cd-3144">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="504cd-3145">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="504cd-3145">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="504cd-3146">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="504cd-3146">The checksum passes.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3147">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3147">Keywords</span></span>
   
#### <a name="keyworduknhsnumber"></a><span data-ttu-id="504cd-3148">Кэйворд_ук_нхс_нумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-3148">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="504cd-3149">national health service</span><span class="sxs-lookup"><span data-stu-id="504cd-3149">national health service</span></span> 
- <span data-ttu-id="504cd-3150">NHS</span><span class="sxs-lookup"><span data-stu-id="504cd-3150">nhs</span></span> 
- <span data-ttu-id="504cd-3151">health services authority</span><span class="sxs-lookup"><span data-stu-id="504cd-3151">health services authority</span></span> 
- <span data-ttu-id="504cd-3152">health authority</span><span class="sxs-lookup"><span data-stu-id="504cd-3152">health authority</span></span>

#### <a name="keyworduknhsnumber1"></a><span data-ttu-id="504cd-3153">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="504cd-3153">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="504cd-3154">patient id</span><span class="sxs-lookup"><span data-stu-id="504cd-3154">patient id</span></span> 
- <span data-ttu-id="504cd-3155">patient identification</span><span class="sxs-lookup"><span data-stu-id="504cd-3155">patient identification</span></span> 
- <span data-ttu-id="504cd-3156">patient no</span><span class="sxs-lookup"><span data-stu-id="504cd-3156">patient no</span></span> 
- <span data-ttu-id="504cd-3157">patient number</span><span class="sxs-lookup"><span data-stu-id="504cd-3157">patient number</span></span>

#### <a name="keyworduknhsnumberdob"></a><span data-ttu-id="504cd-3158">Кэйворд_ук_нхс_нумбер_доб</span><span class="sxs-lookup"><span data-stu-id="504cd-3158">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="504cd-3159">ГРУПП</span><span class="sxs-lookup"><span data-stu-id="504cd-3159">GP</span></span> 
- <span data-ttu-id="504cd-3160">ДОБ</span><span class="sxs-lookup"><span data-stu-id="504cd-3160">DOB</span></span> 
- <span data-ttu-id="504cd-3161">D. O. B</span><span class="sxs-lookup"><span data-stu-id="504cd-3161">D.O.B</span></span> 
- <span data-ttu-id="504cd-3162">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="504cd-3162">Date of Birth</span></span> 
- <span data-ttu-id="504cd-3163">Birth Date</span><span class="sxs-lookup"><span data-stu-id="504cd-3163">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="504cd-p144">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="504cd-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3166">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3166">Format</span></span>

<span data-ttu-id="504cd-3167">7 символов или 9 символов, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3167">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3168">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3168">Pattern</span></span>

<span data-ttu-id="504cd-3169">Два возможных шаблона:</span><span class="sxs-lookup"><span data-stu-id="504cd-3169">Two possible patterns:</span></span>

- <span data-ttu-id="504cd-3170">Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-3170">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="504cd-3171">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3171">Six digits</span></span>
- <span data-ttu-id="504cd-3172">"A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="504cd-3172">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="504cd-3173">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="504cd-3173">OR</span></span>

- <span data-ttu-id="504cd-3174">Две буквы</span><span class="sxs-lookup"><span data-stu-id="504cd-3174">Two letters</span></span>
- <span data-ttu-id="504cd-3175">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3175">A space or dash</span></span>
- <span data-ttu-id="504cd-3176">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3176">Two digits</span></span>
- <span data-ttu-id="504cd-3177">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3177">A space or dash</span></span>
- <span data-ttu-id="504cd-3178">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3178">Two digits</span></span>
- <span data-ttu-id="504cd-3179">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3179">A space or dash</span></span>
- <span data-ttu-id="504cd-3180">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3180">Two digits</span></span>
- <span data-ttu-id="504cd-3181">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3181">A space or dash</span></span>
- <span data-ttu-id="504cd-3182">Значение "A", "B", "C" или "'D"</span><span class="sxs-lookup"><span data-stu-id="504cd-3182">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3183">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3183">Checksum</span></span>

<span data-ttu-id="504cd-3184">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3185">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3185">Definition</span></span>

<span data-ttu-id="504cd-3186">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3186">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3187">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3187">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3188">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="504cd-3188">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="504cd-3189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3190">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3190">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3191">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="504cd-3191">No keyword from Keyword_uk_nino is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3192">Keywords</span></span>

#### <a name="keyworduknino"></a><span data-ttu-id="504cd-3193">Кэйворд_ук_нино</span><span class="sxs-lookup"><span data-stu-id="504cd-3193">Keyword_uk_nino</span></span>

- <span data-ttu-id="504cd-3194">national insurance number</span><span class="sxs-lookup"><span data-stu-id="504cd-3194">national insurance number</span></span> 
- <span data-ttu-id="504cd-3195">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="504cd-3195">national insurance contributions</span></span> 
- <span data-ttu-id="504cd-3196">protection act</span><span class="sxs-lookup"><span data-stu-id="504cd-3196">protection act</span></span> 
- <span data-ttu-id="504cd-3197">страхования</span><span class="sxs-lookup"><span data-stu-id="504cd-3197">insurance</span></span> 
- <span data-ttu-id="504cd-3198">social security number</span><span class="sxs-lookup"><span data-stu-id="504cd-3198">social security number</span></span> 
- <span data-ttu-id="504cd-3199">insurance application</span><span class="sxs-lookup"><span data-stu-id="504cd-3199">insurance application</span></span> 
- <span data-ttu-id="504cd-3200">medical application</span><span class="sxs-lookup"><span data-stu-id="504cd-3200">medical application</span></span> 
- <span data-ttu-id="504cd-3201">social insurance</span><span class="sxs-lookup"><span data-stu-id="504cd-3201">social insurance</span></span> 
- <span data-ttu-id="504cd-3202">medical attention</span><span class="sxs-lookup"><span data-stu-id="504cd-3202">medical attention</span></span> 
- <span data-ttu-id="504cd-3203">social security</span><span class="sxs-lookup"><span data-stu-id="504cd-3203">social security</span></span> 
- <span data-ttu-id="504cd-3204">great britain</span><span class="sxs-lookup"><span data-stu-id="504cd-3204">great britain</span></span> 
- <span data-ttu-id="504cd-3205">страхования</span><span class="sxs-lookup"><span data-stu-id="504cd-3205">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="504cd-p145">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="504cd-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3208">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3208">Format</span></span>

<span data-ttu-id="504cd-3209">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3209">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3210">Pattern</span></span>

<span data-ttu-id="504cd-3211">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="504cd-3211">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3212">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3212">Checksum</span></span>

<span data-ttu-id="504cd-3213">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3213">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3214">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3214">Definition</span></span>

<span data-ttu-id="504cd-3215">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3215">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3216">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3216">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3217">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="504cd-3217">A keyword from Keyword_passport is found.</span></span>

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-3218">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3218">Keywords</span></span>

#### <a name="keywordpassport"></a><span data-ttu-id="504cd-3219">Кэйворд_пасспорт</span><span class="sxs-lookup"><span data-stu-id="504cd-3219">Keyword_passport</span></span>

- <span data-ttu-id="504cd-3220">Passport Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3220">Passport Number</span></span> 
- <span data-ttu-id="504cd-3221">Passport No</span><span class="sxs-lookup"><span data-stu-id="504cd-3221">Passport No</span></span> 
- <span data-ttu-id="504cd-3222">Passport#</span><span class="sxs-lookup"><span data-stu-id="504cd-3222">Passport #</span></span> 
- <span data-ttu-id="504cd-3223">Службу</span><span class="sxs-lookup"><span data-stu-id="504cd-3223">Passport#</span></span> 
- <span data-ttu-id="504cd-3224">Пасспортид</span><span class="sxs-lookup"><span data-stu-id="504cd-3224">PassportID</span></span> 
- <span data-ttu-id="504cd-3225">Пасспортно</span><span class="sxs-lookup"><span data-stu-id="504cd-3225">Passportno</span></span> 
- <span data-ttu-id="504cd-3226">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="504cd-3226">passportnumber</span></span> 
- <span data-ttu-id="504cd-3227">パスポート</span><span class="sxs-lookup"><span data-stu-id="504cd-3227">パスポート</span></span> 
- <span data-ttu-id="504cd-3228">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="504cd-3228">パスポート番号</span></span> 
- <span data-ttu-id="504cd-3229">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="504cd-3229">パスポートのNum</span></span> 
- <span data-ttu-id="504cd-3230">パスポート #</span><span class="sxs-lookup"><span data-stu-id="504cd-3230">パスポート＃</span></span> 
- <span data-ttu-id="504cd-3231">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="504cd-3231">Numéro de passeport</span></span> 
- <span data-ttu-id="504cd-3232">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="504cd-3232">Passeport n °</span></span> 
- <span data-ttu-id="504cd-3233">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="504cd-3233">Passeport Non</span></span> 
- <span data-ttu-id="504cd-3234">Passeport#</span><span class="sxs-lookup"><span data-stu-id="504cd-3234">Passeport #</span></span> 
- <span data-ttu-id="504cd-3235">Пассепорт #</span><span class="sxs-lookup"><span data-stu-id="504cd-3235">Passeport#</span></span> 
- <span data-ttu-id="504cd-3236">Пассепортнон</span><span class="sxs-lookup"><span data-stu-id="504cd-3236">PasseportNon</span></span> 
- <span data-ttu-id="504cd-3237">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="504cd-3237">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="504cd-3238">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="504cd-3238">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3239">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3239">Format</span></span>

<span data-ttu-id="504cd-3240">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3240">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3241">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3241">Pattern</span></span>

<span data-ttu-id="504cd-3242">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3242">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3243">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3243">Checksum</span></span>

<span data-ttu-id="504cd-3244">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3244">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3245">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3245">Definition</span></span>

<span data-ttu-id="504cd-3246">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3247">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3247">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3248">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="504cd-3248">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="504cd-3249">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3249">Keywords</span></span>

#### <a name="keywordusabankaccount"></a><span data-ttu-id="504cd-3250">Кэйворд_уса_банк_аккаунт</span><span class="sxs-lookup"><span data-stu-id="504cd-3250">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="504cd-3251">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3251">Checking Account Number</span></span> 
- <span data-ttu-id="504cd-3252">Checking Account</span><span class="sxs-lookup"><span data-stu-id="504cd-3252">Checking Account</span></span> 
- <span data-ttu-id="504cd-3253">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-3253">Checking Account #</span></span> 
- <span data-ttu-id="504cd-3254">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3254">Checking Acct Number</span></span> 
- <span data-ttu-id="504cd-3255">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-3255">Checking Acct #</span></span> 
- <span data-ttu-id="504cd-3256">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3256">Checking Acct No.</span></span> 
- <span data-ttu-id="504cd-3257">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3257">Checking Account No.</span></span> 
- <span data-ttu-id="504cd-3258">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3258">Bank Account Number</span></span> 
- <span data-ttu-id="504cd-3259">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-3259">Bank Account #</span></span> 
- <span data-ttu-id="504cd-3260">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3260">Bank Acct Number</span></span> 
- <span data-ttu-id="504cd-3261">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-3261">Bank Acct #</span></span> 
- <span data-ttu-id="504cd-3262">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3262">Bank Acct No.</span></span> 
- <span data-ttu-id="504cd-3263">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3263">Bank Account No.</span></span> 
- <span data-ttu-id="504cd-3264">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3264">Savings Account Number</span></span> 
- <span data-ttu-id="504cd-3265">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="504cd-3265">Savings Account.</span></span> 
- <span data-ttu-id="504cd-3266">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-3266">Savings Account #</span></span> 
- <span data-ttu-id="504cd-3267">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3267">Savings Acct Number</span></span> 
- <span data-ttu-id="504cd-3268">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-3268">Savings Acct #</span></span> 
- <span data-ttu-id="504cd-3269">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3269">Savings Acct No.</span></span> 
- <span data-ttu-id="504cd-3270">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3270">Savings Account No.</span></span> 
- <span data-ttu-id="504cd-3271">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3271">Debit Account Number</span></span> 
- <span data-ttu-id="504cd-3272">Debit Account</span><span class="sxs-lookup"><span data-stu-id="504cd-3272">Debit Account</span></span> 
- <span data-ttu-id="504cd-3273">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="504cd-3273">Debit Account #</span></span> 
- <span data-ttu-id="504cd-3274">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="504cd-3274">Debit Acct Number</span></span> 
- <span data-ttu-id="504cd-3275">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="504cd-3275">Debit Acct #</span></span> 
- <span data-ttu-id="504cd-3276">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3276">Debit Acct No.</span></span> 
- <span data-ttu-id="504cd-3277">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="504cd-3277">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="504cd-3278">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="504cd-3278">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3279">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3279">Format</span></span>

<span data-ttu-id="504cd-3280">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="504cd-3280">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3281">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3281">Pattern</span></span>

<span data-ttu-id="504cd-3282">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="504cd-3282">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="504cd-3283">Девять цифр, отформатированных как DDD DDD DDD, будут совпадают.</span><span class="sxs-lookup"><span data-stu-id="504cd-3283">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="504cd-3284">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="504cd-3284">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3285">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3285">Checksum</span></span>

<span data-ttu-id="504cd-3286">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3286">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3287">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3287">Definition</span></span>

<span data-ttu-id="504cd-3288">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3288">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3289">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3289">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3290">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="504cd-3290">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="504cd-3291">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="504cd-3291">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="504cd-3292">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3292">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3293">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="504cd-3293">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3294">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="504cd-3294">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="504cd-3295">находится ключевое слово из Keyword_us_drivers_license_abbreviations.</span><span class="sxs-lookup"><span data-stu-id="504cd-3295">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="504cd-3296">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="504cd-3296">No keyword from Keyword_us_drivers_license is found.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3297">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3297">Keywords</span></span>

#### <a name="keywordusdriverslicenseabbreviations"></a><span data-ttu-id="504cd-3298">Кэйворд_ус_дриверс_лиценсе_аббревиатионс</span><span class="sxs-lookup"><span data-stu-id="504cd-3298">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="504cd-3299">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-3299">DL</span></span> 
- <span data-ttu-id="504cd-3300">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="504cd-3300">DLS</span></span> 
- <span data-ttu-id="504cd-3301">КДЛ</span><span class="sxs-lookup"><span data-stu-id="504cd-3301">CDL</span></span> 
- <span data-ttu-id="504cd-3302">КДЛС</span><span class="sxs-lookup"><span data-stu-id="504cd-3302">CDLS</span></span> 
- <span data-ttu-id="504cd-3303">ИД</span><span class="sxs-lookup"><span data-stu-id="504cd-3303">ID</span></span> 
- <span data-ttu-id="504cd-3304">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="504cd-3304">IDs</span></span> 
- <span data-ttu-id="504cd-3305">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-3305">DL#</span></span> 
- <span data-ttu-id="504cd-3306">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="504cd-3306">DLS#</span></span> 
- <span data-ttu-id="504cd-3307">КДЛ #</span><span class="sxs-lookup"><span data-stu-id="504cd-3307">CDL#</span></span> 
- <span data-ttu-id="504cd-3308">КДЛС #</span><span class="sxs-lookup"><span data-stu-id="504cd-3308">CDLS#</span></span> 
- <span data-ttu-id="504cd-3309">КОДОВ</span><span class="sxs-lookup"><span data-stu-id="504cd-3309">ID#</span></span>
- <span data-ttu-id="504cd-3310">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="504cd-3310">IDs#</span></span> 
- <span data-ttu-id="504cd-3311">ID number</span><span class="sxs-lookup"><span data-stu-id="504cd-3311">ID number</span></span> 
- <span data-ttu-id="504cd-3312">ID numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-3312">ID numbers</span></span> 
- <span data-ttu-id="504cd-3313">Лик</span><span class="sxs-lookup"><span data-stu-id="504cd-3313">LIC</span></span> 
- <span data-ttu-id="504cd-3314">Лик #</span><span class="sxs-lookup"><span data-stu-id="504cd-3314">LIC#</span></span> 

#### <a name="keywordusdriverslicense"></a><span data-ttu-id="504cd-3315">Кэйворд_ус_дриверс_лиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-3315">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="504cd-3316">Дриверлик</span><span class="sxs-lookup"><span data-stu-id="504cd-3316">DriverLic</span></span> 
- <span data-ttu-id="504cd-3317">Дриверликс</span><span class="sxs-lookup"><span data-stu-id="504cd-3317">DriverLics</span></span> 
- <span data-ttu-id="504cd-3318">Дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-3318">DriverLicense</span></span> 
- <span data-ttu-id="504cd-3319">Дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-3319">DriverLicenses</span></span> 
- <span data-ttu-id="504cd-3320">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-3320">Driver Lic</span></span> 
- <span data-ttu-id="504cd-3321">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-3321">Driver Lics</span></span> 
- <span data-ttu-id="504cd-3322">Driver License</span><span class="sxs-lookup"><span data-stu-id="504cd-3322">Driver License</span></span> 
- <span data-ttu-id="504cd-3323">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-3323">Driver Licenses</span></span> 
- <span data-ttu-id="504cd-3324">Дриверслик</span><span class="sxs-lookup"><span data-stu-id="504cd-3324">DriversLic</span></span> 
- <span data-ttu-id="504cd-3325">Дриверсликс</span><span class="sxs-lookup"><span data-stu-id="504cd-3325">DriversLics</span></span> 
- <span data-ttu-id="504cd-3326">Дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-3326">DriversLicense</span></span> 
- <span data-ttu-id="504cd-3327">Дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-3327">DriversLicenses</span></span> 
- <span data-ttu-id="504cd-3328">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-3328">Drivers Lic</span></span> 
- <span data-ttu-id="504cd-3329">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-3329">Drivers Lics</span></span> 
- <span data-ttu-id="504cd-3330">Drivers License</span><span class="sxs-lookup"><span data-stu-id="504cd-3330">Drivers License</span></span> 
- <span data-ttu-id="504cd-3331">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-3331">Drivers Licenses</span></span> 
- <span data-ttu-id="504cd-3332">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="504cd-3332">Driver'Lic</span></span> 
- <span data-ttu-id="504cd-3333">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="504cd-3333">Driver'Lics</span></span> 
- <span data-ttu-id="504cd-3334">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="504cd-3334">Driver'License</span></span> 
- <span data-ttu-id="504cd-3335">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-3335">Driver'Licenses</span></span> 
- <span data-ttu-id="504cd-3336">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-3336">Driver' Lic</span></span> 
- <span data-ttu-id="504cd-3337">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-3337">Driver' Lics</span></span> 
- <span data-ttu-id="504cd-3338">Driver' License</span><span class="sxs-lookup"><span data-stu-id="504cd-3338">Driver' License</span></span> 
- <span data-ttu-id="504cd-3339">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-3339">Driver' Licenses</span></span>
- <span data-ttu-id="504cd-3340">Дривер'слик</span><span class="sxs-lookup"><span data-stu-id="504cd-3340">Driver'sLic</span></span> 
- <span data-ttu-id="504cd-3341">Дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="504cd-3341">Driver'sLics</span></span> 
- <span data-ttu-id="504cd-3342">Дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="504cd-3342">Driver'sLicense</span></span> 
- <span data-ttu-id="504cd-3343">Дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="504cd-3343">Driver'sLicenses</span></span> 
- <span data-ttu-id="504cd-3344">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="504cd-3344">Driver's Lic</span></span> 
- <span data-ttu-id="504cd-3345">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="504cd-3345">Driver's Lics</span></span> 
- <span data-ttu-id="504cd-3346">Driver's License</span><span class="sxs-lookup"><span data-stu-id="504cd-3346">Driver's License</span></span> 
- <span data-ttu-id="504cd-3347">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-3347">Driver's Licenses</span></span> 
- <span data-ttu-id="504cd-3348">identification number</span><span class="sxs-lookup"><span data-stu-id="504cd-3348">identification number</span></span> 
- <span data-ttu-id="504cd-3349">identification numbers</span><span class="sxs-lookup"><span data-stu-id="504cd-3349">identification numbers</span></span> 
- <span data-ttu-id="504cd-3350">identification #</span><span class="sxs-lookup"><span data-stu-id="504cd-3350">identification #</span></span> 
- <span data-ttu-id="504cd-3351">id card</span><span class="sxs-lookup"><span data-stu-id="504cd-3351">id card</span></span> 
- <span data-ttu-id="504cd-3352">id cards</span><span class="sxs-lookup"><span data-stu-id="504cd-3352">id cards</span></span> 
- <span data-ttu-id="504cd-3353">identification card</span><span class="sxs-lookup"><span data-stu-id="504cd-3353">identification card</span></span> 
- <span data-ttu-id="504cd-3354">identification cards</span><span class="sxs-lookup"><span data-stu-id="504cd-3354">identification cards</span></span> 
- <span data-ttu-id="504cd-3355">Дриверлик #</span><span class="sxs-lookup"><span data-stu-id="504cd-3355">DriverLic#</span></span> 
- <span data-ttu-id="504cd-3356">Дриверликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-3356">DriverLics#</span></span> 
- <span data-ttu-id="504cd-3357">Дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-3357">DriverLicense#</span></span> 
- <span data-ttu-id="504cd-3358">Дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-3358">DriverLicenses#</span></span> 
- <span data-ttu-id="504cd-3359">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-3359">Driver Lic#</span></span> 
- <span data-ttu-id="504cd-3360">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-3360">Driver Lics#</span></span> 
- <span data-ttu-id="504cd-3361">Driver License#</span><span class="sxs-lookup"><span data-stu-id="504cd-3361">Driver License#</span></span> 
- <span data-ttu-id="504cd-3362">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-3362">Driver Licenses#</span></span> 
- <span data-ttu-id="504cd-3363">Дриверслик #</span><span class="sxs-lookup"><span data-stu-id="504cd-3363">DriversLic#</span></span> 
- <span data-ttu-id="504cd-3364">Дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-3364">DriversLics#</span></span> 
- <span data-ttu-id="504cd-3365">Дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-3365">DriversLicense#</span></span> 
- <span data-ttu-id="504cd-3366">Дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-3366">DriversLicenses#</span></span> 
- <span data-ttu-id="504cd-3367">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-3367">Drivers Lic#</span></span> 
- <span data-ttu-id="504cd-3368">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-3368">Drivers Lics#</span></span> 
- <span data-ttu-id="504cd-3369">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="504cd-3369">Drivers License#</span></span> 
- <span data-ttu-id="504cd-3370">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-3370">Drivers Licenses#</span></span> 
- <span data-ttu-id="504cd-3371">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="504cd-3371">Driver'Lic#</span></span> 
- <span data-ttu-id="504cd-3372">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="504cd-3372">Driver'Lics#</span></span> 
- <span data-ttu-id="504cd-3373">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="504cd-3373">Driver'License#</span></span> 
- <span data-ttu-id="504cd-3374">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="504cd-3374">Driver'Licenses#</span></span> 
- <span data-ttu-id="504cd-3375">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-3375">Driver' Lic#</span></span> 
- <span data-ttu-id="504cd-3376">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-3376">Driver' Lics#</span></span> 
- <span data-ttu-id="504cd-3377">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="504cd-3377">Driver' License#</span></span> 
- <span data-ttu-id="504cd-3378">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-3378">Driver' Licenses#</span></span> 
- <span data-ttu-id="504cd-3379">Дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="504cd-3379">Driver'sLic#</span></span> 
- <span data-ttu-id="504cd-3380">Дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="504cd-3380">Driver'sLics#</span></span> 
- <span data-ttu-id="504cd-3381">Дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="504cd-3381">Driver'sLicense#</span></span> 
- <span data-ttu-id="504cd-3382">Дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="504cd-3382">Driver'sLicenses#</span></span> 
- <span data-ttu-id="504cd-3383">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="504cd-3383">Driver's Lic#</span></span> 
- <span data-ttu-id="504cd-3384">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="504cd-3384">Driver's Lics#</span></span> 
- <span data-ttu-id="504cd-3385">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="504cd-3385">Driver's License#</span></span> 
- <span data-ttu-id="504cd-3386">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="504cd-3386">Driver's Licenses#</span></span> 
- <span data-ttu-id="504cd-3387">id card#</span><span class="sxs-lookup"><span data-stu-id="504cd-3387">id card#</span></span> 
- <span data-ttu-id="504cd-3388">id cards#</span><span class="sxs-lookup"><span data-stu-id="504cd-3388">id cards#</span></span> 
- <span data-ttu-id="504cd-3389">identification card#</span><span class="sxs-lookup"><span data-stu-id="504cd-3389">identification card#</span></span> 
- <span data-ttu-id="504cd-3390">identification cards#</span><span class="sxs-lookup"><span data-stu-id="504cd-3390">identification cards#</span></span> 


#### <a name="keywordstatenamedriverslicensename"></a><span data-ttu-id="504cd-3391">Кэйворд_ [стате_наме] _дриверс_лиценсе_наме</span><span class="sxs-lookup"><span data-stu-id="504cd-3391">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="504cd-3392">Аббревиатура штата (например, NY)</span><span class="sxs-lookup"><span data-stu-id="504cd-3392">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="504cd-3393">Название штата (например, New York)</span><span class="sxs-lookup"><span data-stu-id="504cd-3393">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="504cd-3394">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="504cd-3394">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3395">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3395">Format</span></span>

<span data-ttu-id="504cd-3396">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="504cd-3396">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3397">Pattern</span></span>

<span data-ttu-id="504cd-3398">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="504cd-3398">Formatted:</span></span>
- <span data-ttu-id="504cd-3399">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="504cd-3399">The digit "9"</span></span> 
- <span data-ttu-id="504cd-3400">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3400">Two digits</span></span> 
- <span data-ttu-id="504cd-3401">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3401">A space or dash</span></span> 
- <span data-ttu-id="504cd-3402">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="504cd-3402">A "7" or "8"</span></span> 
- <span data-ttu-id="504cd-3403">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="504cd-3403">A digit</span></span> 
- <span data-ttu-id="504cd-3404">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="504cd-3404">A space, or dash</span></span> 
- <span data-ttu-id="504cd-3405">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3405">Four digits</span></span>

<span data-ttu-id="504cd-3406">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="504cd-3406">Unformatted:</span></span>
- <span data-ttu-id="504cd-3407">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="504cd-3407">The digit "9"</span></span> 
- <span data-ttu-id="504cd-3408">Две цифры</span><span class="sxs-lookup"><span data-stu-id="504cd-3408">Two digits</span></span> 
- <span data-ttu-id="504cd-3409">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="504cd-3409">A "7" or "8"</span></span> 
- <span data-ttu-id="504cd-3410">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="504cd-3410">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3411">Checksum</span></span>

<span data-ttu-id="504cd-3412">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3412">No</span></span>

### <a name="definition"></a><span data-ttu-id="504cd-3413">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3413">Definition</span></span>

<span data-ttu-id="504cd-3414">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3415">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3415">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3416">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-3416">At least one of the following is true:</span></span>
    - <span data-ttu-id="504cd-3417">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="504cd-3417">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="504cd-3418">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="504cd-3418">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="504cd-3419">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-3419">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="504cd-3420">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="504cd-3420">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="504cd-3421">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3421">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3422">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3422">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3423">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="504cd-3423">At least one of the following is true:</span></span>
    - <span data-ttu-id="504cd-3424">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="504cd-3424">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="504cd-3425">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="504cd-3425">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="504cd-3426">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="504cd-3426">The function Func_us_date finds a date in the right date format.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3427">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3427">Keywords</span></span>

#### <a name="keyworditin"></a><span data-ttu-id="504cd-3428">Кэйворд_итин</span><span class="sxs-lookup"><span data-stu-id="504cd-3428">Keyword_itin</span></span>

- <span data-ttu-id="504cd-3429">дубликат</span><span class="sxs-lookup"><span data-stu-id="504cd-3429">taxpayer</span></span> 
- <span data-ttu-id="504cd-3430">tax id</span><span class="sxs-lookup"><span data-stu-id="504cd-3430">tax id</span></span> 
- <span data-ttu-id="504cd-3431">tax identification</span><span class="sxs-lookup"><span data-stu-id="504cd-3431">tax identification</span></span> 
- <span data-ttu-id="504cd-3432">SharePointв</span><span class="sxs-lookup"><span data-stu-id="504cd-3432">itin</span></span> 
- <span data-ttu-id="504cd-3433">SSN</span><span class="sxs-lookup"><span data-stu-id="504cd-3433">ssn</span></span> 
- <span data-ttu-id="504cd-3434">ИНН</span><span class="sxs-lookup"><span data-stu-id="504cd-3434">tin</span></span> 
- <span data-ttu-id="504cd-3435">social security</span><span class="sxs-lookup"><span data-stu-id="504cd-3435">social security</span></span> 
- <span data-ttu-id="504cd-3436">tax payer</span><span class="sxs-lookup"><span data-stu-id="504cd-3436">tax payer</span></span> 
- <span data-ttu-id="504cd-3437">итинс</span><span class="sxs-lookup"><span data-stu-id="504cd-3437">itins</span></span> 
- <span data-ttu-id="504cd-3438">такси</span><span class="sxs-lookup"><span data-stu-id="504cd-3438">taxid</span></span> 
- <span data-ttu-id="504cd-3439">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="504cd-3439">individual taxpayer</span></span> 

#### <a name="keyworditincollaborative"></a><span data-ttu-id="504cd-3440">Кэйворд_итин_коллаборативе</span><span class="sxs-lookup"><span data-stu-id="504cd-3440">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="504cd-3441">License</span><span class="sxs-lookup"><span data-stu-id="504cd-3441">License</span></span> 
- <span data-ttu-id="504cd-3442">DL</span><span class="sxs-lookup"><span data-stu-id="504cd-3442">DL</span></span> 
- <span data-ttu-id="504cd-3443">ДОБ</span><span class="sxs-lookup"><span data-stu-id="504cd-3443">DOB</span></span> 
- <span data-ttu-id="504cd-3444">Birthdate</span><span class="sxs-lookup"><span data-stu-id="504cd-3444">Birthdate</span></span> 
- <span data-ttu-id="504cd-3445">День рождения</span><span class="sxs-lookup"><span data-stu-id="504cd-3445">Birthday</span></span> 
- <span data-ttu-id="504cd-3446">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="504cd-3446">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="504cd-3447">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="504cd-3447">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="504cd-3448">Format</span><span class="sxs-lookup"><span data-stu-id="504cd-3448">Format</span></span>

<span data-ttu-id="504cd-3449">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="504cd-3449">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="504cd-3450">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="504cd-3450">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="504cd-3451">Шаблон</span><span class="sxs-lookup"><span data-stu-id="504cd-3451">Pattern</span></span>

<span data-ttu-id="504cd-3452">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="504cd-3452">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="504cd-3453">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="504cd-3453">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="504cd-3454">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="504cd-3454">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="504cd-3455">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="504cd-3455">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="504cd-3456">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="504cd-3456">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="504cd-3457">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="504cd-3457">Checksum</span></span>

<span data-ttu-id="504cd-3458">Нет</span><span class="sxs-lookup"><span data-stu-id="504cd-3458">No</span></span>


### <a name="definition"></a><span data-ttu-id="504cd-3459">Определение</span><span class="sxs-lookup"><span data-stu-id="504cd-3459">Definition</span></span>

<span data-ttu-id="504cd-3460">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3461">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3461">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3462">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="504cd-3462">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="504cd-3463">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3464">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3464">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3465">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="504cd-3465">A keyword from Keyword_ssn is found.</span></span>

<span data-ttu-id="504cd-3466">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3467">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3467">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3468">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="504cd-3468">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="504cd-3469">Функция Func_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3469">The function Func_ssn does not find content that matches the pattern.</span></span>

<span data-ttu-id="504cd-3470">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="504cd-3470">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="504cd-3471">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3471">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="504cd-3472">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="504cd-3472">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="504cd-3473">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="504cd-3473">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>

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

### <a name="keywords"></a><span data-ttu-id="504cd-3474">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="504cd-3474">Keywords</span></span>

#### <a name="keywordssn"></a><span data-ttu-id="504cd-3475">Кэйворд_ссн</span><span class="sxs-lookup"><span data-stu-id="504cd-3475">Keyword_ssn</span></span>

- <span data-ttu-id="504cd-3476">Social Security</span><span class="sxs-lookup"><span data-stu-id="504cd-3476">Social Security</span></span> 
- <span data-ttu-id="504cd-3477">Social Security#</span><span class="sxs-lookup"><span data-stu-id="504cd-3477">Social Security#</span></span> 
- <span data-ttu-id="504cd-3478">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="504cd-3478">Soc Sec</span></span> 
- <span data-ttu-id="504cd-3479">SSN</span><span class="sxs-lookup"><span data-stu-id="504cd-3479">SSN</span></span> 
- <span data-ttu-id="504cd-3480">SSNS</span><span class="sxs-lookup"><span data-stu-id="504cd-3480">SSNS</span></span> 
- <span data-ttu-id="504cd-3481">SSN</span><span class="sxs-lookup"><span data-stu-id="504cd-3481">SSN#</span></span> 
- <span data-ttu-id="504cd-3482">НН</span><span class="sxs-lookup"><span data-stu-id="504cd-3482">SS#</span></span> 
- <span data-ttu-id="504cd-3483">SSID</span><span class="sxs-lookup"><span data-stu-id="504cd-3483">SSID</span></span> 
   

