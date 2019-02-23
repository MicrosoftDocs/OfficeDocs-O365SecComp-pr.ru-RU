---
title: Что позволяют искать типы конфиденциальной информации
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
search.appverid: MET150
ms.topic: reference
f1_keywords:
- ms.o365.cc.UnifiedDLPRuleContainsSensitiveInformation
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
ms.assetid: fd505979-76be-4d9f-b459-abef3fc9e86b
description: Защита от потери данных (DLP) в центре безопасности &amp; Office 365 включает в себя 80 типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показано, как будет выглядеть политика DLP при обнаружении каждого типа.
ms.openlocfilehash: 17fb0b8d745168f8000fba9e6fc42f3c255a1937
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216359"
---
# <a name="what-the-sensitive-information-types-look-for"></a>Что позволяют искать типы конфиденциальной информации

Защита от потери данных (DLP) в центре безопасности &amp; Office 365 содержит множество типов конфиденциальной информации, готовых к использованию в политиках защиты от потери данных. В этом разделе перечислены все эти типы конфиденциальной информации и показано, как будет выглядеть политика DLP при обнаружении каждого типа. Тип конфиденциальной информации определяется шаблоном, который может быть идентифицирован регулярным выражением или функцией. Кроме того, подкрепляющее, такие как ключевые слова и контрольные суммы, можно использовать для определения типа конфиденциальной информации. Уровень вероятности и близость также используются в процессе оценки.
  
## <a name="aba-routing-number"></a>Код банка ABA

### <a name="format"></a>Формат

9 цифр в виде форматированного или неформатированного шаблона.

### <a name="pattern"></a>Шаблон

С форматированием
- четыре цифры, начиная с 0, 1, 2, 3, 6, 7 или 8;
- дефис;
- Четыре цифры
- дефис; 
- Одна цифра

Неформатированные: 9 последовательных цифр, начиная с 0, 1, 2, 3, 6, 7 или 8. 

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_aba_routing находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_ABA_Routing.

```
<!-- ABA Routing Number -->
<Entity id="cb353f78-2b72-4c3c-8827-92ebe4f69fdf" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_aba_routing" />
        <Match idRef="Keyword_ABA_Routing" />
      </Pattern>
 </Entity>
```


### <a name="keywords"></a>Ключевые слова

#### <a name="keywordabarouting"></a>Кэйворд_аба_раутинг

- aba
- 
aba#
- 
aba routing #
- номер маршрутизации код банка ABA
- 
aba#
- 
abarouting#
- 
aba number
- 
abaroutingnumber
- 
american bank association routing #
- 
american bank association routing number
- 
americanbankassociationrouting#
- 
americanbankassociationroutingnumber
- 
bank routing number
- 
bankrouting#
- 
bankroutingnumber
- 
routing transit number
- 
RTN
 
   
## <a name="argentina-national-identity-dni-number"></a>Номер внутреннего удостоверения личности для Аргентины (DNI)

### <a name="format"></a>Формат

Восемь цифр, разделенных точками.

### <a name="pattern"></a>Шаблон

Восемь цифр:
- Две цифры
- точка;
- три цифры; 
- точка;
- Три цифры

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_argentina_national_id находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_argentina_national_id.

```
<!-- Argentina National Identity (DNI) Number -->
<Entity id="eefbb00e-8282-433c-8620-8f1da3bffdb2" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_argentina_national_id"/>
      <Match idRef="Keyword_argentina_national_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordargentinanationalid"></a>Кэйворд_аржентина_натионал_ид

- Argentina National Identity number
 
- Идентификация 
- Идентификация национальной идентификационной карточки 
- DNI
 
- Национальная реестр пользователей NIC 
- Documento Nacional de Identidad
 
- Registro Nacional de las Personas
 
- Identidad
 
- Identificación
 
   
## <a name="australia-bank-account-number"></a>Номер банковского счета для Австралии

### <a name="format"></a>Формат

6–10 цифр с номером филиала банка в штате или без него.

### <a name="pattern"></a>Шаблон

Номер счета — 6-10 цифр. Номер филиала банковского состояния Австралии:
- Три цифры 
- дефис; 
- Три цифры

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_australia_bank_account_number.
- регулярное выражение Regex_australia_bank_account_number_bsb находит содержимое, которое соответствует шаблону.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_australia_bank_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_australia_bank_account_number.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordaustraliabankaccountnumber"></a>Кэйворд_аустралиа_банк_аккаунт_нумбер

- swift bank code
- 
correspondent bank
- 
base currency
- 
usa account
- 
holder address
- 
bank address
- 
information account
- 
fund transfers
- 
bank charges
- 
bank details
- 
banking information
- 
full names
- 

iaea

   
## <a name="australia-drivers-license-number"></a>Номер водительского удостоверения для Австралии

### <a name="format"></a>Формат

Девять букв и цифр.

### <a name="pattern"></a>Шаблон

Девять букв и цифр: 

- две цифры или буквы (без учета регистра); 
- Две цифры 
- пять цифр или букв (без учета регистра).

ИЛИ

- 1–2 дополнительные буквы (без учета регистра); 
- 4–9 цифр.

ИЛИ

- девять цифр или букв (без учета регистра).

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_australia_drivers_license_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_australia_drivers_license_number;
- ни одно ключевое слово из Keyword_australia_drivers_license_number_exclusions не находится.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordaustraliadriverslicensenumber"></a>Кэйворд_аустралиа_дриверс_лиценсе_нумбер

- international driving permits
- 
australian automobile association
- 
international driving permit
- Дриверлиценце
- Дриверлиценцес
- Драйвер Лик
- Driver Licence

- Driver Licences

- Дриверслик
- Дриверслиценце
- Дриверслиценцес
- Драйверы Лик
- Драйверы ликс
- Лицензия на драйверы
- Лицензии на драйверы
- Driver ' LIC
- Driver ' LICS
- Driver ' Licence
- Driver ' Licences
- Драйвер "Лик
- Драйвер "ЛИКС
- Лицензия на драйвер
- Лицензии на драйвер
- Дривер'слик
- Дривер'сликс
- Дривер'слиценце
- Дривер'слиценцес
- Лик драйвера
- Ликс драйвера
- Driver's Licence

- Driver's Licences

- Дриверлик #
- Дриверликс #
- Дриверлиценце #
- Дриверлиценцес #
- Driver Lic#
- 
Driver Lics#

- Лицензия на драйвер #
- Лицензия на драйвер #
- Дриверслик #
- Дриверсликс #
- Дриверслиценце #
- Дриверслиценцес #
- Drivers Лик #
- Drivers ликс #
- Драйвер, лицензия #
- Лицензии на драйверы #
- Driver' Lic#

- Driver' Lics#

- Driver' Licence#

- Driver' Licences#

- Driver' Lic#

- Driver' Lics#

- Драйвер "водительская лицензия"
- Водитель # число лицензий
- Дривер'слик #
- Дривер'сликс #
- Дривер'слиценце #
- Дривер'слиценцес #
- Driver's Lic#

- Driver's Lics#

- Номер лицензии на драйвер
- Лицензии на драйвер # 

#### <a name="keywordaustraliadriverslicensenumberexclusions"></a>Кэйворд_аустралиа_дриверс_лиценсе_нумбер_ексклусионс

- aaa
- Дриверлиценсе
- Дриверлиценсес
- Лицензия на драйвер
- Лицензии на драйверы
- Дриверслиценсе
- Дриверслиценсес
- Лицензия на драйверы
- Лицензии на драйверы
- Driver ' License
- Driver ' Licenses
- Лицензия "Driver"
- Лицензии на драйвер
- Дривер'слиценсе
- Дривер'слиценсес
- Лицензия на драйвер
- Лицензии на драйвер
- Дриверлиценсе #
- Дриверлиценсес #
- Номер лицензии драйвера
- Лицензии на драйверы #
- Дриверслиценсе #
- Дриверслиценсес #
- Driver License #
- Лицензии на драйверы #
- Driver' License#

- Driver' Licenses#

- Driver' License#

- Driver' Licenses#

- Дривер'слиценсе #
- Дривер'слиценсес #
- Driver's License#

- 

Driver's Licenses#
   
## <a name="australia-medical-account-number"></a>Номер карты медицинского страхования для Австралии

### <a name="format"></a>Формат

10–11 цифр.

### <a name="pattern"></a>Шаблон

10–11 цифр.
- Первая цифра находится в диапазоне 2–6.
- Девятая цифра — проверочная.
- Десятая цифра — цифра серии.
- Одиннадцатая цифра (необязательно) — индивидуальный номер.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_Australia_Medical_Account_Number;
- Контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_australian_medical_account_number находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordaustraliamedicalaccountnumber"></a>Кэйворд_аустралиа_медикал_аккаунт_нумбер

- bank account details
- 
medicare payments
- 
mortgage account
- 
bank payments
- 
information branch
- 
credit card loan
- 
department of human services
- Локальная служба
- 

medicare

   
## <a name="australia-passport-number"></a>Номер паспорта гражданина Австралии

### <a name="format"></a>Формат

Буква, за которой следуют семь цифр.

### <a name="pattern"></a>Шаблон

Буква (без учета регистра), за которой следуют семь цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_australia_passport_number находит содержимое, которое соответствует шаблону;
- Найдено ключевое слово из Кэйворд_пасспорт или Кэйворд_аустралиа_пасспорт_нумбер.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordpassport"></a>Кэйворд_пасспорт

- Passport Number
- 
Passport No
- Passport#

- Passport#

- Пасспортид
- Passportno

- passportnumber

- パスポート
- パスポート番号

- パスポートのNum

- 
パスポート＃
 
- Numéro de passeport
- 
Passeport n °
- Passeport Non

- Passeport#

- Passeport#

- Пассепортнон
- Passeportn °


#### <a name="keywordaustraliapassportnumber"></a>Кэйворд_аустралиа_пасспорт_нумбер

- passport
- 
passport details
- 
immigration and citizenship
- 
commonwealth of australia
- 
department of immigration
- 
residential address
- 
department of immigration and citizenship
- visa

- 
national identity card
- номер паспорта
- 
travel document
- 

issuing authority
   
## <a name="australia-tax-file-number"></a>Номер налогоплательщика для Австралии

### <a name="format"></a>Формат

8–9 цифр.

### <a name="pattern"></a>Шаблон

8–9 цифр, которые обычно разделены пробелами указанным ниже образом.
- Три цифры 
- Необязательный пробел 
- Три цифры 
- Необязательный пробел 
- 2–3 цифры, причем последняя цифра — контрольная

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_australian_tax_file_number находит содержимое, которое соответствует шаблону;
- ни одно ключевое слово из Keyword_Australia_Tax_File_Number или Keyword_number_exclusions не найдено;
- Контрольная сумма проходит проверку.

```
    <!-- Australia Tax File Number -->
<Entity id="e29bc95f-ff70-4a37-aa01-04d17360a4c5" patternsProximity="300" recommendedConfidence="85">
    
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_australian_tax_file_number" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Keyword_Australia_Tax_File_Number" />
          <Match idRef="Keyword_number_exclusions" />
        </Any>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordaustraliataxfilenumber"></a>Кэйворд_аустралиа_такс_филе_нумбер

- australian business number
- 
marginal tax rate
- 
medicare levy
- 
portfolio number
- 
service veterans
- 
withholding tax
- 
individual tax return
- 

tax file number

#### <a name="keywordnumberexclusions"></a>Кэйворд_нумбер_ексклусионс

- 00000001
- 11111111
- 22222222
- 33333333
- 44444444
- 55555555
- 66666666
- 77777777
- 88888888
- 99999999
- 000000000
- 111111111
- 222222222
- 333333333
- 444444444
- 555555555
- 666666666
- 777777777
- 888888888
- 999999999
- 0000000000
- 1111111111
- 2222222222
- 3333333333
- 4444444444
- 5555555555
- 6666666666
- 7777777777
- 8888888888
- 9999999999
   
## <a name="belgium-national-number"></a>Номер национального документа для Бельгии

### <a name="format"></a>Формат

11 цифр, а также разделители.

### <a name="pattern"></a>Шаблон

11 цифр, а также разделители:
- шесть цифр и две точки в формате ГГ.ММ.ДД для даты рождения; 
- дефис; 
- три последовательные цифры (нечетные для мужчин, четные для женщин); 
- точка; 
- две проверочные цифры.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_belgium_national_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_belgium_national_number;
- Контрольная сумма проходит проверку.

