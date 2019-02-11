---
title: Добавление фирменного стиля организации в зашифрованные сообщения
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: Как администратор Exchange можно применять вашей организации фирменной символики в вашей организации зашифрованные сообщения электронной почты и содержимое портала шифрования.
ms.openlocfilehash: 4b22b72a8b77c2978a7cf25166978759119c272c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696223"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Добавление фирменной символики организации в зашифрованные сообщения

Как администратор Exchange Online или Exchange Online Protection можно применить вашей компании, фирменная символика настраивать внешний вид сообщений электронной почты вашей организации шифрования сообщений Office 365 и содержимое портала шифрования. Командлеты Get-OMEConfiguration и Set-OMEConfiguration Windows PowerShell можно настроить следующие аспекты возможности просмотра для получателей зашифрованные сообщения электронной почты:
  
- Вводный текст зашифрованного сообщения электронной почты
- Текст заявления об отказе зашифрованного сообщения электронной почты
- Текст, который отображается на портале OME
- Логотип, который отображается в сообщении электронной почты и портала OME
- Цвет фона в сообщение электронной почты и портала OME

Кроме того, в любое время вы можете восстановить интерфейс по умолчанию.

Если вы хотите больше контроля, можно создать несколько шаблонов для зашифрованного сообщения электронной почты, поступающих из вашей организации. С помощью этих шаблонов, можно управлять больше, чем просто внешнего вида сообщений электронной почты, но также управлять части для конечных пользователей. Например можно указать, использовать ли получателей почты, у которых этот шаблон и использующие Google Yahoo и учетные записи Microsoft эти учетные записи выполнить вход на портал шифрования сообщений Office 365. Можно использовать шаблоны для удовлетворения соответствующих несколько вариантов использования, таких как:

- Шаблоны для каждого подразделения, такие как процент, продаж, и т.д.
- Шаблоны для различных продуктов.
- Шаблоны для разных регионах или странах

После того как вы создали шаблоны, можно применять их на зашифрованные сообщения электронной почты с помощью правил потока обработки почты Exchange. Можно отозвать все сообщения, которые являются с фирменной символикой с помощью этих шаблонов.
  
||
|:-----|
|В этой статье является частью серии статей о шифровании сообщений Office 365, размер которых. Эта статья предназначена для администраторов и специалистов по ИТ. Если вы только что подробную информацию об отправке или получении зашифрованного сообщения, просматривать список статей в [Шифрования сообщений Office 365 (OME)](ome.md) и найдите статьи, который лучше все соответствует вашим требованиям. |
||

## <a name="create-branding-templates"></a>Создание фирменной настройки шаблонов

Создание фирменной настройки шаблонов для вашей организации в Windows PowerShell с помощью командлета New-OMEConfiguration. После создания шаблона, можно определить части шаблона с помощью командлета Set-OMEConfiguration. Можно создать несколько шаблонов.

![Части настраиваемой электронной почты](media/ome-template-breakout.png)
  
