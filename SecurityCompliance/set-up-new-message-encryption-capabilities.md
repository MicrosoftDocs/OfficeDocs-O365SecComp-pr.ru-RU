---
title: Настройка новых возможностей шифрования сообщений Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ff0c040-b25c-4378-9904-b1b50210d00e
description: Новые возможности шифрования сообщений Office 365, основанные на Azure Information Protection, ваша организация может использовать защищенную электронную связь с пользователями внутри и за пределами Организации. Новые возможности OME работают с другими организациями Office 365, Outlook.com, Gmail и другими почтовыми службами.
ms.openlocfilehash: fd237e537aa1ff961d2d975b3b30f4a51744ba7c
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479655"
---
# <a name="set-up-new-office-365-message-encryption-capabilities"></a>Настройка новых возможностей шифрования сообщений Office 365

Новые возможности шифрования сообщений Office 365 (OME) позволяют организациям обмениваться защищенной электронной почтой с любыми устройствами. Пользователи могут обмениваться защищенными сообщениями с другими организациями Office 365, а также клиентами, не являющимися клиентами Office 365, с помощью Outlook.com, Gmail и других почтовых служб.


>[!NOTE]
>Эта статья предназначена для администраторов и ИТ-специалистов. Если вы являетесь конечным пользователем, просмотрите список статей в статье [Шифрование сообщений Office 365 (OME)](ome.md) для соответствующих решений.

Выполните приведенные ниже действия, чтобы убедиться, что новые возможности OME доступны в клиенте Office 365.

## <a name="verify-azure-rights-management-arm-is-active"></a>Проверка активности Azure Rights Management (ARM)

>[!NOTE]
>Новые возможности OME используют функции защиты в [Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/what-is-information-protection), технологии, используемой службой [Azure Rights Management (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms).

Единственным необходимым условием для использования новых возможностей OME является то, что служба [управления правами Azure (ARM)](https://docs.microsoft.com/en-us/azure/information-protection/what-is-azure-rms) должна быть активирована в клиенте Office 365. Если это так, Office 365 автоматически активирует новые возможности OME, и вам не нужно ничего делать.

ARM также активизируется автоматически для большинства соответствующих планов, поэтому вам, скорее всего, не придется ничего делать. Дополнительную поддержку вы найдете в статье [Активация управления правами Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-service) .

>[!IMPORTANT]
>Если вы используете службу управления правами Active Directory (AD RMS) с Exchange Online, вам необходимо [выполнить миграцию в Azure Information Protection](https://docs.microsoft.com/en-us/azure/information-protection/migrate-from-ad-rms-to-azure-rms) , прежде чем вы сможете использовать новые возможности OME. Служба AD RMS несовместима с ARM.  

Дополнительные сведения см.

- [Какие подписки необходимы для использования новых возможностей OME?](ome-faq.md#what-subscriptions-do-i-need-to-use-the-new-ome-capabilities) чтобы проверить, включается ли план подписки в Azure Information Protection (включая ARM).
- [Azure Information Protection](https://azure.microsoft.com/en-us/services/information-protection/) для получения сведений о приобретении подлежащей подписке.  

### <a name="manually-activating-arm"></a>Ручная активация ARM

Если вы отключили ARM или не активировали его автоматически по какой бы то ни было причине, вы можете активировать его вручную в:

- **Центр администрирования office 365**: в этой статье приведены инструкции по [активации Azure Rights Management из центра администрирования Office 365](https://docs.microsoft.com/en-us/azure/information-protection/activate-office365) .
- **Портал Azure**: Узнайте [, как активировать управление правами Azure на портале Azure](https://docs.microsoft.com/en-gb/azure/information-protection/activate-azure) для получения инструкций.

## <a name="configure-management-of-your-azure-information-protection-tenant-key"></a>Настройка управления ключом клиента Azure Information Protection

Этот шаг является необязательным. Предоставление корпорации Майкрософт возможности управлять корневым ключом для Azure Information Protection является параметром по умолчанию и рекомендуемой практикой для большинства клиентов Office 365. В этом случае вам не нужно ничего делать.

Существует множество причин, например требований соответствия требованиям, которые могут быть готовы к созданию и управлению собственным корневым ключом (также известным как перенесите свой ключ (БЙОК)). В этом случае рекомендуется выполнить необходимые действия перед настройкой новых возможностей OME. Чтобы узнать больше [, ознакомьтесь с разделом Планирование и реализация клиентского ключа клиента для Azure Information Protection](https://docs.microsoft.com/information-protection/plan-design/plan-implement-tenant-key) .

## <a name="verify-new-ome-configuration-in-exchange-online-powershell"></a>Проверка новой конфигурации OME в Exchange Online PowerShell

Вы можете убедиться, что клиент Office 365 правильно настроен для использования новых возможностей OME в [Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps).
  
1. [Подключитесь к Exchange Online PowerShell](https://docs.microsoft.com/en-us/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell) , используя учетную запись с разрешениями глобального администратора в клиенте Office 365.

2. Запустите командлет Test-IRMConfiguration, используя следующий синтаксис:

     ```powershell
     Test-IRMConfiguration [-Sender <email address >]
     ```  

   **Пример**:

     ```powershell
     Test-IRMConfiguration -Sender securityadmin@contoso.com
     ```

     - Предоставление электронной почты отправителя необязательно, но заставляет систему выполнять дополнительные проверки. Используйте адрес электронной почты любого пользователя в клиенте Office 365. 

     Результаты должны выглядеть следующим образом:

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

   - Имя вашей организации Office 365 заменит *contoso*.

   - Имена шаблонов по умолчанию могут отличаться от показанных выше. Дополнительную информацию можно узнать в статье [Настройка шаблонов для Azure Information Protection и управление ими](https://docs.microsoft.com/en-us/azure/information-protection/configure-policy-templates) .

3. Запустите командлет reMove – PSSession, чтобы отключиться от службы управления правами.

     ```powershell
     Remove-PSSession $session
     ```

## <a name="update-mail-flow-rules-to-use-new-ome-capabilities"></a>Обновление правил для почтового процесса для использования новых возможностей OME

Если вы уже настроили правила обработки почты [для шифрования электронной почты](define-mail-flow-rules-to-encrypt-email.md) в клиенте Office 365, необходимо обновить существующие правила, чтобы использовать новые возможности OME. Для новых развертываний это действие не требуется на этом этапе.   

>[!Note]
>Правила для поЧтовых ящиков определяют условия, при которых сообщения электронной почты шифруются, а также, когда необходимо удалить шифрование. Дополнительные сведения: [Определение правил для почтового процесса для шифрования сообщений электронной почты в Office 365](define-mail-flow-rules-to-encrypt-email.md) .

Чтобы обновить существующие правила для использования новых возможностей OME:

1. В центре администрирования Office 365 откройте центр **администрирования _Гт_ Exchange**.

2. В центре администрирования Exchange перейдите к разделу **_Гт_ Mail Flow Rules**. 
3. Для каждого правила **выполните следующие**действия:
    - Выберите **изменить безопасность сообщения**.
    - Выберите **применить шифрование сообщений Office 365 и защиту прав**.
    - Выберите шаблон RMS в списке.
    - Нажмите кнопку **сохранить**.
    - Нажмите кнопку **ОК**.
  
>[!IMPORTANT]
>Если вы не обновите существующие правила для почтовых ящиков, ваши пользователи продолжат получать зашифрованную почту, использующую предыдущий формат вложений HTML, а не новые возможности OME.