```
<!-- Belgium National Number -->
  <Entity id="fb969c9e-0fd1-4b18-8091-a2123c5e6a54" recommendedConfidence="75" patternsProximity="300">
   <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_belgium_national_number"/>
     <Match idRef="Keyword_belgium_national_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordbelgiumnationalnumber"></a>Кэйворд_белгиум_натионал_нумбер

- Identity
- Registration
- Identification 
- ID 
- Identiteitskaart
- Registratie nummer 
 
- Identificatie nummer
 
- Identiteit
- Registratie
- Identificatie

 
- Carte d’identité
 
- numéro d'immatriculation
- numéro d'identification
- 
identité
 
- inscription
 
- Identifikation
- Identifizierung
- Identifikationsnummer
- Personalausweis
- Registrierung
- Registrationsnummer

   
## <a name="brazil-cpf-number"></a>Номер CPF для Бразилии

### <a name="format"></a>Формат

11 цифр, которые включают проверочную цифру и могут быть форматированными или неформатированными.

### <a name="pattern"></a>Шаблон

С форматированием
- три цифры;  
- точка;  
- три цифры; 
- точка;  
- Три цифры 
- Дефис 
- две проверочные цифры.

Без форматирования
- 11 цифр, где две последние цифры — проверочные.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_brazil_cpf;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_brazil_cpf находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordbrazilcpf"></a>Кэйворд_бразил_кпф

- CPF
- Identification
- Registration
- Revenue
- Cadastro de Pessoas Físicas
 
- Imposto
 
- Identificação
 
- Inscrição
 
- Receita

 
   
## <a name="brazil-legal-entity-number-cnpj"></a>Номер юридического лица для Бразилии (CNPJ)

### <a name="format"></a>Формат

14 цифр, которые включают регистрационный номер, номер филиала и проверочные цифры, а также разделители.

### <a name="pattern"></a>Шаблон
14 цифр, а также разделители:
- Две цифры 
- точка; 
- три цифры;  
- точка; 
- три цифры (эти первые восемь цифр — регистрационный номер); 
- косая черта; 
- номер отделения из четырех цифр; 
- дефис; 
- две проверочные цифры.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_brazil_cnpj;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_brazil_cnpj находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordbrazilcnpj"></a>Кэйворд_бразил_кнпж

- CNPJ
 
- CNPJ/MF 
- CNPJ-MF
 
- National Registry of Legal Entities
 
- Taxpayers Registry
 
- Legal entity
 
- Legal entities
 
- Registration Status
 
- Business
 
- Company
- CNPJ
 
- Cadastro Nacional da Pessoa Jurídica
 
- Cadastro Geral de Contribuintes
 
- CGC
 
- Pessoa jurídica
 
- Pessoas jurídicas
 
- Situação cadastral
 
- Inscrição
 
- Empresa
 
   
## <a name="brazil-national-id-card-rg"></a>	Номер внутреннего удостоверения личности для Бразилии (RG)

### <a name="format"></a>Формат

Registro Geral (старый формат): девять цифр

Registro de identidade (RIC) (новый формат): 11 цифр

### <a name="pattern"></a>Шаблон

Registro Geral (старый формат):
- Две цифры 
- точка; 
- три цифры;  
- точка; 
- Три цифры 
- дефис; 
- одна цифра — проверочная.

Registro de identidade (RIC) (новый формат):
- 10 цифр; 
- дефис; 
- одна цифра — проверочная.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_brazil_rg находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_brazil_rg;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_brazil_rg находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordbrazilrg"></a>Кэйворд_бразил_рг

Кéдула de identidade Identity Card National ID нúмеро de ррегистро Registro de Иидентидаде Registro Geral RG (это ключевое слово учитывает регистр) RIC (это ключевое слово учитывает регистр). 
   
## <a name="canada-bank-account-number"></a>Номер банковского счета для Канады

### <a name="format"></a>Формат

Семь или двенадцать цифр.

### <a name="pattern"></a>Шаблон

Номер банковского счета для Канады — семь или двенадцать цифр.

Транзитный номер банковского счета в Канаде имеет указанный ниже формат.
- Пять цифр 
- дефис; 
- Три цифры или
- ноль "0"; 
- восемь цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_canada_bank_account_number.
- регулярное выражение Regex_canada_bank_account_transit_number находит содержимое, которое соответствует шаблону.

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_canada_bank_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_canada_bank_account_number.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordcanadabankaccountnumber"></a>Кэйворд_канада_банк_аккаунт_нумбер

- canada savings bonds
- 
canada revenue agency
- 
canadian financial institution
- 
direct deposit form
- 
canadian citizen
- 
legal representative
- 
notary public
- 
commissioner for oaths
- 
child care benefit
- 
universal child care
- 
canada child tax benefit
- 
income tax benefit
- 
harmonized sales tax
- social insurance number
- 
income tax refund
- 
child tax benefit
- 
territorial payments
- 
institution number
- 
deposit request
- 
banking information
- 

direct deposit
   
## <a name="canada-drivers-license-number"></a>Номер водительского удостоверения для Канады

### <a name="format"></a>Формат

Зависит от провинции.

### <a name="pattern"></a>Шаблон

Различные шаблоны, соответствующие провинциям Альберта, Британская Колумбия, Манитоба, Нью-Брансуик, Ньюфаундленд и Лабрадор, Новая Шотландия, Онтарио, Остров Принца Эдуарда, Квебек и Саскачеван.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_[province_name]_drivers_license_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_[province_name]_drivers_license_name;
- находится ключевое слово из Keyword_canada_drivers_license.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordprovincenamedriverslicensename"></a>Keyword_[province_name]_drivers_license_name

- Аббревиатура провинции, например AB.
- 
Название провинции, например Альберта.

#### <a name="keywordcanadadriverslicense"></a>Кэйворд_канада_дриверс_лиценсе

- DL
- DLS
- КДЛ
- КДЛС
- Дриверлик
- Дриверликс
- Дриверлиценсе
- Дриверлиценсес
- Дриверлиценце
- Дриверлиценцес
- Драйвер Лик
- Драйвер ликс
- Лицензия на драйвер
- Лицензии на драйверы
- Driver Licence

- Driver Licences

- Дриверслик
- Дриверсликс
- Дриверслиценце
- Дриверслиценцес
- Дриверслиценсе
- Дриверслиценсес
- Драйверы Лик
- Драйверы ликс
- Лицензия на драйверы
- Лицензии на драйверы
- Лицензия на драйверы
- Лицензии на драйверы
- Driver ' LIC
- Driver ' LICS
- Driver ' License
- Driver ' Licenses
- Driver ' Licence
- Driver ' Licences
- Драйвер "Лик
- Драйвер "ЛИКС
- Лицензия "Driver"
- Лицензии на драйвер
- Лицензия на драйвер
- Лицензии на драйвер
- Дривер'слик
- Дривер'сликс
- Дривер'слиценсе
- Дривер'слиценсес
- Дривер'слиценце
- Дривер'слиценцес
- Лик драйвера
- Ликс драйвера
- Лицензия на драйвер
- Лицензии на драйвер
- Driver's Licence

- Driver's Licences

- Разрешение de Кондуире
- id
- идентификаторы
- 
idcard number
- 
idcard numbers
- 
idcard#
- 
idcard #s
- карточка идкард
- карточки идкард
- идкард
- identification number

- identification numbers

- identification #

- 
identification #s
- идентификационная карточка
- идентификационные карточки
- 
identification
 
- DL#
- 
DLS#
 
- CDL#
 
- CDLS#
 
- Дриверлик # 
- Дриверликс # 
- Дриверлиценсе # 
- Дриверлиценсес # 
- Дриверлиценце # 
- Дриверлиценцес # 
- Driver Lic#
- 
Driver Lics#
 
- Номер лицензии драйвера 
- Лицензии на драйверы # 
- Номер лицензии драйвера 
- Лицензия на драйвер # 
- Дриверслик # 
- Дриверсликс # 
- Дриверслиценсе # 
- Дриверслиценсес # 
- Дриверслиценце # 
- Дриверслиценцес # 
- Drivers Лик # 
- Drivers ликс # 
- Driver License # 
- Лицензии на драйверы # 
- Драйвер, лицензия # 
- Лицензии на драйверы # 
- Driver' Lic#
 
- Driver' Lics#
 
- Driver' License#
 
- Driver' Licenses#
 
- Driver' Licence#
 
- Driver' Licences#
 
- Driver' Lic#
 
- Driver' Lics#
 
- Driver' License#
 
- Driver' Licenses#
 
- Драйвер "водительская лицензия" 
- Водитель # число лицензий 
- Дривер'слик # 
- Дривер'сликс # 
- Дривер'слиценсе # 
- Дривер'слиценсес # 
- Дривер'слиценце # 
- Дривер'слиценцес # 
- Driver's Lic#
 
- Driver's Lics#
 
- Driver's License#
 
- Driver's Licenses#
 
- Номер лицензии на драйвер 
- Лицензии на драйвер # 
- Разрешение de Кондуире # 
- кодов 
- идентификаторы 
- idcard card#
 
- idcard cards#
 
- idcard#
 
- identification card#
 
- identification cards#
 
- identification #
 
   
## <a name="canada-health-service-number"></a>Номер службы здравоохранения для Канады

### <a name="format"></a>Формат

10 цифр.

### <a name="pattern"></a>Шаблон

10 цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_canada_health_service_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_canada_health_service_number.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordcanadahealthservicenumber"></a>Кэйворд_канада_хеалс_сервице_нумбер

- personal health number
- 
patient information
- службы работоспособности
- 
speciality services
- 
automobile accident
- 
patient hospital
- 
psychiatrist
- 
workers compensation
- 
disability
      
## <a name="canada-passport-number"></a>Номер паспорта гражданина Канады

### <a name="format"></a>Формат

Две прописные буквы, за которыми следуют шесть цифр.

### <a name="pattern"></a>Шаблон

Две прописные буквы, за которыми следуют шесть цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_canada_passport_number находит содержимое, которое соответствует шаблону;
- Найдено ключевое слово из Кэйворд_канада_пасспорт_нумбер или Кэйворд_пасспорт.

``` 
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordcanadapassportnumber"></a>Кэйворд_канада_пасспорт_нумбер

- canadian citizenship
- 
canadian passport
- 
passport application
- 
passport photos
- 
certified translator
- 
canadian citizens
- 
processing times
- 

renewal application

#### <a name="keywordpassport"></a>Кэйворд_пасспорт

- Passport Number
- 
Passport No
- Passport#

- Passport#

- Пасспортид
- Passportno

- passportnumber

- パスポート
- パスポート番号

- パスポートのNum

- パスポート＃

- Numéro de passeport
- 
Passeport n °
- Passeport Non

- Passeport#

- Passeport#

- Пассепортнон
- 

Passeportn °
   
## <a name="canada-personal-health-identification-number-phin"></a>Персональный идентификационный номер службы здравоохранения для Канады (PHIN)

### <a name="format"></a>Формат

Девять цифр.

### <a name="pattern"></a>Шаблон

Девять цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_канада_фин находит содержимое, которое соответствует шаблону. Найдены по крайней мере два ключевых слова от Кэйворд_канада_фин или Кэйворд_канада_провинцес.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordcanadaphin"></a>Кэйворд_канада_фин

- social insurance number
- 
health information act
- 
income tax information
- 
manitoba health
- 
health registration
- 
prescription purchases
- 
benefit eligibility
- 
personal health
- 
power of attorney
- 
registration number
- personal health number
- 
practitioner referral
- 
wellness professional
- 
patient referral
- 

health and wellness

#### <a name="keywordcanadaprovinces"></a>Кэйворд_канада_провинцес

- Nunavut
- 
Quebec
- 
Northwest Territories
- 
Ontario
- 
British Columbia
- 
Alberta
- 
Saskatchewan
- 
Manitoba
- 
Yukon
- 
Newfoundland and Labrador
- 
New Brunswick
- 
Nova Scotia
- 
Prince Edward Island
- Канада
   
## <a name="canada-social-insurance-number"></a>Номер карты социального страхования для Канады

### <a name="format"></a>Формат

Девять цифр с необязательными дефисами или пробелами.

### <a name="pattern"></a>Шаблон

С форматированием
- Три цифры 
- дефис или пробел;  
- Три цифры 
- дефис или пробел;  
- Три цифры

Неформатированные: девять цифр

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_canadian_sin находит содержимое, которое соответствует шаблону.
- Выполняются по меньшей мере два из таких условий:
    - найдено ключевое слово из Keyword_sin;
    - найдено ключевое слово из Keyword_sin_collaborative;
    - функция Func_eu_date находит дату в правильном формате.
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_unformatted_canadian_sin находит содержимое, которое соответствует шаблону;
- найдено ключевое слово из Keyword_sin;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsin"></a>Кэйворд_син

- Синус 
- social insurance
 
- numero d'assurance sociale
 
- sins
 
- SSN 
- ssNS 
- социальное обеспечение безопасности 
- numero d'assurance social
 
- Национальный идентификационный номер 
- 
national id 
- sin#
 
- soc ins
 
- social ins
 

#### <a name="keywordsincollaborative"></a>Кэйворд_син_коллаборативе

- driver's license 
- drivers license 
- Лицензия на драйвер 
- drivers licence 
- DOB
 
- Birthdate 
- День рождения  
- Date of Birth
 
   
## <a name="chile-identity-card-number"></a>	Номер удостоверения личности для Чили

### <a name="format"></a>Формат

7-8 цифр и разделители — контрольная цифра или буква

### <a name="pattern"></a>Шаблон

7–8 цифр, а также разделители:
- 1 или 2 цифры; 
- точка; 
- три цифры; 
- точка; 
- три цифры; 
- Тире 
- одна цифра или буква (без учета регистра) — проверочная.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_chile_id_card находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_chile_id_card;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_chile_id_card находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordchileidcard"></a>Кэйворд_чиле_ид_кард

- National Identification Number
 
- Identity card 
- ID 
- Identification 
- Rol Único Nacional
 
- ВЫПОЛНЯЕМ 
- Rol Único Tributario
 
- RUT
 
- Cédula de Identidad
 
- Número De Identificación Nacional
 
- Tarjeta de identificación
 
- Identificación
 
   
## <a name="china-resident-identity-card-prc-number"></a>	Номер удостоверения личности жителя Китая (КНР)

### <a name="format"></a>Формат

18 цифр.

### <a name="pattern"></a>Шаблон

18 цифр:
- шесть цифр — код адреса; 
- восемь цифр в виде ГГГГММДД — дата рождения; 
- три цифры — серия карты; 
- одна цифра — проверочная.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_china_resident_id находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_china_resident_id;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_china_resident_id находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

### <a name="keywordchinaresidentid"></a>Кэйворд_чина_ресидент_ид

- Resident Identity Card
 
- NO7 
- National Identification Card
 
- 身份证  
- 居民 身份证  
- 居民身份证
 
- 鉴定

 
- 身分證  
- 居民 身份證
- 鑑定  
   
## <a name="credit-card-number"></a>Номер кредитной карты

### <a name="format"></a>Формат

16 цифр, которые могут быть форматированными или неформатированными (цццццццццццццццц) и должны пройти проверку Луна.

### <a name="pattern"></a>Шаблон

