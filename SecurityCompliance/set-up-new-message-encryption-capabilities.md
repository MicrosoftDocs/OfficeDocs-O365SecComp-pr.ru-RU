---
title: Настройка новых возможностей шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Новые возможности шифрования сообщений Office 365, основанные на Azure Information Protection, помогают защитить переписку с людьми внутри вашей организации и вне ее. Они поддерживают другие организации Office 365, Outlook.com, Gmail и прочие почтовые службы.
ms.openlocfilehash: 835b1d6f40868684536dbea8f75dab0665950210
ms.sourcegitcommit: 33c8e9c16143650ca443d73e91631f9180a9268e
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/25/2019
ms.locfileid: "35854803"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Настройка новых возможностей шифрования сообщений Office 365

Новые возможности шифрования сообщений в Office 365 (OME) позволяют организациям обмениваться защищенными сообщениями с кем угодно с любого устройства. Пользователи могут обмениваться защищенными сообщениями с другими организациями Office 365, а также с сотрудниками других организаций, использующих Outlook.com, Gmail и прочие почтовые службы.

||
|:-----|
|Эта статья является частью серии, посвященной шифрованию сообщений в Office 365. Эта статья предназначена для системных администраторов и ИТ-специалистов. Если вам нужны сведения о том, как отправлять и получать зашифрованные сообщения, см. список статей, посвященных [шифрованию сообщений в Office 365 (OME)](ome.md), чтобы найти наиболее подходящую статью. |
||

Чтобы убедиться, что новые возможности OME доступны в вашей организации Office 365, выполните указанные ниже действия.

## <a name="verify-that-azure-rights-management-is-active"></a>Проверьте, активна ли служба Azure Rights Management

