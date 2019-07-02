---
title: Поиск данных третьих сторон, импортированных в Office 365, с помощью поиска контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Воспользуйтесь средством поиска обнаружения электронных данных поиска контента для поиска элементов, импортированных в почтовые ящики в Office 365, из стороннего источника данных. Можно создать запрос для поиска всех импортированных элементов или создать запрос для поиска определенных типов данных третьих сторон. В этой статье перечислены значения, которые можно использовать в запросе с ключевыми словами для поиска в сторонних типах данных, которые можно импортировать в Office 365.
ms.openlocfilehash: 0881456d377569fb55f0daf0d0a8a2a15bce62fc
ms.sourcegitcommit: f2798d46acfbd56314e809cd3fe0350be807e420
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2019
ms.locfileid: "35014755"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Поиск данных третьих сторон, импортированных в Office 365, с помощью поиска контента

[Средство обнаружения электронных данных поиска контента](content-search.md) можно использовать в центре безопасности & соответствия требованиям для поиска элементов, импортированных в почтовые ящики в Office 365, из стороннего источника данных. Вы можете создать запрос для поиска всех импортированных сторонних элементов данных или создать запрос для поиска только определенных элементов данных стороннего производителя. Кроме того, вы также можете создать политику хранения Office 365 на основе запросов или удержание обнаружения электронных данных на основе запросов для сохранения сторонних данных в Office 365. 
  
Дополнительные сведения об импорте сторонних данных и списке типов данных сторонних производителей, которые можно импортировать в Office 365, приведены в статье [Работа с партнером для архивации сторонних данных в office 365](work-with-partner-to-archive-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Создание запроса для поиска всех сторонних данных

Чтобы выполнить поиск (или поместиться на удержании) любого типа сторонних данных, импортированных в Office 365, можно использовать параметр `kind:externaldata` Message-value в поле ключевое слово для поиска контента или при создании удержания на основе запроса. Например, чтобы найти элементы, импортированные из стороннего источника данных и содержащие слово "contoso" в свойстве subject импортированного элемента, используйте следующий запрос: 
  
```
kind:externaldata AND subject:contoso
```

Пример запроса к предыдущему ключевому слову включает свойство Subject. Список других свойств сторонних элементов данных, которые можно включить в запрос ключевых слов, приведен в разделе "Дополнительные сведения" в разделе " [Работа с партнером для архивации сторонних данных в Office 365](work-with-partner-to-archive-third-party-data.md#more-information)".
  
При создании запросов для поиска и хранения сторонних данных можно также использовать условия для сужения результатов поиска. Дополнительные сведения о создании поисковых запросов можно узнать в статье [запросы и условия поиска контента](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Создание запроса для поиска определенных типов сторонних данных

Вместо того чтобы искать все типы сторонних данных, можно создать запросы, которые ищут только сведения об указанном типе сторонних данных, используя следующую комбинацию свойства сообщения в поле ключевое слово для поиска контента:
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Например, чтобы искать только данные Facebook, содержащие слово "contoso" в свойстве subject, используйте следующий запрос:
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

В следующей таблице приведены типы данных третьих сторон, которые можно найти, а также значение, которое будет использоваться для свойства `itemclass:` Message для точного поиска этого типа сторонних данных. Обратите внимание, что в синтаксисе запроса регистр не учитывается. 
  
|**Сторонний тип данных**|**Значение `itemclass:` свойства**|
|:-----|:-----|
|СТАРАЙТЕСЬ  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol;  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL с клиентом Pivot;  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice;  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Арес  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted;  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange;  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive;  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Заполнитель AXS  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed;  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Базаарвоице  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|Беаршаре  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|БитТоррент  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|BlackBerry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|Журналы звонков BlackBerry  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|Служба обмена сообщениями BlackBerry  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|ПИН-код BlackBerry  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail;  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Обмен сообщениями Bloomberg  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box  <br/> | `ipm.externaldata.Box*` <br/> |
|Сервер присутствия &amp; для обмена мгновенными сообщениями Cisco  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber;  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud для Salesforce Chatter;  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Direct Connect;  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|Фксконнект  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Гнутелла  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google +  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google говорите  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|Готомипк  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|Хипчат  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Хопстер  <br/> | `ipm.externaldata.Hopster*` <br/> |
|Хубконнекс  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|Подключения IBM  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|Чат  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger;  <br/> | `ipm.externaldata.Indii*` <br/> |
|Инстаграм  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg;  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|Инвестедже  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive  <br/> | `ipm.externaldata.Jive*` <br/> |
|Живеапиретентион  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|ЖКСТА  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|МФТП  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Microsoft UC  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|Выровнять по расмнению  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard;  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|СЕТЬЮ  <br/> | `ipm.externaldata.MSN*` <br/> |
|Миспаце  <br/> | `ipm.externaldata.MySpace*` <br/> |
|Неонетворк  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|Опеннап  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Пинтерест  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Сводка  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter;  <br/> | `ipm.externaldata.Chatter*` <br/> |
|Skype для бизнеса  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid;  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|Софтесер  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|Скуавкер  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Симфони  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters.  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger.  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Тор  <br/> | `ipm.externaldata.Tor*` <br/> |
|ТТТ  <br/> | `ipm.externaldata.TTT*` <br/> |
|Twitter  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat;  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|Винмкс  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Винни  <br/> | `ipm.externaldata.Winny*` <br/> |
|Yahoo!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|Елловжаккет  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|YouTube  <br/> | `ipm.externaldata.YouTube*` <br/> |
