---
title: Создание пользовательских типов конфиденциальной информации с помощью точного совпадения данных
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 05/15/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Создание пользовательских типов конфиденциальной информации с помощью классификации на основе точного совпадения данных.
ms.openlocfilehash: 3b15bf0197918d6bbc3897f9fa578c40b70d3f4e
ms.sourcegitcommit: 4eb4ca899adcf4d86501530f875eb49af8cdaeb7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/16/2019
ms.locfileid: "34083192"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification-preview"></a>Создание пользовательских типов конфиденциальной информации с помощью классификации на основе точного совпадения данных (предварительная версия)

## <a name="overview"></a>Общие сведения

[Пользовательские типы конфиденциальной информации](custom-sensitive-info-types.md) используются для предотвращения непреднамеренного или неприемлемого предоставления общего доступа к конфиденциальной информации. Как администратор вы можете использовать [Центр безопасности и соответствия требованиям](create-a-custom-sensitive-information-type.md) или [PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md), чтобы определить пользовательский тип конфиденциальной информации на основе шаблонов, признаков (ключевые слова, например *сотрудник*, *эмблема*, *идентификатор* и т. д), расстояния между символами (как близко располагается признак к символам в определенном шаблоне) и уровней вероятности. Такие пользовательские типы конфиденциальной информации соответствуют бизнес-требованиям большинства организаций.

Но что если вам нужен пользовательский тип конфиденциальной информации, использующий точные значения данных, а не шаблоны и близость? С помощью классификации на основе точного совпадения данных (EDM) вы можете создать пользовательский тип конфиденциальной информации со следующими характеристиками:
- динамичный и обновляемый;
- дополнительные возможности масштабирования;
- снижает число ошибочно положительных результатов;
- поддерживает структурированные конфиденциальные данные;
- более безопасная обработка конфиденциальной информации;
- использование с несколькими облачными службами Майкрософт.

![Классификация на основе EDM](media/EDMClassification.png)

Классификация на основе EDM позволяет создавать пользовательские типы конфиденциальной информации, ссылающиеся на точные значения в базе данных конфиденциальной информации. Базу данных можно обновлять ежедневно или еженедельно, и она может содержать до 10 миллионов строк данных. Таким образом ваши пользовательские типы конфиденциальной информации остаются актуальными и применимыми при смене сотрудников, пациентов или клиентов, а также при изменении записей. Вы также можете использовать классификацию на основе EDM с политиками, такими как [политики защиты от потери данных](data-loss-prevention-policies.md) (DLP) или [политики файлов Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies).

## <a name="required-licenses-and-permissions"></a>Обязательные лицензии и разрешения

