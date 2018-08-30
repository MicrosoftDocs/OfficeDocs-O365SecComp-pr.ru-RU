---
title: Страховой номер для ЕС или иметь эквивалентные права идентификатор
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 1fabd341-e594-4bfe-961c-62aa82893f60
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении страховой номер для ЕС или эквивалентный код тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 6f1027dcfb648ed937b8180d74d4bc6348dab650
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534728"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>Страховой номер для ЕС или иметь эквивалентные права идентификатор

В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении ЕС страховой номер (SSN) или эквивалентный код тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Формат

10 цифр в указанном формате
  
### <a name="pattern"></a>Шаблон

10 цифр:
  
-  Три цифры, которые соответствуют серийный номер 
    
- Один контрольный разряд
    
- Шести цифр, которые соответствуют Дата рождения (DDMMYY)
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_austria_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_austria_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_austria_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_austria_eu_ssn_or_equivalent" />
        </Pattern>
<Pattern confidenceLevel="75">
            <IdMatch idRef="Func_austria_eu_ssn_or_equivalent" />
          </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsaustriaeussnorequivalent"></a>Keywords_austria_eu_ssn_or_equivalent

социального страхования нет
  
social security number

  

social security code
  
страховой номер
  
Австрия ssn
  
SSN #
  
SSN
  
страховой кода
  
страховой код #
  
socialsecurityno #
  
sozialversicherungsnummer
  
soziale sicherheit kein
  
versicherungsnummer
  
## <a name="belgium"></a>Бельгия

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

11 разрядов
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_belgium_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_belgium_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_belgium_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_belgium_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_belgium_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsbelgiumeussnorequivalent"></a>Keywords_belgium_eu_ssn_or_equivalent

Бельгия национальный номер
  
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
  
Национальный numéro
  
numéro de sécurité

  
numéro d'assuré
  
Национальный identifiant
  
identifiantnational #
  
numéronational #
  
## <a name="croatia"></a>Хорватия

### <a name="format"></a>Формат

11 знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 11 цифр: 
  
-  10 цифр 
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_croatia_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_croatia_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_croatia_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_croatia_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordscroatiaeussnorequivalent"></a>Keywords_croatia_eu_ssn_or_equivalent

персональный идентификационный номер
  
Число главных граждан
  
Национальный идентификационный номер
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
nationalnumber
  
bnn #
  
bnn
  
личный идентификатор
  
personalidnumber #
  
oib
  
osobni identifikacijski broj
  
## <a name="czech-republic"></a>Чешская Республика

### <a name="format"></a>Формат

10 цифр и обратная косая черта в указанному шаблону
  
### <a name="pattern"></a>Шаблон

10 цифр и обратную косую черту:
  
- Шесть цифры, которые соответствуют Дата рождения (ГГММДД): 
    
- Обратная косая черта
    
- Три цифры, которые соответствуют серийный номер, отделяющий лиц на тот же день рождения
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_czech_republic_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_czech_republic_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_czech_republic_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_czech_republic_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_czech_republic_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Keywords_czech_republic_eu_ssn_or_equivalent

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
  
## <a name="denmark"></a>Дания

### <a name="format"></a>Формат

10 цифр и дефис в указанному шаблону
  
### <a name="pattern"></a>Шаблон

10 цифр и дефис:
  
- Шести цифр, которые соответствуют Дата рождения (DDMMYY) 
    
- дефис;
    
- Четыре цифры, которые соответствуют порядковый номер
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_denmark_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_denmark_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_denmark_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_denmark_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsdenmarkeussnorequivalent"></a>Keywords_denmark_eu_ssn_or_equivalent

персональный идентификационный номер
  
Национальный идентификационный номер
  
social security number

  
nationalnumber #
  
SSN #
  
SSN
  
Национальный номер
  
личный идентификатор
  
personalidnumber #
  
CPR nummer
  
personnummer
  
## <a name="finland"></a>Финляндия

### <a name="format"></a>Формат

Комбинация 11 символов в указанном формате
  
### <a name="pattern"></a>Шаблон

Комбинация 11 символов в указанном формате:
  
-  Шесть цифр 
    
- Один экземпляр одно из следующих действий:
    
  - А также символ
    
  - Знак минус
    
  - Буква «A» (без учета регистра)
    
- Три цифры
    
- Одна буква или одной цифры
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_finland_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_finland_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_finland_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_finland_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsfinlandeussnorequivalent"></a>Keywords_finland_eu_ssn_or_equivalent

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
  
hetu
  
## <a name="france"></a>Франция

Для получения дополнительных сведений обратитесь к разделу «Франция страховой номер (INSEE)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Германия

Для получения дополнительных сведений обратитесь к разделу «Номер идентификационной карты для Германии» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Греция

Для получения дополнительных сведений обратитесь к разделу «Греция национальной ИДЕНТИФИКАЦИОННОЙ карты» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Венгрия

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_hungary_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_hungary_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordshungaryeussnorequivalent"></a>Keywords_hungary_eu_ssn_or_equivalent

Венгерский страховой номер
  
social security number

  
socialsecuritynumber #
  
hssn #
  
socialsecuritynno
  
hssn
  
сэкономленные
  
сэкономленные #
  
SSN
  
SSN #
  
социального страхования нет
  
áfa
  
közösségi adószám
  
általános forgalmi adó szám
  
hozzáadottérték adó
  
áfa szám
  
szám magyar áfa
  
## <a name="portugal"></a>Португалия

Для получения дополнительных сведений обратитесь к разделу «Номер карты Португалия граждане» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Испания

Для получения дополнительных сведений обратитесь к разделу «Испания страховой номер (SSN)» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Швеция

### <a name="format"></a>Формат

12 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

12 цифр:
  
-  Восемь символов, которые соответствуют Дата рождения (ГГГГММДД) 
    
- Три цифры, которые соответствуют серийный номер где: 
    
  - Последний знак в серийный номер указывает пол, назначение нечетным количеством для м и четным женщина
    
  - До 1990, назначения серийный номер откорреспондирован для Район, где рождения носителя номер или (если рождения перед 1947) которых он/она живущих, в соответствии с записями налогах на 1 января 1947, с помощью специального кода (обычно 9 7 цифр) для immigrants 
    
- Один контрольный разряд
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_sweden_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_sweden_eu_ssn_or_equivalent` найден. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_sweden_eu_ssn_or_equivalent` находит контент, который соответствует шаблону. 
    
```
 <!-- EU SSN or Equivalent Number -->
<Entity id="d24e32a4-c0bb-4ba8-899d-6303b95742d9" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
          <Match idRef="Keywords_sweden_eu_ssn_or_equivalent" />
        </Pattern> 
       <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_ssn_or_equivalent" />
        </Pattern>      
</Entity>
```

### <a name="keywords"></a>Keywords

#### <a name="keywordsswedeneussnorequivalent"></a>Keywords_sweden_eu_ssn_or_equivalent

личный идентификатор
  
identification number

  
личный идентификатор не
  
удостоверение не
  
Идентификация нет
  
персональный идентификационный нет
  
Идентификатор personnummer
  
Идентификатор personligt-nummer
  
Идентификатор unikt-nummer
  
personnummer
  
identifikationsnumret
  
personnummer #
  
identifikationsnumret #
  
## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