Очень сложный и надежный шаблон, который определяет карты всех основных мировых стандартов, включая Visa, MasterCard, Discover Card, JCB, American Express, подарочные карты и карты Diners Club.

### <a name="checksum"></a>Контрольная сумма

Да (рассчитывается по алгоритму Луна).

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_credit_card находит содержимое, которое соответствует шаблону;
- Верно одно из условий ниже:
    - найдено ключевое слово из Keyword_cc_verification;
    - найдено ключевое слово из Keyword_cc_name;
    - функция Func_expiration_date находит дату в правильном формате.
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- функция Func_credit_card находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordccverification"></a>Кэйворд_кк_верификатион

- card verification
- card identification number
- cvn

- cid

- CVC2
- CVV2
- pin block

- security code

- security number

- security no

- issue number

- issue no

- cryptogramme

- numéro de sécurité

- numero de securite

- kreditkartenprüfnummer

- kreditkartenprufnummer

- prüfziffer

- prufziffer

- сичерхеитс коде
- sicherheitscode

- sicherheitsnummer

- verfalldatum

- codice di verifica

- cod. sicurezza

- сикурезза наложенного платежа
- 
n autorizzazione
- código

- codigo

- cod. seg

- СЕГ наложенного платежа
- código de segurança

- codigo de seguranca

- codigo de segurança

- código de seguranca

- cód. segurança

- наложен. сегуранка наложенный платеж. сегуранçа
- cód. seguranca

- кóд сегуранçа
- наложенный на наложенный сегуранка сегуранçа
- кóд сегуранка
- número de verificação

- numero de verificacao

- ablauf

- gültig bis

- gültigkeitsdatum

- gultig bis

- gultigkeitsdatum

- scadenza

- data scad

- fecha de expiracion

- fecha de venc

- vencimiento

- válido hasta

- valido hasta

- vto

- data de expiração

- data de expiracao

- data em que expira

- validade

- valor

- vencimento

- Венк 

#### <a name="keywordccname"></a>Кэйворд_кк_наме

- amex
- 
american express
- americanexpress

- Visa
- mastercard

- master card

- 
mc
 
- mastercards
- 
master cards
- Клуб Динер
- diners club

- dinersclub

- discover card

- discovercard

- discover cards

- JCB
- japanese card bureau

- carte blanche

- carteblanche

- credit card

- Центральной
- CC #:
- 
expiration date
- exp date

- 
expiry date
- 
date d’expiration
- 
date d'exp
- 
date expiration
- bank card

- 
bankcard
- card number

- card num

- cardnumber

- cardnumbers

- card numbers

- creditcard

- credit cards

- creditcards

- ccn

- card holder

- cardholder

- card holders

- cardholders

- check card

- checkcard

- check cards

- checkcards

- debit card

- debitcard

- debit cards

- debitcards

- atm card

- atmcard

- atm cards

- atmcards

- 
enroute
- 
en route
- card type

- carte bancaire

- carte de crédit

- carte de credit

- numéro de carte

- numero de carte

- nº de la carte

- nº de carte

- kreditkarte

- karte

- karteninhaber

- karteninhabers
- kreditkarteninhaber

- kreditkarteninstitut

- kreditkartentyp

- eigentümername

- 
kartennr
 
- kartennummer
- 
kreditkartennummer
- кредиткартен — нуммер
- carta di credito

- carta credito

- Корзина "
- n корзина
- nr. carta

- нрная корзина
- numero carta

- numero della carta

- numero di carta

- tarjeta credito

- tarjeta de credito

- 
tarjeta crédito
- 
tarjeta de crédito
- tarjeta de atm

- tarjeta atm

- tarjeta debito

- tarjeta de debito

- 
tarjeta débito
- 
tarjeta de débito
- nº de tarjeta

- no. de tarjeta

- нет де таржета
- numero de tarjeta

- número de tarjeta

- tarjeta no

- tarjetahabiente

- cartão de crédito

- cartão de credito

- cartao de crédito

- cartao de credito

- cartão de débito

- cartao de débito

- cartão de debito

- cartao de debito

- débito automático
- debito automatico

- 
número do cartão
- 
numero do cartão
 
- número do cartao
- 
numero do cartao
- número de cartão

- numero de cartão

- número de cartao

- numero de cartao

- n º Do картãо
- nº do cartao

- nº. do cartão

- не выполнять картãо
- не выполнять картао
- no. do cartão

- 
no. do cartao
 
   
## <a name="croatia-identity-card-number"></a>	Номер удостоверения личности для Хорватии

### <a name="format"></a>Формат

Девять цифр.

### <a name="pattern"></a>Шаблон

Девять последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_croatia_id_card находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_croatia_id_card.

```
<!--Croatia Identity Card Number-->
<Entity id="ff12f884-c20a-4189-b185-34c8e7258d47" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Func_croatia_id_card"/>
     <Match idRef="Keyword_croatia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordcroatiaidcard"></a>Кэйворд_кроатиа_ид_кард

- Croatian identity card
- Osobna iskaznica

   
## <a name="croatia-personal-identification-oib-number"></a>	Индивидуальный идентификационный номер (OIB) для Хорватии

### <a name="format"></a>Формат

11 разрядов

### <a name="pattern"></a>Шаблон

11 цифр:
- 10 цифр. 
- Последняя цифра — контрольная цифра для международного обмена данными, буквы добавляются до одиннадцати цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_croatia_oib_number;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_croatia_oib_number находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordcroatiaoibnumber"></a>Кэйворд_кроатиа_оиб_нумбер

- Personal Identification Number
- Osobni identifikacijski broj
 
- OIB
 

   
## <a name="czech-personal-identity-number"></a>Номер личного удостоверения для чешского языка

### <a name="format"></a>Формат

Девять цифр с необязательной косой чертой (старый формат) 10 цифрами с необязательной косой чертой (новый формат)

### <a name="pattern"></a>Шаблон

Девять цифр (старый формат):
- девять цифр.

ИЛИ

- Шесть цифр, представляющих дату рождения
- косая черта;
- Три цифры

10 цифр (новый формат):
- 10 цифр.

ИЛИ

- Шесть цифр, представляющих дату рождения
- косая черта; 
- Четыре цифры, где последняя цифра является контрольной цифрой

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_кзеч_ид_кард находит содержимое, которое соответствует шаблону; Найдено ключевое слово из Кэйворд_кзеч_ид_кард. Контрольная сумма проходит проверку.

```
<!-- Czech Personal Identity Number -->
<Entity id="60c0725a-4eb6-455b-9dda-05d8a7396497"      patternsProximity="300" recommendedConfidence="85">
   <Pattern confidenceLevel="85">
      <IdMatch idRef="Func_czech_id_card" />
      <Match idRef="Keyword_czech_id_card" />
   </Pattern>
</Entity>
```
### <a name="keywords"></a>Ключевые слова

- номер личного удостоверения для чешского языка
- Роднé číсло
   
## <a name="denmark-personal-identification-number"></a>	Индивидуальный идентификационный номер для Дании

### <a name="format"></a>Формат

10 цифр, содержащих дефис.

### <a name="pattern"></a>Шаблон

10 цифр:
- шесть цифр в формате ДДММГГ — дата рождения; 
- дефис; 
- четыре цифры, где последняя цифра — проверочная.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации обнаружен, если в пределах близости от 300 символов: регулярное выражение Режекс_денмарк_ид находит содержимое, которое соответствует шаблону. Найдено ключевое слово из Кэйворд_денмарк_ид. Контрольная сумма проходит проверку.

```
<!-- Denmark Personal Identification Number -->
<Entity id="6c4f2fef-56e1-4c00-8093-88d7a01cf460" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_denmark_id"/>
     <Match idRef="Keyword_denmark_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keyworddenmarkid"></a>Кэйворд_денмарк_ид

- Personal Identification Number
- CPR
- Det Centrale Personregister
- Personnummer
   
## <a name="drug-enforcement-agency-dea-number"></a>Номер Управления по борьбе с наркотиками США (DEA)

### <a name="format"></a>Формат

Две буквы, за которыми следуют семь цифр.

### <a name="pattern"></a>Шаблон

Шаблон должен включать в себя все указанные ниже элементы.
- Одна буква (без учета регистра) из следующего набора: abcdefghjklmnprstux, представляющая собой код регистрирующегося лица 
- Одна буква (без учета регистра), представляющая собой первую букву фамилии регистрирующегося лица 
- Семь цифр, последняя из которых — контрольная

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_dea_number находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
<!-- DEA Number -->
<Entity id="9a5445ad-406e-43eb-8bd7-cac17ab6d0e4" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_dea_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

Нет

   
## <a name="eu-debit-card-number"></a>Номер банковской карты для ЕС

### <a name="format"></a>Формат

16 цифр.

### <a name="pattern"></a>Шаблон

Очень сложный и надежный шаблон.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_eu_debit_card находит содержимое, которое соответствует шаблону.
- Верно по меньшей мере одно из условий ниже:
    - найдено ключевое слово из Keyword_eu_debit_card;
    - найдено ключевое слово из Keyword_card_terms_dict;
    - найдено ключевое слово из Keyword_card_security_terms_dict;
    - найдено ключевое слово из Keyword_card_expiration_terms_dict;
    - функция Func_expiration_date находит дату в правильном формате.
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordeudebitcard"></a>Кэйворд_еу_дебит_кард

- номер счета 
- card number
 
- card no.
 
- security number
 
- Центральной 

#### <a name="keywordcardtermsdict"></a>Кэйворд_кард_термс_дикт

- acct nbr
 
- acct num
 
- acct no
 
- american express
 
- americanexpress
 
- americano espresso
 
- amex 
- atm card
 
- atm cards
 
- atm kaart
 
- atmcard
 
- atmcards
 
- atmkaart
 
- atmkaarten
 
- bancontact
 
- bank card
 
- bankkaart
 
- card holder
 
- card holders
 
- card num
 
- card number
 
- card numbers
 
- card type
 
- cardano numerico
 
- cardholder
 
- cardholders
 
- cardnumber
 
- cardnumbers
 
- carta bianca
 
- carta credito
 
- carta di credito
 
- cartao de credito
 
- cartao de crédito
 
- cartao de debito
 
- cartao de débito
 
- carte bancaire
 
- carte blanche
 
- carte bleue
 
- carte de credit
 
- carte de crédit
 
- carte di credito
 
- carteblanche
 
- cartão de credito
 
- cartão de crédito
 
- cartão de debito
 
- cartão de débito
 
- cb
 
- ccn
 
- check card
 
- check cards
 
- checkcard

- checkcards
 
- chequekaart
 
- cirrus
 
- cirrus-edc-maestro
 
- controlekaart
 
- controlekaarten
 
- credit card
 
- credit cards
 
- creditcard
 
- creditcards
 
- debetkaart
 
- debetkaarten
 
- debit card
 
- debit cards
 
- debitcard
 
- debitcards
 
- debito automatico
 
- diners club
 
- dinersclub
 
- Повтор 
- discover card
 
- discover cards
 
- discovercard
 
- discovercards
 
- débito automático
- 
edc
 
- eigentümername
 
- european debit card
 
- hoofdkaart
 
- hoofdkaarten
 
- in viaggio
 
- japanese card bureau
 
- japanse kaartdienst
 
- jcb
 
- kaart
 
- kaart num
 
- kaartaantal
 
- kaartaantallen
 
- kaarthouder
 
- kaarthouders
 
- karte
  
- karteninhaber
 
- karteninhabers
- 
kartennr
 
- kartennummer 
- kreditkarte
 
- кредиткартен — нуммер 
- kreditkarteninhaber
 
- kreditkarteninstitut
 
- kreditkartennummer
 
- kreditkartentyp
 
- maestro
 
- master card
 
- master cards
 
- mastercard
 
- mastercards 
- MC 
- mister cash
 
- n корзина 
- Корзина " 
- нет де таржета 
- не выполнять картао 
- не выполнять картãо 
- no. de tarjeta
 
- no. do cartao
 
- no. do cartão
 
- нрная корзина 
- nr. carta
 
- numeri di scheda
 
- numero carta
 
- numero de cartao
 
- numero de carte
 
- numero de cartão
 
- numero de tarjeta

- numero della carta
 
- numero di carta
 
- numero di scheda
 
- numero do cartao
 
- numero do cartão
 
- numéro de carte
 
- nº carta
 
- nº de carte
 
- nº de la carte
 
- nº de tarjeta
 
- nº do cartao
 
- n º Do картãо 
- nº. do cartão
 
- número de cartao
 
- número de cartão
 
- número de tarjeta
 
- número do cartao 
- scheda dell'assegno
 
- scheda dell'atmosfera
 
- scheda dell'atmosfera
 
- scheda della banca
 
- scheda di controllo
 
- scheda di debito
 
- scheda matrice
 
- schede dell'atmosfera
 
- schede di controllo
 
- schede di debito
 
- schede matrici
 
- scoprono la scheda
 
- scoprono le schede
 
- solo
 
- supporti di scheda
 
- supporto di scheda
 
- ключ 
- tarjeta atm
 
- tarjeta credito
 
- tarjeta de atm
 
- tarjeta de credito
 
- tarjeta de debito
 
- tarjeta debito
 
- tarjeta no

- tarjetahabiente
 
- tipo della scheda
 
- ufficio giapponese della 
- scheda
 
- v pay
 
- v — оплата 
- visa
 
- visa plus
 
- visa electron
 
- visto
 
- visum
 
- vpay
   

#### <a name="keywordcardsecuritytermsdict"></a>Кэйворд_кард_секурити_термс_дикт

- card identification number
- card verification 
- cardi la verifica
 
- cid
 
- СЕГ наложенного платежа 
- сегуранка наложенного платежа 
- сегуранçа наложенного платежа 
- сикурезза наложенного платежа 
- cod. seg
 
- cod. seguranca
 
- cod. segurança
 
- cod. sicurezza
 
- codice di sicurezza
 
- codice di verifica
 
- codigo
 
- codigo de seguranca
 
