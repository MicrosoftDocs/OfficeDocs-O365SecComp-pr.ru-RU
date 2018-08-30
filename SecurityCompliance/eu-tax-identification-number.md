---
title: Идентификационный номер налога ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: f04919c8-2356-4de2-bb2a-b9f67f339726
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении идентификационный номер налога ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 5192496b393d15fd6d063e09c9bfe1cb3dd7e2dd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534821"
---
# <a name="eu-tax-identification-number"></a>Идентификационный номер налога ЕС

В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных ЕС Tax код (TIN). Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Формат

Девяти цифр с необязательным дефис и косой черты
  
### <a name="pattern"></a>Шаблон

Девять цифры с необязательным дефис и косой черты:
  
-  Две цифры 
    
- Дефис (необязательно)
    
- Три цифры
    
- Косая черта (необязательно)
    
- Четыре цифры
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_austria_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_austria_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_austria_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeutaxfilenumber"></a>Keywords_austria_eu_tax_file_number

номер налога
  
номер
  
номер налогоплательщика
  
tax id

  
ST.nr.
  
steuernummer
  
## <a name="belgium"></a>Бельгия

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 цифр:
  
- Две цифры
    
- «0» или «1»
    
- Одна цифра
    
- «0» или «1» или «2» или «3» 
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_belgium_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_belgium_eu_tax_file_number` найден. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbelgiumeutaxfilenumber"></a>Keywords_belgium_eu_tax_file_number

номер налога
  
Национальный номер регистрации
  
номер налогоплательщика
  
tax id

  
NIF
  
NIF #
  
Национальный registre де numéro
  
numéro d'identification fiscale
  
## <a name="bulgaria"></a>Болгария

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

10 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_bulgaria_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_bulgaria_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_bulgaria_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbulgariaeutaxfilenumber"></a>Keywords_bulgaria_eu_tax_file_number

bucn
  
Универсальный правах номер
  
bucn #
  
uniformcivilnumber #
  
универсальный идентификатор правах
  
Унифицированный правах no
  
egn
  
болгарский универсальный правах номер
  
uniformcivilno #
  
egn #
  
УНИФОРМ ГРАЖДАНСКИ НОМЕР
  
Идентификатор униформ
  
Идентификатор граждански униформ
  
УНИФОРМ ГРАЖДАНСКИ НЕ
  
## <a name="croatia"></a>Хорватия

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 цифр:
  
- 10 цифр, случайным образом выбранные
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_croatia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_croatia_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_croatia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscroatiaeutaxfilenumber"></a>Keywords_croatia_eu_tax_file_number

номер налога
  
налогах
  
tax id

  
Идентификатор объекта
  
Идентификатор объекта #
  
porezni broj
  
## <a name="cyprus"></a>Кипр

### <a name="format"></a>Формат

Восемь цифр и одной буквы в указанному шаблону
  
### <a name="pattern"></a>Шаблон

Восемь цифр и одной буквы:
  
-  «0» 
    
- семь цифр;
    
- Одна буква (без учета регистра)
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_cyprus_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_cyprus_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_cyprus_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscypruseutaxfilenumber"></a>Keywords_cyprus_eu_tax_file_number

номер налога
  
налогах
  
tax id

  
Код налога
  
крестики
  
крестики #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
ΦΟΡΟΛΟΓΙΚΉ ΤΑΥΤΌΤΗΤΑ
  
ΚΩΔΙΚΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="czech-republic"></a>Чешская Республика

### <a name="format"></a>Формат

9 или 10 цифр с необязательным обратная косая черта
  
### <a name="pattern"></a>Шаблон

9 или 10 цифр с необязательным backslashl:
  
- Шесть цифр 
    
- Обратная косая черта (необязательно)
    
- Три или четыре цифры
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_czech_republic_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_czech_republic_eu_tax_file_number` найден. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsczechrepubliceutaxfilenumber"></a>Keywords_czech_republic_eu_tax_file_number

номер налога
  
налогах
  
tax id

  
личный номер
  
daňové číslo
  
osobní číslo
  
## <a name="denmark"></a>Дания

### <a name="format"></a>Формат

10 цифр, содержащий дефис
  
### <a name="pattern"></a>Шаблон

10 цифр, содержащий hyphenl:
  
-  Шести цифр, которые соответствуют Дата рождения (DDMMYY) 
    
