---
title: Номер паспорта ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении номер паспорта ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840328"
---
# <a name="eu-passport-number"></a>Номер паспорта ЕС

В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении номер паспорта ЕС тип конфиденциальных данных. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Формат

Один буквы, необязательное поле и семь цифр
  
### <a name="pattern"></a>Шаблон

Сочетание одной буквы, семь цифр и один пробел:
  
- Одна буква (без учета регистра)
    
- Один пробел (необязательно)
    
- семь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_austria_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_austria_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_austria_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта Австрия  <br/> Passport не  <br/> reisepass  <br/> österreichisch reisepass  <br/> |
   
## <a name="belgium"></a>Бельгия

### <a name="format"></a>Формат

Две буквы, а затем шести цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Две буквы и следуют шести цифр
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_belgium_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_belgium_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_belgium_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта Бельгия  <br/> Passport не  <br/> paspoort  <br/> paspoortnummer  <br/> reisepass kein  <br/> reisepass  <br/> |
   
## <a name="bulgaria"></a>Болгария

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 Девять цифр. 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_bulgaria_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_bulgaria_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_bulgaria_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта болгарский  <br/> Passport не  <br/> НОМЕР НА ПАСПОРТА  <br/> |
   
## <a name="croatia"></a>Хорватия

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 Девять цифр. 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_croatia_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_croatia_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_croatia_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта Хорватский  <br/> Passport не  <br/> broj putovnice  <br/> |
   
## <a name="cyprus"></a>Кипр

### <a name="format"></a>Формат

Один буквы, цифры 6-8 без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Один буквы, цифры 6-8
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_cyprus_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_cyprus_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_cyprus_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта Кипр  <br/> Passport не  <br/> ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ  <br/> |
   
## <a name="czech-republic"></a>Чешская Республика

### <a name="format"></a>Формат

Восьми знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восьми знаков без пробелов и разделители
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_czech_republic_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_czech_republic_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_czech_republic_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта чешский  <br/> Passport не  <br/> cestovní pas  <br/> PAS  <br/> |
   
## <a name="denmark"></a>Дания

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 Девять цифр. 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_denmark_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_denmark_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_denmark_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта датский  <br/> Passport не  <br/> PAS  <br/> pasnummer  <br/> |
   
## <a name="estonia"></a>Эстония

### <a name="format"></a>Формат

Один буквы, семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Один буквы, семь цифр
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_estonia_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_estonia_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_estonia_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта эстонский  <br/> Passport не  <br/> этап kodaniku eesti  <br/> |
   
## <a name="finland"></a>Финляндия

Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Финляндия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="france"></a>Франция

Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Гражданина Франции» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Германия

Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Германия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Греция

### <a name="format"></a>Формат

Две буквы, затем семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Две буквы, за которыми следуют семь цифр.
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_greece_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_greece_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_greece_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта греческий  <br/> Passport не  <br/> ΔΙΑΒΑΤΗΡΙΟ  <br/> |
   
## <a name="hungary"></a>Венгрия

### <a name="format"></a>Формат

Две буквы, затем шесть или семь цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Две буквы, затем шесть или семь цифр
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_hungary_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_hungary_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_hungary_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта венгерский  <br/> Passport не  <br/> útlevél száma  <br/> |
   
## <a name="ireland"></a>Ireland (Ирландия)

### <a name="format"></a>Формат

Два букв или цифр, а затем семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Два букв или цифр, а затем семь цифр:
  
- две цифры или буквы (без учета регистра);
    
- семь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_ireland_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_ireland_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_ireland_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта Ирландский  <br/> Passport не  <br/> PAS  <br/> passport  <br/> passeport  <br/> passeport numero  <br/> |
   
## <a name="italy"></a>Италия

### <a name="format"></a>Формат

Два букв или цифр, а затем семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Два букв или цифр, а затем семь цифр:
  
- две цифры или буквы (без учета регистра);
    
- семь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_italy_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_italy_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_italy_eu_passport_number**|
|:-----|
|Номер паспорта итальянский  <br/> repubblica italiana passaporto  <br/> passaporto  <br/> passaporto italiana  <br/> Номер паспорта  <br/> italiana passaporto numero  <br/> passaporto numero  <br/> numéro passeport italien  <br/> numéro passeport  <br/> |
   