- codigo de segurança
 
- crittogramma
 
- cryptogram
 
- cryptogramme
 
- CV2 
- cvc
 
- CVC2 
- cvn
 
- cvv
 
- CVV2 
- кóд сегуранка 
- кóд сегуранçа 
- cód. seguranca
 
- cód. segurança
 
- código
 
- código de seguranca
 
- código de segurança
 
- de kaart controle
 
- geeft nr uit
 
- issue no
 
- issue number
 
- kaartidentificatienummer
 
- kreditkartenprufnummer
 
- kreditkartenprüfnummer
 
- kwestieaantal
 
- no. dell'edizione
 
- no. di sicurezza
 
- numero de securite
 
- numero de verificacao
 
- numero dell'edizione
 
- numero di identificazione della 
- scheda
 
- numero di sicurezza
 
- numero van veiligheid
 
- numéro de sécurité
 
- nº autorizzazione
 
- número de verificação
 
- perno il blocco
 
- pin block
 
- prufziffer
 
- prüfziffer
 
- security code
 
- security no
 
- security number
 
- sicherheits kode
 
- sicherheitscode
 
- sicherheitsnummer
 
- speldblok
 
- veiligheid nr
 
- veiligheidsaantal
 
- veiligheidscode
 
- veiligheidsnummer
 
- verfalldatum
 

#### <a name="keywordcardexpirationtermsdict"></a>Кэйворд_кард_експиратион_термс_дикт

- ablauf
 
- data de expiracao
 
- data de expiração
 
- data del exp
 
- data di exp
 
- data di scadenza
 
- data em que expira
 
- data scad
 
- data scadenza
 
- date de validité
 
- datum afloop
 
- datum van exp
 
- de afloop
 
- espira
 
- espira
 
- exp date
 
- exp datum
 
- срока действия 
- expire
 
- expires
 
- expiry
 
- fecha de expiracion
 
- fecha de venc
 
- gultig bis
 
- gultigkeitsdatum
 
- gültig bis
 
- gültigkeitsdatum
 
- la scadenza
 
- scadenza
 
- valable
 
- validade
 
- valido hasta
 
- valor
 
- venc
 
- vencimento
 
- vencimiento
 
- verloopt
 
- vervaldag
 
- vervaldatum
 
- vto
 
- válido hasta
 
   
## <a name="eu-drivers-license-number"></a>Номер водительского удостоверения для драйвера ЕС

Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации номера лицензии для драйвера ЕС](eu-driver-s-license-number.md).
  
## <a name="eu-national-identification-number"></a>Национальный идентификационный номер ЕС

Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для национального идентификационНого номера ЕС](eu-national-identification-number.md).
  
## <a name="eu-passport-number"></a>Номер паспорта ЕС

Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации о номере паспорта ЕС](eu-passport-number.md).
  
## <a name="eu-social-security-number-or-equivalent-id"></a>Номер социального страхования ЕС или эквивалентный идентификатор

Чтобы узнать больше, ознакомьтесь со статьей [номер социального страхования ЕС или эквивалентный тип конфиденциальной информации ID](eu-social-security-number-or-equivalent-id.md).
  
## <a name="eu-tax-identification-number"></a>Идентификационный номер налогоплательщика ЕС

Чтобы узнать больше, ознакомьтесь со статьей [тип конфиденциальной информации для налогОвого кода ЕС](eu-tax-identification-number.md).
  
## <a name="finland-national-id"></a>Национальный идентификатор, Финляндия

### <a name="format"></a>Формат

Шесть цифр, а также символ, обозначающий век, три цифры и контрольная цифра.

### <a name="pattern"></a>Шаблон

Шаблон должен включать в себя все указанные ниже элементы.
- Шесть цифр в формате ДДММГГ, представляющие собой дату рождения 
- Маркер века (символы "-" и "+" или буква "a") 
- Трехзначный личный идентификационный номер 
- Цифра или буква (без учета регистра) — проверочная.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_finnish_national_id находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_finnish_national_id;
- Контрольная сумма проходит проверку.

```
<!-- Finnish National ID-->
<Entity id="338FD995-4CB5-4F87-AD35-79BD1DD926C1" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finnish_national_id" />
          <Match idRef="Keyword_finnish_national_id" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

- Кэйворд_финниш_натионал_ид
- 

Sosiaaliturvatunnus
- SOTU Henkilötunnus HETU
- Personbeteckning
- Personnummer
   
## <a name="finland-passport-number"></a>Номер паспорта для Финляндии

Комбинация, состоящая из девяти букв и цифр, комбинация из девяти букв и цифр: две буквы (без учета регистра) семь цифр контрольная сумма нет определения политика защиты от потери данных — 75% уверенности в том, что этот тип конфиденциальной информации определен, если в близость от 300 символов: регулярное выражение Режекс_финланд_пасспорт_нумбер находит содержимое, которое соответствует шаблону. Найдено ключевое слово из Кэйворд_финланд_пасспорт_нумбер. Ключевые слова <!-- Finland Passport Number --> 
 <Entity id="d1685ac3-1d3a-40f8-8198-32ef5669c7a5" recommendedConfidence="75" patternsProximity="300"> <Pattern confidenceLevel="75"> <IdMatch idRef="Regex_finland_passport_number"/> <Match idRef="Keyword_finland_passport_number"/> </Pattern> 
 </Entity>
   
## <a name="france-drivers-license-number"></a>Номер водительского удостоверения для Франции

### <a name="format"></a>Формат

12 цифр.

### <a name="pattern"></a>Шаблон

12 цифр с проверкой подлинности, чтобы избежать путаницы с похожими шаблонами, например французскими номерами телефонов.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_french_drivers_license находит содержимое, которое соответствует шаблону.
- Верно по меньшей мере одно из условий ниже:
- найдено ключевое слово из Keyword_french_drivers_license;
- функция Func_eu_date находит дату в правильном формате.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordfrenchdriverslicense"></a>Кэйворд_френч_дриверс_лиценсе

- drivers licence
- drivers license
- driving licence

- Управление лицензией
- 
permis de conduire
- 
licence number
- 
license number
- 
licence numbers
- 

license numbers

## <a name="france-national-id-card-cni"></a>Номер внутреннего удостоверения личности для Франции (CNI)

### <a name="format"></a>Формат

12 цифр.

### <a name="pattern"></a>Шаблон

12 цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- регулярное выражение Regex_france_cni находит содержимое, которое соответствует шаблону.

```
<!-- France CNI -->
<Entity id="f741ac74-1bc0-4665-b69b-f0c7f927c0c4" patternsProximity="300" recommendedConfidence="65">
  <Pattern confidenceLevel="65">
        <IdMatch idRef="Regex_france_cni" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

Нет
   
## <a name="france-passport-number"></a>Номер паспорта гражданина Франции

### <a name="format"></a>Формат

Девять цифр и букв.

### <a name="pattern"></a>Шаблон

Девять цифр и букв
- Две цифры 
- Две буквы (без учета регистра) 
- Пять цифр

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_fr_passport находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_passport.

```
<!-- France Passport Number -->
<Entity id="3008b884-8c8c-4cd8-a289-99f34fc7ff5d" patternsProximity="300" recommendedConfidence="75">
  <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_fr_passport" />
        <Match idRef="Keyword_passport" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordpassport"></a>Кэйворд_пасспорт

- Passport Number
- 
Passport No
- Passport#

- Passport#

- Пасспортид
- Passportno

- passportnumber

- パスポート
- パスポート番号

- パスポートのNum

- 
パスポート＃
 
- Numéro de passeport
- 
Passeport n °
- Passeport Non

- Passeport#

- Passeport#

- Пассепортнон
- 

Passeportn °

      
## <a name="france-social-security-number-insee"></a>Страховой номер для Франции (INSEE)

### <a name="format"></a>Формат

15 цифр.

### <a name="pattern"></a>Шаблон

Должен соответствовать одному из двух шаблонов:
- 13 цифр, за которыми следует пробел, за которым следуют две цифры.<br/>
или
- 15 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.
- находится ключевое слово из Keyword_fr_insee;
- Контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Функ_френч_инси или Функ_фр_инси находит содержимое, которое соответствует шаблону.
- ни одно ключевое слово из Keyword_fr_insee не находится;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordfrinsee"></a>Кэйворд_фр_инси

- insee
- 
securité sociale
- 
securite sociale
- 
national id
- 
national identification
- 
numéro d'identité
- нет д'идентитé
- 
no. d'identité
- 
numero d'identite
- нет д'идентите
- 
no. d'identite
- social security number

- 
social security code
- social insurance number
- 
le numéro d'identification nationale
- 
d'identité nationale
- 
numéro de sécurité sociale
- 
le code de la sécurité sociale
- 
numéro d'assurance sociale
- 
numéro de sécu
- 
code sécu
 
   
## <a name="german-drivers-license-number"></a>Номер водительского удостоверения для Германии

### <a name="format"></a>Формат

Сочетание 11 цифр и букв.

### <a name="pattern"></a>Шаблон

11 цифр и букв (без учета регистра)
- цифра или буква;  
- Две цифры 
- Шесть цифр или букв 
- Одна цифра 
- Одна цифра или буква

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_german_drivers_license находит содержимое, которое соответствует шаблону;
- Верно по меньшей мере одно из условий ниже:
    - найдено ключевое слово из Keyword_german_drivers_license_number;
    - найдено ключевое слово из Keyword_german_drivers_license_collaborative;
    - найдено ключевое слово из Keyword_german_drivers_license;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordgermandriverslicensenumber"></a>Кэйворд_жерман_дриверс_лиценсе_нумбер

- Führerschein
- 
Fuhrerschein
- Фуехрерсчеин
- 
Führerscheinnummer
- 
Fuhrerscheinnummer
- 
Fuehrerscheinnummer
- 
Führerschein-
 
- Fuhrerschein-
 
- Fuehrerschein-
 
- Фüхрерсчеиннуммернр
- Фухрерсчеиннуммернр
- Фуехрерсчеиннуммернр
- Фüхрерсчеиннуммерклассе
- Фухрерсчеиннуммерклассе
- Фуехрерсчеиннуммерклассе
- Führerschein- Nr

- Fuhrerschein- Nr

- Fuehrerschein- Nr
 
- Führerschein- Klasse
 
- Fuhrerschein- Klasse
 
- Fuehrerschein- Klasse
- Фüхрерсчеиннуммернр 
- Фухрерсчеиннуммернр 
- Фуехрерсчеиннуммернр 
- Фüхрерсчеиннуммерклассе 
- Фухрерсчеиннуммерклассе 
- Фуехрерсчеиннуммерклассе 
- Führerschein- Nr
 
- Fuhrerschein- Nr
 
- Fuehrerschein- Nr
 
- Führerschein- Klasse
 
- Fuhrerschein- Klasse
 
- Fuehrerschein- Klasse 
- DL 
- DLS
- 
Driv Lic
 
- Driv Licen
 
- Driv License
- 
Driv Licenses
 
- Driv Licence
 
- Driv Licences
 
- Driv Lic
 
- Driver Licen
 
- Лицензия на драйвер 
- Лицензии на драйверы 
- Driver Licence
 
- Driver Licences
 
- Драйверы Лик 
- Драйверы лицен 
- Лицензия на драйверы 
- Лицензии на драйверы 
- Лицензия на драйверы 
- Лицензии на драйверы 
- Лик драйвера 
- Driver's Licen
 
- Лицензия на драйвер 
- Лицензии на драйвер 
- Driver's Licence
 
- Driver's Licences
 
- Driving Lic
 
- Driving Licen
 
- Driving License
 
- Driving Licenses
 
- Driving Licence

 
- Driving Licences

#### <a name="keywordgermandriverslicensecollaborative"></a>Кэйворд_жерман_дриверс_лиценсе_коллаборативе

- 
Nr-Führerschein
 
- Nr-Fuhrerschein
 
- Nr-Fuehrerschein
 
- No-Führerschein
 
- No-Fuhrerschein
 
- No-Fuehrerschein
 
- N-Führerschein
 
- N-Fuhrerschein
 
- N-Fuehrerschein
- 
Nr-Führerschein
 
- Nr-Fuhrerschein
 
- Nr-Fuehrerschein
 
- No-Führerschein
 
- No-Fuhrerschein
 
- No-Fuehrerschein
 
- N-Führerschein
 
- N-Fuhrerschein
 
- N-Fuehrerschein 

#### <a name="keywordgermandriverslicense"></a>Кэйворд_жерман_дриверс_лиценсе

- ausstellungsdatum
- 
ausstellungsort
- 
ausstellende behöde
- 
ausstellende behorde
- 

ausstellende behoerde
   
## <a name="german-passport-number"></a>Номер паспорта гражданина Германии

### <a name="format"></a>Формат

10 цифр или букв.

### <a name="pattern"></a>Шаблон

Шаблон должен включать в себя все указанные ниже элементы.
- Первый символ — цифра или буква из следующего набора: C, F, G, H, J, K. 
- Три цифры 
- Пять цифр или букв из следующего набора: C, F-H, J-N, P, R, T, V-Z 
- Одна цифра

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_german_passport находит содержимое, которое соответствует шаблону;
- находится любое ключевое слово из пяти соответствующих списков;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_german_passport_data находит содержимое, которое соответствует шаблону;
- находится любое ключевое слово из пяти соответствующих списков;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordgermanpassport"></a>Кэйворд_жерман_пасспорт

- reisepass
- 
reisepasse
- 
reisepassnummer
- passport
- 

passports

#### <a name="keywordgermanpassportcollaborative"></a>Кэйворд_жерман_пасспорт_коллаборативе

- geburtsdatum
- ausstellungsdatum
- 
ausstellungsort

#### <a name="keywordgermanpassportnumber"></a>Кэйворд_жерман_пасспорт_нумбер

No — Реисепасс НР — Реисепасс

#### <a name="keywordgermanpassport1"></a>Keyword_german_passport1

Reisepass-Nr


#### <a name="keywordgermanpassport2"></a>Keyword_german_passport2

бнатионалит. t
   
## <a name="germany-identity-card-number"></a>Номер идентификационной карты гражданина Германии

### <a name="format"></a>Формат

С 1 ноября 2010: девять букв и цифр

От 1 апреля 1987 до 31 октября 2010:10 цифр.

### <a name="pattern"></a>Шаблон

С 1 ноября 2010 г.:
- Одна буква (без учета регистра) 
- восемь цифр.

От 1 апреля 1987 до 31 октября 2010:
- 10 цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- регулярное выражение Regex_germany_id_card находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_germany_id_card.

```
<!-- Germany Identity Card Number -->
<Entity id="e577372f-c42e-47a0-9d85-bebed1c237d4" recommendedConfidence="65" patternsProximity="300">
  <Pattern confidenceLevel="65">
     <IdMatch idRef="Regex_germany_id_card"/>
     <Match idRef="Keyword_germany_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordgermanyidcard"></a>Кэйворд_жермани_ид_кард

