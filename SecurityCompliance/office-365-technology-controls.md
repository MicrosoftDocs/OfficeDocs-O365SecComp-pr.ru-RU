---
title: Технологические элементы управления в Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Сводка: Обзор технологии управления корпорации Майкрософт и рекомендации по Office 365.'
ms.openlocfilehash: 2ef04b558f5fa82075d9aa602b83d437aa4b2ee6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534736"
---
# <a name="office-365-technology-controls"></a>Технологические элементы управления в Office 365 

Корпорация Майкрософт использует несколько средств для управления, управление и аудит доступа к данным клиента в Exchange Online и технологий SharePoint Online, включая защищенного хранилища и защищенного хранилища клиента, многофакторная проверка подлинности и многое другое. Yammer Enterprise используется как элементы управления, как описано в [Yammer Enterprise средства управления доступом](office-365-yammer-enterprise-access-controls.md).

Инженеры Office 365 иметь ноль положение доступ к данным клиента Office 365 и они должны проходить процесс утверждения, который включает в себя Microsoft и — если клиента лицензируемые функции клиента защищенного хранилища для Exchange Online и SharePoint Online — клиент утверждения, для доступа к данным клиента для операций службы. При предоставлении утверждения конкретной службы административные учетные записи, подготовленных только что времени с достаточно права на выполнение задачи, необходимые для запроса службы.

## <a name="lockbox-and-customer-lockbox"></a>Защищенного хранилища и защищенного хранилища клиента
Очень редко, но клиент может запросить помощь от корпорации Майкрософт, который может предоставлять Microsoft инженер по содержимому клиента для облегчения их о проблеме. Для управления доступом к Exchange Online (Это включает все Скайп для бизнес-данных, хранимых в почтовых ящиках пользователей (Скайп для бизнеса покрытия не включает вещания собрания Скайп записи или контент, отправляемых пользователями на собрания)) и SharePoint Online (который включает в себя OneDrive для бизнеса), корпорация Майкрософт использует систему управления доступа, называется защищенного хранилища. Любой Инженер службы поддержки Майкрософт могут получить доступ к любой системы Exchange Online и SharePoint Online или данных, их необходимо отправить запрос доступа с помощью защищенного хранилища. С помощью защищенного хранилища является обязательным для всех с повышенными правами доступа к Exchange Online или SharePoint Online.

Защищенного хранилища обрабатывает запросы на разрешения, предоставленные инженеров возможность выполнять операционные и административные функции в службе. Инженеры отправить запросы через защищенного хранилища, который должны быть утверждены диспетчера перед Инженер службы поддержки, имеющего возможность доступа к данным клиента. После утверждения диспетчера инженер имеет временными и область ограниченный доступ к данным клиента для работы на проблему клиента.

