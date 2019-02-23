---
title: Настройка групп и пользователей в случае среды разработки и тестирования для политической кампании
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 0e22bcf3-bad3-42a4-b44f-276e0cf4790f
description: Сводка. Сведения о создании пробных подписок на Office 365 и Enterprise Mobility + Security (EMS) с пользователями и группами в случае среды разработки и тестирования для политической кампании.
ms.openlocfilehash: 098ae2c3005e0c6ba7939c52260b1a2c49dc557e
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223708"
---
# <a name="configure-groups-and-users-for-a-political-campaign-devtest-environment"></a>Настройка групп и пользователей в случае среды разработки и тестирования для политической кампании

 **Сводка.** Сведения о создании пробных подписок на Office 365 и Enterprise Mobility + Security (EMS) с пользователями и группами в случае среды разработки и тестирования для политической кампании.
  
Инструкции из этой статьи помогут создать среду разработки и тестирования, которая включает упрощенные учетные записи пользователей и группы. Она необходима для решения, упомянутого в статье [Руководство по безопасности (Майкрософт) для политических кампаний, некоммерческих и других динамических организаций](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md).
  
## <a name="phase-1-create-your-office-365-devtest-environment"></a>Этап 1. Создание среды разработки и тестирования Office 365

На этом этапе вы получите пробные подписки на Office 365 E5 и Enterprise Mobility + Security (EMS) E5 для вымышленной организации, которая проводит политическую кампанию.
  
Сначала следуйте инструкциям для **этапа 2**, указанного в [разделе о среде разработки и тестирования Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).
  
Затем оформите пробную подписку на EMS E5 и добавьте ее для той же организации, что и пробную подписку на Office 365.
  
1. Если необходимо, войдите на портал Office 365 с использованием учетных данных учетной записи глобального администратора пробной подписки. Справочные сведения см. в статье [Вход в Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).
    
2. Выберите плитку **Администрирование**.
    
3. Открыв вкладку **Центр администрирования Office** в браузере, на панели навигации слева щелкните **Выставление счетов > Приобретение служб**.
    
4. На странице **Приобретение служб** найдите элемент **Enterprise Mobility + Security E5**. Наведите на него указатель мыши и выберите **Начать бесплатный пробный период**.
    
5. На странице **Подтверждение заказа** нажмите кнопку **Попробовать**.
    
6. На странице **Получение заказа** нажмите кнопку **Продолжить**.
    
Затем включите лицензию на EMS E5 для своей учетной записи глобального администратора.
  
1. Открыв вкладку браузера **Центр администрирования Office 365**, на панели навигации слева выберите **Пользователи > Активные пользователи**.
    
2. Выберите свою учетную запись глобального администратора и щелкните ссылку **Изменить** для параметра **Лицензии на продукты**.
    
3. На панели **Лицензии на продукты** переведите переключатель **Enterprise Mobility + Security E5** в положение **Вкл.**, нажмите **Сохранить**, а затем дважды **Закрыть**.
    
## <a name="phase-2-create-and-configure-your-azure-active-directory-ad-groups"></a>Этап 2. Создание и настройка групп Azure Active Directory (AD)

На этом этапе создаются и настраиваются группы Azure AD для кампании.
  
Сначала создайте набор групп для обычной политической кампании на портале Azure.
  