- Identity Card
- ID
- Identification
- Personalausweis
- Identifizierungsnummer
- Ausweis
- Identifikation
   
## <a name="greece-national-id-card"></a>Номер внутреннего удостоверения личности для Греции

### <a name="format"></a>Формат

Сочетание 7–8 букв и чисел, а также тире.

### <a name="pattern"></a>Шаблон

Семь букв и чисел (старый формат):
- одна буква (любая буква греческого алфавита); 
- Тире 
- шесть цифр.

Восемь букв и чисел (новый формат):
- две буквы, которые в прописном виде есть как в греческом, так и латинском алфавите (ABEZHIKMNOPTYX); 
- Тире 
- шесть цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_greece_id_card находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_greece_id_card.

```
<!-- Greece National ID Card -->
<Entity id="82568215-1da1-46d3-874a-d2294d81b5ac" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_greece_id_card"/>
     <Match idRef="Keyword_greece_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordgreeceidcard"></a>Кэйворд_грице_ид_кард

- Greek identity Card
- Tautotita
- Δελτίο αστυνομικής ταυτότητας
- Ταυτότητα
   
## <a name="hong-kong-identity-card-hkid-number"></a>Номер удостоверения личности для Гонконга (HKID)

### <a name="format"></a>Формат

Сочетание 8–9 букв и чисел, а также необязательные скобки вокруг последнего символа.

### <a name="pattern"></a>Шаблон

Сочетание 8–9 букв:
- 1–2 буквы (без учета регистра); 
- Шесть цифр 
- последний символ (любая цифра или буква "A") является проверочной цифрой и заключен в скобки (необязательно).

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_hong_kong_id_card;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- функция Func_hong_kong_id_card находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordhongkongidcard"></a>Кэйворд_хонг_конг_ид_кард

- идентификационная карточка Гонконг
- ХКИДК
- идентификационная карточка
- identity card
- идентификационная карточка HK
- Идентификатор Гонконг
- 香港身份證

- 香港永久性居民身份證

- 身份證

- 身份証
- 身分證 
- 身分証
- 香港身份証
- 香港身分證
- 香港身分証
- 香港身份證

- 香港居民身份證
- 香港居民身份証
- 香港居民身分證
- 香港居民身分証
- 香港永久性居民身份証
- 香港永久性居民身分證
- 香港永久性居民身分証
- 香港永久性居民身份證

- 香港非永久性居民身份證
- 香港非永久性居民身份証
- 香港非永久性居民身分證
- 香港非永久性居民身分証
- 香港特別行政區永久性居民身份證
- 香港特別行政區永久性居民身份証
- 香港特別行政區永久性居民身分證
- 香港特別行政區永久性居民身分証
- 香港特別行政區非永久性居民身份證
- 香港特別行政區非永久性居民身份証
- 香港特別行政區非永久性居民身分證
- 香港特別行政區非永久性居民身分証
   
## <a name="india-permanent-account-number-pan"></a>Идентификационный номер налогоплательщика для Индии (PAN)

### <a name="format"></a>Формат

10 букв или цифр.

### <a name="pattern"></a>Шаблон

10 букв или цифр:
- пять букв (без учета регистра); 
- Четыре цифры 
- буква, которая является алфавитным проверочным символом.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_india_permanent_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_india_permanent_account_number;
- Контрольная сумма проходит проверку.

```
<!-- India Permanent Account Number -->
<Entity id="2602bfee-9bb0-47a5-a7a6-2bf3053e2804" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_india_permanent_account_number"/>
     <Match idRef="Keyword_india_permanent_account_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordindiapermanentaccountnumber"></a>Кэйворд_индиа_перманент_аккаунт_нумбер

- Permanent Account Number
 
- PAN
 
   
## <a name="india-unique-identification-aadhaar-number"></a>Индивидуальный идентификационный номер (Aadhaar) для Индии

### <a name="format"></a>Формат

12 цифр, содержащих необязательные пробелы или тире.

### <a name="pattern"></a>Шаблон

12 цифр:
- четыре цифры; 
- необязательный пробел или тире; 
- четыре цифры; 
- необязательный пробел или тире; 
- последняя цифра — проверочная.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных — 85% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону; Найдено ключевое слово из Кэйворд_индиа_аадхар. Контрольная сумма проходит проверку. Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_индиа_аадхаар находит содержимое, которое соответствует шаблону; Контрольная сумма проходит проверку. <!-- India Unique Identification (Aadhaar) number -->
<Entity id="1ca46b29-76f5-4f46-9383-cfa15e91048f" recommendedConfidence="85" patternsProximity="300"> <Pattern confidenceLevel="85"> <IdMatch idRef="Func_india_aadhaar"/> <Match idRef="Keyword_india_aadhar"/> </Pattern> <Pattern confidenceLevel="75"> <IdMatch idRef="Func_india_aadhaar"/> </Pattern>
</Entity>

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordindiaaadhar"></a>Кэйворд_индиа_аадхар
- Aadhar
- Aadhaar
- UID
- आधार
   
## <a name="indonesia-identity-card-ktp-number"></a>Номер удостоверения личности (KTP) для Индонезии

### <a name="format"></a>Формат

16 цифр, содержащих необязательные точки.

### <a name="pattern"></a>Шаблон

16 цифр:
- две цифры (код провинции); 
- точка (необязательно); 
- две цифры (код округа или города); 
- две цифры (код района); 
- точка (необязательно); 
- шесть цифр в формате ДДММГГ (дата рождения); 
- точка (необязательно); 
- Четыре цифры

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.
- находится ключевое слово из Keyword_indonesia_id_card.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_indonesia_id_card находит содержимое, которое соответствует шаблону.

```
<!-- Indonesia Identity Card (KTP) Number -->
<Entity id="da68fdb0-f383-4981-8c86-82689d3b7d55" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_indonesia_id_card"/>
     <Match idRef="Keyword_indonesia_id_card"/>
  </Pattern>
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_indonesia_id_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordindonesiaidcard"></a>Кэйворд_индонесиа_ид_кард

- KTP
- Kartu Tanda Penduduk
 
- Nomor Induk Kependudukan
 
   
## <a name="international-banking-account-number-iban"></a>Международный номер банковского счета (IBAN)

### <a name="format"></a>Формат

Код страны (две буквы), а также проверочные цифры (две) и номер bban (до 30 символов)

### <a name="pattern"></a>Шаблон

Шаблон должен включать в себя все указанные ниже элементы.

- Двухбуквенный код страны
- Две проверочные цифры (после которых может следовать пробел)  
- 1–7 групп из четырех букв или цифр (могут разделяться пробелами)
- 1–3 буквы или цифры

Формат для названия каждой из стран немного отличается. Тип конфиденциальной информации IBAN применяется к следующим 60 странам:

ad, ae, al, at, az, ba, be, bg, bh, ch, cr, cy, cz, de, dk, do, ee, es, fi, fo, fr, gb, ge, gi, gl, gr, hr, hu, ie, il, is, it, kw, kz, lb, li, lt, lu, lv, mc, md, me, mk, mr, mt, mu, nl, no, pl, pt, ro, rs, sa, se, si, sk, sm, tn, tr, vg

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_iban находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
<Entity id="e7dc4711-11b7-4cb0-b88b-2c394a771f0e" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_iban" />
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

Нет

   
## <a name="ip-address"></a>IP-адрес

### <a name="format"></a>Формат

#### <a name="ipv4"></a>IPv4:
Сложный шаблон, ответственный за форматированные (с точками) и неформатированные (без точек) версии IPv4-адресов.

#### <a name="ipv6"></a>Протокол IPv6
 Сложный шаблон, ответственный за форматированные номера IPv6 (вместе с двоеточиями).

### <a name="pattern"></a>Шаблон

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;
- ни одно ключевое слово из Keyword_ipaddress не находится.

В случае с протоколом IPv4 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- регулярное выражение Regex_ipv4_address находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_ipaddress.

В случае с протоколом IPv6 политика защиты от потери данных с вероятностью в 95 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- регулярное выражение Regex_ipv6_address находит содержимое, которое соответствует шаблону;
- Не обнаружено ключевых слов из списка Keyword_ipaddress.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordipaddress"></a>Кэйворд_ипаддресс

- IP (ключевое слово с учетом регистра)
- ip address
 
- ip addresses
- internet protocol
- 
IP-כתובת ה
 
   
## <a name="international-classification-of-diseases-icd-10-cm"></a>Международная классификация Diseases (ICD-10-CM)

### <a name="format"></a>Формат

Словаря

### <a name="pattern"></a>Шаблон

Недопустим

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Найдено ключевое слово из Dictionary_icd_10_cm.

```
      <!-- ICD-10 CM -->
      <Entity id="3356946c-6bb7-449b-b253-6ffa419c0ce7" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_10_cm" />
        </Pattern>
      </Entity>
```

Ключевые слова

Любой термин из словаря ключевых слов Dictionary_icd_10_cm, основанный на [международной классификации Diseases, десятОй редакции Клиникал модификации (ICD-10-cm)](https://go.microsoft.com/fwlink/?linkid=852604). Этот тип ищет только термин, а не коды страхования.

   
## <a name="international-classification-of-diseases-icd-9-cm"></a>Международная классификация Diseases (ICD-9-CM)

### <a name="format"></a>Формат

Словаря

### <a name="pattern"></a>Шаблон

Недопустим

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Найдено ключевое слово из Dictionary_icd_9_cm.

```
      <Entity id="fa3f9c74-ee07-4c52-b5f2-085d6b2c0ec4" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Dictionary_icd_9_cm" />
        </Pattern>
      </Entity>
```

### <a name="keywords"></a>Ключевые слова

Любой термин из словаря ключевых слов Dictionary_icd_9_cm, основанный на [международной классификации Diseases, девятОй редакции, Клиникал модификации (ICD-9-cm)](https://go.microsoft.com/fwlink/?linkid=852605). Этот тип ищет только термин, а не коды страхования.
   
## <a name="ireland-personal-public-service-pps-number"></a>Индивидуальный социальный номер (PPS) для Ирландии

### <a name="format"></a>Формат

Старый формат (до 31 декабря 2012):
- семь цифр, за которыми следуют 1–2 буквы.  

Новый формат (1 января 2013 и после):
- семь цифр, за которыми следуют две буквы.

### <a name="pattern"></a>Шаблон

Старый формат (до 31 декабря 2012):
- семь цифр; 
- 1–2 буквы (без учета регистра). 

Новый формат (1 января 2013 и после):
- семь цифр; 
- буква (без учета регистра), которая является алфавитным проверочным символом; 
- буква "A" или "H" (без учета регистра).

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_ireland_pps находит содержимое, которое соответствует шаблону.
- Верно одно из условий ниже:
    - найдено ключевое слово из Keyword_ireland_pps;
    - функция Func_eu_date находит дату в правильном формате.
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- функция Func_ireland_pps находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordirelandpps"></a>Кэйворд_иреланд_ппс

- Personal Public Service Number 
 
- PPS Number
 
- PPS Num
 
- PPS No.
 
- PPS #
 
- PPS 
- PPSN
 
- Public Services Card
 
- Uimhir Phearsanta Seirbhíse Poiblí
 
- Uimh. PSP
 
- PSP
 
   
## <a name="israel-bank-account-number"></a>Номер банковского счета для Израиля

### <a name="format"></a>Формат

13 цифр.

### <a name="pattern"></a>Шаблон

С форматированием
- Две цифры 
- Тире 
- три цифры;  
- Тире 
- восемь цифр.

Без форматирования
- 	13 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_israel_bank_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_israel_bank_account_number.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordisraelbankaccountnumber"></a>Кэйворд_исраел_банк_аккаунт_нумбер

- Bank Account Number
 
- Bank Account
 
- Account Number
 
- מספר חשבון בנק
 
   
## <a name="israel-national-id"></a>Национальный идентификатор для Израиля

### <a name="format"></a>Формат

Девять цифр.

### <a name="pattern"></a>Шаблон

Девять последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_israeli_national_id_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_Israel_National_ID;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordisraelnationalid"></a>Кэйворд_исраел_натионал_ид

- מספר זהות
 
- National ID Number
   
## <a name="italy-drivers-license-number"></a>Номер водительского удостоверения для Италии

### <a name="format"></a>Формат

Сочетание из 10 букв и цифр.

### <a name="pattern"></a>Шаблон

- Сочетание 10 букв и цифр.
- одна буква (без учета регистра);  
- Буква "A" или "V" (без учета регистра) 
- Семь букв (без учета регистра), цифр или символов подчеркивания 
- Одна буква (без учета регистра)

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_italy_drivers_license_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_italy_drivers_license_number.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keyworditalydriverslicensenumber"></a>Кэйворд_итали_дриверс_лиценсе_нумбер

- numero di patente di guida
 
- patente di guida
 
   
## <a name="japan-bank-account-number"></a>Номер банковского счета для Японии

### <a name="format"></a>Формат

Семь или восемь цифр.

### <a name="pattern"></a>Шаблон

Номер банковского счета:
- семь или восемь цифр.
- Код филиала для банковского счета.
- Четыре цифры 
- Пробел или тире (необязательно) 
- три цифры.

Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_jp_bank_account находит содержимое, которое соответствует шаблону.
- Находится ключевое слово из Keyword_jp_bank_account.
- Верно одно из условий ниже:
- функция Func_jp_bank_account_branch_code находит содержимое, которое соответствует шаблону;
- найдено ключевое слово из Keyword_jp_bank_branch_code.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_jp_bank_account находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_jp_bank_account.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordjpbankaccount"></a>Кэйворд_жп_банк_аккаунт

- Checking Account Number
 
- Checking Account
 
- Checking Account #
 
- Checking Acct Number
 
- Checking Acct #
 
- Checking Acct No.
 
- Checking Account No.
 
- Bank Account Number
 
- Bank Account
 
- Bank Account #
 
- Bank Acct Number
 
- Bank Acct #
 
- Bank Acct No.
 
- Bank Account No.
 
- Savings Account Number
 
- Учетная запись сбережений 
- Savings Account #
 
- Savings Acct Number
 
- Savings Acct #
 
- Savings Acct No.
 
- Savings Account No.
 
- Debit Account Number
 
- Debit Account
 
- Debit Account #
 
- Debit Acct Number
 
- Debit Acct #
 
- Debit Acct No.
 
- Debit Account No.
 
- 口座番号を当座預金口座の確認
 
- ＃アカウントの確認、勘定番号の確認
 
- ＃勘定の確認
 
- 勘定番号の確認
 
- 口座番号の確認
 
- 銀行口座番号 
- 銀行口座 
- 銀行口座＃
 
- 銀行の勘定番号
 
- 銀行のacct＃
 
- 銀行の勘定いいえ
 
- 銀行口座番号
- 
普通預金口座番号
 
- 預金口座
 
- 貯蓄口座＃
 
- 貯蓄勘定の数
 
- 貯蓄勘定＃
 
- 貯蓄勘定番号
 
- 普通預金口座番号
 
- 引き落とし口座番号
 
- 口座番号 
- 口座番号＃
 
- デビットのacct番号
 
- デビット勘定＃
 
- デビットACCTの番号
 
- デビット口座番号
 

#### <a name="keywordjpbankbranchcode"></a>Кэйворд_жп_банк_бранч_коде

Otemachi

## <a name="japan-drivers-license-number"></a>Номер водительского удостоверения для Японии

### <a name="format"></a>Формат

12 цифр.

### <a name="pattern"></a>Шаблон

12 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_jp_drivers_license_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_jp_drivers_license_number.

```
<!-- Japan Driver's License Number -->
<Entity id="c6011143-d087-451c-8313-7f6d4aed2270" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_drivers_license_number" />
        <Match idRef ="Keyword_jp_drivers_license_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordjpdriverslicensenumber"></a>Кэйворд_жп_дриверс_лиценсе_нумбер