- дефис;
    
- Четыре цифры, которые соответствуют порядковый номер, где первая цифра соответствует века рождения и последней цифры соответствует Пол сотрудника (нечетной м и даже женщина)
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_denmark_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_denmark_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_denmark_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsdenmarkeutaxfilenumber"></a>Keywords_denmark_eu_tax_file_number

номер налога
  
налогах
  
tax id

  
Номер CPR
  
CPR #
  
skat nummer
  
Идентификатор skat
  
## <a name="estonia"></a>Эстония

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 цифр:
  
-  Одна цифра, соответствующий пол и века рождения где нечетным количеством указывает м, а четного числа женщина следующим образом: 1, 2 19 века; 3, 4 20 века; и 5, 6 для 21 веке 
    
- Шести цифр, которые соответствуют Дата рождения (ГГММДД)
    
- Три цифры, которые соответствуют серийный номер, отделяя лиц на тот же день рождения
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_estonia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_estonia_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_estonia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsestoniaeutaxfilenumber"></a>Keywords_estonia_eu_tax_file_number

номер налога
  
налогах
  
tax id

  
личный код
  
maksunumber
  
Идентификатор maksu
  
isikukood
  
## <a name="finland"></a>Финляндия

### <a name="format"></a>Формат

Комбинация 11 символов цифры, буквы, и плюс и минус
  
### <a name="pattern"></a>Шаблон

Комбинация 11 символов цифры, буквы, и плюс и минус:
  
- Шесть цифр
    
- Одно из следующих значений: знак плюс, минус или букву «» (не регистр), где значок "плюс" означает рождения между 1800-1899 вход "минус" означает, что рождения между 1900-1999 и «A» означает, что рождения 2000 и после
    
- Три цифры
    
- Одна буква или один номер
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_finland_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_finland_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_finland_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfinlandeutaxfilenumber"></a>Keywords_finland_eu_tax_file_number

identification number

  
личный код
  
Количество идентификаторов
  
Национальный идентификатор для Финляндии номер
  
personalidnumber #
  
Национальный идентификационный номер
  
Табельный номер
  
Национальный идентификатор для не.
  
Идентификационный номер
  
Идентификатор не
  
tunnistenumero
  
henkilötunnus
  
yksilöllinen henkilökohtainen tunnistenumero
  
ainutlaatuinen henkilökohtainen tunnus
  
identiteetti numero
  
suomen kansallinen henkilötunnus
  
henkilötunnusnumero #
  
kansallisen tunnistenumero
  
tunnusnumero
  
kansallinen tunnus numero
  
## <a name="france"></a>Франция

### <a name="format"></a>Формат

13 цифр для отдельных пользователей и девяти цифр для сущностей
  
### <a name="pattern"></a>Шаблон

13 цифр для отдельных пользователей:
  
- Одной цифры, которые должны быть 0, 1, 2 или 3
    
- 12 цифр.
    
Девяти цифр для сущностей
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_france_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_france_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_france_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfranceeutaxfilenumber"></a>Keywords_france_eu_tax_file_number

Идентификационный номер налога
  
номер налога
  
tax id

  
numéro d'identification fiscale
  
## <a name="germany"></a>Германия

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 разрядов:
  
-  10 цифр 
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_germany_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_germany_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_germany_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsgermanyeutaxfilenumber"></a>Keywords_germany_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
код налогоплательщика #
  
Идентификационный номер налога
  
не налогах идентификации.
  
steuernummer
  
Идентификатор steuer
  
steueridentifikationsnummer
  
