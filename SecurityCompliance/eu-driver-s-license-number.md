---
title: Номер водительского удостоверения ЕС
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных номер водительского ЕС. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534810"
---
# <a name="eu-drivers-license-number"></a>Номер водительского удостоверения ЕС

В этом разделе показано, что политики (DLP) защита от потери данных выполняет поиск при обнаружении тип конфиденциальных данных номер водительского ЕС. Этот тип конфиденциальных данных определяет различные шаблоны, ключевые слова и другие свидетельства для каждой страны.
  
## <a name="austria"></a>Австрия

### <a name="format"></a>Формат

Восьми знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь цифр
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_austria_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_austria_eu_driver's_license_number` найден. 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_austria_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> Лицензия водительского удостоверения  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/>  номер водительского удостоверения  <br/> dlno #  <br/> fuhrerschein  <br/> fuhrerschein republik osterreich  <br/> |
   
## <a name="belgium"></a>Бельгия

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

10 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_belgium_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_belgium_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords__belgium_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> dlno #  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> führerscheinnummer  <br/> fuhrerscheinnummer  <br/> fuehrerscheinnummer  <br/> führerschein-nr  <br/> fuehrerschein-Nr  <br/> fuehrerschein-nr  <br/> |
   
## <a name="bulgaria"></a>Болгария

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_bulgaria_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_bulgaria_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_bulgaria_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> УПРАВЛЕНИЕ НА СВИДЕТЕЛСТВО ЗА МПС  <br/> СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО  <br/> СУМПС  <br/> ШОФЬОРСКА КНИЖКА  <br/> |
   
## <a name="croatia"></a>Хорватия

### <a name="format"></a>Формат

Восьми знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь цифр
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_croatia_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_croatia_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_croatia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> vozačka dozvola  <br/> |
   
## <a name="cyprus"></a>Кипр

### <a name="format"></a>Формат

12 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

12 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_cyprus_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_cyprus_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_cyprus_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> |
   
## <a name="czech-republic"></a>Чешская Республика

### <a name="format"></a>Формат

Две буквы, а затем шести цифр
  
### <a name="pattern"></a>Шаблон

8 букв или цифр:
  
- Две буквы (без учета регистра)
    
- пробел (необязательно); 
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_czech_republic_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_czech_republic_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_czech_republic_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> Řidičský prúkaz  <br/> |
   
## <a name="denmark"></a>Дания

### <a name="format"></a>Формат

Восьми знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Восемь цифр
  
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_denmark_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_denmark_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a>Keywords

| |
|**Keywords_denmark_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> kørekort  <br/> kørekortnummer  <br/> |
   
## <a name="estonia"></a>Эстония

### <a name="format"></a>Формат

Две буквы, а затем шести цифр
  
### <a name="pattern"></a>Шаблон

Две буквы и шести цифр:
  
-  Буквы «И» (без учета регистра) 
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_estonia_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_estonia_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_estonia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения  <br/> dlno #  <br/> 
permis de conduire  <br/> |
   
## <a name="finland"></a>Финляндия

### <a name="format"></a>Формат

10 цифр, содержащих дефис.
  
### <a name="pattern"></a>Шаблон

10 цифр, содержащий дефис:
  
-  Шесть цифр 
    
- дефис;
    
-  Четыре цифры 
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_finland_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_finland_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_finland_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> ajokortti  <br/> |
   
## <a name="france"></a>Франция

Для получения дополнительных сведений обратитесь к разделу «Номер водительского удостоверения Франция» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="germany"></a>Германия

Для получения дополнительных сведений обратитесь к разделу «Немецкий номер водительского удостоверения» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="greece"></a>Греция

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 Девять цифр. 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_greece_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_greece_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_greece_eu_driver's_license_number**|
|:-----|
|DLL-библиотека #  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> ΔΕΙΑ ΟΔΉΓΗΣΗΣ  <br/> Adeia odigisis  <br/> |
   
## <a name="hungary"></a>Венгрия

### <a name="format"></a>Формат

Две буквы, а затем шести цифр
  
### <a name="pattern"></a>Шаблон

Две буквы и шести цифр:
  
-  Две буквы (без учета регистра) 
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_hungary_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_hungary_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_hungary_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> vezetoi engedely  <br/> |
   
## <a name="ireland"></a>Ireland

### <a name="format"></a>Формат

Шести цифр, а затем четырех букв
  
### <a name="pattern"></a>Шаблон

Шести цифр и четыре буквы:
  
- Шесть цифр
    
- Четыре буквы (без учета регистра)
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_ireland_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_ireland_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_ireland_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> ceadúnas tiomána  <br/> |
   
## <a name="italy"></a>Италия

Для получения дополнительных сведений обратитесь к разделу «Номер водительского удостоверения Италия» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="latvia"></a>Латвия

### <a name="format"></a>Формат

Три буквы, а затем шести цифр
  
### <a name="pattern"></a>Шаблон

Три буквы и шести цифр:
  
-  Три буквы (без учета регистра) 
    
- Шесть цифр
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_latvia_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_latvia_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_latvia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> autovadītāja apliecība  <br/> |
   
## <a name="lithuania"></a>Литва

### <a name="format"></a>Формат

Восьми знаков без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 Восемь цифр 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_lithuania_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_lithuania_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_lithuania_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> vairuotojo pažymėjimas  <br/> |
   
## <a name="luxemburg"></a>Luxemburg

### <a name="format"></a>Формат

Шести цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

 Шесть цифр 
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_luxemburg_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_luxemburg_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_luxemburg_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> fahrerlaubnis  <br/> |
   
## <a name="malta"></a>Мальта

