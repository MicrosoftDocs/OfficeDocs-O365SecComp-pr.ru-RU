---
title: Среда разработки и тестирования изолированного сайта группы SharePoint Online
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- TLG
- Ent_TLGs
ms.assetid: d1795031-beef-49ea-a6fc-5da5450d320d
description: Сводка. Настройте сайт группы SharePoint Online, изолированный от остальной организации, в среде Office 365 для разработки и тестирования.
ms.openlocfilehash: a8a02c10f799b136b299801a3636820e4f64e087
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217139"
---
# <a name="isolated-sharepoint-online-team-site-devtest-environment"></a>Среда разработки и тестирования изолированного сайта группы SharePoint Online

 **Сводка.** Настройте сайт группы SharePoint Online, изолированный от остальной организации, в среде Office 365 для разработки и тестирования.
  
Сайты групп SharePoint Online в Office 365 — это расположения для совместной работы с помощью общей библиотеки документов, записной книжки OneNote и других служб. Во многих случаях требуется широкий доступ и совместная работа между отделами и организациями. Однако в некоторых случаях необходимо управлять доступом и разрешениями для совместной работы небольшой группы пользователей.
  
Доступ к сайтам группы SharePoint Online и к каким пользователям можно управлять с помощью групп SharePoint и уровней разрешений. По умолчанию сайты SharePoint Online имеют три уровня доступа:
  
- **Участники** могут просматривать, создавать и изменять ресурсы на сайте.
    
- **Владельцы** могут полностью контролировать сайт, в том числе изменять разрешения.
    
- **Посетители** могут просматривать ресурсы на сайте.
    
В этой статье описывается настройка изолированного сайта группы SharePoint Online для секретного проекта исследований с именем ProjectX. Требования доступа:
  
- Только участники проекта могут получить доступ к сайту и его содержимому (документам, записной книжке OneNote, страницам), уровни разрешений SharePoint на просмотр и редактирование определяются членством в группе.
    
- Только создатель сайта и члены группы администраторов сайта могут выполнять администрирование сайта, в том числе изменять разрешения на уровне сайта.
    
Настройка изолированного сайта группы SharePoint Online в среде Office 365 для разработки и тестирования выполняется в три этапа:
  
1. Создание среды разработки и тестирования Office 365.
    
2. Создание пользователей и групп для ProjectX.
    
3. Создание сайта группы SharePoint Online для ProjectX и его изоляция.
    
