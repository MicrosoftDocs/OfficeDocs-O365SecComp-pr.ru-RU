---
title: Настройка параметров S/MIME в Exchange Online для Outlook в Интернете
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c7dee22c-9b5b-425c-91a9-d093204ff84e
ms.collection:
- M365-security-compliance
description: Краткое описание администраторов Exchange Online, необходимых для просмотра и настройки параметров S/MIME в Outlook в Интернете в Exchange Online.
ms.openlocfilehash: d890b7f39d16d8c0f3866d5ff0024fe31160af6b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258997"
---
# <a name="configure-smime-settings-in-exchange-online-for-outlook-on-the-web"></a>Настройка параметров S/MIME в Exchange Online для Outlook в Интернете

В качестве администратора Exchange Online можно настроить Outlook в Интернете (прежнее название — Outlook Web App), чтобы разрешить отправку и получение сообщений, защищенных С помощью S/MIME. Используйте командлеты **Get-SmimeConfig** и **Set-SmimeConfig** для просмотра и управления этой функцией в Exchange Online PowerShell. Сведения о подключении к Exchange Online PowerShell см. в статье [Подключение к Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).

Подробные сведения о синтаксисе и параметрах можно найти в статье [Get – SmimeConfig](http://technet.microsoft.com/library/4b29fa89-0840-4fe9-8885-019fcef2e02b.aspx) и [Set/SmimeConfig](http://technet.microsoft.com/library/de357ce0-8143-4c36-8032-026292fc63f0.aspx).

## <a name="considerations-for-chrome"></a>Рекомендации для Chrome

Чтобы использовать S/MIME в Outlook в Интернете в веб-браузере Google Chrome, вы (или другой администратор) должны настроить и настроить политику Чромиум с именем **екстенсионинсталлфорцелист** , чтобы установить расширение Microsoft S/MIME в Chrome. В политике должна использоваться синтаксическая конструкция: `<extension-id>;https://outlook.office.com/owa/SmimeCrxUpdate.ashx` , например: `maafgiompdekodanheihhgilkjchcakm;https://outlook.office.com/owa/SmimeCrxUpdate.ashx`. Обратите внимание, что для применения этой политики требуются компьютеры, присоединенные к домену, поэтому для эффективного использования S/MIME в Chrome необходимы компьютеры, присоединенные к домену.

Этот шаг является необходимым условием для использования Chrome; Он не заменяет элемент управления S/MIME, установленный пользователями. Подробные сведения о политике **екстенсионинсталлфорцелист** можно найти в статье [екстенсионинсталлфорцелист](http://dev.chromium.org/administrators/policy-list-3#ExtensionInstallForcelist).

## <a name="for-more-information"></a>Дополнительные сведения

[S/MIME для подписи и шифрования сообщений](s-mime-for-message-signing-and-encryption.md)
