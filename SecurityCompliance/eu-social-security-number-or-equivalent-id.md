---
title: Номер социального страхования ЕС или эквивалентный идентификатор
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает номер социального страхования ЕС или эквивалентный тип конфиденциальной информации. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
ms.openlocfilehash: c0c808eafa52209c79f3b4e8a2113f587fd8a771
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255557"
---
# <a name="eu-social-security-number-or-equivalent-id"></a>Номер социального страхования ЕС или эквивалентный идентификатор

В этом разделе показано, как будет выглядеть политика защиты от потери данных (DLP), когда она обнаруживает тип конфиденциальной информации ЕС или эквивалентный идентификатор. Этот тип конфиденциальной информации определяет различные шаблоны, ключевые слова и другие доказательства для каждой страны.
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Format

10 цифр в указанном формате
  
### <a name="pattern"></a>Шаблон

10 цифр:
  
-  Три цифры, соответствующие серийному номеру. 
    
- Одна контрольная цифра
    
- Шесть цифр, соответствующих дате рождения (ДДММГГ —)
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_austria_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_austria_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsaustriaeussnorequivalent"></a>Кэйвордс_аустриа_еу_ссн_ор_екуивалент

социальное страхование нет
  
social security number
  
social security code
  
страховой номер
  
Австрийский SSN
  
SSN
  
SSN
  
код страхования
  
код страхования
  
соЦиалсекуритино #
  
созиалверсичерунгснуммер
  
созиале сичерхеит Кеин
  
версичерунгснуммер
  
## <a name="belgium"></a>Бельгия

### <a name="format"></a>Format

11 цифр без пробелов и разделителей
  
### <a name="pattern"></a>Шаблон

11 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_belgium_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_belgium_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsbelgiumeussnorequivalent"></a>Кэйвордс_белгиум_еу_ссн_ор_екуивалент

Бельгийский национальный номер
  
номер страны
  
social security number
  
натионалнумбер #
  
SSN
  
SSN
  
натионалнумбер
  
БНН #
  
БНН
  
личный идентификационный номер
  
персоналиднумбер #
  
Национальный нумéро
  
numéro de sécurité
  
нумéро д'ассурé
  
Идентификация National
  
идентифиантнатионал #
  
нумéронатионал #
  
## <a name="croatia"></a>Хорватия

### <a name="format"></a>Format

11 цифр без пробелов и разделителей
  
### <a name="pattern"></a>Шаблон

 11 цифр: 
  
-  Десять цифр 
    
- Одна контрольная цифра
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_croatia_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_croatia_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordscroatiaeussnorequivalent"></a>Кэйвордс_кроатиа_еу_ссн_ор_екуивалент

персональный идентификационный номер
  
основной номер в соотношении
  
national identification number
  
social security number
  
натионалнумбер #
  
SSN
  
SSN
  
натионалнумбер
  
БНН #
  
БНН
  
личный идентификационный номер
  
персоналиднумбер #
  
OIB
  
особни идентификаЦижски Брож
  
## <a name="czech-republic"></a>Чешская Республика

### <a name="format"></a>Format

Десять цифр и обратная косая черта в указанном шаблоне
  
### <a name="pattern"></a>Шаблон

Десять цифр и обратная косая черта:
  
- Шесть цифр, соответствующих дате рождения (ГГММДД): 
    
- Обратная косая черта
    
- Три цифры, которые соответствуют серийному номеру, которые отделяют пользователей на одну и ту же дату.
    
- Одна контрольная цифра
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_czech_republic_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_czech_republic_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsczechrepubliceussnorequivalent"></a>Кэйвордс_кзеч_републик_еу_ссн_ор_екуивалент

номер рождения
  
national identification number
  
персональный идентификационный номер
  
social security number
  
натионалнумбер #
  
SSN
  
SSN
  
номер страны
  
личный идентификационный номер
  
персоналиднумбер #
  
рč
  
роднé číсло
  
родне Цисло
  
## <a name="denmark"></a>Дания

### <a name="format"></a>Format

Десять цифр и дефис в заданном шаблоне
  
### <a name="pattern"></a>Шаблон

Десять цифр и дефис:
  
- Шесть цифр, соответствующих дате рождения (ДДММГГ —) 
    
- дефис;
    
- Четыре цифры, которые соответствуют порядковому номеру
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_denmark_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_denmark_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsdenmarkeussnorequivalent"></a>Кэйвордс_денмарк_еу_ссн_ор_екуивалент

персональный идентификационный номер
  
