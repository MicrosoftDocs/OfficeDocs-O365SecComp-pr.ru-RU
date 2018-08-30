---
title: Добавление фирменного стиля организации в зашифрованные сообщения
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: 'Как администратор Exchange можно применять вашей организации фирменной символики в вашей организации зашифрованные сообщения электронной почты и содержимое портала шифрования. '
ms.openlocfilehash: 2f34b5cea3155f587fd7787f1f69270d1373400b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534865"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Добавление фирменной символики организации в зашифрованные сообщения

Как администратор Exchange Online или Exchange Online Protection можно применить вашей компании, фирменная символика настраивать внешний вид сообщений электронной почты вашей организации шифрования сообщений Office 365 и содержимое портала шифрования. Командлеты Get-OMEConfiguration и Set-OMEConfiguration Windows PowerShell можно настроить следующие аспекты возможности просмотра для получателей зашифрованные сообщения электронной почты:
  
- Вводный текст зашифрованного сообщения электронной почты
    
- Текст заявления об отказе зашифрованного сообщения электронной почты
    
- Текст, который отображается на портале OME
    
- Логотип, который отображается в сообщении электронной почты и портала OME
    
- Цвет фона в сообщение электронной почты и портала OME
    
Кроме того, в любое время вы можете восстановить интерфейс по умолчанию.
  
||
|:-----|
|В этой статье является частью серии статей о шифровании сообщений Office 365, размер которых. Эта статья предназначена для администраторов и специалистов по ИТ. Если вы только что подробную информацию об отправке или получении зашифрованного сообщения, просматривать список статей в [Шифрования сообщений Office 365 (OME)](ome.md) и найдите статьи, который лучше все соответствует вашим требованиям. |
||
   
**Настройка внешнего вида OME сообщений портала и адрес электронной почты, шифруется с OME с марки вашей организации**
  
1. Подключение к Exchange Online с помощью удаленной оболочки PowerShell, как описано в разделе [подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Командлет Set-OMEConfiguration, как описано в [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) или используйте следующую таблицу для удобства. 
    
**Параметры настройки шифрования**

|**Настройка этой функции шифрования**|**Используйте эти команды**|
|:-----|:-----|
|Текст по умолчанию, сопровождающий зашифрованные сообщения электронной почты. Текст по умолчанию, отображающийся над инструкциями по просмотру зашифрованных сообщений  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Заявление об отказе в зашифрованном сообщении электронной почты.  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only."` <br/> |
|Текст, отображающийся в верхней части портала просмотра зашифрованных сообщений.<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Логотип  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Поддерживаемые форматы файлов: PNG, JPG, BMP, TIFF  <br/> Оптимальный размер файла логотипа: менее 40 КБ  <br/> Оптимальный размер изображения логотипа: 170 x 70 пикселей  <br/> |
|Цвет фона  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -BackgroundColor "#ffffff"` <br/> |
   
**Для удаления настроек марки из OME сообщения портала и адрес электронной почты, шифруется с OME**
  
1. Подключение к Exchange Online с помощью удаленной оболочки PowerShell, как описано в разделе [подключение к Exchange Online с помощью удаленной оболочки PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Командлет Set-OMEConfiguration, как описано в [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Для удаления организации фирменной настройки из DisclaimerText, EmailText, и PortalText значения значение равно пустой строке, `""`. Для всех "изображение" значения, такие как логотип, задайте значение `"$null"`.
    
**Параметры настройки шифрования**

**Сброс функции шифрования к тексту и изображению по умолчанию**|**Используйте эти команды**|
|:-----|:-----|
|Текст по умолчанию, сопровождающий зашифрованные сообщения электронной почты.  <br/> Текст по умолчанию, отображающийся над инструкциями по просмотру зашифрованных сообщений.  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Заявление об отказе в зашифрованном сообщении электронной почты.  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Пример:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Текст, отображающийся в верхней части портала просмотра зашифрованных сообщений.  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Пример возврат к значениям по умолчанию:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Логотип  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Пример возврат к значениям по умолчанию:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
|Цвет фона  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Пример возврат к значениям по умолчанию:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null` <br/> |
   

