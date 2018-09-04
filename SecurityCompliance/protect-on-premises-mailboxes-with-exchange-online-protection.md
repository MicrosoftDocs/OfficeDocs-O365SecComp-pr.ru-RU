---
title: Защита локальных почтовых ящиков с Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/1/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- GEU150
- GMA150
- GPA150
- MET150
ms.assetid: c5e95951-da67-4ec7-92c5-982abd477e69
description: Даже в том случае, если вы планируете размещать некоторые или все почтовые ящики на локальную, по-прежнему можно защищать почтовые ящики с Exchange Online Protection (EOP). Для настройки соединителей вашей учетная запись должна быть глобального администратора Office 365 или администратора компании Exchange (группа ролей управления организацией). Сведения о связи разрешения Office 365 с разрешения Exchange содержатся в разделе назначение роли администратора в Office 365, которой с 21Vianet. Если все ваши почтовые ящики Exchange на месте, выполните следующие действия для настройки службы EOP.
ms.openlocfilehash: 4751bb2183e61d292805d1799519644b77b08c2a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535498"
---
# <a name="protect-on-premises-mailboxes-with-exchange-online-protection"></a>Защита локальных почтовых ящиков с Exchange Online Protection

> [!NOTE]
> Эта статья относится только к Office 365, которой с 21Vianet в Китае. 
  