1. Откройте портал Azure ([https://portal.azure.com](https://portal.azure.com)) на отдельной вкладке браузера. Если необходимо, выполните вход, используя данные учетной записи глобального администратора для пробной подписки на Office 365 E5.
    
2. На портале Azure последовательно выберите **Azure Active Directory > Пользователи и группы > Все группы**.
    
3. Выполните приведенные ниже шаги для каждой группы из этого списка:
    
  - "Старший и стратегический персонал";
    
  - "ИТ-персонал";
    
  - "Специалисты по аналитике";
    
  - "Основной штат сотрудников";
    
  - "Операционный персонал";
    
  - "Выездной персонал".
    
1. В колонке **Все группы** выберите пункт **+ Новая группа**.
    
2. Введите имя группы из списка в поле **Имя**.
    
3. Выберите **Динамический пользователь** для параметра **Членство**.
    
4. Выберите вариант **Да** для параметра **Включить функции Office**.
    
5. Выберите **Добавить динамический запрос**.
    
6. В поле **Место добавления пользователей** выберите **Отдел**.
    
7. В следующем поле выберите **Равно**.
    
8. В следующем поле введите имя группы из списка.
    
9. Выберите **Добавить запрос** > **Создать**.
    
10. Выберите **Пользователи и группы — Все группы**.
    
Затем настройте группы так, чтобы их членам автоматически назначались лицензии на Office 365 E5 и EMS E5.
  
1. На портале Azure последовательно выберите **Azure Active Directory > Лицензии > Все продукты**.
    
2. В списке выберите **Enterprise Mobility + Security E5** и **Office 365 корпоративный E5**, затем нажмите **+ Назначить**.
    
3. В колонке **Назначение лицензии** щелкните **Пользователи и группы**.
    
4. В списке выберите следующие группы:
    
  - Специалисты по аналитике
    
  - Выездной персонал
    
  - ИТ-персонал
    
  - Операционный персонал
    
  - Основной штат сотрудников
    
  - Старший и стратегический персонал
    
5. Выберите **Выбрать** > **Назначить**.
    
6. Закройте вкладку портала Azure в браузере.
    
## <a name="phase-3-add-your-user-accounts"></a>Этап 3. Добавление учетных записей пользователей

На этом этапе добавляются демонстрационные учетные записи пользователей для политической кампании.
  
Вначале [подключитесь с использованием модуля Azure Active Directory 2 для PowerShell](https://go.microsoft.com/fwlink/?linkid=842218).
  
Затем введите название организации, адрес и общий пароль и выполните эти команды в командной строке PowerShell или интегрированной среде сценариев (ISE):
  
```
$orgName="<organization name, such as contoso for the contoso.onmicrosoft.com trial subscription domain name>"
$location="<the ISO ALPHA2 country code, such as US for the United States>"
$commonPassword="<common password for all the new accounts>"

$PasswordProfile=New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password=$commonPassword

$deptName="Senior and strategic staff"
$userNames=@("Candidate","ChiefOfStaff","Strategic1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="IT staff"
$userNames=@("ITAdmin1","ITAdmin2") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Analytics staff"
$userNames=@("DataScientist1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Regular core staff"
$userNames=@("Regular1","Regular2") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Operations staff"
$userNames=@("Operations1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }
$deptName="Field staff"
$userNames=@("FieldConsultant1") 
foreach ($element in $userNames){ New-AzureADUser -DisplayName $element -PasswordProfile $PasswordProfile -UserPrincipalName ($element + "@" + $orgName + ".onmicrosoft.com") -AccountEnabled $true -MailNickName $element -Department $deptName -UsageLocation $location }

```

> [!IMPORTANT]
> Общий пароль используется для автоматизации и упрощения настройки среды разработки и тестирования. Не рекомендуется для рабочих подписок. При входе в каждую из этих новых учетных записей пользователя вам будут показаны запросы на изменение пароля. 
  
Чтобы проверить динамическое членство в группах и групповое лицензирование:
  
1. На вкладке браузера **Домашняя страница Microsoft Office** щелкните плитку **Администрирование**.
    
2. На новой вкладке браузера **Центр администрирования Office** щелкните **Пользователи**.
    
3. В списке пользователей выберите **Кандидат**.
    
4. В области свойств учетной записи **Кандидат** убедитесь, что:
    
  - она входит в состав группы **Старший и стратегический персонал** (в разделе **Членство в группах**);
    
  - ей назначены лицензии на **Enterprise Mobility + Security E5** и **Office 365 корпоративный E5** (в разделе **Лицензии на продукты**).
    
5. Закройте область учетной записи пользователя **Кандидат**.
    
## <a name="record-values-for-future-reference"></a>Запишите значения для дальнейшего использования

Запишите эти значения для работы с пробными подписками Office 365 и EMS для этой среды разработки и тестирования:
  
- Название вашей организации: ![](./media/Common-Images/TableLine.png) 
    
    Например, для доменного имени contoso.onmicrosoft.com название организации — "contoso".
    
- Имя глобального администратора Office 365: ![](./media/Common-Images/TableLine.png).onmicrosoft.com
    
    Запишите пароль для этой учетной записи и общий первоначальный пароль для других учетных записей пользователей в надежном месте.
    
## <a name="next-step"></a>Следующий этап

Создайте четыре типа для сайтов группы SharePoint Online в этой среде разработки и тестирования, следуя инструкциям из статьи [Создание сайтов группы в среде разработки и тестирования для политической кампании](create-team-sites-in-a-political-campaign-dev-test-environment.md).
  
## <a name="see-also"></a>См. также

[Руководство по безопасности (Майкрософт) для политических кампаний, некоммерческих и других динамических организаций](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[Создание сайтов группы в среде разработки и тестирования для политической кампании](create-team-sites-in-a-political-campaign-dev-test-environment.md)
  
[Руководства по лаборатории тестирования для облачных решений](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[Освоение облака и гибридные решения](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