### <a name="format"></a>Формат

Сочетание двух символов и шести цифр в указанному шаблону
  
### <a name="pattern"></a>Шаблон

Сочетание двух символов и шести цифр:
  
- Два знаков (цифр или символов, без учета регистра)
    
- пробел (необязательно); 
    
- Три цифры
    
- пробел (необязательно); 
    
- Три цифры
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_malta_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_malta_eu_driver's_license_number` найден. 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_malta_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> liċenzja задач sewqan  <br/> |
   
## <a name="netherlands"></a>Нидерланды

### <a name="format"></a>Формат

10 цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

10 цифр.
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_netherlands_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_netherlands_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_netherlands_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> 
permis de conduire  <br/> rijbewijs  <br/> rijbewijsnummer  <br/> |
   
## <a name="poland"></a>Польша

### <a name="format"></a>Формат

14 цифр, содержащий 2 косая черта
  
### <a name="pattern"></a>Шаблон

14 цифр и косая черта 2:
  
-  Пять цифр 
    
- косая черта;
    
- Две цифры
    
- косая черта;
    
- семь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_poland_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_poland_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_poland_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> prawo jazdy  <br/> |
   
## <a name="portugal"></a>Португалия

### <a name="format"></a>Формат

Две буквы, затем семь номеров в указанному шаблону
  
### <a name="pattern"></a>Шаблон

Две буквы, затем семь номеров с помощью специальных символов:
  
-  Две буквы (без учета регистра) 
    
- дефис;
    
- Шесть цифр
    
- Пробел
    
- Одна цифра
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_portugal_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_portugal_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_portugal_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> motorista де carteira  <br/> |
   
## <a name="romania"></a>Румыния

### <a name="format"></a>Формат

Один символ, а затем восьми знаков
  
### <a name="pattern"></a>Шаблон

Один символ, а затем восьми знаков:
  
-  Один (без учета регистра) букв или цифр 
    
- восемь цифр.
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_romania_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_romania_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_romania_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> conducere де permis  <br/> |
   
## <a name="slovakia"></a>Словакия

### <a name="format"></a>Формат

Один символ, а затем семь цифр
  
### <a name="pattern"></a>Шаблон

Один символ, а затем семь цифр
  
- Один (без учета регистра) букв или цифр
    
-  семь цифр. 
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovakia_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovakia_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovakia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> vodičský preukaz  <br/> |
   
## <a name="slovenia"></a>Словения

### <a name="format"></a>Формат

Девяти цифр без пробелов и разделители
  
### <a name="pattern"></a>Шаблон

Девять цифр.
  
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_slovenia_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_slovenia_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_slovenia_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> vozniško dovoljenje  <br/> |
   
## <a name="spain"></a>Испания

### <a name="format"></a>Формат

Восемь цифр, за которой следует один символ
  
### <a name="pattern"></a>Шаблон

Восемь цифр, за которой следует один символ:
  
-  восемь цифр. 
    
- Одну цифру или букву (без учета регистра)
    
### <a name="checksum"></a>Контрольная сумма

Да
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Функция `Func_spain_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_spain_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_spain_eu_driver's_license_number**|
|:-----|
|dlno #  <br/> dl#  <br/> драйверы lic.  <br/> драйвер лицензия  <br/> driver license  <br/> drivers licence  <br/> drivers license  <br/> Лицензия водительского удостоверения  <br/> driver's license  <br/> driving licence
  <br/> управляющий лицензии  <br/> Номер лицензии драйвера  <br/> драйвер номер  <br/> драйверы лицензия номер  <br/> Номер драйверы  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> средство повышения лицензия номер  <br/> номер водительского удостоверения  <br/> управляющий разрешения  <br/> управляющий номер разрешения  <br/> conducción де permiso  <br/> permiso conducción  <br/> número licencia conducir  <br/> número de carnet де conducir  <br/> número carnet conducir  <br/> licencia conducir  <br/> número de permiso де conducir  <br/> conducir permiso де número  <br/> número permiso conducir  <br/> permiso conducir  <br/> manejo де licencia  <br/> EL carnet de conducir  <br/> carnet conducir  <br/> |
   
## <a name="sweden"></a>Швеция

### <a name="format"></a>Формат

10 цифр, содержащий дефис
  
### <a name="pattern"></a>Шаблон

10 цифр, содержащий дефис:
  
-  Шесть цифр 
    
- дефис;
    
- Четыре цифры
    
### <a name="checksum"></a>Контрольная сумма

Нет
  
### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
  
- Регулярное выражение `Regex_sweden_eu_driver's_license_number` находит контент, который соответствует шаблону. 
    
- Ключевое слово из `Keywords_sweden_eu_driver's_license_number` найден. 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a>Keywords

| |
|**Keywords_sweden_eu_driver's_license_number**|
|:-----|
|dl#  <br/> driver license  <br/> драйвер номер  <br/> драйвер лицензия  <br/> драйверы lic.  <br/> drivers license  <br/> drivers licence  <br/> driver's license  <br/> номер водительского удостоверения  <br/> номер водительского удостоверения для лицензирования  <br/> номер водительского удостоверения  <br/> dlno #  <br/> körkort  <br/> |
   
## <a name="uk"></a>(ВЕЛИКОБРИТАНИЯ)

Для получения дополнительных сведений обратитесь к разделу «Номер водительского удостоверения Великобритания» в [Поиск типы конфиденциальных сведений](what-the-sensitive-information-types-look-for.md).
  
## <a name="see-also"></a>См. также

[Что позволяют искать типы конфиденциальной информации](what-the-sensitive-information-types-look-for.md)