Даже в том случае, если вы планируете размещать некоторые или все почтовые ящики на локальную, по-прежнему можно защищать почтовые ящики с Exchange Online Protection (EOP). Для настройки соединителей вашей учетная запись должна быть глобального администратора Office 365 или администратора компании Exchange (группа ролей управления организацией). Сведения о связи разрешения Office 365 с разрешения Exchange содержатся в разделе [Назначение роли администратора в Office 365, которой с 21Vianet](https://support.office.com/article/d58b8089-cbfd-41ec-b64c-9cfcbef495ac). Если все ваши почтовые ящики Exchange на месте, выполните следующие действия для настройки службы EOP. 
  
## <a name="step-1-use-the-office-365-admin-center-to-add-and-verify-your-domain"></a>Действие 1. Добавление и проверка домена с помощью Центр администрирования Office 365

1. Чтобы добавить свой домен в службу, в Центр администрирования Office 365 перейдите в раздел Настройка.
    
2.  Выполните действия, описанные в портале, чтобы добавить применимые записи DNS у поставщика услуг размещения DNS для подтверждения прав владельца домена. 
    
> [!TIP]
> [Добавление домена и пользователям Office 365, которой с 21Vianet](https://support.office.com/article/1cd4839b-d051-46b8-ab9b-bc7752024e78) и [Создание записей DNS для Office 365 при самостоятельном управлении записями DNS-записи](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b) являются полезные справочные материалы по Добавление домена в службу и настройке DNS. 
  
### <a name="step-2-add-recipients-and-configure-the-domain-type"></a>Шаг 2: Добавление получателей и настройка типа домена

Перед настройкой передачи почты через службу EOP мы рекомендуем добавить в службу получателей. Это можно сделать несколькими способами, как описано в разделе [Управление почтовыми пользователями в EOP](https://go.microsoft.com/fwlink/?LinkId=506782). Кроме того, если вы хотите включить функцию пограничной блокировки на основе каталогов (DBEB) для принудительной проверки получателей в службе после их добавления, необходимо задать тип домена как "Уполномоченный". Дополнительные сведения о пограничной блокировке на основе каталогов см. в разделе [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](https://go.microsoft.com/fwlink/?LinkId=506781).
  
## <a name="step-3-use-the-eac-to-set-up-mail-flow"></a>Действие 3. Использование Центра администрирования Exchange для настройки потока обработки почты

Создание соединителей в центре администрирования Exchange (EAC), чтобы разрешить поток почты между EOP и ваш почтовый сервер локальной. Подробные инструкции в разделе [Создание необходимых соединителей для настройки потока базовой электронной почты через службу EOP](https://go.microsoft.com/fwlink/?LinkId=506780).
  
 Как проверить выполнение задачи? 
  
 Использование анализатора удаленного подключения для выполнения теста для проверки потока почты между службой и среды. Для получения дополнительных сведений обратитесь к разделу «Использование анализатора удаленного подключения для проверки доставки почты» в [Проверка потока почты с помощью анализатора удаленного подключения](https://go.microsoft.com/fwlink/?LinkId=506784).
  
## <a name="step-4-allow-inbound-port-25-smtp-access"></a>Действие 4. Разрешение доступа к входящему порту 25 для трафика SMTP

После настройки соединителей ожидания 72 часов, чтобы разрешить распространения обновлений запись DNS. После этого следует ограничьте входящий трафик SMTP порт 25 на брандмауэре или почтовых серверов для приема почты только от центров обработки данных EOP, в частности с IP-адресов, перечисленных в [URL-адреса и IP-адреса диапазонов для Office 365, которой с 21Vianet](https://support.office.com/article/5c47c07d-f9b6-4b78-a329-bfdc1b6da7a0#__exchange_online_protection). Это обеспечивает защиту в локальную среду путем ограничения области входящих сообщений, которые можно получить. Кроме того Если у вас есть параметры на ваш почтовый сервер, которые управляют IP-адресами, разрешенных для подключения для ретрансляции почты, обновите эти параметры.
  
> [!TIP]
> Настройте на сервере SMTP время подключения, равное 60 секундам. Это значение подходит для большинства ситуаций, обеспечивая определенную задержку, например если отправлено сообщение с крупным вложением. 
  
## <a name="step-5-use-the-shell-to-ensure-that-spam-is-routed-to-each-users-junk-email-folder"></a>Действие 5. С помощью командной консоли убедитесь, что нежелательная почта маршрутизируется в папку нежелательной почты каждого пользователя.

Чтобы обеспечить правильную маршрутизацию (нежелательной) нежелательных сообщений электронной почты в папку нежелательной почты каждого пользователя, необходимо выполнить несколько действий по настройке. Действия приведенные в [Убедитесь, что нежелательной почты перенаправляется в папку нежелательной почты каждого пользователя](https://go.microsoft.com/fwlink/?LinkId=506804). Если не хотите переместить сообщения в папку нежелательной почты каждого пользователя, можно выбрать другое действие посредством изменения политик фильтрации содержимого в центре администрирования Exchange. Дополнительные сведения можно [Настроить политики фильтрации содержимого](https://go.microsoft.com/fwlink/?LinkId=506805). 
  
## <a name="step-6-use-the-office-365-admin-center-to-point-your-mx-record-to-eop"></a>Действие 6. Настройка записи MX, указывающей на Exchange Online Protection, с помощью Центр администрирования Office 365

Выполните действия конфигурации домена Office 365, чтобы обновить запись MX для вашего домена, чтобы потоки входящей электронной почты через службу EOP. Для получения дополнительных сведений можно снова ссылаться на [Создание записей DNS для Office 365 при самостоятельном управлении записями DNS-записей](https://support.office.com/article/0669bf14-414d-4f51-8231-6b710ce7980b).
  
Как проверить выполнение задачи?
  
 Использование анализатора удаленного подключения требуется выполнить проверку, выполняется проверка записи MX. Дополнительные сведения см в разделе «Использование анализатора удаленного подключения для проверки записи MX и исходящего соединителя» [Проверка потока почты с помощью анализатора удаленного подключения](https://go.microsoft.com/fwlink/?LinkId=506784). 
  
На этот момент выполнена проверка правильности настройки локального исходящего соединителя предоставляемой службы, а также проверка того, что запись MX указывает на EOP. Теперь можно выполнить следующие дополнительные тесты, чтобы убедиться, что служба успешно доставляет электронную почту в локальную среду.
  
- В анализаторе удаленных подключений перейдите на вкладку **Office 365** и запустите тест **Входящая электронная почта SMTP**, расположенный в разделе **Тесты передачи электронной почты через Интернет**.
    
- Отправьте сообщение с любой учетной записи электронной почты в Интернете получателю в вашей организации, чей домен соответствует добавленному в службу. Подтвердите доставку сообщения в локальный почтовый ящик с помощью Microsoft Outlook или другого почтового клиента.
    
- Если нужно запустить тест для исходящей почты, вы можете отправить электронное сообщение от пользователя в вашей организации на учетную запись электронной почты в Интернете и подтвердить получение сообщения.
    
## <a name="less-common-a-hybrid-setup-with-mailboxes-on-premises-and-in-the-cloud"></a>Меньшее распространение: Настройка гибридных с локальные почтовые ящики и в облаке

Если у вас есть Exchange локальные почтовые ящики и один или несколько почтовых ящиков в облаке в Exchange Online, у вас есть *гибридного* установки. При настройке гибридных таких функций, как обмен сведениями о доступности календаря и маршрутизация почты совместной работы в своей локальной и облачных средах. Во время переноса почтовых ящиков в Exchange Online может быть гибридного установки на месте. Иначе, чем защиты изолированная EOP настройки гибридной среде. 
  
Можно выбрать гибридный сценарий, чтобы воспользоваться преимуществами электронной почты на основе облака для большинства своих сотрудников. Это можно сделать размещенной некоторые локальные почтовые ящики; Например для вашего юридического отдела. 
  
Гибридные установки может оказаться сложной задачей, но она имеет множество преимуществ. Для получения дополнительных сведений о настройке гибридных сценариев с сервером Exchange, видеть [функции гибридного развертывания Exchange Настройка с помощью Office 365 обслуживается 21Vianet](https://support.office.com/article/26e7cc26-c980-4cc5-a082-c333de544b6d).
  
