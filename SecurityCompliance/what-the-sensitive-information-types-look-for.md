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
ms.openlocfilehash: d486510c35aaf147e6d63e28d1df36ef689e3975
ms.sourcegitcommit: a5a7e43822336ed18d8f5879167766686cf6b2a3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2019
ms.locfileid: "36478258"
---
# <a name="what-the-sensitive-information-types-look-for"></a><span data-ttu-id="31aad-104">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="31aad-104">What the sensitive information types look for</span></span>

<span data-ttu-id="31aad-105">Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="31aad-105">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies.</span></span> <span data-ttu-id="31aad-106">В этой статье перечислены все эти типы конфиденциальной информации и показано, каким именно образом политика защиты от потери данных выявляет каждый тип.</span><span class="sxs-lookup"><span data-stu-id="31aad-106">This topic lists all of these sensitive information types and shows what a DLP policy looks for when it detects each type.</span></span> <span data-ttu-id="31aad-107">Тип конфиденциальной информации определяется шаблоном, который можно идентифицировать регулярным выражением или функцией.</span><span class="sxs-lookup"><span data-stu-id="31aad-107">A sensitive information type is defined by a pattern that can be identified by a regular expression or a function.</span></span> <span data-ttu-id="31aad-108">Кроме того, для идентификации типа конфиденциальной информации могут использоваться подкрепляющие доказательства, такие как ключевые слова и контрольные суммы.</span><span class="sxs-lookup"><span data-stu-id="31aad-108">In addition, corroborative evidence such as keywords and checksums can be used to identify a sensitive information type.</span></span> <span data-ttu-id="31aad-109">Уровень вероятности и расположение слов и знаков также используются в процессе оценки.</span><span class="sxs-lookup"><span data-stu-id="31aad-109">Confidence level and proximity are also used in the evaluation process.</span></span>
  
## <a name="aba-routing-number"></a><span data-ttu-id="31aad-110">Код банка ABA</span><span class="sxs-lookup"><span data-stu-id="31aad-110">ABA Routing Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-111">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-111">Format</span></span>

<span data-ttu-id="31aad-112">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="31aad-112">9 digits which may be in a formatted or unformatted pattern</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-113">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-113">Pattern</span></span>

<span data-ttu-id="31aad-114">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="31aad-114">Formatted:</span></span>
- <span data-ttu-id="31aad-115">четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;</span><span class="sxs-lookup"><span data-stu-id="31aad-115">Four digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span>
- <span data-ttu-id="31aad-116">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-116">A hyphen</span></span>
- <span data-ttu-id="31aad-117">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-117">Four digits</span></span>
- <span data-ttu-id="31aad-118">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-118">A hyphen</span></span>
- <span data-ttu-id="31aad-119">цифра.</span><span class="sxs-lookup"><span data-stu-id="31aad-119">A digit</span></span>

<span data-ttu-id="31aad-120">Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8.</span><span class="sxs-lookup"><span data-stu-id="31aad-120">Unformatted: 9 consecutive digits beginning with 0, 1, 2, 3, 6, 7, or 8</span></span> 

### <a name="checksum"></a><span data-ttu-id="31aad-121">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-121">Checksum</span></span>

<span data-ttu-id="31aad-122">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-122">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-123">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-123">Definition</span></span>

<span data-ttu-id="31aad-124">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-124">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-125">функция Func_aba_routing находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-125">The function Func_aba_routing finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-126">находится ключевое слово из Keyword_ABA_Routing.</span><span class="sxs-lookup"><span data-stu-id="31aad-126">A keyword from Keyword_ABA_Routing is found.</span></span>

```xml
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a><span data-ttu-id="31aad-127">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-127">Keywords</span></span>

#### <a name="keyword_aba_routing"></a><span data-ttu-id="31aad-128">Keyword_ABA_Routing</span><span class="sxs-lookup"><span data-stu-id="31aad-128">Keyword_ABA_Routing</span></span>

- <span data-ttu-id="31aad-129">код банка ABA</span><span class="sxs-lookup"><span data-stu-id="31aad-129">aba</span></span>
- <span data-ttu-id="31aad-130">aba#</span><span class="sxs-lookup"><span data-stu-id="31aad-130">aba #</span></span>
- <span data-ttu-id="31aad-131">aba routing #</span><span class="sxs-lookup"><span data-stu-id="31aad-131">aba routing #</span></span>
- <span data-ttu-id="31aad-132">aba routing number</span><span class="sxs-lookup"><span data-stu-id="31aad-132">aba routing number</span></span>
- <span data-ttu-id="31aad-133">код банка ABA #</span><span class="sxs-lookup"><span data-stu-id="31aad-133">aba#</span></span>
- <span data-ttu-id="31aad-134">абараутинг #</span><span class="sxs-lookup"><span data-stu-id="31aad-134">abarouting#</span></span>
- <span data-ttu-id="31aad-135">aba number</span><span class="sxs-lookup"><span data-stu-id="31aad-135">aba number</span></span>
- <span data-ttu-id="31aad-136">абараутингнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-136">abaroutingnumber</span></span>
- <span data-ttu-id="31aad-137">american bank association routing #</span><span class="sxs-lookup"><span data-stu-id="31aad-137">american bank association routing #</span></span>
- <span data-ttu-id="31aad-138">american bank association routing number</span><span class="sxs-lookup"><span data-stu-id="31aad-138">american bank association routing number</span></span>
- <span data-ttu-id="31aad-139">американбанкассоЦиатионраутинг #</span><span class="sxs-lookup"><span data-stu-id="31aad-139">americanbankassociationrouting#</span></span>
- <span data-ttu-id="31aad-140">американбанкассоЦиатионраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-140">americanbankassociationroutingnumber</span></span>
- <span data-ttu-id="31aad-141">bank routing number</span><span class="sxs-lookup"><span data-stu-id="31aad-141">bank routing number</span></span>
- <span data-ttu-id="31aad-142">банкраутинг #</span><span class="sxs-lookup"><span data-stu-id="31aad-142">bankrouting#</span></span>
- <span data-ttu-id="31aad-143">банкраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-143">bankroutingnumber</span></span>
- <span data-ttu-id="31aad-144">routing transit number</span><span class="sxs-lookup"><span data-stu-id="31aad-144">routing transit number</span></span>
- <span data-ttu-id="31aad-145">ртн</span><span class="sxs-lookup"><span data-stu-id="31aad-145">RTN</span></span> 
   
## <a name="argentina-national-identity-dni-number"></a><span data-ttu-id="31aad-146">Номер внутреннего удостоверения личности для Аргентины (DNI)</span><span class="sxs-lookup"><span data-stu-id="31aad-146">Argentina National Identity (DNI) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-147">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-147">Format</span></span>

<span data-ttu-id="31aad-148">Восемь цифр, разделенных точками.</span><span class="sxs-lookup"><span data-stu-id="31aad-148">Eight digits separated by periods</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-149">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-149">Pattern</span></span>

<span data-ttu-id="31aad-150">Восемь цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-150">Eight digits:</span></span>
- <span data-ttu-id="31aad-151">две цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-151">Two digits</span></span>
- <span data-ttu-id="31aad-152">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-152">A period</span></span>
- <span data-ttu-id="31aad-153">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-153">Three digits</span></span>
- <span data-ttu-id="31aad-154">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-154">A period</span></span>
- <span data-ttu-id="31aad-155">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-155">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-156">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-156">Checksum</span></span>

<span data-ttu-id="31aad-157">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-157">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-158">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-158">Definition</span></span>

<span data-ttu-id="31aad-159">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-159">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-160">регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-160">The regular expression Regex_argentina_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-161">находится ключевое слово из Keyword_argentina_national_id.</span><span class="sxs-lookup"><span data-stu-id="31aad-161">A keyword from Keyword_argentina_national_id is found.</span></span>

```xml
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-162">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-162">Keywords</span></span>

#### <a name="keyword_argentina_national_id"></a><span data-ttu-id="31aad-163">Keyword_argentina_national_id</span><span class="sxs-lookup"><span data-stu-id="31aad-163">Keyword_argentina_national_id</span></span>

- <span data-ttu-id="31aad-164">Argentina National Identity number</span><span class="sxs-lookup"><span data-stu-id="31aad-164">Argentina National Identity number</span></span> 
- <span data-ttu-id="31aad-165">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="31aad-165">Identity</span></span> 
- <span data-ttu-id="31aad-166">Идентификация национальной идентификационной карточки</span><span class="sxs-lookup"><span data-stu-id="31aad-166">Identification National Identity Card</span></span> 
- <span data-ttu-id="31aad-167">DNI</span><span class="sxs-lookup"><span data-stu-id="31aad-167">DNI</span></span> 
- <span data-ttu-id="31aad-168">Национальная реестр пользователей NIC</span><span class="sxs-lookup"><span data-stu-id="31aad-168">NIC National Registry of Persons</span></span> 
- <span data-ttu-id="31aad-169">Documento Nacional de Identidad</span><span class="sxs-lookup"><span data-stu-id="31aad-169">Documento Nacional de Identidad</span></span> 
- <span data-ttu-id="31aad-170">Registro Nacional de las Personas</span><span class="sxs-lookup"><span data-stu-id="31aad-170">Registro Nacional de las Personas</span></span> 
- <span data-ttu-id="31aad-171">идентидад</span><span class="sxs-lookup"><span data-stu-id="31aad-171">Identidad</span></span> 
- <span data-ttu-id="31aad-172">идентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="31aad-172">Identificación</span></span> 
   
## <a name="australia-bank-account-number"></a><span data-ttu-id="31aad-173">Номер банковского счета для Австралии</span><span class="sxs-lookup"><span data-stu-id="31aad-173">Australia Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-174">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-174">Format</span></span>

<span data-ttu-id="31aad-175">6–10 цифр с номером филиала банка в штате или без него.</span><span class="sxs-lookup"><span data-stu-id="31aad-175">6-10 digits with or without a bank state branch number</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-176">Pattern</span></span>

<span data-ttu-id="31aad-177">Номер счета состоит из 6–10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-177">Account number is 6-10 digits.</span></span>
<span data-ttu-id="31aad-178">Номер филиала государственного банка Австралии</span><span class="sxs-lookup"><span data-stu-id="31aad-178">Australia bank state branch number:</span></span>
- <span data-ttu-id="31aad-179">три цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-179">Three digits</span></span> 
- <span data-ttu-id="31aad-180">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-180">A hyphen</span></span> 
- <span data-ttu-id="31aad-181">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-181">Three digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-182">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-182">Checksum</span></span>

<span data-ttu-id="31aad-183">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-183">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-184">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-184">Definition</span></span>

<span data-ttu-id="31aad-185">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-185">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-186">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-186">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="31aad-187">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-187">A keyword from Keyword_australia_bank_account_number is found.</span></span>
- <span data-ttu-id="31aad-188">регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-188">The regular expression Regex_australia_bank_account_number_bsb finds content that matches the pattern.</span></span>

<span data-ttu-id="31aad-189">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-189">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-190">регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-190">The regular expression Regex_australia_bank_account_number finds content that matches the pattern..</span></span>
- <span data-ttu-id="31aad-191">находится ключевое слово из Keyword_australia_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-191">A keyword from Keyword_australia_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-192">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-192">Keywords</span></span>

#### <a name="keyword_australia_bank_account_number"></a><span data-ttu-id="31aad-193">Keyword_australia_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="31aad-193">Keyword_australia_bank_account_number</span></span>

- <span data-ttu-id="31aad-194">swift bank code</span><span class="sxs-lookup"><span data-stu-id="31aad-194">swift bank code</span></span>
- <span data-ttu-id="31aad-195">correspondent bank</span><span class="sxs-lookup"><span data-stu-id="31aad-195">correspondent bank</span></span>
- <span data-ttu-id="31aad-196">base currency</span><span class="sxs-lookup"><span data-stu-id="31aad-196">base currency</span></span>
- <span data-ttu-id="31aad-197">usa account</span><span class="sxs-lookup"><span data-stu-id="31aad-197">usa account</span></span>
- <span data-ttu-id="31aad-198">holder address</span><span class="sxs-lookup"><span data-stu-id="31aad-198">holder address</span></span>
- <span data-ttu-id="31aad-199">bank address</span><span class="sxs-lookup"><span data-stu-id="31aad-199">bank address</span></span>
- <span data-ttu-id="31aad-200">information account</span><span class="sxs-lookup"><span data-stu-id="31aad-200">information account</span></span>
- <span data-ttu-id="31aad-201">fund transfers</span><span class="sxs-lookup"><span data-stu-id="31aad-201">fund transfers</span></span>
- <span data-ttu-id="31aad-202">bank charges</span><span class="sxs-lookup"><span data-stu-id="31aad-202">bank charges</span></span>
- <span data-ttu-id="31aad-203">bank details</span><span class="sxs-lookup"><span data-stu-id="31aad-203">bank details</span></span>
- <span data-ttu-id="31aad-204">banking information</span><span class="sxs-lookup"><span data-stu-id="31aad-204">banking information</span></span>
- <span data-ttu-id="31aad-205">full names</span><span class="sxs-lookup"><span data-stu-id="31aad-205">full names</span></span>
- <span data-ttu-id="31aad-206">иаеа</span><span class="sxs-lookup"><span data-stu-id="31aad-206">iaea</span></span>

   
## <a name="australia-drivers-license-number"></a><span data-ttu-id="31aad-207">Номер водительского удостоверения для Австралии</span><span class="sxs-lookup"><span data-stu-id="31aad-207">Australia Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-208">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-208">Format</span></span>

<span data-ttu-id="31aad-209">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-209">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-210">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-210">Pattern</span></span>

<span data-ttu-id="31aad-211">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-211">Nine letters and digits:</span></span> 

- <span data-ttu-id="31aad-212">две цифры или буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-212">Two digits or letters (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-213">две цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-213">Two digits</span></span> 
- <span data-ttu-id="31aad-214">пять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="31aad-214">Five digits or letters (not case sensitive)</span></span>

<span data-ttu-id="31aad-215">OR</span><span class="sxs-lookup"><span data-stu-id="31aad-215">OR</span></span>

- <span data-ttu-id="31aad-216">1–2 дополнительные буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-216">1-2 optional letters (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-217">4–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-217">4-9 digits</span></span>

<span data-ttu-id="31aad-218">OR</span><span class="sxs-lookup"><span data-stu-id="31aad-218">OR</span></span>

- <span data-ttu-id="31aad-219">девять цифр или букв (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="31aad-219">Nine digits or letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-220">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-220">Checksum</span></span>

<span data-ttu-id="31aad-221">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-221">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-222">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-222">Definition</span></span>

<span data-ttu-id="31aad-223">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-223">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-224">регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-224">The regular expression Regex_australia_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-225">находится ключевое слово из Keyword_australia_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-225">A keyword from Keyword_australia_drivers_license_number is found.</span></span>
- <span data-ttu-id="31aad-226">ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.</span><span class="sxs-lookup"><span data-stu-id="31aad-226">No keyword from Keyword_australia_drivers_license_number_exclusions is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-227">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-227">Keywords</span></span>

#### <a name="keyword_australia_drivers_license_number"></a><span data-ttu-id="31aad-228">Keyword_australia_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="31aad-228">Keyword_australia_drivers_license_number</span></span>

- <span data-ttu-id="31aad-229">international driving permits</span><span class="sxs-lookup"><span data-stu-id="31aad-229">international driving permits</span></span>
- <span data-ttu-id="31aad-230">australian automobile association</span><span class="sxs-lookup"><span data-stu-id="31aad-230">australian automobile association</span></span>
- <span data-ttu-id="31aad-231">international driving permit</span><span class="sxs-lookup"><span data-stu-id="31aad-231">international driving permit</span></span>
- <span data-ttu-id="31aad-232">дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="31aad-232">DriverLicence</span></span>
- <span data-ttu-id="31aad-233">дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="31aad-233">DriverLicences</span></span>
- <span data-ttu-id="31aad-234">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-234">Driver Lic</span></span>
- <span data-ttu-id="31aad-235">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-235">Driver Licence</span></span>
- <span data-ttu-id="31aad-236">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-236">Driver Licences</span></span>
- <span data-ttu-id="31aad-237">дриверслик</span><span class="sxs-lookup"><span data-stu-id="31aad-237">DriversLic</span></span>
- <span data-ttu-id="31aad-238">дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="31aad-238">DriversLicence</span></span>
- <span data-ttu-id="31aad-239">дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="31aad-239">DriversLicences</span></span>
- <span data-ttu-id="31aad-240">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-240">Drivers Lic</span></span>
- <span data-ttu-id="31aad-241">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-241">Drivers Lics</span></span>
- <span data-ttu-id="31aad-242">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-242">Drivers Licence</span></span>
- <span data-ttu-id="31aad-243">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-243">Drivers Licences</span></span>
- <span data-ttu-id="31aad-244">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="31aad-244">Driver'Lic</span></span>
- <span data-ttu-id="31aad-245">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="31aad-245">Driver'Lics</span></span>
- <span data-ttu-id="31aad-246">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-246">Driver'Licence</span></span>
- <span data-ttu-id="31aad-247">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-247">Driver'Licences</span></span>
- <span data-ttu-id="31aad-248">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-248">Driver' Lic</span></span>
- <span data-ttu-id="31aad-249">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-249">Driver' Lics</span></span>
- <span data-ttu-id="31aad-250">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-250">Driver' Licence</span></span>
- <span data-ttu-id="31aad-251">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-251">Driver' Licences</span></span>
- <span data-ttu-id="31aad-252">дривер'слик</span><span class="sxs-lookup"><span data-stu-id="31aad-252">Driver'sLic</span></span>
- <span data-ttu-id="31aad-253">дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="31aad-253">Driver'sLics</span></span>
- <span data-ttu-id="31aad-254">дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="31aad-254">Driver'sLicence</span></span>
- <span data-ttu-id="31aad-255">дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="31aad-255">Driver'sLicences</span></span>
- <span data-ttu-id="31aad-256">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-256">Driver's Lic</span></span>
- <span data-ttu-id="31aad-257">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-257">Driver's Lics</span></span>
- <span data-ttu-id="31aad-258">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-258">Driver's Licence</span></span>
- <span data-ttu-id="31aad-259">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-259">Driver's Licences</span></span>
- <span data-ttu-id="31aad-260">дриверлик #</span><span class="sxs-lookup"><span data-stu-id="31aad-260">DriverLic#</span></span>
- <span data-ttu-id="31aad-261">дриверликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-261">DriverLics#</span></span>
- <span data-ttu-id="31aad-262">дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="31aad-262">DriverLicence#</span></span>
- <span data-ttu-id="31aad-263">дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="31aad-263">DriverLicences#</span></span>
- <span data-ttu-id="31aad-264">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-264">Driver Lic#</span></span>
- <span data-ttu-id="31aad-265">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-265">Driver Lics#</span></span>
- <span data-ttu-id="31aad-266">Driver Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-266">Driver Licence#</span></span>
- <span data-ttu-id="31aad-267">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-267">Driver Licences#</span></span>
- <span data-ttu-id="31aad-268">дриверслик #</span><span class="sxs-lookup"><span data-stu-id="31aad-268">DriversLic#</span></span>
- <span data-ttu-id="31aad-269">дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-269">DriversLics#</span></span>
- <span data-ttu-id="31aad-270">дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="31aad-270">DriversLicence#</span></span>
- <span data-ttu-id="31aad-271">дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="31aad-271">DriversLicences#</span></span>
- <span data-ttu-id="31aad-272">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-272">Drivers Lic#</span></span>
- <span data-ttu-id="31aad-273">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-273">Drivers Lics#</span></span>
- <span data-ttu-id="31aad-274">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-274">Drivers Licence#</span></span>
- <span data-ttu-id="31aad-275">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-275">Drivers Licences#</span></span>
- <span data-ttu-id="31aad-276">Driver ' LIC #</span><span class="sxs-lookup"><span data-stu-id="31aad-276">Driver'Lic#</span></span>
- <span data-ttu-id="31aad-277">Driver ' LICS #</span><span class="sxs-lookup"><span data-stu-id="31aad-277">Driver'Lics#</span></span>
- <span data-ttu-id="31aad-278">Driver ' Licence #</span><span class="sxs-lookup"><span data-stu-id="31aad-278">Driver'Licence#</span></span>
- <span data-ttu-id="31aad-279">Driver ' Licences #</span><span class="sxs-lookup"><span data-stu-id="31aad-279">Driver'Licences#</span></span>
- <span data-ttu-id="31aad-280">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-280">Driver' Lic#</span></span>
- <span data-ttu-id="31aad-281">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-281">Driver' Lics#</span></span>
- <span data-ttu-id="31aad-282">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-282">Driver' Licence#</span></span>
- <span data-ttu-id="31aad-283">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-283">Driver' Licences#</span></span>
- <span data-ttu-id="31aad-284">дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="31aad-284">Driver'sLic#</span></span>
- <span data-ttu-id="31aad-285">дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-285">Driver'sLics#</span></span>
- <span data-ttu-id="31aad-286">дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="31aad-286">Driver'sLicence#</span></span>
- <span data-ttu-id="31aad-287">дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="31aad-287">Driver'sLicences#</span></span>
- <span data-ttu-id="31aad-288">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-288">Driver's Lic#</span></span>
- <span data-ttu-id="31aad-289">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-289">Driver's Lics#</span></span>
- <span data-ttu-id="31aad-290">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-290">Driver's Licence#</span></span>
- <span data-ttu-id="31aad-291">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-291">Driver's Licences#</span></span> 

#### <a name="keyword_australia_drivers_license_number_exclusions"></a><span data-ttu-id="31aad-292">Keyword_australia_drivers_license_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="31aad-292">Keyword_australia_drivers_license_number_exclusions</span></span>

- <span data-ttu-id="31aad-293">AAA</span><span class="sxs-lookup"><span data-stu-id="31aad-293">aaa</span></span>
- <span data-ttu-id="31aad-294">дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-294">DriverLicense</span></span>
- <span data-ttu-id="31aad-295">дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-295">DriverLicenses</span></span>
- <span data-ttu-id="31aad-296">Driver License</span><span class="sxs-lookup"><span data-stu-id="31aad-296">Driver License</span></span>
- <span data-ttu-id="31aad-297">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-297">Driver Licenses</span></span>
- <span data-ttu-id="31aad-298">дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-298">DriversLicense</span></span>
- <span data-ttu-id="31aad-299">дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-299">DriversLicenses</span></span>
- <span data-ttu-id="31aad-300">Drivers License</span><span class="sxs-lookup"><span data-stu-id="31aad-300">Drivers License</span></span>
- <span data-ttu-id="31aad-301">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-301">Drivers Licenses</span></span>
- <span data-ttu-id="31aad-302">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="31aad-302">Driver'License</span></span>
- <span data-ttu-id="31aad-303">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-303">Driver'Licenses</span></span>
- <span data-ttu-id="31aad-304">Driver' License</span><span class="sxs-lookup"><span data-stu-id="31aad-304">Driver' License</span></span>
- <span data-ttu-id="31aad-305">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-305">Driver' Licenses</span></span>
- <span data-ttu-id="31aad-306">дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-306">Driver'sLicense</span></span>
- <span data-ttu-id="31aad-307">дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-307">Driver'sLicenses</span></span>
- <span data-ttu-id="31aad-308">Driver's License</span><span class="sxs-lookup"><span data-stu-id="31aad-308">Driver's License</span></span>
- <span data-ttu-id="31aad-309">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-309">Driver's Licenses</span></span>
- <span data-ttu-id="31aad-310">дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-310">DriverLicense#</span></span>
- <span data-ttu-id="31aad-311">дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-311">DriverLicenses#</span></span>
- <span data-ttu-id="31aad-312">Driver License#</span><span class="sxs-lookup"><span data-stu-id="31aad-312">Driver License#</span></span>
- <span data-ttu-id="31aad-313">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-313">Driver Licenses#</span></span>
- <span data-ttu-id="31aad-314">дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-314">DriversLicense#</span></span>
- <span data-ttu-id="31aad-315">дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-315">DriversLicenses#</span></span>
- <span data-ttu-id="31aad-316">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="31aad-316">Drivers License#</span></span>
- <span data-ttu-id="31aad-317">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-317">Drivers Licenses#</span></span>
- <span data-ttu-id="31aad-318">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="31aad-318">Driver'License#</span></span>
- <span data-ttu-id="31aad-319">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="31aad-319">Driver'Licenses#</span></span>
- <span data-ttu-id="31aad-320">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="31aad-320">Driver' License#</span></span>
- <span data-ttu-id="31aad-321">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-321">Driver' Licenses#</span></span>
- <span data-ttu-id="31aad-322">дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-322">Driver'sLicense#</span></span>
- <span data-ttu-id="31aad-323">дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-323">Driver'sLicenses#</span></span>
- <span data-ttu-id="31aad-324">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="31aad-324">Driver's License#</span></span>
- <span data-ttu-id="31aad-325">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-325">Driver's Licenses#</span></span>
   
## <a name="australia-medical-account-number"></a><span data-ttu-id="31aad-326">Номер карты медицинского страхования для Австралии</span><span class="sxs-lookup"><span data-stu-id="31aad-326">Australia Medical Account Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-327">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-327">Format</span></span>

<span data-ttu-id="31aad-328">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-328">10-11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-329">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-329">Pattern</span></span>

<span data-ttu-id="31aad-330">10–11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-330">10-11 digits:</span></span>
- <span data-ttu-id="31aad-331">Первая цифра находится в диапазоне 2–6.</span><span class="sxs-lookup"><span data-stu-id="31aad-331">First digit is in the range 2-6</span></span>
- <span data-ttu-id="31aad-332">Девятая цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-332">Ninth digit is a check digit</span></span>
- <span data-ttu-id="31aad-333">Десятая цифра — цифра серии.</span><span class="sxs-lookup"><span data-stu-id="31aad-333">Tenth digit is the issue digit</span></span>
- <span data-ttu-id="31aad-334">Одиннадцатая цифра (необязательно) — индивидуальный номер.</span><span class="sxs-lookup"><span data-stu-id="31aad-334">Eleventh digit (optional) is the individual number</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-335">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-335">Checksum</span></span>

<span data-ttu-id="31aad-336">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-336">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-337">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-337">Definition</span></span>

<span data-ttu-id="31aad-338">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-338">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-339">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-339">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-340">находится ключевое слово из Keyword_Australia_Medical_Account_Number;</span><span class="sxs-lookup"><span data-stu-id="31aad-340">A keyword from Keyword_Australia_Medical_Account_Number is found.</span></span>
- <span data-ttu-id="31aad-341">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-341">The checksum passes.</span></span>

<span data-ttu-id="31aad-342">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-342">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-343">функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-343">The function Func_australian_medical_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-344">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-344">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-345">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-345">Keywords</span></span>

#### <a name="keyword_australia_medical_account_number"></a><span data-ttu-id="31aad-346">Keyword_Australia_Medical_Account_Number</span><span class="sxs-lookup"><span data-stu-id="31aad-346">Keyword_Australia_Medical_Account_Number</span></span>

- <span data-ttu-id="31aad-347">bank account details</span><span class="sxs-lookup"><span data-stu-id="31aad-347">bank account details</span></span>
- <span data-ttu-id="31aad-348">medicare payments</span><span class="sxs-lookup"><span data-stu-id="31aad-348">medicare payments</span></span>
- <span data-ttu-id="31aad-349">mortgage account</span><span class="sxs-lookup"><span data-stu-id="31aad-349">mortgage account</span></span>
- <span data-ttu-id="31aad-350">bank payments</span><span class="sxs-lookup"><span data-stu-id="31aad-350">bank payments</span></span>
- <span data-ttu-id="31aad-351">information branch</span><span class="sxs-lookup"><span data-stu-id="31aad-351">information branch</span></span>
- <span data-ttu-id="31aad-352">credit card loan</span><span class="sxs-lookup"><span data-stu-id="31aad-352">credit card loan</span></span>
- <span data-ttu-id="31aad-353">department of human services</span><span class="sxs-lookup"><span data-stu-id="31aad-353">department of human services</span></span>
- <span data-ttu-id="31aad-354">local service</span><span class="sxs-lookup"><span data-stu-id="31aad-354">local service</span></span>
- <span data-ttu-id="31aad-355">медикаре</span><span class="sxs-lookup"><span data-stu-id="31aad-355">medicare</span></span>

   
## <a name="australia-passport-number"></a><span data-ttu-id="31aad-356">Номер паспорта гражданина Австралии</span><span class="sxs-lookup"><span data-stu-id="31aad-356">Australia Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-357">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-357">Format</span></span>

<span data-ttu-id="31aad-358">Буква, за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-358">A letter followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-359">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-359">Pattern</span></span>

<span data-ttu-id="31aad-360">Буква (без учета регистра), за которой следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-360">A letter (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-361">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-361">Checksum</span></span>

<span data-ttu-id="31aad-362">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-362">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-363">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-363">Definition</span></span>

<span data-ttu-id="31aad-364">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-365">регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-365">The regular expression Regex_australia_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-366">Найдено ключевое слово из Keyword_passport или Keyword_australia_passport_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-366">A keyword from Keyword_passport or Keyword_australia_passport_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-367">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-367">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="31aad-368">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-368">Keyword_passport</span></span>

- <span data-ttu-id="31aad-369">Passport Number</span><span class="sxs-lookup"><span data-stu-id="31aad-369">Passport Number</span></span>
- <span data-ttu-id="31aad-370">Passport No</span><span class="sxs-lookup"><span data-stu-id="31aad-370">Passport No</span></span>
- <span data-ttu-id="31aad-371">Passport#</span><span class="sxs-lookup"><span data-stu-id="31aad-371">Passport #</span></span>
- <span data-ttu-id="31aad-372">Службу #</span><span class="sxs-lookup"><span data-stu-id="31aad-372">Passport#</span></span>
- <span data-ttu-id="31aad-373">пасспортид</span><span class="sxs-lookup"><span data-stu-id="31aad-373">PassportID</span></span>
- <span data-ttu-id="31aad-374">пасспортно</span><span class="sxs-lookup"><span data-stu-id="31aad-374">Passportno</span></span>
- <span data-ttu-id="31aad-375">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-375">passportnumber</span></span>
- <span data-ttu-id="31aad-376">パスポート</span><span class="sxs-lookup"><span data-stu-id="31aad-376">パスポート</span></span>
- <span data-ttu-id="31aad-377">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="31aad-377">パスポート番号</span></span>
- <span data-ttu-id="31aad-378">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="31aad-378">パスポートのNum</span></span>
- <span data-ttu-id="31aad-379">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="31aad-379">パスポート ＃</span></span> 
- <span data-ttu-id="31aad-380">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="31aad-380">Numéro de passeport</span></span>
- <span data-ttu-id="31aad-381">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="31aad-381">Passeport n °</span></span>
- <span data-ttu-id="31aad-382">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="31aad-382">Passeport Non</span></span>
- <span data-ttu-id="31aad-383">Passeport#</span><span class="sxs-lookup"><span data-stu-id="31aad-383">Passeport #</span></span>
- <span data-ttu-id="31aad-384">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="31aad-384">Passeport#</span></span>
- <span data-ttu-id="31aad-385">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="31aad-385">PasseportNon</span></span>
- <span data-ttu-id="31aad-386">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="31aad-386">Passeportn °</span></span>

#### <a name="keyword_australia_passport_number"></a><span data-ttu-id="31aad-387">Keyword_australia_passport_number</span><span class="sxs-lookup"><span data-stu-id="31aad-387">Keyword_australia_passport_number</span></span>

- <span data-ttu-id="31aad-388">службу</span><span class="sxs-lookup"><span data-stu-id="31aad-388">passport</span></span>
- <span data-ttu-id="31aad-389">passport details</span><span class="sxs-lookup"><span data-stu-id="31aad-389">passport details</span></span>
- <span data-ttu-id="31aad-390">immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="31aad-390">immigration and citizenship</span></span>
- <span data-ttu-id="31aad-391">commonwealth of australia</span><span class="sxs-lookup"><span data-stu-id="31aad-391">commonwealth of australia</span></span>
- <span data-ttu-id="31aad-392">department of immigration</span><span class="sxs-lookup"><span data-stu-id="31aad-392">department of immigration</span></span>
- <span data-ttu-id="31aad-393">residential address</span><span class="sxs-lookup"><span data-stu-id="31aad-393">residential address</span></span>
- <span data-ttu-id="31aad-394">department of immigration and citizenship</span><span class="sxs-lookup"><span data-stu-id="31aad-394">department of immigration and citizenship</span></span>
- <span data-ttu-id="31aad-395">Visa</span><span class="sxs-lookup"><span data-stu-id="31aad-395">visa</span></span>
- <span data-ttu-id="31aad-396">national identity card</span><span class="sxs-lookup"><span data-stu-id="31aad-396">national identity card</span></span>
- <span data-ttu-id="31aad-397">passport number</span><span class="sxs-lookup"><span data-stu-id="31aad-397">passport number</span></span>
- <span data-ttu-id="31aad-398">travel document</span><span class="sxs-lookup"><span data-stu-id="31aad-398">travel document</span></span>
- <span data-ttu-id="31aad-399">issuing authority</span><span class="sxs-lookup"><span data-stu-id="31aad-399">issuing authority</span></span>
   
## <a name="australia-tax-file-number"></a><span data-ttu-id="31aad-400">Номер налогоплательщика для Австралии</span><span class="sxs-lookup"><span data-stu-id="31aad-400">Australia Tax File Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-401">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-401">Format</span></span>

<span data-ttu-id="31aad-402">8–9 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-402">8-9 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-403">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-403">Pattern</span></span>

<span data-ttu-id="31aad-404">8–9 цифр, которые обычно разделены пробелами указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="31aad-404">8-9 digits typically presented with spaces as follows:</span></span>
- <span data-ttu-id="31aad-405">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-405">Three digits</span></span> 
- <span data-ttu-id="31aad-406">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-406">An optional space</span></span> 
- <span data-ttu-id="31aad-407">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-407">Three digits</span></span> 
- <span data-ttu-id="31aad-408">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-408">An optional space</span></span> 
- <span data-ttu-id="31aad-409">2–3 цифры, причем последняя цифра — контрольная</span><span class="sxs-lookup"><span data-stu-id="31aad-409">2-3 digits where the last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-410">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-410">Checksum</span></span>

<span data-ttu-id="31aad-411">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-411">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-412">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-412">Definition</span></span>

<span data-ttu-id="31aad-413">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-413">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-414">функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-414">The function Func_australian_tax_file_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-415">ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;</span><span class="sxs-lookup"><span data-stu-id="31aad-415">No keyword from Keyword_Australia_Tax_File_Number or Keyword_number_exclusions is found.</span></span>
- <span data-ttu-id="31aad-416">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-416">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-417">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-417">Keywords</span></span>

#### <a name="keyword_australia_tax_file_number"></a><span data-ttu-id="31aad-418">Keyword_Australia_Tax_File_Number</span><span class="sxs-lookup"><span data-stu-id="31aad-418">Keyword_Australia_Tax_File_Number</span></span>

- <span data-ttu-id="31aad-419">australian business number</span><span class="sxs-lookup"><span data-stu-id="31aad-419">australian business number</span></span>
- <span data-ttu-id="31aad-420">marginal tax rate</span><span class="sxs-lookup"><span data-stu-id="31aad-420">marginal tax rate</span></span>
- <span data-ttu-id="31aad-421">medicare levy</span><span class="sxs-lookup"><span data-stu-id="31aad-421">medicare levy</span></span>
- <span data-ttu-id="31aad-422">portfolio number</span><span class="sxs-lookup"><span data-stu-id="31aad-422">portfolio number</span></span>
- <span data-ttu-id="31aad-423">service veterans</span><span class="sxs-lookup"><span data-stu-id="31aad-423">service veterans</span></span>
- <span data-ttu-id="31aad-424">withholding tax</span><span class="sxs-lookup"><span data-stu-id="31aad-424">withholding tax</span></span>
- <span data-ttu-id="31aad-425">individual tax return</span><span class="sxs-lookup"><span data-stu-id="31aad-425">individual tax return</span></span>
- <span data-ttu-id="31aad-426">tax file number</span><span class="sxs-lookup"><span data-stu-id="31aad-426">tax file number</span></span>

#### <a name="keyword_number_exclusions"></a><span data-ttu-id="31aad-427">Keyword_number_exclusions</span><span class="sxs-lookup"><span data-stu-id="31aad-427">Keyword_number_exclusions</span></span>

- <span data-ttu-id="31aad-428">00000001</span><span class="sxs-lookup"><span data-stu-id="31aad-428">00000000</span></span>
- <span data-ttu-id="31aad-429">11111111</span><span class="sxs-lookup"><span data-stu-id="31aad-429">11111111</span></span>
- <span data-ttu-id="31aad-430">22222222</span><span class="sxs-lookup"><span data-stu-id="31aad-430">22222222</span></span>
- <span data-ttu-id="31aad-431">33333333</span><span class="sxs-lookup"><span data-stu-id="31aad-431">33333333</span></span>
- <span data-ttu-id="31aad-432">44444444</span><span class="sxs-lookup"><span data-stu-id="31aad-432">44444444</span></span>
- <span data-ttu-id="31aad-433">55555555</span><span class="sxs-lookup"><span data-stu-id="31aad-433">55555555</span></span>
- <span data-ttu-id="31aad-434">66666666</span><span class="sxs-lookup"><span data-stu-id="31aad-434">66666666</span></span>
- <span data-ttu-id="31aad-435">77777777</span><span class="sxs-lookup"><span data-stu-id="31aad-435">77777777</span></span>
- <span data-ttu-id="31aad-436">88888888</span><span class="sxs-lookup"><span data-stu-id="31aad-436">88888888</span></span>
- <span data-ttu-id="31aad-437">99999999</span><span class="sxs-lookup"><span data-stu-id="31aad-437">99999999</span></span>
- <span data-ttu-id="31aad-438">000000000</span><span class="sxs-lookup"><span data-stu-id="31aad-438">000000000</span></span>
- <span data-ttu-id="31aad-439">111111111</span><span class="sxs-lookup"><span data-stu-id="31aad-439">111111111</span></span>
- <span data-ttu-id="31aad-440">222222222</span><span class="sxs-lookup"><span data-stu-id="31aad-440">222222222</span></span>
- <span data-ttu-id="31aad-441">333333333</span><span class="sxs-lookup"><span data-stu-id="31aad-441">333333333</span></span>
- <span data-ttu-id="31aad-442">444444444</span><span class="sxs-lookup"><span data-stu-id="31aad-442">444444444</span></span>
- <span data-ttu-id="31aad-443">555555555</span><span class="sxs-lookup"><span data-stu-id="31aad-443">555555555</span></span>
- <span data-ttu-id="31aad-444">666666666</span><span class="sxs-lookup"><span data-stu-id="31aad-444">666666666</span></span>
- <span data-ttu-id="31aad-445">777777777</span><span class="sxs-lookup"><span data-stu-id="31aad-445">777777777</span></span>
- <span data-ttu-id="31aad-446">888888888</span><span class="sxs-lookup"><span data-stu-id="31aad-446">888888888</span></span>
- <span data-ttu-id="31aad-447">999999999</span><span class="sxs-lookup"><span data-stu-id="31aad-447">999999999</span></span>
- <span data-ttu-id="31aad-448">0000000000</span><span class="sxs-lookup"><span data-stu-id="31aad-448">0000000000</span></span>
- <span data-ttu-id="31aad-449">1111111111</span><span class="sxs-lookup"><span data-stu-id="31aad-449">1111111111</span></span>
- <span data-ttu-id="31aad-450">2222222222</span><span class="sxs-lookup"><span data-stu-id="31aad-450">2222222222</span></span>
- <span data-ttu-id="31aad-451">3333333333</span><span class="sxs-lookup"><span data-stu-id="31aad-451">3333333333</span></span>
- <span data-ttu-id="31aad-452">4444444444</span><span class="sxs-lookup"><span data-stu-id="31aad-452">4444444444</span></span>
- <span data-ttu-id="31aad-453">5555555555</span><span class="sxs-lookup"><span data-stu-id="31aad-453">5555555555</span></span>
- <span data-ttu-id="31aad-454">6666666666</span><span class="sxs-lookup"><span data-stu-id="31aad-454">6666666666</span></span>
- <span data-ttu-id="31aad-455">7777777777</span><span class="sxs-lookup"><span data-stu-id="31aad-455">7777777777</span></span>
- <span data-ttu-id="31aad-456">8888888888</span><span class="sxs-lookup"><span data-stu-id="31aad-456">8888888888</span></span>
- <span data-ttu-id="31aad-457">9999999999</span><span class="sxs-lookup"><span data-stu-id="31aad-457">9999999999</span></span>

## <a name="azure-documentdb-auth-key"></a><span data-ttu-id="31aad-458">Ключ проверки подлинности Azure DocumentDB</span><span class="sxs-lookup"><span data-stu-id="31aad-458">Azure DocumentDB Auth Key</span></span>

### <a name="format"></a><span data-ttu-id="31aad-459">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-459">Format</span></span>

<span data-ttu-id="31aad-460">Строка "DocumentDb", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="31aad-460">The string "DocumentDb" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-461">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-461">Pattern</span></span>

- <span data-ttu-id="31aad-462">Строка "DocumentDb"</span><span class="sxs-lookup"><span data-stu-id="31aad-462">The string "DocumentDb"</span></span>
- <span data-ttu-id="31aad-463">Любая комбинация из 3-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-463">Any combination of between 3-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-464">Символ "больше" (>), знак равенства (=), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="31aad-464">A greater than symbol (>), an equal sign (=), a quotation mark ("), or an apostrophe (')</span></span>
- <span data-ttu-id="31aad-465">Любая комбинация 86 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="31aad-465">Any combination of 86 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="31aad-466">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="31aad-466">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-467">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-467">Checksum</span></span>

<span data-ttu-id="31aad-468">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-468">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-469">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-469">Definition</span></span>

<span data-ttu-id="31aad-470">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-470">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-471">Регулярное выражение CEP_Regex_AzureDocumentDBAuthKey находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-471">The regular expression CEP_Regex_AzureDocumentDBAuthKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-472">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-472">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-473">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-473">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-474">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-474">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-475">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-475">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-476">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-476">contoso</span></span>
- <span data-ttu-id="31aad-477">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-477">fabrikam</span></span>
- <span data-ttu-id="31aad-478">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-478">northwind</span></span>
- <span data-ttu-id="31aad-479">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-479">sandbox</span></span>
- <span data-ttu-id="31aad-480">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-480">onebox</span></span>
- <span data-ttu-id="31aad-481">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-481">localhost</span></span>
- <span data-ttu-id="31aad-482">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-482">127.0.0.1</span></span>
- <span data-ttu-id="31aad-483">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-483">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-484">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-484">com</span></span>
- <span data-ttu-id="31aad-485">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-485">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-486">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-486">net</span></span>

## <a name="azure-iaas-database-connection-string-and-azure-sql-connection-string"></a><span data-ttu-id="31aad-487">Строка подключения к базе данных Azure IAAS и строка подключения к SQL Azure</span><span class="sxs-lookup"><span data-stu-id="31aad-487">Azure IAAS Database Connection String and Azure SQL Connection String</span></span>

### <a name="format"></a><span data-ttu-id="31aad-488">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-488">Format</span></span>

<span data-ttu-id="31aad-489">Строка "Server", "Server" или "Data Source", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "клаудапп. Azure".</span><span class="sxs-lookup"><span data-stu-id="31aad-489">The string "Server", "server", or "data source" followed by the characters and strings outlined in the pattern below, including the string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-490">com "или" клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="31aad-490">com" or "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-491">NET "или" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="31aad-491">net" or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-492">NET ", а также строку" Password "или" Password "или" pwd ".</span><span class="sxs-lookup"><span data-stu-id="31aad-492">net", and the string "Password" or "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-493">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-493">Pattern</span></span>

- <span data-ttu-id="31aad-494">Строка "Server", "Server" или "Data Source"</span><span class="sxs-lookup"><span data-stu-id="31aad-494">The string "Server", "server", or "data source"</span></span>
- <span data-ttu-id="31aad-495">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-495">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-496">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-496">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-497">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-497">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-498">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-498">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-499">Строка "клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="31aad-499">The string "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-500">com "," клаудапп. Azure.</span><span class="sxs-lookup"><span data-stu-id="31aad-500">com", "cloudapp.azure.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-501">NET "или" Database. Windows.</span><span class="sxs-lookup"><span data-stu-id="31aad-501">net", or "database.windows.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-502">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-502">net"</span></span>
- <span data-ttu-id="31aad-503">Любая комбинация из 1-300 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-503">Any combination of between 1-300 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-504">Строка "Password", "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="31aad-504">The string "Password", "password", or "pwd"</span></span>
- <span data-ttu-id="31aad-505">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-505">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-506">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-506">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-507">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-507">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-508">Один или несколько символов, не отделяющая точку с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="31aad-508">One or more characters that is not a semicolon (;), quotation mark ("), or apostrophe (')</span></span>
- <span data-ttu-id="31aad-509">Точка с запятой (;), кавычки (") или апостроф (')</span><span class="sxs-lookup"><span data-stu-id="31aad-509">A semicolon (;), quotation mark ("), or apostrophe (')</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-510">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-510">Checksum</span></span>

<span data-ttu-id="31aad-511">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-511">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-512">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-512">Definition</span></span>

<span data-ttu-id="31aad-513">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-513">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-514">Регулярное выражение CEP_Regex_AzureConnectionString находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-514">The regular expression CEP_Regex_AzureConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-515">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-515">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-516">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-516">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-517">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-517">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-518">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-518">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-519">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-519">contoso</span></span>
- <span data-ttu-id="31aad-520">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-520">fabrikam</span></span>
- <span data-ttu-id="31aad-521">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-521">northwind</span></span>
- <span data-ttu-id="31aad-522">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-522">sandbox</span></span>
- <span data-ttu-id="31aad-523">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-523">onebox</span></span>
- <span data-ttu-id="31aad-524">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-524">localhost</span></span>
- <span data-ttu-id="31aad-525">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-525">127.0.0.1</span></span>
- <span data-ttu-id="31aad-526">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-526">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-527">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-527">com</span></span>
- <span data-ttu-id="31aad-528">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-528">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-529">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-529">net</span></span>

## <a name="azure-iot-connection-string"></a><span data-ttu-id="31aad-530">Строка подключения Azure IoT</span><span class="sxs-lookup"><span data-stu-id="31aad-530">Azure IoT Connection String</span></span>

### <a name="format"></a><span data-ttu-id="31aad-531">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-531">Format</span></span>

<span data-ttu-id="31aad-532">Строка "HostName", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, включая строки "Azure — Devices.</span><span class="sxs-lookup"><span data-stu-id="31aad-532">The string "HostName" followed by the characters and strings outlined in the pattern below, including the strings "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-533">NET "и" Шаредакцесскэй ".</span><span class="sxs-lookup"><span data-stu-id="31aad-533">net" and "SharedAccessKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-534">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-534">Pattern</span></span>

- <span data-ttu-id="31aad-535">Строка "HostName"</span><span class="sxs-lookup"><span data-stu-id="31aad-535">The string "HostName"</span></span>
- <span data-ttu-id="31aad-536">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-536">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-537">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-537">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-538">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-538">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-539">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-539">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-540">Строка "Azure — Devices.</span><span class="sxs-lookup"><span data-stu-id="31aad-540">The string "azure-devices.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-541">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-541">net"</span></span>
- <span data-ttu-id="31aad-542">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-542">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-543">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="31aad-543">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="31aad-544">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-544">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-545">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-545">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-546">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-546">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-547">Любая комбинация 43 строчных или прописных букв, цифр, символов косой черты (/) или знака плюса (+).</span><span class="sxs-lookup"><span data-stu-id="31aad-547">Any combination of 43 lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="31aad-548">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-548">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-549">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-549">Checksum</span></span>

<span data-ttu-id="31aad-550">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-550">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-551">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-551">Definition</span></span>

<span data-ttu-id="31aad-552">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-552">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-553">Регулярное выражение CEP_Regex_AzureIoTConnectionString находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-553">The regular expression CEP_Regex_AzureIoTConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-554">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-554">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-555">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-555">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-556">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-556">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-557">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-557">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-558">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-558">contoso</span></span>
- <span data-ttu-id="31aad-559">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-559">fabrikam</span></span>
- <span data-ttu-id="31aad-560">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-560">northwind</span></span>
- <span data-ttu-id="31aad-561">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-561">sandbox</span></span>
- <span data-ttu-id="31aad-562">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-562">onebox</span></span>
- <span data-ttu-id="31aad-563">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-563">localhost</span></span>
- <span data-ttu-id="31aad-564">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-564">127.0.0.1</span></span>
- <span data-ttu-id="31aad-565">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-565">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-566">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-566">com</span></span>
- <span data-ttu-id="31aad-567">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-567">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-568">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-568">net</span></span>

## <a name="azure-publish-setting-password"></a><span data-ttu-id="31aad-569">Пароль для параметра публикации Azure</span><span class="sxs-lookup"><span data-stu-id="31aad-569">Azure Publish Setting Password</span></span>

### <a name="format"></a><span data-ttu-id="31aad-570">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-570">Format</span></span>

<span data-ttu-id="31aad-571">Строка "усерпвд =", за которой следует буквенно-цифровая строка.</span><span class="sxs-lookup"><span data-stu-id="31aad-571">The string "userpwd=" followed by an alphanumeric string.</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-572">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-572">Pattern</span></span>

- <span data-ttu-id="31aad-573">Строка "усерпвд ="</span><span class="sxs-lookup"><span data-stu-id="31aad-573">The string "userpwd="</span></span>
- <span data-ttu-id="31aad-574">Любая комбинация букв или цифр в нижнем регистре 60</span><span class="sxs-lookup"><span data-stu-id="31aad-574">Any combination of 60 lowercase letters or digits</span></span>
- <span data-ttu-id="31aad-575">Знак кавычек (")</span><span class="sxs-lookup"><span data-stu-id="31aad-575">A quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-576">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-576">Checksum</span></span>

<span data-ttu-id="31aad-577">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-577">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-578">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-578">Definition</span></span>

<span data-ttu-id="31aad-579">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-579">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-580">Регулярное выражение CEP_Regex_AzurePublishSettingPasswords находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-580">The regular expression CEP_Regex_AzurePublishSettingPasswords finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-581">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-581">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>


```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-582">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-582">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-583">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-583">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-584">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-584">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-585">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-585">contoso</span></span>
- <span data-ttu-id="31aad-586">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-586">fabrikam</span></span>
- <span data-ttu-id="31aad-587">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-587">northwind</span></span>
- <span data-ttu-id="31aad-588">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-588">sandbox</span></span>
- <span data-ttu-id="31aad-589">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-589">onebox</span></span>
- <span data-ttu-id="31aad-590">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-590">localhost</span></span>
- <span data-ttu-id="31aad-591">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-591">127.0.0.1</span></span>
- <span data-ttu-id="31aad-592">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-592">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-593">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-593">com</span></span>
- <span data-ttu-id="31aad-594">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-594">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-595">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-595">net</span></span>

## <a name="azure-redis-cache-connection-string"></a><span data-ttu-id="31aad-596">Строка подключения к кэшу Azure Redis</span><span class="sxs-lookup"><span data-stu-id="31aad-596">Azure Redis Cache Connection String</span></span>

### <a name="format"></a><span data-ttu-id="31aad-597">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-597">Format</span></span>

<span data-ttu-id="31aad-598">Строка "Redis. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="31aad-598">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-599">NET, за которыми следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "Password" или "pwd".</span><span class="sxs-lookup"><span data-stu-id="31aad-599">net" followed by the characters and strings outlined in the pattern below, including the string "password" or "pwd".</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-600">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-600">Pattern</span></span>

- <span data-ttu-id="31aad-601">Строка "Redis. Cache. Windows.</span><span class="sxs-lookup"><span data-stu-id="31aad-601">The string "redis.cache.windows.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-602">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-602">net"</span></span>
- <span data-ttu-id="31aad-603">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-603">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-604">Строка "Password" или "pwd"</span><span class="sxs-lookup"><span data-stu-id="31aad-604">The string "password" or "pwd"</span></span>
- <span data-ttu-id="31aad-605">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-605">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-606">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-606">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-607">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-607">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-608">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="31aad-608">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="31aad-609">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-609">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-610">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-610">Checksum</span></span>

<span data-ttu-id="31aad-611">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-611">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-612">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-612">Definition</span></span>

<span data-ttu-id="31aad-613">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-614">Регулярное выражение CEP_Regex_AzureRedisCacheConnectionString находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="31aad-614">The regular expression CEP_Regex_AzureRedisCacheConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="31aad-615">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-615">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-616">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-616">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-617">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-617">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-618">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-618">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-619">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-619">contoso</span></span>
- <span data-ttu-id="31aad-620">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-620">fabrikam</span></span>
- <span data-ttu-id="31aad-621">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-621">northwind</span></span>
- <span data-ttu-id="31aad-622">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-622">sandbox</span></span>
- <span data-ttu-id="31aad-623">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-623">onebox</span></span>
- <span data-ttu-id="31aad-624">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-624">localhost</span></span>
- <span data-ttu-id="31aad-625">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-625">127.0.0.1</span></span>
- <span data-ttu-id="31aad-626">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-626">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-627">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-627">com</span></span>
- <span data-ttu-id="31aad-628">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-628">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-629">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-629">net</span></span>

## <a name="azure-sas"></a><span data-ttu-id="31aad-630">SAS Azure</span><span class="sxs-lookup"><span data-stu-id="31aad-630">Azure SAS</span></span>

### <a name="format"></a><span data-ttu-id="31aad-631">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-631">Format</span></span>

<span data-ttu-id="31aad-632">Строка "SIG", за которой следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="31aad-632">The string "sig" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-633">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-633">Pattern</span></span>

- <span data-ttu-id="31aad-634">Строка "SIG"</span><span class="sxs-lookup"><span data-stu-id="31aad-634">The string "sig"</span></span>
- <span data-ttu-id="31aad-635">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-635">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-636">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-636">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-637">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-637">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-638">Любое сочетание 43-53 символов, которые являются буквами нижнего или верхнего регистра, цифрами или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="31aad-638">Any combination of between 43-53 characters that are lower- or uppercase letters, digits, or the percent sign (%)</span></span>
- <span data-ttu-id="31aad-639">Строка "% 3D"</span><span class="sxs-lookup"><span data-stu-id="31aad-639">The string "%3d"</span></span>
- <span data-ttu-id="31aad-640">Любой символ, который не является буквой нижнего или верхнего регистра, цифрой или знаком процента (%)</span><span class="sxs-lookup"><span data-stu-id="31aad-640">Any character that is not a lower- or uppercase letter, digit, or percent sign (%)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-641">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-641">Checksum</span></span>

<span data-ttu-id="31aad-642">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-642">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-643">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-643">Definition</span></span>

<span data-ttu-id="31aad-644">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-644">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-645">Регулярное выражение CEP_Regex_AzureSAS находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-645">The regular expression CEP_Regex_AzureSAS finds content that matches the pattern.</span></span>

```xml
<!--Azure SAS-->
<Entity id="4d235014-e564-47f4-a6fb-6ebb4a826834" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureSAS" />
  </Pattern>
</Entity>
```

## <a name="azure-service-bus-connection-string"></a><span data-ttu-id="31aad-646">Строка подключения к служебной шине Azure</span><span class="sxs-lookup"><span data-stu-id="31aad-646">Azure Service Bus Connection String</span></span>

### <a name="format"></a><span data-ttu-id="31aad-647">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-647">Format</span></span>

<span data-ttu-id="31aad-648">Строка "EndPoint", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строки "сервицебус. Windows.</span><span class="sxs-lookup"><span data-stu-id="31aad-648">The string "EndPoint" followed by the characters and strings outlined in the pattern below, including the strings "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-649">NET "и" Шаредакцескэй ".</span><span class="sxs-lookup"><span data-stu-id="31aad-649">net" and "SharedAccesKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-650">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-650">Pattern</span></span>

- <span data-ttu-id="31aad-651">Строка "EndPoint"</span><span class="sxs-lookup"><span data-stu-id="31aad-651">The string "EndPoint"</span></span>
- <span data-ttu-id="31aad-652">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-652">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-653">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-653">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-654">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-654">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-655">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-655">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-656">Строка "сервицебус. Windows.</span><span class="sxs-lookup"><span data-stu-id="31aad-656">The string "servicebus.windows.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-657">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-657">net"</span></span>
- <span data-ttu-id="31aad-658">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-658">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-659">Строка "Шаредакцесскэй"</span><span class="sxs-lookup"><span data-stu-id="31aad-659">The string "SharedAccessKey"</span></span>
- <span data-ttu-id="31aad-660">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-660">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-661">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-661">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-662">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-662">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-663">Любое сочетание 43 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="31aad-663">Any combination of 43 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="31aad-664">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-664">An equal sign (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-665">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-665">Checksum</span></span>

<span data-ttu-id="31aad-666">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-666">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-667">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-667">Definition</span></span>

<span data-ttu-id="31aad-668">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-668">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-669">Регулярное выражение CEP_Regex_AzureServiceBusConnectionString находит содержимое, которое соответствует шаблону..</span><span class="sxs-lookup"><span data-stu-id="31aad-669">The regular expression CEP_Regex_AzureServiceBusConnectionString finds content that matches the pattern..</span></span>
- <span data-ttu-id="31aad-670">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-670">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-671">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-671">Keywords</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-672">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-672">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-673">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-673">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-674">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-674">contoso</span></span>
- <span data-ttu-id="31aad-675">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-675">fabrikam</span></span>
- <span data-ttu-id="31aad-676">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-676">northwind</span></span>
- <span data-ttu-id="31aad-677">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-677">sandbox</span></span>
- <span data-ttu-id="31aad-678">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-678">onebox</span></span>
- <span data-ttu-id="31aad-679">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-679">localhost</span></span>
- <span data-ttu-id="31aad-680">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-680">127.0.0.1</span></span>
- <span data-ttu-id="31aad-681">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-681">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-682">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-682">com</span></span>
- <span data-ttu-id="31aad-683">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-683">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-684">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-684">net</span></span>

## <a name="azure-storage-account-key"></a><span data-ttu-id="31aad-685">Ключ учетной записи хранилища Azure</span><span class="sxs-lookup"><span data-stu-id="31aad-685">Azure Storage Account Key</span></span>

### <a name="format"></a><span data-ttu-id="31aad-686">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-686">Format</span></span>

<span data-ttu-id="31aad-687">Строка "Дефаултендпоинтспротокол", за которой следуют символы и строки, описанные в приведенном ниже шаблоне, в том числе строку "AccountKey".</span><span class="sxs-lookup"><span data-stu-id="31aad-687">The string "DefaultEndpointsProtocol" followed by the characters and strings outlined in the pattern below, including the string "AccountKey".</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-688">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-688">Pattern</span></span>

- <span data-ttu-id="31aad-689">Строка "Дефаултендпоинтспротокол"</span><span class="sxs-lookup"><span data-stu-id="31aad-689">The string "DefaultEndpointsProtocol"</span></span>
- <span data-ttu-id="31aad-690">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-690">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-691">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-691">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-692">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-692">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-693">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-693">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-694">Строка "AccountKey"</span><span class="sxs-lookup"><span data-stu-id="31aad-694">The string "AccountKey"</span></span>
- <span data-ttu-id="31aad-695">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-695">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-696">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-696">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-697">0-2 символов пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-697">0-2 whitespace characters</span></span>
- <span data-ttu-id="31aad-698">Любое сочетание 86 символов, которые представляют собой буквы нижнего или верхнего регистра, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="31aad-698">Any combination of 86 characters that are lower- or uppercase letters, digits, forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="31aad-699">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="31aad-699">Two equal signs (=)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-700">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-700">Checksum</span></span>

<span data-ttu-id="31aad-701">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-701">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-702">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-702">Definition</span></span>

<span data-ttu-id="31aad-703">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-703">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-704">Регулярное выражение CEP_Regex_AzureStorageAccountKey находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-704">The regular expression CEP_Regex_AzureStorageAccountKey finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-705">Регулярное выражение CEP_AzureEmulatorStorageAccountFilter не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-705">The regular expression CEP_AzureEmulatorStorageAccountFilter does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-706">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-706">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-707">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-707">Keywords</span></span>

#### <a name="cep_azureemulatorstorageaccountfilter"></a><span data-ttu-id="31aad-708">CEP_AzureEmulatorStorageAccountFilter</span><span class="sxs-lookup"><span data-stu-id="31aad-708">CEP_AzureEmulatorStorageAccountFilter</span></span>

<span data-ttu-id="31aad-709">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-709">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/Кбхбексогмгв = =</span><span class="sxs-lookup"><span data-stu-id="31aad-710">Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-711">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-711">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-712">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-712">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-713">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-713">contoso</span></span>
- <span data-ttu-id="31aad-714">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-714">fabrikam</span></span>
- <span data-ttu-id="31aad-715">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-715">northwind</span></span>
- <span data-ttu-id="31aad-716">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-716">sandbox</span></span>
- <span data-ttu-id="31aad-717">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-717">onebox</span></span>
- <span data-ttu-id="31aad-718">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-718">localhost</span></span>
- <span data-ttu-id="31aad-719">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-719">127.0.0.1</span></span>
- <span data-ttu-id="31aad-720">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-720">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-721">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-721">com</span></span>
- <span data-ttu-id="31aad-722">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-722">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-723">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-723">net</span></span>

## <a name="azure-storage-account-key-generic"></a><span data-ttu-id="31aad-724">Ключ учетной записи хранилища Azure (общий)</span><span class="sxs-lookup"><span data-stu-id="31aad-724">Azure Storage Account Key (Generic)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-725">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-725">Format</span></span>

<span data-ttu-id="31aad-726">Любая комбинация 86 строчных или прописных букв, цифр, знаков косой черты (/) или знака плюса (+) перед или за ними следуют символы, указанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="31aad-726">Any combination of 86 lower- or uppercase letters, digits, the forward slash (/), or plus sign (+), preceded or followed by the characters outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-727">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-727">Pattern</span></span>

- <span data-ttu-id="31aad-728">0-1 из символа "больше" (>), апостроф ('), знак равенства (=), знак кавычек (") или решетка (#)</span><span class="sxs-lookup"><span data-stu-id="31aad-728">0-1 of the greater than symbol (>), apostrophe ('), equal sign (=), quotation mark ("), or number sign (#)</span></span>
- <span data-ttu-id="31aad-729">Любое сочетание 86 символов, которые представляют собой буквы в нижнем или верхнем регистре, цифры, косую черту (/) или знак плюса (+).</span><span class="sxs-lookup"><span data-stu-id="31aad-729">Any combination of 86 characters that are lower- or uppercase letters, digits, the forward slash (/), or plus sign (+)</span></span>
- <span data-ttu-id="31aad-730">Два знака равенства (=)</span><span class="sxs-lookup"><span data-stu-id="31aad-730">Two equal signs (=)</span></span>


### <a name="checksum"></a><span data-ttu-id="31aad-731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-731">Checksum</span></span>

<span data-ttu-id="31aad-732">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-732">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-733">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-733">Definition</span></span>

<span data-ttu-id="31aad-734">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-735">Регулярное выражение CEP_Regex_AzureStorageAccountKeyGeneric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-735">The regular expression CEP_Regex_AzureStorageAccountKeyGeneric finds content that matches the pattern.</span></span>

```xml
<!--Azure Storage Account Key (Generic)-->
<Entity id="7ff41bd0-5419-4523-91d6-383b3a37f084" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="CEP_Regex_AzureStorageAccountKeyGeneric" />
  </Pattern>
</Entity>
```

## <a name="belgium-national-number"></a><span data-ttu-id="31aad-736">Номер национального документа для Бельгии</span><span class="sxs-lookup"><span data-stu-id="31aad-736">Belgium National Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-737">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-737">Format</span></span>

<span data-ttu-id="31aad-738">11 цифр, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="31aad-738">11 digits plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-739">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-739">Pattern</span></span>

<span data-ttu-id="31aad-740">11 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="31aad-740">11 digits plus delimiters:</span></span>
- <span data-ttu-id="31aad-741">шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения;</span><span class="sxs-lookup"><span data-stu-id="31aad-741">Six digits and two periods in the format YY.MM.DD for date of birth</span></span> 
- <span data-ttu-id="31aad-742">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-742">A hyphen</span></span> 
- <span data-ttu-id="31aad-743">три последовательные цифры (нечетные для мужчин, четные для женщин);</span><span class="sxs-lookup"><span data-stu-id="31aad-743">Three sequential digits (odd for males, even for females)</span></span> 
- <span data-ttu-id="31aad-744">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-744">A period</span></span> 
- <span data-ttu-id="31aad-745">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-745">Two digits that are a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-746">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-746">Checksum</span></span>

<span data-ttu-id="31aad-747">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-747">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-748">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-748">Definition</span></span>

<span data-ttu-id="31aad-749">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-749">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-750">функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-750">The function Func_belgium_national_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-751">находится ключевое слово из Keyword_belgium_national_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-751">A keyword from Keyword_belgium_national_number is found.</span></span>
- <span data-ttu-id="31aad-752">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-752">The checksum passes.</span></span>

```xml
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-753">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-753">Keywords</span></span>

#### <a name="keyword_belgium_national_number"></a><span data-ttu-id="31aad-754">Keyword_belgium_national_number</span><span class="sxs-lookup"><span data-stu-id="31aad-754">Keyword_belgium_national_number</span></span>

- <span data-ttu-id="31aad-755">Удостоверение</span><span class="sxs-lookup"><span data-stu-id="31aad-755">Identity</span></span>
- <span data-ttu-id="31aad-756">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="31aad-756">Registration</span></span>
- <span data-ttu-id="31aad-757">Процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-757">Identification</span></span> 
- <span data-ttu-id="31aad-758">ID</span><span class="sxs-lookup"><span data-stu-id="31aad-758">ID</span></span> 
- <span data-ttu-id="31aad-759">идентитеитскаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-759">Identiteitskaart</span></span>
- <span data-ttu-id="31aad-760">Registratie nummer</span><span class="sxs-lookup"><span data-stu-id="31aad-760">Registratie nummer</span></span> 
- <span data-ttu-id="31aad-761">Identificatie nummer</span><span class="sxs-lookup"><span data-stu-id="31aad-761">Identificatie nummer</span></span> 
- <span data-ttu-id="31aad-762">идентитеит</span><span class="sxs-lookup"><span data-stu-id="31aad-762">Identiteit</span></span>
- <span data-ttu-id="31aad-763">регистратие</span><span class="sxs-lookup"><span data-stu-id="31aad-763">Registratie</span></span>
- <span data-ttu-id="31aad-764">идентификатие</span><span class="sxs-lookup"><span data-stu-id="31aad-764">Identificatie</span></span> 
- <span data-ttu-id="31aad-765">Carte d’identité</span><span class="sxs-lookup"><span data-stu-id="31aad-765">Carte d’identité</span></span> 
- <span data-ttu-id="31aad-766">numéro d'immatriculation</span><span class="sxs-lookup"><span data-stu-id="31aad-766">numéro d'immatriculation</span></span>
- <span data-ttu-id="31aad-767">numéro d'identification</span><span class="sxs-lookup"><span data-stu-id="31aad-767">numéro d'identification</span></span>
- <span data-ttu-id="31aad-768">идентитé</span><span class="sxs-lookup"><span data-stu-id="31aad-768">identité</span></span> 
- <span data-ttu-id="31aad-769">инскриптион</span><span class="sxs-lookup"><span data-stu-id="31aad-769">inscription</span></span> 
- <span data-ttu-id="31aad-770">идентификатион</span><span class="sxs-lookup"><span data-stu-id="31aad-770">Identifikation</span></span>
- <span data-ttu-id="31aad-771">идентифизиерунг</span><span class="sxs-lookup"><span data-stu-id="31aad-771">Identifizierung</span></span>
- <span data-ttu-id="31aad-772">идентификатионснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-772">Identifikationsnummer</span></span>
- <span data-ttu-id="31aad-773">персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="31aad-773">Personalausweis</span></span>
- <span data-ttu-id="31aad-774">регистриерунг</span><span class="sxs-lookup"><span data-stu-id="31aad-774">Registrierung</span></span>
- <span data-ttu-id="31aad-775">регистратионснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-775">Registrationsnummer</span></span>

   
## <a name="brazil-cpf-number"></a><span data-ttu-id="31aad-776">Номер CPF для Бразилии</span><span class="sxs-lookup"><span data-stu-id="31aad-776">Brazil CPF Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-777">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-777">Format</span></span>

<span data-ttu-id="31aad-778">11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.</span><span class="sxs-lookup"><span data-stu-id="31aad-778">11 digits that include a check digit and can be formatted or unformatted</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-779">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-779">Pattern</span></span>

<span data-ttu-id="31aad-780">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="31aad-780">Formatted:</span></span>
- <span data-ttu-id="31aad-781">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-781">Three digits</span></span> 
- <span data-ttu-id="31aad-782">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-782">A period</span></span> 
- <span data-ttu-id="31aad-783">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-783">Three digits</span></span> 
- <span data-ttu-id="31aad-784">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-784">A period</span></span> 
- <span data-ttu-id="31aad-785">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-785">Three digits</span></span> 
- <span data-ttu-id="31aad-786">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-786">A hyphen</span></span> 
- <span data-ttu-id="31aad-787">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-787">Two digits which are check digits</span></span>

<span data-ttu-id="31aad-788">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="31aad-788">Unformatted:</span></span>
- <span data-ttu-id="31aad-789">11 цифр, где две последние цифры — проверочные.</span><span class="sxs-lookup"><span data-stu-id="31aad-789">11 digits where the last two digits are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-790">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-790">Checksum</span></span>

<span data-ttu-id="31aad-791">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-791">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-792">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-792">Definition</span></span>

<span data-ttu-id="31aad-793">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-793">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-794">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-794">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-795">находится ключевое слово из Keyword_brazil_cpf;</span><span class="sxs-lookup"><span data-stu-id="31aad-795">A keyword from Keyword_brazil_cpf is found.</span></span>
- <span data-ttu-id="31aad-796">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-796">The checksum passes.</span></span>

<span data-ttu-id="31aad-797">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-797">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-798">функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-798">The function Func_brazil_cpf finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-799">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-799">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-800">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-800">Keywords</span></span>

#### <a name="keyword_brazil_cpf"></a><span data-ttu-id="31aad-801">Keyword_brazil_cpf</span><span class="sxs-lookup"><span data-stu-id="31aad-801">Keyword_brazil_cpf</span></span>

- <span data-ttu-id="31aad-802">CPF</span><span class="sxs-lookup"><span data-stu-id="31aad-802">CPF</span></span>
- <span data-ttu-id="31aad-803">Процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-803">Identification</span></span>
- <span data-ttu-id="31aad-804">Зарегистрировал</span><span class="sxs-lookup"><span data-stu-id="31aad-804">Registration</span></span>
- <span data-ttu-id="31aad-805">Реализации</span><span class="sxs-lookup"><span data-stu-id="31aad-805">Revenue</span></span>
- <span data-ttu-id="31aad-806">Cadastro de Pessoas Físicas</span><span class="sxs-lookup"><span data-stu-id="31aad-806">Cadastro de Pessoas Físicas</span></span> 
- <span data-ttu-id="31aad-807">импосто</span><span class="sxs-lookup"><span data-stu-id="31aad-807">Imposto</span></span> 
- <span data-ttu-id="31aad-808">идентификаçãо</span><span class="sxs-lookup"><span data-stu-id="31aad-808">Identificação</span></span> 
- <span data-ttu-id="31aad-809">инскриçãо</span><span class="sxs-lookup"><span data-stu-id="31aad-809">Inscrição</span></span> 
- <span data-ttu-id="31aad-810">рецеита</span><span class="sxs-lookup"><span data-stu-id="31aad-810">Receita</span></span> 
   
## <a name="brazil-legal-entity-number-cnpj"></a><span data-ttu-id="31aad-811">Номер юридического лица для Бразилии (CNPJ)</span><span class="sxs-lookup"><span data-stu-id="31aad-811">Brazil Legal Entity Number (CNPJ)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-812">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-812">Format</span></span>

<span data-ttu-id="31aad-813">14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.</span><span class="sxs-lookup"><span data-stu-id="31aad-813">14 digits that include a registration number, branch number, and check digits, plus delimiters</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-814">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-814">Pattern</span></span>
<span data-ttu-id="31aad-815">14 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="31aad-815">14 digits, plus delimiters:</span></span>
- <span data-ttu-id="31aad-816">две цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-816">Two digits</span></span> 
- <span data-ttu-id="31aad-817">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-817">A period</span></span> 
- <span data-ttu-id="31aad-818">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-818">Three digits</span></span> 
- <span data-ttu-id="31aad-819">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-819">A period</span></span> 
- <span data-ttu-id="31aad-820">три цифры (эти первые восемь цифр — регистрационный номер);</span><span class="sxs-lookup"><span data-stu-id="31aad-820">Three digits (these first eight digits are the registration number)</span></span> 
- <span data-ttu-id="31aad-821">косая черта;</span><span class="sxs-lookup"><span data-stu-id="31aad-821">A forward slash</span></span> 
- <span data-ttu-id="31aad-822">номер отделения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-822">Four-digit branch number</span></span> 
- <span data-ttu-id="31aad-823">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-823">A hyphen</span></span> 
- <span data-ttu-id="31aad-824">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-824">Two digits which are check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-825">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-825">Checksum</span></span>

<span data-ttu-id="31aad-826">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-826">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-827">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-827">Definition</span></span>

<span data-ttu-id="31aad-828">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-828">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-829">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-829">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-830">находится ключевое слово из Keyword_brazil_cnpj;</span><span class="sxs-lookup"><span data-stu-id="31aad-830">A keyword from Keyword_brazil_cnpj is found.</span></span>
- <span data-ttu-id="31aad-831">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-831">The checksum passes.</span></span>

<span data-ttu-id="31aad-832">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-832">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-833">функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-833">The function Func_brazil_cnpj finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-834">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-834">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-835">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-835">Keywords</span></span>

#### <a name="keyword_brazil_cnpj"></a><span data-ttu-id="31aad-836">Keyword_brazil_cnpj</span><span class="sxs-lookup"><span data-stu-id="31aad-836">Keyword_brazil_cnpj</span></span>

- <span data-ttu-id="31aad-837">CNPJ</span><span class="sxs-lookup"><span data-stu-id="31aad-837">CNPJ</span></span> 
- <span data-ttu-id="31aad-838">CNPJ/MF</span><span class="sxs-lookup"><span data-stu-id="31aad-838">CNPJ/MF</span></span> 
- <span data-ttu-id="31aad-839">CNPJ – MF</span><span class="sxs-lookup"><span data-stu-id="31aad-839">CNPJ-MF</span></span> 
- <span data-ttu-id="31aad-840">National Registry of Legal Entities</span><span class="sxs-lookup"><span data-stu-id="31aad-840">National Registry of Legal Entities</span></span> 
- <span data-ttu-id="31aad-841">Taxpayers Registry</span><span class="sxs-lookup"><span data-stu-id="31aad-841">Taxpayers Registry</span></span> 
- <span data-ttu-id="31aad-842">Legal entity</span><span class="sxs-lookup"><span data-stu-id="31aad-842">Legal entity</span></span> 
- <span data-ttu-id="31aad-843">Legal entities</span><span class="sxs-lookup"><span data-stu-id="31aad-843">Legal entities</span></span> 
- <span data-ttu-id="31aad-844">Registration Status</span><span class="sxs-lookup"><span data-stu-id="31aad-844">Registration Status</span></span> 
- <span data-ttu-id="31aad-845">Бизнес</span><span class="sxs-lookup"><span data-stu-id="31aad-845">Business</span></span> 
- <span data-ttu-id="31aad-846">Company</span><span class="sxs-lookup"><span data-stu-id="31aad-846">Company</span></span>
- <span data-ttu-id="31aad-847">CNPJ</span><span class="sxs-lookup"><span data-stu-id="31aad-847">CNPJ</span></span> 
- <span data-ttu-id="31aad-848">Cadastro Nacional da Pessoa Jurídica</span><span class="sxs-lookup"><span data-stu-id="31aad-848">Cadastro Nacional da Pessoa Jurídica</span></span> 
- <span data-ttu-id="31aad-849">Cadastro Geral de Contribuintes</span><span class="sxs-lookup"><span data-stu-id="31aad-849">Cadastro Geral de Contribuintes</span></span> 
- <span data-ttu-id="31aad-850">кгк</span><span class="sxs-lookup"><span data-stu-id="31aad-850">CGC</span></span> 
- <span data-ttu-id="31aad-851">Pessoa jurídica</span><span class="sxs-lookup"><span data-stu-id="31aad-851">Pessoa jurídica</span></span> 
- <span data-ttu-id="31aad-852">Pessoas jurídicas</span><span class="sxs-lookup"><span data-stu-id="31aad-852">Pessoas jurídicas</span></span> 
- <span data-ttu-id="31aad-853">Situação cadastral</span><span class="sxs-lookup"><span data-stu-id="31aad-853">Situação cadastral</span></span> 
- <span data-ttu-id="31aad-854">инскриçãо</span><span class="sxs-lookup"><span data-stu-id="31aad-854">Inscrição</span></span> 
- <span data-ttu-id="31aad-855">емпреса</span><span class="sxs-lookup"><span data-stu-id="31aad-855">Empresa</span></span> 
   
## <a name="brazil-national-id-card-rg"></a><span data-ttu-id="31aad-856">	Номер внутреннего удостоверения личности для Бразилии (RG)</span><span class="sxs-lookup"><span data-stu-id="31aad-856">Brazil National ID Card (RG)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-857">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-857">Format</span></span>

<span data-ttu-id="31aad-858">Registro Geral (старый формат): девять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-858">Registro Geral (old format): Nine digits</span></span>

<span data-ttu-id="31aad-859">Registro de identidade (RIC) (новый формат): 11 цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-859">Registro de Identidade (RIC) (new format): 11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-860">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-860">Pattern</span></span>

<span data-ttu-id="31aad-861">Registro Geral (старый формат):</span><span class="sxs-lookup"><span data-stu-id="31aad-861">Registro Geral (old format):</span></span>
- <span data-ttu-id="31aad-862">две цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-862">Two digits</span></span> 
- <span data-ttu-id="31aad-863">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-863">A period</span></span> 
- <span data-ttu-id="31aad-864">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-864">Three digits</span></span> 
- <span data-ttu-id="31aad-865">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-865">A period</span></span> 
- <span data-ttu-id="31aad-866">три цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-866">Three digits</span></span> 
- <span data-ttu-id="31aad-867">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-867">A hyphen</span></span> 
- <span data-ttu-id="31aad-868">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-868">One digit which is a check digit</span></span>

<span data-ttu-id="31aad-869">Registro de identidade (RIC) (новый формат):</span><span class="sxs-lookup"><span data-stu-id="31aad-869">Registro de Identidade (RIC) (new format):</span></span>
- <span data-ttu-id="31aad-870">10 цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-870">10 digits</span></span> 
- <span data-ttu-id="31aad-871">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-871">A hyphen</span></span> 
- <span data-ttu-id="31aad-872">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-872">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-873">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-873">Checksum</span></span>

<span data-ttu-id="31aad-874">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-874">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-875">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-875">Definition</span></span>

<span data-ttu-id="31aad-876">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-876">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-877">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-877">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-878">находится ключевое слово из Keyword_brazil_rg;</span><span class="sxs-lookup"><span data-stu-id="31aad-878">A keyword from Keyword_brazil_rg is found.</span></span>
- <span data-ttu-id="31aad-879">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-879">The checksum passes.</span></span>

<span data-ttu-id="31aad-880">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-880">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-881">функция Func_brazil_rg находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-881">The function Func_brazil_rg finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-882">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-882">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-883">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-883">Keywords</span></span>

#### <a name="keyword_brazil_rg"></a><span data-ttu-id="31aad-884">Keyword_brazil_rg</span><span class="sxs-lookup"><span data-stu-id="31aad-884">Keyword_brazil_rg</span></span>

<span data-ttu-id="31aad-885">Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр).</span><span class="sxs-lookup"><span data-stu-id="31aad-885">Cédula de identidade identity card national id número de rregistro registro de Iidentidade registro geral RG (this keyword is case sensitive) RIC (this keyword is case sensitive)</span></span> 
   
## <a name="canada-bank-account-number"></a><span data-ttu-id="31aad-886">Номер банковского счета для Канады</span><span class="sxs-lookup"><span data-stu-id="31aad-886">Canada Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-887">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-887">Format</span></span>

<span data-ttu-id="31aad-888">Семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-888">Seven or twelve digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-889">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-889">Pattern</span></span>

<span data-ttu-id="31aad-890">Номер банковского счета для Канады — семь или двенадцать цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-890">A Canada Bank Account Number is seven or twelve digits.</span></span>

<span data-ttu-id="31aad-891">Транзитный номер банковского счета в Канаде имеет указанный ниже формат.</span><span class="sxs-lookup"><span data-stu-id="31aad-891">A Canada bank account transit number is:</span></span>
- <span data-ttu-id="31aad-892">пять цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-892">Five digits</span></span> 
- <span data-ttu-id="31aad-893">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-893">A hyphen</span></span> 
- <span data-ttu-id="31aad-894">Три цифры или</span><span class="sxs-lookup"><span data-stu-id="31aad-894">Three digits OR</span></span>
- <span data-ttu-id="31aad-895">ноль "0";</span><span class="sxs-lookup"><span data-stu-id="31aad-895">A zero "0"</span></span> 
- <span data-ttu-id="31aad-896">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-896">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-897">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-897">Checksum</span></span>

<span data-ttu-id="31aad-898">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-898">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-899">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-899">Definition</span></span>

<span data-ttu-id="31aad-900">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-900">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-901">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-901">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-902">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-902">A keyword from Keyword_canada_bank_account_number is found.</span></span>
- <span data-ttu-id="31aad-903">регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-903">The regular expression Regex_canada_bank_account_transit_number finds content that matches the pattern.</span></span>

<span data-ttu-id="31aad-904">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-904">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-905">регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-905">The regular expression Regex_canada_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-906">находится ключевое слово из Keyword_canada_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-906">A keyword from Keyword_canada_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-907">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-907">Keywords</span></span>

#### <a name="keyword_canada_bank_account_number"></a><span data-ttu-id="31aad-908">Keyword_canada_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="31aad-908">Keyword_canada_bank_account_number</span></span>

- <span data-ttu-id="31aad-909">canada savings bonds</span><span class="sxs-lookup"><span data-stu-id="31aad-909">canada savings bonds</span></span>
- <span data-ttu-id="31aad-910">canada revenue agency</span><span class="sxs-lookup"><span data-stu-id="31aad-910">canada revenue agency</span></span>
- <span data-ttu-id="31aad-911">canadian financial institution</span><span class="sxs-lookup"><span data-stu-id="31aad-911">canadian financial institution</span></span>
- <span data-ttu-id="31aad-912">direct deposit form</span><span class="sxs-lookup"><span data-stu-id="31aad-912">direct deposit form</span></span>
- <span data-ttu-id="31aad-913">canadian citizen</span><span class="sxs-lookup"><span data-stu-id="31aad-913">canadian citizen</span></span>
- <span data-ttu-id="31aad-914">legal representative</span><span class="sxs-lookup"><span data-stu-id="31aad-914">legal representative</span></span>
- <span data-ttu-id="31aad-915">notary public</span><span class="sxs-lookup"><span data-stu-id="31aad-915">notary public</span></span>
- <span data-ttu-id="31aad-916">commissioner for oaths</span><span class="sxs-lookup"><span data-stu-id="31aad-916">commissioner for oaths</span></span>
- <span data-ttu-id="31aad-917">child care benefit</span><span class="sxs-lookup"><span data-stu-id="31aad-917">child care benefit</span></span>
- <span data-ttu-id="31aad-918">universal child care</span><span class="sxs-lookup"><span data-stu-id="31aad-918">universal child care</span></span>
- <span data-ttu-id="31aad-919">canada child tax benefit</span><span class="sxs-lookup"><span data-stu-id="31aad-919">canada child tax benefit</span></span>
- <span data-ttu-id="31aad-920">income tax benefit</span><span class="sxs-lookup"><span data-stu-id="31aad-920">income tax benefit</span></span>
- <span data-ttu-id="31aad-921">harmonized sales tax</span><span class="sxs-lookup"><span data-stu-id="31aad-921">harmonized sales tax</span></span>
- <span data-ttu-id="31aad-922">social insurance number</span><span class="sxs-lookup"><span data-stu-id="31aad-922">social insurance number</span></span>
- <span data-ttu-id="31aad-923">income tax refund</span><span class="sxs-lookup"><span data-stu-id="31aad-923">income tax refund</span></span>
- <span data-ttu-id="31aad-924">child tax benefit</span><span class="sxs-lookup"><span data-stu-id="31aad-924">child tax benefit</span></span>
- <span data-ttu-id="31aad-925">territorial payments</span><span class="sxs-lookup"><span data-stu-id="31aad-925">territorial payments</span></span>
- <span data-ttu-id="31aad-926">institution number</span><span class="sxs-lookup"><span data-stu-id="31aad-926">institution number</span></span>
- <span data-ttu-id="31aad-927">deposit request</span><span class="sxs-lookup"><span data-stu-id="31aad-927">deposit request</span></span>
- <span data-ttu-id="31aad-928">banking information</span><span class="sxs-lookup"><span data-stu-id="31aad-928">banking information</span></span>
- <span data-ttu-id="31aad-929">direct deposit</span><span class="sxs-lookup"><span data-stu-id="31aad-929">direct deposit</span></span>
   
## <a name="canada-drivers-license-number"></a><span data-ttu-id="31aad-930">Номер водительского удостоверения для Канады</span><span class="sxs-lookup"><span data-stu-id="31aad-930">Canada Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-931">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-931">Format</span></span>

<span data-ttu-id="31aad-932">Зависит от провинции.</span><span class="sxs-lookup"><span data-stu-id="31aad-932">Varies by province</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-933">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-933">Pattern</span></span>

<span data-ttu-id="31aad-934">Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.</span><span class="sxs-lookup"><span data-stu-id="31aad-934">Various patterns covering Alberta, British Columbia, Manitoba, New Brunswick, Newfoundland/Labrador, Nova Scotia, Ontario, Prince Edward Island, Quebec, and Saskatchewan</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-935">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-935">Checksum</span></span>

<span data-ttu-id="31aad-936">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-936">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-937">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-937">Definition</span></span>

<span data-ttu-id="31aad-938">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-938">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-939">функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-939">The function Func_[province_name]_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-940">находится ключевое слово из Keyword_[province_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="31aad-940">A keyword from Keyword_[province_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="31aad-941">находится ключевое слово из Keyword_canada_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="31aad-941">A keyword from Keyword_canada_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-942">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-942">Keywords</span></span>

#### <a name="keyword_province_name_drivers_license_name"></a><span data-ttu-id="31aad-943">Keyword_[province_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="31aad-943">Keyword_[province_name]_drivers_license_name</span></span>

- <span data-ttu-id="31aad-944">Аббревиатура провинции, например AB.</span><span class="sxs-lookup"><span data-stu-id="31aad-944">The province abbreviation, for example AB</span></span>
- <span data-ttu-id="31aad-945">Название провинции, например Альберта.</span><span class="sxs-lookup"><span data-stu-id="31aad-945">The province name, for example Alberta</span></span>

#### <a name="keyword_canada_drivers_license"></a><span data-ttu-id="31aad-946">Keyword_canada_drivers_license</span><span class="sxs-lookup"><span data-stu-id="31aad-946">Keyword_canada_drivers_license</span></span>

- <span data-ttu-id="31aad-947">DL</span><span class="sxs-lookup"><span data-stu-id="31aad-947">DL</span></span>
- <span data-ttu-id="31aad-948">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="31aad-948">DLS</span></span>
- <span data-ttu-id="31aad-949">кдл</span><span class="sxs-lookup"><span data-stu-id="31aad-949">CDL</span></span>
- <span data-ttu-id="31aad-950">кдлс</span><span class="sxs-lookup"><span data-stu-id="31aad-950">CDLS</span></span>
- <span data-ttu-id="31aad-951">дриверлик</span><span class="sxs-lookup"><span data-stu-id="31aad-951">DriverLic</span></span>
- <span data-ttu-id="31aad-952">дриверликс</span><span class="sxs-lookup"><span data-stu-id="31aad-952">DriverLics</span></span>
- <span data-ttu-id="31aad-953">дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-953">DriverLicense</span></span>
- <span data-ttu-id="31aad-954">дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-954">DriverLicenses</span></span>
- <span data-ttu-id="31aad-955">дриверлиценце</span><span class="sxs-lookup"><span data-stu-id="31aad-955">DriverLicence</span></span>
- <span data-ttu-id="31aad-956">дриверлиценцес</span><span class="sxs-lookup"><span data-stu-id="31aad-956">DriverLicences</span></span>
- <span data-ttu-id="31aad-957">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-957">Driver Lic</span></span>
- <span data-ttu-id="31aad-958">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-958">Driver Lics</span></span>
- <span data-ttu-id="31aad-959">Driver License</span><span class="sxs-lookup"><span data-stu-id="31aad-959">Driver License</span></span>
- <span data-ttu-id="31aad-960">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-960">Driver Licenses</span></span>
- <span data-ttu-id="31aad-961">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-961">Driver Licence</span></span>
- <span data-ttu-id="31aad-962">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-962">Driver Licences</span></span>
- <span data-ttu-id="31aad-963">дриверслик</span><span class="sxs-lookup"><span data-stu-id="31aad-963">DriversLic</span></span>
- <span data-ttu-id="31aad-964">дриверсликс</span><span class="sxs-lookup"><span data-stu-id="31aad-964">DriversLics</span></span>
- <span data-ttu-id="31aad-965">дриверслиценце</span><span class="sxs-lookup"><span data-stu-id="31aad-965">DriversLicence</span></span>
- <span data-ttu-id="31aad-966">дриверслиценцес</span><span class="sxs-lookup"><span data-stu-id="31aad-966">DriversLicences</span></span>
- <span data-ttu-id="31aad-967">дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-967">DriversLicense</span></span>
- <span data-ttu-id="31aad-968">дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-968">DriversLicenses</span></span>
- <span data-ttu-id="31aad-969">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-969">Drivers Lic</span></span>
- <span data-ttu-id="31aad-970">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-970">Drivers Lics</span></span>
- <span data-ttu-id="31aad-971">Drivers License</span><span class="sxs-lookup"><span data-stu-id="31aad-971">Drivers License</span></span>
- <span data-ttu-id="31aad-972">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-972">Drivers Licenses</span></span>
- <span data-ttu-id="31aad-973">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-973">Drivers Licence</span></span>
- <span data-ttu-id="31aad-974">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-974">Drivers Licences</span></span>
- <span data-ttu-id="31aad-975">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="31aad-975">Driver'Lic</span></span>
- <span data-ttu-id="31aad-976">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="31aad-976">Driver'Lics</span></span>
- <span data-ttu-id="31aad-977">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="31aad-977">Driver'License</span></span>
- <span data-ttu-id="31aad-978">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-978">Driver'Licenses</span></span>
- <span data-ttu-id="31aad-979">Driver ' Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-979">Driver'Licence</span></span>
- <span data-ttu-id="31aad-980">Driver ' Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-980">Driver'Licences</span></span>
- <span data-ttu-id="31aad-981">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-981">Driver' Lic</span></span>
- <span data-ttu-id="31aad-982">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-982">Driver' Lics</span></span>
- <span data-ttu-id="31aad-983">Driver' License</span><span class="sxs-lookup"><span data-stu-id="31aad-983">Driver' License</span></span>
- <span data-ttu-id="31aad-984">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-984">Driver' Licenses</span></span>
- <span data-ttu-id="31aad-985">Driver' Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-985">Driver' Licence</span></span>
- <span data-ttu-id="31aad-986">Driver' Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-986">Driver' Licences</span></span>
- <span data-ttu-id="31aad-987">дривер'слик</span><span class="sxs-lookup"><span data-stu-id="31aad-987">Driver'sLic</span></span>
- <span data-ttu-id="31aad-988">дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="31aad-988">Driver'sLics</span></span>
- <span data-ttu-id="31aad-989">дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-989">Driver'sLicense</span></span>
- <span data-ttu-id="31aad-990">дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-990">Driver'sLicenses</span></span>
- <span data-ttu-id="31aad-991">дривер'слиценце</span><span class="sxs-lookup"><span data-stu-id="31aad-991">Driver'sLicence</span></span>
- <span data-ttu-id="31aad-992">дривер'слиценцес</span><span class="sxs-lookup"><span data-stu-id="31aad-992">Driver'sLicences</span></span>
- <span data-ttu-id="31aad-993">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-993">Driver's Lic</span></span>
- <span data-ttu-id="31aad-994">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-994">Driver's Lics</span></span>
- <span data-ttu-id="31aad-995">Driver's License</span><span class="sxs-lookup"><span data-stu-id="31aad-995">Driver's License</span></span>
- <span data-ttu-id="31aad-996">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-996">Driver's Licenses</span></span>
- <span data-ttu-id="31aad-997">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-997">Driver's Licence</span></span>
- <span data-ttu-id="31aad-998">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-998">Driver's Licences</span></span>
- <span data-ttu-id="31aad-999">Permis de Conduire</span><span class="sxs-lookup"><span data-stu-id="31aad-999">Permis de Conduire</span></span>
- <span data-ttu-id="31aad-1000">id</span><span class="sxs-lookup"><span data-stu-id="31aad-1000">id</span></span>
- <span data-ttu-id="31aad-1001">ids</span><span class="sxs-lookup"><span data-stu-id="31aad-1001">ids</span></span>
- <span data-ttu-id="31aad-1002">idcard number</span><span class="sxs-lookup"><span data-stu-id="31aad-1002">idcard number</span></span>
- <span data-ttu-id="31aad-1003">idcard numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-1003">idcard numbers</span></span>
- <span data-ttu-id="31aad-1004">idcard#</span><span class="sxs-lookup"><span data-stu-id="31aad-1004">idcard #</span></span>
- <span data-ttu-id="31aad-1005">idcard #s</span><span class="sxs-lookup"><span data-stu-id="31aad-1005">idcard #s</span></span>
- <span data-ttu-id="31aad-1006">idcard card</span><span class="sxs-lookup"><span data-stu-id="31aad-1006">idcard card</span></span>
- <span data-ttu-id="31aad-1007">idcard cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1007">idcard cards</span></span>
- <span data-ttu-id="31aad-1008">идкард</span><span class="sxs-lookup"><span data-stu-id="31aad-1008">idcard</span></span>
- <span data-ttu-id="31aad-1009">identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-1009">identification number</span></span>
- <span data-ttu-id="31aad-1010">identification numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-1010">identification numbers</span></span>
- <span data-ttu-id="31aad-1011">identification #</span><span class="sxs-lookup"><span data-stu-id="31aad-1011">identification #</span></span>
- <span data-ttu-id="31aad-1012">identification #s</span><span class="sxs-lookup"><span data-stu-id="31aad-1012">identification #s</span></span>
- <span data-ttu-id="31aad-1013">identification card</span><span class="sxs-lookup"><span data-stu-id="31aad-1013">identification card</span></span>
- <span data-ttu-id="31aad-1014">identification cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1014">identification cards</span></span>
- <span data-ttu-id="31aad-1015">процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-1015">identification</span></span> 
- <span data-ttu-id="31aad-1016">DL #</span><span class="sxs-lookup"><span data-stu-id="31aad-1016">DL#</span></span>
- <span data-ttu-id="31aad-1017">БИБЛИОТЕК #</span><span class="sxs-lookup"><span data-stu-id="31aad-1017">DLS#</span></span> 
- <span data-ttu-id="31aad-1018">кдл #</span><span class="sxs-lookup"><span data-stu-id="31aad-1018">CDL#</span></span> 
- <span data-ttu-id="31aad-1019">кдлс #</span><span class="sxs-lookup"><span data-stu-id="31aad-1019">CDLS#</span></span> 
- <span data-ttu-id="31aad-1020">дриверлик #</span><span class="sxs-lookup"><span data-stu-id="31aad-1020">DriverLic#</span></span> 
- <span data-ttu-id="31aad-1021">дриверликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-1021">DriverLics#</span></span> 
- <span data-ttu-id="31aad-1022">дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-1022">DriverLicense#</span></span> 
- <span data-ttu-id="31aad-1023">дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-1023">DriverLicenses#</span></span> 
- <span data-ttu-id="31aad-1024">дриверлиценце #</span><span class="sxs-lookup"><span data-stu-id="31aad-1024">DriverLicence#</span></span> 
- <span data-ttu-id="31aad-1025">дриверлиценцес #</span><span class="sxs-lookup"><span data-stu-id="31aad-1025">DriverLicences#</span></span> 
- <span data-ttu-id="31aad-1026">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-1026">Driver Lic#</span></span>
- <span data-ttu-id="31aad-1027">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-1027">Driver Lics#</span></span> 
- <span data-ttu-id="31aad-1028">Driver License#</span><span class="sxs-lookup"><span data-stu-id="31aad-1028">Driver License#</span></span> 
- <span data-ttu-id="31aad-1029">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-1029">Driver Licenses#</span></span> 
- <span data-ttu-id="31aad-1030">Driver License#</span><span class="sxs-lookup"><span data-stu-id="31aad-1030">Driver License#</span></span> 
- <span data-ttu-id="31aad-1031">Driver Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-1031">Driver Licences#</span></span> 
- <span data-ttu-id="31aad-1032">дриверслик #</span><span class="sxs-lookup"><span data-stu-id="31aad-1032">DriversLic#</span></span> 
- <span data-ttu-id="31aad-1033">дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-1033">DriversLics#</span></span> 
- <span data-ttu-id="31aad-1034">дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-1034">DriversLicense#</span></span> 
- <span data-ttu-id="31aad-1035">дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-1035">DriversLicenses#</span></span> 
- <span data-ttu-id="31aad-1036">дриверслиценце #</span><span class="sxs-lookup"><span data-stu-id="31aad-1036">DriversLicence#</span></span> 
- <span data-ttu-id="31aad-1037">дриверслиценцес #</span><span class="sxs-lookup"><span data-stu-id="31aad-1037">DriversLicences#</span></span> 
- <span data-ttu-id="31aad-1038">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-1038">Drivers Lic#</span></span> 
- <span data-ttu-id="31aad-1039">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-1039">Drivers Lics#</span></span> 
- <span data-ttu-id="31aad-1040">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="31aad-1040">Drivers License#</span></span> 
- <span data-ttu-id="31aad-1041">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-1041">Drivers Licenses#</span></span> 
- <span data-ttu-id="31aad-1042">Drivers Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-1042">Drivers Licence#</span></span> 
- <span data-ttu-id="31aad-1043">Drivers Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-1043">Drivers Licences#</span></span> 
- <span data-ttu-id="31aad-1044">Driver ' LIC #</span><span class="sxs-lookup"><span data-stu-id="31aad-1044">Driver'Lic#</span></span> 
- <span data-ttu-id="31aad-1045">Driver ' LICS #</span><span class="sxs-lookup"><span data-stu-id="31aad-1045">Driver'Lics#</span></span> 
- <span data-ttu-id="31aad-1046">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="31aad-1046">Driver'License#</span></span> 
- <span data-ttu-id="31aad-1047">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="31aad-1047">Driver'Licenses#</span></span> 
- <span data-ttu-id="31aad-1048">Driver ' Licence #</span><span class="sxs-lookup"><span data-stu-id="31aad-1048">Driver'Licence#</span></span> 
- <span data-ttu-id="31aad-1049">Driver ' Licences #</span><span class="sxs-lookup"><span data-stu-id="31aad-1049">Driver'Licences#</span></span> 
- <span data-ttu-id="31aad-1050">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-1050">Driver' Lic#</span></span> 
- <span data-ttu-id="31aad-1051">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-1051">Driver' Lics#</span></span> 
- <span data-ttu-id="31aad-1052">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="31aad-1052">Driver' License#</span></span> 
- <span data-ttu-id="31aad-1053">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-1053">Driver' Licenses#</span></span> 
- <span data-ttu-id="31aad-1054">Driver' Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-1054">Driver' Licence#</span></span> 
- <span data-ttu-id="31aad-1055">Driver' Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-1055">Driver' Licences#</span></span> 
- <span data-ttu-id="31aad-1056">дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="31aad-1056">Driver'sLic#</span></span> 
- <span data-ttu-id="31aad-1057">дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-1057">Driver'sLics#</span></span> 
- <span data-ttu-id="31aad-1058">дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-1058">Driver'sLicense#</span></span> 
- <span data-ttu-id="31aad-1059">дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-1059">Driver'sLicenses#</span></span> 
- <span data-ttu-id="31aad-1060">дривер'слиценце #</span><span class="sxs-lookup"><span data-stu-id="31aad-1060">Driver'sLicence#</span></span> 
- <span data-ttu-id="31aad-1061">дривер'слиценцес #</span><span class="sxs-lookup"><span data-stu-id="31aad-1061">Driver'sLicences#</span></span> 
- <span data-ttu-id="31aad-1062">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-1062">Driver's Lic#</span></span> 
- <span data-ttu-id="31aad-1063">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-1063">Driver's Lics#</span></span> 
- <span data-ttu-id="31aad-1064">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="31aad-1064">Driver's License#</span></span> 
- <span data-ttu-id="31aad-1065">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-1065">Driver's Licenses#</span></span> 
- <span data-ttu-id="31aad-1066">Driver's Licence#</span><span class="sxs-lookup"><span data-stu-id="31aad-1066">Driver's Licence#</span></span> 
- <span data-ttu-id="31aad-1067">Driver's Licences#</span><span class="sxs-lookup"><span data-stu-id="31aad-1067">Driver's Licences#</span></span> 
- <span data-ttu-id="31aad-1068">Permis de Conduire#</span><span class="sxs-lookup"><span data-stu-id="31aad-1068">Permis de Conduire#</span></span> 
- <span data-ttu-id="31aad-1069">кодов #</span><span class="sxs-lookup"><span data-stu-id="31aad-1069">id#</span></span> 
- <span data-ttu-id="31aad-1070">идентификаторы #</span><span class="sxs-lookup"><span data-stu-id="31aad-1070">ids#</span></span> 
- <span data-ttu-id="31aad-1071">idcard card#</span><span class="sxs-lookup"><span data-stu-id="31aad-1071">idcard card#</span></span> 
- <span data-ttu-id="31aad-1072">idcard cards#</span><span class="sxs-lookup"><span data-stu-id="31aad-1072">idcard cards#</span></span> 
- <span data-ttu-id="31aad-1073">идкард #</span><span class="sxs-lookup"><span data-stu-id="31aad-1073">idcard#</span></span> 
- <span data-ttu-id="31aad-1074">identification card#</span><span class="sxs-lookup"><span data-stu-id="31aad-1074">identification card#</span></span> 
- <span data-ttu-id="31aad-1075">identification cards#</span><span class="sxs-lookup"><span data-stu-id="31aad-1075">identification cards#</span></span> 
- <span data-ttu-id="31aad-1076">процедура #</span><span class="sxs-lookup"><span data-stu-id="31aad-1076">identification#</span></span> 
   
## <a name="canada-health-service-number"></a><span data-ttu-id="31aad-1077">Номер службы здравоохранения для Канады</span><span class="sxs-lookup"><span data-stu-id="31aad-1077">Canada Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1078">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1078">Format</span></span>

<span data-ttu-id="31aad-1079">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1079">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1080">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1080">Pattern</span></span>

<span data-ttu-id="31aad-1081">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1081">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1082">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1082">Checksum</span></span>

<span data-ttu-id="31aad-1083">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-1083">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1084">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1084">Definition</span></span>

<span data-ttu-id="31aad-1085">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1085">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1086">регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1086">The regular expression Regex_canada_health_service_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1087">находится ключевое слово из Keyword_canada_health_service_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-1087">A keyword from Keyword_canada_health_service_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1088">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1088">Keywords</span></span>

#### <a name="keyword_canada_health_service_number"></a><span data-ttu-id="31aad-1089">Keyword_canada_health_service_number</span><span class="sxs-lookup"><span data-stu-id="31aad-1089">Keyword_canada_health_service_number</span></span>

- <span data-ttu-id="31aad-1090">personal health number</span><span class="sxs-lookup"><span data-stu-id="31aad-1090">personal health number</span></span>
- <span data-ttu-id="31aad-1091">patient information</span><span class="sxs-lookup"><span data-stu-id="31aad-1091">patient information</span></span>
- <span data-ttu-id="31aad-1092">health services</span><span class="sxs-lookup"><span data-stu-id="31aad-1092">health services</span></span>
- <span data-ttu-id="31aad-1093">speciality services</span><span class="sxs-lookup"><span data-stu-id="31aad-1093">speciality services</span></span>
- <span data-ttu-id="31aad-1094">automobile accident</span><span class="sxs-lookup"><span data-stu-id="31aad-1094">automobile accident</span></span>
- <span data-ttu-id="31aad-1095">patient hospital</span><span class="sxs-lookup"><span data-stu-id="31aad-1095">patient hospital</span></span>
- <span data-ttu-id="31aad-1096">псичиатрист</span><span class="sxs-lookup"><span data-stu-id="31aad-1096">psychiatrist</span></span>
- <span data-ttu-id="31aad-1097">workers compensation</span><span class="sxs-lookup"><span data-stu-id="31aad-1097">workers compensation</span></span>
- <span data-ttu-id="31aad-1098">ограничен</span><span class="sxs-lookup"><span data-stu-id="31aad-1098">disability</span></span>
      
## <a name="canada-passport-number"></a><span data-ttu-id="31aad-1099">Номер паспорта гражданина Канады</span><span class="sxs-lookup"><span data-stu-id="31aad-1099">Canada Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1100">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1100">Format</span></span>

<span data-ttu-id="31aad-1101">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1101">Two uppercase letters followed by six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1102">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1102">Pattern</span></span>

<span data-ttu-id="31aad-1103">Две прописные буквы, за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1103">Two uppercase letters followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1104">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1104">Checksum</span></span>

<span data-ttu-id="31aad-1105">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-1105">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1106">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1106">Definition</span></span>

<span data-ttu-id="31aad-1107">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1107">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1108">регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1108">The regular expression Regex_canada_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1109">Найдено ключевое слово из Keyword_canada_passport_number или Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="31aad-1109">A keyword from Keyword_canada_passport_number or Keyword_passport is found.</span></span>

```xml 
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

### <a name="keywords"></a><span data-ttu-id="31aad-1110">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1110">Keywords</span></span>

#### <a name="keyword_canada_passport_number"></a><span data-ttu-id="31aad-1111">Keyword_canada_passport_number</span><span class="sxs-lookup"><span data-stu-id="31aad-1111">Keyword_canada_passport_number</span></span>

- <span data-ttu-id="31aad-1112">canadian citizenship</span><span class="sxs-lookup"><span data-stu-id="31aad-1112">canadian citizenship</span></span>
- <span data-ttu-id="31aad-1113">canadian passport</span><span class="sxs-lookup"><span data-stu-id="31aad-1113">canadian passport</span></span>
- <span data-ttu-id="31aad-1114">passport application</span><span class="sxs-lookup"><span data-stu-id="31aad-1114">passport application</span></span>
- <span data-ttu-id="31aad-1115">passport photos</span><span class="sxs-lookup"><span data-stu-id="31aad-1115">passport photos</span></span>
- <span data-ttu-id="31aad-1116">certified translator</span><span class="sxs-lookup"><span data-stu-id="31aad-1116">certified translator</span></span>
- <span data-ttu-id="31aad-1117">canadian citizens</span><span class="sxs-lookup"><span data-stu-id="31aad-1117">canadian citizens</span></span>
- <span data-ttu-id="31aad-1118">processing times</span><span class="sxs-lookup"><span data-stu-id="31aad-1118">processing times</span></span>
- <span data-ttu-id="31aad-1119">renewal application</span><span class="sxs-lookup"><span data-stu-id="31aad-1119">renewal application</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="31aad-1120">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-1120">Keyword_passport</span></span>

- <span data-ttu-id="31aad-1121">Passport Number</span><span class="sxs-lookup"><span data-stu-id="31aad-1121">Passport Number</span></span>
- <span data-ttu-id="31aad-1122">Passport No</span><span class="sxs-lookup"><span data-stu-id="31aad-1122">Passport No</span></span>
- <span data-ttu-id="31aad-1123">Passport#</span><span class="sxs-lookup"><span data-stu-id="31aad-1123">Passport #</span></span>
- <span data-ttu-id="31aad-1124">Службу #</span><span class="sxs-lookup"><span data-stu-id="31aad-1124">Passport#</span></span>
- <span data-ttu-id="31aad-1125">пасспортид</span><span class="sxs-lookup"><span data-stu-id="31aad-1125">PassportID</span></span>
- <span data-ttu-id="31aad-1126">пасспортно</span><span class="sxs-lookup"><span data-stu-id="31aad-1126">Passportno</span></span>
- <span data-ttu-id="31aad-1127">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-1127">passportnumber</span></span>
- <span data-ttu-id="31aad-1128">パスポート</span><span class="sxs-lookup"><span data-stu-id="31aad-1128">パスポート</span></span>
- <span data-ttu-id="31aad-1129">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="31aad-1129">パスポート番号</span></span>
- <span data-ttu-id="31aad-1130">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="31aad-1130">パスポートのNum</span></span>
- <span data-ttu-id="31aad-1131">パスポート #</span><span class="sxs-lookup"><span data-stu-id="31aad-1131">パスポート＃</span></span>
- <span data-ttu-id="31aad-1132">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="31aad-1132">Numéro de passeport</span></span>
- <span data-ttu-id="31aad-1133">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="31aad-1133">Passeport n °</span></span>
- <span data-ttu-id="31aad-1134">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="31aad-1134">Passeport Non</span></span>
- <span data-ttu-id="31aad-1135">Passeport#</span><span class="sxs-lookup"><span data-stu-id="31aad-1135">Passeport #</span></span>
- <span data-ttu-id="31aad-1136">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="31aad-1136">Passeport#</span></span>
- <span data-ttu-id="31aad-1137">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="31aad-1137">PasseportNon</span></span>
- <span data-ttu-id="31aad-1138">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="31aad-1138">Passeportn °</span></span>
   
## <a name="canada-personal-health-identification-number-phin"></a><span data-ttu-id="31aad-1139">Персональный идентификационный номер службы здравоохранения для Канады (PHIN)</span><span class="sxs-lookup"><span data-stu-id="31aad-1139">Canada Personal Health Identification Number (PHIN)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1140">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1140">Format</span></span>

<span data-ttu-id="31aad-1141">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1141">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1142">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1142">Pattern</span></span>

<span data-ttu-id="31aad-1143">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1143">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1144">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1144">Checksum</span></span>

<span data-ttu-id="31aad-1145">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-1145">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1146">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1146">Definition</span></span>

<span data-ttu-id="31aad-1147">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Regex_canada_phin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-1147">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_canada_phin finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-1148">Найдены по крайней мере два ключевых слова от Keyword_canada_phin или Keyword_canada_provinces.</span><span class="sxs-lookup"><span data-stu-id="31aad-1148">At least two keywords from Keyword_canada_phin or Keyword_canada_provinces are found..</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1149">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1149">Keywords</span></span>

#### <a name="keyword_canada_phin"></a><span data-ttu-id="31aad-1150">Keyword_canada_phin</span><span class="sxs-lookup"><span data-stu-id="31aad-1150">Keyword_canada_phin</span></span>

- <span data-ttu-id="31aad-1151">social insurance number</span><span class="sxs-lookup"><span data-stu-id="31aad-1151">social insurance number</span></span>
- <span data-ttu-id="31aad-1152">health information act</span><span class="sxs-lookup"><span data-stu-id="31aad-1152">health information act</span></span>
- <span data-ttu-id="31aad-1153">income tax information</span><span class="sxs-lookup"><span data-stu-id="31aad-1153">income tax information</span></span>
- <span data-ttu-id="31aad-1154">manitoba health</span><span class="sxs-lookup"><span data-stu-id="31aad-1154">manitoba health</span></span>
- <span data-ttu-id="31aad-1155">health registration</span><span class="sxs-lookup"><span data-stu-id="31aad-1155">health registration</span></span>
- <span data-ttu-id="31aad-1156">prescription purchases</span><span class="sxs-lookup"><span data-stu-id="31aad-1156">prescription purchases</span></span>
- <span data-ttu-id="31aad-1157">benefit eligibility</span><span class="sxs-lookup"><span data-stu-id="31aad-1157">benefit eligibility</span></span>
- <span data-ttu-id="31aad-1158">personal health</span><span class="sxs-lookup"><span data-stu-id="31aad-1158">personal health</span></span>
- <span data-ttu-id="31aad-1159">power of attorney</span><span class="sxs-lookup"><span data-stu-id="31aad-1159">power of attorney</span></span>
- <span data-ttu-id="31aad-1160">registration number</span><span class="sxs-lookup"><span data-stu-id="31aad-1160">registration number</span></span>
- <span data-ttu-id="31aad-1161">personal health number</span><span class="sxs-lookup"><span data-stu-id="31aad-1161">personal health number</span></span>
- <span data-ttu-id="31aad-1162">practitioner referral</span><span class="sxs-lookup"><span data-stu-id="31aad-1162">practitioner referral</span></span>
- <span data-ttu-id="31aad-1163">wellness professional</span><span class="sxs-lookup"><span data-stu-id="31aad-1163">wellness professional</span></span>
- <span data-ttu-id="31aad-1164">patient referral</span><span class="sxs-lookup"><span data-stu-id="31aad-1164">patient referral</span></span>
- <span data-ttu-id="31aad-1165">health and wellness</span><span class="sxs-lookup"><span data-stu-id="31aad-1165">health and wellness</span></span>

#### <a name="keyword_canada_provinces"></a><span data-ttu-id="31aad-1166">Keyword_canada_provinces</span><span class="sxs-lookup"><span data-stu-id="31aad-1166">Keyword_canada_provinces</span></span>

- <span data-ttu-id="31aad-1167">нунавут</span><span class="sxs-lookup"><span data-stu-id="31aad-1167">Nunavut</span></span>
- <span data-ttu-id="31aad-1168">Квебека</span><span class="sxs-lookup"><span data-stu-id="31aad-1168">Quebec</span></span>
- <span data-ttu-id="31aad-1169">Northwest Territories</span><span class="sxs-lookup"><span data-stu-id="31aad-1169">Northwest Territories</span></span>
- <span data-ttu-id="31aad-1170">Онтарио</span><span class="sxs-lookup"><span data-stu-id="31aad-1170">Ontario</span></span>
- <span data-ttu-id="31aad-1171">British Columbia</span><span class="sxs-lookup"><span data-stu-id="31aad-1171">British Columbia</span></span>
- <span data-ttu-id="31aad-1172">Альберта</span><span class="sxs-lookup"><span data-stu-id="31aad-1172">Alberta</span></span>
- <span data-ttu-id="31aad-1173">Саскачеван</span><span class="sxs-lookup"><span data-stu-id="31aad-1173">Saskatchewan</span></span>
- <span data-ttu-id="31aad-1174">Манитоба</span><span class="sxs-lookup"><span data-stu-id="31aad-1174">Manitoba</span></span>
- <span data-ttu-id="31aad-1175">Yukon</span><span class="sxs-lookup"><span data-stu-id="31aad-1175">Yukon</span></span>
- <span data-ttu-id="31aad-1176">Newfoundland and Labrador</span><span class="sxs-lookup"><span data-stu-id="31aad-1176">Newfoundland and Labrador</span></span>
- <span data-ttu-id="31aad-1177">New Brunswick</span><span class="sxs-lookup"><span data-stu-id="31aad-1177">New Brunswick</span></span>
- <span data-ttu-id="31aad-1178">Nova Scotia</span><span class="sxs-lookup"><span data-stu-id="31aad-1178">Nova Scotia</span></span>
- <span data-ttu-id="31aad-1179">Prince Edward Island</span><span class="sxs-lookup"><span data-stu-id="31aad-1179">Prince Edward Island</span></span>
- <span data-ttu-id="31aad-1180">Канада</span><span class="sxs-lookup"><span data-stu-id="31aad-1180">Canada</span></span>
   
## <a name="canada-social-insurance-number"></a><span data-ttu-id="31aad-1181">Номер карты социального страхования для Канады</span><span class="sxs-lookup"><span data-stu-id="31aad-1181">Canada Social Insurance Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1182">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1182">Format</span></span>

<span data-ttu-id="31aad-1183">Девять цифр с необязательными дефисами или пробелами.</span><span class="sxs-lookup"><span data-stu-id="31aad-1183">Nine digits with optional hyphens or spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1184">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1184">Pattern</span></span>

<span data-ttu-id="31aad-1185">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="31aad-1185">Formatted:</span></span>
- <span data-ttu-id="31aad-1186">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-1186">Three digits</span></span> 
- <span data-ttu-id="31aad-1187">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-1187">A hyphen or space</span></span> 
- <span data-ttu-id="31aad-1188">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-1188">Three digits</span></span> 
- <span data-ttu-id="31aad-1189">Дефис или пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-1189">A hyphen or space</span></span> 
- <span data-ttu-id="31aad-1190">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-1190">Three digits</span></span>

<span data-ttu-id="31aad-1191">Неформатированные: девять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-1191">Unformatted: Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1192">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1192">Checksum</span></span>

<span data-ttu-id="31aad-1193">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1193">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1194">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1194">Definition</span></span>

<span data-ttu-id="31aad-1195">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1195">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1196">Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-1196">The function Func_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1197">Выполняются по меньшей мере два из таких условий:</span><span class="sxs-lookup"><span data-stu-id="31aad-1197">At least two of any combination of the following:</span></span>
    - <span data-ttu-id="31aad-1198">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="31aad-1198">A keyword from Keyword_sin is found.</span></span>
    - <span data-ttu-id="31aad-1199">найдено ключевое слово из Keyword_sin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="31aad-1199">A keyword from Keyword_sin_collaborative is found.</span></span>
    - <span data-ttu-id="31aad-1200">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-1200">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-1201">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1201">The checksum passes.</span></span>

<span data-ttu-id="31aad-1202">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1202">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1203">функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1203">The function Func_unformatted_canadian_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1204">найдено ключевое слово из Keyword_sin;</span><span class="sxs-lookup"><span data-stu-id="31aad-1204">A keyword from Keyword_sin is found.</span></span>
- <span data-ttu-id="31aad-1205">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1205">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1206">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1206">Keywords</span></span>

#### <a name="keyword_sin"></a><span data-ttu-id="31aad-1207">Keyword_sin</span><span class="sxs-lookup"><span data-stu-id="31aad-1207">Keyword_sin</span></span>

- <span data-ttu-id="31aad-1208">sin</span><span class="sxs-lookup"><span data-stu-id="31aad-1208">sin</span></span> 
- <span data-ttu-id="31aad-1209">social insurance</span><span class="sxs-lookup"><span data-stu-id="31aad-1209">social insurance</span></span> 
- <span data-ttu-id="31aad-1210">numero d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="31aad-1210">numero d'assurance sociale</span></span> 
- <span data-ttu-id="31aad-1211">грехов</span><span class="sxs-lookup"><span data-stu-id="31aad-1211">sins</span></span> 
- <span data-ttu-id="31aad-1212">SSN</span><span class="sxs-lookup"><span data-stu-id="31aad-1212">ssn</span></span> 
- <span data-ttu-id="31aad-1213">ssNS</span><span class="sxs-lookup"><span data-stu-id="31aad-1213">ssns</span></span> 
- <span data-ttu-id="31aad-1214">social security</span><span class="sxs-lookup"><span data-stu-id="31aad-1214">social security</span></span> 
- <span data-ttu-id="31aad-1215">numero d'assurance social</span><span class="sxs-lookup"><span data-stu-id="31aad-1215">numero d'assurance social</span></span> 
- <span data-ttu-id="31aad-1216">national identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-1216">national identification number</span></span> 
- <span data-ttu-id="31aad-1217">national id</span><span class="sxs-lookup"><span data-stu-id="31aad-1217">national id</span></span> 
- <span data-ttu-id="31aad-1218">Синус #</span><span class="sxs-lookup"><span data-stu-id="31aad-1218">sin#</span></span> 
- <span data-ttu-id="31aad-1219">soc ins</span><span class="sxs-lookup"><span data-stu-id="31aad-1219">soc ins</span></span> 
- <span data-ttu-id="31aad-1220">social ins</span><span class="sxs-lookup"><span data-stu-id="31aad-1220">social ins</span></span> 

#### <a name="keyword_sin_collaborative"></a><span data-ttu-id="31aad-1221">Keyword_sin_collaborative</span><span class="sxs-lookup"><span data-stu-id="31aad-1221">Keyword_sin_collaborative</span></span>

- <span data-ttu-id="31aad-1222">driver's license</span><span class="sxs-lookup"><span data-stu-id="31aad-1222">driver's license</span></span> 
- <span data-ttu-id="31aad-1223">drivers license</span><span class="sxs-lookup"><span data-stu-id="31aad-1223">drivers license</span></span> 
- <span data-ttu-id="31aad-1224">driver's licence</span><span class="sxs-lookup"><span data-stu-id="31aad-1224">driver's licence</span></span> 
- <span data-ttu-id="31aad-1225">drivers licence</span><span class="sxs-lookup"><span data-stu-id="31aad-1225">drivers licence</span></span> 
- <span data-ttu-id="31aad-1226">доб</span><span class="sxs-lookup"><span data-stu-id="31aad-1226">DOB</span></span> 
- <span data-ttu-id="31aad-1227">Birthdate</span><span class="sxs-lookup"><span data-stu-id="31aad-1227">Birthdate</span></span> 
- <span data-ttu-id="31aad-1228">День рождения </span><span class="sxs-lookup"><span data-stu-id="31aad-1228">Birthday</span></span> 
- <span data-ttu-id="31aad-1229">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="31aad-1229">Date of Birth</span></span> 
   
## <a name="chile-identity-card-number"></a><span data-ttu-id="31aad-1230">	Номер удостоверения личности для Чили</span><span class="sxs-lookup"><span data-stu-id="31aad-1230">Chile Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1231">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1231">Format</span></span>

<span data-ttu-id="31aad-1232">7-8 цифр и разделители — контрольная цифра или буква</span><span class="sxs-lookup"><span data-stu-id="31aad-1232">7-8 digits plus delimiters a check digit or letter</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1233">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1233">Pattern</span></span>

<span data-ttu-id="31aad-1234">7–8 цифр, а также разделители:</span><span class="sxs-lookup"><span data-stu-id="31aad-1234">7-8 digits plus delimiters:</span></span>
- <span data-ttu-id="31aad-1235">1 или 2 цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-1235">1-2 digits</span></span> 
- <span data-ttu-id="31aad-1236">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-1236">A period</span></span> 
- <span data-ttu-id="31aad-1237">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-1237">Three digits</span></span> 
- <span data-ttu-id="31aad-1238">точка;</span><span class="sxs-lookup"><span data-stu-id="31aad-1238">A period</span></span> 
- <span data-ttu-id="31aad-1239">три цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-1239">Three digits</span></span> 
- <span data-ttu-id="31aad-1240">тире;</span><span class="sxs-lookup"><span data-stu-id="31aad-1240">A dash</span></span> 
- <span data-ttu-id="31aad-1241">одна цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-1241">One digit or letter (not case sensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1242">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1242">Checksum</span></span>

<span data-ttu-id="31aad-1243">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1243">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1244">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1244">Definition</span></span>

<span data-ttu-id="31aad-1245">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1245">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1246">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1246">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1247">находится ключевое слово из Keyword_chile_id_card;</span><span class="sxs-lookup"><span data-stu-id="31aad-1247">A keyword from Keyword_chile_id_card is found.</span></span>
- <span data-ttu-id="31aad-1248">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1248">The checksum passes.</span></span>

<span data-ttu-id="31aad-1249">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1250">функция Func_chile_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1250">The function Func_chile_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1251">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1251">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1252">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1252">Keywords</span></span>

#### <a name="keyword_chile_id_card"></a><span data-ttu-id="31aad-1253">Keyword_chile_id_card</span><span class="sxs-lookup"><span data-stu-id="31aad-1253">Keyword_chile_id_card</span></span>

- <span data-ttu-id="31aad-1254">National Identification Number</span><span class="sxs-lookup"><span data-stu-id="31aad-1254">National Identification Number</span></span> 
- <span data-ttu-id="31aad-1255">Identity card</span><span class="sxs-lookup"><span data-stu-id="31aad-1255">Identity card</span></span> 
- <span data-ttu-id="31aad-1256">ID</span><span class="sxs-lookup"><span data-stu-id="31aad-1256">ID</span></span> 
- <span data-ttu-id="31aad-1257">Процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-1257">Identification</span></span> 
- <span data-ttu-id="31aad-1258">Rol Único Nacional</span><span class="sxs-lookup"><span data-stu-id="31aad-1258">Rol Único Nacional</span></span> 
- <span data-ttu-id="31aad-1259">ВЫПОЛНЯЕМ</span><span class="sxs-lookup"><span data-stu-id="31aad-1259">RUN</span></span> 
- <span data-ttu-id="31aad-1260">Rol Único Tributario</span><span class="sxs-lookup"><span data-stu-id="31aad-1260">Rol Único Tributario</span></span> 
- <span data-ttu-id="31aad-1261">СНИЖАТЬСЯ</span><span class="sxs-lookup"><span data-stu-id="31aad-1261">RUT</span></span> 
- <span data-ttu-id="31aad-1262">Cédula de Identidad</span><span class="sxs-lookup"><span data-stu-id="31aad-1262">Cédula de Identidad</span></span> 
- <span data-ttu-id="31aad-1263">Número De Identificación Nacional</span><span class="sxs-lookup"><span data-stu-id="31aad-1263">Número De Identificación Nacional</span></span> 
- <span data-ttu-id="31aad-1264">Tarjeta de identificación</span><span class="sxs-lookup"><span data-stu-id="31aad-1264">Tarjeta de identificación</span></span> 
- <span data-ttu-id="31aad-1265">идентификаЦиóн</span><span class="sxs-lookup"><span data-stu-id="31aad-1265">Identificación</span></span> 
   
## <a name="china-resident-identity-card-prc-number"></a><span data-ttu-id="31aad-1266">	Номер удостоверения личности жителя Китая (КНР)</span><span class="sxs-lookup"><span data-stu-id="31aad-1266">China Resident Identity Card (PRC) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1267">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1267">Format</span></span>

<span data-ttu-id="31aad-1268">18 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1268">18 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1269">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1269">Pattern</span></span>

<span data-ttu-id="31aad-1270">18 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-1270">18 digits:</span></span>
- <span data-ttu-id="31aad-1271">шесть цифр — код адреса;</span><span class="sxs-lookup"><span data-stu-id="31aad-1271">Six digits which are an address code</span></span> 
- <span data-ttu-id="31aad-1272">восемь цифр в виде ГГГГММДД — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="31aad-1272">Eight digits in the form YYYYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="31aad-1273">три цифры — серия карты;</span><span class="sxs-lookup"><span data-stu-id="31aad-1273">Three digits which are an order code</span></span> 
- <span data-ttu-id="31aad-1274">одна цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-1274">One digit which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1275">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1275">Checksum</span></span>

<span data-ttu-id="31aad-1276">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1276">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1277">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1277">Definition</span></span>

<span data-ttu-id="31aad-1278">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1278">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1279">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1279">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1280">находится ключевое слово из Keyword_china_resident_id;</span><span class="sxs-lookup"><span data-stu-id="31aad-1280">A keyword from Keyword_china_resident_id is found.</span></span>
- <span data-ttu-id="31aad-1281">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1281">The checksum passes.</span></span>

<span data-ttu-id="31aad-1282">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1283">функция Func_china_resident_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1283">The function Func_china_resident_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1284">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1284">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1285">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1285">Keywords</span></span>

### <a name="keyword_china_resident_id"></a><span data-ttu-id="31aad-1286">Keyword_china_resident_id</span><span class="sxs-lookup"><span data-stu-id="31aad-1286">Keyword_china_resident_id</span></span>

- <span data-ttu-id="31aad-1287">Resident Identity Card</span><span class="sxs-lookup"><span data-stu-id="31aad-1287">Resident Identity Card</span></span> 
- <span data-ttu-id="31aad-1288">NO7</span><span class="sxs-lookup"><span data-stu-id="31aad-1288">PRC</span></span> 
- <span data-ttu-id="31aad-1289">National Identification Card</span><span class="sxs-lookup"><span data-stu-id="31aad-1289">National Identification Card</span></span> 
- <span data-ttu-id="31aad-1290">身份证</span><span class="sxs-lookup"><span data-stu-id="31aad-1290">身份证</span></span> 
- <span data-ttu-id="31aad-1291">居民 身份证</span><span class="sxs-lookup"><span data-stu-id="31aad-1291">居民 身份证</span></span> 
- <span data-ttu-id="31aad-1292">居民身份证</span><span class="sxs-lookup"><span data-stu-id="31aad-1292">居民身份证</span></span> 
- <span data-ttu-id="31aad-1293">鉴定</span><span class="sxs-lookup"><span data-stu-id="31aad-1293">鉴定</span></span> 
- <span data-ttu-id="31aad-1294">身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-1294">身分證</span></span> 
- <span data-ttu-id="31aad-1295">居民 身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-1295">居民 身份證</span></span>
- <span data-ttu-id="31aad-1296">鑑定</span><span class="sxs-lookup"><span data-stu-id="31aad-1296">鑑定</span></span> 
   
## <a name="credit-card-number"></a><span data-ttu-id="31aad-1297">Номер кредитной карты</span><span class="sxs-lookup"><span data-stu-id="31aad-1297">Credit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1298">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1298">Format</span></span>

<span data-ttu-id="31aad-1299">16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.</span><span class="sxs-lookup"><span data-stu-id="31aad-1299">16 digits which can be formatted or unformatted (dddddddddddddddd) and must pass the Luhn test.</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1300">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1300">Pattern</span></span>

<span data-ttu-id="31aad-1301">Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.</span><span class="sxs-lookup"><span data-stu-id="31aad-1301">Very complex and robust pattern that detects cards from all major brands worldwide, including Visa, MasterCard, Discover Card, JCB, American Express, gift cards, and diner cards.</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1302">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1302">Checksum</span></span>

<span data-ttu-id="31aad-1303">Да (рассчитывается по алгоритму Луна).</span><span class="sxs-lookup"><span data-stu-id="31aad-1303">Yes, the Luhn checksum</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1304">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1304">Definition</span></span>

<span data-ttu-id="31aad-1305">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1305">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1306">Функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1306">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1307">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-1307">One of the following is true:</span></span>
    - <span data-ttu-id="31aad-1308">найдено ключевое слово из Keyword_cc_verification;</span><span class="sxs-lookup"><span data-stu-id="31aad-1308">A keyword from Keyword_cc_verification is found.</span></span>
    - <span data-ttu-id="31aad-1309">найдено ключевое слово из Keyword_cc_name;</span><span class="sxs-lookup"><span data-stu-id="31aad-1309">A keyword from Keyword_cc_name is found.</span></span>
    - <span data-ttu-id="31aad-1310">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-1310">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-1311">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1311">The checksum passes.</span></span>

<span data-ttu-id="31aad-1312">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1312">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1313">функция Func_credit_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1313">The function Func_credit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1314">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1314">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1315">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1315">Keywords</span></span>

#### <a name="keyword_cc_verification"></a><span data-ttu-id="31aad-1316">Keyword_cc_verification</span><span class="sxs-lookup"><span data-stu-id="31aad-1316">Keyword_cc_verification</span></span>

- <span data-ttu-id="31aad-1317">card verification</span><span class="sxs-lookup"><span data-stu-id="31aad-1317">card verification</span></span>
- <span data-ttu-id="31aad-1318">card identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-1318">card identification number</span></span>
- <span data-ttu-id="31aad-1319">квн</span><span class="sxs-lookup"><span data-stu-id="31aad-1319">cvn</span></span>
- <span data-ttu-id="31aad-1320">cid</span><span class="sxs-lookup"><span data-stu-id="31aad-1320">cid</span></span>
- <span data-ttu-id="31aad-1321">cvc2</span><span class="sxs-lookup"><span data-stu-id="31aad-1321">cvc2</span></span>
- <span data-ttu-id="31aad-1322">cvv2</span><span class="sxs-lookup"><span data-stu-id="31aad-1322">cvv2</span></span>
- <span data-ttu-id="31aad-1323">pin block</span><span class="sxs-lookup"><span data-stu-id="31aad-1323">pin block</span></span>
- <span data-ttu-id="31aad-1324">security code</span><span class="sxs-lookup"><span data-stu-id="31aad-1324">security code</span></span>
- <span data-ttu-id="31aad-1325">security number</span><span class="sxs-lookup"><span data-stu-id="31aad-1325">security number</span></span>
- <span data-ttu-id="31aad-1326">security no</span><span class="sxs-lookup"><span data-stu-id="31aad-1326">security no</span></span>
- <span data-ttu-id="31aad-1327">issue number</span><span class="sxs-lookup"><span data-stu-id="31aad-1327">issue number</span></span>
- <span data-ttu-id="31aad-1328">issue no</span><span class="sxs-lookup"><span data-stu-id="31aad-1328">issue no</span></span>
- <span data-ttu-id="31aad-1329">криптограмме</span><span class="sxs-lookup"><span data-stu-id="31aad-1329">cryptogramme</span></span>
- <span data-ttu-id="31aad-1330">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="31aad-1330">numéro de sécurité</span></span>
- <span data-ttu-id="31aad-1331">numero de securite</span><span class="sxs-lookup"><span data-stu-id="31aad-1331">numero de securite</span></span>
- <span data-ttu-id="31aad-1332">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1332">kreditkartenprüfnummer</span></span>
- <span data-ttu-id="31aad-1333">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1333">kreditkartenprufnummer</span></span>
- <span data-ttu-id="31aad-1334">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="31aad-1334">prüfziffer</span></span>
- <span data-ttu-id="31aad-1335">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="31aad-1335">prufziffer</span></span>
- <span data-ttu-id="31aad-1336">sicherheits Kode</span><span class="sxs-lookup"><span data-stu-id="31aad-1336">sicherheits Kode</span></span>
- <span data-ttu-id="31aad-1337">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="31aad-1337">sicherheitscode</span></span>
- <span data-ttu-id="31aad-1338">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1338">sicherheitsnummer</span></span>
- <span data-ttu-id="31aad-1339">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1339">verfalldatum</span></span>
- <span data-ttu-id="31aad-1340">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="31aad-1340">codice di verifica</span></span>
- <span data-ttu-id="31aad-1341">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1341">cod.</span></span> <span data-ttu-id="31aad-1342">сикурезза</span><span class="sxs-lookup"><span data-stu-id="31aad-1342">sicurezza</span></span>
- <span data-ttu-id="31aad-1343">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="31aad-1343">cod sicurezza</span></span>
- <span data-ttu-id="31aad-1344">n autorizzazione</span><span class="sxs-lookup"><span data-stu-id="31aad-1344">n autorizzazione</span></span>
- <span data-ttu-id="31aad-1345">кóдиго</span><span class="sxs-lookup"><span data-stu-id="31aad-1345">código</span></span>
- <span data-ttu-id="31aad-1346">кодиго</span><span class="sxs-lookup"><span data-stu-id="31aad-1346">codigo</span></span>
- <span data-ttu-id="31aad-1347">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1347">cod.</span></span> <span data-ttu-id="31aad-1348">сег</span><span class="sxs-lookup"><span data-stu-id="31aad-1348">seg</span></span>
- <span data-ttu-id="31aad-1349">cod seg</span><span class="sxs-lookup"><span data-stu-id="31aad-1349">cod seg</span></span>
- <span data-ttu-id="31aad-1350">código de segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1350">código de segurança</span></span>
- <span data-ttu-id="31aad-1351">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1351">codigo de seguranca</span></span>
- <span data-ttu-id="31aad-1352">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1352">codigo de segurança</span></span>
- <span data-ttu-id="31aad-1353">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1353">código de seguranca</span></span>
- <span data-ttu-id="31aad-1354">кóд.</span><span class="sxs-lookup"><span data-stu-id="31aad-1354">cód.</span></span> <span data-ttu-id="31aad-1355">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="31aad-1355">segurança</span></span>
- <span data-ttu-id="31aad-1356">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1356">cod.</span></span> <span data-ttu-id="31aad-1357">сегуранка наложенный платеж.</span><span class="sxs-lookup"><span data-stu-id="31aad-1357">seguranca cod.</span></span> <span data-ttu-id="31aad-1358">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="31aad-1358">segurança</span></span>
- <span data-ttu-id="31aad-1359">кóд.</span><span class="sxs-lookup"><span data-stu-id="31aad-1359">cód.</span></span> <span data-ttu-id="31aad-1360">сегуранка</span><span class="sxs-lookup"><span data-stu-id="31aad-1360">seguranca</span></span>
- <span data-ttu-id="31aad-1361">cód segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1361">cód segurança</span></span>
- <span data-ttu-id="31aad-1362">наложенный на наложенный сегуранка сегуранçа</span><span class="sxs-lookup"><span data-stu-id="31aad-1362">cod seguranca cod segurança</span></span>
- <span data-ttu-id="31aad-1363">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1363">cód seguranca</span></span>
- <span data-ttu-id="31aad-1364">número de verificação</span><span class="sxs-lookup"><span data-stu-id="31aad-1364">número de verificação</span></span>
- <span data-ttu-id="31aad-1365">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="31aad-1365">numero de verificacao</span></span>
- <span data-ttu-id="31aad-1366">аблауф</span><span class="sxs-lookup"><span data-stu-id="31aad-1366">ablauf</span></span>
- <span data-ttu-id="31aad-1367">gültig bis</span><span class="sxs-lookup"><span data-stu-id="31aad-1367">gültig bis</span></span>
- <span data-ttu-id="31aad-1368">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1368">gültigkeitsdatum</span></span>
- <span data-ttu-id="31aad-1369">gultig bis</span><span class="sxs-lookup"><span data-stu-id="31aad-1369">gultig bis</span></span>
- <span data-ttu-id="31aad-1370">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1370">gultigkeitsdatum</span></span>
- <span data-ttu-id="31aad-1371">скаденза</span><span class="sxs-lookup"><span data-stu-id="31aad-1371">scadenza</span></span>
- <span data-ttu-id="31aad-1372">data scad</span><span class="sxs-lookup"><span data-stu-id="31aad-1372">data scad</span></span>
- <span data-ttu-id="31aad-1373">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="31aad-1373">fecha de expiracion</span></span>
- <span data-ttu-id="31aad-1374">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="31aad-1374">fecha de venc</span></span>
- <span data-ttu-id="31aad-1375">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="31aad-1375">vencimiento</span></span>
- <span data-ttu-id="31aad-1376">válido hasta</span><span class="sxs-lookup"><span data-stu-id="31aad-1376">válido hasta</span></span>
- <span data-ttu-id="31aad-1377">valido hasta</span><span class="sxs-lookup"><span data-stu-id="31aad-1377">valido hasta</span></span>
- <span data-ttu-id="31aad-1378">вто</span><span class="sxs-lookup"><span data-stu-id="31aad-1378">vto</span></span>
- <span data-ttu-id="31aad-1379">data de expiração</span><span class="sxs-lookup"><span data-stu-id="31aad-1379">data de expiração</span></span>
- <span data-ttu-id="31aad-1380">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="31aad-1380">data de expiracao</span></span>
- <span data-ttu-id="31aad-1381">data em que expira</span><span class="sxs-lookup"><span data-stu-id="31aad-1381">data em que expira</span></span>
- <span data-ttu-id="31aad-1382">валидаде</span><span class="sxs-lookup"><span data-stu-id="31aad-1382">validade</span></span>
- <span data-ttu-id="31aad-1383">валор</span><span class="sxs-lookup"><span data-stu-id="31aad-1383">valor</span></span>
- <span data-ttu-id="31aad-1384">венЦименто</span><span class="sxs-lookup"><span data-stu-id="31aad-1384">vencimento</span></span>
- <span data-ttu-id="31aad-1385">венк</span><span class="sxs-lookup"><span data-stu-id="31aad-1385">Venc</span></span> 

#### <a name="keyword_cc_name"></a><span data-ttu-id="31aad-1386">Keyword_cc_name</span><span class="sxs-lookup"><span data-stu-id="31aad-1386">Keyword_cc_name</span></span>

- <span data-ttu-id="31aad-1387">амекс</span><span class="sxs-lookup"><span data-stu-id="31aad-1387">amex</span></span>
- <span data-ttu-id="31aad-1388">american express</span><span class="sxs-lookup"><span data-stu-id="31aad-1388">american express</span></span>
- <span data-ttu-id="31aad-1389">американекспресс</span><span class="sxs-lookup"><span data-stu-id="31aad-1389">americanexpress</span></span>
- <span data-ttu-id="31aad-1390">Visa</span><span class="sxs-lookup"><span data-stu-id="31aad-1390">Visa</span></span>
- <span data-ttu-id="31aad-1391">MasterCard</span><span class="sxs-lookup"><span data-stu-id="31aad-1391">mastercard</span></span>
- <span data-ttu-id="31aad-1392">master card</span><span class="sxs-lookup"><span data-stu-id="31aad-1392">master card</span></span>
- <span data-ttu-id="31aad-1393">MC</span><span class="sxs-lookup"><span data-stu-id="31aad-1393">mc</span></span> 
- <span data-ttu-id="31aad-1394">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1394">mastercards</span></span>
- <span data-ttu-id="31aad-1395">master cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1395">master cards</span></span>
- <span data-ttu-id="31aad-1396">diner's Club</span><span class="sxs-lookup"><span data-stu-id="31aad-1396">diner's Club</span></span>
- <span data-ttu-id="31aad-1397">diners club</span><span class="sxs-lookup"><span data-stu-id="31aad-1397">diners club</span></span>
- <span data-ttu-id="31aad-1398">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="31aad-1398">dinersclub</span></span>
- <span data-ttu-id="31aad-1399">discover card</span><span class="sxs-lookup"><span data-stu-id="31aad-1399">discover card</span></span>
- <span data-ttu-id="31aad-1400">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="31aad-1400">discovercard</span></span>
- <span data-ttu-id="31aad-1401">discover cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1401">discover cards</span></span>
- <span data-ttu-id="31aad-1402">JCB</span><span class="sxs-lookup"><span data-stu-id="31aad-1402">JCB</span></span>
- <span data-ttu-id="31aad-1403">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="31aad-1403">japanese card bureau</span></span>
- <span data-ttu-id="31aad-1404">carte blanche</span><span class="sxs-lookup"><span data-stu-id="31aad-1404">carte blanche</span></span>
- <span data-ttu-id="31aad-1405">картебланче</span><span class="sxs-lookup"><span data-stu-id="31aad-1405">carteblanche</span></span>
- <span data-ttu-id="31aad-1406">credit card</span><span class="sxs-lookup"><span data-stu-id="31aad-1406">credit card</span></span>
- <span data-ttu-id="31aad-1407">Центральной #</span><span class="sxs-lookup"><span data-stu-id="31aad-1407">cc#</span></span>
- <span data-ttu-id="31aad-1408">CC #:</span><span class="sxs-lookup"><span data-stu-id="31aad-1408">cc#:</span></span>
- <span data-ttu-id="31aad-1409">expiration date</span><span class="sxs-lookup"><span data-stu-id="31aad-1409">expiration date</span></span>
- <span data-ttu-id="31aad-1410">exp date</span><span class="sxs-lookup"><span data-stu-id="31aad-1410">exp date</span></span>
- <span data-ttu-id="31aad-1411">expiry date</span><span class="sxs-lookup"><span data-stu-id="31aad-1411">expiry date</span></span>
- <span data-ttu-id="31aad-1412">date d’expiration</span><span class="sxs-lookup"><span data-stu-id="31aad-1412">date d’expiration</span></span>
- <span data-ttu-id="31aad-1413">date d'exp</span><span class="sxs-lookup"><span data-stu-id="31aad-1413">date d'exp</span></span>
- <span data-ttu-id="31aad-1414">date expiration</span><span class="sxs-lookup"><span data-stu-id="31aad-1414">date expiration</span></span>
- <span data-ttu-id="31aad-1415">bank card</span><span class="sxs-lookup"><span data-stu-id="31aad-1415">bank card</span></span>
- <span data-ttu-id="31aad-1416">банккард</span><span class="sxs-lookup"><span data-stu-id="31aad-1416">bankcard</span></span>
- <span data-ttu-id="31aad-1417">card number</span><span class="sxs-lookup"><span data-stu-id="31aad-1417">card number</span></span>
- <span data-ttu-id="31aad-1418">card num</span><span class="sxs-lookup"><span data-stu-id="31aad-1418">card num</span></span>
- <span data-ttu-id="31aad-1419">карднумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-1419">cardnumber</span></span>
- <span data-ttu-id="31aad-1420">карднумберс</span><span class="sxs-lookup"><span data-stu-id="31aad-1420">cardnumbers</span></span>
- <span data-ttu-id="31aad-1421">card numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-1421">card numbers</span></span>
- <span data-ttu-id="31aad-1422">кредиткард</span><span class="sxs-lookup"><span data-stu-id="31aad-1422">creditcard</span></span>
- <span data-ttu-id="31aad-1423">credit cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1423">credit cards</span></span>
- <span data-ttu-id="31aad-1424">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1424">creditcards</span></span>
- <span data-ttu-id="31aad-1425">CCN</span><span class="sxs-lookup"><span data-stu-id="31aad-1425">ccn</span></span>
- <span data-ttu-id="31aad-1426">card holder</span><span class="sxs-lookup"><span data-stu-id="31aad-1426">card holder</span></span>
- <span data-ttu-id="31aad-1427">банков</span><span class="sxs-lookup"><span data-stu-id="31aad-1427">cardholder</span></span>
- <span data-ttu-id="31aad-1428">card holders</span><span class="sxs-lookup"><span data-stu-id="31aad-1428">card holders</span></span>
- <span data-ttu-id="31aad-1429">карты</span><span class="sxs-lookup"><span data-stu-id="31aad-1429">cardholders</span></span>
- <span data-ttu-id="31aad-1430">check card</span><span class="sxs-lookup"><span data-stu-id="31aad-1430">check card</span></span>
- <span data-ttu-id="31aad-1431">чекккард</span><span class="sxs-lookup"><span data-stu-id="31aad-1431">checkcard</span></span>
- <span data-ttu-id="31aad-1432">check cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1432">check cards</span></span>
- <span data-ttu-id="31aad-1433">чекккардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1433">checkcards</span></span>
- <span data-ttu-id="31aad-1434">debit card</span><span class="sxs-lookup"><span data-stu-id="31aad-1434">debit card</span></span>
- <span data-ttu-id="31aad-1435">дебиткард</span><span class="sxs-lookup"><span data-stu-id="31aad-1435">debitcard</span></span>
- <span data-ttu-id="31aad-1436">debit cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1436">debit cards</span></span>
- <span data-ttu-id="31aad-1437">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1437">debitcards</span></span>
- <span data-ttu-id="31aad-1438">atm card</span><span class="sxs-lookup"><span data-stu-id="31aad-1438">atm card</span></span>
- <span data-ttu-id="31aad-1439">атмкард</span><span class="sxs-lookup"><span data-stu-id="31aad-1439">atmcard</span></span>
- <span data-ttu-id="31aad-1440">atm cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1440">atm cards</span></span>
- <span data-ttu-id="31aad-1441">атмкардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1441">atmcards</span></span>
- <span data-ttu-id="31aad-1442">енрауте</span><span class="sxs-lookup"><span data-stu-id="31aad-1442">enroute</span></span>
- <span data-ttu-id="31aad-1443">en route</span><span class="sxs-lookup"><span data-stu-id="31aad-1443">en route</span></span>
- <span data-ttu-id="31aad-1444">card type</span><span class="sxs-lookup"><span data-stu-id="31aad-1444">card type</span></span>
- <span data-ttu-id="31aad-1445">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="31aad-1445">carte bancaire</span></span>
- <span data-ttu-id="31aad-1446">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="31aad-1446">carte de crédit</span></span>
- <span data-ttu-id="31aad-1447">carte de credit</span><span class="sxs-lookup"><span data-stu-id="31aad-1447">carte de credit</span></span>
- <span data-ttu-id="31aad-1448">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1448">numéro de carte</span></span>
- <span data-ttu-id="31aad-1449">numero de carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1449">numero de carte</span></span>
- <span data-ttu-id="31aad-1450">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1450">nº de la carte</span></span>
- <span data-ttu-id="31aad-1451">nº de carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1451">nº de carte</span></span>
- <span data-ttu-id="31aad-1452">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="31aad-1452">kreditkarte</span></span>
- <span data-ttu-id="31aad-1453">карте</span><span class="sxs-lookup"><span data-stu-id="31aad-1453">karte</span></span>
- <span data-ttu-id="31aad-1454">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="31aad-1454">karteninhaber</span></span>
- <span data-ttu-id="31aad-1455">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="31aad-1455">karteninhabers</span></span>
- <span data-ttu-id="31aad-1456">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="31aad-1456">kreditkarteninhaber</span></span>
- <span data-ttu-id="31aad-1457">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="31aad-1457">kreditkarteninstitut</span></span>
- <span data-ttu-id="31aad-1458">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="31aad-1458">kreditkartentyp</span></span>
- <span data-ttu-id="31aad-1459">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="31aad-1459">eigentümername</span></span>
- <span data-ttu-id="31aad-1460">картеннр</span><span class="sxs-lookup"><span data-stu-id="31aad-1460">kartennr</span></span> 
- <span data-ttu-id="31aad-1461">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1461">kartennummer</span></span>
- <span data-ttu-id="31aad-1462">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1462">kreditkartennummer</span></span>
- <span data-ttu-id="31aad-1463">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1463">kreditkarten-nummer</span></span>
- <span data-ttu-id="31aad-1464">carta di credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1464">carta di credito</span></span>
- <span data-ttu-id="31aad-1465">carta credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1465">carta credito</span></span>
- <span data-ttu-id="31aad-1466">Корзина "</span><span class="sxs-lookup"><span data-stu-id="31aad-1466">carta</span></span>
- <span data-ttu-id="31aad-1467">n carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1467">n carta</span></span>
- <span data-ttu-id="31aad-1468">НР.</span><span class="sxs-lookup"><span data-stu-id="31aad-1468">nr.</span></span> <span data-ttu-id="31aad-1469">Корзина "</span><span class="sxs-lookup"><span data-stu-id="31aad-1469">carta</span></span>
- <span data-ttu-id="31aad-1470">nr carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1470">nr carta</span></span>
- <span data-ttu-id="31aad-1471">numero carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1471">numero carta</span></span>
- <span data-ttu-id="31aad-1472">numero della carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1472">numero della carta</span></span>
- <span data-ttu-id="31aad-1473">numero di carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1473">numero di carta</span></span>
- <span data-ttu-id="31aad-1474">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1474">tarjeta credito</span></span>
- <span data-ttu-id="31aad-1475">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1475">tarjeta de credito</span></span>
- <span data-ttu-id="31aad-1476">tarjeta crédito</span><span class="sxs-lookup"><span data-stu-id="31aad-1476">tarjeta crédito</span></span>
- <span data-ttu-id="31aad-1477">tarjeta de crédito</span><span class="sxs-lookup"><span data-stu-id="31aad-1477">tarjeta de crédito</span></span>
- <span data-ttu-id="31aad-1478">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="31aad-1478">tarjeta de atm</span></span>
- <span data-ttu-id="31aad-1479">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="31aad-1479">tarjeta atm</span></span>
- <span data-ttu-id="31aad-1480">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1480">tarjeta debito</span></span>
- <span data-ttu-id="31aad-1481">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1481">tarjeta de debito</span></span>
- <span data-ttu-id="31aad-1482">tarjeta débito</span><span class="sxs-lookup"><span data-stu-id="31aad-1482">tarjeta débito</span></span>
- <span data-ttu-id="31aad-1483">tarjeta de débito</span><span class="sxs-lookup"><span data-stu-id="31aad-1483">tarjeta de débito</span></span>
- <span data-ttu-id="31aad-1484">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1484">nº de tarjeta</span></span>
- <span data-ttu-id="31aad-1485">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1485">no.</span></span> <span data-ttu-id="31aad-1486">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1486">de tarjeta</span></span>
- <span data-ttu-id="31aad-1487">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1487">no de tarjeta</span></span>
- <span data-ttu-id="31aad-1488">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1488">numero de tarjeta</span></span>
- <span data-ttu-id="31aad-1489">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1489">número de tarjeta</span></span>
- <span data-ttu-id="31aad-1490">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="31aad-1490">tarjeta no</span></span>
- <span data-ttu-id="31aad-1491">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="31aad-1491">tarjetahabiente</span></span>
- <span data-ttu-id="31aad-1492">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="31aad-1492">cartão de crédito</span></span>
- <span data-ttu-id="31aad-1493">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1493">cartão de credito</span></span>
- <span data-ttu-id="31aad-1494">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="31aad-1494">cartao de crédito</span></span>
- <span data-ttu-id="31aad-1495">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1495">cartao de credito</span></span>
- <span data-ttu-id="31aad-1496">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="31aad-1496">cartão de débito</span></span>
- <span data-ttu-id="31aad-1497">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="31aad-1497">cartao de débito</span></span>
- <span data-ttu-id="31aad-1498">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1498">cartão de debito</span></span>
- <span data-ttu-id="31aad-1499">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1499">cartao de debito</span></span>
- <span data-ttu-id="31aad-1500">débito automático</span><span class="sxs-lookup"><span data-stu-id="31aad-1500">débito automático</span></span>
- <span data-ttu-id="31aad-1501">debito automatico</span><span class="sxs-lookup"><span data-stu-id="31aad-1501">debito automatico</span></span>
- <span data-ttu-id="31aad-1502">número do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1502">número do cartão</span></span>
- <span data-ttu-id="31aad-1503">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1503">numero do cartão</span></span> 
- <span data-ttu-id="31aad-1504">número do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1504">número do cartao</span></span>
- <span data-ttu-id="31aad-1505">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1505">numero do cartao</span></span>
- <span data-ttu-id="31aad-1506">número de cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1506">número de cartão</span></span>
- <span data-ttu-id="31aad-1507">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1507">numero de cartão</span></span>
- <span data-ttu-id="31aad-1508">número de cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1508">número de cartao</span></span>
- <span data-ttu-id="31aad-1509">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1509">numero de cartao</span></span>
- <span data-ttu-id="31aad-1510">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1510">nº do cartão</span></span>
- <span data-ttu-id="31aad-1511">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1511">nº do cartao</span></span>
- <span data-ttu-id="31aad-1512">n º.</span><span class="sxs-lookup"><span data-stu-id="31aad-1512">nº.</span></span> <span data-ttu-id="31aad-1513">do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1513">do cartão</span></span>
- <span data-ttu-id="31aad-1514">no do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1514">no do cartão</span></span>
- <span data-ttu-id="31aad-1515">no do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1515">no do cartao</span></span>
- <span data-ttu-id="31aad-1516">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1516">no.</span></span> <span data-ttu-id="31aad-1517">do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1517">do cartão</span></span>
- <span data-ttu-id="31aad-1518">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1518">no.</span></span> <span data-ttu-id="31aad-1519">do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1519">do cartao</span></span> 
   
## <a name="croatia-identity-card-number"></a><span data-ttu-id="31aad-1520">	Номер удостоверения личности для Хорватии</span><span class="sxs-lookup"><span data-stu-id="31aad-1520">Croatia Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1521">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1521">Format</span></span>

<span data-ttu-id="31aad-1522">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1522">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1523">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1523">Pattern</span></span>

<span data-ttu-id="31aad-1524">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1524">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1525">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1525">Checksum</span></span>

<span data-ttu-id="31aad-1526">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-1526">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1527">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1527">Definition</span></span>

<span data-ttu-id="31aad-1528">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1528">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1529">функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1529">The function Func_croatia_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1530">находится ключевое слово из Keyword_croatia_id_card.</span><span class="sxs-lookup"><span data-stu-id="31aad-1530">A keyword from Keyword_croatia_id_card is found.</span></span>

```xml
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-1531">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1531">Keywords</span></span>

#### <a name="keyword_croatia_id_card"></a><span data-ttu-id="31aad-1532">Keyword_croatia_id_card</span><span class="sxs-lookup"><span data-stu-id="31aad-1532">Keyword_croatia_id_card</span></span>

- <span data-ttu-id="31aad-1533">Croatian identity card</span><span class="sxs-lookup"><span data-stu-id="31aad-1533">Croatian identity card</span></span>
- <span data-ttu-id="31aad-1534">Osobna iskaznica</span><span class="sxs-lookup"><span data-stu-id="31aad-1534">Osobna iskaznica</span></span>

   
## <a name="croatia-personal-identification-oib-number"></a><span data-ttu-id="31aad-1535">	Индивидуальный идентификационный номер (OIB) для Хорватии</span><span class="sxs-lookup"><span data-stu-id="31aad-1535">Croatia Personal Identification (OIB) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1536">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1536">Format</span></span>

<span data-ttu-id="31aad-1537">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1537">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1538">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1538">Pattern</span></span>

<span data-ttu-id="31aad-1539">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-1539">11 digits:</span></span>
- <span data-ttu-id="31aad-1540">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1540">10 digits</span></span> 
- <span data-ttu-id="31aad-1541">Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1541">Final digit is a check digit For the purposes of international data exchange, the letters HR are added preceding the eleven digits.</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1542">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1542">Checksum</span></span>

<span data-ttu-id="31aad-1543">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1543">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1544">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1544">Definition</span></span>

<span data-ttu-id="31aad-1545">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1545">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1546">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1546">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1547">находится ключевое слово из Keyword_croatia_oib_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-1547">A keyword from Keyword_croatia_oib_number is found.</span></span>
- <span data-ttu-id="31aad-1548">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1548">The checksum passes.</span></span>

<span data-ttu-id="31aad-1549">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1549">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1550">функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1550">The function Func_croatia_oib_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1551">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1551">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1552">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1552">Keywords</span></span>

#### <a name="keyword_croatia_oib_number"></a><span data-ttu-id="31aad-1553">Keyword_croatia_oib_number</span><span class="sxs-lookup"><span data-stu-id="31aad-1553">Keyword_croatia_oib_number</span></span>

- <span data-ttu-id="31aad-1554">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="31aad-1554">Personal Identification Number</span></span>
- <span data-ttu-id="31aad-1555">Osobni identifikacijski broj</span><span class="sxs-lookup"><span data-stu-id="31aad-1555">Osobni identifikacijski broj</span></span> 
- <span data-ttu-id="31aad-1556">OIB</span><span class="sxs-lookup"><span data-stu-id="31aad-1556">OIB</span></span> 

   
## <a name="czech-personal-identity-number"></a><span data-ttu-id="31aad-1557">Номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="31aad-1557">Czech Personal Identity Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1558">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1558">Format</span></span>

<span data-ttu-id="31aad-1559">Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)</span><span class="sxs-lookup"><span data-stu-id="31aad-1559">Nine digits with optional forward slash (old format) 10 digits with optional forward slash (new format)</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1560">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1560">Pattern</span></span>

<span data-ttu-id="31aad-1561">Девять цифр (старый формат):</span><span class="sxs-lookup"><span data-stu-id="31aad-1561">Nine digits (old format):</span></span>
- <span data-ttu-id="31aad-1562">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1562">Nine digits</span></span>

<span data-ttu-id="31aad-1563">OR</span><span class="sxs-lookup"><span data-stu-id="31aad-1563">OR</span></span>

- <span data-ttu-id="31aad-1564">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="31aad-1564">Six digits that represent date of birth</span></span>
- <span data-ttu-id="31aad-1565">косая черта;</span><span class="sxs-lookup"><span data-stu-id="31aad-1565">A forward slash</span></span>
- <span data-ttu-id="31aad-1566">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-1566">Three digits</span></span>

<span data-ttu-id="31aad-1567">10 цифр (новый формат):</span><span class="sxs-lookup"><span data-stu-id="31aad-1567">10 digits (new format):</span></span>
- <span data-ttu-id="31aad-1568">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1568">10 digits</span></span>

<span data-ttu-id="31aad-1569">OR</span><span class="sxs-lookup"><span data-stu-id="31aad-1569">OR</span></span>

- <span data-ttu-id="31aad-1570">Шесть цифр, представляющих дату рождения</span><span class="sxs-lookup"><span data-stu-id="31aad-1570">Six digits that represent date of birth</span></span>
- <span data-ttu-id="31aad-1571">косая черта;</span><span class="sxs-lookup"><span data-stu-id="31aad-1571">A forward slash</span></span> 
- <span data-ttu-id="31aad-1572">Четыре цифры, где последняя цифра является контрольной цифрой</span><span class="sxs-lookup"><span data-stu-id="31aad-1572">Four digits where last digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1573">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1573">Checksum</span></span>

<span data-ttu-id="31aad-1574">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1574">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1575">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1575">Definition</span></span>

<span data-ttu-id="31aad-1576">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_czech_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1576">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_czech_id_card finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-1577">находится ключевое слово из Keyword_czech_id_card;</span><span class="sxs-lookup"><span data-stu-id="31aad-1577">A keyword from Keyword_czech_id_card is found.</span></span>
<span data-ttu-id="31aad-1578">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1578">The checksum passes.</span></span>

```xml
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a><span data-ttu-id="31aad-1579">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1579">Keywords</span></span>

- <span data-ttu-id="31aad-1580">номер личного удостоверения для чешского языка</span><span class="sxs-lookup"><span data-stu-id="31aad-1580">czech personal identity number</span></span>
- <span data-ttu-id="31aad-1581">Роднé číсло</span><span class="sxs-lookup"><span data-stu-id="31aad-1581">Rodné číslo</span></span>
   
## <a name="denmark-personal-identification-number"></a><span data-ttu-id="31aad-1582">	Индивидуальный идентификационный номер для Дании</span><span class="sxs-lookup"><span data-stu-id="31aad-1582">Denmark Personal Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1583">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1583">Format</span></span>

<span data-ttu-id="31aad-1584">10 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="31aad-1584">10 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1585">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1585">Pattern</span></span>

<span data-ttu-id="31aad-1586">10 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-1586">10 digits:</span></span>
- <span data-ttu-id="31aad-1587">шесть цифр в формате ДДММГГ — дата рождения;</span><span class="sxs-lookup"><span data-stu-id="31aad-1587">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="31aad-1588">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-1588">A hyphen</span></span> 
- <span data-ttu-id="31aad-1589">четыре цифры, где последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-1589">Four digits where the final digit is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1590">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1590">Checksum</span></span>

<span data-ttu-id="31aad-1591">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1591">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1592">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1592">Definition</span></span>

<span data-ttu-id="31aad-1593">Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Regex_denmark_id находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-1593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_denmark_id finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-1594">находится ключевое слово из Keyword_denmark_id;</span><span class="sxs-lookup"><span data-stu-id="31aad-1594">A keyword from Keyword_denmark_id is found.</span></span>
<span data-ttu-id="31aad-1595">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1595">The checksum passes.</span></span>

```xml
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-1596">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1596">Keywords</span></span>

#### <a name="keyword_denmark_id"></a><span data-ttu-id="31aad-1597">Keyword_denmark_id</span><span class="sxs-lookup"><span data-stu-id="31aad-1597">Keyword_denmark_id</span></span>

- <span data-ttu-id="31aad-1598">Personal Identification Number</span><span class="sxs-lookup"><span data-stu-id="31aad-1598">Personal Identification Number</span></span>
- <span data-ttu-id="31aad-1599">CPR</span><span class="sxs-lookup"><span data-stu-id="31aad-1599">CPR</span></span>
- <span data-ttu-id="31aad-1600">Det Centrale Personregister</span><span class="sxs-lookup"><span data-stu-id="31aad-1600">Det Centrale Personregister</span></span>
- <span data-ttu-id="31aad-1601">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1601">Personnummer</span></span>
   
## <a name="drug-enforcement-agency-dea-number"></a><span data-ttu-id="31aad-1602">Номер Управления по борьбе с наркотиками США (DEA)</span><span class="sxs-lookup"><span data-stu-id="31aad-1602">Drug Enforcement Agency (DEA) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1603">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1603">Format</span></span>

<span data-ttu-id="31aad-1604">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1604">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1605">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1605">Pattern</span></span>

<span data-ttu-id="31aad-1606">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="31aad-1606">Pattern must include all of the following:</span></span>
- <span data-ttu-id="31aad-1607">Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="31aad-1607">One letter (not case sensitive) from this set of possible letters: abcdefghjklmnprstux, which is a registrant code</span></span> 
- <span data-ttu-id="31aad-1608">Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица</span><span class="sxs-lookup"><span data-stu-id="31aad-1608">One letter (not case sensitive), which is the first letter of the registrant's last name</span></span> 
- <span data-ttu-id="31aad-1609">Семь цифр, последняя из которых — контрольная</span><span class="sxs-lookup"><span data-stu-id="31aad-1609">Seven digits, the last of which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1610">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1610">Checksum</span></span>

<span data-ttu-id="31aad-1611">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1611">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1612">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1612">Definition</span></span>

<span data-ttu-id="31aad-1613">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1613">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1614">функция Func_dea_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1614">The function Func_dea_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1615">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1615">The checksum passes.</span></span>

```xml
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-1616">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1616">Keywords</span></span>

<span data-ttu-id="31aad-1617">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-1617">None</span></span>

   
## <a name="eu-debit-card-number"></a><span data-ttu-id="31aad-1618">Номер банковской карты для ЕС</span><span class="sxs-lookup"><span data-stu-id="31aad-1618">EU Debit Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1619">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1619">Format</span></span>

<span data-ttu-id="31aad-1620">16 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1620">16 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1621">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1621">Pattern</span></span>

<span data-ttu-id="31aad-1622">Очень сложный и надежный шаблон.</span><span class="sxs-lookup"><span data-stu-id="31aad-1622">Very complex and robust pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1623">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1623">Checksum</span></span>

<span data-ttu-id="31aad-1624">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1624">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1625">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1625">Definition</span></span>

<span data-ttu-id="31aad-1626">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1626">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1627">Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-1627">The function Func_eu_debit_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1628">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-1628">At least one of the following is true:</span></span>
    - <span data-ttu-id="31aad-1629">найдено ключевое слово из Keyword_eu_debit_card;</span><span class="sxs-lookup"><span data-stu-id="31aad-1629">A keyword from Keyword_eu_debit_card is found.</span></span>
    - <span data-ttu-id="31aad-1630">найдено ключевое слово из Keyword_card_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="31aad-1630">A keyword from Keyword_card_terms_dict is found.</span></span>
    - <span data-ttu-id="31aad-1631">найдено ключевое слово из Keyword_card_security_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="31aad-1631">A keyword from Keyword_card_security_terms_dict is found.</span></span>
    - <span data-ttu-id="31aad-1632">найдено ключевое слово из Keyword_card_expiration_terms_dict;</span><span class="sxs-lookup"><span data-stu-id="31aad-1632">A keyword from Keyword_card_expiration_terms_dict is found.</span></span>
    - <span data-ttu-id="31aad-1633">функция Func_expiration_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-1633">The function Func_expiration_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-1634">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1634">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1635">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1635">Keywords</span></span>

#### <a name="keyword_eu_debit_card"></a><span data-ttu-id="31aad-1636">Keyword_eu_debit_card</span><span class="sxs-lookup"><span data-stu-id="31aad-1636">Keyword_eu_debit_card</span></span>

- <span data-ttu-id="31aad-1637">account number</span><span class="sxs-lookup"><span data-stu-id="31aad-1637">account number</span></span> 
- <span data-ttu-id="31aad-1638">card number</span><span class="sxs-lookup"><span data-stu-id="31aad-1638">card number</span></span> 
- <span data-ttu-id="31aad-1639">card no.</span><span class="sxs-lookup"><span data-stu-id="31aad-1639">card no.</span></span> 
- <span data-ttu-id="31aad-1640">security number</span><span class="sxs-lookup"><span data-stu-id="31aad-1640">security number</span></span> 
- <span data-ttu-id="31aad-1641">Центральной #</span><span class="sxs-lookup"><span data-stu-id="31aad-1641">cc#</span></span> 

#### <a name="keyword_card_terms_dict"></a><span data-ttu-id="31aad-1642">Keyword_card_terms_dict</span><span class="sxs-lookup"><span data-stu-id="31aad-1642">Keyword_card_terms_dict</span></span>

- <span data-ttu-id="31aad-1643">acct nbr</span><span class="sxs-lookup"><span data-stu-id="31aad-1643">acct nbr</span></span> 
- <span data-ttu-id="31aad-1644">acct num</span><span class="sxs-lookup"><span data-stu-id="31aad-1644">acct num</span></span> 
- <span data-ttu-id="31aad-1645">acct no</span><span class="sxs-lookup"><span data-stu-id="31aad-1645">acct no</span></span> 
- <span data-ttu-id="31aad-1646">american express</span><span class="sxs-lookup"><span data-stu-id="31aad-1646">american express</span></span> 
- <span data-ttu-id="31aad-1647">американекспресс</span><span class="sxs-lookup"><span data-stu-id="31aad-1647">americanexpress</span></span> 
- <span data-ttu-id="31aad-1648">americano espresso</span><span class="sxs-lookup"><span data-stu-id="31aad-1648">americano espresso</span></span> 
- <span data-ttu-id="31aad-1649">амекс</span><span class="sxs-lookup"><span data-stu-id="31aad-1649">amex</span></span> 
- <span data-ttu-id="31aad-1650">atm card</span><span class="sxs-lookup"><span data-stu-id="31aad-1650">atm card</span></span> 
- <span data-ttu-id="31aad-1651">atm cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1651">atm cards</span></span> 
- <span data-ttu-id="31aad-1652">atm kaart</span><span class="sxs-lookup"><span data-stu-id="31aad-1652">atm kaart</span></span> 
- <span data-ttu-id="31aad-1653">атмкард</span><span class="sxs-lookup"><span data-stu-id="31aad-1653">atmcard</span></span> 
- <span data-ttu-id="31aad-1654">атмкардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1654">atmcards</span></span> 
- <span data-ttu-id="31aad-1655">атмкаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1655">atmkaart</span></span> 
- <span data-ttu-id="31aad-1656">атмкаартен</span><span class="sxs-lookup"><span data-stu-id="31aad-1656">atmkaarten</span></span> 
- <span data-ttu-id="31aad-1657">банконтакт</span><span class="sxs-lookup"><span data-stu-id="31aad-1657">bancontact</span></span> 
- <span data-ttu-id="31aad-1658">bank card</span><span class="sxs-lookup"><span data-stu-id="31aad-1658">bank card</span></span> 
- <span data-ttu-id="31aad-1659">банккаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1659">bankkaart</span></span> 
- <span data-ttu-id="31aad-1660">card holder</span><span class="sxs-lookup"><span data-stu-id="31aad-1660">card holder</span></span> 
- <span data-ttu-id="31aad-1661">card holders</span><span class="sxs-lookup"><span data-stu-id="31aad-1661">card holders</span></span> 
- <span data-ttu-id="31aad-1662">card num</span><span class="sxs-lookup"><span data-stu-id="31aad-1662">card num</span></span> 
- <span data-ttu-id="31aad-1663">card number</span><span class="sxs-lookup"><span data-stu-id="31aad-1663">card number</span></span> 
- <span data-ttu-id="31aad-1664">card numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-1664">card numbers</span></span> 
- <span data-ttu-id="31aad-1665">card type</span><span class="sxs-lookup"><span data-stu-id="31aad-1665">card type</span></span> 
- <span data-ttu-id="31aad-1666">cardano numerico</span><span class="sxs-lookup"><span data-stu-id="31aad-1666">cardano numerico</span></span> 
- <span data-ttu-id="31aad-1667">банков</span><span class="sxs-lookup"><span data-stu-id="31aad-1667">cardholder</span></span> 
- <span data-ttu-id="31aad-1668">карты</span><span class="sxs-lookup"><span data-stu-id="31aad-1668">cardholders</span></span> 
- <span data-ttu-id="31aad-1669">карднумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-1669">cardnumber</span></span> 
- <span data-ttu-id="31aad-1670">карднумберс</span><span class="sxs-lookup"><span data-stu-id="31aad-1670">cardnumbers</span></span> 
- <span data-ttu-id="31aad-1671">carta bianca</span><span class="sxs-lookup"><span data-stu-id="31aad-1671">carta bianca</span></span> 
- <span data-ttu-id="31aad-1672">carta credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1672">carta credito</span></span> 
- <span data-ttu-id="31aad-1673">carta di credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1673">carta di credito</span></span> 
- <span data-ttu-id="31aad-1674">cartao de credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1674">cartao de credito</span></span> 
- <span data-ttu-id="31aad-1675">cartao de crédito</span><span class="sxs-lookup"><span data-stu-id="31aad-1675">cartao de crédito</span></span> 
- <span data-ttu-id="31aad-1676">cartao de debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1676">cartao de debito</span></span> 
- <span data-ttu-id="31aad-1677">cartao de débito</span><span class="sxs-lookup"><span data-stu-id="31aad-1677">cartao de débito</span></span> 
- <span data-ttu-id="31aad-1678">carte bancaire</span><span class="sxs-lookup"><span data-stu-id="31aad-1678">carte bancaire</span></span> 
- <span data-ttu-id="31aad-1679">carte blanche</span><span class="sxs-lookup"><span data-stu-id="31aad-1679">carte blanche</span></span> 
- <span data-ttu-id="31aad-1680">carte bleue</span><span class="sxs-lookup"><span data-stu-id="31aad-1680">carte bleue</span></span> 
- <span data-ttu-id="31aad-1681">carte de credit</span><span class="sxs-lookup"><span data-stu-id="31aad-1681">carte de credit</span></span> 
- <span data-ttu-id="31aad-1682">carte de crédit</span><span class="sxs-lookup"><span data-stu-id="31aad-1682">carte de crédit</span></span> 
- <span data-ttu-id="31aad-1683">carte di credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1683">carte di credito</span></span> 
- <span data-ttu-id="31aad-1684">картебланче</span><span class="sxs-lookup"><span data-stu-id="31aad-1684">carteblanche</span></span> 
- <span data-ttu-id="31aad-1685">cartão de credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1685">cartão de credito</span></span> 
- <span data-ttu-id="31aad-1686">cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="31aad-1686">cartão de crédito</span></span> 
- <span data-ttu-id="31aad-1687">cartão de debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1687">cartão de debito</span></span> 
- <span data-ttu-id="31aad-1688">cartão de débito</span><span class="sxs-lookup"><span data-stu-id="31aad-1688">cartão de débito</span></span> 
- <span data-ttu-id="31aad-1689">cb</span><span class="sxs-lookup"><span data-stu-id="31aad-1689">cb</span></span> 
- <span data-ttu-id="31aad-1690">CCN</span><span class="sxs-lookup"><span data-stu-id="31aad-1690">ccn</span></span> 
- <span data-ttu-id="31aad-1691">check card</span><span class="sxs-lookup"><span data-stu-id="31aad-1691">check card</span></span> 
- <span data-ttu-id="31aad-1692">check cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1692">check cards</span></span> 
- <span data-ttu-id="31aad-1693">чекккард</span><span class="sxs-lookup"><span data-stu-id="31aad-1693">checkcard</span></span>
- <span data-ttu-id="31aad-1694">чекккардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1694">checkcards</span></span> 
- <span data-ttu-id="31aad-1695">чекуекаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1695">chequekaart</span></span> 
- <span data-ttu-id="31aad-1696">Logic</span><span class="sxs-lookup"><span data-stu-id="31aad-1696">cirrus</span></span> 
- <span data-ttu-id="31aad-1697">Cirrus центр EDC — Маестро</span><span class="sxs-lookup"><span data-stu-id="31aad-1697">cirrus-edc-maestro</span></span> 
- <span data-ttu-id="31aad-1698">контролекаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1698">controlekaart</span></span> 
- <span data-ttu-id="31aad-1699">контролекаартен</span><span class="sxs-lookup"><span data-stu-id="31aad-1699">controlekaarten</span></span> 
- <span data-ttu-id="31aad-1700">credit card</span><span class="sxs-lookup"><span data-stu-id="31aad-1700">credit card</span></span> 
- <span data-ttu-id="31aad-1701">credit cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1701">credit cards</span></span> 
- <span data-ttu-id="31aad-1702">кредиткард</span><span class="sxs-lookup"><span data-stu-id="31aad-1702">creditcard</span></span> 
- <span data-ttu-id="31aad-1703">кредиткардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1703">creditcards</span></span> 
- <span data-ttu-id="31aad-1704">дебеткаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1704">debetkaart</span></span> 
- <span data-ttu-id="31aad-1705">дебеткаартен</span><span class="sxs-lookup"><span data-stu-id="31aad-1705">debetkaarten</span></span> 
- <span data-ttu-id="31aad-1706">debit card</span><span class="sxs-lookup"><span data-stu-id="31aad-1706">debit card</span></span> 
- <span data-ttu-id="31aad-1707">debit cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1707">debit cards</span></span> 
- <span data-ttu-id="31aad-1708">дебиткард</span><span class="sxs-lookup"><span data-stu-id="31aad-1708">debitcard</span></span> 
- <span data-ttu-id="31aad-1709">дебиткардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1709">debitcards</span></span> 
- <span data-ttu-id="31aad-1710">debito automatico</span><span class="sxs-lookup"><span data-stu-id="31aad-1710">debito automatico</span></span> 
- <span data-ttu-id="31aad-1711">diners club</span><span class="sxs-lookup"><span data-stu-id="31aad-1711">diners club</span></span> 
- <span data-ttu-id="31aad-1712">динерсклуб</span><span class="sxs-lookup"><span data-stu-id="31aad-1712">dinersclub</span></span> 
- <span data-ttu-id="31aad-1713">Повтор</span><span class="sxs-lookup"><span data-stu-id="31aad-1713">discover</span></span> 
- <span data-ttu-id="31aad-1714">discover card</span><span class="sxs-lookup"><span data-stu-id="31aad-1714">discover card</span></span> 
- <span data-ttu-id="31aad-1715">discover cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1715">discover cards</span></span> 
- <span data-ttu-id="31aad-1716">дисковеркард</span><span class="sxs-lookup"><span data-stu-id="31aad-1716">discovercard</span></span> 
- <span data-ttu-id="31aad-1717">дисковеркардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1717">discovercards</span></span> 
- <span data-ttu-id="31aad-1718">débito automático</span><span class="sxs-lookup"><span data-stu-id="31aad-1718">débito automático</span></span>
- <span data-ttu-id="31aad-1719">центр EDC</span><span class="sxs-lookup"><span data-stu-id="31aad-1719">edc</span></span> 
- <span data-ttu-id="31aad-1720">еижентüмернаме</span><span class="sxs-lookup"><span data-stu-id="31aad-1720">eigentümername</span></span> 
- <span data-ttu-id="31aad-1721">european debit card</span><span class="sxs-lookup"><span data-stu-id="31aad-1721">european debit card</span></span> 
- <span data-ttu-id="31aad-1722">хуфдкаарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1722">hoofdkaart</span></span> 
- <span data-ttu-id="31aad-1723">хуфдкаартен</span><span class="sxs-lookup"><span data-stu-id="31aad-1723">hoofdkaarten</span></span> 
- <span data-ttu-id="31aad-1724">in viaggio</span><span class="sxs-lookup"><span data-stu-id="31aad-1724">in viaggio</span></span> 
- <span data-ttu-id="31aad-1725">japanese card bureau</span><span class="sxs-lookup"><span data-stu-id="31aad-1725">japanese card bureau</span></span> 
- <span data-ttu-id="31aad-1726">japanse kaartdienst</span><span class="sxs-lookup"><span data-stu-id="31aad-1726">japanse kaartdienst</span></span> 
- <span data-ttu-id="31aad-1727">JCB</span><span class="sxs-lookup"><span data-stu-id="31aad-1727">jcb</span></span> 
- <span data-ttu-id="31aad-1728">каарт</span><span class="sxs-lookup"><span data-stu-id="31aad-1728">kaart</span></span> 
- <span data-ttu-id="31aad-1729">kaart num</span><span class="sxs-lookup"><span data-stu-id="31aad-1729">kaart num</span></span> 
- <span data-ttu-id="31aad-1730">каартаантал</span><span class="sxs-lookup"><span data-stu-id="31aad-1730">kaartaantal</span></span> 
- <span data-ttu-id="31aad-1731">каартаанталлен</span><span class="sxs-lookup"><span data-stu-id="31aad-1731">kaartaantallen</span></span> 
- <span data-ttu-id="31aad-1732">каарсаудер</span><span class="sxs-lookup"><span data-stu-id="31aad-1732">kaarthouder</span></span> 
- <span data-ttu-id="31aad-1733">каарсаудерс</span><span class="sxs-lookup"><span data-stu-id="31aad-1733">kaarthouders</span></span> 
- <span data-ttu-id="31aad-1734">карте</span><span class="sxs-lookup"><span data-stu-id="31aad-1734">karte</span></span>  
- <span data-ttu-id="31aad-1735">картенинхабер</span><span class="sxs-lookup"><span data-stu-id="31aad-1735">karteninhaber</span></span> 
- <span data-ttu-id="31aad-1736">картенинхаберс</span><span class="sxs-lookup"><span data-stu-id="31aad-1736">karteninhabers</span></span>
- <span data-ttu-id="31aad-1737">картеннр</span><span class="sxs-lookup"><span data-stu-id="31aad-1737">kartennr</span></span> 
- <span data-ttu-id="31aad-1738">картеннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1738">kartennummer</span></span> 
- <span data-ttu-id="31aad-1739">кредиткарте</span><span class="sxs-lookup"><span data-stu-id="31aad-1739">kreditkarte</span></span> 
- <span data-ttu-id="31aad-1740">кредиткартен — нуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1740">kreditkarten-nummer</span></span> 
- <span data-ttu-id="31aad-1741">кредиткартенинхабер</span><span class="sxs-lookup"><span data-stu-id="31aad-1741">kreditkarteninhaber</span></span> 
- <span data-ttu-id="31aad-1742">кредиткартенинститут</span><span class="sxs-lookup"><span data-stu-id="31aad-1742">kreditkarteninstitut</span></span> 
- <span data-ttu-id="31aad-1743">кредиткартеннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1743">kreditkartennummer</span></span> 
- <span data-ttu-id="31aad-1744">кредиткартентип</span><span class="sxs-lookup"><span data-stu-id="31aad-1744">kreditkartentyp</span></span> 
- <span data-ttu-id="31aad-1745">маестро</span><span class="sxs-lookup"><span data-stu-id="31aad-1745">maestro</span></span> 
- <span data-ttu-id="31aad-1746">master card</span><span class="sxs-lookup"><span data-stu-id="31aad-1746">master card</span></span> 
- <span data-ttu-id="31aad-1747">master cards</span><span class="sxs-lookup"><span data-stu-id="31aad-1747">master cards</span></span> 
- <span data-ttu-id="31aad-1748">MasterCard</span><span class="sxs-lookup"><span data-stu-id="31aad-1748">mastercard</span></span> 
- <span data-ttu-id="31aad-1749">мастеркардс</span><span class="sxs-lookup"><span data-stu-id="31aad-1749">mastercards</span></span> 
- <span data-ttu-id="31aad-1750">MC</span><span class="sxs-lookup"><span data-stu-id="31aad-1750">mc</span></span> 
- <span data-ttu-id="31aad-1751">mister cash</span><span class="sxs-lookup"><span data-stu-id="31aad-1751">mister cash</span></span> 
- <span data-ttu-id="31aad-1752">n carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1752">n carta</span></span> 
- <span data-ttu-id="31aad-1753">Корзина "</span><span class="sxs-lookup"><span data-stu-id="31aad-1753">carta</span></span> 
- <span data-ttu-id="31aad-1754">no de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1754">no de tarjeta</span></span> 
- <span data-ttu-id="31aad-1755">no do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1755">no do cartao</span></span> 
- <span data-ttu-id="31aad-1756">no do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1756">no do cartão</span></span> 
- <span data-ttu-id="31aad-1757">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1757">no.</span></span> <span data-ttu-id="31aad-1758">de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1758">de tarjeta</span></span> 
- <span data-ttu-id="31aad-1759">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1759">no.</span></span> <span data-ttu-id="31aad-1760">do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1760">do cartao</span></span> 
- <span data-ttu-id="31aad-1761">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1761">no.</span></span> <span data-ttu-id="31aad-1762">do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1762">do cartão</span></span> 
- <span data-ttu-id="31aad-1763">nr carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1763">nr carta</span></span> 
- <span data-ttu-id="31aad-1764">НР.</span><span class="sxs-lookup"><span data-stu-id="31aad-1764">nr.</span></span> <span data-ttu-id="31aad-1765">Корзина "</span><span class="sxs-lookup"><span data-stu-id="31aad-1765">carta</span></span> 
- <span data-ttu-id="31aad-1766">numeri di scheda</span><span class="sxs-lookup"><span data-stu-id="31aad-1766">numeri di scheda</span></span> 
- <span data-ttu-id="31aad-1767">numero carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1767">numero carta</span></span> 
- <span data-ttu-id="31aad-1768">numero de cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1768">numero de cartao</span></span> 
- <span data-ttu-id="31aad-1769">numero de carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1769">numero de carte</span></span> 
- <span data-ttu-id="31aad-1770">numero de cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1770">numero de cartão</span></span> 
- <span data-ttu-id="31aad-1771">numero de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1771">numero de tarjeta</span></span>
- <span data-ttu-id="31aad-1772">numero della carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1772">numero della carta</span></span> 
- <span data-ttu-id="31aad-1773">numero di carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1773">numero di carta</span></span> 
- <span data-ttu-id="31aad-1774">numero di scheda</span><span class="sxs-lookup"><span data-stu-id="31aad-1774">numero di scheda</span></span> 
- <span data-ttu-id="31aad-1775">numero do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1775">numero do cartao</span></span> 
- <span data-ttu-id="31aad-1776">numero do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1776">numero do cartão</span></span> 
- <span data-ttu-id="31aad-1777">numéro de carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1777">numéro de carte</span></span> 
- <span data-ttu-id="31aad-1778">nº carta</span><span class="sxs-lookup"><span data-stu-id="31aad-1778">nº carta</span></span> 
- <span data-ttu-id="31aad-1779">nº de carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1779">nº de carte</span></span> 
- <span data-ttu-id="31aad-1780">nº de la carte</span><span class="sxs-lookup"><span data-stu-id="31aad-1780">nº de la carte</span></span> 
- <span data-ttu-id="31aad-1781">nº de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1781">nº de tarjeta</span></span> 
- <span data-ttu-id="31aad-1782">nº do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1782">nº do cartao</span></span> 
- <span data-ttu-id="31aad-1783">nº do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1783">nº do cartão</span></span> 
- <span data-ttu-id="31aad-1784">n º.</span><span class="sxs-lookup"><span data-stu-id="31aad-1784">nº.</span></span> <span data-ttu-id="31aad-1785">do cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1785">do cartão</span></span> 
- <span data-ttu-id="31aad-1786">número de cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1786">número de cartao</span></span> 
- <span data-ttu-id="31aad-1787">número de cartão</span><span class="sxs-lookup"><span data-stu-id="31aad-1787">número de cartão</span></span> 
- <span data-ttu-id="31aad-1788">número de tarjeta</span><span class="sxs-lookup"><span data-stu-id="31aad-1788">número de tarjeta</span></span> 
- <span data-ttu-id="31aad-1789">número do cartao</span><span class="sxs-lookup"><span data-stu-id="31aad-1789">número do cartao</span></span> 
- <span data-ttu-id="31aad-1790">scheda dell'assegno</span><span class="sxs-lookup"><span data-stu-id="31aad-1790">scheda dell'assegno</span></span> 
- <span data-ttu-id="31aad-1791">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="31aad-1791">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="31aad-1792">scheda dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="31aad-1792">scheda dell'atmosfera</span></span> 
- <span data-ttu-id="31aad-1793">scheda della banca</span><span class="sxs-lookup"><span data-stu-id="31aad-1793">scheda della banca</span></span> 
- <span data-ttu-id="31aad-1794">scheda di controllo</span><span class="sxs-lookup"><span data-stu-id="31aad-1794">scheda di controllo</span></span> 
- <span data-ttu-id="31aad-1795">scheda di debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1795">scheda di debito</span></span> 
- <span data-ttu-id="31aad-1796">scheda matrice</span><span class="sxs-lookup"><span data-stu-id="31aad-1796">scheda matrice</span></span> 
- <span data-ttu-id="31aad-1797">schede dell'atmosfera</span><span class="sxs-lookup"><span data-stu-id="31aad-1797">schede dell'atmosfera</span></span> 
- <span data-ttu-id="31aad-1798">schede di controllo</span><span class="sxs-lookup"><span data-stu-id="31aad-1798">schede di controllo</span></span> 
- <span data-ttu-id="31aad-1799">schede di debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1799">schede di debito</span></span> 
- <span data-ttu-id="31aad-1800">schede matrici</span><span class="sxs-lookup"><span data-stu-id="31aad-1800">schede matrici</span></span> 
- <span data-ttu-id="31aad-1801">scoprono la scheda</span><span class="sxs-lookup"><span data-stu-id="31aad-1801">scoprono la scheda</span></span> 
- <span data-ttu-id="31aad-1802">scoprono le schede</span><span class="sxs-lookup"><span data-stu-id="31aad-1802">scoprono le schede</span></span> 
- <span data-ttu-id="31aad-1803">ОС</span><span class="sxs-lookup"><span data-stu-id="31aad-1803">solo</span></span> 
- <span data-ttu-id="31aad-1804">supporti di scheda</span><span class="sxs-lookup"><span data-stu-id="31aad-1804">supporti di scheda</span></span> 
- <span data-ttu-id="31aad-1805">supporto di scheda</span><span class="sxs-lookup"><span data-stu-id="31aad-1805">supporto di scheda</span></span> 
- <span data-ttu-id="31aad-1806">отключен</span><span class="sxs-lookup"><span data-stu-id="31aad-1806">switch</span></span> 
- <span data-ttu-id="31aad-1807">tarjeta atm</span><span class="sxs-lookup"><span data-stu-id="31aad-1807">tarjeta atm</span></span> 
- <span data-ttu-id="31aad-1808">tarjeta credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1808">tarjeta credito</span></span> 
- <span data-ttu-id="31aad-1809">tarjeta de atm</span><span class="sxs-lookup"><span data-stu-id="31aad-1809">tarjeta de atm</span></span> 
- <span data-ttu-id="31aad-1810">tarjeta de credito</span><span class="sxs-lookup"><span data-stu-id="31aad-1810">tarjeta de credito</span></span> 
- <span data-ttu-id="31aad-1811">tarjeta de debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1811">tarjeta de debito</span></span> 
- <span data-ttu-id="31aad-1812">tarjeta debito</span><span class="sxs-lookup"><span data-stu-id="31aad-1812">tarjeta debito</span></span> 
- <span data-ttu-id="31aad-1813">tarjeta no</span><span class="sxs-lookup"><span data-stu-id="31aad-1813">tarjeta no</span></span>
- <span data-ttu-id="31aad-1814">таржетахабиенте</span><span class="sxs-lookup"><span data-stu-id="31aad-1814">tarjetahabiente</span></span> 
- <span data-ttu-id="31aad-1815">tipo della scheda</span><span class="sxs-lookup"><span data-stu-id="31aad-1815">tipo della scheda</span></span> 
- <span data-ttu-id="31aad-1816">ufficio giapponese della</span><span class="sxs-lookup"><span data-stu-id="31aad-1816">ufficio giapponese della</span></span> 
- <span data-ttu-id="31aad-1817">счеда</span><span class="sxs-lookup"><span data-stu-id="31aad-1817">scheda</span></span> 
- <span data-ttu-id="31aad-1818">v pay</span><span class="sxs-lookup"><span data-stu-id="31aad-1818">v pay</span></span> 
- <span data-ttu-id="31aad-1819">v — оплата</span><span class="sxs-lookup"><span data-stu-id="31aad-1819">v-pay</span></span> 
- <span data-ttu-id="31aad-1820">Visa</span><span class="sxs-lookup"><span data-stu-id="31aad-1820">visa</span></span> 
- <span data-ttu-id="31aad-1821">visa plus</span><span class="sxs-lookup"><span data-stu-id="31aad-1821">visa plus</span></span> 
- <span data-ttu-id="31aad-1822">visa electron</span><span class="sxs-lookup"><span data-stu-id="31aad-1822">visa electron</span></span> 
- <span data-ttu-id="31aad-1823">висто</span><span class="sxs-lookup"><span data-stu-id="31aad-1823">visto</span></span> 
- <span data-ttu-id="31aad-1824">висум</span><span class="sxs-lookup"><span data-stu-id="31aad-1824">visum</span></span> 
- <span data-ttu-id="31aad-1825">впай</span><span class="sxs-lookup"><span data-stu-id="31aad-1825">vpay</span></span>   

#### <a name="keyword_card_security_terms_dict"></a><span data-ttu-id="31aad-1826">Keyword_card_security_terms_dict</span><span class="sxs-lookup"><span data-stu-id="31aad-1826">Keyword_card_security_terms_dict</span></span>

- <span data-ttu-id="31aad-1827">card identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-1827">card identification number</span></span>
- <span data-ttu-id="31aad-1828">card verification</span><span class="sxs-lookup"><span data-stu-id="31aad-1828">card verification</span></span> 
- <span data-ttu-id="31aad-1829">cardi la verifica</span><span class="sxs-lookup"><span data-stu-id="31aad-1829">cardi la verifica</span></span> 
- <span data-ttu-id="31aad-1830">cid</span><span class="sxs-lookup"><span data-stu-id="31aad-1830">cid</span></span> 
- <span data-ttu-id="31aad-1831">cod seg</span><span class="sxs-lookup"><span data-stu-id="31aad-1831">cod seg</span></span> 
- <span data-ttu-id="31aad-1832">cod seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1832">cod seguranca</span></span> 
- <span data-ttu-id="31aad-1833">cod segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1833">cod segurança</span></span> 
- <span data-ttu-id="31aad-1834">cod sicurezza</span><span class="sxs-lookup"><span data-stu-id="31aad-1834">cod sicurezza</span></span> 
- <span data-ttu-id="31aad-1835">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1835">cod.</span></span> <span data-ttu-id="31aad-1836">сег</span><span class="sxs-lookup"><span data-stu-id="31aad-1836">seg</span></span> 
- <span data-ttu-id="31aad-1837">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1837">cod.</span></span> <span data-ttu-id="31aad-1838">сегуранка</span><span class="sxs-lookup"><span data-stu-id="31aad-1838">seguranca</span></span> 
- <span data-ttu-id="31aad-1839">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1839">cod.</span></span> <span data-ttu-id="31aad-1840">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="31aad-1840">segurança</span></span> 
- <span data-ttu-id="31aad-1841">наложен.</span><span class="sxs-lookup"><span data-stu-id="31aad-1841">cod.</span></span> <span data-ttu-id="31aad-1842">сикурезза</span><span class="sxs-lookup"><span data-stu-id="31aad-1842">sicurezza</span></span> 
- <span data-ttu-id="31aad-1843">codice di sicurezza</span><span class="sxs-lookup"><span data-stu-id="31aad-1843">codice di sicurezza</span></span> 
- <span data-ttu-id="31aad-1844">codice di verifica</span><span class="sxs-lookup"><span data-stu-id="31aad-1844">codice di verifica</span></span> 
- <span data-ttu-id="31aad-1845">кодиго</span><span class="sxs-lookup"><span data-stu-id="31aad-1845">codigo</span></span> 
- <span data-ttu-id="31aad-1846">codigo de seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1846">codigo de seguranca</span></span> 
- <span data-ttu-id="31aad-1847">codigo de segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1847">codigo de segurança</span></span> 
- <span data-ttu-id="31aad-1848">криттограмма</span><span class="sxs-lookup"><span data-stu-id="31aad-1848">crittogramma</span></span> 
- <span data-ttu-id="31aad-1849">криптограм</span><span class="sxs-lookup"><span data-stu-id="31aad-1849">cryptogram</span></span> 
- <span data-ttu-id="31aad-1850">криптограмме</span><span class="sxs-lookup"><span data-stu-id="31aad-1850">cryptogramme</span></span> 
- <span data-ttu-id="31aad-1851">cv2</span><span class="sxs-lookup"><span data-stu-id="31aad-1851">cv2</span></span> 
- <span data-ttu-id="31aad-1852">квк</span><span class="sxs-lookup"><span data-stu-id="31aad-1852">cvc</span></span> 
- <span data-ttu-id="31aad-1853">cvc2</span><span class="sxs-lookup"><span data-stu-id="31aad-1853">cvc2</span></span> 
- <span data-ttu-id="31aad-1854">квн</span><span class="sxs-lookup"><span data-stu-id="31aad-1854">cvn</span></span> 
- <span data-ttu-id="31aad-1855">квв</span><span class="sxs-lookup"><span data-stu-id="31aad-1855">cvv</span></span> 
- <span data-ttu-id="31aad-1856">cvv2</span><span class="sxs-lookup"><span data-stu-id="31aad-1856">cvv2</span></span> 
- <span data-ttu-id="31aad-1857">cód seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1857">cód seguranca</span></span> 
- <span data-ttu-id="31aad-1858">cód segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1858">cód segurança</span></span> 
- <span data-ttu-id="31aad-1859">кóд.</span><span class="sxs-lookup"><span data-stu-id="31aad-1859">cód.</span></span> <span data-ttu-id="31aad-1860">сегуранка</span><span class="sxs-lookup"><span data-stu-id="31aad-1860">seguranca</span></span> 
- <span data-ttu-id="31aad-1861">кóд.</span><span class="sxs-lookup"><span data-stu-id="31aad-1861">cód.</span></span> <span data-ttu-id="31aad-1862">сегуранçа</span><span class="sxs-lookup"><span data-stu-id="31aad-1862">segurança</span></span> 
- <span data-ttu-id="31aad-1863">кóдиго</span><span class="sxs-lookup"><span data-stu-id="31aad-1863">código</span></span> 
- <span data-ttu-id="31aad-1864">código de seguranca</span><span class="sxs-lookup"><span data-stu-id="31aad-1864">código de seguranca</span></span> 
- <span data-ttu-id="31aad-1865">código de segurança</span><span class="sxs-lookup"><span data-stu-id="31aad-1865">código de segurança</span></span> 
- <span data-ttu-id="31aad-1866">de kaart controle</span><span class="sxs-lookup"><span data-stu-id="31aad-1866">de kaart controle</span></span> 
- <span data-ttu-id="31aad-1867">geeft nr uit</span><span class="sxs-lookup"><span data-stu-id="31aad-1867">geeft nr uit</span></span> 
- <span data-ttu-id="31aad-1868">issue no</span><span class="sxs-lookup"><span data-stu-id="31aad-1868">issue no</span></span> 
- <span data-ttu-id="31aad-1869">issue number</span><span class="sxs-lookup"><span data-stu-id="31aad-1869">issue number</span></span> 
- <span data-ttu-id="31aad-1870">каартидентификатиенуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1870">kaartidentificatienummer</span></span> 
- <span data-ttu-id="31aad-1871">кредиткартенпруфнуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1871">kreditkartenprufnummer</span></span> 
- <span data-ttu-id="31aad-1872">кредиткартенпрüфнуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1872">kreditkartenprüfnummer</span></span> 
- <span data-ttu-id="31aad-1873">квестиеаантал</span><span class="sxs-lookup"><span data-stu-id="31aad-1873">kwestieaantal</span></span> 
- <span data-ttu-id="31aad-1874">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1874">no.</span></span> <span data-ttu-id="31aad-1875">делл'едизионе</span><span class="sxs-lookup"><span data-stu-id="31aad-1875">dell'edizione</span></span> 
- <span data-ttu-id="31aad-1876">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-1876">no.</span></span> <span data-ttu-id="31aad-1877">di sicurezza</span><span class="sxs-lookup"><span data-stu-id="31aad-1877">di sicurezza</span></span> 
- <span data-ttu-id="31aad-1878">numero de securite</span><span class="sxs-lookup"><span data-stu-id="31aad-1878">numero de securite</span></span> 
- <span data-ttu-id="31aad-1879">numero de verificacao</span><span class="sxs-lookup"><span data-stu-id="31aad-1879">numero de verificacao</span></span> 
- <span data-ttu-id="31aad-1880">numero dell'edizione</span><span class="sxs-lookup"><span data-stu-id="31aad-1880">numero dell'edizione</span></span> 
- <span data-ttu-id="31aad-1881">numero di identificazione della</span><span class="sxs-lookup"><span data-stu-id="31aad-1881">numero di identificazione della</span></span> 
- <span data-ttu-id="31aad-1882">счеда</span><span class="sxs-lookup"><span data-stu-id="31aad-1882">scheda</span></span> 
- <span data-ttu-id="31aad-1883">numero di sicurezza</span><span class="sxs-lookup"><span data-stu-id="31aad-1883">numero di sicurezza</span></span> 
- <span data-ttu-id="31aad-1884">numero van veiligheid</span><span class="sxs-lookup"><span data-stu-id="31aad-1884">numero van veiligheid</span></span> 
- <span data-ttu-id="31aad-1885">numéro de sécurité</span><span class="sxs-lookup"><span data-stu-id="31aad-1885">numéro de sécurité</span></span> 
- <span data-ttu-id="31aad-1886">nº autorizzazione</span><span class="sxs-lookup"><span data-stu-id="31aad-1886">nº autorizzazione</span></span> 
- <span data-ttu-id="31aad-1887">número de verificação</span><span class="sxs-lookup"><span data-stu-id="31aad-1887">número de verificação</span></span> 
- <span data-ttu-id="31aad-1888">perno il blocco</span><span class="sxs-lookup"><span data-stu-id="31aad-1888">perno il blocco</span></span> 
- <span data-ttu-id="31aad-1889">pin block</span><span class="sxs-lookup"><span data-stu-id="31aad-1889">pin block</span></span> 
- <span data-ttu-id="31aad-1890">пруфзиффер</span><span class="sxs-lookup"><span data-stu-id="31aad-1890">prufziffer</span></span> 
- <span data-ttu-id="31aad-1891">прüфзиффер</span><span class="sxs-lookup"><span data-stu-id="31aad-1891">prüfziffer</span></span> 
- <span data-ttu-id="31aad-1892">security code</span><span class="sxs-lookup"><span data-stu-id="31aad-1892">security code</span></span> 
- <span data-ttu-id="31aad-1893">security no</span><span class="sxs-lookup"><span data-stu-id="31aad-1893">security no</span></span> 
- <span data-ttu-id="31aad-1894">security number</span><span class="sxs-lookup"><span data-stu-id="31aad-1894">security number</span></span> 
- <span data-ttu-id="31aad-1895">sicherheits kode</span><span class="sxs-lookup"><span data-stu-id="31aad-1895">sicherheits kode</span></span> 
- <span data-ttu-id="31aad-1896">сичерхеитскоде</span><span class="sxs-lookup"><span data-stu-id="31aad-1896">sicherheitscode</span></span> 
- <span data-ttu-id="31aad-1897">сичерхеитснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1897">sicherheitsnummer</span></span> 
- <span data-ttu-id="31aad-1898">спелдблок</span><span class="sxs-lookup"><span data-stu-id="31aad-1898">speldblok</span></span> 
- <span data-ttu-id="31aad-1899">veiligheid nr</span><span class="sxs-lookup"><span data-stu-id="31aad-1899">veiligheid nr</span></span> 
- <span data-ttu-id="31aad-1900">веилигхеидсаантал</span><span class="sxs-lookup"><span data-stu-id="31aad-1900">veiligheidsaantal</span></span> 
- <span data-ttu-id="31aad-1901">веилигхеидскоде</span><span class="sxs-lookup"><span data-stu-id="31aad-1901">veiligheidscode</span></span> 
- <span data-ttu-id="31aad-1902">веилигхеидснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1902">veiligheidsnummer</span></span> 
- <span data-ttu-id="31aad-1903">верфаллдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1903">verfalldatum</span></span> 

#### <a name="keyword_card_expiration_terms_dict"></a><span data-ttu-id="31aad-1904">Keyword_card_expiration_terms_dict</span><span class="sxs-lookup"><span data-stu-id="31aad-1904">Keyword_card_expiration_terms_dict</span></span>

- <span data-ttu-id="31aad-1905">аблауф</span><span class="sxs-lookup"><span data-stu-id="31aad-1905">ablauf</span></span> 
- <span data-ttu-id="31aad-1906">data de expiracao</span><span class="sxs-lookup"><span data-stu-id="31aad-1906">data de expiracao</span></span> 
- <span data-ttu-id="31aad-1907">data de expiração</span><span class="sxs-lookup"><span data-stu-id="31aad-1907">data de expiração</span></span> 
- <span data-ttu-id="31aad-1908">data del exp</span><span class="sxs-lookup"><span data-stu-id="31aad-1908">data del exp</span></span> 
- <span data-ttu-id="31aad-1909">data di exp</span><span class="sxs-lookup"><span data-stu-id="31aad-1909">data di exp</span></span> 
- <span data-ttu-id="31aad-1910">data di scadenza</span><span class="sxs-lookup"><span data-stu-id="31aad-1910">data di scadenza</span></span> 
- <span data-ttu-id="31aad-1911">data em que expira</span><span class="sxs-lookup"><span data-stu-id="31aad-1911">data em que expira</span></span> 
- <span data-ttu-id="31aad-1912">data scad</span><span class="sxs-lookup"><span data-stu-id="31aad-1912">data scad</span></span> 
- <span data-ttu-id="31aad-1913">data scadenza</span><span class="sxs-lookup"><span data-stu-id="31aad-1913">data scadenza</span></span> 
- <span data-ttu-id="31aad-1914">date de validité</span><span class="sxs-lookup"><span data-stu-id="31aad-1914">date de validité</span></span> 
- <span data-ttu-id="31aad-1915">datum afloop</span><span class="sxs-lookup"><span data-stu-id="31aad-1915">datum afloop</span></span> 
- <span data-ttu-id="31aad-1916">datum van exp</span><span class="sxs-lookup"><span data-stu-id="31aad-1916">datum van exp</span></span> 
- <span data-ttu-id="31aad-1917">de afloop</span><span class="sxs-lookup"><span data-stu-id="31aad-1917">de afloop</span></span> 
- <span data-ttu-id="31aad-1918">еспира</span><span class="sxs-lookup"><span data-stu-id="31aad-1918">espira</span></span> 
- <span data-ttu-id="31aad-1919">еспира</span><span class="sxs-lookup"><span data-stu-id="31aad-1919">espira</span></span> 
- <span data-ttu-id="31aad-1920">exp date</span><span class="sxs-lookup"><span data-stu-id="31aad-1920">exp date</span></span> 
- <span data-ttu-id="31aad-1921">exp datum</span><span class="sxs-lookup"><span data-stu-id="31aad-1921">exp datum</span></span> 
- <span data-ttu-id="31aad-1922">срока действия</span><span class="sxs-lookup"><span data-stu-id="31aad-1922">expiration</span></span> 
- <span data-ttu-id="31aad-1923">истекает</span><span class="sxs-lookup"><span data-stu-id="31aad-1923">expire</span></span> 
- <span data-ttu-id="31aad-1924">истекает</span><span class="sxs-lookup"><span data-stu-id="31aad-1924">expires</span></span> 
- <span data-ttu-id="31aad-1925">окончания срока действия</span><span class="sxs-lookup"><span data-stu-id="31aad-1925">expiry</span></span> 
- <span data-ttu-id="31aad-1926">fecha de expiracion</span><span class="sxs-lookup"><span data-stu-id="31aad-1926">fecha de expiracion</span></span> 
- <span data-ttu-id="31aad-1927">fecha de venc</span><span class="sxs-lookup"><span data-stu-id="31aad-1927">fecha de venc</span></span> 
- <span data-ttu-id="31aad-1928">gultig bis</span><span class="sxs-lookup"><span data-stu-id="31aad-1928">gultig bis</span></span> 
- <span data-ttu-id="31aad-1929">гултигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1929">gultigkeitsdatum</span></span> 
- <span data-ttu-id="31aad-1930">gültig bis</span><span class="sxs-lookup"><span data-stu-id="31aad-1930">gültig bis</span></span> 
- <span data-ttu-id="31aad-1931">гüлтигкеитсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1931">gültigkeitsdatum</span></span> 
- <span data-ttu-id="31aad-1932">la scadenza</span><span class="sxs-lookup"><span data-stu-id="31aad-1932">la scadenza</span></span> 
- <span data-ttu-id="31aad-1933">скаденза</span><span class="sxs-lookup"><span data-stu-id="31aad-1933">scadenza</span></span> 
- <span data-ttu-id="31aad-1934">валабле</span><span class="sxs-lookup"><span data-stu-id="31aad-1934">valable</span></span> 
- <span data-ttu-id="31aad-1935">валидаде</span><span class="sxs-lookup"><span data-stu-id="31aad-1935">validade</span></span> 
- <span data-ttu-id="31aad-1936">valido hasta</span><span class="sxs-lookup"><span data-stu-id="31aad-1936">valido hasta</span></span> 
- <span data-ttu-id="31aad-1937">валор</span><span class="sxs-lookup"><span data-stu-id="31aad-1937">valor</span></span> 
- <span data-ttu-id="31aad-1938">венк</span><span class="sxs-lookup"><span data-stu-id="31aad-1938">venc</span></span> 
- <span data-ttu-id="31aad-1939">венЦименто</span><span class="sxs-lookup"><span data-stu-id="31aad-1939">vencimento</span></span> 
- <span data-ttu-id="31aad-1940">венЦимиенто</span><span class="sxs-lookup"><span data-stu-id="31aad-1940">vencimiento</span></span> 
- <span data-ttu-id="31aad-1941">верлупт</span><span class="sxs-lookup"><span data-stu-id="31aad-1941">verloopt</span></span> 
- <span data-ttu-id="31aad-1942">вервалдаг</span><span class="sxs-lookup"><span data-stu-id="31aad-1942">vervaldag</span></span> 
- <span data-ttu-id="31aad-1943">вервалдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-1943">vervaldatum</span></span> 
- <span data-ttu-id="31aad-1944">вто</span><span class="sxs-lookup"><span data-stu-id="31aad-1944">vto</span></span> 
- <span data-ttu-id="31aad-1945">válido hasta</span><span class="sxs-lookup"><span data-stu-id="31aad-1945">válido hasta</span></span> 
   
## <a name="eu-drivers-license-number"></a><span data-ttu-id="31aad-1946">Номер водительского удостоверения для драйвера ЕС</span><span class="sxs-lookup"><span data-stu-id="31aad-1946">EU Driver's License Number</span></span>

<span data-ttu-id="31aad-1947">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).</span><span class="sxs-lookup"><span data-stu-id="31aad-1947">To learn more, see [EU Driver's License Number sensitive information type](eu-driver-s-license-number.md).</span></span>
  
## <a name="eu-national-identification-number"></a><span data-ttu-id="31aad-1948">Национальный идентификационный номер ЕС</span><span class="sxs-lookup"><span data-stu-id="31aad-1948">EU National Identification Number</span></span>

<span data-ttu-id="31aad-1949">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационного номера ЕС](eu-national-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="31aad-1949">To learn more, see [EU National Identification Number sensitive information type](eu-national-identification-number.md).</span></span>
  
## <a name="eu-passport-number"></a><span data-ttu-id="31aad-1950">Номер паспорта ЕС</span><span class="sxs-lookup"><span data-stu-id="31aad-1950">EU Passport Number</span></span>

<span data-ttu-id="31aad-1951">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).</span><span class="sxs-lookup"><span data-stu-id="31aad-1951">To learn more, see [EU Passport Number sensitive information type](eu-passport-number.md).</span></span>
  
## <a name="eu-social-security-number-or-equivalent-id"></a><span data-ttu-id="31aad-1952">Номер социального страхования ЕС или эквивалентный идентификатор</span><span class="sxs-lookup"><span data-stu-id="31aad-1952">EU Social Security Number or Equivalent ID</span></span>

<span data-ttu-id="31aad-1953">Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).</span><span class="sxs-lookup"><span data-stu-id="31aad-1953">To learn more, see [EU Social Security Number or Equivalent ID sensitive information type](eu-social-security-number-or-equivalent-id.md).</span></span>
  
## <a name="eu-tax-identification-number"></a><span data-ttu-id="31aad-1954">Идентификационный номер налогоплательщика ЕС</span><span class="sxs-lookup"><span data-stu-id="31aad-1954">EU Tax Identification Number</span></span>

<span data-ttu-id="31aad-1955">Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогового кода ЕС](eu-tax-identification-number.md).</span><span class="sxs-lookup"><span data-stu-id="31aad-1955">To learn more, see [EU Tax Identification Number sensitive information type](eu-tax-identification-number.md).</span></span>
  
## <a name="finland-national-id"></a><span data-ttu-id="31aad-1956">Национальный идентификатор, Финляндия</span><span class="sxs-lookup"><span data-stu-id="31aad-1956">Finland National ID</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1957">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1957">Format</span></span>

<span data-ttu-id="31aad-1958">Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.</span><span class="sxs-lookup"><span data-stu-id="31aad-1958">Six digits plus a character indicating a century plus three digits plus a check digit</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1959">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1959">Pattern</span></span>

<span data-ttu-id="31aad-1960">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="31aad-1960">Pattern must include all of the following:</span></span>
- <span data-ttu-id="31aad-1961">Шесть цифр в формате ДДММГГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="31aad-1961">Six digits in the format format DDMMYY which are a date of birth</span></span> 
- <span data-ttu-id="31aad-1962">Маркер века (символы "-" и "+" или буква "a")</span><span class="sxs-lookup"><span data-stu-id="31aad-1962">Century marker (either '-', '+' or 'a')</span></span> 
- <span data-ttu-id="31aad-1963">Трехзначный личный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="31aad-1963">Three-digit personal identification number</span></span> 
- <span data-ttu-id="31aad-1964">Цифра или буква (без учета регистра) — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-1964">A digit or letter (case insensitive) which is a check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1965">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1965">Checksum</span></span>

<span data-ttu-id="31aad-1966">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-1966">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1967">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1967">Definition</span></span>

<span data-ttu-id="31aad-1968">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1968">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1969">функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-1969">The function Func_finnish_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1970">находится ключевое слово из Keyword_finnish_national_id;</span><span class="sxs-lookup"><span data-stu-id="31aad-1970">A keyword from Keyword_finnish_national_id is found.</span></span>
- <span data-ttu-id="31aad-1971">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-1971">The checksum passes.</span></span>

```xml
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-1972">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1972">Keywords</span></span>

- <span data-ttu-id="31aad-1973">Keyword_finnish_national_id</span><span class="sxs-lookup"><span data-stu-id="31aad-1973">Keyword_finnish_national_id</span></span>
- <span data-ttu-id="31aad-1974">сосиаалитурватуннус</span><span class="sxs-lookup"><span data-stu-id="31aad-1974">Sosiaaliturvatunnus</span></span>
- <span data-ttu-id="31aad-1975">SOTU Henkilötunnus HETU</span><span class="sxs-lookup"><span data-stu-id="31aad-1975">SOTU Henkilötunnus HETU</span></span>
- <span data-ttu-id="31aad-1976">персонбетеккнинг</span><span class="sxs-lookup"><span data-stu-id="31aad-1976">Personbeteckning</span></span>
- <span data-ttu-id="31aad-1977">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-1977">Personnummer</span></span>
   
## <a name="finland-passport-number"></a><span data-ttu-id="31aad-1978">Номер паспорта для Финляндии</span><span class="sxs-lookup"><span data-stu-id="31aad-1978">Finland Passport Number</span></span>

<span data-ttu-id="31aad-1979">Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Regex_finland_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-1979">Format Combination of nine letters and digits Pattern Combination of nine letters and digits: Two letters (not case sensitive) Seven digits Checksum No Definition A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The regular expression Regex_finland_passport_number finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-1980">находится ключевое слово из Keyword_finland_passport_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-1980">A keyword from Keyword_finland_passport_number is found.</span></span>
<!-- Finland Passport Number -->
<span data-ttu-id="31aad-1981"><Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="31aad-1981"></span></span>
<span data-ttu-id="31aad-1982">Ключевые слова Keyword_finland_passport_number Passport Пасси</span><span class="sxs-lookup"><span data-stu-id="31aad-1982">Keywords Keyword_finland_passport_number Passport Passi</span></span>
   
## <a name="france-drivers-license-number"></a><span data-ttu-id="31aad-1983">Номер водительского удостоверения для Франции</span><span class="sxs-lookup"><span data-stu-id="31aad-1983">France Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-1984">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-1984">Format</span></span>

<span data-ttu-id="31aad-1985">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-1985">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-1986">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-1986">Pattern</span></span>

<span data-ttu-id="31aad-1987">12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.</span><span class="sxs-lookup"><span data-stu-id="31aad-1987">12 digits with validation to discount similar patterns such as French telephone numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-1988">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-1988">Checksum</span></span>

<span data-ttu-id="31aad-1989">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-1989">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-1990">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-1990">Definition</span></span>

<span data-ttu-id="31aad-1991">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-1991">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-1992">Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-1992">The function Func_french_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-1993">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-1993">At least one of the following is true:</span></span>
- <span data-ttu-id="31aad-1994">найдено ключевое слово из Keyword_french_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="31aad-1994">A keyword from Keyword_french_drivers_license is found.</span></span>
- <span data-ttu-id="31aad-1995">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-1995">The function Func_eu_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-1996">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-1996">Keywords</span></span>

#### <a name="keyword_french_drivers_license"></a><span data-ttu-id="31aad-1997">Keyword_french_drivers_license</span><span class="sxs-lookup"><span data-stu-id="31aad-1997">Keyword_french_drivers_license</span></span>

- <span data-ttu-id="31aad-1998">drivers licence</span><span class="sxs-lookup"><span data-stu-id="31aad-1998">drivers licence</span></span>
- <span data-ttu-id="31aad-1999">drivers license</span><span class="sxs-lookup"><span data-stu-id="31aad-1999">drivers license</span></span>
- <span data-ttu-id="31aad-2000">driving licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2000">driving licence</span></span>
- <span data-ttu-id="31aad-2001">driving license</span><span class="sxs-lookup"><span data-stu-id="31aad-2001">driving license</span></span>
- <span data-ttu-id="31aad-2002">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="31aad-2002">permis de conduire</span></span>
- <span data-ttu-id="31aad-2003">licence number</span><span class="sxs-lookup"><span data-stu-id="31aad-2003">licence number</span></span>
- <span data-ttu-id="31aad-2004">license number</span><span class="sxs-lookup"><span data-stu-id="31aad-2004">license number</span></span>
- <span data-ttu-id="31aad-2005">licence numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-2005">licence numbers</span></span>
- <span data-ttu-id="31aad-2006">license numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-2006">license numbers</span></span>

## <a name="france-national-id-card-cni"></a><span data-ttu-id="31aad-2007">Номер внутреннего удостоверения личности для Франции (CNI)</span><span class="sxs-lookup"><span data-stu-id="31aad-2007">France National ID Card (CNI)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2008">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2008">Format</span></span>

<span data-ttu-id="31aad-2009">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2009">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2010">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2010">Pattern</span></span>

<span data-ttu-id="31aad-2011">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2011">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2012">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2012">Checksum</span></span>

<span data-ttu-id="31aad-2013">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2013">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2014">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2014">Definition</span></span>

<span data-ttu-id="31aad-2015">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2015">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2016">регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-2016">The regular expression Regex_france_cni finds content that matches the pattern.</span></span>

```xml
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2017">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2017">Keywords</span></span>

<span data-ttu-id="31aad-2018">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2018">None</span></span>
   
## <a name="france-passport-number"></a><span data-ttu-id="31aad-2019">Номер паспорта гражданина Франции</span><span class="sxs-lookup"><span data-stu-id="31aad-2019">France Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2020">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2020">Format</span></span>

<span data-ttu-id="31aad-2021">Девять цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="31aad-2021">Nine digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2022">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2022">Pattern</span></span>

<span data-ttu-id="31aad-2023">Девять цифр и букв</span><span class="sxs-lookup"><span data-stu-id="31aad-2023">Nine digits and letters:</span></span>
- <span data-ttu-id="31aad-2024">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2024">Two digits</span></span> 
- <span data-ttu-id="31aad-2025">Две буквы (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-2025">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2026">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-2026">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2027">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2027">Checksum</span></span>

<span data-ttu-id="31aad-2028">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2028">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2029">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2029">Definition</span></span>

<span data-ttu-id="31aad-2030">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2030">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2031">функция Func_fr_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2031">The function Func_fr_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2032">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="31aad-2032">A keyword from Keyword_passport is found.</span></span>

```xml
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2033">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2033">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="31aad-2034">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-2034">Keyword_passport</span></span>

- <span data-ttu-id="31aad-2035">Passport Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2035">Passport Number</span></span>
- <span data-ttu-id="31aad-2036">Passport No</span><span class="sxs-lookup"><span data-stu-id="31aad-2036">Passport No</span></span>
- <span data-ttu-id="31aad-2037">Passport#</span><span class="sxs-lookup"><span data-stu-id="31aad-2037">Passport #</span></span>
- <span data-ttu-id="31aad-2038">Службу #</span><span class="sxs-lookup"><span data-stu-id="31aad-2038">Passport#</span></span>
- <span data-ttu-id="31aad-2039">пасспортид</span><span class="sxs-lookup"><span data-stu-id="31aad-2039">PassportID</span></span>
- <span data-ttu-id="31aad-2040">пасспортно</span><span class="sxs-lookup"><span data-stu-id="31aad-2040">Passportno</span></span>
- <span data-ttu-id="31aad-2041">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-2041">passportnumber</span></span>
- <span data-ttu-id="31aad-2042">パスポート</span><span class="sxs-lookup"><span data-stu-id="31aad-2042">パスポート</span></span>
- <span data-ttu-id="31aad-2043">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2043">パスポート番号</span></span>
- <span data-ttu-id="31aad-2044">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="31aad-2044">パスポートのNum</span></span>
- <span data-ttu-id="31aad-2045">パスポート＃</span><span class="sxs-lookup"><span data-stu-id="31aad-2045">パスポート ＃</span></span> 
- <span data-ttu-id="31aad-2046">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="31aad-2046">Numéro de passeport</span></span>
- <span data-ttu-id="31aad-2047">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="31aad-2047">Passeport n °</span></span>
- <span data-ttu-id="31aad-2048">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="31aad-2048">Passeport Non</span></span>
- <span data-ttu-id="31aad-2049">Passeport#</span><span class="sxs-lookup"><span data-stu-id="31aad-2049">Passeport #</span></span>
- <span data-ttu-id="31aad-2050">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="31aad-2050">Passeport#</span></span>
- <span data-ttu-id="31aad-2051">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="31aad-2051">PasseportNon</span></span>
- <span data-ttu-id="31aad-2052">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="31aad-2052">Passeportn °</span></span>

      
## <a name="france-social-security-number-insee"></a><span data-ttu-id="31aad-2053">Страховой номер для Франции (INSEE)</span><span class="sxs-lookup"><span data-stu-id="31aad-2053">France Social Security Number (INSEE)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2054">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2054">Format</span></span>

<span data-ttu-id="31aad-2055">15 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2055">15 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2056">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2056">Pattern</span></span>

<span data-ttu-id="31aad-2057">Должен соответствовать одному из двух шаблонов:</span><span class="sxs-lookup"><span data-stu-id="31aad-2057">Must match one of two patterns:</span></span>
- <span data-ttu-id="31aad-2058">13 цифр, за которыми следует пробел, за которым следуют две цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-2058">13 digits followed by a space followed by two digits</span></span><br/>
<span data-ttu-id="31aad-2059">или</span><span class="sxs-lookup"><span data-stu-id="31aad-2059">or</span></span>
- <span data-ttu-id="31aad-2060">15 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2060">15 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2061">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2061">Checksum</span></span>

<span data-ttu-id="31aad-2062">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2062">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2063">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2063">Definition</span></span>

<span data-ttu-id="31aad-2064">Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2064">A DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2065">Функция Func_french_insee или Func_fr_insee находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-2065">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2066">находится ключевое слово из Keyword_fr_insee;</span><span class="sxs-lookup"><span data-stu-id="31aad-2066">A keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="31aad-2067">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2067">The checksum passes.</span></span>

<span data-ttu-id="31aad-2068">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2068">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2069">Функция Func_french_insee или Func_fr_insee находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-2069">The function Func_french_insee or Func_fr_insee finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2070">ни одно ключевое слово из Keyword_fr_insee не находится;</span><span class="sxs-lookup"><span data-stu-id="31aad-2070">No keyword from Keyword_fr_insee is found.</span></span>
- <span data-ttu-id="31aad-2071">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2071">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2072">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2072">Keywords</span></span>

#### <a name="keyword_fr_insee"></a><span data-ttu-id="31aad-2073">Keyword_fr_insee</span><span class="sxs-lookup"><span data-stu-id="31aad-2073">Keyword_fr_insee</span></span>

- <span data-ttu-id="31aad-2074">INSEE</span><span class="sxs-lookup"><span data-stu-id="31aad-2074">insee</span></span>
- <span data-ttu-id="31aad-2075">securité sociale</span><span class="sxs-lookup"><span data-stu-id="31aad-2075">securité sociale</span></span>
- <span data-ttu-id="31aad-2076">securite sociale</span><span class="sxs-lookup"><span data-stu-id="31aad-2076">securite sociale</span></span>
- <span data-ttu-id="31aad-2077">national id</span><span class="sxs-lookup"><span data-stu-id="31aad-2077">national id</span></span>
- <span data-ttu-id="31aad-2078">national identification</span><span class="sxs-lookup"><span data-stu-id="31aad-2078">national identification</span></span>
- <span data-ttu-id="31aad-2079">numéro d'identité</span><span class="sxs-lookup"><span data-stu-id="31aad-2079">numéro d'identité</span></span>
- <span data-ttu-id="31aad-2080">no d'identité</span><span class="sxs-lookup"><span data-stu-id="31aad-2080">no d'identité</span></span>
- <span data-ttu-id="31aad-2081">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-2081">no.</span></span> <span data-ttu-id="31aad-2082">д'идентитé</span><span class="sxs-lookup"><span data-stu-id="31aad-2082">d'identité</span></span>
- <span data-ttu-id="31aad-2083">numero d'identite</span><span class="sxs-lookup"><span data-stu-id="31aad-2083">numero d'identite</span></span>
- <span data-ttu-id="31aad-2084">no d'identite</span><span class="sxs-lookup"><span data-stu-id="31aad-2084">no d'identite</span></span>
- <span data-ttu-id="31aad-2085">Нет.</span><span class="sxs-lookup"><span data-stu-id="31aad-2085">no.</span></span> <span data-ttu-id="31aad-2086">д'идентите</span><span class="sxs-lookup"><span data-stu-id="31aad-2086">d'identite</span></span>
- <span data-ttu-id="31aad-2087">social security number</span><span class="sxs-lookup"><span data-stu-id="31aad-2087">social security number</span></span>
- <span data-ttu-id="31aad-2088">social security code</span><span class="sxs-lookup"><span data-stu-id="31aad-2088">social security code</span></span>
- <span data-ttu-id="31aad-2089">social insurance number</span><span class="sxs-lookup"><span data-stu-id="31aad-2089">social insurance number</span></span>
- <span data-ttu-id="31aad-2090">le numéro d'identification nationale</span><span class="sxs-lookup"><span data-stu-id="31aad-2090">le numéro d'identification nationale</span></span>
- <span data-ttu-id="31aad-2091">d'identité nationale</span><span class="sxs-lookup"><span data-stu-id="31aad-2091">d'identité nationale</span></span>
- <span data-ttu-id="31aad-2092">numéro de sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="31aad-2092">numéro de sécurité sociale</span></span>
- <span data-ttu-id="31aad-2093">le code de la sécurité sociale</span><span class="sxs-lookup"><span data-stu-id="31aad-2093">le code de la sécurité sociale</span></span>
- <span data-ttu-id="31aad-2094">numéro d'assurance sociale</span><span class="sxs-lookup"><span data-stu-id="31aad-2094">numéro d'assurance sociale</span></span>
- <span data-ttu-id="31aad-2095">numéro de sécu</span><span class="sxs-lookup"><span data-stu-id="31aad-2095">numéro de sécu</span></span>
- <span data-ttu-id="31aad-2096">code sécu</span><span class="sxs-lookup"><span data-stu-id="31aad-2096">code sécu</span></span> 
   
## <a name="german-drivers-license-number"></a><span data-ttu-id="31aad-2097">Номер водительского удостоверения для Германии</span><span class="sxs-lookup"><span data-stu-id="31aad-2097">German Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2098">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2098">Format</span></span>

<span data-ttu-id="31aad-2099">Сочетание 11 цифр и букв.</span><span class="sxs-lookup"><span data-stu-id="31aad-2099">Combination of 11 digits and letters</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2100">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2100">Pattern</span></span>

<span data-ttu-id="31aad-2101">11 цифр и букв (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-2101">11 digits and letters (not case sensitive):</span></span>
- <span data-ttu-id="31aad-2102">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="31aad-2102">A digit or letter</span></span> 
- <span data-ttu-id="31aad-2103">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2103">Two digits</span></span> 
- <span data-ttu-id="31aad-2104">Шесть цифр или букв</span><span class="sxs-lookup"><span data-stu-id="31aad-2104">Six digits or letters</span></span> 
- <span data-ttu-id="31aad-2105">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="31aad-2105">A digit</span></span> 
- <span data-ttu-id="31aad-2106">Одна цифра или буква</span><span class="sxs-lookup"><span data-stu-id="31aad-2106">A digit or letter</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2107">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2107">Checksum</span></span>

<span data-ttu-id="31aad-2108">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2108">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2109">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2109">Definition</span></span>

<span data-ttu-id="31aad-2110">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2110">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2111">Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2111">The function Func_german_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2112">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-2112">At least one of the following is true:</span></span>
    - <span data-ttu-id="31aad-2113">найдено ключевое слово из Keyword_german_drivers_license_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-2113">A keyword from Keyword_german_drivers_license_number is found.</span></span>
    - <span data-ttu-id="31aad-2114">найдено ключевое слово из Keyword_german_drivers_license_collaborative;</span><span class="sxs-lookup"><span data-stu-id="31aad-2114">A keyword from Keyword_german_drivers_license_collaborative is found.</span></span>
    - <span data-ttu-id="31aad-2115">найдено ключевое слово из Keyword_german_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="31aad-2115">A keyword from Keyword_german_drivers_license is found.</span></span>
- <span data-ttu-id="31aad-2116">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2116">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2117">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2117">Keywords</span></span>

#### <a name="keyword_german_drivers_license_number"></a><span data-ttu-id="31aad-2118">Keyword_german_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2118">Keyword_german_drivers_license_number</span></span>

- <span data-ttu-id="31aad-2119">фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2119">Führerschein</span></span>
- <span data-ttu-id="31aad-2120">фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2120">Fuhrerschein</span></span>
- <span data-ttu-id="31aad-2121">фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2121">Fuehrerschein</span></span>
- <span data-ttu-id="31aad-2122">фüхрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2122">Führerscheinnummer</span></span>
- <span data-ttu-id="31aad-2123">фухрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2123">Fuhrerscheinnummer</span></span>
- <span data-ttu-id="31aad-2124">фуехрерсчеиннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2124">Fuehrerscheinnummer</span></span>
- <span data-ttu-id="31aad-2125">Фüхрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="31aad-2125">Führerschein-</span></span> 
- <span data-ttu-id="31aad-2126">Фухрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="31aad-2126">Fuhrerschein-</span></span> 
- <span data-ttu-id="31aad-2127">Фуехрерсчеин —</span><span class="sxs-lookup"><span data-stu-id="31aad-2127">Fuehrerschein-</span></span> 
- <span data-ttu-id="31aad-2128">фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="31aad-2128">FührerscheinnummerNr</span></span>
- <span data-ttu-id="31aad-2129">фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="31aad-2129">FuhrerscheinnummerNr</span></span>
- <span data-ttu-id="31aad-2130">фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="31aad-2130">FuehrerscheinnummerNr</span></span>
- <span data-ttu-id="31aad-2131">фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2131">FührerscheinnummerKlasse</span></span>
- <span data-ttu-id="31aad-2132">фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2132">FuhrerscheinnummerKlasse</span></span>
- <span data-ttu-id="31aad-2133">фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2133">FuehrerscheinnummerKlasse</span></span>
- <span data-ttu-id="31aad-2134">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="31aad-2134">Führerschein- Nr</span></span>
- <span data-ttu-id="31aad-2135">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="31aad-2135">Fuhrerschein- Nr</span></span>
- <span data-ttu-id="31aad-2136">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="31aad-2136">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="31aad-2137">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="31aad-2137">Führerschein- Klasse</span></span> 
- <span data-ttu-id="31aad-2138">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="31aad-2138">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="31aad-2139">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="31aad-2139">Fuehrerschein- Klasse</span></span>
- <span data-ttu-id="31aad-2140">фüхрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="31aad-2140">FührerscheinnummerNr</span></span> 
- <span data-ttu-id="31aad-2141">фухрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="31aad-2141">FuhrerscheinnummerNr</span></span> 
- <span data-ttu-id="31aad-2142">фуехрерсчеиннуммернр</span><span class="sxs-lookup"><span data-stu-id="31aad-2142">FuehrerscheinnummerNr</span></span> 
- <span data-ttu-id="31aad-2143">фüхрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2143">FührerscheinnummerKlasse</span></span> 
- <span data-ttu-id="31aad-2144">фухрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2144">FuhrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="31aad-2145">фуехрерсчеиннуммерклассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2145">FuehrerscheinnummerKlasse</span></span> 
- <span data-ttu-id="31aad-2146">Führerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="31aad-2146">Führerschein- Nr</span></span> 
- <span data-ttu-id="31aad-2147">Fuhrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="31aad-2147">Fuhrerschein- Nr</span></span> 
- <span data-ttu-id="31aad-2148">Fuehrerschein- Nr</span><span class="sxs-lookup"><span data-stu-id="31aad-2148">Fuehrerschein- Nr</span></span> 
- <span data-ttu-id="31aad-2149">Führerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="31aad-2149">Führerschein- Klasse</span></span> 
- <span data-ttu-id="31aad-2150">Fuhrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="31aad-2150">Fuhrerschein- Klasse</span></span> 
- <span data-ttu-id="31aad-2151">Fuehrerschein- Klasse</span><span class="sxs-lookup"><span data-stu-id="31aad-2151">Fuehrerschein- Klasse</span></span> 
- <span data-ttu-id="31aad-2152">DL</span><span class="sxs-lookup"><span data-stu-id="31aad-2152">DL</span></span> 
- <span data-ttu-id="31aad-2153">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="31aad-2153">DLS</span></span>
- <span data-ttu-id="31aad-2154">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-2154">Driv Lic</span></span> 
- <span data-ttu-id="31aad-2155">Driv Licen</span><span class="sxs-lookup"><span data-stu-id="31aad-2155">Driv Licen</span></span> 
- <span data-ttu-id="31aad-2156">Driv License</span><span class="sxs-lookup"><span data-stu-id="31aad-2156">Driv License</span></span>
- <span data-ttu-id="31aad-2157">Driv Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2157">Driv Licenses</span></span> 
- <span data-ttu-id="31aad-2158">Driv Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2158">Driv Licence</span></span> 
- <span data-ttu-id="31aad-2159">Driv Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-2159">Driv Licences</span></span> 
- <span data-ttu-id="31aad-2160">Driv Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-2160">Driv Lic</span></span> 
- <span data-ttu-id="31aad-2161">Driver Licen</span><span class="sxs-lookup"><span data-stu-id="31aad-2161">Driver Licen</span></span> 
- <span data-ttu-id="31aad-2162">Driver License</span><span class="sxs-lookup"><span data-stu-id="31aad-2162">Driver License</span></span> 
- <span data-ttu-id="31aad-2163">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2163">Driver Licenses</span></span> 
- <span data-ttu-id="31aad-2164">Driver Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2164">Driver Licence</span></span> 
- <span data-ttu-id="31aad-2165">Driver Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-2165">Driver Licences</span></span> 
- <span data-ttu-id="31aad-2166">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-2166">Drivers Lic</span></span> 
- <span data-ttu-id="31aad-2167">Drivers Licen</span><span class="sxs-lookup"><span data-stu-id="31aad-2167">Drivers Licen</span></span> 
- <span data-ttu-id="31aad-2168">Drivers License</span><span class="sxs-lookup"><span data-stu-id="31aad-2168">Drivers License</span></span> 
- <span data-ttu-id="31aad-2169">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2169">Drivers Licenses</span></span> 
- <span data-ttu-id="31aad-2170">Drivers Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2170">Drivers Licence</span></span> 
- <span data-ttu-id="31aad-2171">Drivers Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-2171">Drivers Licences</span></span> 
- <span data-ttu-id="31aad-2172">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-2172">Driver's Lic</span></span> 
- <span data-ttu-id="31aad-2173">Driver's Licen</span><span class="sxs-lookup"><span data-stu-id="31aad-2173">Driver's Licen</span></span> 
- <span data-ttu-id="31aad-2174">Driver's License</span><span class="sxs-lookup"><span data-stu-id="31aad-2174">Driver's License</span></span> 
- <span data-ttu-id="31aad-2175">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2175">Driver's Licenses</span></span> 
- <span data-ttu-id="31aad-2176">Driver's Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2176">Driver's Licence</span></span> 
- <span data-ttu-id="31aad-2177">Driver's Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-2177">Driver's Licences</span></span> 
- <span data-ttu-id="31aad-2178">Driving Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-2178">Driving Lic</span></span> 
- <span data-ttu-id="31aad-2179">Driving Licen</span><span class="sxs-lookup"><span data-stu-id="31aad-2179">Driving Licen</span></span> 
- <span data-ttu-id="31aad-2180">Driving License</span><span class="sxs-lookup"><span data-stu-id="31aad-2180">Driving License</span></span> 
- <span data-ttu-id="31aad-2181">Driving Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2181">Driving Licenses</span></span> 
- <span data-ttu-id="31aad-2182">Driving Licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2182">Driving Licence</span></span> 
- <span data-ttu-id="31aad-2183">Driving Licences</span><span class="sxs-lookup"><span data-stu-id="31aad-2183">Driving Licences</span></span>

#### <a name="keyword_german_drivers_license_collaborative"></a><span data-ttu-id="31aad-2184">Keyword_german_drivers_license_collaborative</span><span class="sxs-lookup"><span data-stu-id="31aad-2184">Keyword_german_drivers_license_collaborative</span></span>

- <span data-ttu-id="31aad-2185">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2185">Nr-Führerschein</span></span> 
- <span data-ttu-id="31aad-2186">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2186">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="31aad-2187">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2187">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="31aad-2188">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2188">No-Führerschein</span></span> 
- <span data-ttu-id="31aad-2189">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2189">No-Fuhrerschein</span></span> 
- <span data-ttu-id="31aad-2190">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2190">No-Fuehrerschein</span></span> 
- <span data-ttu-id="31aad-2191">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2191">N-Führerschein</span></span> 
- <span data-ttu-id="31aad-2192">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2192">N-Fuhrerschein</span></span> 
- <span data-ttu-id="31aad-2193">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2193">N-Fuehrerschein</span></span>
- <span data-ttu-id="31aad-2194">НР — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2194">Nr-Führerschein</span></span> 
- <span data-ttu-id="31aad-2195">НР — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2195">Nr-Fuhrerschein</span></span> 
- <span data-ttu-id="31aad-2196">НР — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2196">Nr-Fuehrerschein</span></span> 
- <span data-ttu-id="31aad-2197">Нет — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2197">No-Führerschein</span></span> 
- <span data-ttu-id="31aad-2198">Нет — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2198">No-Fuhrerschein</span></span> 
- <span data-ttu-id="31aad-2199">Нет — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2199">No-Fuehrerschein</span></span> 
- <span data-ttu-id="31aad-2200">N — Фüхрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2200">N-Führerschein</span></span> 
- <span data-ttu-id="31aad-2201">N — Фухрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2201">N-Fuhrerschein</span></span> 
- <span data-ttu-id="31aad-2202">N — Фуехрерсчеин</span><span class="sxs-lookup"><span data-stu-id="31aad-2202">N-Fuehrerschein</span></span> 

#### <a name="keyword_german_drivers_license"></a><span data-ttu-id="31aad-2203">Keyword_german_drivers_license</span><span class="sxs-lookup"><span data-stu-id="31aad-2203">Keyword_german_drivers_license</span></span>

- <span data-ttu-id="31aad-2204">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-2204">ausstellungsdatum</span></span>
- <span data-ttu-id="31aad-2205">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="31aad-2205">ausstellungsort</span></span>
- <span data-ttu-id="31aad-2206">ausstellende behöde</span><span class="sxs-lookup"><span data-stu-id="31aad-2206">ausstellende behöde</span></span>
- <span data-ttu-id="31aad-2207">ausstellende behorde</span><span class="sxs-lookup"><span data-stu-id="31aad-2207">ausstellende behorde</span></span>
- <span data-ttu-id="31aad-2208">ausstellende behoerde</span><span class="sxs-lookup"><span data-stu-id="31aad-2208">ausstellende behoerde</span></span>
   
## <a name="german-passport-number"></a><span data-ttu-id="31aad-2209">Номер паспорта гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="31aad-2209">German Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2210">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2210">Format</span></span>

<span data-ttu-id="31aad-2211">10 цифр или букв.</span><span class="sxs-lookup"><span data-stu-id="31aad-2211">10 digits or letters</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2212">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2212">Pattern</span></span>

<span data-ttu-id="31aad-2213">Шаблон должен включать в себя все указанные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="31aad-2213">Pattern must include all of the following:</span></span>
- <span data-ttu-id="31aad-2214">Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K.</span><span class="sxs-lookup"><span data-stu-id="31aad-2214">First character is a digit or a letter from this set (C, F, G, H, J, K)</span></span> 
- <span data-ttu-id="31aad-2215">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2215">Three digits</span></span> 
- <span data-ttu-id="31aad-2216">Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z</span><span class="sxs-lookup"><span data-stu-id="31aad-2216">Five digits or letters from this set (C, -H, J-N, P, R, T, V-Z)</span></span> 
- <span data-ttu-id="31aad-2217">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="31aad-2217">A digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2218">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2218">Checksum</span></span>

<span data-ttu-id="31aad-2219">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2219">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2220">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2220">Definition</span></span>

<span data-ttu-id="31aad-2221">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2221">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2222">функция Func_german_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2222">The function Func_german_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2223">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="31aad-2223">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="31aad-2224">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2224">The checksum passes.</span></span>

<span data-ttu-id="31aad-2225">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2226">функция Func_german_passport_data находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2226">The function Func_german_passport_data finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2227">находится любое ключевое слово из пяти соответствующих списков;</span><span class="sxs-lookup"><span data-stu-id="31aad-2227">A keyword from any of the five keyword lists is found.</span></span>
- <span data-ttu-id="31aad-2228">контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2228">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2229">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2229">Keywords</span></span>

#### <a name="keyword_german_passport"></a><span data-ttu-id="31aad-2230">Keyword_german_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-2230">Keyword_german_passport</span></span>

- <span data-ttu-id="31aad-2231">реисепасс</span><span class="sxs-lookup"><span data-stu-id="31aad-2231">reisepass</span></span>
- <span data-ttu-id="31aad-2232">реисепассе</span><span class="sxs-lookup"><span data-stu-id="31aad-2232">reisepasse</span></span>
- <span data-ttu-id="31aad-2233">реисепасснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2233">reisepassnummer</span></span>
- <span data-ttu-id="31aad-2234">службу</span><span class="sxs-lookup"><span data-stu-id="31aad-2234">passport</span></span>
- <span data-ttu-id="31aad-2235">паспорты</span><span class="sxs-lookup"><span data-stu-id="31aad-2235">passports</span></span>

#### <a name="keyword_german_passport_collaborative"></a><span data-ttu-id="31aad-2236">Keyword_german_passport_collaborative</span><span class="sxs-lookup"><span data-stu-id="31aad-2236">Keyword_german_passport_collaborative</span></span>

- <span data-ttu-id="31aad-2237">жебуртсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-2237">geburtsdatum</span></span>
- <span data-ttu-id="31aad-2238">аусстеллунгсдатум</span><span class="sxs-lookup"><span data-stu-id="31aad-2238">ausstellungsdatum</span></span>
- <span data-ttu-id="31aad-2239">аусстеллунгсорт</span><span class="sxs-lookup"><span data-stu-id="31aad-2239">ausstellungsort</span></span>

#### <a name="keyword_german_passport_number"></a><span data-ttu-id="31aad-2240">Keyword_german_passport_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2240">Keyword_german_passport_number</span></span>

<span data-ttu-id="31aad-2241">No — Реисепасс НР — Реисепасс</span><span class="sxs-lookup"><span data-stu-id="31aad-2241">No-Reisepass Nr-Reisepass</span></span>

#### <a name="keyword_german_passport1"></a><span data-ttu-id="31aad-2242">Keyword_german_passport1</span><span class="sxs-lookup"><span data-stu-id="31aad-2242">Keyword_german_passport1</span></span>

<span data-ttu-id="31aad-2243">Реисепасс — НР</span><span class="sxs-lookup"><span data-stu-id="31aad-2243">Reisepass-Nr</span></span>

#### <a name="keyword_german_passport2"></a><span data-ttu-id="31aad-2244">Keyword_german_passport2</span><span class="sxs-lookup"><span data-stu-id="31aad-2244">Keyword_german_passport2</span></span>

<span data-ttu-id="31aad-2245">бнатионалит. t</span><span class="sxs-lookup"><span data-stu-id="31aad-2245">bnationalit.t</span></span>
   
## <a name="germany-identity-card-number"></a><span data-ttu-id="31aad-2246">Номер идентификационной карты гражданина Германии</span><span class="sxs-lookup"><span data-stu-id="31aad-2246">Germany Identity Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2247">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2247">Format</span></span>

<span data-ttu-id="31aad-2248">С 1 ноября 2010: девять букв и цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-2248">Since 1 November 2010: Nine letters and digits</span></span>

<span data-ttu-id="31aad-2249">От 1 апреля 1987 до 31 октября 2010:10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2249">From 1 April 1987 until 31 October 2010: 10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2250">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2250">Pattern</span></span>

<span data-ttu-id="31aad-2251">С 1 ноября 2010 г.:</span><span class="sxs-lookup"><span data-stu-id="31aad-2251">Since 1 November 2010:</span></span>
- <span data-ttu-id="31aad-2252">одна буква (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-2252">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2253">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2253">Eight digits</span></span>

<span data-ttu-id="31aad-2254">От 1 апреля 1987 до 31 октября 2010:</span><span class="sxs-lookup"><span data-stu-id="31aad-2254">From 1 April 1987 until 31 October 2010:</span></span>
- <span data-ttu-id="31aad-2255">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2255">10 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2256">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2256">Checksum</span></span>

<span data-ttu-id="31aad-2257">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2257">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2258">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2258">Definition</span></span>

<span data-ttu-id="31aad-2259">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2259">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2260">регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2260">The regular expression Regex_germany_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2261">находится ключевое слово из Keyword_germany_id_card.</span><span class="sxs-lookup"><span data-stu-id="31aad-2261">A keyword from Keyword_germany_id_card is found.</span></span>

```xml
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2262">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2262">Keywords</span></span>

#### <a name="keyword_germany_id_card"></a><span data-ttu-id="31aad-2263">Keyword_germany_id_card</span><span class="sxs-lookup"><span data-stu-id="31aad-2263">Keyword_germany_id_card</span></span>

- <span data-ttu-id="31aad-2264">Identity Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2264">Identity Card</span></span>
- <span data-ttu-id="31aad-2265">ID</span><span class="sxs-lookup"><span data-stu-id="31aad-2265">ID</span></span>
- <span data-ttu-id="31aad-2266">Процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-2266">Identification</span></span>
- <span data-ttu-id="31aad-2267">персоналаусвеис</span><span class="sxs-lookup"><span data-stu-id="31aad-2267">Personalausweis</span></span>
- <span data-ttu-id="31aad-2268">идентифизиерунгснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2268">Identifizierungsnummer</span></span>
- <span data-ttu-id="31aad-2269">аусвеис</span><span class="sxs-lookup"><span data-stu-id="31aad-2269">Ausweis</span></span>
- <span data-ttu-id="31aad-2270">идентификатион</span><span class="sxs-lookup"><span data-stu-id="31aad-2270">Identifikation</span></span>
   
## <a name="greece-national-id-card"></a><span data-ttu-id="31aad-2271">Номер внутреннего удостоверения личности для Греции</span><span class="sxs-lookup"><span data-stu-id="31aad-2271">Greece National ID Card</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2272">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2272">Format</span></span>

<span data-ttu-id="31aad-2273">Сочетание 7–8 букв и чисел, а также тире.</span><span class="sxs-lookup"><span data-stu-id="31aad-2273">Combination of 7-8 letters and numbers plus a dash</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2274">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2274">Pattern</span></span>

<span data-ttu-id="31aad-2275">Семь букв и чисел (старый формат):</span><span class="sxs-lookup"><span data-stu-id="31aad-2275">Seven letters and numbers (old format):</span></span>
- <span data-ttu-id="31aad-2276">одна буква (любая буква греческого алфавита);</span><span class="sxs-lookup"><span data-stu-id="31aad-2276">One letter (any letter of the Greek alphabet)</span></span> 
- <span data-ttu-id="31aad-2277">тире;</span><span class="sxs-lookup"><span data-stu-id="31aad-2277">A dash</span></span> 
- <span data-ttu-id="31aad-2278">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2278">Six digits</span></span>

<span data-ttu-id="31aad-2279">Восемь букв и чисел (новый формат):</span><span class="sxs-lookup"><span data-stu-id="31aad-2279">Eight letters and numbers (new format):</span></span>
- <span data-ttu-id="31aad-2280">две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX);</span><span class="sxs-lookup"><span data-stu-id="31aad-2280">Two letters whose uppercase character occurs in both the Greek and Latin alphabets (ABEZHIKMNOPTYX)</span></span> 
- <span data-ttu-id="31aad-2281">тире;</span><span class="sxs-lookup"><span data-stu-id="31aad-2281">A dash</span></span> 
- <span data-ttu-id="31aad-2282">шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2282">Six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2283">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2283">Checksum</span></span>

<span data-ttu-id="31aad-2284">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2284">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2285">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2285">Definition</span></span>

<span data-ttu-id="31aad-2286">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2286">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2287">регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2287">The regular expression Regex_greece_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2288">находится ключевое слово из Keyword_greece_id_card.</span><span class="sxs-lookup"><span data-stu-id="31aad-2288">A keyword from Keyword_greece_id_card is found.</span></span>

```xml
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2289">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2289">Keywords</span></span>

#### <a name="keyword_greece_id_card"></a><span data-ttu-id="31aad-2290">Keyword_greece_id_card</span><span class="sxs-lookup"><span data-stu-id="31aad-2290">Keyword_greece_id_card</span></span>

- <span data-ttu-id="31aad-2291">Greek identity Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2291">Greek identity Card</span></span>
- <span data-ttu-id="31aad-2292">таутотита</span><span class="sxs-lookup"><span data-stu-id="31aad-2292">Tautotita</span></span>
- <span data-ttu-id="31aad-2293">Δελτίο αστυνομικής ταυτότητας</span><span class="sxs-lookup"><span data-stu-id="31aad-2293">Δελτίο αστυνομικής ταυτότητας</span></span>
- <span data-ttu-id="31aad-2294">ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="31aad-2294">Ταυτότητα</span></span>
   
## <a name="hong-kong-identity-card-hkid-number"></a><span data-ttu-id="31aad-2295">Номер удостоверения личности для Гонконга (HKID)</span><span class="sxs-lookup"><span data-stu-id="31aad-2295">Hong Kong Identity Card (HKID) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2296">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2296">Format</span></span>

<span data-ttu-id="31aad-2297">Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.</span><span class="sxs-lookup"><span data-stu-id="31aad-2297">Combination of 8-9 letters and numbers plus optional parentheses around the final character</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2298">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2298">Pattern</span></span>

<span data-ttu-id="31aad-2299">Сочетание 8–9 букв:</span><span class="sxs-lookup"><span data-stu-id="31aad-2299">Combination of 8-9 letters:</span></span>
- <span data-ttu-id="31aad-2300">1–2 буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-2300">1-2 letters (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2301">шесть цифр; </span><span class="sxs-lookup"><span data-stu-id="31aad-2301">Six digits</span></span> 
- <span data-ttu-id="31aad-2302">последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).</span><span class="sxs-lookup"><span data-stu-id="31aad-2302">The final character (any digit or the letter A), which is the check digit and is optionally enclosed in parentheses.</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2303">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2303">Checksum</span></span>

<span data-ttu-id="31aad-2304">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2304">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2305">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2305">Definition</span></span>

<span data-ttu-id="31aad-2306">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2306">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2307">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2307">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2308">находится ключевое слово из Keyword_hong_kong_id_card;</span><span class="sxs-lookup"><span data-stu-id="31aad-2308">A keyword from Keyword_hong_kong_id_card is found.</span></span>
- <span data-ttu-id="31aad-2309">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2309">The checksum passes.</span></span>

<span data-ttu-id="31aad-2310">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2310">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2311">функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2311">The function Func_hong_kong_id_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2312">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2312">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2313">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2313">Keywords</span></span>

#### <a name="keyword_hong_kong_id_card"></a><span data-ttu-id="31aad-2314">Keyword_hong_kong_id_card</span><span class="sxs-lookup"><span data-stu-id="31aad-2314">Keyword_hong_kong_id_card</span></span>

- <span data-ttu-id="31aad-2315">идентификационная карточка Гонконг</span><span class="sxs-lookup"><span data-stu-id="31aad-2315">hong kong identity card</span></span>
- <span data-ttu-id="31aad-2316">хкидк</span><span class="sxs-lookup"><span data-stu-id="31aad-2316">HKIDC</span></span>
- <span data-ttu-id="31aad-2317">id card</span><span class="sxs-lookup"><span data-stu-id="31aad-2317">id card</span></span>
- <span data-ttu-id="31aad-2318">identity card</span><span class="sxs-lookup"><span data-stu-id="31aad-2318">identity card</span></span>
- <span data-ttu-id="31aad-2319">идентификационная карточка HK</span><span class="sxs-lookup"><span data-stu-id="31aad-2319">hk identity card</span></span>
- <span data-ttu-id="31aad-2320">Идентификатор Гонконг</span><span class="sxs-lookup"><span data-stu-id="31aad-2320">hong kong id</span></span>
- <span data-ttu-id="31aad-2321">香港身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2321">香港身份證</span></span>
- <span data-ttu-id="31aad-2322">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2322">香港永久性居民身份證</span></span>
- <span data-ttu-id="31aad-2323">身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2323">身份證</span></span>
- <span data-ttu-id="31aad-2324">身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2324">身份証</span></span>
- <span data-ttu-id="31aad-2325">身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2325">身分證</span></span>
- <span data-ttu-id="31aad-2326">身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2326">身分証</span></span>
- <span data-ttu-id="31aad-2327">香港身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2327">香港身份証</span></span>
- <span data-ttu-id="31aad-2328">香港身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2328">香港身分證</span></span>
- <span data-ttu-id="31aad-2329">香港身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2329">香港身分証</span></span>
- <span data-ttu-id="31aad-2330">香港身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2330">香港身份證</span></span>
- <span data-ttu-id="31aad-2331">香港居民身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2331">香港居民身份證</span></span>
- <span data-ttu-id="31aad-2332">香港居民身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2332">香港居民身份証</span></span>
- <span data-ttu-id="31aad-2333">香港居民身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2333">香港居民身分證</span></span>
- <span data-ttu-id="31aad-2334">香港居民身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2334">香港居民身分証</span></span>
- <span data-ttu-id="31aad-2335">香港永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2335">香港永久性居民身份証</span></span>
- <span data-ttu-id="31aad-2336">香港永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2336">香港永久性居民身分證</span></span>
- <span data-ttu-id="31aad-2337">香港永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2337">香港永久性居民身分証</span></span>
- <span data-ttu-id="31aad-2338">香港永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2338">香港永久性居民身份證</span></span>
- <span data-ttu-id="31aad-2339">香港非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2339">香港非永久性居民身份證</span></span>
- <span data-ttu-id="31aad-2340">香港非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2340">香港非永久性居民身份証</span></span>
- <span data-ttu-id="31aad-2341">香港非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2341">香港非永久性居民身分證</span></span>
- <span data-ttu-id="31aad-2342">香港非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2342">香港非永久性居民身分証</span></span>
- <span data-ttu-id="31aad-2343">香港特別行政區永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2343">香港特別行政區永久性居民身份證</span></span>
- <span data-ttu-id="31aad-2344">香港特別行政區永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2344">香港特別行政區永久性居民身份証</span></span>
- <span data-ttu-id="31aad-2345">香港特別行政區永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2345">香港特別行政區永久性居民身分證</span></span>
- <span data-ttu-id="31aad-2346">香港特別行政區永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2346">香港特別行政區永久性居民身分証</span></span>
- <span data-ttu-id="31aad-2347">香港特別行政區非永久性居民身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2347">香港特別行政區非永久性居民身份證</span></span>
- <span data-ttu-id="31aad-2348">香港特別行政區非永久性居民身份証</span><span class="sxs-lookup"><span data-stu-id="31aad-2348">香港特別行政區非永久性居民身份証</span></span>
- <span data-ttu-id="31aad-2349">香港特別行政區非永久性居民身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-2349">香港特別行政區非永久性居民身分證</span></span>
- <span data-ttu-id="31aad-2350">香港特別行政區非永久性居民身分証</span><span class="sxs-lookup"><span data-stu-id="31aad-2350">香港特別行政區非永久性居民身分証</span></span>
   
## <a name="india-permanent-account-number-pan"></a><span data-ttu-id="31aad-2351">Идентификационный номер налогоплательщика для Индии (PAN)</span><span class="sxs-lookup"><span data-stu-id="31aad-2351">India Permanent Account Number (PAN)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2352">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2352">Format</span></span>

<span data-ttu-id="31aad-2353">10 букв или цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2353">10 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2354">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2354">Pattern</span></span>

<span data-ttu-id="31aad-2355">10 букв или цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2355">10 letters or digits:</span></span>
- <span data-ttu-id="31aad-2356">пять букв (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-2356">Five letters (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2357">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2357">Four digits</span></span> 
- <span data-ttu-id="31aad-2358">буква, которая является алфавитным проверочным символом.</span><span class="sxs-lookup"><span data-stu-id="31aad-2358">A letter which is an alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2359">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2359">Checksum</span></span>

<span data-ttu-id="31aad-2360">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2360">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2361">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2361">Definition</span></span>

<span data-ttu-id="31aad-2362">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2362">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2363">регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2363">The regular expression Regex_india_permanent_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2364">находится ключевое слово из Keyword_india_permanent_account_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-2364">A keyword from Keyword_india_permanent_account_number is found.</span></span>
- <span data-ttu-id="31aad-2365">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2365">The checksum passes.</span></span>

```xml
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2366">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2366">Keywords</span></span>

#### <a name="keyword_india_permanent_account_number"></a><span data-ttu-id="31aad-2367">Keyword_india_permanent_account_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2367">Keyword_india_permanent_account_number</span></span>

- <span data-ttu-id="31aad-2368">Permanent Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2368">Permanent Account Number</span></span> 
- <span data-ttu-id="31aad-2369">ПАНОРАМИРОВАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31aad-2369">PAN</span></span> 
   
## <a name="india-unique-identification-aadhaar-number"></a><span data-ttu-id="31aad-2370">Индивидуальный идентификационный номер (Aadhaar) для Индии</span><span class="sxs-lookup"><span data-stu-id="31aad-2370">India Unique Identification (Aadhaar) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2371">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2371">Format</span></span>

<span data-ttu-id="31aad-2372">12 цифр, содержащих необязательные пробелы или тире.</span><span class="sxs-lookup"><span data-stu-id="31aad-2372">12 digits containing optional spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2373">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2373">Pattern</span></span>

<span data-ttu-id="31aad-2374">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2374">12 digits:</span></span>
- <span data-ttu-id="31aad-2375">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-2375">Four digits</span></span> 
- <span data-ttu-id="31aad-2376">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="31aad-2376">An optional space or dash</span></span> 
- <span data-ttu-id="31aad-2377">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-2377">Four digits</span></span> 
- <span data-ttu-id="31aad-2378">необязательный пробел или тире;</span><span class="sxs-lookup"><span data-stu-id="31aad-2378">An optional space or dash</span></span> 
- <span data-ttu-id="31aad-2379">последняя цифра — проверочная.</span><span class="sxs-lookup"><span data-stu-id="31aad-2379">The final digit which is the check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2380">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2380">Checksum</span></span>

<span data-ttu-id="31aad-2381">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2381">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2382">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2382">Definition</span></span>

<span data-ttu-id="31aad-2383">Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_india_aadhaar находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2383">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-2384">находится ключевое слово из Keyword_india_aadhar;</span><span class="sxs-lookup"><span data-stu-id="31aad-2384">A keyword from Keyword_india_aadhar is found.</span></span>
<span data-ttu-id="31aad-2385">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2385">The checksum passes.</span></span>
<span data-ttu-id="31aad-2386">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_india_aadhaar находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2386">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_india_aadhaar finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-2387">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2387">The checksum passes.</span></span>
```xml
<!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_india_aadhaar"/>
     <Match idRef="Keyword_india_aadhar"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_india_aadhaar"/>
  </Pattern>
</Entity>

### Keywords
   
#### Keyword_india_aadhar
- Aadhar
- Aadhaar
- UID
- आधार
   
## Indonesia Identity Card (KTP) Number

### Format

16 digits containing optional periods

### Pattern

16 digits:
- Two-digit province code 
- A period (optional) 
- Two-digit regency or city code 
- Two-digit subdistrict code 
- A period (optional) 
- Six digits in the format DDMMYY which are the date of birth 
- A period (optional) 
- Four digits

### Checksum

No

### Definition

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.
- A keyword from Keyword_indonesia_id_card is found.

A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The regular expression Regex_indonesia_id_card finds content that matches the pattern.

```
<!-- Indonesia Identity Card (KTP) Number -->
<span data-ttu-id="31aad-2388"><Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Regex_indonesia_id_card"/> <Match idRef="Keyword_indonesia_id_card"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_indonesia_id_card"/> </Pattern>
</Entity></span><span class="sxs-lookup"><span data-stu-id="31aad-2388"></span></span>
```

### Keywords
   
#### Keyword_indonesia_id_card

- KTP
- Kartu Tanda Penduduk 
- Nomor Induk Kependudukan 
   
## International Banking Account Number (IBAN)

### Format

Country code (two letters) plus check digits (two digits) plus bban number (up to 30 characters)

### Pattern

Pattern must include all of the following:

- Two-letter country code
- Two check digits (followed by an optional space) 
- 1-7 groups of four letters or digits (can be separated by spaces)
- 1-3 letters or digits

The format for each country is slightly different. The IBAN sensitive information type covers these 60 countries:

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg

### Checksum

Yes

### Definition

A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:
- The function Func_iban finds content that matches the pattern.
- The checksum passes.

```xml
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2389">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2389">Keywords</span></span>

<span data-ttu-id="31aad-2390">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2390">None</span></span>

   
## <a name="ip-address"></a><span data-ttu-id="31aad-2391">IP-адрес</span><span class="sxs-lookup"><span data-stu-id="31aad-2391">IP Address</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2392">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2392">Format</span></span>

#### <a name="ipv4"></a><span data-ttu-id="31aad-2393">IPv4</span><span class="sxs-lookup"><span data-stu-id="31aad-2393">IPv4:</span></span>
<span data-ttu-id="31aad-2394">Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="31aad-2394">Complex pattern which accounts for formatted (periods) and unformatted (no periods) versions of the IPv4 addresses</span></span>

#### <a name="ipv6"></a><span data-ttu-id="31aad-2395">Поддерживающ</span><span class="sxs-lookup"><span data-stu-id="31aad-2395">IPv6:</span></span>
<span data-ttu-id="31aad-2396"> Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).</span><span class="sxs-lookup"><span data-stu-id="31aad-2396">Complex pattern which accounts for formatted IPv6 numbers (which include colons)</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2397">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2397">Pattern</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2398">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2398">Checksum</span></span>

<span data-ttu-id="31aad-2399">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2399">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2400">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2400">Definition</span></span>

<span data-ttu-id="31aad-2401">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2401">For IPv6, a DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2402">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2402">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2403">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="31aad-2403">No keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="31aad-2404">В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2404">For IPv4, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2405">регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2405">The regular expression Regex_ipv4_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2406">находится ключевое слово из Keyword_ipaddress.</span><span class="sxs-lookup"><span data-stu-id="31aad-2406">A keyword from Keyword_ipaddress is found.</span></span>

<span data-ttu-id="31aad-2407">В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2407">For IPv6, a DLP policy is 95% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2408">регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2408">The regular expression Regex_ipv6_address finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2409">ни одно ключевое слово из Keyword_ipaddress не находится.</span><span class="sxs-lookup"><span data-stu-id="31aad-2409">No keyword from Keyword_ipaddress is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2410">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2410">Keywords</span></span>

#### <a name="keyword_ipaddress"></a><span data-ttu-id="31aad-2411">Keyword_ipaddress</span><span class="sxs-lookup"><span data-stu-id="31aad-2411">Keyword_ipaddress</span></span>

- <span data-ttu-id="31aad-2412">IP (ключевое слово с учетом регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-2412">IP (this keyword is case sensitive)</span></span>
- <span data-ttu-id="31aad-2413">ip address</span><span class="sxs-lookup"><span data-stu-id="31aad-2413">ip address</span></span> 
- <span data-ttu-id="31aad-2414">ip addresses</span><span class="sxs-lookup"><span data-stu-id="31aad-2414">ip addresses</span></span>
- <span data-ttu-id="31aad-2415">internet protocol</span><span class="sxs-lookup"><span data-stu-id="31aad-2415">internet protocol</span></span>
- <span data-ttu-id="31aad-2416">IP-כתובת ה</span><span class="sxs-lookup"><span data-stu-id="31aad-2416">IP-כתובת ה</span></span> 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a><span data-ttu-id="31aad-2417">Международная классификация Diseases (ICD-10-CM)</span><span class="sxs-lookup"><span data-stu-id="31aad-2417">International Classification of Diseases (ICD-10-CM)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2418">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2418">Format</span></span>

<span data-ttu-id="31aad-2419">Dictionary</span><span class="sxs-lookup"><span data-stu-id="31aad-2419">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2420">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2420">Pattern</span></span>

<span data-ttu-id="31aad-2421">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="31aad-2421">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2422">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2422">Checksum</span></span>

<span data-ttu-id="31aad-2423">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2423">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2424">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2424">Definition</span></span>

<span data-ttu-id="31aad-2425">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2425">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2426">Найдено ключевое слово из Dictionary_icd_10_cm.</span><span class="sxs-lookup"><span data-stu-id="31aad-2426">A keyword from Dictionary_icd_10_cm is found.</span></span>

```xml
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

<span data-ttu-id="31aad-2427">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2427">Keywords</span></span>

<span data-ttu-id="31aad-2428">Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятой редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604).</span><span class="sxs-lookup"><span data-stu-id="31aad-2428">Any term from the Dictionary_icd_10_cm keyword dictionary, which is based on the [International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)](https://go.microsoft.com/fwlink/?linkid=852604).</span></span> <span data-ttu-id="31aad-2429">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="31aad-2429">This type looks only for the term, not the insurance codes.</span></span>

   
## <a name="international-classification-of-diseases-icd-9-cm"></a><span data-ttu-id="31aad-2430">Международная классификация Diseases (ICD-9-CM)</span><span class="sxs-lookup"><span data-stu-id="31aad-2430">International Classification of Diseases (ICD-9-CM)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2431">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2431">Format</span></span>

<span data-ttu-id="31aad-2432">Dictionary</span><span class="sxs-lookup"><span data-stu-id="31aad-2432">Dictionary</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2433">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2433">Pattern</span></span>

<span data-ttu-id="31aad-2434">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="31aad-2434">Keyword</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2435">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2435">Checksum</span></span>

<span data-ttu-id="31aad-2436">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2436">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2437">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2437">Definition</span></span>

<span data-ttu-id="31aad-2438">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2438">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2439">Найдено ключевое слово из Dictionary_icd_9_cm.</span><span class="sxs-lookup"><span data-stu-id="31aad-2439">A keyword from Dictionary_icd_9_cm is found.</span></span>

```xml
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2440">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2440">Keywords</span></span>

<span data-ttu-id="31aad-2441">Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятой редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605).</span><span class="sxs-lookup"><span data-stu-id="31aad-2441">Any term from the Dictionary_icd_9_cm keyword dictionary, which is based on the [International Classification of Diseases,Ninth Revision, Clinical Modification (ICD-9-CM)](https://go.microsoft.com/fwlink/?linkid=852605).</span></span> <span data-ttu-id="31aad-2442">Этот тип ищет только термин, а не коды страхования.</span><span class="sxs-lookup"><span data-stu-id="31aad-2442">This type looks only for the term, not the insurance codes.</span></span>
   
## <a name="ireland-personal-public-service-pps-number"></a><span data-ttu-id="31aad-2443">Индивидуальный социальный номер (PPS) для Ирландии</span><span class="sxs-lookup"><span data-stu-id="31aad-2443">Ireland Personal Public Service (PPS) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2444">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2444">Format</span></span>

<span data-ttu-id="31aad-2445">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="31aad-2445">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="31aad-2446">семь цифр, за которыми следуют 1–2 буквы. </span><span class="sxs-lookup"><span data-stu-id="31aad-2446">Seven digits followed by 1-2 letters</span></span> 

<span data-ttu-id="31aad-2447">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="31aad-2447">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="31aad-2448">семь цифр, за которыми следуют две буквы.</span><span class="sxs-lookup"><span data-stu-id="31aad-2448">Seven digits followed by two letters</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2449">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2449">Pattern</span></span>

<span data-ttu-id="31aad-2450">Старый формат (до 31 декабря 2012):</span><span class="sxs-lookup"><span data-stu-id="31aad-2450">Old format (until 31 Dec 2012):</span></span>
- <span data-ttu-id="31aad-2451">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-2451">Seven digits</span></span> 
- <span data-ttu-id="31aad-2452">1–2 буквы (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="31aad-2452">1-2 letters (not case sensitive)</span></span> 

<span data-ttu-id="31aad-2453">Новый формат (1 января 2013 и после):</span><span class="sxs-lookup"><span data-stu-id="31aad-2453">New format (1 Jan 2013 and after):</span></span>
- <span data-ttu-id="31aad-2454">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-2454">Seven digits</span></span> 
- <span data-ttu-id="31aad-2455">буква (без учета регистра), которая является алфавитным проверочным символом;</span><span class="sxs-lookup"><span data-stu-id="31aad-2455">A letter (not case sensitive) which is an alphabetic check digit</span></span> 
- <span data-ttu-id="31aad-2456">буква "A" или "H" (без учета регистра).</span><span class="sxs-lookup"><span data-stu-id="31aad-2456">The letter "A" or "H" (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2457">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2457">Checksum</span></span>

<span data-ttu-id="31aad-2458">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2458">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2459">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2459">Definition</span></span>

<span data-ttu-id="31aad-2460">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2461">Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-2461">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2462">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-2462">One of the following is true:</span></span>
    - <span data-ttu-id="31aad-2463">найдено ключевое слово из Keyword_ireland_pps;</span><span class="sxs-lookup"><span data-stu-id="31aad-2463">A keyword from Keyword_ireland_pps is found.</span></span>
    - <span data-ttu-id="31aad-2464">функция Func_eu_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-2464">The function Func_eu_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-2465">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2465">The checksum passes.</span></span>

<span data-ttu-id="31aad-2466">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2466">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2467">функция Func_ireland_pps находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2467">The function Func_ireland_pps finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2468">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2468">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2469">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2469">Keywords</span></span>

#### <a name="keyword_ireland_pps"></a><span data-ttu-id="31aad-2470">Keyword_ireland_pps</span><span class="sxs-lookup"><span data-stu-id="31aad-2470">Keyword_ireland_pps</span></span>

- <span data-ttu-id="31aad-2471">Personal Public Service Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2471">Personal Public Service Number</span></span> 
- <span data-ttu-id="31aad-2472">PPS Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2472">PPS Number</span></span> 
- <span data-ttu-id="31aad-2473">PPS Num</span><span class="sxs-lookup"><span data-stu-id="31aad-2473">PPS Num</span></span> 
- <span data-ttu-id="31aad-2474">PPS No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2474">PPS No.</span></span> 
- <span data-ttu-id="31aad-2475">PPS #</span><span class="sxs-lookup"><span data-stu-id="31aad-2475">PPS #</span></span> 
- <span data-ttu-id="31aad-2476">PPS #</span><span class="sxs-lookup"><span data-stu-id="31aad-2476">PPS#</span></span> 
- <span data-ttu-id="31aad-2477">ппсн</span><span class="sxs-lookup"><span data-stu-id="31aad-2477">PPSN</span></span> 
- <span data-ttu-id="31aad-2478">Public Services Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2478">Public Services Card</span></span> 
- <span data-ttu-id="31aad-2479">Uimhir Phearsanta Seirbhíse Poiblí</span><span class="sxs-lookup"><span data-stu-id="31aad-2479">Uimhir Phearsanta Seirbhíse Poiblí</span></span> 
- <span data-ttu-id="31aad-2480">Уимх.</span><span class="sxs-lookup"><span data-stu-id="31aad-2480">Uimh.</span></span> <span data-ttu-id="31aad-2481">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="31aad-2481">PSP</span></span> 
- <span data-ttu-id="31aad-2482">НАСТРОЕН</span><span class="sxs-lookup"><span data-stu-id="31aad-2482">PSP</span></span> 
   
## <a name="israel-bank-account-number"></a><span data-ttu-id="31aad-2483">Номер банковского счета для Израиля</span><span class="sxs-lookup"><span data-stu-id="31aad-2483">Israel Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2484">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2484">Format</span></span>

<span data-ttu-id="31aad-2485">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2485">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2486">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2486">Pattern</span></span>

<span data-ttu-id="31aad-2487">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="31aad-2487">Formatted:</span></span>
- <span data-ttu-id="31aad-2488">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2488">Two digits</span></span> 
- <span data-ttu-id="31aad-2489">Тире</span><span class="sxs-lookup"><span data-stu-id="31aad-2489">A dash</span></span> 
- <span data-ttu-id="31aad-2490">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2490">Three digits</span></span> 
- <span data-ttu-id="31aad-2491">Тире</span><span class="sxs-lookup"><span data-stu-id="31aad-2491">A dash</span></span> 
- <span data-ttu-id="31aad-2492">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-2492">Eight digits</span></span>

<span data-ttu-id="31aad-2493">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="31aad-2493">Unformatted:</span></span>
- <span data-ttu-id="31aad-2494">	13 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2494">13 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2495">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2495">Checksum</span></span>

<span data-ttu-id="31aad-2496">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2496">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2497">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2497">Definition</span></span>

<span data-ttu-id="31aad-2498">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2499">регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2499">The regular expression Regex_israel_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2500">находится ключевое слово из Keyword_israel_bank_account_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-2500">A keyword from Keyword_israel_bank_account_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2501">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2501">Keywords</span></span>

#### <a name="keyword_israel_bank_account_number"></a><span data-ttu-id="31aad-2502">Keyword_israel_bank_account_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2502">Keyword_israel_bank_account_number</span></span>

- <span data-ttu-id="31aad-2503">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2503">Bank Account Number</span></span> 
- <span data-ttu-id="31aad-2504">Bank Account</span><span class="sxs-lookup"><span data-stu-id="31aad-2504">Bank Account</span></span> 
- <span data-ttu-id="31aad-2505">Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2505">Account Number</span></span> 
- <span data-ttu-id="31aad-2506">מספר חשבון בנק</span><span class="sxs-lookup"><span data-stu-id="31aad-2506">מספר חשבון בנק</span></span> 
   
## <a name="israel-national-id"></a><span data-ttu-id="31aad-2507">Национальный идентификатор для Израиля</span><span class="sxs-lookup"><span data-stu-id="31aad-2507">Israel National ID</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2508">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2508">Format</span></span>

<span data-ttu-id="31aad-2509">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2509">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2510">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2510">Pattern</span></span>

<span data-ttu-id="31aad-2511">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2511">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2512">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2512">Checksum</span></span>

<span data-ttu-id="31aad-2513">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2513">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2514">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2514">Definition</span></span>

<span data-ttu-id="31aad-2515">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2515">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2516">функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2516">The function Func_israeli_national_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2517">находится ключевое слово из Keyword_Israel_National_ID;</span><span class="sxs-lookup"><span data-stu-id="31aad-2517">A keyword from Keyword_Israel_National_ID is found.</span></span>
- <span data-ttu-id="31aad-2518">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2518">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2519">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2519">Keywords</span></span>

#### <a name="keyword_israel_national_id"></a><span data-ttu-id="31aad-2520">Keyword_Israel_National_ID</span><span class="sxs-lookup"><span data-stu-id="31aad-2520">Keyword_Israel_National_ID</span></span>

- <span data-ttu-id="31aad-2521">מספר זהות</span><span class="sxs-lookup"><span data-stu-id="31aad-2521">מספר זהות</span></span> 
- <span data-ttu-id="31aad-2522">National ID Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2522">National ID Number</span></span>
   
## <a name="italy-drivers-license-number"></a><span data-ttu-id="31aad-2523">Номер водительского удостоверения для Италии</span><span class="sxs-lookup"><span data-stu-id="31aad-2523">Italy Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2524">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2524">Format</span></span>

<span data-ttu-id="31aad-2525">Сочетание из 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2525">A combination of 10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2526">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2526">Pattern</span></span>

- <span data-ttu-id="31aad-2527">Сочетание 10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2527">A combination of 10 letters and digits:</span></span>
- <span data-ttu-id="31aad-2528">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-2528">One letter (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2529">Буква "A" или "V" (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-2529">The letter "A" or "V" (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2530">Семь букв (без учета регистра), цифр или символов подчеркивания</span><span class="sxs-lookup"><span data-stu-id="31aad-2530">Seven letters (not case sensitive), digits, or the underscore character</span></span> 
- <span data-ttu-id="31aad-2531">Одна буква (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-2531">One letter (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2532">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2532">Checksum</span></span>

<span data-ttu-id="31aad-2533">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2533">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2534">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2534">Definition</span></span>

<span data-ttu-id="31aad-2535">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2536">регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2536">The regular expression Regex_italy_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2537">находится ключевое слово из Keyword_italy_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-2537">A keyword from Keyword_italy_drivers_license_number is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2538">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2538">Keywords</span></span>

#### <a name="keyword_italy_drivers_license_number"></a><span data-ttu-id="31aad-2539">Keyword_italy_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2539">Keyword_italy_drivers_license_number</span></span>

- <span data-ttu-id="31aad-2540">numero di patente di guida</span><span class="sxs-lookup"><span data-stu-id="31aad-2540">numero di patente di guida</span></span> 
- <span data-ttu-id="31aad-2541">patente di guida</span><span class="sxs-lookup"><span data-stu-id="31aad-2541">patente di guida</span></span> 
   
## <a name="japan-bank-account-number"></a><span data-ttu-id="31aad-2542">Номер банковского счета для Японии</span><span class="sxs-lookup"><span data-stu-id="31aad-2542">Japan Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2543">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2543">Format</span></span>

<span data-ttu-id="31aad-2544">Семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2544">Seven or eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2545">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2545">Pattern</span></span>

<span data-ttu-id="31aad-2546">Номер банковского счета:</span><span class="sxs-lookup"><span data-stu-id="31aad-2546">Bank account number:</span></span>
- <span data-ttu-id="31aad-2547">семь или восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2547">Seven or eight digits</span></span>
- <span data-ttu-id="31aad-2548">Код филиала для банковского счета.</span><span class="sxs-lookup"><span data-stu-id="31aad-2548">Bank account branch code:</span></span>
- <span data-ttu-id="31aad-2549">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2549">Four digits</span></span> 
- <span data-ttu-id="31aad-2550">Пробел или тире (необязательно)</span><span class="sxs-lookup"><span data-stu-id="31aad-2550">A space or dash (optional)</span></span> 
- <span data-ttu-id="31aad-2551">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2551">Three digits</span></span>

<span data-ttu-id="31aad-2552">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2552">Checksum</span></span>

<span data-ttu-id="31aad-2553">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2553">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2554">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2554">Definition</span></span>

<span data-ttu-id="31aad-2555">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2555">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2556">Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-2556">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2557">Находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="31aad-2557">A keyword from Keyword_jp_bank_account is found.</span></span>
- <span data-ttu-id="31aad-2558">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-2558">One of the following is true:</span></span>
- <span data-ttu-id="31aad-2559">функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2559">The function Func_jp_bank_account_branch_code finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2560">найдено ключевое слово из Keyword_jp_bank_branch_code.</span><span class="sxs-lookup"><span data-stu-id="31aad-2560">A keyword from Keyword_jp_bank_branch_code is found.</span></span>

<span data-ttu-id="31aad-2561">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2561">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2562">функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2562">The function Func_jp_bank_account finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2563">находится ключевое слово из Keyword_jp_bank_account.</span><span class="sxs-lookup"><span data-stu-id="31aad-2563">A keyword from Keyword_jp_bank_account is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2564">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2564">Keywords</span></span>

#### <a name="keyword_jp_bank_account"></a><span data-ttu-id="31aad-2565">Keyword_jp_bank_account</span><span class="sxs-lookup"><span data-stu-id="31aad-2565">Keyword_jp_bank_account</span></span>

- <span data-ttu-id="31aad-2566">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2566">Checking Account Number</span></span> 
- <span data-ttu-id="31aad-2567">Checking Account</span><span class="sxs-lookup"><span data-stu-id="31aad-2567">Checking Account</span></span> 
- <span data-ttu-id="31aad-2568">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-2568">Checking Account #</span></span> 
- <span data-ttu-id="31aad-2569">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2569">Checking Acct Number</span></span> 
- <span data-ttu-id="31aad-2570">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-2570">Checking Acct #</span></span> 
- <span data-ttu-id="31aad-2571">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2571">Checking Acct No.</span></span> 
- <span data-ttu-id="31aad-2572">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2572">Checking Account No.</span></span> 
- <span data-ttu-id="31aad-2573">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2573">Bank Account Number</span></span> 
- <span data-ttu-id="31aad-2574">Bank Account</span><span class="sxs-lookup"><span data-stu-id="31aad-2574">Bank Account</span></span> 
- <span data-ttu-id="31aad-2575">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-2575">Bank Account #</span></span> 
- <span data-ttu-id="31aad-2576">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2576">Bank Acct Number</span></span> 
- <span data-ttu-id="31aad-2577">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-2577">Bank Acct #</span></span> 
- <span data-ttu-id="31aad-2578">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2578">Bank Acct No.</span></span> 
- <span data-ttu-id="31aad-2579">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2579">Bank Account No.</span></span> 
- <span data-ttu-id="31aad-2580">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2580">Savings Account Number</span></span> 
- <span data-ttu-id="31aad-2581">Savings Account</span><span class="sxs-lookup"><span data-stu-id="31aad-2581">Savings Account</span></span> 
- <span data-ttu-id="31aad-2582">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-2582">Savings Account #</span></span> 
- <span data-ttu-id="31aad-2583">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2583">Savings Acct Number</span></span> 
- <span data-ttu-id="31aad-2584">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-2584">Savings Acct #</span></span> 
- <span data-ttu-id="31aad-2585">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2585">Savings Acct No.</span></span> 
- <span data-ttu-id="31aad-2586">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2586">Savings Account No.</span></span> 
- <span data-ttu-id="31aad-2587">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2587">Debit Account Number</span></span> 
- <span data-ttu-id="31aad-2588">Debit Account</span><span class="sxs-lookup"><span data-stu-id="31aad-2588">Debit Account</span></span> 
- <span data-ttu-id="31aad-2589">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-2589">Debit Account #</span></span> 
- <span data-ttu-id="31aad-2590">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2590">Debit Acct Number</span></span> 
- <span data-ttu-id="31aad-2591">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-2591">Debit Acct #</span></span> 
- <span data-ttu-id="31aad-2592">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2592">Debit Acct No.</span></span> 
- <span data-ttu-id="31aad-2593">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2593">Debit Account No.</span></span> 
- <span data-ttu-id="31aad-2594">口座番号を当座預金口座の確認</span><span class="sxs-lookup"><span data-stu-id="31aad-2594">口座番号を当座預金口座の確認</span></span> 
- <span data-ttu-id="31aad-2595">#アカウントの確認 、 勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="31aad-2595">＃アカウントの確認、勘定番号の確認</span></span> 
- <span data-ttu-id="31aad-2596">#勘定の確認</span><span class="sxs-lookup"><span data-stu-id="31aad-2596">＃勘定の確認</span></span> 
- <span data-ttu-id="31aad-2597">勘定番号の確認</span><span class="sxs-lookup"><span data-stu-id="31aad-2597">勘定番号の確認</span></span> 
- <span data-ttu-id="31aad-2598">口座番号の確認</span><span class="sxs-lookup"><span data-stu-id="31aad-2598">口座番号の確認</span></span> 
- <span data-ttu-id="31aad-2599">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2599">銀行口座番号</span></span> 
- <span data-ttu-id="31aad-2600">銀行口座</span><span class="sxs-lookup"><span data-stu-id="31aad-2600">銀行口座</span></span> 
- <span data-ttu-id="31aad-2601">銀行口座 #</span><span class="sxs-lookup"><span data-stu-id="31aad-2601">銀行口座＃</span></span> 
- <span data-ttu-id="31aad-2602">銀行の勘定番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2602">銀行の勘定番号</span></span> 
- <span data-ttu-id="31aad-2603">銀行のаккт #</span><span class="sxs-lookup"><span data-stu-id="31aad-2603">銀行のacct＃</span></span> 
- <span data-ttu-id="31aad-2604">銀行の勘定いいえ</span><span class="sxs-lookup"><span data-stu-id="31aad-2604">銀行の勘定いいえ</span></span> 
- <span data-ttu-id="31aad-2605">銀行口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2605">銀行口座番号</span></span>
- <span data-ttu-id="31aad-2606">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2606">普通預金口座番号</span></span> 
- <span data-ttu-id="31aad-2607">預金口座</span><span class="sxs-lookup"><span data-stu-id="31aad-2607">預金口座</span></span> 
- <span data-ttu-id="31aad-2608">貯蓄口座 #</span><span class="sxs-lookup"><span data-stu-id="31aad-2608">貯蓄口座＃</span></span> 
- <span data-ttu-id="31aad-2609">貯蓄勘定の数</span><span class="sxs-lookup"><span data-stu-id="31aad-2609">貯蓄勘定の数</span></span> 
- <span data-ttu-id="31aad-2610">貯蓄勘定 #</span><span class="sxs-lookup"><span data-stu-id="31aad-2610">貯蓄勘定＃</span></span> 
- <span data-ttu-id="31aad-2611">貯蓄勘定番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2611">貯蓄勘定番号</span></span> 
- <span data-ttu-id="31aad-2612">普通預金口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2612">普通預金口座番号</span></span> 
- <span data-ttu-id="31aad-2613">引き落とし口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2613">引き落とし口座番号</span></span> 
- <span data-ttu-id="31aad-2614">口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2614">口座番号</span></span> 
- <span data-ttu-id="31aad-2615">口座番号 #</span><span class="sxs-lookup"><span data-stu-id="31aad-2615">口座番号＃</span></span> 
- <span data-ttu-id="31aad-2616">デビットのаккт番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2616">デビットのacct番号</span></span> 
- <span data-ttu-id="31aad-2617">デビット勘定 #</span><span class="sxs-lookup"><span data-stu-id="31aad-2617">デビット勘定＃</span></span> 
- <span data-ttu-id="31aad-2618">デビットакктの番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2618">デビットACCTの番号</span></span> 
- <span data-ttu-id="31aad-2619">デビット口座番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2619">デビット口座番号</span></span> 

#### <a name="keyword_jp_bank_branch_code"></a><span data-ttu-id="31aad-2620">Keyword_jp_bank_branch_code</span><span class="sxs-lookup"><span data-stu-id="31aad-2620">Keyword_jp_bank_branch_code</span></span>

<span data-ttu-id="31aad-2621">отемачи</span><span class="sxs-lookup"><span data-stu-id="31aad-2621">Otemachi</span></span>

## <a name="japan-drivers-license-number"></a><span data-ttu-id="31aad-2622">Номер водительского удостоверения для Японии</span><span class="sxs-lookup"><span data-stu-id="31aad-2622">Japan Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2623">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2623">Format</span></span>

<span data-ttu-id="31aad-2624">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2624">12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2625">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2625">Pattern</span></span>

<span data-ttu-id="31aad-2626">12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2626">12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2627">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2627">Checksum</span></span>

<span data-ttu-id="31aad-2628">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2628">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2629">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2629">Definition</span></span>

<span data-ttu-id="31aad-2630">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2630">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2631">функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2631">The function Func_jp_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2632">находится ключевое слово из Keyword_jp_drivers_license_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-2632">A keyword from Keyword_jp_drivers_license_number is found.</span></span>

```xml
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2633">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2633">Keywords</span></span>

#### <a name="keyword_jp_drivers_license_number"></a><span data-ttu-id="31aad-2634">Keyword_jp_drivers_license_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2634">Keyword_jp_drivers_license_number</span></span>

- <span data-ttu-id="31aad-2635">DL #</span><span class="sxs-lookup"><span data-stu-id="31aad-2635">dl#</span></span> 
- <span data-ttu-id="31aad-2636">DL</span><span class="sxs-lookup"><span data-stu-id="31aad-2636">DL＃</span></span> 
- <span data-ttu-id="31aad-2637">библиотек #</span><span class="sxs-lookup"><span data-stu-id="31aad-2637">dls#</span></span> 
- <span data-ttu-id="31aad-2638">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="31aad-2638">DLS＃</span></span> 
- <span data-ttu-id="31aad-2639">driver license</span><span class="sxs-lookup"><span data-stu-id="31aad-2639">driver license</span></span> 
- <span data-ttu-id="31aad-2640">driver licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2640">driver licenses</span></span> 
- <span data-ttu-id="31aad-2641">drivers license</span><span class="sxs-lookup"><span data-stu-id="31aad-2641">drivers license</span></span> 
- <span data-ttu-id="31aad-2642">driver's license</span><span class="sxs-lookup"><span data-stu-id="31aad-2642">driver's license</span></span> 
- <span data-ttu-id="31aad-2643">drivers licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2643">drivers licenses</span></span> 
- <span data-ttu-id="31aad-2644">driver's licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-2644">driver's licenses</span></span> 
- <span data-ttu-id="31aad-2645">driving licence</span><span class="sxs-lookup"><span data-stu-id="31aad-2645">driving licence</span></span> 
- <span data-ttu-id="31aad-2646">лик #</span><span class="sxs-lookup"><span data-stu-id="31aad-2646">lic#</span></span> 
- <span data-ttu-id="31aad-2647">Лик #</span><span class="sxs-lookup"><span data-stu-id="31aad-2647">LIC＃</span></span> 
- <span data-ttu-id="31aad-2648">ликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-2648">lics#</span></span> 
- <span data-ttu-id="31aad-2649">state id</span><span class="sxs-lookup"><span data-stu-id="31aad-2649">state id</span></span> 
- <span data-ttu-id="31aad-2650">state identification</span><span class="sxs-lookup"><span data-stu-id="31aad-2650">state identification</span></span> 
- <span data-ttu-id="31aad-2651">state identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-2651">state identification number</span></span> 
- <span data-ttu-id="31aad-2652">低所得国 #</span><span class="sxs-lookup"><span data-stu-id="31aad-2652">低所得国＃</span></span> 
- <span data-ttu-id="31aad-2653">免許証</span><span class="sxs-lookup"><span data-stu-id="31aad-2653">免許証</span></span> 
- <span data-ttu-id="31aad-2654">状態ид</span><span class="sxs-lookup"><span data-stu-id="31aad-2654">状態ID</span></span>
- <span data-ttu-id="31aad-2655">状態の識別</span><span class="sxs-lookup"><span data-stu-id="31aad-2655">状態の識別</span></span> 
- <span data-ttu-id="31aad-2656">状態の識別番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2656">状態の識別番号</span></span> 
- <span data-ttu-id="31aad-2657">運転免許</span><span class="sxs-lookup"><span data-stu-id="31aad-2657">運転免許</span></span> 
- <span data-ttu-id="31aad-2658">運転免許証</span><span class="sxs-lookup"><span data-stu-id="31aad-2658">運転免許証</span></span> 
- <span data-ttu-id="31aad-2659">運転免許証番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2659">運転免許証番号</span></span> 
   
## <a name="japan-passport-number"></a><span data-ttu-id="31aad-2660">Номер паспорта гражданина Японии</span><span class="sxs-lookup"><span data-stu-id="31aad-2660">Japan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2661">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2661">Format</span></span>

<span data-ttu-id="31aad-2662">Две буквы, за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2662">Two letters followed by seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2663">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2663">Pattern</span></span>

<span data-ttu-id="31aad-2664">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2664">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2665">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2665">Checksum</span></span>

<span data-ttu-id="31aad-2666">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2666">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2667">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2667">Definition</span></span>

<span data-ttu-id="31aad-2668">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2668">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2669">функция Func_jp_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2669">The function Func_jp_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2670">находится ключевое слово из Keyword_jp_passport.</span><span class="sxs-lookup"><span data-stu-id="31aad-2670">A keyword from Keyword_jp_passport is found.</span></span>

```xml
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2671">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2671">Keywords</span></span>

#### <a name="keyword_jp_passport"></a><span data-ttu-id="31aad-2672">Keyword_jp_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-2672">Keyword_jp_passport</span></span>

- <span data-ttu-id="31aad-2673">パスポート</span><span class="sxs-lookup"><span data-stu-id="31aad-2673">パスポート</span></span> 
- <span data-ttu-id="31aad-2674">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2674">パスポート番号</span></span> 
- <span data-ttu-id="31aad-2675">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="31aad-2675">パスポートのNum</span></span> 
- <span data-ttu-id="31aad-2676">パスポート #</span><span class="sxs-lookup"><span data-stu-id="31aad-2676">パスポート＃</span></span> 
   
## <a name="japan-resident-registration-number"></a><span data-ttu-id="31aad-2677">Номер регистрации резидента Японии</span><span class="sxs-lookup"><span data-stu-id="31aad-2677">Japan Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2678">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2678">Format</span></span>

<span data-ttu-id="31aad-2679">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2679">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2680">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2680">Pattern</span></span>

<span data-ttu-id="31aad-2681">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2681">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2682">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2682">Checksum</span></span>

<span data-ttu-id="31aad-2683">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2683">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2684">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2684">Definition</span></span>

<span data-ttu-id="31aad-2685">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2685">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2686">функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2686">The function Func_jp_resident_registration_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2687">находится ключевое слово из Keyword_jp_resident_registration_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-2687">A keyword from Keyword_jp_resident_registration_number is found.</span></span>

```xml
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2688">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2688">Keywords</span></span>

#### <a name="keyword_jp_resident_registration_number"></a><span data-ttu-id="31aad-2689">Keyword_jp_resident_registration_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2689">Keyword_jp_resident_registration_number</span></span>

- <span data-ttu-id="31aad-2690">Resident Registration Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2690">Resident Registration Number</span></span>
- <span data-ttu-id="31aad-2691">Resident Register Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2691">Resident Register Number</span></span> 
- <span data-ttu-id="31aad-2692">Residents Basic Registry Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2692">Residents Basic Registry Number</span></span> 
- <span data-ttu-id="31aad-2693">Resident Registration No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2693">Resident Registration No.</span></span> 
- <span data-ttu-id="31aad-2694">Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2694">Resident Register No.</span></span> 
- <span data-ttu-id="31aad-2695">Residents Basic Registry No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2695">Residents Basic Registry No.</span></span> 
- <span data-ttu-id="31aad-2696">Basic Resident Register No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2696">Basic Resident Register No.</span></span> 
- <span data-ttu-id="31aad-2697">住民登録番号 、 登録番号をレジデント</span><span class="sxs-lookup"><span data-stu-id="31aad-2697">住民登録番号、登録番号をレジデント</span></span> 
- <span data-ttu-id="31aad-2698">住民基本登録番号 、 登録番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2698">住民基本登録番号、登録番号</span></span> 
- <span data-ttu-id="31aad-2699">住民基本レジストリ番号を常駐</span><span class="sxs-lookup"><span data-stu-id="31aad-2699">住民基本レジストリ番号を常駐</span></span> 
- <span data-ttu-id="31aad-2700">登録番号を常駐住民基本台帳登録番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2700">登録番号を常駐住民基本台帳登録番号</span></span> 

   
## <a name="japan-social-insurance-number-sin"></a><span data-ttu-id="31aad-2701">Номер карты социального страхования для Японии (SIN)</span><span class="sxs-lookup"><span data-stu-id="31aad-2701">Japan Social Insurance Number (SIN)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2702">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2702">Format</span></span>

<span data-ttu-id="31aad-2703">7–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2703">7-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2704">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2704">Pattern</span></span>

<span data-ttu-id="31aad-2705">7–12 цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-2705">7-12 digits:</span></span>
- <span data-ttu-id="31aad-2706">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-2706">Four digits</span></span> 
- <span data-ttu-id="31aad-2707">Дефис (необязательно)</span><span class="sxs-lookup"><span data-stu-id="31aad-2707">A hyphen (optional)</span></span> 
- <span data-ttu-id="31aad-2708">Шесть цифр или</span><span class="sxs-lookup"><span data-stu-id="31aad-2708">Six digits OR</span></span>
- <span data-ttu-id="31aad-2709">7–12 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2709">7-12 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2710">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2710">Checksum</span></span>

<span data-ttu-id="31aad-2711">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2711">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2712">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2712">Definition</span></span>

<span data-ttu-id="31aad-2713">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2713">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2714">функция Func_jp_sin находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2714">The function Func_jp_sin finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2715">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="31aad-2715">A keyword from Keyword_jp_sin is found.</span></span>

<span data-ttu-id="31aad-2716">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2716">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2717">функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2717">The function Func_jp_sin_pre_1997 finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2718">находится ключевое слово из Keyword_jp_sin.</span><span class="sxs-lookup"><span data-stu-id="31aad-2718">A keyword from Keyword_jp_sin is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2719">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2719">Keywords</span></span>

#### <a name="keyword_jp_sin"></a><span data-ttu-id="31aad-2720">Keyword_jp_sin</span><span class="sxs-lookup"><span data-stu-id="31aad-2720">Keyword_jp_sin</span></span>

- <span data-ttu-id="31aad-2721">Social Insurance No.</span><span class="sxs-lookup"><span data-stu-id="31aad-2721">Social Insurance No.</span></span> 
- <span data-ttu-id="31aad-2722">Social Insurance Num</span><span class="sxs-lookup"><span data-stu-id="31aad-2722">Social Insurance Num</span></span> 
- <span data-ttu-id="31aad-2723">Social Insurance Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2723">Social Insurance Number</span></span> 
- <span data-ttu-id="31aad-2724">社会保険のテンキー</span><span class="sxs-lookup"><span data-stu-id="31aad-2724">社会保険のテンキー</span></span> 
- <span data-ttu-id="31aad-2725">社会保険番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2725">社会保険番号</span></span> 

## <a name="japanese-residence-card-number"></a><span data-ttu-id="31aad-2726">Номер карточки для японского языка</span><span class="sxs-lookup"><span data-stu-id="31aad-2726">Japanese Residence Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2727">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2727">Format</span></span>

<span data-ttu-id="31aad-2728">12 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-2728">12 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2729">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2729">Pattern</span></span>

<span data-ttu-id="31aad-2730">12 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2730">12 letters and digits:</span></span>
- <span data-ttu-id="31aad-2731">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-2731">Two letters (not case sensitive)</span></span>
- <span data-ttu-id="31aad-2732">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2732">Eight digits</span></span> 
- <span data-ttu-id="31aad-2733">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-2733">Two letters (not case sensitive)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2734">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2734">Checksum</span></span>

<span data-ttu-id="31aad-2735">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2735">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2736">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2736">Definition</span></span>

<span data-ttu-id="31aad-2737">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2737">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2738">Регулярное выражение Regex_jp_residence_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2738">The regular expression Regex_jp_residence_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2739">Найдено ключевое слово из Keyword_jp_residence_card_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-2739">A keyword from Keyword_jp_residence_card_number is found.</span></span>

```xml
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2740">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2740">Keywords</span></span>

#### <a name="keyword_jp_residence_card_number"></a><span data-ttu-id="31aad-2741">Keyword_jp_residence_card_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2741">Keyword_jp_residence_card_number</span></span>

- <span data-ttu-id="31aad-2742">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="31aad-2742">Residence card number</span></span>
- <span data-ttu-id="31aad-2743">Номер карточки проживания</span><span class="sxs-lookup"><span data-stu-id="31aad-2743">Residence card no</span></span>
- <span data-ttu-id="31aad-2744">Карточка проживания #</span><span class="sxs-lookup"><span data-stu-id="31aad-2744">Residence card #</span></span>
- <span data-ttu-id="31aad-2745">在留カード番号</span><span class="sxs-lookup"><span data-stu-id="31aad-2745">在留カード番号</span></span>
   
## <a name="malaysia-id-card-number"></a><span data-ttu-id="31aad-2746">Номер удостоверения личности для Малайзии</span><span class="sxs-lookup"><span data-stu-id="31aad-2746">Malaysia ID Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2747">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2747">Format</span></span>

<span data-ttu-id="31aad-2748">12 цифр, содержащих необязательные дефисы.</span><span class="sxs-lookup"><span data-stu-id="31aad-2748">12 digits containing optional hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2749">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2749">Pattern</span></span>

<span data-ttu-id="31aad-2750">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2750">12 digits:</span></span>
- <span data-ttu-id="31aad-2751">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="31aad-2751">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="31aad-2752">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="31aad-2752">A dash (optional)</span></span> 
- <span data-ttu-id="31aad-2753">код места рождения из двух букв;</span><span class="sxs-lookup"><span data-stu-id="31aad-2753">Two-letter place-of-birth code</span></span> 
- <span data-ttu-id="31aad-2754">дефис (необязательно);</span><span class="sxs-lookup"><span data-stu-id="31aad-2754">A dash (optional)</span></span> 
- <span data-ttu-id="31aad-2755">три случайные цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-2755">Three random digits</span></span> 
- <span data-ttu-id="31aad-2756">код пола из одной цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-2756">One-digit gender code</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2757">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2757">Checksum</span></span>

<span data-ttu-id="31aad-2758">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2758">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2759">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2759">Definition</span></span>

<span data-ttu-id="31aad-2760">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2760">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2761">регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2761">The regular expression Regex_malaysia_id_card_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2762">находится ключевое слово из Keyword_malaysia_id_card_number.</span><span class="sxs-lookup"><span data-stu-id="31aad-2762">A keyword from Keyword_malaysia_id_card_number is found.</span></span>

```xml
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2763">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2763">Keywords</span></span>
   
#### <a name="keyword_malaysia_id_card_number"></a><span data-ttu-id="31aad-2764">Keyword_malaysia_id_card_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2764">Keyword_malaysia_id_card_number</span></span>

- <span data-ttu-id="31aad-2765">карточка цифрового приложения</span><span class="sxs-lookup"><span data-stu-id="31aad-2765">digital application card</span></span>
- <span data-ttu-id="31aad-2766">i/c</span><span class="sxs-lookup"><span data-stu-id="31aad-2766">i/c</span></span>
- <span data-ttu-id="31aad-2767">i/c нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2767">i/c no</span></span>
- <span data-ttu-id="31aad-2768">внутренних</span><span class="sxs-lookup"><span data-stu-id="31aad-2768">ic</span></span>
- <span data-ttu-id="31aad-2769">МФ нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2769">ic no</span></span>
- <span data-ttu-id="31aad-2770">id card</span><span class="sxs-lookup"><span data-stu-id="31aad-2770">id card</span></span>
- <span data-ttu-id="31aad-2771">идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="31aad-2771">identification Card</span></span>
- <span data-ttu-id="31aad-2772">identity card</span><span class="sxs-lookup"><span data-stu-id="31aad-2772">identity card</span></span>
- <span data-ttu-id="31aad-2773">k/p</span><span class="sxs-lookup"><span data-stu-id="31aad-2773">k/p</span></span>
- <span data-ttu-id="31aad-2774">k/p</span><span class="sxs-lookup"><span data-stu-id="31aad-2774">k/p no</span></span>
- <span data-ttu-id="31aad-2775">кад акуан Дири</span><span class="sxs-lookup"><span data-stu-id="31aad-2775">kad akuan diri</span></span>
- <span data-ttu-id="31aad-2776">кад апликаси Digital</span><span class="sxs-lookup"><span data-stu-id="31aad-2776">kad aplikasi digital</span></span>
- <span data-ttu-id="31aad-2777">кад пенженалан Малайзии</span><span class="sxs-lookup"><span data-stu-id="31aad-2777">kad pengenalan malaysia</span></span>
- <span data-ttu-id="31aad-2778">ключев</span><span class="sxs-lookup"><span data-stu-id="31aad-2778">kp</span></span>
- <span data-ttu-id="31aad-2779">ключевой номер</span><span class="sxs-lookup"><span data-stu-id="31aad-2779">kp no</span></span>
- <span data-ttu-id="31aad-2780">микад</span><span class="sxs-lookup"><span data-stu-id="31aad-2780">mykad</span></span>
- <span data-ttu-id="31aad-2781">микас</span><span class="sxs-lookup"><span data-stu-id="31aad-2781">mykas</span></span>
- <span data-ttu-id="31aad-2782">микид</span><span class="sxs-lookup"><span data-stu-id="31aad-2782">mykid</span></span>
- <span data-ttu-id="31aad-2783">мипр</span><span class="sxs-lookup"><span data-stu-id="31aad-2783">mypr</span></span>
- <span data-ttu-id="31aad-2784">митентера</span><span class="sxs-lookup"><span data-stu-id="31aad-2784">mytentera</span></span>
- <span data-ttu-id="31aad-2785">идентификационная карточка Малайзии</span><span class="sxs-lookup"><span data-stu-id="31aad-2785">malaysia identity card</span></span>
- <span data-ttu-id="31aad-2786">идентификационная карточка малайсиан</span><span class="sxs-lookup"><span data-stu-id="31aad-2786">malaysian identity card</span></span>
- <span data-ttu-id="31aad-2787">NRIC</span><span class="sxs-lookup"><span data-stu-id="31aad-2787">nric</span></span>
- <span data-ttu-id="31aad-2788">Личная идентификационная карточка</span><span class="sxs-lookup"><span data-stu-id="31aad-2788">personal identification card</span></span>
   
## <a name="netherlands-citizens-service-bsn-number"></a><span data-ttu-id="31aad-2789">Номер гражданской службы для Нидерландов (BSN)</span><span class="sxs-lookup"><span data-stu-id="31aad-2789">Netherlands Citizen's Service (BSN) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2790">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2790">Format</span></span>

<span data-ttu-id="31aad-2791">8–9 цифр, содержащих необязательные пробелы.</span><span class="sxs-lookup"><span data-stu-id="31aad-2791">8-9 digits containing optional spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2792">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2792">Pattern</span></span>

<span data-ttu-id="31aad-2793">8–9 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2793">8-9 digits:</span></span>
- <span data-ttu-id="31aad-2794">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-2794">Three digits</span></span> 
- <span data-ttu-id="31aad-2795">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="31aad-2795">A space (optional)</span></span> 
- <span data-ttu-id="31aad-2796">три цифры; </span><span class="sxs-lookup"><span data-stu-id="31aad-2796">Three digits</span></span> 
- <span data-ttu-id="31aad-2797">пробел (необязательно); </span><span class="sxs-lookup"><span data-stu-id="31aad-2797">A space (optional)</span></span> 
- <span data-ttu-id="31aad-2798">2–3 цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-2798">2-3 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2799">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2799">Checksum</span></span>

<span data-ttu-id="31aad-2800">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2800">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2801">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2801">Definition</span></span>

<span data-ttu-id="31aad-2802">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2802">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2803">функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2803">The function Func_netherlands_bsn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2804">находится ключевое слово из Keyword_netherlands_bsn;</span><span class="sxs-lookup"><span data-stu-id="31aad-2804">A keyword from Keyword_netherlands_bsn is found.</span></span>
- <span data-ttu-id="31aad-2805">функция Func_eu_date2 находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-2805">The function Func_eu_date2 finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-2806">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2806">The checksum passes.</span></span>

```xml
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2807">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2807">Keywords</span></span>

#### <a name="keyword_netherlands_bsn"></a><span data-ttu-id="31aad-2808">Keyword_netherlands_bsn</span><span class="sxs-lookup"><span data-stu-id="31aad-2808">Keyword_netherlands_bsn</span></span>

- <span data-ttu-id="31aad-2809">Citizen service number</span><span class="sxs-lookup"><span data-stu-id="31aad-2809">Citizen service number</span></span> 
- <span data-ttu-id="31aad-2810">BSN</span><span class="sxs-lookup"><span data-stu-id="31aad-2810">BSN</span></span> 
- <span data-ttu-id="31aad-2811">буржерсервиценуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2811">Burgerservicenummer</span></span> 
- <span data-ttu-id="31aad-2812">софинуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2812">Sofinummer</span></span> 
- <span data-ttu-id="31aad-2813">Persoonsgebonden nummer</span><span class="sxs-lookup"><span data-stu-id="31aad-2813">Persoonsgebonden nummer</span></span> 
- <span data-ttu-id="31aad-2814">персунснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2814">Persoonsnummer</span></span>    

   
## <a name="new-zealand-ministry-of-health-number"></a><span data-ttu-id="31aad-2815">Номер министерства здравоохранения для Новой Зеландии</span><span class="sxs-lookup"><span data-stu-id="31aad-2815">New Zealand Ministry of Health Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2816">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2816">Format</span></span>

<span data-ttu-id="31aad-2817">Три буквы, пробел (необязательно) и четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-2817">Three letters, a space (optional), and four digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2818">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2818">Pattern</span></span>

<span data-ttu-id="31aad-2819">Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2819">Three letters (not case sensitive) a space (optional) four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2820">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2820">Checksum</span></span>

<span data-ttu-id="31aad-2821">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2821">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2822">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2822">Definition</span></span>

<span data-ttu-id="31aad-2823">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2823">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2824">функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2824">The function Func_new_zealand_ministry_of_health_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2825">находится ключевое слово из Keyword_nz_terms;</span><span class="sxs-lookup"><span data-stu-id="31aad-2825">A keyword from Keyword_nz_terms is found.</span></span>
- <span data-ttu-id="31aad-2826">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2826">The checksum passes.</span></span>

```xml
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

<span data-ttu-id="31aad-2827">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2827">Keywords</span></span>

<span data-ttu-id="31aad-2828">Keyword_nz_terms</span><span class="sxs-lookup"><span data-stu-id="31aad-2828">Keyword_nz_terms</span></span>

- <span data-ttu-id="31aad-2829">нхи</span><span class="sxs-lookup"><span data-stu-id="31aad-2829">NHI</span></span> 
- <span data-ttu-id="31aad-2830">Новая Зеландия</span><span class="sxs-lookup"><span data-stu-id="31aad-2830">New Zealand</span></span> 
- <span data-ttu-id="31aad-2831">Работоспособность</span><span class="sxs-lookup"><span data-stu-id="31aad-2831">Health</span></span> 
- <span data-ttu-id="31aad-2832">обращения</span><span class="sxs-lookup"><span data-stu-id="31aad-2832">treatment</span></span> 
   
## <a name="norway-identification-number"></a><span data-ttu-id="31aad-2833">Идентификационный номер для Норвегии</span><span class="sxs-lookup"><span data-stu-id="31aad-2833">Norway Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2834">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2834">Format</span></span>

<span data-ttu-id="31aad-2835">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2835">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2836">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2836">Pattern</span></span>

<span data-ttu-id="31aad-2837">11 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2837">11 digits:</span></span>
- <span data-ttu-id="31aad-2838">шесть цифр в формате ДДММГГ (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="31aad-2838">Six digits in the format DDMMYY which are the date of birth</span></span> 
- <span data-ttu-id="31aad-2839">индивидуальный номер из трех цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-2839">Three-digit individual number</span></span> 
- <span data-ttu-id="31aad-2840">две проверочные цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-2840">Two check digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2841">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2841">Checksum</span></span>

<span data-ttu-id="31aad-2842">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2842">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2843">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2843">Definition</span></span>

<span data-ttu-id="31aad-2844">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2844">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2845">функция Func_norway_id_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2845">The function Func_norway_id_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2846">находится ключевое слово из Keyword_norway_id_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-2846">A keyword from Keyword_norway_id_number is found.</span></span>
- <span data-ttu-id="31aad-2847">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2847">The checksum passes.</span></span>
- <span data-ttu-id="31aad-2848">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2848">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2849">функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2849">The function Func_norway_id_numbe finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2850">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2850">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2851">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2851">Keywords</span></span>

#### <a name="keyword_norway_id_number"></a><span data-ttu-id="31aad-2852">Keyword_norway_id_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2852">Keyword_norway_id_number</span></span>

- <span data-ttu-id="31aad-2853">Personal identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-2853">Personal identification number</span></span>
- <span data-ttu-id="31aad-2854">Norwegian ID Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2854">Norwegian ID Number</span></span>
- <span data-ttu-id="31aad-2855">ID Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2855">ID Number</span></span>
- <span data-ttu-id="31aad-2856">Процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-2856">Identification</span></span>
- <span data-ttu-id="31aad-2857">персоннуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2857">Personnummer</span></span>
- <span data-ttu-id="31aad-2858">фøдселснуммер</span><span class="sxs-lookup"><span data-stu-id="31aad-2858">Fødselsnummer</span></span>

   
## <a name="philippines-unified-multi-purpose-id-number"></a><span data-ttu-id="31aad-2859">Единый многофункциональный идентификационный номер для Филиппин</span><span class="sxs-lookup"><span data-stu-id="31aad-2859">Philippines Unified Multi-Purpose ID Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2860">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2860">Format</span></span>

<span data-ttu-id="31aad-2861">12 цифр, разделенных дефисами.</span><span class="sxs-lookup"><span data-stu-id="31aad-2861">12 digits separated by hyphens</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2862">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2862">Pattern</span></span>

<span data-ttu-id="31aad-2863">12 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2863">12 digits:</span></span>
- <span data-ttu-id="31aad-2864">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-2864">Four digits</span></span> 
- <span data-ttu-id="31aad-2865">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-2865">A hyphen</span></span> 
- <span data-ttu-id="31aad-2866">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-2866">Seven digits</span></span> 
- <span data-ttu-id="31aad-2867">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-2867">A hyphen</span></span> 
- <span data-ttu-id="31aad-2868">одна цифра.</span><span class="sxs-lookup"><span data-stu-id="31aad-2868">One digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2869">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2869">Checksum</span></span>

<span data-ttu-id="31aad-2870">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2870">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2871">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2871">Definition</span></span>

<span data-ttu-id="31aad-2872">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2872">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2873">регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2873">The regular expression Regex_philippines_unified_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2874">находится ключевое слово из Keyword_philippines_id.</span><span class="sxs-lookup"><span data-stu-id="31aad-2874">A keyword from Keyword_philippines_id is found.</span></span>

```xml
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2875">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2875">Keywords</span></span>
   
#### <a name="keyword_philippines_id"></a><span data-ttu-id="31aad-2876">Keyword_philippines_id</span><span class="sxs-lookup"><span data-stu-id="31aad-2876">Keyword_philippines_id</span></span>

- <span data-ttu-id="31aad-2877">Unified Multi-Purpose ID</span><span class="sxs-lookup"><span data-stu-id="31aad-2877">Unified Multi-Purpose ID</span></span> 
- <span data-ttu-id="31aad-2878">умид</span><span class="sxs-lookup"><span data-stu-id="31aad-2878">UMID</span></span> 
- <span data-ttu-id="31aad-2879">Identity Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2879">Identity Card</span></span> 
- <span data-ttu-id="31aad-2880">Pinag-isang Multi-Layunin ID</span><span class="sxs-lookup"><span data-stu-id="31aad-2880">Pinag-isang Multi-Layunin ID</span></span>
   
## <a name="poland-identity-card"></a><span data-ttu-id="31aad-2881">Номер удостоверения личности для Польши</span><span class="sxs-lookup"><span data-stu-id="31aad-2881">Poland Identity Card</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2882">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2882">Format</span></span>

<span data-ttu-id="31aad-2883">Три буквы и шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2883">Three letters and six digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2884">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2884">Pattern</span></span>

<span data-ttu-id="31aad-2885">Три буквы (без учета регистра), за которыми следуют шесть цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2885">Three letters (not case sensitive) followed by six digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2886">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2886">Checksum</span></span>

<span data-ttu-id="31aad-2887">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2887">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2888">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2888">Definition</span></span>

<span data-ttu-id="31aad-2889">Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Func_polish_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2889">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters: The function Func_polish_national_id finds content that matches the pattern.</span></span>
<span data-ttu-id="31aad-2890">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-2890">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
<span data-ttu-id="31aad-2891">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2891">The checksum passes.</span></span>

```xml
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2892">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2892">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="31aad-2893">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2893">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="31aad-2894">Довóд особисти</span><span class="sxs-lookup"><span data-stu-id="31aad-2894">Dowód osobisty</span></span>
- <span data-ttu-id="31aad-2895">Нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="31aad-2895">Numer dowodu osobistego</span></span>
- <span data-ttu-id="31aad-2896">Назва i нумер доводу особистего</span><span class="sxs-lookup"><span data-stu-id="31aad-2896">Nazwa i numer dowodu osobistego</span></span>
- <span data-ttu-id="31aad-2897">Назва i НР доводу особистего</span><span class="sxs-lookup"><span data-stu-id="31aad-2897">Nazwa i nr dowodu osobistego</span></span>
- <span data-ttu-id="31aad-2898">Nazwa i nr dowodu tożsamości</span><span class="sxs-lookup"><span data-stu-id="31aad-2898">Nazwa i nr dowodu tożsamości</span></span>
- <span data-ttu-id="31aad-2899">Dowód Tożsamości</span><span class="sxs-lookup"><span data-stu-id="31aad-2899">Dowód Tożsamości</span></span>
- <span data-ttu-id="31aad-2900">Dow.</span><span class="sxs-lookup"><span data-stu-id="31aad-2900">dow.</span></span> <span data-ttu-id="31aad-2901">совместим.</span><span class="sxs-lookup"><span data-stu-id="31aad-2901">os.</span></span>

   
## <a name="poland-national-id-pesel"></a><span data-ttu-id="31aad-2902">Национальный идентификатор (PESEL), Польша</span><span class="sxs-lookup"><span data-stu-id="31aad-2902">Poland National ID (PESEL)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2903">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2903">Format</span></span>

<span data-ttu-id="31aad-2904">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2904">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2905">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2905">Pattern</span></span>

<span data-ttu-id="31aad-2906">11 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2906">11 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2907">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2907">Checksum</span></span>

<span data-ttu-id="31aad-2908">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2908">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2909">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2909">Definition</span></span>

<span data-ttu-id="31aad-2910">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2910">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2911">функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2911">The function Func_pesel_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2912">находится ключевое слово из Keyword_pesel_identification_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-2912">A keyword from Keyword_pesel_identification_number is found.</span></span>
- <span data-ttu-id="31aad-2913">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2913">The checksum passes.</span></span>

```xml
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2914">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2914">Keywords</span></span>

#### <a name="keyword_pesel_identification_number"></a><span data-ttu-id="31aad-2915">Keyword_pesel_identification_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2915">Keyword_pesel_identification_number</span></span>

- <span data-ttu-id="31aad-2916">Nr PESEL</span><span class="sxs-lookup"><span data-stu-id="31aad-2916">Nr PESEL</span></span>
- <span data-ttu-id="31aad-2917">PESEL</span><span class="sxs-lookup"><span data-stu-id="31aad-2917">PESEL</span></span>   

   
## <a name="poland-passport"></a><span data-ttu-id="31aad-2918">Номер паспорта для Польши</span><span class="sxs-lookup"><span data-stu-id="31aad-2918">Poland Passport</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2919">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2919">Format</span></span>

<span data-ttu-id="31aad-2920">Две буквы и семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2920">Two letters and seven digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2921">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2921">Pattern</span></span>

<span data-ttu-id="31aad-2922">Две буквы (без учета регистра), за которыми следуют семь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2922">Two letters (not case sensitive) followed by seven digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2923">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2923">Checksum</span></span>

<span data-ttu-id="31aad-2924">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2924">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2925">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2925">Definition</span></span>

<span data-ttu-id="31aad-2926">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2926">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2927">функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2927">The function Func_polish_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2928">находится ключевое слово из Keyword_polish_national_id_passport_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-2928">A keyword from Keyword_polish_national_id_passport_number is found.</span></span>
- <span data-ttu-id="31aad-2929">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2929">The checksum passes.</span></span>

```xml
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2930">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2930">Keywords</span></span>

#### <a name="keyword_polish_national_id_passport_number"></a><span data-ttu-id="31aad-2931">Keyword_polish_national_id_passport_number</span><span class="sxs-lookup"><span data-stu-id="31aad-2931">Keyword_polish_national_id_passport_number</span></span>

- <span data-ttu-id="31aad-2932">Нумер пасзпорту</span><span class="sxs-lookup"><span data-stu-id="31aad-2932">Numer paszportu</span></span>
- <span data-ttu-id="31aad-2933">НР.</span><span class="sxs-lookup"><span data-stu-id="31aad-2933">Nr.</span></span> <span data-ttu-id="31aad-2934">пасзпорту</span><span class="sxs-lookup"><span data-stu-id="31aad-2934">Paszportu</span></span>
- <span data-ttu-id="31aad-2935">пасзпорт</span><span class="sxs-lookup"><span data-stu-id="31aad-2935">Paszport</span></span>

   
## <a name="portugal-citizen-card-number"></a><span data-ttu-id="31aad-2936">Номер карты гражданина Португалии</span><span class="sxs-lookup"><span data-stu-id="31aad-2936">Portugal Citizen Card Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2937">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2937">Format</span></span>

<span data-ttu-id="31aad-2938">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2938">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2939">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2939">Pattern</span></span>

<span data-ttu-id="31aad-2940">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2940">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2941">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2941">Checksum</span></span>

<span data-ttu-id="31aad-2942">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2942">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2943">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2943">Definition</span></span>

<span data-ttu-id="31aad-2944">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2944">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2945">регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2945">The regular expression Regex_portugal_citizen_card finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2946">находится ключевое слово из Keyword_portugal_citizen_card.</span><span class="sxs-lookup"><span data-stu-id="31aad-2946">A keyword from Keyword_portugal_citizen_card is found.</span></span>

```xml
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-2947">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2947">Keywords</span></span>

#### <a name="keyword_portugal_citizen_card"></a><span data-ttu-id="31aad-2948">Keyword_portugal_citizen_card</span><span class="sxs-lookup"><span data-stu-id="31aad-2948">Keyword_portugal_citizen_card</span></span>

- <span data-ttu-id="31aad-2949">Citizen Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2949">Citizen Card</span></span>
- <span data-ttu-id="31aad-2950">National ID Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2950">National ID Card</span></span>
- <span data-ttu-id="31aad-2951">CC</span><span class="sxs-lookup"><span data-stu-id="31aad-2951">CC</span></span>
- <span data-ttu-id="31aad-2952">Cartão de Cidadão</span><span class="sxs-lookup"><span data-stu-id="31aad-2952">Cartão de Cidadão</span></span>
- <span data-ttu-id="31aad-2953">Bilhete de Identidade</span><span class="sxs-lookup"><span data-stu-id="31aad-2953">Bilhete de Identidade</span></span>
   
## <a name="saudi-arabia-national-id"></a><span data-ttu-id="31aad-2954">Национальный идентификатор для Саудовской Аравии</span><span class="sxs-lookup"><span data-stu-id="31aad-2954">Saudi Arabia National ID</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2955">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2955">Format</span></span>

<span data-ttu-id="31aad-2956">10 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2956">10 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2957">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2957">Pattern</span></span>

<span data-ttu-id="31aad-2958">10 последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2958">10 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2959">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2959">Checksum</span></span>

<span data-ttu-id="31aad-2960">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-2960">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2961">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2961">Definition</span></span>

<span data-ttu-id="31aad-2962">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2962">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2963">регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2963">The regular expression Regex_saudi_arabia_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2964">находится ключевое слово из Keyword_saudi_arabia_national_id.</span><span class="sxs-lookup"><span data-stu-id="31aad-2964">A keyword from Keyword_saudi_arabia_national_id is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2965">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2965">Keywords</span></span>

#### <a name="keyword_saudi_arabia_national_id"></a><span data-ttu-id="31aad-2966">Keyword_saudi_arabia_national_id</span><span class="sxs-lookup"><span data-stu-id="31aad-2966">Keyword_saudi_arabia_national_id</span></span>

- <span data-ttu-id="31aad-2967">Identification Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2967">Identification Card</span></span> 
- <span data-ttu-id="31aad-2968">I card number</span><span class="sxs-lookup"><span data-stu-id="31aad-2968">I card number</span></span> 
- <span data-ttu-id="31aad-2969">ID number</span><span class="sxs-lookup"><span data-stu-id="31aad-2969">ID number</span></span> 
- <span data-ttu-id="31aad-2970">الوطنية الهوية بطاقة رقم</span><span class="sxs-lookup"><span data-stu-id="31aad-2970">الوطنية الهوية بطاقة رقم</span></span> 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a><span data-ttu-id="31aad-2971">Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)</span><span class="sxs-lookup"><span data-stu-id="31aad-2971">Singapore National Registration Identity Card (NRIC) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-2972">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-2972">Format</span></span>

<span data-ttu-id="31aad-2973">Девять букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-2973">Nine letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-2974">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-2974">Pattern</span></span>

- <span data-ttu-id="31aad-2975">Девять букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-2975">Nine letters and digits:</span></span>
- <span data-ttu-id="31aad-2976">буква "F", "G", "S" или "T" (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-2976">The letter "F", "G", "S", or "T" (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-2977">семь цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-2977">Seven digits</span></span> 
- <span data-ttu-id="31aad-2978">алфавитный проверочный символ.</span><span class="sxs-lookup"><span data-stu-id="31aad-2978">An alphabetic check digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-2979">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-2979">Checksum</span></span>

<span data-ttu-id="31aad-2980">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-2980">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-2981">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-2981">Definition</span></span>

<span data-ttu-id="31aad-2982">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2982">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2983">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2983">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2984">находится ключевое слово из Keyword_singapore_nric;</span><span class="sxs-lookup"><span data-stu-id="31aad-2984">A keyword from Keyword_singapore_nric is found.</span></span>
- <span data-ttu-id="31aad-2985">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2985">The checksum passes.</span></span>

<span data-ttu-id="31aad-2986">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-2986">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-2987">регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-2987">The regular expression Regex_singapore_nric finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-2988">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-2988">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-2989">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-2989">Keywords</span></span>
   
#### <a name="keyword_singapore_nric"></a><span data-ttu-id="31aad-2990">Keyword_singapore_nric</span><span class="sxs-lookup"><span data-stu-id="31aad-2990">Keyword_singapore_nric</span></span>

- <span data-ttu-id="31aad-2991">National Registration Identity Card</span><span class="sxs-lookup"><span data-stu-id="31aad-2991">National Registration Identity Card</span></span> 
- <span data-ttu-id="31aad-2992">Identity Card Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2992">Identity Card Number</span></span> 
- <span data-ttu-id="31aad-2993">NRIC</span><span class="sxs-lookup"><span data-stu-id="31aad-2993">NRIC</span></span> 
- <span data-ttu-id="31aad-2994">ВНУТРЕННИХ</span><span class="sxs-lookup"><span data-stu-id="31aad-2994">IC</span></span> 
- <span data-ttu-id="31aad-2995">Foreign Identification Number</span><span class="sxs-lookup"><span data-stu-id="31aad-2995">Foreign Identification Number</span></span> 
- <span data-ttu-id="31aad-2996">ПРОЦЕНТ</span><span class="sxs-lookup"><span data-stu-id="31aad-2996">FIN</span></span> 
- <span data-ttu-id="31aad-2997">身份证</span><span class="sxs-lookup"><span data-stu-id="31aad-2997">身份证</span></span> 
- <span data-ttu-id="31aad-2998">身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-2998">身份證</span></span> 
   
## <a name="south-africa-identification-number"></a><span data-ttu-id="31aad-2999">Идентификационный номер для Южной Африки</span><span class="sxs-lookup"><span data-stu-id="31aad-2999">South Africa Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3000">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3000">Format</span></span>

<span data-ttu-id="31aad-3001">13 цифр, которые могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="31aad-3001">13 digits that may contain spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3002">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3002">Pattern</span></span>

<span data-ttu-id="31aad-3003">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-3003">13 digits:</span></span>
- <span data-ttu-id="31aad-3004">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="31aad-3004">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="31aad-3005">четыре цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-3005">Four digits</span></span> 
- <span data-ttu-id="31aad-3006">индикатор гражданства в виде одной цифры;</span><span class="sxs-lookup"><span data-stu-id="31aad-3006">A single-digit citizenship indicator</span></span> 
- <span data-ttu-id="31aad-3007">цифра "8" или "9";</span><span class="sxs-lookup"><span data-stu-id="31aad-3007">The digit "8" or "9"</span></span> 
- <span data-ttu-id="31aad-3008">одна цифра (проверочная).</span><span class="sxs-lookup"><span data-stu-id="31aad-3008">One digit which is a checksum digit</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3009">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3009">Checksum</span></span>

<span data-ttu-id="31aad-3010">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3010">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3011">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3011">Definition</span></span>

<span data-ttu-id="31aad-3012">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3012">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3013">функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3013">The function Func_south_africa_identification_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3014">находится ключевое слово из Keyword_south_africa_identification_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-3014">A keyword from Keyword_south_africa_identification_number is found.</span></span>
- <span data-ttu-id="31aad-3015">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3015">The checksum passes.</span></span>

```xml
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3016">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3016">Keywords</span></span>
   
#### <a name="keyword_south_africa_identification_number"></a><span data-ttu-id="31aad-3017">Keyword_south_africa_identification_number</span><span class="sxs-lookup"><span data-stu-id="31aad-3017">Keyword_south_africa_identification_number</span></span>

- <span data-ttu-id="31aad-3018">Identity card</span><span class="sxs-lookup"><span data-stu-id="31aad-3018">Identity card</span></span>
- <span data-ttu-id="31aad-3019">ID</span><span class="sxs-lookup"><span data-stu-id="31aad-3019">ID</span></span>
- <span data-ttu-id="31aad-3020">Процедура</span><span class="sxs-lookup"><span data-stu-id="31aad-3020">Identification</span></span> 
   
## <a name="south-korea-resident-registration-number"></a><span data-ttu-id="31aad-3021">Регистрационный номер жителя Южной Кореи</span><span class="sxs-lookup"><span data-stu-id="31aad-3021">South Korea Resident Registration Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3022">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3022">Format</span></span>

<span data-ttu-id="31aad-3023">13 цифр, содержащих дефис.</span><span class="sxs-lookup"><span data-stu-id="31aad-3023">13 digits containing a hyphen</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3024">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3024">Pattern</span></span>

<span data-ttu-id="31aad-3025">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-3025">13 digits:</span></span>
- <span data-ttu-id="31aad-3026">шесть цифр в формате ГГММДД (дата рождения);</span><span class="sxs-lookup"><span data-stu-id="31aad-3026">Six digits in the format YYMMDD which are the date of birth</span></span> 
- <span data-ttu-id="31aad-3027">дефис;</span><span class="sxs-lookup"><span data-stu-id="31aad-3027">A hyphen</span></span> 
- <span data-ttu-id="31aad-3028">одна цифра (определяет век и пол);</span><span class="sxs-lookup"><span data-stu-id="31aad-3028">One digit determined by the century and gender</span></span> 
- <span data-ttu-id="31aad-3029">код региона рождения из четырех цифр;</span><span class="sxs-lookup"><span data-stu-id="31aad-3029">Four-digit region-of-birth code</span></span> 
- <span data-ttu-id="31aad-3030">одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают;</span><span class="sxs-lookup"><span data-stu-id="31aad-3030">One digit used to differentiate people for whom the preceding numbers are identical</span></span> 
- <span data-ttu-id="31aad-3031">проверочная цифра.</span><span class="sxs-lookup"><span data-stu-id="31aad-3031">A check digit.</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3032">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3032">Checksum</span></span>

<span data-ttu-id="31aad-3033">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3033">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3034">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3034">Definition</span></span>

<span data-ttu-id="31aad-3035">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3035">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3036">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3036">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3037">находится ключевое слово из Keyword_south_korea_resident_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-3037">A keyword from Keyword_south_korea_resident_number is found.</span></span>
- <span data-ttu-id="31aad-3038">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3038">The checksum passes.</span></span>

<span data-ttu-id="31aad-3039">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3039">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3040">функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3040">The function Func_south_korea_resident_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3041">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3041">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3042">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3042">Keywords</span></span>
   
#### <a name="keyword_south_korea_resident_number"></a><span data-ttu-id="31aad-3043">Keyword_south_korea_resident_number</span><span class="sxs-lookup"><span data-stu-id="31aad-3043">Keyword_south_korea_resident_number</span></span>

- <span data-ttu-id="31aad-3044">National ID card</span><span class="sxs-lookup"><span data-stu-id="31aad-3044">National ID card</span></span> 
- <span data-ttu-id="31aad-3045">Citizen's Registration Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3045">Citizen's Registration Number</span></span> 
- <span data-ttu-id="31aad-3046">Jumin deungnok beonho</span><span class="sxs-lookup"><span data-stu-id="31aad-3046">Jumin deungnok beonho</span></span> 
- <span data-ttu-id="31aad-3047">ррн</span><span class="sxs-lookup"><span data-stu-id="31aad-3047">RRN</span></span> 
- <span data-ttu-id="31aad-3048">주민등록번호</span><span class="sxs-lookup"><span data-stu-id="31aad-3048">주민등록번호</span></span>
   
## <a name="spain-social-security-number-ssn"></a><span data-ttu-id="31aad-3049">Страховой номер для Испании (SSN)</span><span class="sxs-lookup"><span data-stu-id="31aad-3049">Spain Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3050">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3050">Format</span></span>

<span data-ttu-id="31aad-3051">11–12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3051">11-12 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3052">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3052">Pattern</span></span>

<span data-ttu-id="31aad-3053">11-12 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-3053">11-12 digits:</span></span>
- <span data-ttu-id="31aad-3054">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3054">Two digits</span></span> 
- <span data-ttu-id="31aad-3055">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="31aad-3055">A forward slash (optional)</span></span> 
- <span data-ttu-id="31aad-3056">7–8 цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3056">7-8 digits</span></span> 
- <span data-ttu-id="31aad-3057">Косая черта (необязательно)</span><span class="sxs-lookup"><span data-stu-id="31aad-3057">A forward slash (optional)</span></span> 
- <span data-ttu-id="31aad-3058">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3058">Two digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3059">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3059">Checksum</span></span>

<span data-ttu-id="31aad-3060">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3060">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3061">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3061">Definition</span></span>

<span data-ttu-id="31aad-3062">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3062">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3063">функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3063">The function Func_spanish_social_security_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3064">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3064">The checksum passes.</span></span>

```xml
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3065">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3065">Keywords</span></span>

<span data-ttu-id="31aad-3066">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3066">None</span></span>

## <a name="sql-server-connection-string"></a><span data-ttu-id="31aad-3067">Строка подключения к SQL Server</span><span class="sxs-lookup"><span data-stu-id="31aad-3067">SQL Server Connection String</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3068">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3068">Format</span></span>

<span data-ttu-id="31aad-3069">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId", за которыми следуют символы и строки, описанные в приведенном ниже шаблоне.</span><span class="sxs-lookup"><span data-stu-id="31aad-3069">The string "User Id", "User ID", "uid", or "UserId" followed by the characters and strings outlined in the pattern below.</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3070">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3070">Pattern</span></span>

- <span data-ttu-id="31aad-3071">Строка "идентификатор пользователя", "идентификатор пользователя", "UID" или "UserId"</span><span class="sxs-lookup"><span data-stu-id="31aad-3071">The string "User Id", "User ID", "uid", or "UserId"</span></span>
- <span data-ttu-id="31aad-3072">Любая комбинация из 1-200 прописных или строчных букв, цифр, символов, специальных символов и пробелов.</span><span class="sxs-lookup"><span data-stu-id="31aad-3072">Any combination of between 1-200 lower- or uppercase letters, digits, symbols, special characters, or spaces</span></span>
- <span data-ttu-id="31aad-3073">Строка "Password" или "pwd", где "pwd" не предшествует буква нижнего регистра</span><span class="sxs-lookup"><span data-stu-id="31aad-3073">The string "Password" or "pwd" where "pwd" is not preceded by a lowercase letter</span></span>
- <span data-ttu-id="31aad-3074">Знак равенства (=);</span><span class="sxs-lookup"><span data-stu-id="31aad-3074">An equal sign (=)</span></span>
- <span data-ttu-id="31aad-3075">Любой символ, не являющийся знаком доллара ($), символ процента (%), символ "больше" (>), символ "@", "символ" (@), знак кавычек ("), точка с запятой (;), левая фигурная скобка ([) или левая квадратная скобка ({)</span><span class="sxs-lookup"><span data-stu-id="31aad-3075">Any character that is not a dollar sign ($), percent symbol (%), greater than symbol (>), at symbol (@), quotation mark ("), semicolon (;), left brace ([), or left bracket ({)</span></span>
- <span data-ttu-id="31aad-3076">Любая комбинация 7-128 символов, не отделяющая точку с запятой (;), косая черта (/) или кавычки (").</span><span class="sxs-lookup"><span data-stu-id="31aad-3076">Any combination of 7-128 characters that are not a semicolon (;), forward slash (/), or quotation mark (")</span></span>
- <span data-ttu-id="31aad-3077">Точка с запятой (;) или кавычки (")</span><span class="sxs-lookup"><span data-stu-id="31aad-3077">A semicolon (;) or quotation mark (")</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3078">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3078">Checksum</span></span>

<span data-ttu-id="31aad-3079">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3079">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3080">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3080">Definition</span></span>

<span data-ttu-id="31aad-3081">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3081">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3082">Регулярное выражение CEP_Regex_SQLServerConnectionString находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3082">The regular expression CEP_Regex_SQLServerConnectionString finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3083">**Не** найдено ключевое слово из CEP_GlobalFilter.</span><span class="sxs-lookup"><span data-stu-id="31aad-3083">A keyword from CEP_GlobalFilter is **not** found.</span></span>
- <span data-ttu-id="31aad-3084">Регулярное выражение CEP_PasswordPlaceHolder не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3084">The regular expression CEP_PasswordPlaceHolder does **not** find content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3085">Регулярное выражение CEP_CommonExampleKeywords не \*\*\*\* находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3085">The regular expression CEP_CommonExampleKeywords does **not** find content that matches the pattern.</span></span>

```sql
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

### <a name="keywords"></a><span data-ttu-id="31aad-3086">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3086">Keywords</span></span>

#### <a name="cep_globalfilter"></a><span data-ttu-id="31aad-3087">CEP_GlobalFilter</span><span class="sxs-lookup"><span data-stu-id="31aad-3087">CEP_GlobalFilter</span></span>

- <span data-ttu-id="31aad-3088">Некоторые пароли</span><span class="sxs-lookup"><span data-stu-id="31aad-3088">some-password</span></span>
- <span data-ttu-id="31aad-3089">сомепассворд</span><span class="sxs-lookup"><span data-stu-id="31aad-3089">somepassword</span></span>
- <span data-ttu-id="31aad-3090">секретпассворд</span><span class="sxs-lookup"><span data-stu-id="31aad-3090">secretPassword</span></span>
- <span data-ttu-id="31aad-3091">примером</span><span class="sxs-lookup"><span data-stu-id="31aad-3091">sample</span></span>

#### <a name="cep_passwordplaceholder"></a><span data-ttu-id="31aad-3092">CEP_PasswordPlaceHolder</span><span class="sxs-lookup"><span data-stu-id="31aad-3092">CEP_PasswordPlaceHolder</span></span>

<span data-ttu-id="31aad-3093">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-3093">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-3094">Пароль или pwd, за которым следует 0-2 пробелов, знак равенства (=), 0-2 пробелы и звездочка (\*)--или--</span><span class="sxs-lookup"><span data-stu-id="31aad-3094">Password or pwd followed by 0-2 spaces, an equal sign (=), 0-2 spaces, and an asterisk (\*) --OR--</span></span>
- <span data-ttu-id="31aad-3095">Пароль или pwd, а затем:</span><span class="sxs-lookup"><span data-stu-id="31aad-3095">Password or pwd followed by:</span></span>
    - <span data-ttu-id="31aad-3096">Знак равенства (=)</span><span class="sxs-lookup"><span data-stu-id="31aad-3096">Equal sign (=)</span></span>
    - <span data-ttu-id="31aad-3097">Символ "меньше" (<)</span><span class="sxs-lookup"><span data-stu-id="31aad-3097">Less than symbol (<)</span></span>
    - <span data-ttu-id="31aad-3098">Любое сочетание 1-200 символов, которые являются буквами верхнего или нижнего регистра, цифрами, звездочкой (\*), дефисом (-), подчеркиванием (_) или символом пробела</span><span class="sxs-lookup"><span data-stu-id="31aad-3098">Any combination of 1-200 characters that are upper- or lowercase letters, digits, an asterisk (\*), hyphen (-), underline (_), or whitespace character</span></span>
    - <span data-ttu-id="31aad-3099">Символ "больше" (>)</span><span class="sxs-lookup"><span data-stu-id="31aad-3099">Greater than symbol (>)</span></span>

#### <a name="cep_commonexamplekeywords"></a><span data-ttu-id="31aad-3100">CEP_CommonExampleKeywords</span><span class="sxs-lookup"><span data-stu-id="31aad-3100">CEP_CommonExampleKeywords</span></span>

<span data-ttu-id="31aad-3101">(Технически, обратите внимание, что этот тип конфиденциальной информации определяет эти ключевые слова с помощью регулярного выражения, а не списка ключевых слов.)</span><span class="sxs-lookup"><span data-stu-id="31aad-3101">(Note that technically, this sensitive information type identifies these keywords by using a regular expression, not a keyword list.)</span></span>

- <span data-ttu-id="31aad-3102">компанией</span><span class="sxs-lookup"><span data-stu-id="31aad-3102">contoso</span></span>
- <span data-ttu-id="31aad-3103">компании</span><span class="sxs-lookup"><span data-stu-id="31aad-3103">fabrikam</span></span>
- <span data-ttu-id="31aad-3104">базу</span><span class="sxs-lookup"><span data-stu-id="31aad-3104">northwind</span></span>
- <span data-ttu-id="31aad-3105">песочниц</span><span class="sxs-lookup"><span data-stu-id="31aad-3105">sandbox</span></span>
- <span data-ttu-id="31aad-3106">онебокс</span><span class="sxs-lookup"><span data-stu-id="31aad-3106">onebox</span></span>
- <span data-ttu-id="31aad-3107">localhost</span><span class="sxs-lookup"><span data-stu-id="31aad-3107">localhost</span></span>
- <span data-ttu-id="31aad-3108">127.0.0.1</span><span class="sxs-lookup"><span data-stu-id="31aad-3108">127.0.0.1</span></span>
- <span data-ttu-id="31aad-3109">тестакс.</span><span class="sxs-lookup"><span data-stu-id="31aad-3109">testacs.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-3110">порта</span><span class="sxs-lookup"><span data-stu-id="31aad-3110">com</span></span>
- <span data-ttu-id="31aad-3111">s — int.</span><span class="sxs-lookup"><span data-stu-id="31aad-3111">s-int.</span></span><!--no-hyperlink--><span data-ttu-id="31aad-3112">команде</span><span class="sxs-lookup"><span data-stu-id="31aad-3112">net</span></span>

## <a name="sweden-national-id"></a><span data-ttu-id="31aad-3113">Национальный идентификатор для Швеции</span><span class="sxs-lookup"><span data-stu-id="31aad-3113">Sweden National ID</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3114">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3114">Format</span></span>

<span data-ttu-id="31aad-3115">10 или 12 цифр и дополнительный разделитель.</span><span class="sxs-lookup"><span data-stu-id="31aad-3115">10 or 12 digits and an optional delimiter</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3116">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3116">Pattern</span></span>

<span data-ttu-id="31aad-3117">10 или 12 цифр с необязательным разделителем</span><span class="sxs-lookup"><span data-stu-id="31aad-3117">10 or 12 digits and an optional delimiter:</span></span>
- <span data-ttu-id="31aad-3118">2–4 цифры (необязательно)</span><span class="sxs-lookup"><span data-stu-id="31aad-3118">2-4 digits (optional)</span></span> 
- <span data-ttu-id="31aad-3119">Шесть цифр в формате даты ГГММДД.</span><span class="sxs-lookup"><span data-stu-id="31aad-3119">Six digits in date format YYMMDD</span></span> 
- <span data-ttu-id="31aad-3120">Разделитель - или + (необязательно)</span><span class="sxs-lookup"><span data-stu-id="31aad-3120">Delimiter of "-" or "+" (optional), plus</span></span>
- <span data-ttu-id="31aad-3121">четыре цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-3121">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3122">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3122">Checksum</span></span>

<span data-ttu-id="31aad-3123">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3123">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3124">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3124">Definition</span></span>

<span data-ttu-id="31aad-3125">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3125">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3126">функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3126">The function Func_swedish_national_identifier finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3127">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3127">The checksum passes.</span></span>

```xml
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3128">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3128">Keywords</span></span>

<span data-ttu-id="31aad-3129">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3129">No</span></span>
   
## <a name="sweden-passport-number"></a><span data-ttu-id="31aad-3130">Номер паспорта гражданина Швеции</span><span class="sxs-lookup"><span data-stu-id="31aad-3130">Sweden Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3131">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3131">Format</span></span>

<span data-ttu-id="31aad-3132">Восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3132">Eight digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3133">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3133">Pattern</span></span>

<span data-ttu-id="31aad-3134">Восемь последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3134">Eight consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3135">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3135">Checksum</span></span>

<span data-ttu-id="31aad-3136">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3136">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3137">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3137">Definition</span></span>

<span data-ttu-id="31aad-3138">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3138">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3139">Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3139">The regular expression Regex_sweden_passport_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3140">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-3140">One of the following is true:</span></span>
    - <span data-ttu-id="31aad-3141">найдено ключевое слово из Keyword_passport;</span><span class="sxs-lookup"><span data-stu-id="31aad-3141">A keyword from Keyword_passport is found.</span></span>
    - <span data-ttu-id="31aad-3142">найдено ключевое слово из Keyword_sweden_passport.</span><span class="sxs-lookup"><span data-stu-id="31aad-3142">A keyword from Keyword_sweden_passport is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3143">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3143">Keywords</span></span>
   
#### <a name="keyword_sweden_passport"></a><span data-ttu-id="31aad-3144">Keyword_sweden_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-3144">Keyword_sweden_passport</span></span>

- <span data-ttu-id="31aad-3145">visa requirements</span><span class="sxs-lookup"><span data-stu-id="31aad-3145">visa requirements</span></span> 
- <span data-ttu-id="31aad-3146">Alien Registration Card</span><span class="sxs-lookup"><span data-stu-id="31aad-3146">Alien Registration Card</span></span> 
- <span data-ttu-id="31aad-3147">Schengen visas</span><span class="sxs-lookup"><span data-stu-id="31aad-3147">Schengen visas</span></span> 
- <span data-ttu-id="31aad-3148">Schengen visa</span><span class="sxs-lookup"><span data-stu-id="31aad-3148">Schengen visa</span></span> 
- <span data-ttu-id="31aad-3149">Visa Processing</span><span class="sxs-lookup"><span data-stu-id="31aad-3149">Visa Processing</span></span> 
- <span data-ttu-id="31aad-3150">Visa Type</span><span class="sxs-lookup"><span data-stu-id="31aad-3150">Visa Type</span></span> 
- <span data-ttu-id="31aad-3151">Single Entry</span><span class="sxs-lookup"><span data-stu-id="31aad-3151">Single Entry</span></span> 
- <span data-ttu-id="31aad-3152">Multiple Entry</span><span class="sxs-lookup"><span data-stu-id="31aad-3152">Multiple Entry</span></span> 
- <span data-ttu-id="31aad-3153">G3 Processing Fees</span><span class="sxs-lookup"><span data-stu-id="31aad-3153">G3 Processing Fees</span></span> 

#### <a name="keyword_passport"></a><span data-ttu-id="31aad-3154">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-3154">Keyword_passport</span></span>

- <span data-ttu-id="31aad-3155">Passport Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3155">Passport Number</span></span> 
- <span data-ttu-id="31aad-3156">Passport No</span><span class="sxs-lookup"><span data-stu-id="31aad-3156">Passport No</span></span> 
- <span data-ttu-id="31aad-3157">Passport#</span><span class="sxs-lookup"><span data-stu-id="31aad-3157">Passport #</span></span> 
- <span data-ttu-id="31aad-3158">Службу #</span><span class="sxs-lookup"><span data-stu-id="31aad-3158">Passport#</span></span> 
- <span data-ttu-id="31aad-3159">пасспортид</span><span class="sxs-lookup"><span data-stu-id="31aad-3159">PassportID</span></span> 
- <span data-ttu-id="31aad-3160">пасспортно</span><span class="sxs-lookup"><span data-stu-id="31aad-3160">Passportno</span></span> 
- <span data-ttu-id="31aad-3161">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-3161">passportnumber</span></span> 
- <span data-ttu-id="31aad-3162">パスポート</span><span class="sxs-lookup"><span data-stu-id="31aad-3162">パスポート</span></span> 
- <span data-ttu-id="31aad-3163">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="31aad-3163">パスポート番号</span></span> 
- <span data-ttu-id="31aad-3164">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="31aad-3164">パスポートのNum</span></span> 
- <span data-ttu-id="31aad-3165">パスポート #</span><span class="sxs-lookup"><span data-stu-id="31aad-3165">パスポート＃</span></span> 
- <span data-ttu-id="31aad-3166">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="31aad-3166">Numéro de passeport</span></span> 
- <span data-ttu-id="31aad-3167">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="31aad-3167">Passeport n °</span></span> 
- <span data-ttu-id="31aad-3168">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="31aad-3168">Passeport Non</span></span> 
- <span data-ttu-id="31aad-3169">Passeport#</span><span class="sxs-lookup"><span data-stu-id="31aad-3169">Passeport #</span></span> 
- <span data-ttu-id="31aad-3170">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="31aad-3170">Passeport#</span></span> 
- <span data-ttu-id="31aad-3171">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="31aad-3171">PasseportNon</span></span> 
- <span data-ttu-id="31aad-3172">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="31aad-3172">Passeportn °</span></span> 
   
## <a name="swift-code"></a><span data-ttu-id="31aad-3173">Код SWIFT</span><span class="sxs-lookup"><span data-stu-id="31aad-3173">SWIFT Code</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3174">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3174">Format</span></span>

<span data-ttu-id="31aad-3175">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-3175">Four letters followed by 5-31 letters or digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3176">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3176">Pattern</span></span>

<span data-ttu-id="31aad-3177">Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3177">Four letters followed by 5-31 letters or digits:</span></span>
- <span data-ttu-id="31aad-3178">Четырехбуквенный код банка (без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-3178">Four-letter bank code (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-3179">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-3179">An optional space</span></span> 
- <span data-ttu-id="31aad-3180">4–28 букв или цифр (основной номер банковского счета, BBAN)</span><span class="sxs-lookup"><span data-stu-id="31aad-3180">4-28 letters or digits (the Basic Bank Account Number (BBAN))</span></span> 
- <span data-ttu-id="31aad-3181">Необязательный пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-3181">An optional space</span></span> 
- <span data-ttu-id="31aad-3182">1–3 буквы или цифры (оставшаяся часть BBAN)</span><span class="sxs-lookup"><span data-stu-id="31aad-3182">1-3 letters or digits (remainder of the BBAN)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3183">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3183">Checksum</span></span>

<span data-ttu-id="31aad-3184">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3184">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3185">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3185">Definition</span></span>

<span data-ttu-id="31aad-3186">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3186">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3187">регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3187">The regular expression Regex_swift finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3188">находится ключевое слово из Keyword_swift.</span><span class="sxs-lookup"><span data-stu-id="31aad-3188">A keyword from Keyword_swift is found.</span></span>

```xml
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3189">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3189">Keywords</span></span>
   
#### <a name="keyword_swift"></a><span data-ttu-id="31aad-3190">Keyword_swift</span><span class="sxs-lookup"><span data-stu-id="31aad-3190">Keyword_swift</span></span>

- <span data-ttu-id="31aad-3191">international organization for standardization 9362</span><span class="sxs-lookup"><span data-stu-id="31aad-3191">international organization for standardization 9362</span></span> 
- <span data-ttu-id="31aad-3192">iso 9362</span><span class="sxs-lookup"><span data-stu-id="31aad-3192">iso 9362</span></span> 
- <span data-ttu-id="31aad-3193">iso9362</span><span class="sxs-lookup"><span data-stu-id="31aad-3193">iso9362</span></span> 
- <span data-ttu-id="31aad-3194">SWIFT\#</span><span class="sxs-lookup"><span data-stu-id="31aad-3194">swift\#</span></span> 
- <span data-ttu-id="31aad-3195">свифткоде</span><span class="sxs-lookup"><span data-stu-id="31aad-3195">swiftcode</span></span> 
- <span data-ttu-id="31aad-3196">свифтнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-3196">swiftnumber</span></span> 
- <span data-ttu-id="31aad-3197">свифтраутингнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-3197">swiftroutingnumber</span></span> 
- <span data-ttu-id="31aad-3198">swift code</span><span class="sxs-lookup"><span data-stu-id="31aad-3198">swift code</span></span> 
- <span data-ttu-id="31aad-3199">swift number #</span><span class="sxs-lookup"><span data-stu-id="31aad-3199">swift number #</span></span> 
- <span data-ttu-id="31aad-3200">swift routing number</span><span class="sxs-lookup"><span data-stu-id="31aad-3200">swift routing number</span></span> 
- <span data-ttu-id="31aad-3201">bic number</span><span class="sxs-lookup"><span data-stu-id="31aad-3201">bic number</span></span> 
- <span data-ttu-id="31aad-3202">bic code</span><span class="sxs-lookup"><span data-stu-id="31aad-3202">bic code</span></span> 
- <span data-ttu-id="31aad-3203">БИК\#</span><span class="sxs-lookup"><span data-stu-id="31aad-3203">bic \#</span></span> 
- <span data-ttu-id="31aad-3204">БИК\#</span><span class="sxs-lookup"><span data-stu-id="31aad-3204">bic\#</span></span> 
- <span data-ttu-id="31aad-3205">bank identifier code</span><span class="sxs-lookup"><span data-stu-id="31aad-3205">bank identifier code</span></span> 
- <span data-ttu-id="31aad-3206">標準化 9362</span><span class="sxs-lookup"><span data-stu-id="31aad-3206">標準化9362</span></span> 
- <span data-ttu-id="31aad-3207">迅速 #</span><span class="sxs-lookup"><span data-stu-id="31aad-3207">迅速＃</span></span> 
- <span data-ttu-id="31aad-3208">свифтコード</span><span class="sxs-lookup"><span data-stu-id="31aad-3208">SWIFTコード</span></span> 
- <span data-ttu-id="31aad-3209">свифт番号</span><span class="sxs-lookup"><span data-stu-id="31aad-3209">SWIFT番号</span></span> 
- <span data-ttu-id="31aad-3210">迅速なルーティング番号</span><span class="sxs-lookup"><span data-stu-id="31aad-3210">迅速なルーティング番号</span></span> 
- <span data-ttu-id="31aad-3211">бик番号</span><span class="sxs-lookup"><span data-stu-id="31aad-3211">BIC番号</span></span> 
- <span data-ttu-id="31aad-3212">бикコード</span><span class="sxs-lookup"><span data-stu-id="31aad-3212">BICコード</span></span> 
- <span data-ttu-id="31aad-3213">銀行識別コードのための国際組織</span><span class="sxs-lookup"><span data-stu-id="31aad-3213">銀行識別コードのための国際組織</span></span> 
- <span data-ttu-id="31aad-3214">Organisation internationale de normalisation 9362</span><span class="sxs-lookup"><span data-stu-id="31aad-3214">Organisation internationale de normalisation 9362</span></span> 
- <span data-ttu-id="31aad-3215">Быстрая\#</span><span class="sxs-lookup"><span data-stu-id="31aad-3215">rapide \#</span></span> 
- <span data-ttu-id="31aad-3216">code SWIFT</span><span class="sxs-lookup"><span data-stu-id="31aad-3216">code SWIFT</span></span> 
- <span data-ttu-id="31aad-3217">le numéro de swift</span><span class="sxs-lookup"><span data-stu-id="31aad-3217">le numéro de swift</span></span> 
- <span data-ttu-id="31aad-3218">swift numéro d'acheminement</span><span class="sxs-lookup"><span data-stu-id="31aad-3218">swift numéro d'acheminement</span></span> 
- <span data-ttu-id="31aad-3219">le numéro BIC</span><span class="sxs-lookup"><span data-stu-id="31aad-3219">le numéro BIC</span></span> 
- <span data-ttu-id="31aad-3220">\#БИК</span><span class="sxs-lookup"><span data-stu-id="31aad-3220">\# BIC</span></span> 
- <span data-ttu-id="31aad-3221">code identificateur de banque</span><span class="sxs-lookup"><span data-stu-id="31aad-3221">code identificateur de banque</span></span> 
   
## <a name="taiwan-national-id"></a><span data-ttu-id="31aad-3222">Национальный идентификатор, Тайвань</span><span class="sxs-lookup"><span data-stu-id="31aad-3222">Taiwan National ID</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3223">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3223">Format</span></span>

<span data-ttu-id="31aad-3224">Одна буква (английская), за которой следуют девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3224">One letter (in English) followed by nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3225">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3225">Pattern</span></span>

<span data-ttu-id="31aad-3226">Один символ , за которым следуют девять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3226">One letter (in English) followed by nine digits:</span></span>
- <span data-ttu-id="31aad-3227">Один символ (на английском языке, без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-3227">One letter (in English, not case sensitive)</span></span> 
- <span data-ttu-id="31aad-3228">Цифра 1 или 2</span><span class="sxs-lookup"><span data-stu-id="31aad-3228">The digit "1" or "2"</span></span> 
- <span data-ttu-id="31aad-3229">Восемь цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3229">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3230">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3230">Checksum</span></span>

<span data-ttu-id="31aad-3231">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3231">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3232">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3232">Definition</span></span>

<span data-ttu-id="31aad-3233">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3233">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3234">функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3234">The function Func_taiwanese_national_id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3235">находится ключевое слово из Keyword_taiwanese_national_id;</span><span class="sxs-lookup"><span data-stu-id="31aad-3235">A keyword from Keyword_taiwanese_national_id is found.</span></span>
- <span data-ttu-id="31aad-3236">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3236">The checksum passes.</span></span>

```xml
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3237">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3237">Keywords</span></span>

#### <a name="keyword_taiwanese_national_id"></a><span data-ttu-id="31aad-3238">Keyword_taiwanese_national_id</span><span class="sxs-lookup"><span data-stu-id="31aad-3238">Keyword_taiwanese_national_id</span></span>

- <span data-ttu-id="31aad-3239">身份證字號</span><span class="sxs-lookup"><span data-stu-id="31aad-3239">身份證字號</span></span> 
- <span data-ttu-id="31aad-3240">身份證</span><span class="sxs-lookup"><span data-stu-id="31aad-3240">身份證</span></span> 
- <span data-ttu-id="31aad-3241">身份證號碼</span><span class="sxs-lookup"><span data-stu-id="31aad-3241">身份證號碼</span></span> 
- <span data-ttu-id="31aad-3242">身份證號</span><span class="sxs-lookup"><span data-stu-id="31aad-3242">身份證號</span></span> 
- <span data-ttu-id="31aad-3243">身分證字號</span><span class="sxs-lookup"><span data-stu-id="31aad-3243">身分證字號</span></span> 
- <span data-ttu-id="31aad-3244">身分證</span><span class="sxs-lookup"><span data-stu-id="31aad-3244">身分證</span></span> 
- <span data-ttu-id="31aad-3245">身分證號碼</span><span class="sxs-lookup"><span data-stu-id="31aad-3245">身分證號碼</span></span> 
- <span data-ttu-id="31aad-3246">身份證號</span><span class="sxs-lookup"><span data-stu-id="31aad-3246">身份證號</span></span> 
- <span data-ttu-id="31aad-3247">身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="31aad-3247">身分證統一編號</span></span> 
- <span data-ttu-id="31aad-3248">國民身分證統一編號</span><span class="sxs-lookup"><span data-stu-id="31aad-3248">國民身分證統一編號</span></span> 
- <span data-ttu-id="31aad-3249">簽名</span><span class="sxs-lookup"><span data-stu-id="31aad-3249">簽名</span></span> 
- <span data-ttu-id="31aad-3250">蓋章</span><span class="sxs-lookup"><span data-stu-id="31aad-3250">蓋章</span></span> 
- <span data-ttu-id="31aad-3251">簽名或蓋章</span><span class="sxs-lookup"><span data-stu-id="31aad-3251">簽名或蓋章</span></span> 
- <span data-ttu-id="31aad-3252">簽章</span><span class="sxs-lookup"><span data-stu-id="31aad-3252">簽章</span></span>   
   
## <a name="taiwan-passport-number"></a><span data-ttu-id="31aad-3253">	Номер паспорта гражданина Тайваня</span><span class="sxs-lookup"><span data-stu-id="31aad-3253">Taiwan Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3254">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3254">Format</span></span>

- <span data-ttu-id="31aad-3255">Номер биометрического паспорта: девять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3255">Biometric passport number: Nine digits</span></span>
- <span data-ttu-id="31aad-3256">Номер биометрической службы Passport: девять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3256">Non-biometric passport number: Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3257">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3257">Pattern</span></span>
<span data-ttu-id="31aad-3258">Номер биометрического паспорта:</span><span class="sxs-lookup"><span data-stu-id="31aad-3258">Biometric passport number:</span></span>
- <span data-ttu-id="31aad-3259">цифра "3";</span><span class="sxs-lookup"><span data-stu-id="31aad-3259">The digit "3"</span></span> 
- <span data-ttu-id="31aad-3260">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3260">Eight digits</span></span>

<span data-ttu-id="31aad-3261">Номер биометрической службы Passport:</span><span class="sxs-lookup"><span data-stu-id="31aad-3261">Non-biometric passport number:</span></span>
- <span data-ttu-id="31aad-3262">девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3262">Nine digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3263">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3263">Checksum</span></span>

<span data-ttu-id="31aad-3264">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3264">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3265">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3265">Definition</span></span>

<span data-ttu-id="31aad-3266">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3266">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3267">регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3267">The regular expression Regex_taiwan_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3268">находится ключевое слово из Keyword_taiwan_passport.</span><span class="sxs-lookup"><span data-stu-id="31aad-3268">A keyword from Keyword_taiwan_passport is found.</span></span>

```xml
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3269">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3269">Keywords</span></span>

#### <a name="keyword_taiwan_passport"></a><span data-ttu-id="31aad-3270">Keyword_taiwan_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-3270">Keyword_taiwan_passport</span></span>

- <span data-ttu-id="31aad-3271">ROC passport number</span><span class="sxs-lookup"><span data-stu-id="31aad-3271">ROC passport number</span></span> 
- <span data-ttu-id="31aad-3272">Passport number</span><span class="sxs-lookup"><span data-stu-id="31aad-3272">Passport number</span></span> 
- <span data-ttu-id="31aad-3273">Passport no</span><span class="sxs-lookup"><span data-stu-id="31aad-3273">Passport no</span></span> 
- <span data-ttu-id="31aad-3274">Passport Num</span><span class="sxs-lookup"><span data-stu-id="31aad-3274">Passport Num</span></span> 
- <span data-ttu-id="31aad-3275">Passport #</span><span class="sxs-lookup"><span data-stu-id="31aad-3275">Passport #</span></span> 
- <span data-ttu-id="31aad-3276">护照</span><span class="sxs-lookup"><span data-stu-id="31aad-3276">护照</span></span> 
- <span data-ttu-id="31aad-3277">中華民國護照</span><span class="sxs-lookup"><span data-stu-id="31aad-3277">中華民國護照</span></span> 
- <span data-ttu-id="31aad-3278">Zhōnghuá Mínguó hùzhào</span><span class="sxs-lookup"><span data-stu-id="31aad-3278">Zhōnghuá Mínguó hùzhào</span></span>
   
## <a name="taiwan-resident-certificate-arctarc-number"></a><span data-ttu-id="31aad-3279">Номер удостоверения жителя Тайваня (ARC/TARC)</span><span class="sxs-lookup"><span data-stu-id="31aad-3279">Taiwan Resident Certificate (ARC/TARC) Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3280">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3280">Format</span></span>

<span data-ttu-id="31aad-3281">10 букв и цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3281">10 letters and digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3282">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3282">Pattern</span></span>

<span data-ttu-id="31aad-3283">10 букв и цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-3283">10 letters and digits:</span></span>
- <span data-ttu-id="31aad-3284">две буквы (без учета регистра);</span><span class="sxs-lookup"><span data-stu-id="31aad-3284">Two letters (not case sensitive)</span></span> 
- <span data-ttu-id="31aad-3285">восемь цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3285">Eight digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3286">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3286">Checksum</span></span>

<span data-ttu-id="31aad-3287">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3287">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3288">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3288">Definition</span></span>

<span data-ttu-id="31aad-3289">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3289">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3290">регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3290">The regular expression Regex_taiwan_resident_certificate finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3291">находится ключевое слово из Keyword_taiwan_resident_certificate.</span><span class="sxs-lookup"><span data-stu-id="31aad-3291">A keyword from Keyword_taiwan_resident_certificate is found.</span></span>

```xml
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3292">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3292">Keywords</span></span>

#### <a name="keyword_taiwan_resident_certificate"></a><span data-ttu-id="31aad-3293">Keyword_taiwan_resident_certificate</span><span class="sxs-lookup"><span data-stu-id="31aad-3293">Keyword_taiwan_resident_certificate</span></span>

- <span data-ttu-id="31aad-3294">Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="31aad-3294">Resident Certificate</span></span> 
- <span data-ttu-id="31aad-3295">Resident Cert</span><span class="sxs-lookup"><span data-stu-id="31aad-3295">Resident Cert</span></span> 
- <span data-ttu-id="31aad-3296">Resident Cert.</span><span class="sxs-lookup"><span data-stu-id="31aad-3296">Resident Cert.</span></span> 
- <span data-ttu-id="31aad-3297">Identification card</span><span class="sxs-lookup"><span data-stu-id="31aad-3297">Identification card</span></span> 
- <span data-ttu-id="31aad-3298">Alien Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="31aad-3298">Alien Resident Certificate</span></span> 
- <span data-ttu-id="31aad-3299">ГИПЕРБОЛ</span><span class="sxs-lookup"><span data-stu-id="31aad-3299">ARC</span></span> 
- <span data-ttu-id="31aad-3300">Taiwan Area Resident Certificate</span><span class="sxs-lookup"><span data-stu-id="31aad-3300">Taiwan Area Resident Certificate</span></span> 
- <span data-ttu-id="31aad-3301">TARC</span><span class="sxs-lookup"><span data-stu-id="31aad-3301">TARC</span></span> 
- <span data-ttu-id="31aad-3302">居留證</span><span class="sxs-lookup"><span data-stu-id="31aad-3302">居留證</span></span> 
- <span data-ttu-id="31aad-3303">外僑居留證</span><span class="sxs-lookup"><span data-stu-id="31aad-3303">外僑居留證</span></span> 
- <span data-ttu-id="31aad-3304">台灣地區居留證</span><span class="sxs-lookup"><span data-stu-id="31aad-3304">台灣地區居留證</span></span> 

## <a name="thai-population-identification-code"></a><span data-ttu-id="31aad-3305">Код идентификации для тайского заполнения</span><span class="sxs-lookup"><span data-stu-id="31aad-3305">Thai Population Identification Code</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3306">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3306">Format</span></span>

<span data-ttu-id="31aad-3307">13 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3307">13 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3308">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3308">Pattern</span></span>

<span data-ttu-id="31aad-3309">13 цифр:</span><span class="sxs-lookup"><span data-stu-id="31aad-3309">13 digits:</span></span>
- <span data-ttu-id="31aad-3310">Первая цифра не равна 0 или 9</span><span class="sxs-lookup"><span data-stu-id="31aad-3310">First digit is not 0 or 9</span></span> 
- <span data-ttu-id="31aad-3311">12 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3311">12 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3312">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3312">Checksum</span></span>

<span data-ttu-id="31aad-3313">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3313">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3314">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3314">Definition</span></span>

<span data-ttu-id="31aad-3315">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3315">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3316">Функция Func_Thai_Citizen_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3316">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3317">Найдено ключевое слово из Keyword_Thai_Citizen_Id.</span><span class="sxs-lookup"><span data-stu-id="31aad-3317">A keyword from Keyword_Thai_Citizen_Id is found.</span></span>

<span data-ttu-id="31aad-3318">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3319">Функция Func_Thai_Citizen_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3319">The function Func_Thai_Citizen_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3320">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3320">Keywords</span></span>

#### <a name="keyword_thai_citizen_id"></a><span data-ttu-id="31aad-3321">Keyword_Thai_Citizen_Id</span><span class="sxs-lookup"><span data-stu-id="31aad-3321">Keyword_Thai_Citizen_Id</span></span>

- <span data-ttu-id="31aad-3322">ID Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3322">ID Number</span></span>
- <span data-ttu-id="31aad-3323">Идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="31aad-3323">Identification Number</span></span>
- <span data-ttu-id="31aad-3324">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="31aad-3324">บัตรประชาชน</span></span>
- <span data-ttu-id="31aad-3325">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="31aad-3325">รหัสบัตรประชาชน</span></span>
- <span data-ttu-id="31aad-3326">บัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="31aad-3326">บัตรประชาชน</span></span>
- <span data-ttu-id="31aad-3327">รหัสบัตรประชาชน</span><span class="sxs-lookup"><span data-stu-id="31aad-3327">รหัสบัตรประชาชน</span></span>
  
## <a name="turkish-national-identification-number"></a><span data-ttu-id="31aad-3328">Турецкий национальный идентификационный номер</span><span class="sxs-lookup"><span data-stu-id="31aad-3328">Turkish National Identification Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3329">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3329">Format</span></span>

<span data-ttu-id="31aad-3330">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3330">11 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3331">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3331">Pattern</span></span>

<span data-ttu-id="31aad-3332">11 цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3332">11 digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3333">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3333">Checksum</span></span>

<span data-ttu-id="31aad-3334">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3334">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3335">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3335">Definition</span></span>

<span data-ttu-id="31aad-3336">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3336">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3337">Функция Func_Turkish_National_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3337">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3338">Найдено ключевое слово из Keyword_Turkish_National_Id.</span><span class="sxs-lookup"><span data-stu-id="31aad-3338">A keyword from Keyword_Turkish_National_Id is found.</span></span>

<span data-ttu-id="31aad-3339">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3339">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3340">Функция Func_Turkish_National_Id обнаружила содержимое, соответствующее шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3340">The function Func_Turkish_National_Id finds content that matches the pattern.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3341">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3341">Keywords</span></span>

#### <a name="keyword_turkish_national_id"></a><span data-ttu-id="31aad-3342">Keyword_Turkish_National_Id</span><span class="sxs-lookup"><span data-stu-id="31aad-3342">Keyword_Turkish_National_Id</span></span>

- <span data-ttu-id="31aad-3343">TC Кимлик No</span><span class="sxs-lookup"><span data-stu-id="31aad-3343">TC Kimlik No</span></span>
- <span data-ttu-id="31aad-3344">TC Кимлик нумарасı</span><span class="sxs-lookup"><span data-stu-id="31aad-3344">TC Kimlik numarası</span></span>
- <span data-ttu-id="31aad-3345">Ватандаşлıк нумарасı</span><span class="sxs-lookup"><span data-stu-id="31aad-3345">Vatandaşlık numarası</span></span>
- <span data-ttu-id="31aad-3346">Ватандаşлıк нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3346">Vatandaşlık no</span></span>

## <a name="uk-drivers-license-number"></a><span data-ttu-id="31aad-p141">Номер водительского удостоверения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="31aad-p141">U.K. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3349">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3349">Format</span></span>

<span data-ttu-id="31aad-3350">Сочетание 18 букв и цифр в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3350">Combination of 18 letters and digits in the specified format</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3351">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3351">Pattern</span></span>

<span data-ttu-id="31aad-3352">18 букв и цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3352">18 letters and digits:</span></span>
- <span data-ttu-id="31aad-3353">Пять букв (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="31aad-3353">Five letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="31aad-3354">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="31aad-3354">One digit</span></span> 
- <span data-ttu-id="31aad-3355">Пять цифр в формате даты ДДММГ, представляющие собой дату рождения</span><span class="sxs-lookup"><span data-stu-id="31aad-3355">Five digits in the date format DDMMY for date of birth</span></span> 
- <span data-ttu-id="31aad-3356">Две буквы (без учета регистра) или цифра 9 вместо буквы</span><span class="sxs-lookup"><span data-stu-id="31aad-3356">Two letters (not case sensitive) or the digit "9" in place of a letter</span></span> 
- <span data-ttu-id="31aad-3357">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3357">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3358">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3358">Checksum</span></span>

<span data-ttu-id="31aad-3359">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3359">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3360">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3360">Definition</span></span>

<span data-ttu-id="31aad-3361">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3361">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3362">функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3362">The function Func_uk_drivers_license finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3363">находится ключевое слово из Keyword_uk_drivers_license;</span><span class="sxs-lookup"><span data-stu-id="31aad-3363">A keyword from Keyword_uk_drivers_license is found.</span></span>
- <span data-ttu-id="31aad-3364">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3364">The checksum passes.</span></span>

```xml
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3365">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3365">Keywords</span></span>

#### <a name="keyword_uk_drivers_license"></a><span data-ttu-id="31aad-3366">Keyword_uk_drivers_license</span><span class="sxs-lookup"><span data-stu-id="31aad-3366">Keyword_uk_drivers_license</span></span>

- <span data-ttu-id="31aad-3367">двла</span><span class="sxs-lookup"><span data-stu-id="31aad-3367">DVLA</span></span> 
- <span data-ttu-id="31aad-3368">light vans</span><span class="sxs-lookup"><span data-stu-id="31aad-3368">light vans</span></span> 
- <span data-ttu-id="31aad-3369">куадбикес</span><span class="sxs-lookup"><span data-stu-id="31aad-3369">quadbikes</span></span> 
- <span data-ttu-id="31aad-3370">motor cars</span><span class="sxs-lookup"><span data-stu-id="31aad-3370">motor cars</span></span> 
- <span data-ttu-id="31aad-3371">125cc</span><span class="sxs-lookup"><span data-stu-id="31aad-3371">125cc</span></span> 
- <span data-ttu-id="31aad-3372">сидекар</span><span class="sxs-lookup"><span data-stu-id="31aad-3372">sidecar</span></span> 
- <span data-ttu-id="31aad-3373">трициклес</span><span class="sxs-lookup"><span data-stu-id="31aad-3373">tricycles</span></span> 
- <span data-ttu-id="31aad-3374">моторциклес</span><span class="sxs-lookup"><span data-stu-id="31aad-3374">motorcycles</span></span> 
- <span data-ttu-id="31aad-3375">photocard licence</span><span class="sxs-lookup"><span data-stu-id="31aad-3375">photocard licence</span></span> 
- <span data-ttu-id="31aad-3376">learner drivers</span><span class="sxs-lookup"><span data-stu-id="31aad-3376">learner drivers</span></span> 
- <span data-ttu-id="31aad-3377">licence holder</span><span class="sxs-lookup"><span data-stu-id="31aad-3377">licence holder</span></span> 
- <span data-ttu-id="31aad-3378">licence holders</span><span class="sxs-lookup"><span data-stu-id="31aad-3378">licence holders</span></span> 
- <span data-ttu-id="31aad-3379">driving licences</span><span class="sxs-lookup"><span data-stu-id="31aad-3379">driving licences</span></span> 
- <span data-ttu-id="31aad-3380">driving licence</span><span class="sxs-lookup"><span data-stu-id="31aad-3380">driving licence</span></span> 
- <span data-ttu-id="31aad-3381">dual control car</span><span class="sxs-lookup"><span data-stu-id="31aad-3381">dual control car</span></span> 
   
## <a name="uk-electoral-roll-number"></a><span data-ttu-id="31aad-p142">Регистрационный номер избирателя для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="31aad-p142">U.K. Electoral Roll Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3384">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3384">Format</span></span>

<span data-ttu-id="31aad-3385">Две буквы, за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-3385">Two letters followed by 1-4 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3386">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3386">Pattern</span></span>

<span data-ttu-id="31aad-3387">Две буквы (без учета регистра), за которыми следуют 1–4 цифры.</span><span class="sxs-lookup"><span data-stu-id="31aad-3387">Two letters (not case sensitive) followed by 1-4 numbers</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3388">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3388">Checksum</span></span>

<span data-ttu-id="31aad-3389">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3389">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3390">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3390">Definition</span></span>

<span data-ttu-id="31aad-3391">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3391">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3392">регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3392">The regular expression Regex_uk_electoral finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3393">находится ключевое слово из Keyword_uk_electoral.</span><span class="sxs-lookup"><span data-stu-id="31aad-3393">A keyword from Keyword_uk_electoral is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3394">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3394">Keywords</span></span>

#### <a name="keyword_uk_electoral"></a><span data-ttu-id="31aad-3395">Keyword_uk_electoral</span><span class="sxs-lookup"><span data-stu-id="31aad-3395">Keyword_uk_electoral</span></span>

- <span data-ttu-id="31aad-3396">council nomination</span><span class="sxs-lookup"><span data-stu-id="31aad-3396">council nomination</span></span> 
- <span data-ttu-id="31aad-3397">nomination form</span><span class="sxs-lookup"><span data-stu-id="31aad-3397">nomination form</span></span> 
- <span data-ttu-id="31aad-3398">electoral register</span><span class="sxs-lookup"><span data-stu-id="31aad-3398">electoral register</span></span> 
- <span data-ttu-id="31aad-3399">electoral roll</span><span class="sxs-lookup"><span data-stu-id="31aad-3399">electoral roll</span></span>

   
## <a name="uk-national-health-service-number"></a><span data-ttu-id="31aad-p143">Номер национальной службы здравоохранения для Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="31aad-p143">U.K. National Health Service Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3402">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3402">Format</span></span>

<span data-ttu-id="31aad-3403">10–17 цифр, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="31aad-3403">10-17 digits separated by spaces</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3404">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3404">Pattern</span></span>

<span data-ttu-id="31aad-3405">10-17 цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3405">10-17 digits:</span></span>
- <span data-ttu-id="31aad-3406">3 или 10 цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3406">Either 3 or 10 digits</span></span> 
- <span data-ttu-id="31aad-3407">Пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-3407">A space</span></span> 
- <span data-ttu-id="31aad-3408">Три цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3408">Three digits</span></span> 
- <span data-ttu-id="31aad-3409">Пробел</span><span class="sxs-lookup"><span data-stu-id="31aad-3409">A space</span></span> 
- <span data-ttu-id="31aad-3410">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3410">Four digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3411">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3411">Checksum</span></span>

<span data-ttu-id="31aad-3412">Да</span><span class="sxs-lookup"><span data-stu-id="31aad-3412">Yes</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3413">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3413">Definition</span></span>

<span data-ttu-id="31aad-3414">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3414">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3415">Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3415">The function Func_uk_nhs_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3416">Верно одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-3416">One of the following is true:</span></span>
    - <span data-ttu-id="31aad-3417">найдено ключевое слово из Keyword_uk_nhs_number;</span><span class="sxs-lookup"><span data-stu-id="31aad-3417">A keyword from Keyword_uk_nhs_number is found.</span></span>
    - <span data-ttu-id="31aad-3418">найдено ключевое слово из Keyword_uk_nhs_number1;</span><span class="sxs-lookup"><span data-stu-id="31aad-3418">A keyword from Keyword_uk_nhs_number1 is found.</span></span>
    - <span data-ttu-id="31aad-3419">найдено ключевое слово из Keyword_uk_nhs_number_dob.</span><span class="sxs-lookup"><span data-stu-id="31aad-3419">A keyword from Keyword_uk_nhs_number_dob is found.</span></span>
- <span data-ttu-id="31aad-3420">Контрольная сумма проходит проверку.</span><span class="sxs-lookup"><span data-stu-id="31aad-3420">The checksum passes.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3421">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3421">Keywords</span></span>
   
#### <a name="keyword_uk_nhs_number"></a><span data-ttu-id="31aad-3422">Keyword_uk_nhs_number</span><span class="sxs-lookup"><span data-stu-id="31aad-3422">Keyword_uk_nhs_number</span></span>

- <span data-ttu-id="31aad-3423">national health service</span><span class="sxs-lookup"><span data-stu-id="31aad-3423">national health service</span></span> 
- <span data-ttu-id="31aad-3424">NHS</span><span class="sxs-lookup"><span data-stu-id="31aad-3424">nhs</span></span> 
- <span data-ttu-id="31aad-3425">health services authority</span><span class="sxs-lookup"><span data-stu-id="31aad-3425">health services authority</span></span> 
- <span data-ttu-id="31aad-3426">health authority</span><span class="sxs-lookup"><span data-stu-id="31aad-3426">health authority</span></span>

#### <a name="keyword_uk_nhs_number1"></a><span data-ttu-id="31aad-3427">Keyword_uk_nhs_number1</span><span class="sxs-lookup"><span data-stu-id="31aad-3427">Keyword_uk_nhs_number1</span></span>

- <span data-ttu-id="31aad-3428">patient id</span><span class="sxs-lookup"><span data-stu-id="31aad-3428">patient id</span></span> 
- <span data-ttu-id="31aad-3429">patient identification</span><span class="sxs-lookup"><span data-stu-id="31aad-3429">patient identification</span></span> 
- <span data-ttu-id="31aad-3430">patient no</span><span class="sxs-lookup"><span data-stu-id="31aad-3430">patient no</span></span> 
- <span data-ttu-id="31aad-3431">patient number</span><span class="sxs-lookup"><span data-stu-id="31aad-3431">patient number</span></span>

#### <a name="keyword_uk_nhs_number_dob"></a><span data-ttu-id="31aad-3432">Keyword_uk_nhs_number_dob</span><span class="sxs-lookup"><span data-stu-id="31aad-3432">Keyword_uk_nhs_number_dob</span></span>

- <span data-ttu-id="31aad-3433">ГРУПП</span><span class="sxs-lookup"><span data-stu-id="31aad-3433">GP</span></span> 
- <span data-ttu-id="31aad-3434">доб</span><span class="sxs-lookup"><span data-stu-id="31aad-3434">DOB</span></span> 
- <span data-ttu-id="31aad-3435">D. O. B</span><span class="sxs-lookup"><span data-stu-id="31aad-3435">D.O.B</span></span> 
- <span data-ttu-id="31aad-3436">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="31aad-3436">Date of Birth</span></span> 
- <span data-ttu-id="31aad-3437">Birth Date</span><span class="sxs-lookup"><span data-stu-id="31aad-3437">Birth Date</span></span> 
   
## <a name="uk-national-insurance-number-nino"></a><span data-ttu-id="31aad-p144">Номер карты национального страхования для Соединенного Королевства (NINO)</span><span class="sxs-lookup"><span data-stu-id="31aad-p144">U.K. National Insurance Number (NINO)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3440">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3440">Format</span></span>

<span data-ttu-id="31aad-3441">7 символов или 9 символов, разделенных пробелами или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3441">7 characters or 9 characters separated by spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3442">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3442">Pattern</span></span>

<span data-ttu-id="31aad-3443">Два возможных шаблона:</span><span class="sxs-lookup"><span data-stu-id="31aad-3443">Two possible patterns:</span></span>

- <span data-ttu-id="31aad-3444">Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-3444">Two letters (valid NINOs use only certain characters in this prefix, which this pattern validates; not case sensitive)</span></span>
- <span data-ttu-id="31aad-3445">Шесть цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3445">Six digits</span></span>
- <span data-ttu-id="31aad-3446">"A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)</span><span class="sxs-lookup"><span data-stu-id="31aad-3446">Either 'A', 'B', 'C', or 'D' (like the prefix, only certain characters are allowed in the suffix; not case sensitive)</span></span>

<span data-ttu-id="31aad-3447">OR</span><span class="sxs-lookup"><span data-stu-id="31aad-3447">OR</span></span>

- <span data-ttu-id="31aad-3448">Две буквы</span><span class="sxs-lookup"><span data-stu-id="31aad-3448">Two letters</span></span>
- <span data-ttu-id="31aad-3449">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3449">A space or dash</span></span>
- <span data-ttu-id="31aad-3450">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3450">Two digits</span></span>
- <span data-ttu-id="31aad-3451">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3451">A space or dash</span></span>
- <span data-ttu-id="31aad-3452">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3452">Two digits</span></span>
- <span data-ttu-id="31aad-3453">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3453">A space or dash</span></span>
- <span data-ttu-id="31aad-3454">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3454">Two digits</span></span>
- <span data-ttu-id="31aad-3455">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3455">A space or dash</span></span>
- <span data-ttu-id="31aad-3456">Значение "A", "B", "C" или "'D"</span><span class="sxs-lookup"><span data-stu-id="31aad-3456">Either 'A', 'B', 'C', or 'D'</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3457">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3457">Checksum</span></span>

<span data-ttu-id="31aad-3458">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3458">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3459">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3459">Definition</span></span>

<span data-ttu-id="31aad-3460">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3460">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3461">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3461">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3462">находится ключевое слово из Keyword_uk_nino.</span><span class="sxs-lookup"><span data-stu-id="31aad-3462">A keyword from Keyword_uk_nino is found.</span></span>

<span data-ttu-id="31aad-3463">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3463">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3464">функция Func_uk_nino находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3464">The function Func_uk_nino finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3465">ни одно ключевое слово из Keyword_uk_nino не находится.</span><span class="sxs-lookup"><span data-stu-id="31aad-3465">No keyword from Keyword_uk_nino is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3466">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3466">Keywords</span></span>

#### <a name="keyword_uk_nino"></a><span data-ttu-id="31aad-3467">Keyword_uk_nino</span><span class="sxs-lookup"><span data-stu-id="31aad-3467">Keyword_uk_nino</span></span>

- <span data-ttu-id="31aad-3468">national insurance number</span><span class="sxs-lookup"><span data-stu-id="31aad-3468">national insurance number</span></span> 
- <span data-ttu-id="31aad-3469">national insurance contributions</span><span class="sxs-lookup"><span data-stu-id="31aad-3469">national insurance contributions</span></span> 
- <span data-ttu-id="31aad-3470">protection act</span><span class="sxs-lookup"><span data-stu-id="31aad-3470">protection act</span></span> 
- <span data-ttu-id="31aad-3471">страхования</span><span class="sxs-lookup"><span data-stu-id="31aad-3471">insurance</span></span> 
- <span data-ttu-id="31aad-3472">social security number</span><span class="sxs-lookup"><span data-stu-id="31aad-3472">social security number</span></span> 
- <span data-ttu-id="31aad-3473">insurance application</span><span class="sxs-lookup"><span data-stu-id="31aad-3473">insurance application</span></span> 
- <span data-ttu-id="31aad-3474">medical application</span><span class="sxs-lookup"><span data-stu-id="31aad-3474">medical application</span></span> 
- <span data-ttu-id="31aad-3475">social insurance</span><span class="sxs-lookup"><span data-stu-id="31aad-3475">social insurance</span></span> 
- <span data-ttu-id="31aad-3476">medical attention</span><span class="sxs-lookup"><span data-stu-id="31aad-3476">medical attention</span></span> 
- <span data-ttu-id="31aad-3477">social security</span><span class="sxs-lookup"><span data-stu-id="31aad-3477">social security</span></span> 
- <span data-ttu-id="31aad-3478">great britain</span><span class="sxs-lookup"><span data-stu-id="31aad-3478">great britain</span></span> 
- <span data-ttu-id="31aad-3479">страхования</span><span class="sxs-lookup"><span data-stu-id="31aad-3479">insurance</span></span>    
   
## <a name="us--uk-passport-number"></a><span data-ttu-id="31aad-p145">Номер паспорта гражданина США и/или Соединенного Королевства</span><span class="sxs-lookup"><span data-stu-id="31aad-p145">U.S. / U.K. Passport Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3482">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3482">Format</span></span>

<span data-ttu-id="31aad-3483">Девять цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3483">Nine digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3484">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3484">Pattern</span></span>

<span data-ttu-id="31aad-3485">Девять последовательных цифр.</span><span class="sxs-lookup"><span data-stu-id="31aad-3485">Nine consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3486">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3486">Checksum</span></span>

<span data-ttu-id="31aad-3487">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3487">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3488">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3488">Definition</span></span>

<span data-ttu-id="31aad-3489">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3489">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3490">функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3490">The function Func_usa_uk_passport finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3491">находится ключевое слово из Keyword_passport.</span><span class="sxs-lookup"><span data-stu-id="31aad-3491">A keyword from Keyword_passport is found.</span></span>

```xml
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3492">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3492">Keywords</span></span>

#### <a name="keyword_passport"></a><span data-ttu-id="31aad-3493">Keyword_passport</span><span class="sxs-lookup"><span data-stu-id="31aad-3493">Keyword_passport</span></span>

- <span data-ttu-id="31aad-3494">Passport Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3494">Passport Number</span></span> 
- <span data-ttu-id="31aad-3495">Passport No</span><span class="sxs-lookup"><span data-stu-id="31aad-3495">Passport No</span></span> 
- <span data-ttu-id="31aad-3496">Passport#</span><span class="sxs-lookup"><span data-stu-id="31aad-3496">Passport #</span></span> 
- <span data-ttu-id="31aad-3497">Службу #</span><span class="sxs-lookup"><span data-stu-id="31aad-3497">Passport#</span></span> 
- <span data-ttu-id="31aad-3498">пасспортид</span><span class="sxs-lookup"><span data-stu-id="31aad-3498">PassportID</span></span> 
- <span data-ttu-id="31aad-3499">пасспортно</span><span class="sxs-lookup"><span data-stu-id="31aad-3499">Passportno</span></span> 
- <span data-ttu-id="31aad-3500">пасспортнумбер</span><span class="sxs-lookup"><span data-stu-id="31aad-3500">passportnumber</span></span> 
- <span data-ttu-id="31aad-3501">パスポート</span><span class="sxs-lookup"><span data-stu-id="31aad-3501">パスポート</span></span> 
- <span data-ttu-id="31aad-3502">パスポート番号</span><span class="sxs-lookup"><span data-stu-id="31aad-3502">パスポート番号</span></span> 
- <span data-ttu-id="31aad-3503">パスポートのнум</span><span class="sxs-lookup"><span data-stu-id="31aad-3503">パスポートのNum</span></span> 
- <span data-ttu-id="31aad-3504">パスポート #</span><span class="sxs-lookup"><span data-stu-id="31aad-3504">パスポート＃</span></span> 
- <span data-ttu-id="31aad-3505">Numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="31aad-3505">Numéro de passeport</span></span> 
- <span data-ttu-id="31aad-3506">Passeport n °</span><span class="sxs-lookup"><span data-stu-id="31aad-3506">Passeport n °</span></span> 
- <span data-ttu-id="31aad-3507">Passeport Non</span><span class="sxs-lookup"><span data-stu-id="31aad-3507">Passeport Non</span></span> 
- <span data-ttu-id="31aad-3508">Passeport#</span><span class="sxs-lookup"><span data-stu-id="31aad-3508">Passeport #</span></span> 
- <span data-ttu-id="31aad-3509">пассепорт #</span><span class="sxs-lookup"><span data-stu-id="31aad-3509">Passeport#</span></span> 
- <span data-ttu-id="31aad-3510">пассепортнон</span><span class="sxs-lookup"><span data-stu-id="31aad-3510">PasseportNon</span></span> 
- <span data-ttu-id="31aad-3511">Passeportn °</span><span class="sxs-lookup"><span data-stu-id="31aad-3511">Passeportn °</span></span> 
   
## <a name="us-bank-account-number"></a><span data-ttu-id="31aad-3512">Номер банковского счета для США</span><span class="sxs-lookup"><span data-stu-id="31aad-3512">U.S. Bank Account Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3513">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3513">Format</span></span>

<span data-ttu-id="31aad-3514">8-17 цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3514">8-17 digits</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3515">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3515">Pattern</span></span>

<span data-ttu-id="31aad-3516">8–17 последовательных цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3516">8-17 consecutive digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3517">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3517">Checksum</span></span>

<span data-ttu-id="31aad-3518">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3518">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3519">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3519">Definition</span></span>

<span data-ttu-id="31aad-3520">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3520">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3521">регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3521">The regular expression Regex_usa_bank_account_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3522">находится ключевое слово из Keyword_usa_Bank_Account.</span><span class="sxs-lookup"><span data-stu-id="31aad-3522">A keyword from Keyword_usa_Bank_Account is found.</span></span>

```xml
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3523">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3523">Keywords</span></span>

#### <a name="keyword_usa_bank_account"></a><span data-ttu-id="31aad-3524">Keyword_usa_Bank_Account</span><span class="sxs-lookup"><span data-stu-id="31aad-3524">Keyword_usa_Bank_Account</span></span>

- <span data-ttu-id="31aad-3525">Checking Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3525">Checking Account Number</span></span> 
- <span data-ttu-id="31aad-3526">Checking Account</span><span class="sxs-lookup"><span data-stu-id="31aad-3526">Checking Account</span></span> 
- <span data-ttu-id="31aad-3527">Checking Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-3527">Checking Account #</span></span> 
- <span data-ttu-id="31aad-3528">Checking Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3528">Checking Acct Number</span></span> 
- <span data-ttu-id="31aad-3529">Checking Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-3529">Checking Acct #</span></span> 
- <span data-ttu-id="31aad-3530">Checking Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3530">Checking Acct No.</span></span> 
- <span data-ttu-id="31aad-3531">Checking Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3531">Checking Account No.</span></span> 
- <span data-ttu-id="31aad-3532">Bank Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3532">Bank Account Number</span></span> 
- <span data-ttu-id="31aad-3533">Bank Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-3533">Bank Account #</span></span> 
- <span data-ttu-id="31aad-3534">Bank Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3534">Bank Acct Number</span></span> 
- <span data-ttu-id="31aad-3535">Bank Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-3535">Bank Acct #</span></span> 
- <span data-ttu-id="31aad-3536">Bank Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3536">Bank Acct No.</span></span> 
- <span data-ttu-id="31aad-3537">Bank Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3537">Bank Account No.</span></span> 
- <span data-ttu-id="31aad-3538">Savings Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3538">Savings Account Number</span></span> 
- <span data-ttu-id="31aad-3539">Savings Account.</span><span class="sxs-lookup"><span data-stu-id="31aad-3539">Savings Account.</span></span> 
- <span data-ttu-id="31aad-3540">Savings Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-3540">Savings Account #</span></span> 
- <span data-ttu-id="31aad-3541">Savings Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3541">Savings Acct Number</span></span> 
- <span data-ttu-id="31aad-3542">Savings Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-3542">Savings Acct #</span></span> 
- <span data-ttu-id="31aad-3543">Savings Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3543">Savings Acct No.</span></span> 
- <span data-ttu-id="31aad-3544">Savings Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3544">Savings Account No.</span></span> 
- <span data-ttu-id="31aad-3545">Debit Account Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3545">Debit Account Number</span></span> 
- <span data-ttu-id="31aad-3546">Debit Account</span><span class="sxs-lookup"><span data-stu-id="31aad-3546">Debit Account</span></span> 
- <span data-ttu-id="31aad-3547">Debit Account #</span><span class="sxs-lookup"><span data-stu-id="31aad-3547">Debit Account #</span></span> 
- <span data-ttu-id="31aad-3548">Debit Acct Number</span><span class="sxs-lookup"><span data-stu-id="31aad-3548">Debit Acct Number</span></span> 
- <span data-ttu-id="31aad-3549">Debit Acct #</span><span class="sxs-lookup"><span data-stu-id="31aad-3549">Debit Acct #</span></span> 
- <span data-ttu-id="31aad-3550">Debit Acct No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3550">Debit Acct No.</span></span> 
- <span data-ttu-id="31aad-3551">Debit Account No.</span><span class="sxs-lookup"><span data-stu-id="31aad-3551">Debit Account No.</span></span> 
   
## <a name="us-drivers-license-number"></a><span data-ttu-id="31aad-3552">Номер водительского удостоверения для США</span><span class="sxs-lookup"><span data-stu-id="31aad-3552">U.S. Driver's License Number</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3553">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3553">Format</span></span>

<span data-ttu-id="31aad-3554">Зависит от штата.</span><span class="sxs-lookup"><span data-stu-id="31aad-3554">Depends on the state</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3555">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3555">Pattern</span></span>

<span data-ttu-id="31aad-3556">В зависимости от штата. Например, для Нью-Йорка:</span><span class="sxs-lookup"><span data-stu-id="31aad-3556">Depends on the state -- for example, New York:</span></span>
- <span data-ttu-id="31aad-3557">Девять цифр, отформатированных как DDD DDD DDD, будут совпадают.</span><span class="sxs-lookup"><span data-stu-id="31aad-3557">Nine digits formatted like ddd ddd ddd will match.</span></span>
- <span data-ttu-id="31aad-3558">Не подойдут девять цифр в формате ццццццццц.</span><span class="sxs-lookup"><span data-stu-id="31aad-3558">Nine digits like ddddddddd will not match.</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3559">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3559">Checksum</span></span>

<span data-ttu-id="31aad-3560">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3560">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3561">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3561">Definition</span></span>

<span data-ttu-id="31aad-3562">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3562">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3563">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3563">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3564">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="31aad-3564">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="31aad-3565">обнаружено ключевое слово из списка Keyword_us_drivers_license.</span><span class="sxs-lookup"><span data-stu-id="31aad-3565">A keyword from Keyword_us_drivers_license is found.</span></span>

<span data-ttu-id="31aad-3566">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3566">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3567">функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;</span><span class="sxs-lookup"><span data-stu-id="31aad-3567">The function Func_new_york_drivers_license_number finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3568">находится ключевое слово из Keyword_[state_name]_drivers_license_name;</span><span class="sxs-lookup"><span data-stu-id="31aad-3568">A keyword from Keyword_[state_name]_drivers_license_name is found.</span></span>
- <span data-ttu-id="31aad-3569">находится ключевое слово из Keyword_us_drivers_license_abbreviations.</span><span class="sxs-lookup"><span data-stu-id="31aad-3569">A keyword from Keyword_us_drivers_license_abbreviations is found.</span></span>
- <span data-ttu-id="31aad-3570">ни одно ключевое слово из Keyword_us_drivers_license не находится.</span><span class="sxs-lookup"><span data-stu-id="31aad-3570">No keyword from Keyword_us_drivers_license is found.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3571">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3571">Keywords</span></span>

#### <a name="keyword_us_drivers_license_abbreviations"></a><span data-ttu-id="31aad-3572">Keyword_us_drivers_license_abbreviations</span><span class="sxs-lookup"><span data-stu-id="31aad-3572">Keyword_us_drivers_license_abbreviations</span></span>

- <span data-ttu-id="31aad-3573">DL</span><span class="sxs-lookup"><span data-stu-id="31aad-3573">DL</span></span> 
- <span data-ttu-id="31aad-3574">БИБЛИОТЕК</span><span class="sxs-lookup"><span data-stu-id="31aad-3574">DLS</span></span> 
- <span data-ttu-id="31aad-3575">кдл</span><span class="sxs-lookup"><span data-stu-id="31aad-3575">CDL</span></span> 
- <span data-ttu-id="31aad-3576">кдлс</span><span class="sxs-lookup"><span data-stu-id="31aad-3576">CDLS</span></span> 
- <span data-ttu-id="31aad-3577">ID</span><span class="sxs-lookup"><span data-stu-id="31aad-3577">ID</span></span> 
- <span data-ttu-id="31aad-3578">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="31aad-3578">IDs</span></span> 
- <span data-ttu-id="31aad-3579">DL #</span><span class="sxs-lookup"><span data-stu-id="31aad-3579">DL#</span></span> 
- <span data-ttu-id="31aad-3580">БИБЛИОТЕК #</span><span class="sxs-lookup"><span data-stu-id="31aad-3580">DLS#</span></span> 
- <span data-ttu-id="31aad-3581">кдл #</span><span class="sxs-lookup"><span data-stu-id="31aad-3581">CDL#</span></span> 
- <span data-ttu-id="31aad-3582">кдлс #</span><span class="sxs-lookup"><span data-stu-id="31aad-3582">CDLS#</span></span> 
- <span data-ttu-id="31aad-3583">КОДОВ #</span><span class="sxs-lookup"><span data-stu-id="31aad-3583">ID#</span></span>
- <span data-ttu-id="31aad-3584">Идентификаторы #</span><span class="sxs-lookup"><span data-stu-id="31aad-3584">IDs#</span></span> 
- <span data-ttu-id="31aad-3585">ID number</span><span class="sxs-lookup"><span data-stu-id="31aad-3585">ID number</span></span> 
- <span data-ttu-id="31aad-3586">ID numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-3586">ID numbers</span></span> 
- <span data-ttu-id="31aad-3587">лик</span><span class="sxs-lookup"><span data-stu-id="31aad-3587">LIC</span></span> 
- <span data-ttu-id="31aad-3588">лик #</span><span class="sxs-lookup"><span data-stu-id="31aad-3588">LIC#</span></span> 

#### <a name="keyword_us_drivers_license"></a><span data-ttu-id="31aad-3589">Keyword_us_drivers_license</span><span class="sxs-lookup"><span data-stu-id="31aad-3589">Keyword_us_drivers_license</span></span>

- <span data-ttu-id="31aad-3590">дриверлик</span><span class="sxs-lookup"><span data-stu-id="31aad-3590">DriverLic</span></span> 
- <span data-ttu-id="31aad-3591">дриверликс</span><span class="sxs-lookup"><span data-stu-id="31aad-3591">DriverLics</span></span> 
- <span data-ttu-id="31aad-3592">дриверлиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-3592">DriverLicense</span></span> 
- <span data-ttu-id="31aad-3593">дриверлиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-3593">DriverLicenses</span></span> 
- <span data-ttu-id="31aad-3594">Driver Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-3594">Driver Lic</span></span> 
- <span data-ttu-id="31aad-3595">Driver Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-3595">Driver Lics</span></span> 
- <span data-ttu-id="31aad-3596">Driver License</span><span class="sxs-lookup"><span data-stu-id="31aad-3596">Driver License</span></span> 
- <span data-ttu-id="31aad-3597">Driver Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-3597">Driver Licenses</span></span> 
- <span data-ttu-id="31aad-3598">дриверслик</span><span class="sxs-lookup"><span data-stu-id="31aad-3598">DriversLic</span></span> 
- <span data-ttu-id="31aad-3599">дриверсликс</span><span class="sxs-lookup"><span data-stu-id="31aad-3599">DriversLics</span></span> 
- <span data-ttu-id="31aad-3600">дриверслиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-3600">DriversLicense</span></span> 
- <span data-ttu-id="31aad-3601">дриверслиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-3601">DriversLicenses</span></span> 
- <span data-ttu-id="31aad-3602">Drivers Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-3602">Drivers Lic</span></span> 
- <span data-ttu-id="31aad-3603">Drivers Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-3603">Drivers Lics</span></span> 
- <span data-ttu-id="31aad-3604">Drivers License</span><span class="sxs-lookup"><span data-stu-id="31aad-3604">Drivers License</span></span> 
- <span data-ttu-id="31aad-3605">Drivers Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-3605">Drivers Licenses</span></span> 
- <span data-ttu-id="31aad-3606">Driver ' LIC</span><span class="sxs-lookup"><span data-stu-id="31aad-3606">Driver'Lic</span></span> 
- <span data-ttu-id="31aad-3607">Driver ' LICS</span><span class="sxs-lookup"><span data-stu-id="31aad-3607">Driver'Lics</span></span> 
- <span data-ttu-id="31aad-3608">Driver ' License</span><span class="sxs-lookup"><span data-stu-id="31aad-3608">Driver'License</span></span> 
- <span data-ttu-id="31aad-3609">Driver ' Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-3609">Driver'Licenses</span></span> 
- <span data-ttu-id="31aad-3610">Driver' Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-3610">Driver' Lic</span></span> 
- <span data-ttu-id="31aad-3611">Driver' Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-3611">Driver' Lics</span></span> 
- <span data-ttu-id="31aad-3612">Driver' License</span><span class="sxs-lookup"><span data-stu-id="31aad-3612">Driver' License</span></span> 
- <span data-ttu-id="31aad-3613">Driver' Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-3613">Driver' Licenses</span></span>
- <span data-ttu-id="31aad-3614">дривер'слик</span><span class="sxs-lookup"><span data-stu-id="31aad-3614">Driver'sLic</span></span> 
- <span data-ttu-id="31aad-3615">дривер'сликс</span><span class="sxs-lookup"><span data-stu-id="31aad-3615">Driver'sLics</span></span> 
- <span data-ttu-id="31aad-3616">дривер'слиценсе</span><span class="sxs-lookup"><span data-stu-id="31aad-3616">Driver'sLicense</span></span> 
- <span data-ttu-id="31aad-3617">дривер'слиценсес</span><span class="sxs-lookup"><span data-stu-id="31aad-3617">Driver'sLicenses</span></span> 
- <span data-ttu-id="31aad-3618">Driver's Lic</span><span class="sxs-lookup"><span data-stu-id="31aad-3618">Driver's Lic</span></span> 
- <span data-ttu-id="31aad-3619">Driver's Lics</span><span class="sxs-lookup"><span data-stu-id="31aad-3619">Driver's Lics</span></span> 
- <span data-ttu-id="31aad-3620">Driver's License</span><span class="sxs-lookup"><span data-stu-id="31aad-3620">Driver's License</span></span> 
- <span data-ttu-id="31aad-3621">Driver's Licenses</span><span class="sxs-lookup"><span data-stu-id="31aad-3621">Driver's Licenses</span></span> 
- <span data-ttu-id="31aad-3622">identification number</span><span class="sxs-lookup"><span data-stu-id="31aad-3622">identification number</span></span> 
- <span data-ttu-id="31aad-3623">identification numbers</span><span class="sxs-lookup"><span data-stu-id="31aad-3623">identification numbers</span></span> 
- <span data-ttu-id="31aad-3624">identification #</span><span class="sxs-lookup"><span data-stu-id="31aad-3624">identification #</span></span> 
- <span data-ttu-id="31aad-3625">id card</span><span class="sxs-lookup"><span data-stu-id="31aad-3625">id card</span></span> 
- <span data-ttu-id="31aad-3626">id cards</span><span class="sxs-lookup"><span data-stu-id="31aad-3626">id cards</span></span> 
- <span data-ttu-id="31aad-3627">identification card</span><span class="sxs-lookup"><span data-stu-id="31aad-3627">identification card</span></span> 
- <span data-ttu-id="31aad-3628">identification cards</span><span class="sxs-lookup"><span data-stu-id="31aad-3628">identification cards</span></span> 
- <span data-ttu-id="31aad-3629">дриверлик #</span><span class="sxs-lookup"><span data-stu-id="31aad-3629">DriverLic#</span></span> 
- <span data-ttu-id="31aad-3630">дриверликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-3630">DriverLics#</span></span> 
- <span data-ttu-id="31aad-3631">дриверлиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-3631">DriverLicense#</span></span> 
- <span data-ttu-id="31aad-3632">дриверлиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-3632">DriverLicenses#</span></span> 
- <span data-ttu-id="31aad-3633">Driver Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-3633">Driver Lic#</span></span> 
- <span data-ttu-id="31aad-3634">Driver Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-3634">Driver Lics#</span></span> 
- <span data-ttu-id="31aad-3635">Driver License#</span><span class="sxs-lookup"><span data-stu-id="31aad-3635">Driver License#</span></span> 
- <span data-ttu-id="31aad-3636">Driver Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-3636">Driver Licenses#</span></span> 
- <span data-ttu-id="31aad-3637">дриверслик #</span><span class="sxs-lookup"><span data-stu-id="31aad-3637">DriversLic#</span></span> 
- <span data-ttu-id="31aad-3638">дриверсликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-3638">DriversLics#</span></span> 
- <span data-ttu-id="31aad-3639">дриверслиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-3639">DriversLicense#</span></span> 
- <span data-ttu-id="31aad-3640">дриверслиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-3640">DriversLicenses#</span></span> 
- <span data-ttu-id="31aad-3641">Drivers Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-3641">Drivers Lic#</span></span> 
- <span data-ttu-id="31aad-3642">Drivers Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-3642">Drivers Lics#</span></span> 
- <span data-ttu-id="31aad-3643">Drivers License#</span><span class="sxs-lookup"><span data-stu-id="31aad-3643">Drivers License#</span></span> 
- <span data-ttu-id="31aad-3644">Drivers Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-3644">Drivers Licenses#</span></span> 
- <span data-ttu-id="31aad-3645">Driver ' LIC #</span><span class="sxs-lookup"><span data-stu-id="31aad-3645">Driver'Lic#</span></span> 
- <span data-ttu-id="31aad-3646">Driver ' LICS #</span><span class="sxs-lookup"><span data-stu-id="31aad-3646">Driver'Lics#</span></span> 
- <span data-ttu-id="31aad-3647">Driver ' License #</span><span class="sxs-lookup"><span data-stu-id="31aad-3647">Driver'License#</span></span> 
- <span data-ttu-id="31aad-3648">Driver ' Licenses #</span><span class="sxs-lookup"><span data-stu-id="31aad-3648">Driver'Licenses#</span></span> 
- <span data-ttu-id="31aad-3649">Driver' Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-3649">Driver' Lic#</span></span> 
- <span data-ttu-id="31aad-3650">Driver' Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-3650">Driver' Lics#</span></span> 
- <span data-ttu-id="31aad-3651">Driver' License#</span><span class="sxs-lookup"><span data-stu-id="31aad-3651">Driver' License#</span></span> 
- <span data-ttu-id="31aad-3652">Driver' Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-3652">Driver' Licenses#</span></span> 
- <span data-ttu-id="31aad-3653">дривер'слик #</span><span class="sxs-lookup"><span data-stu-id="31aad-3653">Driver'sLic#</span></span> 
- <span data-ttu-id="31aad-3654">дривер'сликс #</span><span class="sxs-lookup"><span data-stu-id="31aad-3654">Driver'sLics#</span></span> 
- <span data-ttu-id="31aad-3655">дривер'слиценсе #</span><span class="sxs-lookup"><span data-stu-id="31aad-3655">Driver'sLicense#</span></span> 
- <span data-ttu-id="31aad-3656">дривер'слиценсес #</span><span class="sxs-lookup"><span data-stu-id="31aad-3656">Driver'sLicenses#</span></span> 
- <span data-ttu-id="31aad-3657">Driver's Lic#</span><span class="sxs-lookup"><span data-stu-id="31aad-3657">Driver's Lic#</span></span> 
- <span data-ttu-id="31aad-3658">Driver's Lics#</span><span class="sxs-lookup"><span data-stu-id="31aad-3658">Driver's Lics#</span></span> 
- <span data-ttu-id="31aad-3659">Driver's License#</span><span class="sxs-lookup"><span data-stu-id="31aad-3659">Driver's License#</span></span> 
- <span data-ttu-id="31aad-3660">Driver's Licenses#</span><span class="sxs-lookup"><span data-stu-id="31aad-3660">Driver's Licenses#</span></span> 
- <span data-ttu-id="31aad-3661">id card#</span><span class="sxs-lookup"><span data-stu-id="31aad-3661">id card#</span></span> 
- <span data-ttu-id="31aad-3662">id cards#</span><span class="sxs-lookup"><span data-stu-id="31aad-3662">id cards#</span></span> 
- <span data-ttu-id="31aad-3663">identification card#</span><span class="sxs-lookup"><span data-stu-id="31aad-3663">identification card#</span></span> 
- <span data-ttu-id="31aad-3664">identification cards#</span><span class="sxs-lookup"><span data-stu-id="31aad-3664">identification cards#</span></span> 


#### <a name="keyword_state_name_drivers_license_name"></a><span data-ttu-id="31aad-3665">Keyword_[state_name]_drivers_license_name</span><span class="sxs-lookup"><span data-stu-id="31aad-3665">Keyword_[state_name]_drivers_license_name</span></span>

- <span data-ttu-id="31aad-3666">Аббревиатура штата (например, NY)</span><span class="sxs-lookup"><span data-stu-id="31aad-3666">State abbreviation (for example, "NY")</span></span> 
- <span data-ttu-id="31aad-3667">Название штата (например, New York)</span><span class="sxs-lookup"><span data-stu-id="31aad-3667">State name (for example, "New York")</span></span>    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a><span data-ttu-id="31aad-3668">Идентификационный номер налогоплательщика для США (ITIN)</span><span class="sxs-lookup"><span data-stu-id="31aad-3668">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3669">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3669">Format</span></span>

<span data-ttu-id="31aad-3670">Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).</span><span class="sxs-lookup"><span data-stu-id="31aad-3670">Nine digits that start with a "9" and contain a "7" or "8" as the fourth digit, optionally formatted with spaces or dashes</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3671">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3671">Pattern</span></span>

<span data-ttu-id="31aad-3672">Форматируемые</span><span class="sxs-lookup"><span data-stu-id="31aad-3672">Formatted:</span></span>
- <span data-ttu-id="31aad-3673">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="31aad-3673">The digit "9"</span></span> 
- <span data-ttu-id="31aad-3674">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3674">Two digits</span></span> 
- <span data-ttu-id="31aad-3675">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3675">A space or dash</span></span> 
- <span data-ttu-id="31aad-3676">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="31aad-3676">A "7" or "8"</span></span> 
- <span data-ttu-id="31aad-3677">Одна цифра</span><span class="sxs-lookup"><span data-stu-id="31aad-3677">A digit</span></span> 
- <span data-ttu-id="31aad-3678">Пробел или тире</span><span class="sxs-lookup"><span data-stu-id="31aad-3678">A space, or dash</span></span> 
- <span data-ttu-id="31aad-3679">Четыре цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3679">Four digits</span></span>

<span data-ttu-id="31aad-3680">Неформатированные</span><span class="sxs-lookup"><span data-stu-id="31aad-3680">Unformatted:</span></span>
- <span data-ttu-id="31aad-3681">Цифра 9</span><span class="sxs-lookup"><span data-stu-id="31aad-3681">The digit "9"</span></span> 
- <span data-ttu-id="31aad-3682">Две цифры</span><span class="sxs-lookup"><span data-stu-id="31aad-3682">Two digits</span></span> 
- <span data-ttu-id="31aad-3683">Цифра 7 или 8</span><span class="sxs-lookup"><span data-stu-id="31aad-3683">A "7" or "8"</span></span> 
- <span data-ttu-id="31aad-3684">Пять цифр</span><span class="sxs-lookup"><span data-stu-id="31aad-3684">Five digits</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3685">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3685">Checksum</span></span>

<span data-ttu-id="31aad-3686">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3686">No</span></span>

### <a name="definition"></a><span data-ttu-id="31aad-3687">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3687">Definition</span></span>

<span data-ttu-id="31aad-3688">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3689">Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3689">The function Func_formatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3690">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-3690">At least one of the following is true:</span></span>
    - <span data-ttu-id="31aad-3691">найдено ключевое слово из Keyword_itin;</span><span class="sxs-lookup"><span data-stu-id="31aad-3691">A keyword from Keyword_itin is found.</span></span>
    - <span data-ttu-id="31aad-3692">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="31aad-3692">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="31aad-3693">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3693">The function Func_us_date finds a date in the right date format.</span></span>
    - <span data-ttu-id="31aad-3694">найдено ключевое слово из Keyword_itin_collaborative.</span><span class="sxs-lookup"><span data-stu-id="31aad-3694">A keyword from Keyword_itin_collaborative is found.</span></span>

<span data-ttu-id="31aad-3695">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3695">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3696">Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3696">The function Func_unformatted_itin finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3697">Верно по меньшей мере одно из условий ниже:</span><span class="sxs-lookup"><span data-stu-id="31aad-3697">At least one of the following is true:</span></span>
    - <span data-ttu-id="31aad-3698">найдено ключевое слово из Keyword_itin_collaborative;</span><span class="sxs-lookup"><span data-stu-id="31aad-3698">A keyword from Keyword_itin_collaborative is found.</span></span>
    - <span data-ttu-id="31aad-3699">функция Func_us_address находит адрес в правильном формате;</span><span class="sxs-lookup"><span data-stu-id="31aad-3699">The function Func_us_address finds an address in the right date format.</span></span>
    - <span data-ttu-id="31aad-3700">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3700">The function Func_us_date finds a date in the right date format.</span></span>

```xml
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

### <a name="keywords"></a><span data-ttu-id="31aad-3701">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3701">Keywords</span></span>

#### <a name="keyword_itin"></a><span data-ttu-id="31aad-3702">Keyword_itin</span><span class="sxs-lookup"><span data-stu-id="31aad-3702">Keyword_itin</span></span>

- <span data-ttu-id="31aad-3703">дубликат</span><span class="sxs-lookup"><span data-stu-id="31aad-3703">taxpayer</span></span> 
- <span data-ttu-id="31aad-3704">tax id</span><span class="sxs-lookup"><span data-stu-id="31aad-3704">tax id</span></span> 
- <span data-ttu-id="31aad-3705">tax identification</span><span class="sxs-lookup"><span data-stu-id="31aad-3705">tax identification</span></span> 
- <span data-ttu-id="31aad-3706">SharePointв</span><span class="sxs-lookup"><span data-stu-id="31aad-3706">itin</span></span> 
- <span data-ttu-id="31aad-3707">SSN</span><span class="sxs-lookup"><span data-stu-id="31aad-3707">ssn</span></span> 
- <span data-ttu-id="31aad-3708">ИНН</span><span class="sxs-lookup"><span data-stu-id="31aad-3708">tin</span></span> 
- <span data-ttu-id="31aad-3709">social security</span><span class="sxs-lookup"><span data-stu-id="31aad-3709">social security</span></span> 
- <span data-ttu-id="31aad-3710">tax payer</span><span class="sxs-lookup"><span data-stu-id="31aad-3710">tax payer</span></span> 
- <span data-ttu-id="31aad-3711">итинс</span><span class="sxs-lookup"><span data-stu-id="31aad-3711">itins</span></span> 
- <span data-ttu-id="31aad-3712">такси</span><span class="sxs-lookup"><span data-stu-id="31aad-3712">taxid</span></span> 
- <span data-ttu-id="31aad-3713">individual taxpayer</span><span class="sxs-lookup"><span data-stu-id="31aad-3713">individual taxpayer</span></span> 

#### <a name="keyword_itin_collaborative"></a><span data-ttu-id="31aad-3714">Keyword_itin_collaborative</span><span class="sxs-lookup"><span data-stu-id="31aad-3714">Keyword_itin_collaborative</span></span>

- <span data-ttu-id="31aad-3715">Лицензия</span><span class="sxs-lookup"><span data-stu-id="31aad-3715">License</span></span> 
- <span data-ttu-id="31aad-3716">DL</span><span class="sxs-lookup"><span data-stu-id="31aad-3716">DL</span></span> 
- <span data-ttu-id="31aad-3717">доб</span><span class="sxs-lookup"><span data-stu-id="31aad-3717">DOB</span></span> 
- <span data-ttu-id="31aad-3718">Birthdate</span><span class="sxs-lookup"><span data-stu-id="31aad-3718">Birthdate</span></span> 
- <span data-ttu-id="31aad-3719">День рождения </span><span class="sxs-lookup"><span data-stu-id="31aad-3719">Birthday</span></span> 
- <span data-ttu-id="31aad-3720">Date of Birth</span><span class="sxs-lookup"><span data-stu-id="31aad-3720">Date of Birth</span></span> 
   
## <a name="us-social-security-number-ssn"></a><span data-ttu-id="31aad-3721">Страховой номер для США (SSN)</span><span class="sxs-lookup"><span data-stu-id="31aad-3721">U.S. Social Security Number (SSN)</span></span>

### <a name="format"></a><span data-ttu-id="31aad-3722">Format</span><span class="sxs-lookup"><span data-stu-id="31aad-3722">Format</span></span>

<span data-ttu-id="31aad-3723">9 цифр в виде форматированного или неформатированного шаблона.</span><span class="sxs-lookup"><span data-stu-id="31aad-3723">9 digits, which may be in a formatted or unformatted pattern</span></span>

> [!NOTE]
> <span data-ttu-id="31aad-3724">Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).</span><span class="sxs-lookup"><span data-stu-id="31aad-3724">If issued before mid-2011, an SSN has strong formatting where certain parts of the number must fall within certain ranges to be valid (but there's no checksum).</span></span>

### <a name="pattern"></a><span data-ttu-id="31aad-3725">Шаблон</span><span class="sxs-lookup"><span data-stu-id="31aad-3725">Pattern</span></span>

<span data-ttu-id="31aad-3726">Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:</span><span class="sxs-lookup"><span data-stu-id="31aad-3726">Four functions look for SSNs in four different patterns:</span></span>
- <span data-ttu-id="31aad-3727">Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="31aad-3727">Func_ssn finds SSNs with pre-2011 strong formatting that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="31aad-3728">Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);</span><span class="sxs-lookup"><span data-stu-id="31aad-3728">Func_unformatted_ssn finds SSNs with pre-2011 strong formatting that are unformatted as nine consecutive digits (ddddddddd)</span></span>
- <span data-ttu-id="31aad-3729">Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);</span><span class="sxs-lookup"><span data-stu-id="31aad-3729">Func_randomized_formatted_ssn finds post-2011 SSNs that are formatted with dashes or spaces (ddd-dd-dddd OR ddd dd dddd)</span></span>
- <span data-ttu-id="31aad-3730">Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).</span><span class="sxs-lookup"><span data-stu-id="31aad-3730">Func_randomized_unformatted_ssn finds post-2011 SSNs that are unformatted as nine consecutive digits (ddddddddd)</span></span>

### <a name="checksum"></a><span data-ttu-id="31aad-3731">Контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="31aad-3731">Checksum</span></span>

<span data-ttu-id="31aad-3732">Нет</span><span class="sxs-lookup"><span data-stu-id="31aad-3732">No</span></span>


### <a name="definition"></a><span data-ttu-id="31aad-3733">Определение</span><span class="sxs-lookup"><span data-stu-id="31aad-3733">Definition</span></span>

<span data-ttu-id="31aad-3734">Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3734">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3735">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3735">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3736">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="31aad-3736">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="31aad-3737">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3737">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-3738">Функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3738">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="31aad-3739">Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3739">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3740">Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3740">The function Func_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3741">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="31aad-3741">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="31aad-3742">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3742">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-3743">Функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3743">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="31aad-3744">Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3744">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3745">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3745">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3746">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="31aad-3746">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="31aad-3747">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3747">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-3748">Функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3748">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="31aad-3749">Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:</span><span class="sxs-lookup"><span data-stu-id="31aad-3749">A DLP policy is 55% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3750">Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3750">The function Func_randomized_unformatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3751">Находится ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="31aad-3751">A keyword from Keyword_ssn is found.</span></span>
- <span data-ttu-id="31aad-3752">функция Func_us_date находит дату в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3752">The function Func_us_date finds a date in the right date format.</span></span>
- <span data-ttu-id="31aad-3753">Функция Func_us_address находит адрес в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="31aad-3753">The function Func_us_address finds an address in the right format.</span></span>

<span data-ttu-id="31aad-3754">Политика защиты от потери данных — 40% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах расстояния от 300 символов:</span><span class="sxs-lookup"><span data-stu-id="31aad-3754">A DLP policy is 40% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
- <span data-ttu-id="31aad-3755">Функция Func_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3755">The function Func_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3756">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3756">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3757">Функция Func_randomized_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3757">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3758">Не найдено ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="31aad-3758">A keyword from Keyword_ssn is not found.</span></span>
 
<span data-ttu-id="31aad-3759">или</span><span class="sxs-lookup"><span data-stu-id="31aad-3759">Or</span></span>

- <span data-ttu-id="31aad-3760">Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3760">The function Func_randomized_formatted_ssn finds content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3761">Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3761">The function Func_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3762">Функция Func_randomized_unformatted_ssn не находит содержимое, которое соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="31aad-3762">The function Func_randomized_unformatted_ssn does not find content that matches the pattern.</span></span>
- <span data-ttu-id="31aad-3763">Не найдено ключевое слово из Keyword_ssn.</span><span class="sxs-lookup"><span data-stu-id="31aad-3763">A keyword from Keyword_ssn is not found.</span></span>

```xml
<!-- U.S. Social Security Number (SSN) -->
  <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="1">
          <Match idRef="Keyword_ssn" />
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="1">
          <Match idRef="Func_us_date" />
          <Match idRef="Func_us_address" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="40">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
          <Match idRef="Func_randomized_unformatted_ssn" />
          <Match idRef="Keyword_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a><span data-ttu-id="31aad-3764">Ключевые слова</span><span class="sxs-lookup"><span data-stu-id="31aad-3764">Keywords</span></span>

#### <a name="keyword_ssn"></a><span data-ttu-id="31aad-3765">Keyword_ssn</span><span class="sxs-lookup"><span data-stu-id="31aad-3765">Keyword_ssn</span></span>

- <span data-ttu-id="31aad-3766">Social Security</span><span class="sxs-lookup"><span data-stu-id="31aad-3766">Social Security</span></span> 
- <span data-ttu-id="31aad-3767">Social Security#</span><span class="sxs-lookup"><span data-stu-id="31aad-3767">Social Security#</span></span> 
- <span data-ttu-id="31aad-3768">Soc Sec</span><span class="sxs-lookup"><span data-stu-id="31aad-3768">Soc Sec</span></span> 
- <span data-ttu-id="31aad-3769">SSN</span><span class="sxs-lookup"><span data-stu-id="31aad-3769">SSN</span></span> 
- <span data-ttu-id="31aad-3770">SSNS</span><span class="sxs-lookup"><span data-stu-id="31aad-3770">SSNS</span></span> 
- <span data-ttu-id="31aad-3771">SSN #</span><span class="sxs-lookup"><span data-stu-id="31aad-3771">SSN#</span></span> 
- <span data-ttu-id="31aad-3772">НН #</span><span class="sxs-lookup"><span data-stu-id="31aad-3772">SS#</span></span> 
- <span data-ttu-id="31aad-3773">SSID</span><span class="sxs-lookup"><span data-stu-id="31aad-3773">SSID</span></span> 
   