## <a name="latvia"></a>Латвия

### <a name="format"></a>Формат

Два букв или цифр, а затем семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Два букв или цифр, а затем семь цифр:
  
- две цифры или буквы (без учета регистра);
    
- семь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_latvia_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_latvia_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_latvia_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта латышский  <br/> Passport не  <br/> pase numurs  <br/> |
   
## <a name="lithuania"></a>Литва

### <a name="format"></a>Формат

Восемь цифр или символов без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь цифр или символов (без учета регистра)
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_lithuania_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_lithuania_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_lithuania_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта lithunian  <br/> Passport не  <br/> paso numeris  <br/> |
   
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Формат

Восемь цифр или символов без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь цифр или символов (без учета регистра)
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_nation_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_nation_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_nation_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта латышский  <br/> Passport не  <br/> passnummer  <br/> |
   
## <a name="malta"></a>Мальта

### <a name="format"></a>Формат

Семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 семь цифр. 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_malta_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_malta_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_malta_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта maltese  <br/> Passport не  <br/> всего numru-passaport  <br/> |
   
## <a name="netherlands"></a>Нидерланды

### <a name="format"></a>Формат

Девять букв или цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять букв или цифр
  
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_netherlands_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_netherlands_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_netherlands_eu_passport_number**|
|:-----|
|Номер паспорта голландский  <br/> Номер паспорта  <br/> Номер паспорта Нидерланды  <br/> nederlanden paspoort nummer  <br/> paspoort  <br/> nederlanden paspoortnummer  <br/> paspoortnummer  <br/> |
   
## <a name="poland"></a>Польша

Для получения дополнительных сведений обратитесь к разделу «Номер паспорта для Польши» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="portugal"></a>Португалия

### <a name="format"></a>Формат

Один буквы, шести цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Один буквы шести цифр:
  
- Одна буква (без учета регистра)
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_portugal_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_portugal_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_portugal_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта португальский  <br/> Passport не  <br/> Действие passaporte número  <br/> |
   
## <a name="romania"></a>Румыния

### <a name="format"></a>Формат

Восемь или девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь или девяти цифр
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_romania_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_romania_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_romania_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта румынской  <br/> Passport не  <br/> numărul pașaportului  <br/> |
   
## <a name="slovakia"></a>Словакия

### <a name="format"></a>Формат

Одной цифры или буквы, семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Одной цифры или буквы (без учета регистра), семь цифр
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovakia_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovakia_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_slovakia_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта словацкий  <br/> Passport не  <br/> Číslo pasu  <br/> |
   
## <a name="slovenia"></a>Словения

### <a name="format"></a>Формат

Две буквы, затем семь знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Две буквы, затем семь цифр:
  
- Буква «P»
    
- Один прописная буква
    
- семь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovenia_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovenia_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_slovenia_eu_passport_number**|
|:-----|
|Номер паспорта  <br/> Номер паспорта словенский  <br/> Passport не  <br/> Список a potnega številka  <br/> |
   
## <a name="spain"></a>Испания

### <a name="format"></a>Формат

Сочетание восьми или девяти символов буквы и цифры без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

8 или 9 символ сочетание буквы и цифры:
  
-  Двух цифр или символов 
    
- Одну цифру или буква (необязательно)
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Неприменимо
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_spain_eu_passport_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_spain_eu_passport_number` найден. 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

| |
|**Keywords_spain_eu_passport_number**|
|:-----|
|passport  <br/> Испания паспорта  <br/> Книга паспорта  <br/> Номер паспорта  <br/> Passport не  <br/> libreta pasaporte  <br/> número pasaporte  <br/> españa pasaporte  <br/> pasaporte  <br/> |
   
## <a name="sweden"></a>Швеция

Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Швеция» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="uk"></a>(ВЕЛИКОБРИТАНИЯ)

Для получения дополнительных сведений обратитесь к разделу «Номер паспорта Великобритания США /» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

