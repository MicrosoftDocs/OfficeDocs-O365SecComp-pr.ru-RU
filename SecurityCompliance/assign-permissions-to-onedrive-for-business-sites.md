---
title: Назначение разрешений обнаружения электронных данных на сайтах OneDrive для бизнеса
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Центр обнаружения электронных данных в SharePoint Online можно использовать для поиска всех OneDrive для бизнеса сайтов в определенные ключевые слова, конфиденциальной информации и других критериев поиска в вашей организации. Каждому пользователю в организации является владельцем их OneDrive для бизнеса сайт, который находится в коллекции веб-сайтов с именем https://domain-my.sharepoint.com. По умолчанию глобального администратора Office 365 или compliance manager нельзя использовать центр обнаружения электронных данных в SharePoint Online для поиска любого OneDrive для бизнеса сайтов. Для поиска OneDrive for Business сайтов, Администраторы или руководителями соответствия необходимо быть администратором семейства сайтов, onedrive для бизнеса сайта.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534869"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a>Назначение разрешений обнаружения электронных данных на сайтах OneDrive для бизнеса

Центр обнаружения электронных данных в SharePoint Online можно использовать для поиска всех OneDrive для бизнеса сайтов в определенные ключевые слова, конфиденциальной информации и других критериев поиска в вашей организации. Каждому пользователю в организации является владельцем их OneDrive для бизнеса сайт, который находится в коллекции веб-сайтов с именем https://domain-my.sharepoint.com. По умолчанию глобального администратора Office 365 или compliance manager нельзя использовать центр обнаружения электронных данных в SharePoint Online для поиска любого OneDrive для бизнеса сайтов. Для поиска OneDrive for Business сайтов, Администраторы или руководителями соответствия необходимо быть администратором семейства сайтов, onedrive для бизнеса сайта. 
  
В этой статье описывается шаги, чтобы администратор или соответствия диспетчера администратором семейства сайтов для каждого OneDrive для бизнеса сайта в вашей организации. 
  
