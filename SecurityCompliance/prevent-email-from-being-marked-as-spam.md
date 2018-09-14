---
title: Как не допустить, чтобы настоящая почта помечалась как спам в Office 365
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 34823bbc-a3e3-4949-ba42-97c73997eeed
description: Сведения о том, как предотвратить попадание подлинных сообщений в папку нежелательной почты и не допустить, чтобы они помечались как спам в Office 365.
ms.openlocfilehash: d092dc0a1a222f51f48102eb8c07e8e6051aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534469"
---
# <a name="how-to-prevent-real-email-from-being-marked-as-spam-in-office-365"></a>Как не допустить, чтобы настоящая почта помечалась как спам в Office 365

 **Подлинные электронные сообщения помечаются как спам в Office 365? Попробуйте это решение.**
  
Exchange Online Protection (EOP) старается отфильтровывать спам, чтобы в папку "Входящие" не попадало содержимое, которое не хотят видеть пользователи. Но иногда EOP отфильтровывает сообщения, которые вам нужны.
  
## <a name="determine-the-reason-why-the-message-was-marked-as-spam"></a>Определение причины, по которой сообщение было помечено как спам

Многие проблемы со спамом в Office 365 можно устранить, [просмотрев заголовки электронных сообщений](https://support.office.com/article/cd039382-dc6e-4264-ac74-c048563d212c) и определив причину проблемы. Если вы видите заголовок сообщения с именем X-Forefront-Antispam-Report, содержащий строку SFV:NSPM, это означает, что служба Exchange Online Protection (EOP) проверила сообщение и посчитала его спамом. В этом случае настоятельно рекомендуем [воспользоваться надстройкой "Отчет о сообщении"](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2), чтобы помочь нам улучшить свои фильтры. Если это значение отсутствует в заголовках, это может означать, что либо сообщение не прошло проверку на спам, либо возникла проблема с конфигурацией, из-за которой сообщение было ошибочно классифицировано как спам. Вы можете [узнать больше о заголовках сообщений для защиты от спама](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx).
  
Ищите в заголовке перечисленные ниже названия и значения.
  
### <a name="x-forefront-antispam-report"></a>X-Forefront-Antispam-Report

- **SFV:BLK**. Указывает на то, что сообщение было помечено как спам, потому что адрес отправителя указан в списке заблокированных отправителей на стороне получателя. 
    
- **SFV:SKS**. Указывает на то, что сообщение было помечено как спам до того, как оно прошло фильтр содержимого. В частности, правило транспорта могло пометить сообщение как спам. Выполните трассировку сообщения, чтобы узнать, срабатывало ли правило транспорта, которое могло задать высокую вероятность нежелательной почты. 
    
- **SFV:SKB**. Указывает на то, что сообщение было помечено как спам по причине соответствия списку блокировки в политике фильтра нежелательной почты. 
    
- **SFV:BULK**. Указывает на то, что значение уровня массовой жалобы (BCL) в заголовке x-microsoft-antispam превышает границу, заданную для фильтра содержимого. Массовые рассылки — это электронные сообщения, на которые пользователи могли подписаться, но которые все равно могут быть нежелательными. Найдите в заголовке X-Microsoft-Antispam свойство BCL. Если значение BCL ниже границы, заданной в фильтре содержимого, вы можете настроить границу так, чтобы такие массовые рассылки помечались как спам. Разные пользователи по-разному относятся к массовым рассылкам и имеют разные предпочтения [касательно их обработки](https://blogs.msdn.microsoft.com/tzink/2014/08/25/different-levels-of-bulk-mail-filtering-in-office-365/). Вы можете создавать различные политики или правила для пользователей с разными предпочтениями.
    
- **CAT:SPOOF** или **CAT:PHISH**. Указывает на то, что сообщение похоже на поддельное, то есть его источник вызывает подозрения и его не удается проверить. Если письмо подлинное, отправителю следует надлежащим образом настроить инфраструктуру политики отправителей и DKIM. Дополнительные сведения представлены в заголовке Authentication-Results. Хотя трудно сделать так, чтобы все отправители использовали надлежащие способы проверки подлинности, обход этих проверок может подвергнуть вас большой опасности и является одной из наиболее распространенных причин компрометации. 
    
### <a name="x-customspam"></a>x-customspam

- Наличие этого заголовка означает, что сообщение было помечено как спам, потому что в вашем фильтре содержимого [включен один из расширенных параметров нежелательной почты](https://technet.microsoft.com/library/jj200750%28v=exchg.150%29.aspx). Если вам не нужны эти функции, рекомендуем использовать параметры по умолчанию. 
    
## <a name="solutions-to-additional-causes-of-too-much-spam"></a>Устранение других причин получения больших объемов спама

Для эффективной работы Exchange Online Protection (EOP) администраторы должны выполнить несколько задач. Если вы не являетесь администратором клиента Office 365 и получаете слишком много спама, то можете обратиться к администратору за помощью в выполнении этих задач. В противном случае можете переходить к разделу для пользователей.
  
### <a name="for-admins"></a>Для администраторов

- **Измените записи DNS, чтобы они указывали на Office 365.** Чтобы служба EOP обеспечивала защиту, записи DNS почтового обменника (MX) для всех доменов должны указывать исключительно на Office 365. Если запись MX не указывает на Office 365, то EOP не будет фильтровать спам для пользователей. Если вы хотите использовать другую службу или другое устройство для фильтрации спама на своем домене, рекомендуем отключить защиту от спама в EOP. Для этого вы можете создать правило транспорта, которое задает для вероятности нежелательной почты значение –1. Если позже вы решите использовать EOP, обязательно удалите это правило транспорта. 
    
- **Отключите фильтр SmartScreen в Outlook.** Если пользователи работают с классическим клиентом Outlook, им следует отключить фильтр SmartScreen, поддержка которого прекращена. Работа этого фильтра может приводить к ложным срабатываниям. При использовании обновленного классического клиента Outlook в этом не должно быть необходимости. 
    
- **Включите для пользователей надстройку "Отчет о сообщении".** Настоятельно рекомендуем [включить надстройку "Отчет о сообщении" для пользователей](enable-the-report-message-add-in.md). Администратор также может просматривать отзывы пользователей и настраивать проблемные параметры в соответствии с распространенными жалобами.
    
- **Сразу делайте отправителя разрешенным.** Если требуется быстро сделать того или иного отправителя разрешенным, настоятельно рекомендуем **разрешать ТОЛЬКО его IP-адрес**. Вы также можете сделать отправителя разрешенным и гарантировать, что он будет проходить проверки подлинности (например, инфраструктуры политики отправителей и DKIM), создав правило транспорта, которое ищет как домен отправителя, **так и** заголовок Authentication-Results, указывающий на успешную проверку. 
    
### <a name="for-users"></a>Для пользователей

- **Сообщайте о спаме в корпорацию Майкрософт.** Сообщайте корпорации Майкрософт о нежелательных сообщениях с помощью [надстройки "Отчет о сообщении"](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2). Кроме того, вы можете отправить сообщение по адресу junk@office365.microsoft.com, вложив в него одно или несколько писем.
    
    **Важно!** Если вы не перешлете сообщения в виде вложений, то [в них не будет заголовков и мы не сможем усовершенствовать](https://blogs.msdn.microsoft.com/tzink/2017/11/30/when-creating-support-tickets-about-spam-be-sure-to-include-message-headers/) фильтр нежелательной почты в Office 365. 
    
- **Добавьте отправителя в список разрешений, но не злоупотребляйте этой возможностью.** В качестве крайней меры вы можете [заблокировать или разрешить отправителя в настройках нежелательной почты](https://support.office.com/article/48c9f6f7-2309-4f95-9a4d-de987e880e46). В этом случае следует опасаться целенаправленных попыток фишинга при помощи писем в папке "Входящие".
    