Новые возможности OME используют функции защиты в [службе управления правами Azure (Azure RMS)](https://docs.microsoft.com/ru-RU/azure/information-protection/what-is-information-protection) — технологию, используемую службой [Azure Information Protection](https://docs.microsoft.com/ru-RU/azure/information-protection/what-is-azure-rms) для защиты электронной почты и документов с помощью шифрования и управления доступом.

Единственное обязательное условие для использования новых возможностей OME — [служба управления правами Azure](https://docs.microsoft.com/ru-RU/azure/information-protection/what-is-azure-rms) должна быть активирована в клиенте вашей организации. Если это так, Office 365 автоматически активирует новые возможности OME, а от вас не потребуется никаких действий.

Кроме того, служба Azure RMS автоматически активируется для большинства соответствующих планов. В этом случае от вас тоже не потребуется никаких действий. Дополнительные сведения см. в статье [Активация службы управления правами Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service).

>[!IMPORTANT]
>Если вы используете службу управления правами Active Directory (AD RMS) в Exchange Online, перед использованием новых возможностей OME необходимо [перейти на службу Azure Information Protection](https://docs.microsoft.com/ru-RU/azure/information-protection/migrate-from-ad-rms-to-azure-rms). Служба OME не совместима с AD RMS.  

Дополнительные сведения см. в указанных ниже статьях.

- [Какие подписки необходимо использовать для новых возможностей OME?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) Эта статья поможет вам убедиться, что ваш план подписки включает службу Azure Information Protection (которая включает функции Azure RMS).
- Сведения о приобретении соответствующей подписки см. в статье [Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/).  

### <a name="manually-activating-azure-rights-management"></a>Активация службы управления правами Azure вручную

Если вы отключили службу Azure RMS или по какой-либо причине она не была активирована автоматически, вы можете активировать ее вручную, используя одно из указанных ниже средств.

- 
  **Центр администрирования Microsoft 365**. Инструкции см. в статье [Активация службы управления правами Azure в Центре администрирования](https://docs.microsoft.com/ru-RU/azure/information-protection/activate-office365).
- **Портал Azure**. Инструкции см. в статье [Активация службы управления правами Azure на портале Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure).

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Настройка управления ключом клиента для службы Azure Information Protection

Это действие не является обязательным. По умолчанию корпорации Майкрософт разрешено управлять корневым ключом для службы Azure Information Protection. Этот вариант рекомендуется для большинства клиентов Office 365. В таком случае от вас не требуется никаких действий.

Существует множество причин, по которым вам может потребоваться создать собственный корневой ключ (BYOK), а также управлять им, например для обеспечения соответствия требованиям. В таком случае перед настройкой новых возможностей OME рекомендуется выполнить необходимые действия. Дополнительные сведения см. в статье [Планирование и реализация ключа клиента Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key).

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Проверка новой конфигурации OME в Exchange Online PowerShell

Вы можете убедиться, что клиент Office 365 настроен для использования новых возможностей OME, с помощью [Exchange Online PowerShell](https://docs.microsoft.com/ru-RU/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. 
  [Подключитесь к Exchange Online PowerShell](https://docs.microsoft.com/ru-RU/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) с помощью учетной записи с разрешениями глобального администратора в клиенте Office 365.

2. Запустите командлет Get-IRMConfiguration.

     Для параметра AzureRMSLicensingEnabled должно быть задано значение $True, указывающее, что в клиенте настроены возможности OME. В противном случае используйте командлет Set-IRMConfiguration, чтобы задать для параметра AzureRMSLicensingEnabled значение $True и включить OME.

3. Запустите командлет Test-IRMConfiguration, используя приведенный ниже синтаксис.

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Пример**.

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - Указывать электронный адрес отправителя необязательно, но это позволит системе выполнить дополнительные проверки. Используйте электронный адрес любого пользователя в клиенте Office 365.

     Результаты должны выглядеть примерно так:

     ```text
    Results : Acquiring RMS Templates ...
                - PASS: RMS Templates acquired.  Templates available: Contoso  - Confidential View Only, Contoso  - Confidential, Do Not
            Forward.
            Verifying encryption ...
                - PASS: Encryption verified successfully.
            Verifying decryption ...
                - PASS: Decryption verified successfully.
            Verifying IRM is enabled ...
                - PASS: IRM verified successfully.

            OVERALL RESULT: PASS
    ```

   - Название вашей организации Office 365 заменит *Contoso*.

   - Заданные по умолчанию имена шаблонов могут отличаться от указанных выше. Дополнительные сведения см. в статье [Настройка шаблонов для Azure Information Protection и управление ими](https://docs.microsoft.com/ru-RU/azure/information-protection/configure-policy-templates).

4. Выполните командлет Remove-PSSession, чтобы отключиться от службы управления правами.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="next-steps-define-mail-flow-rules-to-use-new-ome-capabilities"></a>Дальнейшие действия: определение правил потока обработки почты для использования новых возможностей OME

Если правила потока обработки почты для шифрования почты в организации Office 365 уже настроены, то для использования новых возможностей OME их необходимо обновить. Для выполнения новых развертываний необходимо создать новые правила потока обработки почты.

>[!IMPORTANT]
>Если не обновить существующие правила потока обработки почты, пользователи будут и дальше получать зашифрованные сообщения с вложениями в формате HTML без новых возможностей OME.

Правила потока обработки почты определяют, при каких условиях нужно шифровать электронную почту, а также условия для отмены такого шифрования. Если задать действие для правила, все сообщения, которые удовлетворяют его условиям, будут шифроваться при отправке.
  
Дополнительные сведения о создании правил потока обработки почты для OME см. в статье [Определение правил потока обработки почты для шифрования сообщений в Office 365](define-mail-flow-rules-to-encrypt-email.md).

Чтобы обновить существующие правила и использовать новые возможности OME, выполните указанные ниже действия.

1. В Центре администрирования Microsoft 365 выберите пункты **Центры администрирования > Exchange**.
2. В Центре администрирования Exchange выберите **Поток обработки почты > Правила**.
3. Повторите представленную ниже процедуру для каждого правила в разделе **Выполнить следующие действия**.
    - Выберите **Изменить безопасность сообщения**.
    - Выберите **Применить шифрование сообщений Office 365 и защиту с помощью прав**.
    - Выберите шаблон RMS из списка.
    - Нажмите кнопку **Сохранить**.
    - Нажмите кнопку **ОК**.
