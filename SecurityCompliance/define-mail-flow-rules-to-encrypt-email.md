---
title: Определение правил для потока обработки почты для шифрования сообщений электронной почты в Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 9b7daf19-d5f2-415b-bc43-a0f5f4a585e8
description: Как глобальный администратор Office 365 можно создать почты поток правила для включения шифрования сообщений Office 365 (OME). Можно шифровать исходящие сообщения электронной почты и удалить шифрование из внутренних сообщений или из ответов на зашифрованные сообщения, отправленные из вашей организации.
ms.openlocfilehash: 06668f29e69c885adb8c67d723efe42b4a4aa166
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534510"
---
# <a name="define-mail-flow-rules-to-encrypt-email-messages-in-office-365"></a>Определение правил для потока обработки почты для шифрования сообщений электронной почты в Office 365

Как глобальный администратор Office 365 можно создать правила потока почты, также известной как правила транспорта, для защиты сообщений электронной почты, отправляемых и получаемых. Можно настроить правила для шифрования исходящие сообщения электронной почты и удалить шифрование из зашифрованных сообщений, поступающих от внутри организации или из ответов на зашифрованные сообщения, отправленные из вашей организации. Центр администрирования Exchange (EAC) или командлетов Windows PowerShell для Exchange Online можно использовать для создания следующих правил. Помимо общего правила шифрования также можно включить или отключить отдельные сообщения параметры шифрования для конечных пользователей.
  
Если вы недавно перенесены из службы управления правами для защиты информации Azure, вам потребуются для просмотра существующих правил поток почты чтобы убедиться, что они продолжать работать в новой среде. Кроме того Если необходимо воспользоваться преимуществами новых возможностей шифрования сообщений Office 365 (OME), доступных вам защита информации Azure, вам потребуется обновить существующие правила поток почты. В противном случае пользователи будут предоставляться зашифрованных сообщений в формате предыдущей HTML вложения вместо нового эффективной работы OME. Если вы еще не OME еще не настроена, [Настройте новые возможности шифрования сообщений Office 365, построенные защита информации Azure](set-up-new-message-encryption-capabilities.md) сведения см. 
  
Сведения о компонентах, которые составляют правила потока почты и как правила рабочего потока почты см [почтовые поток правил (правил транспорта) в Exchange Online](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx). Для получения дополнительных сведений о работе с Azure Information Protection правила потока почты см. [Настройка Exchange Online правила потока обработки почты для защиты информации Azure метки](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-exo-rules).
  
## <a name="create-a-mail-flow-rule-to-encrypt-email-messages-with-the-new-ome-capabilities"></a>Создание правила потока обработки почты для шифрования сообщений электронной почты с новыми возможностями OME

Можно определить правила потока обработки почты для активации шифрования сообщений с новыми возможностями OME с помощью центра администрирования Exchange.
  
### <a name="to-create-a-rule-for-encrypting-email-messages-with-the-new-ome-capabilities-by-using-the-eac"></a>Создание правила для шифрования сообщений электронной почты с новыми возможностями OME с помощью центра администрирования Exchange

