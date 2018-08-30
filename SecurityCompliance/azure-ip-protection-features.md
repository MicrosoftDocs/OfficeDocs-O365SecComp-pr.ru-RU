---
title: Функции защиты в Azure Information Protection развертывания для существующих клиентов Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 7ad6f58e-65d7-4c82-8e65-0b773666634d
description: При первом этапе для защиты ваших сведений, запуск всех подходящих клиентов защита информации Azure 2018 июля будет функции защиты в Azure Information Protection включен по умолчанию. Функции защиты в Azure Information Protection ранее известных в Office 365, как управление правами или службы управления правами Azure. Если в вашей организации есть плана службы Office E3 или выше план обслуживания вы получите начать защиты данных с помощью Azure защита информации, когда мы развертывания этих функций.
ms.openlocfilehash: be0200da3032dccbcf54e67f3bdfbac800b65526
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534577"
---
# <a name="protection-features-in-azure-information-protection-rolling-out-to-existing-office-365-tenants"></a>Функции защиты в Azure Information Protection развертывания для существующих клиентов Office 365

При первом этапе для защиты ваших сведений, запуск всех подходящих клиентов защита информации Azure 2018 июля будет функции защиты в Azure Information Protection включен по умолчанию. Функции защиты в Azure Information Protection ранее известных в Office 365, как управление правами или службы управления правами Azure. Если в вашей организации есть плана службы Office E3 или выше план обслуживания вы получите начать защиты данных с помощью Azure защита информации, когда мы развертывания этих функций.
  
## <a name="changes-beginning-july-1-2018"></a>Приступая к работе с 1 июля 2018 изменений

Запуск 1 июля 2018, Microsoft будет включить функцию защиты в Azure защита информации для всех клиентов Office 365, имеющих одно из следующих планов подписки:
  
- Шифрование сообщений Office 365 — это входят в состав Office 365 E3 и E5, Microsoft E3 и E5, Office 365 A1, A3 и A5 и Office 365 G3 и G5. Не требуется дополнительных лицензий на получение новых возможностей защиты с Azure защита информации. 
    
- Также можно добавить планы Azure сведения о защите план 1 приведенным ниже, для получения новых возможностей шифрования сообщений Office 365: Exchange Online план 1, Exchange Online (план 2), Microsoft Office 365 F1, основы бизнеса Office 365, Office 365 бизнеса расширенный или Office 365 корпоративный E1.
    
- Каждый пользователь выгодное шифрования сообщений Office 365 должен иметь лицензию поиска с помощью функции.
    
- Полный список представлен [Exchange Online описания служб](https://technet.microsoft.com/library/exchange-online-service-description.aspx) для шифрования сообщений Office 365. 
    
Администраторы клиента можно проверить состояние защиты на портале администратора Office 365. 
  
![Снимок экрана, которое показывает, что активации управления правами в Office 365.](media/303453c8-e4a5-4875-b49f-e80c3eb7b91e.png)
  
## <a name="why-are-we-making-this-change"></a>Почему мы делаете это изменение?

Шифрование сообщений Office 365 использует возможностей защиты в Azure защита информации. В основе последние улучшения для шифрования сообщений Office 365 и более масштабные инвестиций для защиты информации в Microsoft 365 мы упрощая для организаций, включить и использовать возможности наших защиты, в качестве Исторически шифрования технологии были сложно настроить. Включение функции защиты в Azure защита информации по умолчанию, вы можете быстро начать для защиты конфиденциальных данных.
  
## <a name="does-this-impact-me"></a>Это отразится на моей?

Если вашей организации Office 365 приобрели лицензии Office 365 подходящими, клиент будет влиять это изменение.
  
 **Важно!** Если вы используете службы управления правами Active Directory (AD RMS) в локальной среде, необходимо отказаться от этого изменения сразу же или перенос в Azure Information Protection перед мы развернуть это изменение в течение 30 дней. Сведения о том, как для отключения см «использовать службы управления правами, как включить out?» далее в этой статье. Если вы предпочитаете для переноса, см [Миграция с AD RMS для защиты информации Azure.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="can-i-use-azure-information-protection-with-active-directory-rights-management-services-ad-rms"></a>Можно ли использовать Azure сведения о защите с помощью службы управления правами Active Directory (AD RMS)?

Нет. Это не сценария развертывания. Без учета дополнительные действия отказаться, некоторые компьютеры могут автоматически запускать с помощью службы управления правами Azure и также подключитесь к кластер AD RMS. В этом сценарии не поддерживается и имеет ненадежные результаты, поэтому важно отключить это изменение в течение 30 дней до мы развертывание этих новых функций. Сведения о том, как для отключения см «использовать службы управления правами, как включить out?» далее в этой статье. Если вы предпочитаете для переноса, см [Миграция с AD RMS для защиты информации Azure.](https://docs.microsoft.com/azure/information-protection/plan-design/migrate-from-ad-rms-to-azure-rms)
  
## <a name="how-do-i-know-if-im-using-ad-rms"></a>Как узнать, если я использую AD RMS?

Используйте следующие инструкции из [подготовки среды для управления правами Azure при наличии службы управления правами Active Directory (AD RMS)](https://docs.microsoft.com/azure/information-protection/deploy-use/prepare-environment-adrms) для проверки, если вы развернули AD RMS: 
  
1. Хотя это необязательно, в большинстве случаев AD RMS публикация точку подключения службы (SCP) в Active Directory, чтобы компьютеры домена могут обнаруживать кластер AD RMS. 
  
Используйте редактор ADSI, чтобы изучить ли у вас есть SCP, опубликованные в Active Directory: CN = Configuration [имя сервера], CN = Services, CN = RightsManagementServices, CN = SCP
    
2. Если вы не используете точки подключения службы, компьютеры Windows, которые подключаются к кластеру AD RMS должны быть настроены для обнаружения службы со стороны клиента или лицензирования в режиме одобрения администратором с помощью реестра Windows: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MSIPC\ServiceLocation или HKEY_ LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\MSIPC\ServiceLocation 
  
Дополнительные сведения об этих конфигураций реестра можно [Включение обнаружения служб со стороны клиента с помощью реестра Windows](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#enabling-client-side-service-discovery-by-using-the-windows-registry) и [Redirecting лицензирования сервера трафика](https://docs.microsoft.com/azure/information-protection/rms-client/client-deployment-notes#redirecting-licensing-server-traffic).
    
## <a name="i-use-ad-rms-how-do-i-opt-out"></a>Использовать службы управления правами, как отказаться в работе?

Отказ от Предстоящие изменения, выполните следующие действия:
  
1. Использование рабочего или школы учетной записи, имеющей права глобального администратора в организации Office 365, начало сеанса Windows PowerShell и подключитесь к Exchange Online. Сведения содержатся в разделе [подключение к Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps).
    
2. Командлет Set-IRMConfiguration, используя следующий синтаксис:
    
  ```
  Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false 
  ```

## <a name="what-can-i-expect-after-this-change-has-been-made"></a>Что можно ожидать после было сделано это изменение?

Если этот параметр включен, если вы еще не подписано выходной параметр, можно начать с помощью новой версии шифрования сообщений Office 365, которая появилась в [Microsoft Ignite 2017](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Email-Encryption-and-Rights-Protection/ba-p/110801) , а также возможности шифрования и защиты данных Azure Защита. 
  
![Снимок экрана, показывающий OME для защиты сообщений в Outlook в Интернете.](media/599ca9e7-c05a-429e-ae8d-359f1291a3d8.png)
  
Дополнительные сведения о новых улучшений можно [Шифрования сообщений Office 365](ome.md).
  