## <a name="greece"></a>Греция

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_greece_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_greece_eu_tax_file_number` найден. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsgreeceeutaxfilenumber"></a>Keywords_greece_eu_tax_file_number

afm
  
tin

  
не налогах идентификатор.
  
не налогах идентификатор
  
Идентификационный номер налога
  
Номер реестра налоговые
  
не налогах реестра.
  
afm #
  
TIN #
  
taxidno #
  
taxregistryno #
  
ΑΡΙΘΜΌΣ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
aφμ
  
aφμ αριθμός
  
ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ ΝΟ.
  
ΤΟΝ ΑΡΙΘΜΌ ΦΟΡΟΛΟΓΙΚΟΎ ΜΗΤΡΏΟΥ
  
## <a name="hungary"></a>Венгрия

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Десять цифры:
  
-  Одной цифры, которые должны быть «8» 
    
- Пяти цифр, которые соответствуют число дней между датами 01/01/1867 и Дата рождения отдельных
    
- Три цифры, которые соответствуют номер, который создается случайно для различения отдельных пользователей в тот же день рождения
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_hungary_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeutaxfilenumber"></a>Keywords_hungary_eu_tax_file_number

Венгерский tax идентификационный номер
  
Венгерский tin
  
номер идентификатора налогах
  
номер НДС
  
не налогах центра сертификации
  
Номер удостоверения tax идентификатора налогах
  
taxidnumber #
  
TIN #
  
hungatiantin #
  
не налогах идентификации
  
taxidno #
  
adóazonosító szám
  
adószám
  
adóhatóság szám
  
## <a name="ireland"></a>Ireland

### <a name="format"></a>Формат

Семь цифр, а затем буквы без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Семь цифр, а затем буквы:
  
-  семь цифр; 
    
- Одна буква (без учета регистра)
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_ireland_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_ireland_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_ireland_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsirelandeutaxfilenumber"></a>Keywords_ireland_eu_tax_file_number

общего пользования нет
  
личные общего пользования нет
  
PPS нет
  
личные службы нет
  
PPS-службы нет
  
ppsno #
  
Ирландский pps нет
  
publicserviceno #
  
число личных общего пользования
  
uimhir phearsanta seirbhíse poiblí
  
PPS uimh
  
uimhir aitheantais phearsanta
  
## <a name="italy"></a>Италия

### <a name="format"></a>Формат

16 только буквы и цифры в указанному шаблону
  
### <a name="pattern"></a>Шаблон

16 только буквы и цифры:
  
-  Три буквы, которые соответствуют первым трем согласных в поле имя семейства 
    
- Три буквы, которые соответствуют первый, третий и четвертый согласных в поле имя
    
- Две цифры, которые соответствуют к последнему цифры года рождения
    
- Одна цифра, соответствующий месяц рождения — буквы используются в алфавитном порядке, но используются только буквы A E, H, L, M, P, R, чтобы T (таким образом, января-A и октября является R)
    
- Две цифры, которые соответствуют день месяца рождения, где 40 добавляется в день рождения для женщин для различения мужчины
    
- Четыре цифры, которые соответствуют код города, относящиеся к государственный орган, где рождения лица — коды всей страны, используемые для иностранных стран
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_italy_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_italy_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_italy_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsitalyeutaxfilenumber"></a>Keywords_italy_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
код налогоплательщика #
  
Финансовый код
  
codice fiscale
  
## <a name="latvia"></a>Латвия

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 разрядов в указанному шаблону
  
-  Шести цифр, которые соответствуют Дата рождения (DDMMYY) 
    
- Одна цифра, соответствующий века рождения, которой соответствует 19 век «0», «1» соответствует 20 века, а «2» соответствует 21 веке
    
- Четыре цифры
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_latvia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_latvia_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_latvia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslatviaeutaxfilenumber"></a>Keywords_latvia_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
код налогоплательщика #
  
Идентификационный номер налога
  
не налогах идентификации.
  
nodokļa numurs
  
nodokļu identifikācijas numurs
  
nodokļu identifikācija numurs
  
## <a name="lithuania"></a>Литва

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 разрядов
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_lithuania_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_lithuania_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_lithuania_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordslithuaniaeutaxfilenumber"></a>Keywords_lithuania_eu_tax_file_number

номер налога
  
налогах нет.
  
налогах нет #
  
taxnumber #
  
taxnumber
  
tax id

  
код налогоплательщика #
  
Идентификационный номер налога
  
не налогах идентификации.
  
Идентификатор mokesčių
  
mokesčių numeris
  
mokesčių identifikavimas numeris
  
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Формат

13 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

13 цифр:
  
-  11 разрядов 
    
- две проверочные цифры.
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_luxemburg_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_luxemburg_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_luxemburg_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsluxemburgeutaxfilenumber"></a>Keywords_luxemburg_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
код налогоплательщика #
  
Идентификационный номер налога
  
не налогах идентификации.
  
steuernummer
  
Идентификатор steuer
  
steueridentifikationsnummer
  
## <a name="malta"></a>Мальта

### <a name="format"></a>Формат

Для Maltese представителями: 7 цифр и одной буквы в указанному шаблону
  
Не Мальтийский представителями и Maltese сущностей: 9 цифр
  
### <a name="pattern"></a>Шаблон

Maltese представителями: 7 цифр и одной буквы
  
-  семь цифр; 
    
- Одна буква (без учета регистра)
    
Не Мальтийский представителями и Maltese сущностей: 9 цифр
  
-  Девять цифр. 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_malta_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_malta_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
  
- Функция `Func_malta_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsmaltaeutaxfilenumber"></a>Keywords_malta_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
tax id

  
код налогоплательщика #
  
