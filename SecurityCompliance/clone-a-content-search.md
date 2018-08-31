---
title: Клонирование поиска контента безопасности Office 365 &amp; центре соответствия требованиям
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Быстро клонирование существующего контента поиска в системы с помощью сценария Windows PowerShell в данной статье &amp; Compliane центр поиска. При клонировании поиска, создается новый поиск (с новым именем), содержащий те же свойства, как исходного поиска. Затем можно изменить нового поиска (с помощью изменения запроса ключевого слова или диапазон дат) и запустите его.
ms.openlocfilehash: a4f801e3de281e8caf8aeb7d1c2bd48f0facb77c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534719"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Клонирование поиска контента безопасности Office 365 &amp; центре соответствия требованиям

Создание контента поиска в Office 365 безопасность &amp; центре соответствия требованиям, которая выполняет поиск много почтовых ящиков или на сервере SharePoint и OneDrive для бизнеса сайтов может занять некоторое время. Определение сайтов для поиска также может быть может привести к ошибкам при вводе URL-адреса. Чтобы избежать этих проблем, можно использовать сценарий Windows PowerShell в данной статье следует быстро скопировать существующий поиск контента. При клонировании поиска, создается новый поиск (с другим именем), содержащий те же свойства (например, расположения контента и запросов поиска), как исходного поиска. Затем можно редактировать новый поиск (с помощью изменения запроса ключевого слова или диапазон дат) и запустите его.
  
Почему клонирование контента поиска?
  
- Сравнение полученных результатов различных ключевых слов запросов поиска выполните на одном размещения содержимого.
    
- Чтобы избежать повторного ввода большое число размещения содержимого при создании нового поиска.
    
- Уменьшение размера результатов поиска; Например при наличии поиска, которое возвращает слишком много результатов для экспорта, можно клонирование поиска и добавить условие поиска, на основе диапазона дат, чтобы уменьшить количество результатов поиска.
  
## <a name="before-you-begin"></a>Перед началом работы

- Необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для запуска сценария, описанного в данном разделе.
    
- Сценарий включает в себя обработка минимальной ошибок. Основным назначением сценарий — это быстро клонирование поиска контента.
    
- Сценарий создает новый поиск контента, но не запустите ее.
    
- Этот сценарий учитывает ли поиск контента копируемого связан с вариантом eDiscovery. Если поиск связан с дела, новый поиск также будет связан с того же регистра. Если существующий поиск, не сопоставленный с дела, новый поиск отображаются на странице **поиска контента** в безопасности &amp; центре соответствия требованиям. 
    
- Пример сценария, представленные в этом разделе не поддерживается в любой программе стандартной поддержки корпорации Майкрософт и службы. Образец сценария предоставляются как есть без какой-либо. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности образец сценария и документация остается с вами. Событие не корпорации Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценариев несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать примеры сценариев или документации, даже если Microsoft поступали предупреждения о возможности такого ущерба.
  
## <a name="step-1-run-the-script-to-clone-a-search"></a>Шаг 1: Выполните скрипт, чтобы скопировать поиска

Скрипт на этом этапе будет создан новый поиск контента путем копирования существующей. При выполнении этого скрипта появится следующие сведения:
  
- **Учетные данные пользователя** - скрипт будет использовать свои учетные данные для подключения к безопасности &amp; центре соответствия требованиям для своей организации Office 365 с помощью Windows PowerShell. Как уже указано, необходимо быть участником группы ролей диспетчер обнаружения электронных данных в системы &amp; центре соответствия требованиям для выполнения скрипта. 
    
- **Имя существующего поиска** — это поиска контента, которую требуется скопировать. 
    
- **Имя нового поиска, который будет создан** - Если оставить это значение пустым, скрипт будет Создайте имя для нового поиска, который создается на основе имени поиска копируемого. 
    
Следует скопировать поиска:
  
1. Сохраните следующий текст в файл сценария Windows PowerShell с помощью суффикса имени файла .ps1; например `CloneSearch.ps1`.
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 Security &amp; Compliance Center
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. Откройте Windows PowerShell и перейдите к папке, в которой вы сохранили скрипт.
    
3. Выполнение скрипта; Например:
    
    ```
    .\CloneSearch.ps1
    ```

4. Когда требуется ввести учетные данные, введите адрес электронной почты и пароль и нажмите кнопку **ОК**.
    
5. Введите следующую информацию в ответ на запрос с помощью сценария. Введите каждый блок данных и нажмите клавишу **Ввод**.
    
    - Имя существующего поиска.
    
    - Имя нового поиска.
    
    Сценарий создает новый поиск контента, но не запустите ее. Это дает возможность изменить и выполните поиск на следующем шаге. Свойства нового поиска можно просмотреть с помощью командлета **Get-ComplianceSearch** или, перейдя на страницу **контента поиска** или **обнаружения электронных данных** в системы &amp; центре соответствия требованиям, в зависимости от того, является ли новый поиск связанные с дела. 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a>Шаг 2: Изменение и выполнение клонирования поиска в системы &amp; центре соответствия требованиям

После запуска сценария следует скопировать существующего контента поиска вы следующим шагом является переход на безопасность &amp; центре соответствия требованиям для редактирования и запустите новый поиск. Как уже указано, можно изменить поиска, изменив запрос поиска ключевого слова и добавление или удаление условия поиска. Для получения дополнительных сведений см.
  
- [Поиск контента в Office 365](content-search.md)
    
- [Запросы ключевых слов и условия поиска контента](keyword-queries-and-search-conditions.md)
    
- [вариантах eDiscovery безопасности Office 365 &amp; центре соответствия требованиям](ediscovery-cases.md)
