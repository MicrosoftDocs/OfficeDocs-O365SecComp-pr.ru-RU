---
title: Административные элементы управления доступом в Office 365
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
description: 'Сводка: Обзор Office 365 категоризации административного доступа к элементам управления и данных.'
ms.openlocfilehash: afa15d37aa8542985c59dbd9e3d82368421530e8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534854"
---
# <a name="administrative-access-controls-in-office-365"></a>Административные элементы управления доступом в Office 365 

## <a name="introduction"></a>Введение
Компания Майкрософт всегда тратит связан с активным и соответствующим образом в систем и элементов управления, которые автоматизируют большинство операций Office 365 при ограничении намеренно корпорации Майкрософт доступ к содержимому клиента. Люди управляют службы и программного обеспечения работает служба. Это позволяет корпорации Майкрософт для управления Office 365 масштаба, а также управление риски, связанные с внутреннего угрозы для клиентов контент, такой как сообщение о нежелательном субъекты фишинга направленных Инженер службы поддержки Майкрософт и т. д.

По умолчанию специалистов корпорации Майкрософт имеют административные полномочия ноль положение и ноль положение доступ к содержимому клиентов в Office 365. Инженер службы поддержки Майкрософт ограниченный, аудит и безопасного доступа к клиенту контента в течение ограниченного периода времени, но только в случае необходимости для операций службы и только после утверждения участником высшего руководства Microsoft (и для клиентов, находящихся лицензию для функции клиента защищенного хранилища клиента).

Корпорация Майкрософт предоставляет Интернет-служб, включая Office 365, с помощью нескольких форм облачных доставки:

- **Общедоступные облака** - включает в себя многопользовательские версии Office 365, Azure и другие службы, которые размещаются в Северной Америке, Южная Америка, Европа, Азия, Австралия, и т.д.
- **Национальный облака** - включает в себя все облака sovereign и сторонних производителей, используемых за пределами США (за исключением тех, указанной выше), такие как Office 365 в Китае (который управляется 21Vianet) и Office 365 в Германии (который управляется Microsoft, но в разделе модель в котором немецкого данных доверенного лица, Telekom немецкой элементов управления и отслеживает корпорации Майкрософт доступ к данным клиента и систем, которые содержат данные клиента).
- **В облаках государственных организаций** - включает в себя службы Office 365 и Azure, доступные в Соединенных Штатах Америки правительственных клиентов.

Для целей данной статьи службы Office 365: [Exchange Online](https://docs.microsoft.com/Exchange/exchange-online), [Exchange Online Protection](https://docs.microsoft.com/Office365/SecurityCompliance/eop/exchange-online-protection-overview), [SharePoint Online](https://docs.microsoft.com/sharepoint/sharepoint-online) (в том числе [OneDrive для бизнеса](https://docs.microsoft.com/OneDrive/onedrive)) и [Скайп для бизнеса](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online)с дополнительной информации о некоторые элементы управления доступа в [Yammer Enterprise](https://support.office.com/article/yammer-–-admin-help-e1464355-1f97-49ac-b2aa-dd320b179dbe?ui=en-US&rs=en-US&ad=US) . Другие службы Office 365 выходят за рамки данной статьи.

## <a name="office-365-access-controls"></a>Элементы управления доступа к Office 365
Для целей контроля доступа данные Office 365 к категории пользовательских данных или других типов данных. Данные клиента — это все данные, предоставленные пользователем или от имени клиента с помощью клиента Office 365 службы, такие как содержимого клиентов (содержимое непосредственно создавать или отправлять по электронной почте, SharePoint Online контента, включая пользователей Office 365 мгновенных сообщений в календаре элементов, документов и контакты, хранящиеся в Office 365) и сведения для конечных пользователей (EUII) (данных, который является уникальным для пользователя или ссылок на основе для отдельных пользователей, однако не включает содержимое клиента). 

Другие типы данных включают данные учетной записи (включает в себя административные данные, которые являются сведений, предоставленных администраторов при их регистрации или приобретение служб и оплаты данные, которые являются сведения о оплаты инструменты, такие как кредит карт подробные сведения), организационно характера (данные, которые можно использовать для идентификации клиента; или данные об использовании; он не ссылок на основе для отдельных пользователей и не включает содержимое клиента) и системные метаданные (в том числе журналы службы, которые содержат параметры конфигурации состояние системы Microsoft IP-адресов и технические сведения о подписках и клиентов).

Microsoft установила механизма контроля доступа для убедитесь, что никто не имеет неутвержденных доступ к данным контроля доступа или данные клиента (используется для управления доступом к других типов данных и функций в среде, включая доступ к контента клиента или EUII; он включает в себя Microsoft пароли, сертификаты безопасности и других данных, связанных с проверки подлинности) или неутвержденных физических, логических или удаленного доступа в рабочей среде Office 365.

Элементы управления доступом, используемые корпорацией Майкрософт для работы Office 365, можно разбить на три категории:
- Изоляция элементов управления
- Элементы управления персоналом
- Элементы управления технологии

При объединении, эти элементы управления помогают предотвратить и обнаружения вредоносных действий в Office 365. В дополнение к изоляции, персонала и элементы управления технологии, используемые корпорацией Майкрософт, является четвертой категории элементов управления: те, реализованные теми клиентами.

Office 365 позволяет управлять своими данными в одной и той же информации способ управления в локальной среде. Человека, который регистрируется организации в Office 365 автоматически становится глобального администратора (admin). Глобального администратора имеет доступ ко всем возможностям в порталы управления (например, центры администрирования и удаленной оболочки PowerShell) и можно создать или изменить пользователей, назначение роли администратора для других пользователей, сброс паролей пользователей, управления пользовательскими лицензиями, Управление доменами и утверждать защищенного хранилища клиента запросы, среди прочего. Рекомендуется назначить каждой организации по крайней мере две учетные записи администратора, и в зависимости от размера организации, можно указать несколько администраторов, которые выполняют различные функции. Сведения о назначении роли администраторов и разрешения содержатся в разделе [Назначение ролей администратора в Office 365](https://support.office.com/article/Assigning-admin-roles-in-Office-365-eac4d046-1afd-4f1a-85fc-8219c79e1504) и [роли администраторов об Office 365](https://support.office.com/article/Permissions-in-Office-365-DA585EEA-F576-4F55-A1E0-87090B6AAA9D).


## <a name="related-links"></a>Ссылки по теме

- [Изоляция элементов управления](office-365-isolation-controls.md)
- [Элементы управления персоналом](office-365-personnel-controls.md)
- [Элементы управления технологии](office-365-technology-controls.md)
- [Элементы управления доступом к мониторингу и аудиту](office-365-monitoring-and-auditing-access-controls.md)
- [Элементы управления доступом к Yammer корпоративный](office-365-yammer-enterprise-access-controls.md)