---
title: Использование поиска контента для поиска данных сторонних производителей, которая была импортирована в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Используйте средство поиска контента обнаружения электронных данных для поиска элементов, которые были импортированы из источника данных сторонних производителей для почтовых ящиков в Office 365. Можно создать запрос для поиска всех импортированных элементов или создать запрос для поиска определенных сторонних производителей типов данных. В этой статье приведены значения, которые можно использовать в запросе ключевое слово для поиска типы данных сторонних производителей, которые могут быть импортированы в Office 365.
ms.openlocfilehash: 90d9dc52dcd9dba9bc273dfcf1c5f22e3913d6ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22535095"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a>Использование поиска контента для поиска данных сторонних производителей, которая была импортирована в Office 365

Можно использовать [средство поиска контента обнаружения электронных данных](content-search.md) в Office 365 безопасность &amp; центре соответствия требованиям для поиска элементов, которые были импортированы из источника данных сторонних производителей для почтовых ящиков в Office 365. Можно создать запрос для поиска всех импортированных элементов данных в сторонних производителей или создать запрос для поиска только элементов конкретного данных сторонних производителей. Кроме того можно также создать политику хранения на основе запроса или обнаружения электронных данных запроса на удержание для сохранения данных сторонних производителей в Office 365. 
  
Дополнительные сведения об импорте данных сторонних производителей и список типов данных сторонних производителей, которые могут быть импортированы в Office 365 можно [данных архивации сторонних производителей в Office 365](archiving-third-party-data.md). 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a>Создание запроса для поиска всех данных сторонних производителей

Для поиска (или поместить на удержание) любого типа данных сторонних производителей, импортированные в Office 365, вы можете вы можно использовать `kind:externaldata` значение свойства пара сообщений в поле ключевое слово для поиска контента или при создании запроса на удержание. Например для поиска элементов, которые были импортированы из любого источника данных сторонних производителей и со словом «contoso» в свойство Subject импортированного элемента, можно использовать следующий запрос: 
  
```
kind:externaldata AND subject:contoso
```

Свойство subject включает в себя в предыдущем примере запроса ключевого слова. Список других свойств для данных сторонних производителей элементов, которые могут включать в запрос ключевого слова, обратитесь к разделу «Дополнительные сведения» в [данных архивации сторонних производителей в Office 365](archiving-third-party-data.md#more-information).
  
При создании запросов для поиска и хранения данных сторонних производителей, чтобы сузить результаты поиска можно также использовать условия. Дополнительные сведения о создании запросов поиска контента видеть [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md).
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a>Создание запроса для поиска определенных типов данных сторонних производителей

Вместо поиск всех типов данных сторонних производителей, можно создавать запросы, что только поиск укажите тип данных сторонних производителей с помощью следующей пары значение свойства сообщения в поле ключевое слово для поиска контента:
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

Например для поиска только данные Facebook (en), содержащий слово «contoso» в свойстве темы, можно использовать следующий запрос:
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

В следующей таблице приведены типы данных сторонних производителей, которые можно выполнить поиск и значения будут использоваться для `itemclass:` сообщений свойство для поиска специально для этого типа данных сторонних производителей. Обратите внимание на то, что синтаксис запроса не учитывают регистр. 
  
|**Тип данных сторонних производителей**|**Значение `itemclass:` свойства**|
|:-----|:-----|
|AIM;  <br/> | `ipm.externaldata.AIM*` <br/> |
|American Idol;  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|AOL с клиентом Pivot;  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|Apple Juice;  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|Ares;  <br/> | `ipm.externaldata.Ares*` <br/> |
|Axs Encrypted;  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|Axs Exchange;  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|Axs Local Archive;  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|Заполнитель Axs  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|Axs Signed;  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|Bazaarvoice  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|BearShare  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|Отправляемому BitTorrent  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|BlackBerry  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|Журналы звонков blackBerry  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|BlackBerry Messenger  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|BlackBerry ПИН-кода  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|BlackBerry SMS  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|Bloomberg;  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|Bloomberg Mail;
  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|Bloomberg системы обмена сообщениями  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|Box;
  <br/> | `ipm.externaldata.Box*` <br/> |
|Cisco обмена мгновенными Сообщениями &amp; Server сведения о присутствии  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|Cisco Jabber;  <br/> | `ipm.externaldata.Jabber*` <br/> |
|CipherCloud для Salesforce Chatter;  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|Direct Connect;  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|Facebook  <br/> | `ipm.externaldata.Facebook*` <br/> |
|FastTrack  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|FXConnect;  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|Flickr;
  <br/> | `ipm.externaldata.Flickr*` <br/> |
|Gnutella;  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|Google+;
  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|Google Talk  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|GoToMyPC  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|HipChat  <br/> | `ipm.externaldata.HipChat*` <br/> |
|Hopster;  <br/> | `ipm.externaldata.Hopster*` <br/> |
|HubConnex  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|Подключения к IBM  <br/> | `ipm.externaldata.Connections*` <br/> |
|IBM SameTime  <br/> | `ipm.externaldata.Sametime*` <br/> |
|ICE чата  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|Indii Messenger;
  <br/> | `ipm.externaldata.Indii*` <br/> |
|Instagram;
  <br/> | `ipm.externaldata.Instagram*` <br/> |
|Instant Bloomberg;
  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|InvestEdge  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|IRC;  <br/> | `ipm.externaldata.IRC*` <br/> |
|Jive;
  <br/> | `ipm.externaldata.Jive*` <br/> |
|JiveApiRetention  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|JXTA;  <br/> | `ipm.externaldata.JXTA*` <br/> |
|LinkedIn  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|MFTP;  <br/> | `ipm.externaldata.MFTP*` <br/> |
|Майкрософт для объединенных Коммуникаций  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|Выровнять виду  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|Mobile Guard;  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|MSN;  <br/> | `ipm.externaldata.MSN*` <br/> |
|MySpace  <br/> | `ipm.externaldata.MySpace*` <br/> |
|NEONetwork;  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|OpenNap  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|Pinterest;  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|Pivot;  <br/> | `ipm.externaldata.Pivot*` <br/> |
|QQ;  <br/> | `ipm.externaldata.QQ*` <br/> |
|Microsoft SharePoint  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|Salesforce Chatter;  <br/> | `ipm.externaldata.Chatter*` <br/> |
|Skype для бизнеса  <br/> | `ipm.externaldata.Skype*` <br/> |
|Slack Enterprise Grid;  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|SoftEther  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|
Squawker;
  <br/> | `ipm.externaldata.Squawker*` <br/> |
|Symphony;  <br/> | `ipm.externaldata.Symphony*` <br/> |
|Thomson Reuters.  <br/> | `ipm.externaldata.Reuters*` <br/> |
| Thomson Reuters Eikon Messenger.
  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|Tor;  <br/> | `ipm.externaldata.Tor*` <br/> |
|TTT;  <br/> | `ipm.externaldata.TTT*` <br/> |
|Твиттер  <br/> | `ipm.externaldata.Twitter*` <br/> |
|UBS Chat;
  <br/> | `ipm.externaldata.UBS*` <br/> |
|Vimeo.  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|WinMX  <br/> | `ipm.externaldata.WinMX*` <br/> |
|Winny;  <br/> | `ipm.externaldata.Winny*` <br/> |
|Yahoo!  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|Yammer  <br/> | `ipm.externaldata.Yammer*` <br/> |
|YellowJacket  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|Youtube (en)  <br/> | `ipm.externaldata.YouTube*` <br/> |
