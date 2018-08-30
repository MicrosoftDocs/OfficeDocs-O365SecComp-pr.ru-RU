---
title: Национальный ЕС идентификационный номер
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 2ea971bf-9434-4b61-b825-2bbd28ae6064
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных ЕС национальный идентификационный номер. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 29d2126b937ff46039284a74eb2a84f2ebbacb41
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534788"
---
# <a name="eu-national-identification-number"></a>Национальный ЕС идентификационный номер

В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных ЕС национальный идентификационный номер. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Формат

Сочетание 24 знаков буквы, цифры и специальные символы
  
### <a name="pattern"></a>Шаблон

24 символов:
  
-  22 букв (без учета регистра), цифр, обратной косой черты, прямая косая черта и "плюс" 
    
- (Без учета регистра) две буквы, цифры, обратной косой черты, пересылать косая черта, плюс или знак равенства
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_austria_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_austria_eu_national_id_card` найден. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_national_id_card" />
          <Match idRef="Keywords_austria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeunationalidcard"></a>Keywords_austria_eu_national_id_card

Номер Австрия удостоверений
  
Национальный идентификатор номер
  
Количество идентификаторов
  

national id
  
personalausweis republik österreich
  
## <a name="belgium"></a>Бельгия

Для получения дополнительных сведений обратитесь к разделу «Бельгия национальный номер» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="bulgaria"></a>Болгария

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

10 цифр без пробелов и разделители
  
-  Шести цифр, которые соответствуют Дата рождения (ГГММДД) 
    
- Две цифры, которые соответствуют порядке рождения
    
- Одна цифра, соответствующий Пол: четное м и нечетной цифры для женщина
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_bulgaria_national_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_bulgaria_national_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_bulgaria_national_number` находит контент, который соответствует шаблону. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_national_number" />
          <Match idRef="Keywords_bulgaria_national_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbulgarianationalnumber"></a>Keywords_bulgaria_national_number

egn
  
egn #
  
болгарский национальный номер
  
Национальный номер
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
nationalnumber
  
bnn #
  
bnn
  
личный идентификатор
  
personalidnumber #
  
ЕДИНЕН ГРАЖДАНСКИ НОМЕР
  
edinen grazhdanski nomer
  
ЕГН
  
ЕГН #
  
## <a name="croatia"></a>Хорватия