Идентификационный номер налога
  
не налогах идентификации.
  
numru tat-taxxa
  
Идентификатор tat-taxxa
  
numru ta "identifikazzjoni tat-taxxa
  
## <a name="netherlands"></a>Нидерланды

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр. 
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_netherlands_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_netherlands_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_netherlands_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsnetherlandseutaxfilenumber"></a>Keywords_netherlands_eu_tax_file_number

Нидерландские tax идентификационный номер
  
Идентификация tax Нидерланды
  
Идентификационный номер абонента Нидерландские налога
  
Идентификация tax Нидерландские абонента
  
Идентификационный номер налога
  
Голландский ИД.
  
Голландский tax идентификационный номер
  
tax id

  
Идентификатор Tax #
  
номер налога
  
налогах нет #
  
Tax #
  
tin

  
TIN #
  
Нидерландские tin
  
Нидерландские 's tin
  
Nederlands belasting identificatienummer
  
identificatienummer van belasting
  
identificatienummer belasting
  
Nederlands belasting identificatie
  
Идентификатор nummer Nederlands belasting
  
Nederlands belastingnummer
  
btw nummer
  
nederlandse belasting identificatie
  
## <a name="poland"></a>Польша

### <a name="format"></a>Формат

Одиннадцать цифры без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Одиннадцать цифр
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_poland_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_poland_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_poland_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordspolandeutaxfilenumber"></a>Keywords_poland_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
ИНН
  
ИНН #
  
tax id

  
Идентификатор Tax #
  
Идентификатор ИНН
  
Идентификатор уще #
  
Идентификационный номер налога
  
не налогах идентификации.
  
номер НДС
  
НДС нет.
  
vatno #
  
Идентификатор НДС
  
Идентификатор НДС #
  
Номер identyfikacji podatkowej
  
podatkowej identyfikacji polski номер
  
numeridentyfikacjipodatkowej #
  
## <a name="portugal"></a>Португалия

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_portugal_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_portugal_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_portugal_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsportugaleutaxfilenumber"></a>Keywords_portugal_eu_tax_file_number

номер налога
  
налогах нет.
  
taxno #
  
taxnumber #
  
taxnumber
  
NIF
  
NIF #
  
финансовые numero
  
финансовые identificação де número
  
## <a name="romania"></a>Румыния

### <a name="format"></a>Формат

13 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

13 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_romania_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_romania_eu_tax_file_number` найден. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsromaniaeutaxfilenumber"></a>Keywords_romania_eu_tax_file_number

tax id

  
номер идентификатора налогах
  
не налогах файла
  


tax file number
  
налогах нет
  
номер налога
  
код налогоплательщика #
  
taxno #
  
Идентификатор ul taxei
  
fiscală identificare де numărul
  
## <a name="slovakia"></a>Словакия

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

10 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovakia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovakia_eu_tax_file_number` найден. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsslovakiaeutaxfilenumber"></a>Keywords_slovakia_eu_tax_file_number

tax id

  
номер идентификатора налогах
  
Идентификатор кода TIN
  
Нет кода TIN
  
Идентификатор кода tin словацкий
  
tin

  
не налогах файла
  


tax file number
  
налогах нет
  
номер налога
  
код налогоплательщика #
  
taxno #
  
daňové identifikačné číslo
  
daňové číslo
  
daňové číslo súboru
  
## <a name="slovenia"></a>Словения

### <a name="format"></a>Формат

Восьми знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь цифр
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_slovenia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovenia_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_slovenia_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordssloveniaeutaxfilenumber"></a>Keywords_slovenia_eu_tax_file_number

tax id

  
номер идентификатора налогах
  
Идентификатор кода TIN
  
Нет кода TIN
  