national identification number
  
social security number
  
натионалнумбер #
  
SSN
  
SSN
  
номер страны
  
личный идентификационный номер
  
персоналиднумбер #
  
CPR — нуммер
  
персоннуммер
  
## <a name="finland"></a>Финляндия

### <a name="format"></a>Format

11 символов в указанном формате.
  
### <a name="pattern"></a>Шаблон

Сочетание из 11 символов в указанном формате:
  
-  Шесть цифр 
    
- Один из следующих экземпляров:
    
  - Символ "плюс"
    
  - Символ "минус"
    
  - Буква "A" (без учета регистра)
    
- Три цифры
    
- Одна буква или одна цифра
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_finland_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_finland_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsfinlandeussnorequivalent"></a>Кэйвордс_финланд_еу_ссн_ор_екуивалент

identification number
  
личный идентификатор
  
идентификационный номер
  
Финский национальный идентификационный номер
  
персоналиднумбер #
  
national identification number
  
идентификационный номер
  
код страны
  
Национальный идентификационный номер
  
ID No
  
туннистенумеро
  
хенкилöтуннус
  
иксилöллинен хенкилöкохтаинен туннистенумеро
  
аинутлаатуинен хенкилöкохтаинен туннус
  
идентититти нумеро
  
Суомен кансаллинен хенкилöтуннус
  
хенкилöтуннуснумеро #
  
кансаллисен туннистенумеро
  
туннуснумеро
  
кансаллинен туннус нумеро
  
Хету
  
## <a name="france"></a>Франция

Дополнительные сведения см. в разделе "номер социального страхования для Франции (INSEE)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Германия

Дополнительные сведения можно найти в разделе "номер идентификационной карточки для Германии" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Греция

Дополнительные сведения можно найти в разделе "Греция National ID Card", [который будет искать тип конфиденциальной информации](what-the-sensitive-information-types-look-for.md).
  
## <a name="hungary"></a>Венгрия

### <a name="format"></a>Format

Девять цифр без пробелов и разделителей
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_hungary_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_hungary_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordshungaryeussnorequivalent"></a>Кэйвордс_хунгари_еу_ссн_ор_екуивалент

Венгерский номер социального страхования
  
social security number
  
соЦиалсекуритинумбер #
  
хссн #
  
соЦиалсекуритинно
  
хссн
  
Таж
  
Таж #
  
SSN
  
SSN
  
социальное страхование нет
  
áфа
  
кöзöссéги адóсзáм
  
áлталáнос форгалми адó сзáм
  
хоззáадоттéртéк адó
  
áфа сзáм
  
магяр áфа сзáм
  
## <a name="portugal"></a>Португалия

Дополнительные сведения можно найти в разделе "номер карты для Португалия" в разделе [сведения о типах конфиденциальной информации для поиска](what-the-sensitive-information-types-look-for.md).
  
## <a name="spain"></a>Испания

Дополнительные сведения см. в разделе "номер социального страхования для Испании (SSN)" [, в котором ищутся типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md).
  
## <a name="sweden"></a>Швеция

### <a name="format"></a>Format

12 цифр без пробелов и разделителей
  
### <a name="pattern"></a>Шаблон

12 цифр:
  
-  Восемь цифр, которые соответствуют дате рождения (ГГГГММДД) 
    
- Три цифры, которые соответствуют серийному номеру, где: 
    
  - Последняя цифра в числовом номере указывает на пол, назначая нечетное число для пола и четное число для розетки.
    
  - До 1990, назначение серийного номера соответствует району, в котором был выпущен номер, или (если он родился до 1947), где он был удален, в соответствии с налоговыми записями 1 января 1947, с помощью специального кода (как правило, 9 в качестве седьмой цифры). иммигрантс 
    
- Одна контрольная цифра
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
- Найдено ключевое `Keywords_sweden_eu_ssn_or_equivalent` слово FROM. 
    
Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_sweden_eu_ssn_or_equivalent` находит содержимое, которое соответствует шаблону. 
    
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsswedeneussnorequivalent"></a>Кэйвордс_сведен_еу_ссн_ор_екуивалент

личный идентификационный номер
  
identification number
  
личный идентификатор
  
Идентификатор
  
Идентификация нет
  
персональный идентификационный номер
  
Идентификатор персоннуммер
  
Идентификатор персонлигт — нуммер
  
Идентификатор уникт — нуммер
  
персоннуммер
  
идентификатионснумрет
  
персоннуммер #
  
идентификатионснумрет #
  
## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