1. Использование рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, начало сеанса Windows PowerShell и подключитесь к Exchange Online. Сведения содержатся в разделе [подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Командлет New-OMEConfiguration используется для создания нового шаблона.
     ```powershell
     New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
     ```
     Например:
     ```powershell
     New-OMEConfiguration -Identity <Branding template 1>
     ```
3. Определение пользовательских настроек для шаблона, определенные с помощью командлета Set-OMEConfiguration, как описано в [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) или используйте следующую таблицу для удобства.

|**Настройка этой функции шифрования**|**Используйте эти команды**|
|:-----|:-----|
|Цвет фона  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"` <br/> |
|Логотип  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Поддерживаемые форматы файлов: PNG, JPG, BMP, TIFF  <br/> Оптимальный размер файла логотипа: менее 40 КБ  <br/> Оптимальный размер изображения логотипа: 170 x 70 пикселей  <br/> |
|Текст рядом с полем отправителя имя и адрес электронной почты| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Текст, отображаемый на кнопке «Чтение сообщений»| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Текст, который появляется над под кнопкой «Чтение сообщений»| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Заявление об отказе в зашифрованном сообщении электронной почты.  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Текст, отображающийся в верхней части портала просмотра зашифрованных сообщений.<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Для включения или отключения проверки подлинности с помощью единовременного пароля для этого настраиваемого шаблона| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Примеры:** <br/>Чтобы включить одноразовый секретный код для этого настраиваемого шаблона <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> Чтобы отключить одноразовый секретный код для этого настраиваемого шаблона <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|Для включения или отключения проверки подлинности с помощью Microsoft, Google или Yahoo удостоверения для этого настраиваемого шаблона| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Примеры:** <br/>Для включения социальных идентификаторов для этого настраиваемого шаблона <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> Чтобы отключить социальных идентификаторов для этого настраиваемого шаблона <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>Для удаления настроек марки из OME сообщения портала и адрес электронной почты, шифруется с OME
  
1. [Подключение к Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Командлет Set-OMEConfiguration, как описано в [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration). Для удаления организации фирменной настройки из DisclaimerText, EmailText, и PortalText значения значение равно пустой строке, `""`. Для всех "изображение" значения, такие как логотип, задайте значение `"$null"`.

**Параметры настройки шифрования**

**Сброс функции шифрования к тексту и изображению по умолчанию**|**Используйте эти команды**|
|:-----|:-----|
|Текст по умолчанию, сопровождающий зашифрованные сообщения электронной почты.  <br/> Текст по умолчанию, отображающийся над инструкциями по просмотру зашифрованных сообщений.| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Заявление об отказе в зашифрованном сообщении электронной почты.| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Текст, отображающийся в верхней части портала просмотра зашифрованных сообщений.| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Пример возврат к значениям по умолчанию:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Логотип| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Пример возврат к значениям по умолчанию:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Цвет фона| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Пример возврат к значениям по умолчанию:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Создание правила потока почты Exchange, которая применяется с фирменными на зашифрованные сообщения электронной почты

После создания шаблона фирменной настройки, можно создать правила потока обработки почты Exchange для этого фирменной символики на основе определенных условий. Правило будет фирменной символики в следующих сценариях:

- Если сообщение электронной почты вручную зашифрованного конечных пользователей для клиентов Outlook или OWA
- Если сообщение электронной почты автоматически зашифрованного поток обработки почты Exchange правила или политики предотвращения потери данных Office 365

Сведения о том, как создать правило поток почты Exchange, которая применяется шифрование просмотрите [Определение правил поток обработки почты для шифрования сообщений электронной почты в Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. В веб-браузере с помощью учетной записи рабочего или школы, которому предоставлены разрешения глобального администратора, [войти в Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Выберите плитку **администрирования** .

3. Откроется Центр администрирования Office 365. Здесь выберите последовательно элементы **Центры администрирования** \> **Exchange**.

4. В центре администрирования Exchange последовательно выберите пункты **поток обработки почты** \> **правила** и выберите **Создать** ![новый значок](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Создать новое правило**. Дополнительные сведения об использовании центра администрирования Exchange можно [Центр администрирования Exchange в Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. В поле **имя**введите имя правила, например фирменная настройка для отдела продаж.

6. В **Применить это правило, если** выберите условие, выберите условие, **отправитель находится в организации** , а также других условий, который будет из списка доступных условий. Например может потребоваться применение шаблона определенного фирменной настройки для:

     - Все зашифрованные сообщения электронной почты, отправленные от участников финансовый отдел
     - Зашифрованные сообщения электронной почты, отправляемых с определенных ключевым словом, такие как «Внешние» или «Партнер»
     - Зашифрованных сообщений, отправляемых в определенном домене

7. **Выполните следующие действия**, выберите **Изменить безопасность сообщения** > **Применить пользовательское фирменной символики в OME сообщения**. Затем из раскрывающегося списка выберите шаблон фирменной настройки от тех, которые вы создали.
8. (Необязательно) Если правило поток почты также применить шифрование пользовательские настройки, **выполните следующие действия**, выберите **Изменить безопасность сообщения** и затем выберите **применить шифрование сообщений Office 365 и защите прав**. Выберите в списке шаблон службы управления правами, выберите команду **Сохранить**и нажмите кнопку **ОК**.
  
     Список шаблонов содержит все шаблоны по умолчанию и параметры, а также все пользовательские шаблоны, которые вы создали для использования с Office 365. Если список пуст, убедитесь, что настройки шифрования сообщений Office 365 с новыми возможностями как описано в [Set up новые возможности шифрования сообщений Office 365](set-up-new-message-encryption-capabilities.md). Для получения сведений о шаблонах по умолчанию видеть [Настройка и управление шаблонами для защиты информации Azure](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Сведения о параметре **Не пересылать** [не пересылать варианта по электронной почте](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails)см. Сведения о параметре **шифровать только** [параметр шифрования только для сообщений электронной почты](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)см.

     Вы можете **Добавить действие** при указании другого действия.