Словенский кода tin идентификатор
  
tin

  
не налогах файла
  


tax file number
  
налогах нет
  
номер налога
  
код налогоплательщика #
  
taxno #
  
identifikacijska številka davka
  
davčna številka
  
Številka davčne datoteke
  
## <a name="spain"></a>Испания

### <a name="format"></a>Формат

Семь или восемь цифр и один или два буквы указанному шаблону
  
### <a name="pattern"></a>Шаблон

Испанский физических лиц с Испания национальный личность:
  
-  восемь цифр. 
    
- Один прописные буквы (с учетом регистра) 
    
Без проживания Spaniards без Испания национальный личность
  
- Один прописная буква «L» (с учетом регистра)
    
- семь цифр;
    
- Один прописные буквы (с учетом регистра) 
    
Встроенные Spaniards в разделе срок хранения в 14 лет без Испания национальный идентификатор карточки:
  
- Один прописные буквы «K» (с учетом регистра)
    
-  семь цифр; 
    
- Один прописные буквы (с учетом регистра)
    
Foreigners с Foreigner идентификационный номер
  
- То есть одно прописные буквы «X», «Y» или «Z» (с учетом регистра) 
    
- семь цифр;
    
- Один прописные буквы (с учетом регистра) 
    
Foreigners без Foreigner идентификационный номер
  
- Один прописная буква, который является «M» (с учетом регистра) 
    
- семь цифр;
    
- Один прописные буквы (с учетом регистра) 
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_spain_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_spain_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_spain_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsspaineutaxfilenumber"></a>Keywords_spain_eu_tax_file_number

tax id

  
номер идентификатора налогах
  
Идентификатор CIF
  
CIF нет
  
Идентификатор испанского cif
  
CIF
  
не налогах файла
  
Номер испанского cif
  


tax file number
  
испанский cif нет
  
налогах нет
  
номер налога
  
код налогоплательщика #
  
taxno #
  
cifid #
  
spanishcifid #
  
spanishcifno #
  
contribuyente де número
  
corporativo impuesto де número
  
финансовые identificación де número
  
CIF número
  
cifnúmero #
  
## <a name="sweden"></a>Швеция

### <a name="format"></a>Формат

10 цифр и символ в указанному шаблону
  
### <a name="pattern"></a>Шаблон

10 цифр и символ:
  
-  Шести цифр, которые соответствуют Дата рождения (ГГММДД) 
    
- "Плюс", "минус" или обратная косая черта
    
- Три цифры, которые делают идентификационный номер уникальный where: 
    
  - Для номеров выдается, прежде чем 1990 цифры седьмой и восьмому идентификации район рождения или foreign-born людей
    
  - Цифра в девятого положение указывает пол, либо НЕЧЁТ для м или даже женщина
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_sweden_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_sweden_eu_tax_file_number` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_sweden_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsswedeneutaxfilenumber"></a>Keywords_sweden_eu_tax_file_number

tax id

  
не налогах идентификатор.
  
номер идентификатора налогах
  
tax identification

  
Идентификация Tax #
  
налогах нет.
  
Tax #
  
код налогоплательщика #
  
файл налогах
  
не налогах файла.
  
личный идентификатор
  
Идентификатор nummer skatt
  
skatt identifikation
  
personnummer
  
## <a name="uk"></a>(ВЕЛИКОБРИТАНИЯ)

### <a name="format"></a>Формат

Ссылка уникальный налогоплательщика (UTR): 10 цифр без пробелов и разделители
  
Номер национальной страховых (НИНО): Для получения дополнительных сведений, обратитесь к разделу «Великобритания страховых национальный номер (НИНО)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
### <a name="pattern"></a>Шаблон

Уникальной ссылки налогоплательщика (UTR): 10 цифр
  
Номер национальной страховых (НИНО): Для получения дополнительных сведений, обратитесь к разделу «Великобритания страховых национальный номер (НИНО)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_uk_eu_tax_file_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_uk_eu_tax_file_number` найден. 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsukeutaxfilenumber"></a>Keywords_uk_eu_tax_file_number

tax id

  
не налогах идентификатор.
  
номер идентификатора налогах
  
tax identification

  
Идентификация Tax #
  
налогах нет.
  
Tax #
  
код налогоплательщика #
  
файл налогах
  
не налогах файла.
  
## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