- Для выполнения задач, описанных в данной статье, вы должны быть глобальным администратором, администратором соответствия требованиям или администратором Exchange Online. Дополнительные сведения о разрешениях DLP см. в разделе [Разрешения](data-loss-prevention-policies.md#permissions).

- После выпуска в общедоступной версии классификация на основе EDM будет включена в следующие подписки:
    - Office 365 E5
    - Microsoft 365 E5
    - Защита данных и соответствие требованиям Microsoft 365
    - Office 365 Advanced Compliance

> [!NOTE]
> **Классификация на основе EDM в настоящее время доступна в предварительной версия** для [защиты от потери данных в Office 365](data-loss-prevention-policies.md) (с Exchange Online и Microsoft Teams) и [Cloud App Security](https://docs.microsoft.com/cloud-app-security). Если в вашей организации доступны [возможности защиты от потери данных](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc#data-loss-prevention-dlp), вы можете воспользоваться классификацией на основе EDM. Если вы еще не участвуете в программе предварительной оценки [свяжитесь с Майкрософт](https://resources.office.com/us-landing-spe-contactus.html?LCID=EN-US), чтобы приступить к работе. 

## <a name="the-work-flow-at-a-glance"></a>Обзор рабочего процесса

|Этап  |Требуемые параметры  |
|---------|---------|
|[Часть 1. Настройка классификации на основе EDM](#part-1-set-up-edm-based-classification)<br/><br/>(При необходимости)<br/>- [Изменение схемы базы данных](#editing-the-schema-for-edm-based-classification) <br/>- [Удаление схемы](#removing-the-schema-for-edm-based-classification) |– Доступ для чтения конфиденциальных данных<br/>– Схема базы данных в формате XML (доступен пример)<br/>– Пакет правил в формате XML (доступен пример)<br/>– Разрешения администратора на доступ к Центру безопасности и соответствия требованиям (с помощью PowerShell) |
|[Часть 2. Индексация и отправка конфиденциальных данных](#part-2-index-and-upload-the-sensitive-data)<br/><br/>(При необходимости)<br/>[Обновление данных](#refreshing-your-sensitive-information-database) |– Настраиваемая группа безопасности и учетная запись пользователя<br/>– Доступ локального администратора к компьютеру с агентом отправки EDM<br/>– Доступ для чтения конфиденциальных данных<br/>– Процесс и расписание для обновления данных|
|[Часть 3. Использование классификации на основе EDM с помощью облачных служб Майкрософт](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |– Подписка на Office 365 с защитой от потери данных<br/>– Включенная функция классификации на основе EDM (в предварительной версии) |

## <a name="part-1-set-up-edm-based-classification"></a>Часть 1. Настройка классификации на основе EDM

Установка и настройка классификации на основе EDM включает сохранение конфиденциальных данных в формате CSV, определение схемы для базы данных конфиденциальной информации и создание пакета правил с последующей отправкой схемы и пакета правил.

### <a name="define-the-schema-for-your-database-of-sensitive-information"></a>Определение схемы для базы данных конфиденциальной информации

1. Определите конфиденциальную информацию, которую нужно использовать. Экспортируйте данные в приложение, например Microsoft Excel, и сохраните файл в формате CSV. Файл данных может содержать:

    - До 10 миллионов строк конфиденциальных данных
    - До 32 столбцов (полей) на источник данных

2. Структурируйте конфиденциальные данные в CSV-файле таким образом, чтобы первая строка включала имена полей, которые используются для классификации на основе EDM. В CSV-файле можно применять такие имена полей, как ssn, birthdate, firstname, lastname и т. д. Например, наш CSV-файл называется *PatientRecords.csv*, а его столбцы включают *PatientID*, *MRN*, *lastname*, *FirstName*, *SSN* и другие.

3. Определите схему для базы данных конфиденциальной информации в формате XML (как в примере ниже). Назовите этот файл схемы `edm.xml` и настройте его таким образом, чтобы для каждого столбца в базе данных имелась строка, использующая синтаксис `<Field name="" unique="" searchable=""/>`. 

    - Используйте имена столбцов для значений *Field name*.
    - Используйте параметр *unique="true"* для полей, содержащих уникальные значения (номера социального страхования, идентификационные номера и т. д.); в противном случае используйте *unique="false"*.
    - Используйте параметр *searchable="true"* для полей, которые должны поддерживать поиск. Не указывайте для одной базы данных более пяти полей, поддерживающих поиск. Для всех остальных следует применить параметр *searchable="false"*.  

    Например, следующий XML-файл определяет схему для базы данных записей пациентов с пятью полями, для которых указывается возможность поиска: *PatientID*, *MRN*, *SSN*, *Phone* и *DOB*. 
    
    (Вы можете скопировать, изменить и использовать наш пример.)
    
    ```<?xml version="1.0" encoding="utf-8"?> <EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
        <DataStore name="PatientRecords" description="Схема для записей пациентов" version="1">
            <Field name="PatientID" unique="false" searchable="true" /> <Field name="MRN" unique="false" searchable="true" />
            <Field name="FirstName" unique="false" searchable="false" />
            <Field name="LastName" unique="false" searchable="false" />
            <Field name="SSN" unique="false" searchable="true" />
            <Field name="Phone" unique="false" searchable="true" />
            <Field name="DOB" unique="false" searchable="true" />
            <Field name="Gender" unique="false" searchable="false" />
            <Field name="Address" unique="false" searchable="false" />
        </DataStore>
    </EdmSchema>
    ```

4. [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

5. To upload the database schema, run the following cmdlets, one at a time:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    You will be prompted to confirm, as follows:

       Confirm
       Are you sure you want to perform this action?
       New EDM Schema for the data store 'patientrecords' will be imported.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > If you want your changes to occur without confirmation, in Step 5, use this cmdlet instead: `New-DlpEdmSchema -FileData $edmSchemaXml`
    
Now that the schema for your database of sensitive information is defined, the next step is to set up a rule package. Proceed to the section [Set up a rule package](#set-up-a-rule-package).

#### Editing the schema for EDM-based classification 

(As needed) If you want to make changes to your edm.xml file, such as changing which fields are used for EDM-based classification, follow these steps:

1. Edit your edm.mxl file (this is the file discussed in the [Define the schema](#define-the-schema-for-your-database-of-sensitive-information) section of this article).

2. [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

3. To update your database schema, run the following cmdlets, one at a time:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    You will be prompted to confirm, as follows:

       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be updated.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > If you want your changes to occur without confirmation, in Step 3, use this cmdlet instead: `Set-DlpEdmSchema -FileData $edmSchemaXml`

#### Removing the schema for EDM-based classification

(As needed) If you want to remove the schema you're using for EDM-based classification, follow these steps:

1. [Connect to Office 365 Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Run the following PowerShell cmdlet, substituting the data store name of "patientrecords" with the one you want to remove:

    `Remove-DlpEdmSchema -Identity patientrecords`

     You will be prompted to confirm, as follows:
    
       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be removed.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):
    
    > [!TIP]
    > If you want your changes to occur without confirmation, in Step 2, use this cmdlet instead: `Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false`

### Set up a rule package

1. Create a rule package in .xml format (with Unicode encoding), similar to the following example. (You can copy, modify, and use our example.) 

   Recall from the previous procedure that our PatientRecords schema defines five fields as searchable: *PatientID*, *MRN*, *SSN*, *Phone*, and *DOB*. Our example rule package includes those fields and references the database schema file (edm.xml), with one *ExactMatch* items per searchable field. Consider the following ExactMatch item:

   ```
    <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" > <Pattern confidenceLevel="65"> <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" /> </Pattern> </ExactMatch>
   ```

    In this example, note the following:

    - The dataStore name references the .csv file we created earlier: **dataStore = "PatientRecords"**.
    - The idMatch value references a searchable field that is listed in the database schema file: **idMatch matches = "SSN"**.
    - The classification value references an existing or custom sensitive information type: **classification = "U.S. Social Security Number (SSN)"**. (In this case, we use the existing sensitive information type of U.S. Social Security Number.)

    When you set up your rule package, make sure to correctly reference your .csv file and edm.xml file. (You can copy, modify, and use our example.) 

    ```<?xml version="1.0" encoding="utf-8"?>
    <RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
      <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
        <Version build="0" major="2" minor="0" revision="0" />
        <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
        <Details defaultLangCode="en-us">
          <LocalizedDetails langcode="en-us">
            <PublisherName>IP DLP</PublisherName>
            <Name>Health Care EDM Rulepack</Name>
            <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
          </LocalizedDetails>
        </Details>
      </RulePack>
      <Rules>
        <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
          <Pattern confidenceLevel="65">
            <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
            <Any minMatches ="3" maxMatches ="100">
              <match matches="PatientID" />
              <match matches="MRN"/>
              <match matches="FirstName"/>
              <match matches="LastName"/>
              <match matches="Phone"/>
              <match matches="DOB"/>
            </Any>
          </Pattern>
        </ExactMatch>
        <LocalizedStrings>
          <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
            <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
            <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
          </Resource>
        </LocalizedStrings>
      </Rules>
    </RulePackage>
    ```
    
2. Отправьте пакет правил, выполнив по отдельности указанные ниже командлеты PowerShell:

    `$rulepack=Get-Content .\rulepack.xml -Encoding Byte -ReadCount 0`

    `New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack`

На этом этапе вы настроили классификацию на основе EDM. Следующий этап состоит в индексации конфиденциальных данных с дальнейшей отправкой индексированных данных. 

## <a name="part-2-index-and-upload-the-sensitive-data"></a>Часть 2. Индексация и отправка конфиденциальных данных

На этом этапе выполняется настройка пользовательской группы безопасности и учетной записи пользователя, а также настройка агента отправки EDM. Затем используется средство для индексации конфиденциальных данных и отправляются индексированные данные.

### <a name="set-up-the-security-group-and-user-account"></a>Настройка группы безопасности и учетной записи пользователя

1. В качестве глобального администратора перейдите в Центр администрирования ([https://admin.microsoft.com](https://admin.microsoft.com)) и [создайте группу безопасности](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) с именем `EDM_DataUploaders`. 

2. Добавьте одного или нескольких пользователей в группу безопасности *EDM_DataUploaders*. (Эти пользователи будут управлять базой данных конфиденциальной информации.)

3. Убедитесь, что каждый пользователь, управляющий конфиденциальными данными, является локальным администратором на компьютере, используемом для агента отправки EDM.

### <a name="set-up-the-edm-upload-agent"></a>Настройка агента отправки EDM

> [!NOTE]
> Перед началом этой процедуры убедитесь, что вы являетесь участником группы безопасности *EDM_DataUploaders* и локальным администратором на своем компьютере.

1. Скачайте агент отправки EDM по ссылке [https://go.microsoft.com/fwlink/?linkid=2088639](https://go.microsoft.com/fwlink/?linkid=2088639) и установите его. По умолчанию установка должна выполняться в папку `C:\Program Files\Microsoft\EdmUploadAgent`. 

2. Чтобы разрешить работу агента отправки EDM, откройте командную строку Windows (в качестве администратора) и выполните следующую команду:

    `EdmUploadAgent.exe /Authorize`

3. Войдите с помощью рабочей или учебной учетной записи для Office 365.

Следующий этап состоит в использовании агента отправки EDM для индексации конфиденциальных данных с последующей отправкой индексированных данных.

### <a name="index-and-upload-the-sensitive-data"></a>Индексация и отправка конфиденциальных данных

1. Сохраните файл конфиденциальных данных (помните, что в нашем примере — это файл *PatientRecords.csv*) на локальном диске компьютера. (Файл *PatientRecords.csv* из примера сохранен в папку `C:\Edm\Data`.)

2. Чтобы индексировать конфиденциальные данные, выполните следующую команду в командной строке Windows:

    `EdmUploadAgent.exe /CreateHash /DataStoreName <DataStoreName> /DataFile <DataFilePath> /HashLocation <HashedFileLocation>`

    Пример: **EdmUploadAgent.exe /CreateHash /DataStoreName PatientRecords /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash** 

3. Чтобы отправить индексированные данные, выполните следующую команду в командной строке Windows:

    `EdmUploadAgent.exe /UploadHash /DataStoreName <DataStoreName> /HashFile <HashedSourceFilePath>`

    Пример: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\Edm\Hash\PatientRecords.EdmHash** 

4. Чтобы убедиться в отправке своих конфиденциальных данных, выполните следующую команду в командной строке Windows:

    `EdmUploadAgent.exe /GetDataStore`

    Отобразится список хранилищ данных и время их последнего обновления, как показано ниже: <br/>![Пример командлета GetDataStore и результатов](media/EDM-GetDataStore-example.png)

5. Перейдите к настройке процесса и расписания для [обновления базы данных конфиденциальной информации](#refreshing-your-sensitive-information-database).

На этом этапе вы готовы использовать классификацию на основе EDM с помощью облачных служб Майкрософт. Например, вы можете [настроить политику защиты от потери данных с помощью классификации на основе EDM](#to-create-a-dlp-policy-with-edm). 

### <a name="refreshing-your-sensitive-information-database"></a>Обновление базы данных конфиденциальной информации

Вы можете обновлять базу данных конфиденциальной информации ежедневно или еженедельно, а средство отправки EDM может повторно индексировать конфиденциальные данные и повторно отправлять индексированные данные. 

1. Определите процесс и частоту (ежедневно или еженедельно) обновления базы данных конфиденциальной информации.

2. Повторно экспортируйте конфиденциальные данные в приложение, например Microsoft Excel, и сохраните файл в формате CSV. Не изменяйте имя и расположение файла, использованные при выполнении действий, описанных в разделе [Индексация и отправка конфиденциальных данных](#index-and-upload-the-sensitive-data).

    > [!NOTE]
    > Если отсутствуют изменения в структуре (имена полей) CSV-файла, не нужно вносить изменения в файл схемы базы данных при обновлении данных. Но если нужно внести изменения, измените [схему базы данных](#editing-the-schema-for-edm-based-classification) и [пакет правил](#set-up-a-rule-package) соответствующим образом.        

3. Используйте [планировщик заданий](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page) для автоматизации действий 2 и 3 в процедуре [индексации и отправки конфиденциальных данных](#index-and-upload-the-sensitive-data). Вы можете планировать задачи с помощью нескольких методов:
    
    |Метод  |Действия  |
    |---------|---------|
    |Windows PowerShell     |См. документацию по [ScheduledTasks](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) и [пример скрипта PowerShell](#example-powershell-script-for-task-scheduler) в этой статье|
    |API планировщика заданий |См. документацию по [планировщику заданий](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) |
    |Пользовательский интерфейс Windows     |В Windows нажмите кнопку **Пуск** и введите `Task Scheduler`. Затем в списке результатов щелкните правой кнопкой мыши **Планировщик заданий** и выберите команду **Запуск от имени администратора**.          |

#### <a name="example-powershell-script-for-task-scheduler"></a>Пример скрипта PowerShell для планировщика заданий

Этот раздел содержит пример скрипта PowerShell, который можно использовать для планирования задач по индексации данных и отправке индексированных данных:

```powershell
param([string]$dataStoreName,[string]$fileLocation)
# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\$env:USERNAME"
$edminstallpath = 'C:\Program Files\Microsoft\EdmUploadAgent\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\$dataStoreName$csvext"
$hashFile = "$fileLocation\$dataStoreName$edmext"
# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=[Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($creds.Password))
# Register the scheduled task
$taskName = 'EDMUpload_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```
## <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a>Часть 3. Использование классификации на основе EDM с помощью облачных служб Майкрософт

Вы также можете использовать классификацию на основе EDM с функциями защиты информации, такими как [политики защиты от потери данных Office 365](data-loss-prevention-policies.md) и [политики файлов Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/data-protection-policies). В следующей процедуре описано, как использовать EDM с политикой защиты от потери данных, созданной в Центре безопасности и соответствия требованиям Office 365.

### <a name="to-create-a-dlp-policy-with-edm"></a>Создание политики DLP с EDM

1. Перейдите в Центр безопасности и соответствия требованиям ([https://protection.office.com](https://protection.office.com)).

2. Выберите **Защита от потери данных** > **Политика**.

3. Выберите **Создание политики** > **Custom** > **Далее**.

4. На вкладке **Назовите политику** укажите название и описание, а затем нажмите кнопку **Далее**.

5. На вкладке **Выберите расположения** щелкните **Позволить мне выбрать расположения** и нажмите кнопку **Далее**.<br/>![Параметр выбора расположений](media/DLP-EDM-newpolicy-chooselocations.png)<br/>

6. В столбце **Состояние** выберите только вариант **Электронная почта Exchange** и нажмите кнопку **Далее**. <br/>![Политика EDM только с параметром Exchange](media/EDM-DLPpolicy-ExchangeOnly.png)<br/>

7. На вкладке **Параметры политики** установите флажок **Использование дополнительных параметров** и нажмите кнопку **Далее**.<br/>![Использование дополнительных параметров](media/edm-dlp-policy-advancedsettings.png)<br/>

8. Нажмите кнопку **+ Создать правило**.<br/>![Создание правила](media/edm-dlp-newrule.png)<br/>

9. В разделе **Название** укажите название и описание для правила.<br/>![Поля нового правила](media/edm-dlp-newruleform.png)<br/>

10. В разделе **Условия** в списке **+ Добавить условие** выберите вариант **Содержит типы конфиденциальной информации**.<br/>![Контент содержит типы конфиденциальной информации](media/edm-dlp-newrule-conditions.png)<br/>

11. Найдите тип конфиденциальной информации, созданный при настройке пакета правил, и нажмите кнопку **+ Добавить**.<br/>![Поиск типа конфиденциальной информации](media/edm-dlp-newrulefindsensitiverulepack.png)<br/>Затем нажмите кнопку **Готово**.

12. Завершите выбор параметров для правила, таких как **Уведомления пользователей**, **Переопределения пользователя**, **Отчеты об инцидентах** и т. д., и нажмите кнопку **Сохранить**.

13. На вкладке **Параметры политики** проверьте свои правила и нажмите кнопку **Далее**.

14. Укажите, включить ли политику сразу, проверить ее или оставить выключенной. Затем нажмите кнопку **Далее**.

15. На вкладке **Проверьте параметры** просмотрите свою политику. Внесите любые необходимые изменения. После завершения нажмите кнопку **Создать**.

    > [!NOTE]
    > Предоставьте примерно один час новой политике DLP для ее реализации в вашем центре обработки данных.

## <a name="related-articles"></a>Статьи по теме

[Встроенные типы конфиденциальной информации и что они позволяют искать](what-the-sensitive-information-types-look-for.md)

[Пользовательские типы конфиденциальной информации](custom-sensitive-info-types.md)

[Обзор политик защиты от потери данных](data-loss-prevention-policies.md)

[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)