Советы по использованию скрипта в этой статье, включая Пересмотр скрипта в шаге 3, чтобы удалить пользователя как администратора семейства сайтов из службы OneDrive для бизнеса сайтов в разделе [Дополнительные сведения](#more-information) . 
  
## <a name="before-you-begin"></a>Перед началом работы

- Установите командную консоль SharePoint Online. Дополнительные сведения см. в статье [Настройка среды Windows PowerShell для командной консоли SharePoint Online](https://go.microsoft.com/fwlink/p/?LinkID=286318).
    
- Запустите сценарий в шаге 3 каждый раз, необходимо назначить пользователя как администратора семейства сайтов в любой OneDrive для бизнеса сайтов в вашей организации. 
    
    > [!IMPORTANT]
    > Администратор или соответствия руководителя, который является администратором семейства сайтов для OneDrive для сайтов бизнес-можно открыть пользователей OneDrive для бизнеса с библиотеками документов и выполнять те же задачи, что владельца. Важно для элемента управления и отслеживать пользователей, имеющей разрешение обнаружения электронных данных в OneDrive для бизнеса сайтов в вашей организации. 
  
- Пример сценария, представленные в этой статье не поддерживается в любой программе стандартной поддержки корпорации Майкрософт и службы. Образец сценария предоставляются как есть без какой-либо. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности образец сценария и документация остается с вами. Событие не Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценария несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать образец сценария или документация, даже если Microsoft поступали предупреждения о возможности такого ущерба.
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a>Этап 1: Сбор список всех OneDrive для бизнеса сайтов

Первым шагом является создание списка всех OneDrive для бизнеса сайтов в вашей организации. Сведения содержатся в разделе [Создание списка всех расположений OneDrive в вашей организации](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Этот сценарий в этой статье создает текстового файла со списком всех сайтов OneDrive. Скрипт, на котором запущен на шаге 3 назначает указанного пользователя как администратора семейства сайтов в каждом OneDrive для бизнеса сайтов, перечисленные в текстовый файл, созданный на этом этапе. Следующий текст пример форматирования в список сайтов в этом файле. При необходимости можно удалить сайты из этого файла.

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a>Шаг 2: Командная консоль SharePoint Online подключиться к своей организации

1. Откройте на локальном компьютере командную консоль SharePoint Online и выполните следующую команду:

    ```
    $credentials = Get-Credential
    ```

2. В диалоговом окне **Запрос учетных данных Windows PowerShell** введите имя пользователя и пароль глобального администратора Office 365, а затем нажмите кнопку **ОК**.
    
3. Чтобы подключить командную консоль к своей организации SharePoint Online, выполните следующую команду:
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. Убедитесь, что подключение к организации SharePoint Online установлено, получив список всех сайтов в организации с помощью следующей команды:
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a>Этап 3. Назначение пользователя администратором семейства веб-сайтов на сайтах OneDrive для бизнеса

Следующим шагом является запуск сценарий, который присваивает указанному пользователю как администратора семейства сайтов в каждом OneDrive для бизнеса сайта в вашей организации. Этот сценарий использует список OneDrive для бизнеса сайтов, созданной на шаге 1. Как было сказано ранее необходимо запустить этот скрипт каждый раз, когда необходимо назначить пользователя как администратора семейства сайтов OneDrive для бизнеса сайтов.
  
1. Сохраните приведенный ниже текст в текстовый файл. Этот файл можно назвать, например, OD4BAssignSCA.txt.

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. Изменение следующих переменных в начале файла сценария и используйте сведения, необходимые для вашей организации. В следующих примерах предполагается, что указано имя домена вашей организации contoso.onmicrosoft.com. Убедитесь, что заключите значения для переменных с двойные кавычки (» «).
    
    - **$AdminURI** — этот параметр указывает URI для службы администрирования SharePoint Online, например, `"https://contoso-admin.sharepoint.com"`.
    
    - **$AdminAccount** - это указывает учетную запись глобального администратора в организации Office 365, например `"admin@contoso.onmicrosoft.com"`.
    
    - **$eDiscoveryUser** - это учетная запись администратора или соответствия руководителя, который будет назначен в качестве администратора семейства сайтов для каждого OneDrive для бизнеса сайта в вашей организации, например, `"annb@contoso.onmicrosoft.com"`.
    
      > [!NOTE]
      > Изменение учетной записи пользователя, заданной переменной **$eDiscoveryUser** и повторно выполните скрипт, чтобы назначить другого пользователя как администратора семейства сайтов в OneDrive для бизнеса сайты, которые указаны в переменной **$MySiteListFile** . 
  
    - **$MySitePrefix** Это URL-адрес для домена MySite вашей организации. Это домен, который содержит все OneDrive для бизнеса сайтов в вашей организации, например, `"https://contoso-my.sharepoint.com"`.
    
    - **$MySiteListFile** Это указывает полный путь текстовый файл, созданный на шаге 1. Этот файл содержит список OneDrive для бизнеса сайтов в вашей организации, например `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Убедитесь, что заключите значение для этой переменной с одним кавычки (""). Обратите внимание, что следует указать место сохранения текстового файла в шаге 1.
    
3. Сохраните текстовый файл как файл сценария PowerShell, изменив расширение его имени на PS1. Например, файл OD4BAssignSCA.txt сохраняется как OD4BAssignSCA.ps1.
    
4. В командной консоли SharePoint Online перейдите к папке, содержащей сценарий PowerShell, созданный на предыдущем этапе, а затем запустите сценарий. Пример:
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    Будет предложено ввести пароль для учетной записи администратора, который указан в скрипте. Если сценарий выполнен успешно, сообщение `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` , отображаемых для каждого OneDrive для бизнеса сайт, указанный в входного файла, указанного идентификатором **$MySiteListFile**.

## <a name="more-information"></a>Дополнительные сведения

- Скрипта, выполняемого на шаге 3 с помощью командлета **Set-SPOUser** назначение указанного пользователя как администратора семейства сайтов в каждом OneDrive для бизнеса, указанный в файл, указанный в переменной **$MySiteListFile** . Если имеется очень большой организации с помощью тысяч пользователей, попробуйте выполнить следующие действия, чтобы упростить управление предоставление разрешений для обнаружения электронных данных. 
    
  - Отредактируйте файл, созданный на шаге 1, содержащий список OneDrive для бизнеса сайтов, чтобы оно включало только тех сайтов для пользователей, что, участвующие в активной юридических случаев.
    
  - Назначение разрешений не более чем 2500 OneDrive для бизнеса сайтов в день. Например предположим, у вас есть 10 000 OneDrive для бизнеса сайтов в вашей организации. Можно создать список на шаге 1 необходимо собрать все сайты. Затем можно использовать этот файл для создания четыре файла, которые содержат 2500 пользователей. С первого дня будет выполняться скрипт в шаге 3 для назначения разрешений сначала 2500 OneDrive для бизнеса сайтов. На второй день выполните скрипт Далее 2500 onedrive для бизнеса сайтов и так далее.
    
- Вести запись OneDrive для бизнеса сайтов, которые были им назначены разрешения обнаружения электронных данных и пользователя, который назначен в качестве администратора семейства сайтов. Например после назначения разрешений можно Сохраните текстовый файл, содержащий список OneDrive для бизнеса сайтов и добавьте строку к нему, которое идентифицирует пользователя, который назначен в качестве администратора семейства сайтов.
    
- Пользователи могут просматривать список administators семейства сайтов для их OneDrive для бизнеса сайта. Поскольку пользователи, администратор семейства сайтов для собственных OneDrive для бизнеса сайта, их удаление администраторов семейства сайтов. Попробуйте выполнить следующие действия, чтобы снизить вероятность пользователи удаление пользователей, которым назначена разрешения обнаружения электронных данных в OneDrive для бизнеса сайтов.
    
  - Сообщите пользователям, что в целях обнаружения электронных данных и обеспечения соответствия требованиям, специалисты по соответствию требованиям была назначена администратором семейства сайтов в OneDrive для бизнеса сайтов в вашей организации.
    
  - Повторно запустите скрипт в шаге 3, если необходимо, чтобы повторно назначить пользователя как администратора семейства сайтов для OneDrive для бизнеса сайтов.
    
- Можно также использовать скрипта, выполняемого на шаге 3 для удаления пользователя как администратора семейства сайтов из службы OneDrive для бизнеса сайтов. Чтобы удалить пользователя как администратора семейства сайтов, необходимо изменить следующую команду (в конце скрипта) из: 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    на:
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    Кроме того, можно изменить следующую строку с:

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    на:
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    После внесения изменений сохранить сценарий с другим именем, например OD4BRemoveSCA.ps1 и затем использовать его для удаления пользователя из группы OneDrive для бизнеса сайтов как администратора семейства сайтов.
