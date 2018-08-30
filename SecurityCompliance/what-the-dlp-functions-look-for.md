---
title: Сведения, для обнаружения которых используются функции защиты от потери данных
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Типы конфиденциальных сведений найдите конкретный шаблон и отследить, чтобы убедиться в правильной форматирование, применение контрольные и соответствующие ключевые слова и другие сведения. Некоторые из функций выполняется с внутренними функциями. В этом разделе объясняется, что эти функции поиска, помогут вам понять, как работают типы предварительно заданных конфиденциальной информации.
ms.openlocfilehash: 510f98e2b4e1d2480550f11026cf445be6ffc931
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013763"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="81ac7-105">Сведения, для обнаружения которых используются функции защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="81ac7-105">What the DLP functions look for</span></span>

<span data-ttu-id="81ac7-p102">Защита от потери данных включает различные типы конфиденциальной информации, такие как номер кредитной карты, номер дебетовой карты, выпущенной в ЕС, которые предусмотрены политиками защиты от потери данных. Обычно эти типы конфиденциальной информации используются для поиска данных по определенному шаблону, при этом проводится проверка правильности форматирования, применения контрольных сумм, а также наличия соответствующих ключевых слов и других данных. Для некоторых из этих проверок используются внешние функции. Например, чтобы определить, что число является номером кредитной карты, проводится поиск дат, формат которых соответствует формату даты окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="81ac7-p103">В этой статье рассказывается о сведениях, для обнаружения которых используются эти функции, что поможет вам разобраться в предопределенных типах конфиденциальной информации. Дополнительные сведения см. в статье [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="81ac7-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="81ac7-112">Func_us_date</span><span class="sxs-lookup"><span data-stu-id="81ac7-112">Func_us_date</span></span>

<span data-ttu-id="81ac7-p104">Эта функция выполняет поиск даты в формате, обычно используемые в США. Это включает в себя форматы «месяц/день/год», «месяц день год» и «месяц день года». Имена и сокращения месяцев регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="81ac7-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="81ac7-115">Examples:</span></span>
  
- <span data-ttu-id="81ac7-116">2 декабря 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-116">December 2, 2016</span></span>
    
- <span data-ttu-id="81ac7-117">2 декабря 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="81ac7-118">дек 02 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-118">dec 02 2016</span></span>
    
- <span data-ttu-id="81ac7-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-119">12/2/2016</span></span>
    
- <span data-ttu-id="81ac7-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="81ac7-120">12/02/16</span></span>
    
- <span data-ttu-id="81ac7-121">Дек-2-2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="81ac7-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="81ac7-122">12-2-16</span></span>
    
<span data-ttu-id="81ac7-123">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="81ac7-123">Accepted month names:</span></span>
  
- <span data-ttu-id="81ac7-124">Английский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-124">English</span></span>
    
  - <span data-ttu-id="81ac7-125">Январь, февраль, март, апрель, может, июнь, июль, август, сентябрь, октябрь, ноябрь, декабрь</span><span class="sxs-lookup"><span data-stu-id="81ac7-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="81ac7-126">Февраль января Mar. апреля может июня июля августа Сент октября дек ноября.</span><span class="sxs-lookup"><span data-stu-id="81ac7-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="81ac7-127">Func_eu_date</span><span class="sxs-lookup"><span data-stu-id="81ac7-127">Func_eu_date</span></span>

<span data-ttu-id="81ac7-p105">Эта функция служит для поиска даты в формате, который обычно используется в ЕС, а также в большинстве стран за пределами США. Сюда относятся форматы "день/месяц/год", "день-месяц-год" и "день месяц год". Полные или сокращенные названия месяцев вводятся без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="81ac7-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="81ac7-132">Examples:</span></span>
  
- <span data-ttu-id="81ac7-133">2 декабря 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="81ac7-134">02 декабря 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-134">02 dec 2016</span></span>
    
- <span data-ttu-id="81ac7-135">2 декабря 16</span><span class="sxs-lookup"><span data-stu-id="81ac7-135">2 Dec 16</span></span>
    
- <span data-ttu-id="81ac7-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-136">2/12/2016</span></span>
    
- <span data-ttu-id="81ac7-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="81ac7-137">02/12/16</span></span>
    
- <span data-ttu-id="81ac7-138">2 декабря 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="81ac7-139">2 — 12-16</span><span class="sxs-lookup"><span data-stu-id="81ac7-139">2-12-16</span></span>
    
<span data-ttu-id="81ac7-140">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="81ac7-140">Accepted month names:</span></span>
  
- <span data-ttu-id="81ac7-141">Английский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-141">English</span></span>
    
  - <span data-ttu-id="81ac7-142">Январь, февраль, март, апрель, может, июнь, июль, август, сентябрь, октябрь, ноябрь, декабрь</span><span class="sxs-lookup"><span data-stu-id="81ac7-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="81ac7-143">Февраль января Mar. апреля может июня июля августа Сент октября дек ноября.</span><span class="sxs-lookup"><span data-stu-id="81ac7-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="81ac7-144">Нидерландский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-144">Dutch</span></span>
    
  - <span data-ttu-id="81ac7-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="81ac7-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="81ac7-146">Ян февраля maart апреля mei июн июля августа sep сентября центра развертывания Office okt ноября дек</span><span class="sxs-lookup"><span data-stu-id="81ac7-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="81ac7-147">Французский</span><span class="sxs-lookup"><span data-stu-id="81ac7-147">French</span></span>
    
  - <span data-ttu-id="81ac7-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span><span class="sxs-lookup"><span data-stu-id="81ac7-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="81ac7-p106">janv. févr. MARS avril mai juin juil. août сентября. октября ноября. déc.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="81ac7-156">Немецкий</span><span class="sxs-lookup"><span data-stu-id="81ac7-156">German</span></span>
    
  - <span data-ttu-id="81ac7-157">jänuar, februar, märz, апрель, mai, juli juni, август, сентябрь, oktober, ноябрь, dezember</span><span class="sxs-lookup"><span data-stu-id="81ac7-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="81ac7-p107">Ян. / Jän. Февраль März Mai апреля Juni Juli августа Сент Okt. Dez ноября.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="81ac7-161">Итальянский</span><span class="sxs-lookup"><span data-stu-id="81ac7-161">Italian</span></span>
    
  - <span data-ttu-id="81ac7-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span><span class="sxs-lookup"><span data-stu-id="81ac7-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="81ac7-p108">genn. febbr. марта. апреля. magg. giugno luglio ag. Настройка. ott. ноября. dic.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="81ac7-173">Португальский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-173">Portuguese</span></span>
    
  - <span data-ttu-id="81ac7-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="81ac7-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="81ac7-175">Ян fev мар abr mai июн июля назад больше dez ноября</span><span class="sxs-lookup"><span data-stu-id="81ac7-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="81ac7-176">Испанский</span><span class="sxs-lookup"><span data-stu-id="81ac7-176">Spanish</span></span>
    
  - <span data-ttu-id="81ac7-177">enero, febrero, marzo, abril, майо, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span><span class="sxs-lookup"><span data-stu-id="81ac7-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="81ac7-p109">enero февраля. jun. майо abr. marzo июля. Сент agosto/set. октября ноября. dic.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="81ac7-186">Func_eu_date1 (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="81ac7-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="81ac7-187">Рекомендуется использовать эту функцию, поскольку она поддерживает только португальский месяц имен, которые теперь включены в `Func_eu_date` функция выше.</span><span class="sxs-lookup"><span data-stu-id="81ac7-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="81ac7-p110">Эта функция выполняет поиск даты в формате, обычно используемые в португальский. Формат для этой функции совпадает с `Func_eu_date`, отличающихся только в языке.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="81ac7-190">Примеры</span><span class="sxs-lookup"><span data-stu-id="81ac7-190">Examples:</span></span>
  
- <span data-ttu-id="81ac7-191">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="81ac7-192">02 dez 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-192">02 dez 2016</span></span>
    
- <span data-ttu-id="81ac7-193">2 Dez 16</span><span class="sxs-lookup"><span data-stu-id="81ac7-193">2 Dez 16</span></span>
    
- <span data-ttu-id="81ac7-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-194">2/12/2016</span></span>
    
- <span data-ttu-id="81ac7-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="81ac7-195">02/12/16</span></span>
    
- <span data-ttu-id="81ac7-196">2 Dez 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="81ac7-197">2 — 12-16</span><span class="sxs-lookup"><span data-stu-id="81ac7-197">2-12-16</span></span>
    
<span data-ttu-id="81ac7-198">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="81ac7-198">Accepted month names:</span></span>
  
- <span data-ttu-id="81ac7-199">Португальский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-199">Portuguese</span></span>
    
  - <span data-ttu-id="81ac7-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="81ac7-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="81ac7-201">Ян fev мар abr mai июн июля назад больше dez ноября</span><span class="sxs-lookup"><span data-stu-id="81ac7-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="81ac7-202">Func_eu_date2 (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="81ac7-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="81ac7-203">Рекомендуется использовать эту функцию, поскольку она поддерживает только имен голландский месяц, которые теперь включены в `Func_eu_date` функция выше.</span><span class="sxs-lookup"><span data-stu-id="81ac7-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="81ac7-p111">Эта функция выполняет поиск даты в формате, обычно используется на нидерландском. Формат для этой функции совпадает с `Func_eu_date`, отличающихся только в языке.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="81ac7-206">Примеры</span><span class="sxs-lookup"><span data-stu-id="81ac7-206">Examples:</span></span>
  
- <span data-ttu-id="81ac7-207">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="81ac7-208">02 mei 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-208">02 mei 2016</span></span>
    
- <span data-ttu-id="81ac7-209">2 Mei 16</span><span class="sxs-lookup"><span data-stu-id="81ac7-209">2 Mei 16</span></span>
    
- <span data-ttu-id="81ac7-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-210">2/12/2016</span></span>
    
- <span data-ttu-id="81ac7-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="81ac7-211">02/12/16</span></span>
    
- <span data-ttu-id="81ac7-212">2 Mei 2016</span><span class="sxs-lookup"><span data-stu-id="81ac7-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="81ac7-213">2 — 12-16</span><span class="sxs-lookup"><span data-stu-id="81ac7-213">2-12-16</span></span>
    
<span data-ttu-id="81ac7-214">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="81ac7-214">Accepted month names:</span></span>
  
- <span data-ttu-id="81ac7-215">Нидерландский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-215">Dutch</span></span>
    
  - <span data-ttu-id="81ac7-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="81ac7-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="81ac7-217">Ян февраля maart апреля mei июн июля августа sep сентября центра развертывания Office okt ноября дек</span><span class="sxs-lookup"><span data-stu-id="81ac7-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="81ac7-218">Func_expiration_date</span><span class="sxs-lookup"><span data-stu-id="81ac7-218">Func_expiration_date</span></span>

<span data-ttu-id="81ac7-p112">Эта функция выполняет поиск даты в форматах, часто используемые кредит и банковской карты, которые исключить дней пользу месяцев. Эта функция будет соответствовать даты в формате «месяц/год», «месяц года», «[название месяца] года» и «год [месяц аббревиатура]». Имена и сокращения месяцев регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="81ac7-222">Примеры</span><span class="sxs-lookup"><span data-stu-id="81ac7-222">Examples:</span></span>
  
- <span data-ttu-id="81ac7-223">ММ/ГГ (например, 01/11 или 1/11);</span><span class="sxs-lookup"><span data-stu-id="81ac7-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="81ac7-224">ММ/ГГГГ (например, 01/2011 или 1/2011);</span><span class="sxs-lookup"><span data-stu-id="81ac7-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="81ac7-225">ММ-ГГ (например, 01-22 или 1-11);</span><span class="sxs-lookup"><span data-stu-id="81ac7-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="81ac7-226">ММ-ГГГГ (например, 01-2000 или 1-2000).</span><span class="sxs-lookup"><span data-stu-id="81ac7-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="81ac7-227">Следующие форматы поддерживают ГГ или ГГГГ:</span><span class="sxs-lookup"><span data-stu-id="81ac7-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="81ac7-228">Месяц-ГГГГ (например, янв-2010, январь-2010, янв-10 или январь-10);</span><span class="sxs-lookup"><span data-stu-id="81ac7-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="81ac7-229">Месяц ГГГГ (например, "январь 2010", "янв 2010", "январь 10" или "янв 10");</span><span class="sxs-lookup"><span data-stu-id="81ac7-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="81ac7-230">МесяцГГГГ (например, "январь2010", "янв2010", "январь10" или "янв10");</span><span class="sxs-lookup"><span data-stu-id="81ac7-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="81ac7-231">Месяц/гггг — например, «январь/2010"или «янв/2010" или «января/10"или «янв/10"</span><span class="sxs-lookup"><span data-stu-id="81ac7-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="81ac7-232">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="81ac7-232">Accepted month names:</span></span>
  
- <span data-ttu-id="81ac7-233">Английский язык</span><span class="sxs-lookup"><span data-stu-id="81ac7-233">English</span></span>
    
  - <span data-ttu-id="81ac7-234">Январь, февраль, март, апрель, может, июнь, июль, август, сентябрь, октябрь, ноябрь, декабрь</span><span class="sxs-lookup"><span data-stu-id="81ac7-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="81ac7-235">Ян февраля апреля мар может июня июля августа сентября центра развертывания Office дек ноября</span><span class="sxs-lookup"><span data-stu-id="81ac7-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="81ac7-236">Func_us_address</span><span class="sxs-lookup"><span data-stu-id="81ac7-236">Func_us_address</span></span>

<span data-ttu-id="81ac7-p113">Эта функция служит для поиска названия штата США или его почтовой аббревиатуры вместе с почтовым индексом в том же виде, в котором они указываются в почтовых адресах. Необходимо указать правильный почтовый индекс, соответствующий названию штата США или его аббревиатуре. Название штата США и почтовый индекс не должны разделяться знаками пунктуации или буквами.</span><span class="sxs-lookup"><span data-stu-id="81ac7-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="81ac7-240">Примеры</span><span class="sxs-lookup"><span data-stu-id="81ac7-240">Examples:</span></span>
  
- <span data-ttu-id="81ac7-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="81ac7-241">Washington 98052</span></span>
    
- <span data-ttu-id="81ac7-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="81ac7-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="81ac7-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="81ac7-243">WA 98052</span></span>
    
- <span data-ttu-id="81ac7-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="81ac7-244">WA 98052-9998</span></span>
    

