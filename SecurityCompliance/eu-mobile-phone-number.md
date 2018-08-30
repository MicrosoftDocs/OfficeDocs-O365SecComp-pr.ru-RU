---
title: Номер мобильного телефона ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 555e7675-2ae8-42d1-9b8e-2c8f8cd21337
description: Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются тип конфиденциальных данных ЕС номер мобильного телефона.
ms.openlocfilehash: d0818759dae8ed86cc9aef6f7fad48cbd2acf24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534752"
---
# <a name="eu-mobile-phone-number"></a>Номер мобильного телефона ЕС

Защита от потери данных (DLP) в Office 365 безопасность &amp; центре соответствия требованиям включает множество типов конфиденциальной информации, вы можете использовать в политиках защиты от потери данных. В этом разделе описываются тип конфиденциальных данных ЕС номер мобильного телефона. 
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Формат

Цифры без стандартных длины
  
### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_austria_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_austria_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_austria_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_mobile_number"/>
          <Match idRef="Keywords_austria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_austria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="belgium"></a>Бельгия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_belgium_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_belgium_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_belgium_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_mobile_number"/>
          <Match idRef="Keywords_belgium_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_belgium_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="bulgaria"></a>Болгария

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_bulgaria_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_bulgaria_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_bulgaria_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_mobile_number"/>
          <Match idRef="Keywords_bulgaria_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_bulgaria_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="croatia"></a>Хорватия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_croatia_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_croatia_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_croatia_eu_mobile_number` найден. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_mobile_number"/>
          <Match idRef="Keywords_croatia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_croatia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="cyprus"></a>Кипр

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_cyprus_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_cyprus_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_cyprus_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_mobile_number"/>
          <Match idRef="Keywords_cyprus_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_cyprus_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="czech-republic"></a>Чешская Республика

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_czech_republic_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_czech_republic_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_czech_republic_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_mobile_number"/>
          <Match idRef="Keywords_czech_republic_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_czech_republic_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="denmark"></a>Дания

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_denmark_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_denmark_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_denmark_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_mobile_number"/>
          <Match idRef="Keywords_denmark_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_denmark_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="estonia"></a>Эстония

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_estonia_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_estonia_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_estonia_eu_mobile_number` найден. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_mobile_number"/>
          <Match idRef="Keywords_estonia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_estonia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="finland"></a>Финляндия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_finland_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_finland_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_finland_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_mobile_number"/>
          <Match idRef="Keywords_finland_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_finland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="france"></a>Франция

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_france_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_france_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_france_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_mobile_number"/>
          <Match idRef="Keywords_france_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_france_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="germany"></a>Германия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_germany_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_germany_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_germany_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_mobile_number"/>
          <Match idRef="Keywords_germany_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_germany_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="greece"></a>Греция

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_greece_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_greece_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_greece_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_mobile_number"/>
          <Match idRef="Keywords_greece_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_greece_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="hungary"></a>Венгрия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_hungary_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_hungary_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_hungary_eu_mobile_number` найден. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_mobile_number"/>
          <Match idRef="Keywords_hungary_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_hungary_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="ireland"></a>Ireland

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_ireland_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_ireland_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_ireland_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_mobile_number"/>
          <Match idRef="Keywords_ireland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_ireland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="italy"></a>Италия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_italy_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_italy_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_italy_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_mobile_number"/>
          <Match idRef="Keywords_italy_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_italy_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="latvia"></a>Латвия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_latvia_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_latvia_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_latvia_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_mobile_number"/>
          <Match idRef="Keywords_latvia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_latvia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="lithuania"></a>Литва

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_lithuania_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_lithuania_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_lithuania_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_mobile_number"/>
          <Match idRef="Keywords_lithuania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_lithuania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="luxemburg"></a>Luxemburg

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_luxumburg_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_luxumburg_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_luxumburg_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxumburg_eu_mobile_number"/>
          <Match idRef="Keywords_luxumburg_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_luxumburg_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="malta"></a>Мальта

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_malta_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_malta_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_malta_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_mobile_number"/>
          <Match idRef="Keywords_malta_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_malta_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="netherlands"></a>Нидерланды

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_netherlands_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_netherlands_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_netherlands_eu_mobile_number` найден. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_mobile_number"/>
          <Match idRef="Keywords_netherlands_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_netherlands_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="poland"></a>Польша

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_poland_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_poland_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_poland_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_mobile_number"/>
          <Match idRef="Keywords_poland_eu_mobile_number" />
        </Pattern>
<!-- Strictly formatted patterns without mandatory corroborative evidence -->
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_poland_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="portugal"></a>Португалия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_portugal_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_portugal_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_portugal_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_mobile_number"/>
          <Match idRef="Keywords_portugal_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_portugal_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="romania"></a>Румыния

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_romania_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_romania_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_romania_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_mobile_number"/>
          <Match idRef="Keywords_romania_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_romania_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovakia"></a>Словакия

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovakia_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_slovakia_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovakia_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_mobile_number"/>
          <Match idRef="Keywords_slovakia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovakia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="slovenia"></a>Словения

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovenia_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_slovenia_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovenia_eu_mobile_number` найден. 
    
```
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_mobile_number"/>
          <Match idRef="Keywords_slovenia_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_slovenia_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="spain"></a>Испания

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_spain_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_spain_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_spain_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_mobile_number"/>
          <Match idRef="Keywords_spain_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_spain_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="sweden"></a>Швеция

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_sweden_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_sweden_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_sweden_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_mobile_number"/>
          <Match idRef="Keywords_sweden_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_sweden_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="uk"></a>(ВЕЛИКОБРИТАНИЯ)

### <a name="pattern"></a>Шаблон

-  Количество цифр 
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_uk_eu_mobile_number` находит контент, который соответствует шаблону. 
    
- Регулярное выражение `Regex_uk_eu_formatted_mobile_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_uk_eu_mobile_number` найден. 
    
```
 
<Entity id="a56a0418-136a-41ea-a337-4d0388b28e69" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_mobile_number"/>
          <Match idRef="Keywords_uk_eu_mobile_number" />
        </Pattern>
<Pattern confidenceLevel="75">
<IdMatch idRef="Regex_uk_eu_formatted_mobile_number" />
          </Pattern>
</Entity>
```

## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