- dl# 
- DL 
- dls# 
- БИБЛИОТЕК 
- driver license 
- driver licenses 
- drivers license 
- driver's license 
- drivers licenses 
- driver's licenses 
- driving licence
 
- lic# 
- Лик # 
- lics# 
- идентификатор состояния 
- state identification
 
- state identification number
 
- 低所得国＃
 
- 免許証 
- 状態ID
- 
状態の識別
 
- 状態の識別番号
 
- 運転免許 
- 運転免許証 
- 運転免許証番号 
   
## <a name="japan-passport-number"></a>Номер паспорта гражданина Японии

### <a name="format"></a>Формат

Две буквы, за которыми следуют семь цифр.

### <a name="pattern"></a>Шаблон

Две буквы (без учета регистра), за которыми следуют семь цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_jp_passport находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_jp_passport.

```
<!-- Japan Passport Number -->
<Entity id="75177310-1a09-4613-bf6d-833aae3743f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_passport" />
        <Match idRef="Keyword_jp_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordjppassport"></a>Кэйворд_жп_пасспорт

- パスポート
 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
   
## <a name="japan-resident-registration-number"></a>Номер регистрации резидента Японии

### <a name="format"></a>Формат

11 разрядов

### <a name="pattern"></a>Шаблон

11 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_jp_resident_registration_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_jp_resident_registration_number.

```
<!-- Japan Resident Registration Number -->
<Entity id="01c1209b-6389-4faf-a5f8-3f7e13899652" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_jp_resident_registration_number" />
        <Match idRef ="Keyword_jp_resident_registration_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordjpresidentregistrationnumber"></a>Кэйворд_жп_ресидент_регистратион_нумбер

- Resident Registration Number
- Resident Register Number
 
- Residents Basic Registry Number
 
- Resident Registration No.
 
- Resident Register No.
 
- Residents Basic Registry No.
 
- Basic Resident Register No.
 
- 住民登録番号、登録番号をレジデント
 
- 住民基本登録番号、登録番号
 
- 住民基本レジストリ番号を常駐
 
- 登録番号を常駐住民基本台帳登録番号
 

   
## <a name="japan-social-insurance-number-sin"></a>Номер карты социального страхования для Японии (SIN)

### <a name="format"></a>Формат

7–12 цифр.

### <a name="pattern"></a>Шаблон

7–12 цифр
- Четыре цифры 
- Дефис (необязательно) 
- Шесть цифр или
- 7–12 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_jp_sin находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_jp_sin.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_jp_sin_pre_1997 находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_jp_sin.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordjpsin"></a>Кэйворд_жп_син

- Social Insurance No.
 
- Social Insurance Num
 
- Social Insurance Number
 
- 社会保険のテンキー
 
- 社会保険番号
 

## <a name="japanese-residence-card-number"></a>Номер карточки для японского языка

### <a name="format"></a>Формат

12 букв и цифр

### <a name="pattern"></a>Шаблон

12 букв и цифр:
- две буквы (без учета регистра);
- восемь цифр. 
- две буквы (без учета регистра);

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Регулярное выражение Режекс_жп_ресиденце_кард_нумбер находит содержимое, которое соответствует шаблону;
- Найдено ключевое слово из Кэйворд_жп_ресиденце_кард_нумбер.

```
<!--Japan Residence Card Number-->
-<Entity id="ac36fef2-a289-4e2c-bb48-b02366e89fc0" recommendedConfidence="75" patternsProximity="300">
   -<Pattern confidenceLevel="75">
      <IdMatch idRef="Regex_jp_residence_card_number"/>
      <Match idRef="Keyword_jp_residence_card_number"/>
   </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordjpresidencecardnumber"></a>Кэйворд_жп_ресиденце_кард_нумбер

- Номер карточки проживания
- Номер карточки проживания
- Номер карточки проживания
- 在留カード番号
   
## <a name="malaysia-id-card-number"></a>Номер удостоверения личности для Малайзии

### <a name="format"></a>Формат

12 цифр, содержащих необязательные дефисы.

### <a name="pattern"></a>Шаблон

12 цифр:
- шесть цифр в формате ГГММДД (дата рождения); 
- дефис (необязательно); 
- код места рождения из двух букв; 
- дефис (необязательно); 
- три случайные цифры; 
- код пола из одной цифры.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_malaysia_id_card_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_malaysia_id_card_number.

```
<!-- Malaysia ID Card Number -->
</Entity>
      <Entity id="7f0e921c-9677-435b-aba2-bb8f1013c749" patternsProximity="300" recommendedConfidence="85">
        <Pattern confidenceLevel="85">
            <IdMatch idRef="Regex_malaysia_id_card_number" />
            <Match idRef="Keyword_malaysia_id_card_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordmalaysiaidcardnumber"></a>Кэйворд_малайсиа_ид_кард_нумбер

- карточка цифрового приложения
- i/c
- i/c нет
- внутренних
- МФ нет
- идентификационная карточка
- идентификационная карточка
- identity card
- k/p
- k/p
- кад акуан Дири
- кад апликаси Digital
- кад пенженалан Малайзии
- ключев
- ключевой номер
- микад
- Микас
- микид
- МИПР
- митентера
- идентификационная карточка Малайзии
- идентификационная карточка малайсиан
- NRIC
- Личная идентификационная карточка
   
## <a name="netherlands-citizens-service-bsn-number"></a>Номер гражданской службы для Нидерландов (BSN)

### <a name="format"></a>Формат

8–9 цифр, содержащих необязательные пробелы.

### <a name="pattern"></a>Шаблон

8–9 цифр:
- Три цифры 
- пробел (необязательно);  
- Три цифры 
- пробел (необязательно);  
- 2–3 цифры.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_netherlands_bsn находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_netherlands_bsn;
- функция Func_eu_date2 находит дату в правильном формате.
- Контрольная сумма проходит проверку.

```
<!-- Netherlands Citizen's Service (BSN) Number -->
<Entity id="c5f54253-ef7e-44f6-a578-440ed67e946d" patternsProximity="300" recommendedConfidence="85">
  <Pattern confidenceLevel="85">
       <IdMatch idRef="Func_netherlands_bsn" /> 
       <Match idRef="Keyword_netherlands_bsn" /> 
       <Match idRef="Func_eu_date2" /> 
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordnetherlandsbsn"></a>Кэйворд_несерландс_бсн

- Citizen service number
 
- BSN

 
- Burgerservicenummer
 
- Sofinummer
 
- Persoonsgebonden nummer
 
- Persoonsnummer
    

   
## <a name="new-zealand-ministry-of-health-number"></a>Номер министерства здравоохранения для Новой Зеландии

### <a name="format"></a>Формат

Три буквы, пробел (необязательно) и четыре цифры.

### <a name="pattern"></a>Шаблон

Три буквы (без учета регистра), пробел (необязательно) из четырех цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_new_zealand_ministry_of_health_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_nz_terms;
- Контрольная сумма проходит проверку.

```
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

Ключевые слова

Кэйворд_нз_термс

- NHI
 
- Новая Зеландия 
- Работоспособность 
- treatment
 
   
## <a name="norway-identification-number"></a>Идентификационный номер для Норвегии

### <a name="format"></a>Формат

11 разрядов

### <a name="pattern"></a>Шаблон

11 цифр:
- шесть цифр в формате ДДММГГ (дата рождения); 
- индивидуальный номер из трех цифр; 
- две проверочные цифры.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_norway_id_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_norway_id_number;
- контрольная сумма проходит проверку.
- Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_norway_id_numbe находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordnorwayidnumber"></a>Кэйворд_норвай_ид_нумбер

- Personal identification number
- Norwegian ID Number
- ID Number
- Identification
- Personnummer
- Fødselsnummer

   
## <a name="philippines-unified-multi-purpose-id-number"></a>Единый многофункциональный идентификационный номер для Филиппин

### <a name="format"></a>Формат

12 цифр, разделенных дефисами.

### <a name="pattern"></a>Шаблон

12 цифр:
- Четыре цифры 
- дефис; 
- семь цифр; 
- дефис; 
- Одна цифра

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_philippines_unified_id находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_philippines_id.

```
<!-- Philippines Unified Multi-Purpose ID number -->
<Entity id="019b39dd-8c25-4765-91a3-d9c6baf3c3b3" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_philippines_unified_id"/>
     <Match idRef="Keyword_philippines_id"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordphilippinesid"></a>Кэйворд_филиппинес_ид

- Unified Multi-Purpose ID
 
- UMID
 
- Identity Card 
- Pinag-isang Multi-Layunin ID
   
## <a name="poland-identity-card"></a>Номер удостоверения личности для Польши

### <a name="format"></a>Формат

Три буквы и шесть цифр.

### <a name="pattern"></a>Шаблон

Три буквы (без учета регистра), за которыми следуют шесть цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных — 75% уверенности, что она обнаружила этот тип конфиденциальной информации, если в пределах близости от 300 символов: функция Функ_полиш_натионал_ид находит содержимое, которое соответствует шаблону; Найдено ключевое слово из Кэйворд_полиш_натионал_ид_пасспорт_нумбер. Контрольная сумма проходит проверку.

```
<!-- Poland Identity Card-->
<Entity id="25E64989-ED5D-40CA-A939-6C14183BB7BF" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_national_id" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordpolishnationalidpassportnumber"></a>Кэйворд_полиш_натионал_ид_пасспорт_нумбер

- Довóд особисти
- Нумер доводу особистего
- Назва i нумер доводу особистего
- Назва i НР доводу особистего
- Nazwa i nr dowodu tożsamości

- Dowód Tożsamości

- dow. os.


   
## <a name="poland-national-id-pesel"></a>Национальный идентификатор (PESEL), Польша

### <a name="format"></a>Формат

11 разрядов

### <a name="pattern"></a>Шаблон

11 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_pesel_identification_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_pesel_identification_number;
- Контрольная сумма проходит проверку.

```
<!-- Poland National ID (PESEL) -->      
<Entity id="E3AAF206-4297-412F-9E06-BA8487E22456" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_pesel_identification_number" />
          <Match idRef="Keyword_pesel_identification_number" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordpeselidentificationnumber"></a>Кэйворд_песел_идентификатион_нумбер

- Nr PESEL
- PESEL   

   
## <a name="poland-passport"></a>Номер паспорта для Польши

### <a name="format"></a>Формат

Две буквы и семь цифр.

### <a name="pattern"></a>Шаблон

Две буквы (без учета регистра), за которыми следуют семь цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_polish_passport_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_polish_national_id_passport_number;
- Контрольная сумма проходит проверку.

```
<!-- Poland Passport Number -->
<Entity id="03937FB5-D2B6-4487-B61F-0F8BFF7C3517" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_polish_passport_number" />
          <Match idRef="Keyword_polish_national_id_passport_number" />
      </Pattern>
