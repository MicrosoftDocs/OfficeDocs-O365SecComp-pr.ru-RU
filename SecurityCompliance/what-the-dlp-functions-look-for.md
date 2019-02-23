---
title: Сведения, для обнаружения которых используются функции защиты от потери данных
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/18/2016
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 94349ed4-5351-4ee2-bbda-70813c9ed693
description: Типы конфиденциальной информации ищут определенный шаблон и корроборате его, обеспечивая правильное форматирование, заменяя контрольные суммы и ищут соответствующие ключевые слова или другие сведения. Некоторые из этих функций выполняются внутренними функциями. В этом разделе объясняется, что эти функции ищут, чтобы помочь вам оценить принципы работы предопределенных типов конфиденциальных данных.
ms.openlocfilehash: 55c740e892e92902b368b2dcf7b0999cbc60f3ed
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219359"
---
# <a name="what-the-dlp-functions-look-for"></a><span data-ttu-id="e03a7-105">Сведения, для обнаружения которых используются функции защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="e03a7-105">What the DLP functions look for</span></span>

<span data-ttu-id="e03a7-p102">Защита от потери данных включает различные типы конфиденциальной информации, такие как номер кредитной карты, номер дебетовой карты, выпущенной в ЕС, которые предусмотрены политиками защиты от потери данных. Обычно эти типы конфиденциальной информации используются для поиска данных по определенному шаблону, при этом проводится проверка правильности форматирования, применения контрольных сумм, а также наличия соответствующих ключевых слов и других данных. Для некоторых из этих проверок используются внешние функции. Например, чтобы определить, что число является номером кредитной карты, проводится поиск дат, формат которых соответствует формату даты окончания срока действия.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p102">Data loss prevention (DLP) includes sensitive information types, such as Credit Card Number and EU Debit Card Number, which are ready for you to use in your DLP policies. These sensitive information types look for a specific pattern and corroborate it by ensuring proper formatting, enforcing checksums, and looking for relevant keywords or other information. Some of this functionality is performed by internal functions. For example, the Credit Card Number sensitive information type uses a function to look for dates formatted like an expiration date, to help corroborate that a number is a credit card number.</span></span>
  