Для получения дополнительных сведений обратитесь к разделу «Номер Хорватия удостоверений» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="cyprus"></a>Кипр

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 10 цифр 
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_cyprus_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_cyprus_eu_national_id_card` найден. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_national_id_card" />
          <Match idRef="Keywords_cyprus_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscypruseunationalidcard"></a>Keywords_cyprus_eu_national_id_card

Номер идентификационной карты
  
Национальный идентификационный номер
  
личный идентификатор
  
Номер идентификационной карты
  
ΤΑΥΤΟΤΗΤΑΣ
  
## <a name="czech-republic"></a>Чешская Республика

Для получения дополнительных сведений обратитесь к разделу «Чешский национальный номер удостоверений» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="denmark"></a>Дания

Для получения дополнительных сведений обратитесь к разделу «Дания личный идентификационный номер» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="estonia"></a>Эстония

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 цифр:
  
- Одна цифра, соответствующий пол и века рождения (м четных чисел, четного числа гнездо; 1-2: 19 века; 3-4: 20 века; 5-6: 21 веке)
    
- Шести цифр, которые соответствуют Дата рождения (ГГММДД)
    
- Три цифры, которые соответствуют серийный номер, отделяя лиц на тот же день рождения
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_estonia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_estonia_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_estonia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
          <Match idRef="Keywords_estonia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsestoniaeunationalidcard"></a>Keywords_estonia_eu_national_id_card

персональный идентификационный код
  
персональный идентификационный номер
  
Национальный идентификационный номер
  
Национальный номер
  
личный идентификатор
  
personalidnumber #
  
ОК
  
isikukood
  
Идентификатор kaart
  
## <a name="finland"></a>Финляндия

Для получения дополнительных сведений обратитесь к разделу «Национальный идентификатор для Финляндии» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>Франция

Для получения дополнительных сведений обратитесь к разделу «Франция национальной ИДЕНТИФИКАЦИОННОЙ карты (CNI)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Германия

Для получения дополнительных сведений обратитесь к разделу «Номер идентификационной карты для Германии» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Греция

Для получения дополнительных сведений обратитесь к разделу «Греция национальной ИДЕНТИФИКАЦИОННОЙ карты» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Венгрия

### <a name="format"></a>Формат

11 разрядов
  
### <a name="pattern"></a>Шаблон

11 цифр:
  
-  Одна цифра, соответствующий Пол (1-м, 2-женщина, другие номера можно также использовать для жителей рождения перед 1900 или жителей с двойной Гражданская позиция) 
    
- Шести цифр, которые соответствуют Дата рождения (ГГММДД)
    
- Три цифры, которые соответствуют серийный номер
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_hungary_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
          <Match idRef="Keywords_hungary_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_national_id_card" />
</Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeunationalidcard"></a>Keywords_hungary_eu_national_id_card

персональный идентификационный номер
  
identification number

  
личный идентификатор
  
személyazonosító igazolvány
  
## <a name="ireland"></a>Ireland

### <a name="format"></a>Формат

Сочетание девяти символ буквы, цифры и места в указанному шаблону
  
### <a name="pattern"></a>Шаблон

Сочетание девяти символ буквы, цифры и места в указанному шаблону
  
От 01 января 2013 г сейчас:
  
-  семь цифр; 
    
- Один контрольный разряд
    
- Один пробел или прописная буква «W» (с учетом регистра)
    
Перед 01 января 2013 г.:
  
-  семь цифр; 
    
- Один контрольный разряд
    
- Один пробел или прописные буквы (регистр)
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция находит контент, который соответствует шаблону.
    
- Ключевое слово из найти.
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция находит контент, который соответствует шаблону.
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
          <Match idRef="Keywords_ireland_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsirelandeunationalidcard"></a>Keywords_ireland_eu_national_id_card

число личных общего пользования
  
PPS нет
  
Номер карты социального страхования и доходы
  
rsi нет
  
персональный идентификационный номер
  
identification number

  
личный идентификатор
  
uimhir phearsanta seirbhíse poiblí
  
uimh. PSP
  
## <a name="italy"></a>Италия

### <a name="format"></a>Формат

16 символов комбинацию букв или цифр в указанному шаблону
  
### <a name="pattern"></a>Шаблон

16 символов комбинацию букв или цифр:
  
- Три буквы, которые соответствуют первым трем согласных в поле имя семейства
    
- Три буквы, которые соответствуют первый, третий и четвертый согласных в поле имя
    
- Две цифры, которые соответствуют к последнему цифры года рождения
    
- Одна буква, соответствующий букве за месяц рождения — буквы используются в алфавитном порядке, но используются только буквы A E, H, L, M, P, R, чтобы T (таким образом, января-A и октября является R)
    
- Две цифры, которые соответствуют день месяца рождения — для различения мужчин и женщин, 40 добавляется в день рождения для женщин
    
- Четыре цифры, соответствующий код города, относящиеся к государственный орган, где рождения лица (Страна всей коды используются для иностранных)
    
- Одна цифра возможности
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_italy_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_italy_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_italy_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
          <Match idRef="Keywords_italy_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsitalyeunationalidcard"></a>Keywords_italy_eu_national_id_card

личный код
  
личный код
  
число личных сертификатов
  
Финансовый код
  
personalcodeno #
  
личный идентификатор
  
личный код
  
codice personale
  
numero certificato personale
  
numero personale
  
Идентификатор personale numero
  
Идентификатор personale codice
  
codice fiscale
  
## <a name="italy"></a>Италия

### <a name="format"></a>Формат

11 разрядов и дефис в указанном формате
  
### <a name="pattern"></a>Шаблон

11 разрядов и дефис:
  
-  Шести цифр, которые соответствуют Дата рождения (DDMMYY) 
    
- дефис;
    
- Одна цифра, соответствующий века рождения («0» для 19 века, для 20 века «1» и «2» для 21 веке)
    
- Четыре цифры, случайным образом
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_latvia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_latvia_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_latvia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
          <Match idRef="Keywords_latvia_eu_national_id_card" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslatviaeunationalidcard"></a>Keywords_latvia_eu_national_id_card

личный код
  
личный код
  
число личных сертификатов
  
personalcodeno #
  
личный идентификатор
  
личный код
  
действующие лица kods
  
## <a name="lithuania"></a>Литва

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 знаков без пробелов и разделители:
  
- Одна цифра, соответствующий века рождения и пол лица
    
-  Шести цифр, которые соответствуют Дата рождения (ГГММДД) 
    
- Три цифры, которые соответствуют серийный номер Дата рождения
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_lithuania_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_lithuania_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_lithuania_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
          <Match idRef="Keywords_lithuania_eu_national_id_card" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslithuaniaeunationalidcard"></a>Keywords_lithuania_eu_national_id_card

личный цифровой код
  
Уникальный идентификационный номер
  
номер службы граждан
  
количество уникальных идентификаторов
  
uniqueidentityno #
  
личный код.
  
asmeninis skaitmeninis kodas
  
unikalus identifikavimo numeris
  
piliečio paslaugos numeris
  
unikalus identifikavimo kodas
  
asmens kodas.
  
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 разрядов
  
- Одна цифра, соответствующий века рождения и пол лица
    
-  Шести цифр, которые соответствуют Дата рождения (ГГММДД) 
    
- Три цифры, которые соответствуют серийный номер Дата рождения
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_luxemburg_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_luxemburg_eu_national_id_card` найден. 
    