</Entity>
</Version>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordpolishnationalidpassportnumber"></a>Кэйворд_полиш_натионал_ид_пасспорт_нумбер

- Нумер пасзпорту
- НР. Пасзпорту
- Пасзпорт

   
## <a name="portugal-citizen-card-number"></a>Номер карты гражданина Португалии

### <a name="format"></a>Формат

Восемь цифр

### <a name="pattern"></a>Шаблон

Восемь цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_portugal_citizen_card находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_portugal_citizen_card.

```
<!-- Portugal Citizen Card Number -->
<Entity id="91a7ece2-add4-4986-9a15-c84544d81ecd" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Regex_portugal_citizen_card"/>
     <Match idRef="Keyword_portugal_citizen_card"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordportugalcitizencard"></a>Кэйворд_португал_Цитизен_кард

- Citizen Card
- National ID Card
- CC
- Cartão de Cidadão
- Bilhete de Identidade
   
## <a name="saudi-arabia-national-id"></a>Национальный идентификатор для Саудовской Аравии

### <a name="format"></a>Формат

10 цифр.

### <a name="pattern"></a>Шаблон

10 последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_saudi_arabia_national_id находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_saudi_arabia_national_id.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordsaudiarabianationalid"></a>Кэйворд_сауди_арабиа_натионал_ид

- Identification Card
 
- I card number
 
- идентификатор 
- الوطنية الهوية بطاقة رقم
 

   
## <a name="singapore-national-registration-identity-card-nric-number"></a>Номер внутреннего удостоверения личности гражданина Сингапура (NRIC)

### <a name="format"></a>Формат

Девять букв и цифр.

### <a name="pattern"></a>Шаблон

- Девять букв и цифр:
- буква "F", "G", "S" или "T" (без учета регистра); 
- семь цифр; 
- алфавитный проверочный символ.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_singapore_nric;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_singapore_nric находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordsingaporenric"></a>Кэйворд_сингапоре_нрик

- National Registration Identity Card
 
- Identity Card Number
 
- NRIC
 
- IC
 
- Foreign Identification Number
 
- FIN
 
- 身份证  
- 身份證
 
   
## <a name="south-africa-identification-number"></a>Идентификационный номер для Южной Африки

### <a name="format"></a>Формат

13 цифр, которые могут содержать пробелы.

### <a name="pattern"></a>Шаблон

13 цифр:
- шесть цифр в формате ГГММДД (дата рождения); 
- четыре цифры; 
- индикатор гражданства в виде одной цифры; 
- цифра "8" или "9"; 
- одна цифра (проверочная).

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_south_africa_identification_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_south_africa_identification_number;
- Контрольная сумма проходит проверку.

```
<!-- South Africa Identification Number -->
<Entity id="e2adf7cb-8ea6-4048-a2ed-d89eb65f2780" recommendedConfidence="85" patternsProximity="300">
  <Pattern confidenceLevel="85">
     <IdMatch idRef="Func_south_africa_identification_number"/>
     <Match idRef="Keyword_south_africa_identification_number"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordsouthafricaidentificationnumber"></a>Кэйворд_саус_африка_идентификатион_нумбер

- Identity card
- ID
- Identification 
   
## <a name="south-korea-resident-registration-number"></a>Регистрационный номер жителя Южной Кореи

### <a name="format"></a>Формат

13 цифр, содержащих дефис.

### <a name="pattern"></a>Шаблон

13 цифр:
- шесть цифр в формате ГГММДД (дата рождения); 
- дефис; 
- одна цифра (определяет век и пол); 
- код региона рождения из четырех цифр; 
- одна цифра, используемая для разграничения людей, у которых предшествующие цифры совпадают; 
- проверочная цифра.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_south_korea_resident_number;
- контрольная сумма проходит проверку.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_south_korea_resident_number находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordsouthkorearesidentnumber"></a>Кэйворд_саус_кореа_ресидент_нумбер

- National ID card
 
- Citizen's Registration Number
 
- Jumin deungnok beonho
 
- RRN
 
- 주민등록번호
   
## <a name="spain-social-security-number-ssn"></a>Страховой номер для Испании (SSN)

### <a name="format"></a>Формат

11–12 цифр.

### <a name="pattern"></a>Шаблон

11-12 цифр:
- две цифры;  
- Косая черта (необязательно) 
- 7–8 цифр 
- Косая черта (необязательно) 
- Две цифры

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_spanish_social_security_number находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
<!-- Spain SSN -->
<Entity id="5df987c0-8eae-4bce-ace7-b316347f3070" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_spanish_social_security_number" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

Нет
   
## <a name="sweden-national-id"></a>Национальный идентификатор для Швеции

### <a name="format"></a>Формат

10 или 12 цифр и дополнительный разделитель.

### <a name="pattern"></a>Шаблон

10 или 12 цифр с необязательным разделителем
- 2–4 цифры (необязательно) 
- Шесть цифр в формате даты ГГММДД. 
- Разделитель - или + (необязательно)
- четыре цифры.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_swedish_national_identifier находит содержимое, которое соответствует шаблону;
- Контрольная сумма проходит проверку.

```
<!-- Sweden National ID -->
<Entity id="f69aaf40-79be-4fac-8f05-fd1910d272c8" patternsProximity="300" recommendedConfidence="85">
    <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_swedish_national_identifier" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

Нет
   
## <a name="sweden-passport-number"></a>Номер паспорта гражданина Швеции

### <a name="format"></a>Формат

Восемь цифр

### <a name="pattern"></a>Шаблон

Восемь последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Регулярное выражение Regex_sweden_passport_number находит содержимое, которое соответствует шаблону.
- Верно одно из условий ниже:
    - найдено ключевое слово из Keyword_passport;
    - найдено ключевое слово из Keyword_sweden_passport.

```
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

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordswedenpassport"></a>Кэйворд_сведен_пасспорт

- visa requirements
 
- Alien Registration Card
 
- Schengen visas
 
- Schengen visa
 
- Visa Processing
 
- Visa Type
 
- Single Entry
 
- Multiple Entry
 
- G3 Processing Fees

 

#### <a name="keywordpassport"></a>Кэйворд_пасспорт

- Passport Number 
- 
Passport No 
- Passport#
 
- Passport#
 
- Пасспортид 
- Passportno
 
- passportnumber
 
- パスポート 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
- Numéro de passeport 
- 
Passeport n ° 
- Passeport Non
 
- Passeport#
 
- Passeport#
 
- Пассепортнон 
- Passeportn °
 
   
## <a name="swift-code"></a>Код SWIFT

### <a name="format"></a>Формат

Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры.

### <a name="pattern"></a>Шаблон

Четыре буквы, за которыми следуют от 5 до 31 буквы или цифры
- Четырехбуквенный код банка (без учета регистра) 
- Необязательный пробел 
- 4–28 букв или цифр (основной номер банковского счета, BBAN) 
- Необязательный пробел 
- 1–3 буквы или цифры (оставшаяся часть BBAN)

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_swift находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_swift.

```
<Entity id="cb2ab58c-9cb8-4c81-baf8-a4e106791df4" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_swift" />
        <Match idRef="Keyword_swift" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keywordswift"></a>Кэйворд_свифт

- international organization for standardization 9362
 
- iso 9362
 
- iso9362 
- SWIFT\# 
- swiftcode
 
- swiftnumber
 
- swiftroutingnumber
 
- код SWIFT 
- swift number #
 
- swift routing number
 
- bic number
 
- bic code
 
- БИК\# 
- БИК\# 
- bank identifier code
 
- 標準化 9362 
- 迅速＃
 
- SWIFTコード
 
- SWIFT番号
 
- 迅速なルーティング番号
 
- BIC番号
 
- BICコード
 
- 銀行識別コードのための国際組織
 
- Organisation internationale de normalisation 9362
 
- Быстрая\# 
- code SWIFT
 
- le numéro de swift
 
- swift numéro d'acheminement
 
- le numéro BIC
 
- \#БИК 
- code identificateur de banque
 
   
## <a name="taiwan-national-id"></a>Национальный идентификатор, Тайвань

### <a name="format"></a>Формат

Одна буква (английская), за которой следуют девять цифр.

### <a name="pattern"></a>Шаблон

Один символ , за которым следуют девять цифр
- Один символ (на английском языке, без учета регистра) 
- Цифра 1 или 2 
- Восемь цифр

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_taiwanese_national_id находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_taiwanese_national_id;
- Контрольная сумма проходит проверку.

```
<!-- Taiwanese National ID -->
<Entity id="4C7BFC34-8DD1-421D-8FB7-6C6182C2AF03" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_taiwanese_national_id" />
          <Match idRef="Keyword_taiwanese_national_id" />
      </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordtaiwanesenationalid"></a>Кэйворд_таиванесе_натионал_ид

- 身份證字號
 
- 身份證
 
- 身份證號碼
 
- 身份證號
 
- 身分證字號
 
- 身分證  
- 身分證號碼
 
- 身份證號
 
- 身分證統一編號
 
- 國民身分證統一編號
 
- 簽名
 
- 蓋章
 
- 簽名或蓋章

 
- 簽章   
   
## <a name="taiwan-passport-number"></a>	Номер паспорта гражданина Тайваня

### <a name="format"></a>Формат

- Номер биометрического паспорта: девять цифр
- Номер биометрической службы Passport: девять цифр

### <a name="pattern"></a>Шаблон
Номер биометрического паспорта:
- цифра "3"; 
- восемь цифр.

Номер биометрической службы Passport:
- Девять цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_taiwan_passport находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_taiwan_passport.

```
<!-- Taiwan Passport Number -->
<Entity id="e7251cb4-4c2c-41df-963e-924eb3dae04a" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_passport"/>
     <Match idRef="Keyword_taiwan_passport"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordtaiwanpassport"></a>Кэйворд_таиван_пасспорт

- ROC passport number
 
- Номер паспорта 
- Паспорт нет 
- Passport Num
 
- Passport#
 
- 护照
 
- 中華民國護照
 
- Zhōnghuá Mínguó hùzhào
   
## <a name="taiwan-resident-certificate-arctarc-number"></a>Номер удостоверения жителя Тайваня (ARC/TARC)

### <a name="format"></a>Формат

10 букв и цифр.

### <a name="pattern"></a>Шаблон

10 букв и цифр:
- две буквы (без учета регистра); 
- восемь цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_taiwan_resident_certificate находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_taiwan_resident_certificate.

```
<!-- Taiwan Resident Certificate (ARC/TARC) -->
<Entity id="48269fec-05ea-46ea-b326-f5623a58c6e9" recommendedConfidence="75" patternsProximity="300">
  <Pattern confidenceLevel="75">
     <IdMatch idRef="Regex_taiwan_resident_certificate"/>
     <Match idRef="Keyword_taiwan_resident_certificate"/>
  </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordtaiwanresidentcertificate"></a>Кэйворд_таиван_ресидент_цертификате

- Resident Certificate
 
- Резидентный сертификат 
- Resident Cert.
 
- Идентификационная карточка 
- Alien Resident Certificate
 
- ГИПЕРБОЛ 
- Taiwan Area Resident Certificate
 
- TARC
 
- 居留證
 
- 外僑居留證
 
- 台灣地區居留證
 

## <a name="thai-population-identification-code"></a>Код идентификации для тайского заполнения

### <a name="format"></a>Формат

13 цифр.

### <a name="pattern"></a>Шаблон

13 цифр:
- Первая цифра не равна 0 или 9 
- 12 цифр.

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.
- Найдено ключевое слово из Кэйворд_саи_Цитизен_ид.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Функ_саи_Цитизен_ид обнаружила содержимое, соответствующее шаблону.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordthaicitizenid"></a>Кэйворд_саи_Цитизен_ид

- ID Number
- Идентификационный номер
- บัตรประชาชน
- รหัสบัตรประชาชน
- บัตรประชาชน
- รหัสบัตรประชาชน
  
## <a name="turkish-national-identification-number"></a>Турецкий национальный идентификационный номер

### <a name="format"></a>Формат

11 разрядов

### <a name="pattern"></a>Шаблон

11 разрядов

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.
- Найдено ключевое слово из Кэйворд_туркиш_натионал_ид.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Функ_туркиш_натионал_ид обнаружила содержимое, соответствующее шаблону.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordturkishnationalid"></a>Кэйворд_туркиш_натионал_ид

- TC Кимлик No
- TC Кимлик нумарасı
- Ватандаşлıк нумарасı
- Ватандаşлıк нет

## <a name="uk-drivers-license-number"></a>Номер водительского удостоверения для Соединенного Королевства

### <a name="format"></a>Формат

Сочетание 18 букв и цифр в указанном формате.

### <a name="pattern"></a>Шаблон

18 букв и цифр
- Пять букв (без учета регистра) или цифра 9 вместо буквы 
- Одна цифра 
- Пять цифр в формате даты ДДММГ, представляющие собой дату рождения 
- Две буквы (без учета регистра) или цифра 9 вместо буквы 
- Пять цифр

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_uk_drivers_license находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_uk_drivers_license;
- Контрольная сумма проходит проверку.