> [!TIP]
> Щелкните [здесь](http://aka.ms/catlgstack), чтобы просмотреть схему всех статей, относящихся к руководствам по лаборатории тестирования в One Microsoft Cloud.
  
## <a name="phase-1-build-out-your-lightweight-or-simulated-enterprise-office-365-devtest-environment"></a>Этап 1. Создание среды разработки и тестирования Office 365 — упрощенной или для имитированных предприятий

Если вы хотите просто создать изолированный сайт группы SharePoint Online с минимальными требованиями, следуйте инструкциям в статье этапы 2 и 3 из [среды разработки и тестирования Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment).
  
Если вы хотите создать изолированный сайт группы SharePoint Online в смоделированной конфигурации предприятия, следуйте инструкциям в статье [DirSync для среды разработки и тестирования Office 365](https://docs.microsoft.com/office365/enterprise/dirsync-for-your-office-365-dev-test-environment).
  
> [!NOTE]
> Для создания изолированного сайта SharePoint Online не требуется имитированная среда разработки и тестирования предприятия, которая включает имитированную интрасеть, подключенную к Интернету, и синхронизацию каталогов для леса Windows Server AD. Она указана здесь, чтобы вы могли протестировать изолированный сайт SharePoint Online и поэкспериментировать с ним в среде, которая представляет типичную среду для организаций. 
  
## <a name="phase-2-create-user-accounts-and-access-groups"></a>Этап 2: создание учетных записей пользователей и групп доступа

Воспользуйтесь инструкциями из статьи [Подключение к office 365 PowerShell](https://technet.microsoft.com/library/dn975125.aspx) , чтобы подключиться к вашей подПиске на Office 365 с учетной записью глобального администратора из:
  
- компьютера (для упрощенной среды разработки и тестирования Office 365);
    
- виртуальной машины CLIENT1 (для среды Office 365 для разработки и тестирования смоделированного предприятия).
    
Чтобы создать новые группы доступа для сайта группы SharePoint Online ProjectX, выполните следующие команды в командной консоли Windows Azure Active Directory для Windows PowerShell:
  
```
$groupName="ProjectX-Members"
$groupDesc="People allowed to collaborate for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Admins"
$groupDesc="People allowed to administer SharePoint for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
$groupName="ProjectX-Viewers"
$groupDesc="People allowed to view the SharePoint resources for ProjectX."
New-MsolGroup -DisplayName $groupName -Description $groupDesc
```

> [!TIP]
> Щелкните [здесь](https://gallery.technet.microsoft.com/PowerShell-commands-for-an-b2608df1) , чтобы получить текстовый файл, который содержит все команды PowerShell, описанные в этой статье.
  
Введите название организации (например, contosotoycompany) и двузначный код страны, а затем выполните следующие команды в командной строке модуля Windows Azure Active Directory для Windows PowerShell:
  
```
$orgName="<organization name>"
$loc="<two-character country code, such as US>"
$licAssignment= $orgName + ":ENTERPRISEPREMIUM"
$userName= "designer@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Designer" -FirstName Lead -LastName Designer -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

Запишите в надежном месте пароль, созданный командой **New-MsolUser** для учетной записи ведущего дизайнера.
  
Выполните следующие команды в командной строке модуля Windows Azure Active Directory для Windows PowerShell:
  
```
$userName= "researcher@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Lead Researcher" -FirstName Lead -LastName Researcher -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

Запишите в надежном месте пароль, созданный командой **New-MsolUser** для учетной записи ведущего научного сотрудника.
  
Выполните следующие команды в командной строке модуля Windows Azure Active Directory для Windows PowerShell:
  
```
$userName= "devvp@" + $orgName + ".onmicrosoft.com"
New-MsolUser -DisplayName "Development VP" -FirstName Development -LastName VP -UserPrincipalName $userName -UsageLocation $loc -LicenseAssignment $licAssignment -ForceChangePassword $false
```

Запишите в надежном месте пароль, созданный командой **New-MsolUser** для учетной записи вице-президента по развитию.
  
Затем, чтобы добавить новые учетные записи в новые группы доступа, выполните следующие команды PowerShell в командной строке модуля Windows Azure Active Directory для Windows PowerShell:
  
```
$grpName="ProjectX-Members"
$userUPN="designer@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$userUPN="researcher@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Admins"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userCredential.UserName }).ObjectID -GroupMemberType "User"
$grpName="ProjectX-Viewers"
$userUPN="devvp@" + $orgName + ".onmicrosoft.com"
Add-MsolGroupMember -GroupObjectId (Get-MsolGroup | Where { $_.DisplayName -eq $grpName }).ObjectID -GroupMemberObjectId (Get-MsolUser | Where { $_.UserPrincipalName -eq $userUPN }).ObjectID -GroupMemberType "User"
```

Результаты:
  
- Группа доступа ProjectX – Members содержит сведения об дизайнере и учетных записях ведущего сотрудника.
    
- Группа доступа ProjectX — администраторы содержит учетную запись глобального администратора для пробной подписки.
    
- Группа доступа ProjectX – просматривающий содержит учетную запись пользователя ВИЦЕs Development
    
На рисунке 1 показаны группы доступа и их членство.
  
**Рис. 1**

![Группы Office 365 и их участники для изолированного сайта группы SharePoint Online](media/5b7373b9-2a80-4880-afe5-63ffb17237e6.png)
  
## <a name="phase-3-create-a-new-projectx-sharepoint-online-team-site-and-isolate-it"></a>Этап 3. Создание сайта группы SharePoint Online для ProjectX и его изоляция

Чтобы создать сайт группы SharePoint Online для ProjectX, выполните перечисленные ниже действия.
  
1. С помощью браузера на локальном компьютере (облегченная настройка) или на компьютере CLIENT1 (смоделированная конфигурация предприятия) Войдите на портал Office 365 ([https://portal.office.com](https://portal.office.com)), используя учетную запись глобального администратора.
    
2. В списке плиток выберите **SharePoint**.
    
3. На новой вкладке SharePoint в браузере щелкните **+ Создать сайт**.
    
4. В окне **имя сайта группы**введите **projectx**. В окне **Параметры конфиденциальности**выберите пункт **частные пользователи могут получать доступ к этому сайту**.
    
5. В поле **Описание сайта группы** введите **Сайт SharePoint для ProjectX** и нажмите кнопку **Далее**.
    
6. В списке **кого вы хотите добавить**? Нажмите кнопку **Готово**.
    
7. В новой вкладке **Главная, ProjectX** в браузере, на панели инструментов, щелкните значок параметров и выберите **Разрешения для сайта**.
    
8. В области **Разрешения для сайта** щелкните **Параметры дополнительных разрешений**.
    
9. В новой вкладке **Разрешения: Project X** в браузере нажмите **Параметры запросов на доступ**.
    
10. В диалоговом окне **Параметры запросов на доступ** снимите флажки **Разрешить участникам совместный доступ к этому сайту, а также отдельным файлам и папкам** и **Разрешить запросы на доступ** (все три флажка должны быть сняты) и нажмите кнопку **ОК**.
    
11. Выберите **ProjectX — участники** в списке.
    
12. На странице **Пользователи и группы** нажмите кнопку **Создать**.
    
13. В диалоговом окне **Общий доступ** введите **ProjectX-Members**, выберите группу и нажмите **Поделиться**.
    
14. Нажмите кнопку "Назад" в браузере.
    
15. Выберите **ProjectX — владельцы** в списке.
    
16. На странице **Пользователи и группы** нажмите кнопку **Создать**.
    
17. В диалоговом окне **Общий доступ** введите **ProjectX-Admins**, выберите группу и нажмите **Поделиться**.
    
18. Нажмите кнопку "Назад" в браузере.
    
19. Выберите **ProjectX — посетители** в списке.
    
20. На странице **Пользователи и группы** нажмите кнопку **Создать**.
    
21. В диалоговом окне **Общий доступ** введите **ProjectX-Viewers**, выберите группу и нажмите **Поделиться**.
    
22. Закройте вкладку **Пользователи и группы** в браузере, перейдите на вкладку **Главная, ProjectX** в браузере и закройте область **Разрешения для сайта**.

    
Ниже приведены результаты настройки разрешений.
  
- Группа ProjectX Members содержит только группу доступа ProjectX-Members (которая содержит только учетные записи ведущего дизайнера и ведущего пользователя) и группу ProjectX (которая содержит только учетную запись глобального администратора).
    
- Группа SharePoint Owners ProjectX содержит только группу доступа ProjectX-Admins (которая содержит только учетную запись глобального администратора).
    
- Группа SharePoint "Посетители ProjectX" содержит только группу доступа ProjectX-просматривающих (которая содержит только учетную запись "вице-президент разработки").
    
- Участники не могут изменять разрешения на уровне сайта (это могут делать только члены группы ProjectX-Admins).
    
- Другие учетные записи пользователей не могут получить доступ к сайту и его ресурсам и запросить доступ к нему.
    
На рисунке 2 показаны группы SharePoint и их участники.
  
**Рис. 2**

![Группы SharePoint Online и их участники для изолированного сайта группы SharePoint Online](media/595abff4-64f9-49de-a37a-c70c6856936b.png)
  
Теперь рассмотрим доступ, используя учетную запись пользователя конструктора ведущего:
  
1. Закройте вкладку **Главная, ProjectX** в браузере и перейдите на вкладку **Домашняя страница Microsoft Office**.
    
2. Щелкните имя глобального администратора и нажмите **Выйти**.
    
3. Войдите на портал Office 365 ([https://portal.office.com](https://portal.office.com)), используя имя и пароль учетной записи ведущего дизайнера.
    
4. В списке плиток выберите **SharePoint**.
    
5. На новой вкладке **SharePoint** в браузере введите **projectx** в поле поиска, активируйте Поиск, а затем щелкните сайт группы **projectx** . В браузере должна появиться новая вкладка для сайта группы ProjectX.
    
6. Щелкните значок параметров. Обратите внимание, что параметр **Разрешения для сайта** отсутствует, так как только члены группы ProjectX-Admins могут изменять разрешения для сайта.
    
7. Откройте приложение "Блокнот" или другой текстовый редактор.
    
8. Скопируйте URL-адрес сайта группы ProjectX и вставьте его в новой строке в приложении "Блокнот" или другом текстовом редакторе.
    
9. На новой вкладке **Главная, ProjectX** в браузере нажмите **Документы**.
    
10. Скопируйте URL-адрес папки документов ProjectX и вставьте его в новой строке в Блокноте или другом текстовом редакторе.
    
11. В новой вкладке **ProjectX — Документы** в браузере нажмите **Создать > Документ Word**.
    
12. Введите текст на странице **Word Online**, дождитесь состояния **Сохранено**, нажмите кнопку "Назад" в браузере и обновите страницу. В папке **Документы** появится новый файл **Документ.docx**.
    
13. Нажмите кнопку с многоточием в документе **Document. docx** и выберите команду **получить ссылку**.
    
14. Скопируйте URL-адрес в диалоговом окне **общий доступ к Document. docx** и вставьте его в новую строку в блокноте или в текстовом редакторе, а затем закройте диалоговое окно **общий файл document. docx** .
    
15. Закройте вкладки **ProjectX — Документы** и **SharePoint** в браузере и перейдите на вкладку **Домашняя страница Microsoft Office**.
    
16. Щелкните имя **ведущего дизайнера** и нажмите **Выйти**.

    
Теперь рассмотрим доступ, используя учетную запись "вице — президент по разработке":
  
1. Войдите на портал Office 365 (),[https://portal.office.com](https://portal.office.com)используя имя и пароль учетной записи вице-президента по разработке.
    
2. В списке плиток выберите **SharePoint**.
    
3. На новой вкладке **SharePoint** в браузере введите **projectx** в поле поиска, активируйте Поиск, а затем щелкните сайт группы **projectx** . В браузере должна появиться новая вкладка для сайта группы ProjectX.
    
4. Нажмите **Документы** и выберите файл **Документ.docx**.
    
5. Во вкладке **Документ.docx** в браузере попробуйте изменить текст. Вы увидите сообщение о том, что **этот документ доступен только для чтения**, так как у учетной записи вице-президента по развитию есть только разрешения на просмотр сайта.
    
6. Закройте вкладки **Документ.docx**, **ProjectX — Документы** и **SharePoint** в браузере.
    
7. Перейдите на вкладку **Домашняя страница Microsoft Office**, щелкните имя **вице-президента по развитию** и нажмите **Выйти**.

    
Теперь рассмотрим доступ с учетной записью пользователя, не имеющей разрешений.
  
1. Войдите на портал Office 365 ([https://portal.office.com](https://portal.office.com)), используя имя учетной записи пользователя 3 и пароль.
    
2. В списке плиток выберите **SharePoint**.
    
3. 	В новой вкладке **SharePoint** введите **ProjectX** в поле поиска и активируйте поиск. Вы увидите сообщение **Нет результатов, соответствующих вашим условиям поиска**.
    
4. Скопируйте URL-адрес сайта ProjectX из открытого Блокнота или другого текстового редактора в адресную строку браузера и нажмите клавишу **Ввод**. Вы увидите страницу **Доступ запрещен**.
    
5. Скопируйте URL-адрес папки документов ProjectX из Блокнота или другого текстового редактора в адресную строку браузера и нажмите клавишу **Ввод**. Вы увидите страницу **Доступ запрещен**.
    
6. Скопируйте URL-адрес файла Документ.docx из Блокнота или другого текстового редактора в адресную строку браузера и нажмите клавишу **Ввод**. Вы увидите страницу **Доступ запрещен**.
    
7. Закройте вкладку **SharePoint** в браузере, перейдите на вкладку **Домашняя страница Microsoft Office**, щелкните имя **пользователя 3** и нажмите **Выйти**.

    
Теперь изолированный сайт SharePoint Online готов к выполнению дополнительного эксперимента.
  
## <a name="next-step"></a>Следующий этап

Когда вы будете готовы выполнить развертывание изолированного сайта группы SharePoint Online в рабочей среде, просмотрите подробные инструкции из статьи [Разработка изолированного сайта группы SharePoint Online](design-an-isolated-sharepoint-online-team-site.md).
  
## <a name="see-also"></a>См. также

[Изолированные сайты групп SharePoint Online](isolated-sharepoint-online-team-sites.md)
  
[Руководства по созданию сред разработки и тестирования облачных решений](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)
  
[Базовая конфигурация среды разработки и тестирования](https://docs.microsoft.com/office365/enterprise/base-configuration-dev-test-environment)
  
[Среда разработки и тестирования Office 365](https://docs.microsoft.com/office365/enterprise/office-365-dev-test-environment)
  
[Освоение облака и гибридные решения](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