<span data-ttu-id="e03a7-p103">В этой статье рассказывается о сведениях, для обнаружения которых используются эти функции, что поможет вам разобраться в предопределенных типах конфиденциальной информации. Дополнительные сведения см. в статье [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="e03a7-p103">This topic explains what these functions look for, to help you understand how the predefined sensitive information types work. For more information, see [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="funcusdate"></a><span data-ttu-id="e03a7-112">Функ_ус_дате</span><span class="sxs-lookup"><span data-stu-id="e03a7-112">Func_us_date</span></span>

<span data-ttu-id="e03a7-p104">Эта функция ищет дату в формате, обычно используемом в США. К ним относятся форматы "месяц/день/год", "месяц-день-год" и "месяц суток год". В именах или сокращениях месяцев регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p104">This function looks for a date in the format commonly used in the U.S. This includes the formats "month/day/year", "month-day-year", and "month day year ". The names or abbreviations of months are not case sensitive.</span></span> 
  
<span data-ttu-id="e03a7-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="e03a7-115">Examples:</span></span>
  
- <span data-ttu-id="e03a7-116">2 декабря 2016 г.</span><span class="sxs-lookup"><span data-stu-id="e03a7-116">December 2, 2016</span></span>
    
- <span data-ttu-id="e03a7-117">2 декабря 2016 г.</span><span class="sxs-lookup"><span data-stu-id="e03a7-117">Dec 2, 2016</span></span>
    
- <span data-ttu-id="e03a7-118">Dec 02 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-118">dec 02 2016</span></span>
    
- <span data-ttu-id="e03a7-119">12/2/2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-119">12/2/2016</span></span>
    
- <span data-ttu-id="e03a7-120">12/02/16</span><span class="sxs-lookup"><span data-stu-id="e03a7-120">12/02/16</span></span>
    
- <span data-ttu-id="e03a7-121">Dec – 2-2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-121">Dec-2-2016</span></span>
    
- <span data-ttu-id="e03a7-122">12-2-16</span><span class="sxs-lookup"><span data-stu-id="e03a7-122">12-2-16</span></span>
    
<span data-ttu-id="e03a7-123">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="e03a7-123">Accepted month names:</span></span>
  
- <span data-ttu-id="e03a7-124">Английский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-124">English</span></span>
    
  - <span data-ttu-id="e03a7-125">Январь, Февраль, Март, Апрель, Май, Июнь, Июль, Август, Сентябрь, Октябрь, Ноябрь, Декабрь</span><span class="sxs-lookup"><span data-stu-id="e03a7-125">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="e03a7-126">Февраль. Фев. Март. Апр. Май июня. сентября. Oct. Ноя. Дек.</span><span class="sxs-lookup"><span data-stu-id="e03a7-126">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
## <a name="funceudate"></a><span data-ttu-id="e03a7-127">Функ_еу_дате</span><span class="sxs-lookup"><span data-stu-id="e03a7-127">Func_eu_date</span></span>

<span data-ttu-id="e03a7-p105">Эта функция служит для поиска даты в формате, который обычно используется в ЕС, а также в большинстве стран за пределами США. Сюда относятся форматы "день/месяц/год", "день-месяц-год" и "день месяц год". Полные или сокращенные названия месяцев вводятся без учета регистра.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p105">This function looks for a date in the format commonly used in the E.U. (and most places outside the U.S.). This includes the formats "day/month/year", "day-month-year", and "day month year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="e03a7-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="e03a7-132">Examples:</span></span>
  
- <span data-ttu-id="e03a7-133">2 декабря 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-133">2 Dec 2016</span></span>
    
- <span data-ttu-id="e03a7-134">02 декабря 2016 г.</span><span class="sxs-lookup"><span data-stu-id="e03a7-134">02 dec 2016</span></span>
    
- <span data-ttu-id="e03a7-135">2 декабря, 16 декабря</span><span class="sxs-lookup"><span data-stu-id="e03a7-135">2 Dec 16</span></span>
    
- <span data-ttu-id="e03a7-136">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-136">2/12/2016</span></span>
    
- <span data-ttu-id="e03a7-137">02/12/16</span><span class="sxs-lookup"><span data-stu-id="e03a7-137">02/12/16</span></span>
    
- <span data-ttu-id="e03a7-138">2 декабря 2016 г.</span><span class="sxs-lookup"><span data-stu-id="e03a7-138">2-Dec-2016</span></span>
    
- <span data-ttu-id="e03a7-139">2-12-16</span><span class="sxs-lookup"><span data-stu-id="e03a7-139">2-12-16</span></span>
    
<span data-ttu-id="e03a7-140">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="e03a7-140">Accepted month names:</span></span>
  
- <span data-ttu-id="e03a7-141">Английский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-141">English</span></span>
    
  - <span data-ttu-id="e03a7-142">Январь, Февраль, Март, Апрель, Май, Июнь, Июль, Август, Сентябрь, Октябрь, Ноябрь, Декабрь</span><span class="sxs-lookup"><span data-stu-id="e03a7-142">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="e03a7-143">Февраль. Фев. Март. Апр. Май июня. сентября. Oct. Ноя. Дек.</span><span class="sxs-lookup"><span data-stu-id="e03a7-143">Jan. Feb. Mar. Apr. May June July Aug. Sept. Oct. Nov. Dec.</span></span>
    
- <span data-ttu-id="e03a7-144">Нидерландский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-144">Dutch</span></span>
    
  - <span data-ttu-id="e03a7-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="e03a7-145">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="e03a7-146">Февраль февраля МАарт апреля Меи июня 2004 Янв, Сен сентября, Окт ноября декабря</span><span class="sxs-lookup"><span data-stu-id="e03a7-146">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
- <span data-ttu-id="e03a7-147">Французский</span><span class="sxs-lookup"><span data-stu-id="e03a7-147">French</span></span>
    
  - <span data-ttu-id="e03a7-148">жанвиер, фéвриер, Mars, Аврил, Чиангмай, жуин жуиллет, аоûт, септембре, октобре, Новембре, дéцембре</span><span class="sxs-lookup"><span data-stu-id="e03a7-148">janvier, février, mars, avril, mai, juin juillet, août, septembre, octobre, novembre, décembre</span></span>
    
  - <span data-ttu-id="e03a7-p106">жанв. фéвр. режим MARS Аврил Чиангмай жуин жуил. аоûт сентября. Oct. Ноя. дéк.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p106">janv. févr. mars avril mai juin juil. août sept. oct. nov. déc.</span></span>
    
- <span data-ttu-id="e03a7-156">Немецкий</span><span class="sxs-lookup"><span data-stu-id="e03a7-156">German</span></span>
    
  - <span data-ttu-id="e03a7-157">жäнуар, фебруар, мäрз, Апрель, Чиангмай, жуни Жули, Август, Сентябрь, Октобер, Ноябрь, дезембер</span><span class="sxs-lookup"><span data-stu-id="e03a7-157">jänuar, februar, märz, April, mai, juni juli, August, September, oktober, November, dezember</span></span>
    
  - <span data-ttu-id="e03a7-p107">Янв./Жäн. Фев. Мäрз Apr. Чиангмай Жуни Жули Авг. Сентябрь. Окт. Ноя. дез.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p107">Jan./Jän. Feb. März Apr. Mai Juni Juli Aug. Sept. Okt. Nov. Dez.</span></span>
    
- <span data-ttu-id="e03a7-161">Итальянский</span><span class="sxs-lookup"><span data-stu-id="e03a7-161">Italian</span></span>
    
  - <span data-ttu-id="e03a7-162">женнаио, феббраио, Марзо, Апрель, маггио, гиугно, луглио, Агосто, Сеттембре, Оттобре, Новембре, дицембре</span><span class="sxs-lookup"><span data-stu-id="e03a7-162">gennaio, febbraio, marzo, aprile, maggio, giugno, luglio, agosto, settembre, ottobre, novembre, dicembre</span></span>
    
  - <span data-ttu-id="e03a7-p108">Женн. феббр. Мар. Апрель. Магг. гиугно луглио AG. Переключател. and. ноября. DIC.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p108">genn. febbr. mar. apr. magg. giugno luglio ag. sett. ott. nov. dic.</span></span>
    
- <span data-ttu-id="e03a7-173">Португальский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-173">Portuguese</span></span>
    
  - <span data-ttu-id="e03a7-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="e03a7-174">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="e03a7-175">Янв Фев Mar, Чиангмай, 2004 июня, назад, Настройка ноября Ноя дез</span><span class="sxs-lookup"><span data-stu-id="e03a7-175">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
- <span data-ttu-id="e03a7-176">Испанский</span><span class="sxs-lookup"><span data-stu-id="e03a7-176">Spanish</span></span>
    
  - <span data-ttu-id="e03a7-177">енеро, фебреро, Марзо, Абрил, Майо, Жунио, Жулио, Агосто, септиембре, Октубре, новиембре, диЦиембре</span><span class="sxs-lookup"><span data-stu-id="e03a7-177">enero, febrero, marzo, abril, mayo, junio, julio, agosto, septiembre, octubre, noviembre, diciembre</span></span>
    
  - <span data-ttu-id="e03a7-p109">енеро Фев. Марзо Граничный. Майо Июн. Июл. Агосто сентября./Сет. Oct. Ноя. DIC.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p109">enero feb. marzo abr. mayo jun. jul. agosto sept./set. oct. nov. dic.</span></span>
    
## <a name="funceudate1-deprecated"></a><span data-ttu-id="e03a7-186">Func_eu_date1 (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="e03a7-186">Func_eu_date1 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="e03a7-187">Эта функция является устаревшей, так как она поддерживает только названия месяцев на португальском языке, которые теперь `Func_eu_date` включены в функцию, описанную выше.</span><span class="sxs-lookup"><span data-stu-id="e03a7-187">This function is deprecated because it supports only Portuguese month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="e03a7-p110">Эта функция ищет дату в формате, обычно используемом на португальском языке. Формат этой функции такой же, как `Func_eu_date`и в используемом языке.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p110">This function looks for a date in the format commonly used in Portuguese. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="e03a7-190">Примеры</span><span class="sxs-lookup"><span data-stu-id="e03a7-190">Examples:</span></span>
  
- <span data-ttu-id="e03a7-191">2 дез 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-191">2 Dez 2016</span></span>
    
- <span data-ttu-id="e03a7-192">02 дез 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-192">02 dez 2016</span></span>
    
- <span data-ttu-id="e03a7-193">2 дез 16</span><span class="sxs-lookup"><span data-stu-id="e03a7-193">2 Dez 16</span></span>
    
- <span data-ttu-id="e03a7-194">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-194">2/12/2016</span></span>
    
- <span data-ttu-id="e03a7-195">02/12/16</span><span class="sxs-lookup"><span data-stu-id="e03a7-195">02/12/16</span></span>
    
- <span data-ttu-id="e03a7-196">2 — дез — 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-196">2-Dez-2016</span></span>
    
- <span data-ttu-id="e03a7-197">2-12-16</span><span class="sxs-lookup"><span data-stu-id="e03a7-197">2-12-16</span></span>
    
<span data-ttu-id="e03a7-198">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="e03a7-198">Accepted month names:</span></span>
  
- <span data-ttu-id="e03a7-199">Португальский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-199">Portuguese</span></span>
    
  - <span data-ttu-id="e03a7-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span><span class="sxs-lookup"><span data-stu-id="e03a7-200">janeiro, fevereiro, março, marco, abril, maio, junho, julho, agosto, setembro, outubro, novembro, dezembro</span></span>
    
  - <span data-ttu-id="e03a7-201">Янв Фев Mar, Чиангмай, 2004 июня, назад, Настройка ноября Ноя дез</span><span class="sxs-lookup"><span data-stu-id="e03a7-201">jan fev mar abr mai jun jul ago set out nov dez</span></span>
    
## <a name="funceudate2-deprecated"></a><span data-ttu-id="e03a7-202">Func_eu_date2 (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="e03a7-202">Func_eu_date2 (deprecated)</span></span>

> [!NOTE]
> <span data-ttu-id="e03a7-203">Эта функция является устаревшей, так как она поддерживает только названия в голландских месяцах, которые `Func_eu_date` теперь включены в функцию, описанную выше.</span><span class="sxs-lookup"><span data-stu-id="e03a7-203">This function is deprecated because it supports only Dutch month names, which are now included in the  `Func_eu_date` function above.</span></span> 
  
<span data-ttu-id="e03a7-p111">Эта функция ищет дату в формате, обычно используемом в нидерландском языке. Формат этой функции такой же, как `Func_eu_date`и в используемом языке.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p111">This function looks for a date in the format commonly used in Dutch. The format for this function is the same as  `Func_eu_date`, differing only in the language used.</span></span>
  
<span data-ttu-id="e03a7-206">Примеры</span><span class="sxs-lookup"><span data-stu-id="e03a7-206">Examples:</span></span>
  
- <span data-ttu-id="e03a7-207">2 Меи 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-207">2 Mei 2016</span></span>
    
- <span data-ttu-id="e03a7-208">02 Меи 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-208">02 mei 2016</span></span>
    
- <span data-ttu-id="e03a7-209">2 Меи 16</span><span class="sxs-lookup"><span data-stu-id="e03a7-209">2 Mei 16</span></span>
    
- <span data-ttu-id="e03a7-210">2/12/2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-210">2/12/2016</span></span>
    
- <span data-ttu-id="e03a7-211">02/12/16</span><span class="sxs-lookup"><span data-stu-id="e03a7-211">02/12/16</span></span>
    
- <span data-ttu-id="e03a7-212">2 — Меи — 2016</span><span class="sxs-lookup"><span data-stu-id="e03a7-212">2-Mei-2016</span></span>
    
- <span data-ttu-id="e03a7-213">2-12-16</span><span class="sxs-lookup"><span data-stu-id="e03a7-213">2-12-16</span></span>
    
<span data-ttu-id="e03a7-214">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="e03a7-214">Accepted month names:</span></span>
  
- <span data-ttu-id="e03a7-215">Нидерландский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-215">Dutch</span></span>
    
  - <span data-ttu-id="e03a7-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span><span class="sxs-lookup"><span data-stu-id="e03a7-216">januari, februari, maart, April, mei, juni, juli, augustus, September, ocktober, October, November, December</span></span>
    
  - <span data-ttu-id="e03a7-217">Февраль февраля МАарт апреля Меи июня 2004 Янв, Сен сентября, Окт ноября декабря</span><span class="sxs-lookup"><span data-stu-id="e03a7-217">jan feb maart apr mei jun jul aug sep sept oct okt nov dec</span></span>
    
## <a name="funcexpirationdate"></a><span data-ttu-id="e03a7-218">Функ_експиратион_дате</span><span class="sxs-lookup"><span data-stu-id="e03a7-218">Func_expiration_date</span></span>

<span data-ttu-id="e03a7-p112">Эта функция ищет дату в форматах, которые обычно используются кредитными и дебетовыми картами, которые исключают дни в течение месяцев. Эта функция будет сопоставлять даты в формате "месяц/год", "month-Year", "[название месяца] год" и "[аббревиатура] год". В именах или сокращениях месяцев регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p112">This function looks for a date in the formats commonly used by credit and debit cards, which exclude days in favor of months. This function will match dates in format of "month/year", "month-year", "[month name] year", and "[month abbreviation] year". The names or abbreviations of months are not case sensitive.</span></span>
  
<span data-ttu-id="e03a7-222">Примеры</span><span class="sxs-lookup"><span data-stu-id="e03a7-222">Examples:</span></span>
  
- <span data-ttu-id="e03a7-223">ММ/ГГ (например, 01/11 или 1/11);</span><span class="sxs-lookup"><span data-stu-id="e03a7-223">MM/YY -- for example, 01/11 or 1/11</span></span>
    
- <span data-ttu-id="e03a7-224">ММ/ГГГГ (например, 01/2011 или 1/2011);</span><span class="sxs-lookup"><span data-stu-id="e03a7-224">MM/YYYY -- for example, 01/2011 or 1/2011</span></span>
    
- <span data-ttu-id="e03a7-225">ММ-ГГ (например, 01-22 или 1-11);</span><span class="sxs-lookup"><span data-stu-id="e03a7-225">MM-YY -- for example, 01-22 or 1-11</span></span>
    
- <span data-ttu-id="e03a7-226">ММ-ГГГГ (например, 01-2000 или 1-2000).</span><span class="sxs-lookup"><span data-stu-id="e03a7-226">MM-YYYY -- for example, 01-2000 or 1-2000</span></span>
    
<span data-ttu-id="e03a7-227">Следующие форматы поддерживают ГГ или ГГГГ:</span><span class="sxs-lookup"><span data-stu-id="e03a7-227">The following formats support YY or YYYY:</span></span>
  
- <span data-ttu-id="e03a7-228">Месяц-ГГГГ (например, янв-2010, январь-2010, янв-10 или январь-10);</span><span class="sxs-lookup"><span data-stu-id="e03a7-228">Month-YYYY -- for example, .Jan-2010 or january-2010 or Jan-10 or january-10</span></span>
    
- <span data-ttu-id="e03a7-229">Месяц ГГГГ (например, "январь 2010", "янв 2010", "январь 10" или "янв 10");</span><span class="sxs-lookup"><span data-stu-id="e03a7-229">Month YYYY -- for example, 'january 2010' or 'Jan 2010' or 'january 10' or 'Jan 10'</span></span>
    
- <span data-ttu-id="e03a7-230">МесяцГГГГ (например, "январь2010", "янв2010", "январь10" или "янв10");</span><span class="sxs-lookup"><span data-stu-id="e03a7-230">MonthYYYY -- for example, 'january2010' or 'Jan2010' or 'january10' or 'Jan10'</span></span>
    
- <span data-ttu-id="e03a7-231">Month/гггг, например, "Январь/2010" или "Янв/2010" или "Январь/10" или "Янв/10"</span><span class="sxs-lookup"><span data-stu-id="e03a7-231">Month/YYYY -- for example, 'january/2010' or 'Jan/2010' or 'january/10' or 'Jan/10'</span></span>
    
<span data-ttu-id="e03a7-232">Принятые названия месяцев:</span><span class="sxs-lookup"><span data-stu-id="e03a7-232">Accepted month names:</span></span>
  
- <span data-ttu-id="e03a7-233">Английский язык</span><span class="sxs-lookup"><span data-stu-id="e03a7-233">English</span></span>
    
  - <span data-ttu-id="e03a7-234">Январь, Февраль, Март, Апрель, Май, Июнь, Июль, Август, Сентябрь, Октябрь, Ноябрь, Декабрь</span><span class="sxs-lookup"><span data-stu-id="e03a7-234">January, February, march, April, may, June, July, August, September, October, November, December</span></span>
    
  - <span data-ttu-id="e03a7-235">Февраль февраля Mar апреля, Май, Сентябрь октября октября, Май</span><span class="sxs-lookup"><span data-stu-id="e03a7-235">Jan Feb Mar Apr May June July Aug Sept Oct Nov Dec</span></span>
    
## <a name="funcusaddress"></a><span data-ttu-id="e03a7-236">Функ_ус_аддресс</span><span class="sxs-lookup"><span data-stu-id="e03a7-236">Func_us_address</span></span>

<span data-ttu-id="e03a7-p113">Эта функция служит для поиска названия штата США или его почтовой аббревиатуры вместе с почтовым индексом в том же виде, в котором они указываются в почтовых адресах. Необходимо указать правильный почтовый индекс, соответствующий названию штата США или его аббревиатуре. Название штата США и почтовый индекс не должны разделяться знаками пунктуации или буквами.</span><span class="sxs-lookup"><span data-stu-id="e03a7-p113">This function looks for a U.S. state name or postal abbreviation followed by a valid zip code, just as they are used in postal addresses. The zip code must be one of the correct zip codes associated with the U.S. state name or abbreviation. The U.S. state name and zip code cannot be separated by punctuation or letters.</span></span>
  
<span data-ttu-id="e03a7-240">Примеры:</span><span class="sxs-lookup"><span data-stu-id="e03a7-240">Examples:</span></span>
  
- <span data-ttu-id="e03a7-241">Washington 98052</span><span class="sxs-lookup"><span data-stu-id="e03a7-241">Washington 98052</span></span>
    
- <span data-ttu-id="e03a7-242">Washington 98052-9998</span><span class="sxs-lookup"><span data-stu-id="e03a7-242">Washington 98052-9998</span></span>
    
- <span data-ttu-id="e03a7-243">WA 98052</span><span class="sxs-lookup"><span data-stu-id="e03a7-243">WA 98052</span></span>
    
- <span data-ttu-id="e03a7-244">WA 98052-9998</span><span class="sxs-lookup"><span data-stu-id="e03a7-244">WA 98052-9998</span></span>
    