```
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_national_id_card" />
          <Match idRef="Keywords_luxemburg_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsluxemburgeunationalidcard"></a>Keywords_luxemburg_eu_national_id_card

личный код
  
личный идентификатор
  
personalidno #
  
Уникальный идентификатор
  
personalidnumber #
  
Уникальный идентификатор ключа
  
личный код
  
uniqueidkey #
  
отдельные кода
  
отдельные идентификатор
  
Идентификатор eindeutige-nummer
  
Идентификатор eindeutige
  
Идентификатор personnelle
  
numéro d'identification персонала
  
idpersonnelle #
  
persönliche identifikationsnummer
  
eindeutigeid #
  
## <a name="malta"></a>Мальта

### <a name="format"></a>Формат

Семь цифр, следуют одна буква
  
### <a name="pattern"></a>Шаблон

Семь цифр, следуют одна буква:
  
-  семь цифр; 
    
- Один прописные буквы (с учетом регистра)
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_malta_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_malta_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
  
- Регулярное выражение `Regex_malta_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
          <Match idRef="Keywords_malta_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsmaltaeunationalidcard"></a>Keywords_malta_eu_national_id_card

личный цифровой код
  
Уникальный идентификационный номер
  
номер службы граждан
  
количество уникальных идентификаторов
  
uniqueidentityno #
  
kodiċi numerali personali
  
numru ta "identifikazzjoni uniku
  
numru задач servizz taċ-ċittadin
  
numru ta "identità uniku
  
## <a name="netherlands"></a>Нидерланды

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_netherlands_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из найти.
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_netherlands_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
          <Match idRef="Keywords_netherlands_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsnetherlandseunationalidcard"></a>Keywords_netherlands_eu_national_id_card

личный цифровой код
  
Уникальный идентификационный номер
  
номер службы граждан
  
количество уникальных идентификаторов
  
uniqueidentityno #
  
bsn
  
bsn #
  
Код numerieke persoonlijke
  
uniek identificatienummer
  
burgerservicenummer
  
uniek identiteitsnummer
  
## <a name="poland"></a>Польша