```
<!-- U.K. Driver's License Number -->
<Entity id="f93de4be-d94c-40df-a8be-461738047551" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_uk_drivers_license" />
        <Match idRef="Keyword_uk_drivers_license" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordukdriverslicense"></a>Кэйворд_ук_дриверс_лиценсе

- DVLA
 
- light vans
 
- quadbikes
 
- motor cars
 
- 125cc 
- sidecar
 
- tricycles
 
- motorcycles
 
- photocard licence
 
- learner drivers
 
- licence holder
 
- licence holders
 
- driving licences
 
- driving licence
 
- dual control car
 
   
## <a name="uk-electoral-roll-number"></a>Регистрационный номер избирателя для Соединенного Королевства

### <a name="format"></a>Формат

Две буквы, за которыми следуют 1–4 цифры.

### <a name="pattern"></a>Шаблон

Две буквы (без учета регистра), за которыми следуют 1–4 цифры.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_uk_electoral находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_uk_electoral.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordukelectoral"></a>Кэйворд_ук_електорал

- council nomination
 
- nomination form
 
- electoral register

 
- electoral roll

   
## <a name="uk-national-health-service-number"></a>Номер национальной службы здравоохранения для Соединенного Королевства

### <a name="format"></a>Формат

10–17 цифр, разделенных пробелами.

### <a name="pattern"></a>Шаблон

10-17 цифр
- 3 или 10 цифр 
- Пробел 
- Три цифры 
- Пробел 
- Четыре цифры

### <a name="checksum"></a>Контрольная сумма

Да

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_uk_nhs_number находит содержимое, которое соответствует шаблону.
- Верно одно из условий ниже:
    - найдено ключевое слово из Keyword_uk_nhs_number;
    - найдено ключевое слово из Keyword_uk_nhs_number1;
    - найдено ключевое слово из Keyword_uk_nhs_number_dob.
- Контрольная сумма проходит проверку.

```
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

### <a name="keywords"></a>Ключевые слова
   
#### <a name="keyworduknhsnumber"></a>Кэйворд_ук_нхс_нумбер

- national health service
 
- nhs
 
- health services authority

 
- health authority

#### <a name="keyworduknhsnumber1"></a>Keyword_uk_nhs_number1

- patient id
 
- patient identification
 
- patient no

 
- patient number

#### <a name="keyworduknhsnumberdob"></a>Кэйворд_ук_нхс_нумбер_доб

- Групповая политика 
- DOB
 
- D. O. B 
- Date of Birth
 
- Birth Date
 
   
## <a name="uk-national-insurance-number-nino"></a>Номер карты национального страхования для Соединенного Королевства (NINO)

### <a name="format"></a>Формат

7 символов или 9 символов, разделенных пробелами или тире

### <a name="pattern"></a>Шаблон

Два возможных шаблона:

- Две буквы (допустимые Нинос используют только определенные символы в этом префиксе, которые пропускаются при проверке этого шаблона; без учета регистра)
- Шесть цифр
- "A", "B", "C", или "'D" (например, префикс, в суффиксе допускаются только определенные символы; без учета регистра)

ИЛИ

- Две буквы
- Пробел или тире
- Две цифры
- Пробел или тире
- Две цифры
- Пробел или тире
- Две цифры
- Пробел или тире
- Значение "A", "B", "C" или "'D"

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_uk_nino находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_uk_nino.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_uk_nino находит содержимое, которое соответствует шаблону;
- ни одно ключевое слово из Keyword_uk_nino не находится.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keyworduknino"></a>Кэйворд_ук_нино

- national insurance number
 
- national insurance contributions
 
- protection act
 
- insurance
 
- social security number
 
- insurance application
 
- medical application
 
- social insurance
 
- medical attention
 
- социальное обеспечение безопасности 
- great britain
 
- insurance
    
   
## <a name="us--uk-passport-number"></a>Номер паспорта гражданина США и/или Соединенного Королевства

### <a name="format"></a>Формат

Девять цифр.

### <a name="pattern"></a>Шаблон

Девять последовательных цифр.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_usa_uk_passport находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_passport.

```
<Entity id="178ec42a-18b4-47cc-85c7-d62c92fd67f8" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_usa_uk_passport" />
        <Match idRef="Keyword_passport" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordpassport"></a>Кэйворд_пасспорт

- Passport Number 
- 
Passport No 
- Passport#
 
- Passport#
 
- Пасспортид 
- Passportno
 
- passportnumber
 
- パスポート 
- パスポート番号
 
- パスポートのNum
 
- パスポート＃
 
- Numéro de passeport 
- 
Passeport n ° 
- Passeport Non
 
- Passeport#
 
- Passeport#
 
- Пассепортнон 
- Passeportn °
 
   
## <a name="us-bank-account-number"></a>Номер банковского счета для США

### <a name="format"></a>Формат

8-17 цифр

### <a name="pattern"></a>Шаблон

8–17 последовательных цифр

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- регулярное выражение Regex_usa_bank_account_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_usa_Bank_Account.

```
<!-- U.S. Bank Account Number -->
<Entity id="a2ce32a8-f935-4bb6-8e96-2a5157672e2c" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef="Regex_usa_bank_account_number" />
        <Match idRef="Keyword_usa_Bank_Account" />
    </Pattern>
</Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordusabankaccount"></a>Кэйворд_уса_банк_аккаунт

- Checking Account Number
 
- Checking Account
 
- Checking Account #
 
- Checking Acct Number
 
- Checking Acct #
 
- Checking Acct No.
 
- Checking Account No.
 
- Bank Account Number
 
- Bank Account #
 
- Bank Acct Number
 
- Bank Acct #
 
- Bank Acct No.
 
- Bank Account No.
 
- Savings Account Number
 
- Savings Account.
 
- Savings Account #
 
- Savings Acct Number
 
- Savings Acct #
 
- Savings Acct No.
 
- Savings Account No.
 
- Debit Account Number
 
- Debit Account
 
- Debit Account #
 
- Debit Acct Number
 
- Debit Acct #
 
- Debit Acct No.
 
- Debit Account No.
 
   
## <a name="us-drivers-license-number"></a>Номер водительского удостоверения для США

### <a name="format"></a>Формат

Зависит от штата.

### <a name="pattern"></a>Шаблон

В зависимости от штата. Например, для Нью-Йорка:
- Подойдут девять цифр в формате ццц ццц ццц.
- Не подойдут девять цифр в формате ццццццццц.

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_[state_name]_drivers_license_name;
- обнаружено ключевое слово из списка Keyword_us_drivers_license.

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- функция Func_new_york_drivers_license_number находит содержимое, которое соответствует шаблону;
- находится ключевое слово из Keyword_[state_name]_drivers_license_name;
- находится ключевое слово из Keyword_us_drivers_license_abbreviations;
- ни одно ключевое слово из Keyword_us_drivers_license не находится.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordusdriverslicenseabbreviations"></a>Кэйворд_ус_дриверс_лиценсе_аббревиатионс

- DL 
- DLS 
- КДЛ 
- КДЛС 
- ID 
- Идентификаторы 
- DL# 
- 
DLS#
 
- CDL#
 
- CDLS#
 
- ID#
- 
IDs#
 
- идентификатор 
- ID numbers
 
- Лик 
- LIC#
 

#### <a name="keywordusdriverslicense"></a>Кэйворд_ус_дриверс_лиценсе

- Дриверлик 
- Дриверликс 
- Дриверлиценсе 
- Дриверлиценсес 
- Драйвер Лик 
- Драйвер ликс 
- Лицензия на драйвер 
- Лицензии на драйверы 
- Дриверслик 
- Дриверсликс 
- Дриверслиценсе 
- Дриверслиценсес 
- Драйверы Лик 
- Драйверы ликс 
- Лицензия на драйверы 
- Лицензии на драйверы 
- Driver ' LIC 
- Driver ' LICS 
- Driver ' License 
- Driver ' Licenses 
- Драйвер "Лик 
- Драйвер "ЛИКС 
- Лицензия "Driver" 
- Лицензии на драйвер
- Дривер'слик 
- Дривер'сликс 
- Дривер'слиценсе 
- Дривер'слиценсес 
- Лик драйвера 
- Ликс драйвера 
- Лицензия на драйвер 
- Лицензии на драйвер 
- identification number
 
- identification numbers
 
- identification #
 
- идентификационная карточка 
- идентификационные карточки 
- идентификационная карточка 
- идентификационные карточки 
- Дриверлик # 
- Дриверликс # 
- Дриверлиценсе # 
- Дриверлиценсес # 
- Driver Lic# 
- 
Driver Lics#
 
- Номер лицензии драйвера 
- Лицензии на драйверы # 
- Дриверслик # 
- Дриверсликс # 
- Дриверслиценсе # 
- Дриверслиценсес # 
- Drivers Лик # 
- Drivers ликс # 
- Driver License # 
- Лицензии на драйверы # 
- Driver' Lic#
 
- Driver' Lics#
 
- Driver' License#
 
- Driver' Licenses#
 
- Driver' Lic#
 
- Driver' Lics#
 
- Driver' License#
 
- Driver' Licenses#
 
- Дривер'слик # 
- Дривер'сликс # 
- Дривер'слиценсе # 
- Дривер'слиценсес # 
- Driver's Lic#
 
- Driver's Lics#
 
- Driver's License#
 
- Driver's Licenses#
 
- Идентификатор карточки # 
- id cards#
 
- identification card#
 
- identification cards#
 


#### <a name="keywordstatenamedriverslicensename"></a>Keyword_[state_name]_drivers_license_name

- Аббревиатура штата (например, NY)
 
- Название штата (например, New York)
    
   
## <a name="us-individual-taxpayer-identification-number-itin"></a>Идентификационный номер налогоплательщика для США (ITIN)

### <a name="format"></a>Формат

Девять цифр, которые начинаются с "9" и содержат "7" или "8" в качестве четвертой цифры, отформатированных с помощью пробелов или тире (необязательно).

### <a name="pattern"></a>Шаблон

С форматированием
- Цифра 9 
- Две цифры 
- Пробел или тире 
- Цифра 7 или 8 
- Одна цифра 
- Пробел или тире 
- Четыре цифры

Без форматирования
- Цифра 9 
- Две цифры 
- Цифра 7 или 8 
- Пять цифр

### <a name="checksum"></a>Контрольная сумма

Нет

### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_formatted_itin находит содержимое, которое соответствует шаблону.
- Верно по меньшей мере одно из условий ниже:
    - найдено ключевое слово из Keyword_itin;
    - функция Func_us_address находит адрес в правильном формате.
    - функция Func_us_date находит дату в правильном формате;
    - найдено ключевое слово из Keyword_itin_collaborative.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_unformatted_itin находит содержимое, которое соответствует шаблону.
- Верно по меньшей мере одно из условий ниже:
    - найдено ключевое слово из Keyword_itin_collaborative;
    - функция Func_us_address находит адрес в правильном формате.
    - функция Func_us_date находит дату в правильном формате.

```
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

### <a name="keywords"></a>Ключевые слова

#### <a name="keyworditin"></a>Кэйворд_итин

- taxpayer
 
- tax id
 
- tax identification
 
- itin
 
- SSN 
- tin
 
- социальное обеспечение безопасности 
- tax payer
 
- itins
 
- taxid

 
- individual taxpayer
 

#### <a name="keyworditincollaborative"></a>Кэйворд_итин_коллаборативе

- License 
- DL 
- DOB
 
- Birthdate 
- День рождения  
- Date of Birth
 
   
## <a name="us-social-security-number-ssn"></a>Страховой номер для США (SSN)

### <a name="format"></a>Формат

9 цифр в виде форматированного или неформатированного шаблона.

> [!NOTE]
> Есть SSN выдан до середины 2011 г., он отличается строгим форматированием, при котором определенные части номера должны входить в указанные диапазоны (при этом нет контрольной суммы).

### <a name="pattern"></a>Шаблон

Четыре функции выполняют поиск SSN с использованием четырех разных шаблонов:
- Func_ssn находит SSN со строгим форматированием с тире или пробелами, выданные до 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);
- Func_unformatted_ssn находит SSN со строгим форматированием, выданные до 2011 г. (без форматирования в виде девяти последовательных цифр — ццццццццц);
- Func_randomized_formatted_ssn находит SSN с тире или пробелами, выданные после 2011 г. (ццц-цц-цццц ИЛИ ццц цц цццц);
- Func_randomized_unformatted_ssn находит SSN без форматирования в виде девяти последовательных цифр, выданные после 2011 г. (ццццццццц).

### <a name="checksum"></a>Контрольная сумма

Нет


### <a name="definition"></a>Определение

Политика защиты от потери данных с вероятностью в 85 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_ssn находит содержимое, которое соответствует шаблону.
- Находится ключевое слово из Keyword_ssn.

Политика защиты от потери данных с вероятностью в 75 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, не отдаленном более чем на 300 знаков:
- Функция Func_unformatted_ssn находит содержимое, которое соответствует шаблону.
- Находится ключевое слово из Keyword_ssn.

Политика защиты от потери данных с вероятностью в 65 % верно обнаруживает этот тип конфиденциальной информации, если в расположении, отдаленном не более чем на 300 знаков:
- Функция Func_randomized_formatted_ssn находит содержимое, которое соответствует шаблону.
- Находится ключевое слово из Keyword_ssn.
- Функция Func_ssn не находит содержимое, которое соответствует шаблону.

Политика защиты от потери данных с вероятностью в 55 % верно обнаружила этот тип конфиденциальной информации, если в пределах ближайших 300 знаков:
- Функция Func_randomized_unformatted_ssn находит содержимое, которое соответствует шаблону.
- Находится ключевое слово из Keyword_ssn.
- Функция Func_unformatted_ssn не находит содержимое, которое соответствует шаблону.

```
<!-- U.S. Social Security Number (SSN) -->
    <Entity id="a44669fe-0d48-453d-a9b1-2cc83f2cba77" patternsProximity="300" recommendedConfidence="75">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="Func_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <IdMatch idRef="Func_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
      </Pattern>
      <Pattern confidenceLevel="65">
        <IdMatch idRef="Func_randomized_formatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_ssn" />
        </Any>
      </Pattern>
      <Pattern confidenceLevel="55">
        <IdMatch idRef="Func_randomized_unformatted_ssn" />
        <Match idRef="Keyword_ssn" />
        <Any minMatches="0" maxMatches="0">
          <Match idRef="Func_unformatted_ssn" />
        </Any>
      </Pattern>
    </Entity>
```

### <a name="keywords"></a>Ключевые слова

#### <a name="keywordssn"></a>Кэйворд_ссн

- Social Security
 
- Social Security#
 
- Soc Sec
 
- SSN 
- SSNS
 
- SSN#
 
- SS#
 
- SSID
 
   