Защищенного хранилища клиента Office 365, которые помогут провести обязательств соответствия требованиям, которые используются в FedRAMP и HIPAA, если вам требуется процедур на месте для авторизации доступа явных данных. В редких случаях, когда инженер службы Microsoft необходим доступ к данным, предоставить доступа только для данных, необходимых для устранения этой проблемы и для ограниченного периода времени. Действия, выполненные с инженером службы поддержки для целей аудита записываются и будут доступны с помощью [API действия для управления Office 365](https://msdn.microsoft.com/library/office/dn707383.aspx) и [центре соответствия требованиям и безопасности](http://protection.office.com/). Защищенного хранилища клиента вставляет клиента в процесс утверждения защищенного хранилища и обеспечивает возможность управления авторизации доступа Microsoft Exchange Online или контенту SharePoint Online для операции службы.

>**Примечание**: защищенного хранилища клиента доступен в [Office 365 корпоративный E5](https://products.office.com/business/office-365-enterprise-e5-business-software) и как приобрести дополнительный компонент, но должны выполняться вручную действие в центре администрирования Office 365 (в разделе Параметры службы | Защищенного клиента хранилища) его включить. Для получения дополнительных сведений см [Запросы защищенного хранилища клиента Office 365](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2).

Все запросы службы для Exchange Online и SharePoint Online, обрабатываются системой защищенного хранилища. И с защищенного хранилища клиента проходит через процесс утверждения защищенного хранилища любые операции службы, создавая необходимость доступ к этим службам с доступом к данным клиента, а затем позволяет клиенту утвердить или отклонить запрос в дальнейшем.
 
*На рисунке 1 - рабочего процесса защищенного хранилища клиента*

Если запрос отклонен с клиентом, инженер службы поддержки Майкрософт не смогут получить доступ к содержимому клиента и не сможет завершить создание операции службы. Если запрос утвержден клиентом, инженер службы поддержки Майкрософт будет ограничен в времени доступа к контенту клиента через интерфейсы управления отслеживаемых и ограниченное. С помощью защищенного хранилища и защищенного хранилища клиента все утвержденные доступа выполняемых уникальных пользователей, внесение инженеров ответственность за их обработки данных клиента.

## <a name="just-in-time-access"></a>В время доступа
Корпорация Майкрософт использует принцип доступа в времени (Требованию) для Office 365 для уменьшения риска для изменения учетных данных и Навесной атак. Требованию удаляет сохраняемого административного доступа к службам и заменяет эти права возможность повышать в этих ролей по запросу. Удаление сохраняемого прав администратора гарантирует, что учетные данные доступны, только когда они необходимы и удаляет рисков, которые вызывают компании в случаях, когда кража учетных данных.

Модель доступа к Требованию требуется инженерам запросить повышенными привилегиями в течение ограниченного периода для выполнения административных задач. Кроме того OCEs используйте временные учетные записи, созданные с помощью автоматически созданные сложные пароли и предоставления только ролей, которые позволяют им для выполнения необходимых задач. К примеру административного доступа, предоставленных с защищенного хранилища привязкой времени и количество времени, доступа зависит от роли, запрашиваемый. Инженер указывает продолжительность времени доступа, необходимые при выполнении запроса к системе защищенного хранилища. Система защищенного хранилища будет отклонять запросы, где при запросе превышает максимальное разрешенное время для повышения прав. После окончания срока действия запросы на повышение прав удаляется административного доступа и срока действия временной учетной записи.

Если право и Утверждено для доступа (например, чтобы выполнить отладку в системе), инженеров направить однократного использования пароль администратора, созданное системы авторизации каждый раз, когда утвержденных запрос с повышенными правами доступа. Этот пароль копируются в безопасном пароль, инженер, отдельно от Инженер службы поддержки учетных данных для корпоративной среды Microsoft и рассчитан только на сеанс, для которого было утверждено с повышенными правами доступа.

## <a name="constrained-management-interfaces"></a>Интерфейсы управления ограниченного
Для выполнения задач администрирования OCEs использовать двух интерфейсов управления: удаленного рабочего стола с защитой шлюзов служб терминалов (TSGs) и удаленной оболочки PowerShell. В рамках этих управления доступны интерфейсы, которые политик программного обеспечения и управления доступом, передающие значительные ограничения на какие приложения могут быть выполнены и какие команды и командлетов. 

Серверы Office 365 ограничить количество одновременных сеансов для одного сеанса — служба группы администратора, на сервер. TSGs настроены для обеспечения единого одновременных сеансов для пользователей, а не разрешать нескольких сеансов. TSGs Разрешить администраторам группы службы Office 365 для подключения к нескольким серверам параллельно, с помощью одного сеанса на каждом сервере, поэтому администраторы могут эффективно выполнять свои обязанности. Группа администраторов службы нет никаких разрешений TSGs сами. TSG] используется только для применения параметров многофакторная проверка подлинности (многофакторной проверкой Подлинности) и требований шифрования. Когда администратор группы службы подключается к серверу через TSG], определенного сервера будет ограничивает сеанса одного на администратора.

Ограничения использования подключений и конфигурации требования к численности специалистов по Office 365 установленные групповых политик Active Directory. Эти политики включают следующие характеристики:
- TSGs настроены на использование только [FIPS](https://www.microsoft.com/en-us/TrustCenter/Compliance/FIPS) 140-2 проверки шифрования
- Сеансы TSG] настраиваются для отключения в течение 30 минут бездействия пользователя
- Сеансы TSG] настраиваются автоматически журнала отключено через 24 часа

Подключения к TSGs также требуется многофакторной проверкой Подлинности с помощью учетной записи, которая не связана с учетные данные организации Инженер службы поддержки Майкрософт и отдельные физические смарт-карт. Инженеры предоставляются в различных смарт-карт для различных платформах и секретов платформы управления позволяют обеспечить безопасное хранение учетных данных. TSGs использовать групповые политики Active Directory, чтобы контролировать, кто может войти в систему на удаленных серверах, количество разрешенных сеансов и параметры таймаута простоя. Дополнительные политики на месте для ограничения доступа к разрешенные приложения и ограничить доступ к Интернету.

В дополнение к удаленного доступа с помощью специально настроенных TSGs Exchange Online позволяет с помощью операции Инженер службы ролей пользователям открывать определенные административные функции на серверах приложений с помощью удаленной оболочки PowerShell. Для этого пользователя должны быть авторизованы для доступа только для чтения (Отладка) в рабочей среде Office 365. Распространение принципу предоставления минимальных прав включен так же, как он включен для TSGs, с помощью процесса защищенного хранилища.

Для удаленного доступа имеется балансировку сетевой нагрузки виртуальный IP-адрес каждого центра обработки данных, который выступает в качестве точки доступа. Командлеты Remote PowerShell, которые могут быть выполнены основаны на уровень привилегий, определенный в утверждение доступа, полученные в ходе проверки подлинности. Эти командлеты являются только административные функции, которые могут получить доступ к и выполняются пользователями, подключение с помощью этого метода. Remote PowerShell используется для ограничения области поиска команд, доступных для Инженер службы поддержки, который основан на параметрах уровень доступа, предоставленный через процесс защищенного хранилища. Например в Exchange Online Get-Mailbox можно найти, но не приведет к Set-Mailbox.