1. В веб-браузере с помощью учетной записи рабочего или школы, которому предоставлены разрешения глобального администратора, [войти в Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Выберите плитку **администрирования** . 
    
3. Откроется Центр администрирования Office 365. Здесь выберите последовательно элементы **Центры администрирования** \> **Exchange**.
    
4. В центре администрирования Exchange последовательно выберите пункты **поток обработки почты** \> **правил** \> ![новый значок](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) ( **New**) \> **Создать новое правило**. Дополнительные сведения об использовании центра администрирования Exchange можно [Центр администрирования Exchange в Exchange Online](https://technet.microsoft.com/library/jj200743%28v=exchg.150%29.aspx).
    
5. В поле **имя**введите имя правила, например Encrypt mail for DrToniRamos@hotmail.com.
    
6. В разделе **Применить это правило, если** выберите условие и введите значение, если это необходимо. Например, для шифрования сообщений, направленных по адресу DrToniRamos@hotmail.com: 
    
    1. В разделе **Применить это правило, если** выберите **получатель**.
    
    2. Выберите существующее имя из списка контактов или введите новый адрес электронной почты в поле **проверить имена**. 
    
        Чтобы выбрать существующее имя, выберите его в списке и нажмите **ОК**.
    
        Введите новое имя, введите адрес электронной почты в поле **Проверить имена** , а затем выберите **Проверить имена** \> **кнопку ОК**.
    
7. Чтобы добавить дополнительные условия, нажмите кнопку **Дополнительные параметры** , а затем нажмите кнопку **Добавить условие** и выберите из списка. 
    
    К примеру, чтобы правило применяется, только если получатель находится за пределами вашей организации, выберите **Добавить условие** и затем выберите **получатель внешнего и внутреннего** \> **за пределами организации** \> **кнопку ОК**.
    
8. Включение шифрования с помощью новых возможностей OME, из, **выполните следующие действия**, выберите **Изменить безопасность сообщения** и нажмите кнопку **применить шифрование сообщений Office 365 и защите прав**. Выберите в списке шаблон службы управления правами, выберите команду **Сохранить**и нажмите кнопку **ОК**.
    
    Список шаблонов содержит все шаблоны по умолчанию и параметры, а также все пользовательские шаблоны, которые вы создали для использования с Office 365. Если список пуст, убедитесь, что настройки шифрования сообщений Office 365 с новыми возможностями как описано в [Set up новые возможности шифрования сообщений Office 365, построенный на верхней части Защита информации Azure](set-up-new-message-encryption-capabilities.md). Для получения сведений о шаблонах по умолчанию видеть [Настройка и управление шаблонами для защиты информации Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Сведения о параметре **Не пересылать** [не пересылать варианта по электронной почте](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)см. Сведения о параметре **шифровать только** [параметр шифрования только для сообщений электронной почты](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)см.
    
    Вы можете **Добавить действие** при указании другого действия. 
    
### <a name="to-update-an-existing-mail-flow-rule-to-use-the-new-ome-capabilities-by-using-the-eac"></a>Для обновления существующего правила потока обработки почты для использования новых возможностей OME с помощью центра администрирования Exchange

1. В веб-браузере с помощью учетной записи рабочего или школы, которому предоставлены разрешения глобального администратора, [войти в Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Выберите плитку **администрирования** . 
    
3. Откроется Центр администрирования Office 365. Здесь выберите последовательно элементы **Центры администрирования** \> **Exchange**.
    
4. В центре администрирования Exchange последовательно выберите пункты **поток обработки почты** \> **правила**.
    
5. В списке правил потока почты выберите правило, который требуется изменить для использования новых возможностей OME, а затем нажмите ![значок Правка](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif) ( **Изменить**).
    
6. Включение шифрования с помощью новых возможностей OME, из, **выполните следующие действия**, выберите команду **Изменить безопасность сообщения** и нажмите кнопку **применить шифрование сообщений Office 365 и защите прав**. Выберите в списке шаблон службы управления правами, выберите команду **Сохранить** и нажмите кнопку **ОК**.
    
    Список шаблонов содержит все шаблоны по умолчанию и параметры, а также все пользовательские шаблоны, которые вы создали для использования с Office 365. Если список пуст, убедитесь, что настройки шифрования сообщений Office 365 с новыми возможностями как описано в [Set up новые возможности шифрования сообщений Office 365, построенный на верхней части Защита информации Azure](set-up-new-message-encryption-capabilities.md). Для получения сведений о шаблонах по умолчанию видеть [Настройка и управление шаблонами для защиты информации Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Сведения о параметре **Не пересылать** [не пересылать варианта по электронной почте](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)см. Сведения о параметре **шифровать только** [параметр шифрования только для сообщений электронной почты](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)см.
    
    Вы можете **Добавить действие** при указании другого действия. 
    
7. В списке, **выполните следующие действия,** удалите все действия, которые были им назначены **Изменить безопасность сообщения** \> **Применить предыдущей версии OME**.
    
8. Нажмите **Сохранить**.
    
## <a name="creating-rules-for-office-365-message-encryption-without-the-new-capabilities"></a>Создание правил для шифрования сообщений Office 365 без новые возможности

Если еще не перемещены организации Office 365 новые возможности OME, используйте эти задачи для определения правил для потока обработки почты для шифрования сообщений для вашей организации. Корпорация Майкрософт рекомендует, чтобы сделать план для перемещения новых возможностей OME, как только целесообразно для вашей организации. Сведения содержатся в разделе [Set up новые возможности шифрования сообщений Office 365, построенные защита информации Azure](set-up-new-message-encryption-capabilities.md).
  
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-the-eac"></a>Создание правила для шифрования сообщений электронной почты без новых возможностей OME с помощью центра администрирования Exchange

1. В веб-браузере с помощью учетной записи рабочего или школы, которому предоставлены разрешения глобального администратора, [войти в Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Выберите плитку **администрирования** . 
    
3. Откроется Центр администрирования Office 365. Здесь выберите последовательно элементы **Центры администрирования** \> **Exchange**.
    
4. В центре администрирования Exchange последовательно выберите пункты **поток обработки почты** \> **правил** \> **+** ( **New**) \> **Создать новое правило**. Дополнительные сведения об использовании центра администрирования Exchange можно [Центр администрирования Exchange в Exchange Online](https://technet.microsoft.com/library/jj200743%28v=exchg.150%29.aspx).
    
5. В поле **имя**введите имя правила, например Encrypt mail for DrToniRamos@hotmail.com.
    
6. В разделе **Применить это правило, если** выберите условие и введите значение, если это необходимо. Например, для шифрования сообщений, направленных по адресу DrToniRamos@hotmail.com: 
    
1. В разделе **Применить это правило, если** выберите **получатель**.
    
2. Выберите существующее имя из списка контактов или введите новый адрес электронной почты в поле **проверить имена**. 
    
    Чтобы выбрать существующее имя, выберите его в списке и нажмите **ОК**.
    
    Введите новое имя, введите адрес электронной почты в поле **Проверить имена** , а затем выберите **Проверить имена** \> **кнопку ОК**.
    
7. Чтобы добавить дополнительные условия, нажмите кнопку **Дополнительные параметры** и затем выберите **Добавить условие** и выберите из списка. 
    
    К примеру, чтобы правило применяется, только если получатель находится за пределами вашей организации, выберите **Добавить условие** и затем выберите **получатель внешнего и внутреннего** \> **за пределами организации** \> **кнопку ОК**.
    
8. Чтобы включить шифрование без использования новых возможностей OME, **выполните следующие действия**, выберите команду **Изменить безопасность сообщения** \> **Применить предыдущей версии OME**и нажмите кнопку **Сохранить**.
    
    При появлении сообщения об ошибке, лицензирование IRM не включена, а затем вы не установили OME для вашей организации еще. Если вы хотите настроить OME, должна настроить его для использования новых возможностей OME. [Настройте новые возможности шифрования сообщений Office 365, построенные защита информации Azure](set-up-new-message-encryption-capabilities.md)сведения см. Microsoft больше не поддерживает установку новых развертываний OME без новые возможности.
    
    Вы можете **Добавить действие** при указании другого действия. 
    
### <a name="to-create-a-rule-for-encrypting-email-messages-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Создание правила для шифрования сообщений электронной почты без новых возможностей OME с помощью Windows PowerShell для Exchange Online

1. Для создания удаленного сеанса PowerShell в Exchange Online с помощью Windows PowerShell на локальном компьютере. Дополнительные сведения можно [Подключить к Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
    
2. Определение правила с помощью командлета **New-TransportRule** и присвойте атрибуту **ApplyOME** **значение true**.
    
    Например если требуется, что все сообщения электронной почты, адресованное DrToniRamos@hotmail.com должен быть зашифрован, введите следующую команду:
    
     ```
     New-TransportRule -Name "Encrypt rule for Dr Toni Ramos" -SentTo "DrToniRamos@hotmail.com" -SentToScope "NotinOrganization" -ApplyOME $true
     ```

    В этом примере:
    
  - Имя нового правила — «Зашифровать правила для аварийного восстановления Toni Ramos».
    
  - Параметр **- SentTo** указывает условие, которая выглядит для получателей в сообщениях электронной почты. Можно использовать любое значение, уникальным образом идентифицирующее получателя, например, адрес электронной почты, имя, различающееся имя (DN), и т.д. В этом примере получателя идентифицируется «DrToniRamos@hotmail.com» адрес электронной почты. 
    
  - Параметр **- Senttoscope расположение** указывает условие, которое выполняет поиск расположения получателей. В этом примере почтовый ящик получателя находится в hotmail и не является частью организации Office 365, поэтому используется значение «NotInOrganization». 
    
    Дополнительные сведения об условиях, можно настроить на правил поток почты с помощью этого командлета содержатся в разделе [New-TransportRule](https://technet.microsoft.com/en-us/library/bb125138%28v=exchg.160%29.aspx).
    
### <a name="remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities"></a>Удалить шифрование из ответов на зашифрованные без новые возможности OME

Когда пользователи электронной почты отправлять зашифрованные сообщения, получателей копии сообщения может ответить с зашифрованные ответов. Можно создать почты поток правила для автоматического удаления шифрования из ответов на пользователей электронной почты в организации достаточно выполнить вход на портал шифрования для их просмотра. Центр администрирования Exchange или командлетов Windows PowerShell можно использовать для определения эти правила. Если вы еще не используете новые возможности OME, может расшифровать только сообщения, которые являются либо отправляются из внутри организации или сообщений, которые являются ответами на сообщения, отправленные из вашей организации. Не удалось расшифровать зашифрованные сообщения, исходящие от за пределами вашей организации.
  
#### <a name="to-create-a-rule-for-removing-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-the-eac"></a>Создание правила для удаления шифрования из ответов на зашифрованные без новых возможностей OME с помощью центра администрирования Exchange
<a name="DecryptruleEACNoNewOME"> </a>

1. В веб-браузере с помощью учетной записи рабочего или школы, которому предоставлены разрешения администратора для [входа в Office 365](https://support.office.com/article/Sign-in-to-Office-or-Office-365-b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).
    
2. Выберите плитку **администрирования** . 
    
3. Откроется Центр администрирования Office 365. Здесь выберите последовательно элементы **Центры администрирования** \> **Exchange**.
    
4. В центре администрирования Exchange последовательно выберите пункты **поток обработки почты** \> **правил** \> **+** ( **New**) \> **Создать новое правило**. Дополнительные сведения об использовании центра администрирования Exchange можно [Центр администрирования Exchange в Exchange Online](https://technet.microsoft.com/en-us/library/jj200743%28v=exchg.150%29.aspx).
    
5. В поле **имя**введите имя для правила, например Remove encryption from входящей почты.
    
6. В **Применить это правило, если** выберите условия, где необходимо удалить шифрование из сообщений, например **получатель находится** \> **в организации**.
    
7. В, **выполните следующие действия**, выберите **Изменить безопасность сообщения** \> **удалить предыдущую версию OME**.
    
8. Нажмите кнопку **Сохранить**.
    
#### <a name="to-create-a-rule-to-remove-encryption-from-email-replies-encrypted-without-the-new-ome-capabilities-by-using-windows-powershell-for-exchange-online"></a>Создание правила для удаления шифрования из ответов на зашифрованные без новых возможностей OME с помощью Windows PowerShell для Exchange Online
<a name="DecryptrulePShellNoNewOME"> </a>

1. Для создания удаленного сеанса PowerShell в Exchange Online с помощью Windows PowerShell на локальном компьютере. Дополнительные сведения можно [Подключить к Exchange Online PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
    
2. Определение правила с помощью командлета **New-TransportRule** и присвойте атрибуту **RemoveOME** **значение true**.
    
    Например чтобы удалить шифрование все сообщения, отправленные получателям в организации Office 365, введите следующую команду:
    
     ```
     New-TransportRule - Name "Remove encryption from incoming mail"     -SentToScope "InOrganization" -RemoveOME $true
     ```

    В этом примере:
    
  - Имя нового правила — «Remove encryption from incoming mail».
    
  - Параметр **- Senttoscope расположение** указывает условие, которое выполняет поиск расположения получателей. В этом примере используется значение «InOrganization» указывающее, что: 
    
  - Получатель является почтового ящика, почтового пользователя, группы или общей папки с поддержкой почты в вашей организации или
    
  - Электронный адрес получателя находится на обслуживаемом домене, настроенном в качестве домена внутренней ретрансляции или уполномоченного домена, и сообщение было отправлено или получено через подключение с проверкой подлинности.
    
    Дополнительные сведения об условиях, можно настроить на правил поток почты с помощью этого командлета содержатся в разделе [New-TransportRule](https://technet.microsoft.com/en-us/library/bb125138%28v=exchg.160%29.aspx).
    
## <a name="related-topics"></a>Статьи по теме

[Шифрование в Office 365](encryption.md)
  
[Настройка новых возможностей шифрования сообщений Office 365, построенные защита информации Azure](set-up-new-message-encryption-capabilities.md)
  
[Добавление фирменной символики в зашифрованные сообщения](add-your-organization-brand-to-encrypted-messages.md)
  
[Правила потока обработки почты (правила транспорта) в Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=506707)
  
[Правила потока обработки почты (правила транспорта) в Exchange Online Protection](https://go.microsoft.com/fwlink/p/?LinkId=506708)
  