Для получения дополнительных сведений обратитесь к разделу «Польша национальный идентификатор (PESEL)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Португалия

Для получения дополнительных сведений обратитесь к разделу «Номер карты Португалия граждане» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="romania"></a>Румыния

### <a name="format"></a>Формат

13 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

13 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_romania_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_romania_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_romania_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
          <Match idRef="Keywords_romania_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_romania_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsromaniaeunationalidcard"></a>Keywords_romania_eu_national_id_card

личный цифровой код
  
Уникальный идентификационный номер
  
cnp
  
cnp #
  
закрепить
  
ПИН-код #
  
страховой номер
  
insurancenumber #
  
количество уникальных идентификаторов
  
uniqueidentityno #
  
числовой личные COD
  
решить identificare личные
  
COD unic identificare
  
личные unic număr
  
număr identitate
  
личные identificare număr
  
număridentitate #
  
codnumericpersonal #
  
numărpersonalunic #
  
## <a name="slovakia"></a>Словакия

### <a name="format"></a>Формат

10 цифр, содержащий один символ косой черты
  
### <a name="pattern"></a>Шаблон

10 цифр, содержащий один символ косой черты:
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_slovakia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovakia_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_slovakia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
          <Match idRef="Keywords_slovakia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovakia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsslovakiaeunationalidcard"></a>Keywords_slovakia_eu_national_id_card

Номер рождения
  
Национальный идентификационный номер
  
персональный идентификационный номер
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
Национальный номер
  
личный идентификатор
  
personalidnumber #
  
rč
  
rodné číslo
  
rodne cislo
  
## <a name="slovenia"></a>Словения

### <a name="format"></a>Формат

13 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

13 цифр в указанному шаблону:
  
-  Семь цифр, которые соответствуют Дата рождения (DDMMLLL), где «LLL» к последнему соответствует трех цифр год рождения 
    
- Две цифры, которые соответствуют области рождения
    
- Три цифры, которые соответствуют сочетание пол и серийный номер для лиц, рождения на тот же день (для м 000 499) и 500 до 999 женщина
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_slovenia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovenia_eu_national_id_card` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_slovenia_eu_national_id_card` находит контент, который соответствует шаблону. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
          <Match idRef="Keywords_slovenia_eu_national_id_card" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordssloveniaeunationalidcard"></a>Keywords_slovenia_eu_national_id_card

личный цифровой код
  
Уникальный идентификационный номер
  
Уникальный номер регистрации
  
количество уникальных идентификаторов
  
uniqueidentityno #
  
число уникальных главных граждан
  
edinstvena identifikacijska številka
  
uniqueidentityno #
  
edinstvena številka glavnega državljana
  
emšo
  
## <a name="spain"></a>Испания

### <a name="format"></a>Формат

Семь цифр, за которой следует один символ
  
### <a name="pattern"></a>Шаблон

Семь цифр, за которой следует один символ
  
- семь цифр;
    
- Одну цифру или букву (без учета регистра)
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_spain_eu_national_id_card` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_spain_eu_national_id_card"` найден. 
    
```
 
<Entity id="419f449f-6d9d-4be1-a154-b531f7a91b41" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_national_id_card" />
          <Match idRef="Keywords_spain_eu_national_id_card" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsspaineunationalidcard"></a>Keywords_spain_eu_national_id_card

не установлен
  
Национальный идентификационный номер
  
Национальный идентификатор номер
  
страховой номер
  
персональный идентификационный номер
  
Национальный идентификатор
  
личные нет
  
количество уникальных идентификаторов
  
nationalidno #
  
Уникальный идентификатор #
  
не установлен #
  
nationalid #
  
NIE #
  
NIE
  
nienúmero #
  
NIE número
  
documento nacional де identidad
  
identidad único
  
número nacional identidad
  
número не установлен
  
dninúmero #
  
identidadúnico #
  
## <a name="sweden"></a>Швеция

Для получения дополнительных сведений обратитесь к разделу «Национальный идентификатор для Швеции» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

