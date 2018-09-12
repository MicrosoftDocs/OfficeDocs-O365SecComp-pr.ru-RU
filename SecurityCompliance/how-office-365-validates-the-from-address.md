---
title: Как Office 365 проверяет адрес отправителя, чтобы запретить фишинга
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
description: 'Чтобы предотвратить фишинга, Office 365 и Outlook.com теперь требуется соответствие требованиям RFC для из: адреса.'
ms.openlocfilehash: 8425d4ef7635c2beddcd7915daf73736432d4ca9
ms.sourcegitcommit: d89c24258123a3ffde574a391d59afd3aea8470d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2018
ms.locfileid: "23955431"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="4a513-103">Как Office 365 проверяет адрес отправителя, чтобы запретить фишинга</span><span class="sxs-lookup"><span data-stu-id="4a513-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="4a513-p101">Office 365 и учетных записей электронной почты Outlook.com получают все более большое число фишинга. Одним из способов использования фишеры — отправить сообщения, для которых значения для отправителя: адрес, по которому не соответствующий стандарту [RFC 5322](https://tools.ietf.org/html/rfc5322). From: адрес также называется адрес 5322.From. Чтобы предотвратить этот тип фишинга, Office 365 и Outlook.com требуют сообщений, полученных службой для включения стандарту RFC из: адрес, как описано в этой статье.</span><span class="sxs-lookup"><span data-stu-id="4a513-p101">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks. One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322). The From: address is also called the 5322.From address. To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4a513-p102">Сведения в этой статье необходимо иметь общее представление об общий формат адреса электронной почты. Дополнительные сведения см в [RFC 5322](https://tools.ietf.org/html/rfc5322) (особенно разделах 3.2.3, 3.4 и 3.4.1), [согласно документу RFC 5321](https://tools.ietf.org/html/rfc5321), а также [RFC 3696](https://tools.ietf.org/html/rfc3696). В этой статье рассматривается принудительное применение политики для адреса 5322.From. В этой статье не адрес 5321.MailFrom.</span><span class="sxs-lookup"><span data-stu-id="4a513-p102">The information in this article requires you to have a basic understanding of the general format of email addresses. For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696). This article is about policy enforcement for the 5322.From address. This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="4a513-p103">К сожалению, по-прежнему существует несколько серверов старую электронную почту из Интернета, продолжить отправлять «допустимых», в которых отсутствуют сообщения электронной почты или неверно сформированные из: адрес. Если вы регулярно получать электронную почту из организации, использующие эти устаревших систем, рекомендуется других компаний для обновления их почтовых серверов в соответствии со стандартами современных безопасности.</span><span class="sxs-lookup"><span data-stu-id="4a513-p103">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address. If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="4a513-114">Корпорация Майкрософт будет запущен процесс развертывания реализацию политик, описанных в этой статье на 9 ноября 2017.</span><span class="sxs-lookup"><span data-stu-id="4a513-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="4a513-115">Как Office 365 контролирует использование допустимым из: адрес для предотвращения фишинга</span><span class="sxs-lookup"><span data-stu-id="4a513-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="4a513-p104">Office 365 внесение изменений в способ обеспечивает использование From: адресов в сообщениях, она получает чтобы лучше защиты компьютера от фишинга. В этой статье:</span><span class="sxs-lookup"><span data-stu-id="4a513-p104">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks. In this article:</span></span>
  
- [<span data-ttu-id="4a513-118">Все сообщения должны включать допустимый из: адрес</span><span class="sxs-lookup"><span data-stu-id="4a513-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="4a513-119">Формат From: адрес, если не включить отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4a513-119">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="4a513-120">Формат From: адрес при включении отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4a513-120">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="4a513-121">Дополнительные примеры допустимых и недопустимых из: адреса</span><span class="sxs-lookup"><span data-stu-id="4a513-121">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="4a513-122">Не отображать автоматические ответы для настраиваемого домена без нарушения From: политика</span><span class="sxs-lookup"><span data-stu-id="4a513-122">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="4a513-123">Переопределение Office 365 из: адрес принудительное применение политики</span><span class="sxs-lookup"><span data-stu-id="4a513-123">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="4a513-124">Другие способы защиты от cybercrimes в Office 365</span><span class="sxs-lookup"><span data-stu-id="4a513-124">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="4a513-125">Отправка сообщения от имени другого пользователя в не влияет на это изменение для получения дополнительных сведений ознакомьтесь с блогом Terry Zink "[что имеется в виду при обращении к «отправителя» сообщения электронной почты?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)«.</span><span class="sxs-lookup"><span data-stu-id="4a513-125">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="4a513-126">Все сообщения должны включать допустимый из: адрес</span><span class="sxs-lookup"><span data-stu-id="4a513-126">All messages must include a valid From: address</span></span>
<span data-ttu-id="4a513-127"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-127"></span></span>

<span data-ttu-id="4a513-p105">Некоторые автоматическая отправка сообщения не добавляйте From: адреса при их отправки. В прошлом, при получении сообщения без From Office 365 или Outlook.com: адрес службы добавлены следующие по умолчанию из: адрес с сообщением, чтобы сделать его конечный результат:</span><span class="sxs-lookup"><span data-stu-id="4a513-p105">Some automated messages don't include a From: address when they are sent. In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="4a513-p106">Запуск 9 ноября 2017, Office 365 проведем изменений для его центров обработки данных и почтовых серверов, которых требует использования новое правило где сообщения без From: адрес больше не будет принято по Office 365 или Outlook.com. Вместо этого, все сообщения, полученные с Office 365 уже должен содержать действительный из: адрес. В противном случае сообщения будут отправляться в папки нежелательной почты или удаленных элементов в Outlook.com и Office 365.</span><span class="sxs-lookup"><span data-stu-id="4a513-p106">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com. Instead, all messages received by Office 365 must already contain a valid From: address. Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="4a513-133">Общие сведения о синтаксисе: недопустимый формат для отправителя: адрес для Office 365</span><span class="sxs-lookup"><span data-stu-id="4a513-133">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="4a513-134"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-134"></span></span>

<span data-ttu-id="4a513-p107">Формат значения From: адрес, заданный между несколькими RFC подробно. Существует множество вариантов адресации и что может рассматриваться как допустимое или недопустимое. Чтобы упростить ее, корпорация Майкрософт рекомендует использовать следующий формат и определения:</span><span class="sxs-lookup"><span data-stu-id="4a513-p107">The format for the value of the From: address is defined in detail across several RFCs. There are many variations on addressing and what may be considered valid or invalid. To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="4a513-138">Где:</span><span class="sxs-lookup"><span data-stu-id="4a513-138">Where:</span></span>
  
- <span data-ttu-id="4a513-p108">(Необязательно)  *отображаемое имя* — это фразу, описывающую владелец адреса электронной почты. Например это может быть более понятное имя, описывающее отправителя, чем имя почтового ящика. С помощью отображаемое имя является необязательным. Тем не менее если вы решите использовать отображаемое имя, корпорация Майкрософт рекомендует, что вы всегда заключите его в кавычки как показано.</span><span class="sxs-lookup"><span data-stu-id="4a513-p108">(Optional)  *displayname*  is a phrase that describes the owner of the email address. For example, this might be a more user-friendly name to describe the sender than the name of the mailbox. Using a display name is optional. However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="4a513-143">(Обязательно)  *EmailAddress* включает в себя:</span><span class="sxs-lookup"><span data-stu-id="4a513-143">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="4a513-144">Где:</span><span class="sxs-lookup"><span data-stu-id="4a513-144">Where:</span></span>
    
  - <span data-ttu-id="4a513-p109">(Обязательно)  *Local часть* — это строка, которая идентифицирует почтовый ящик, связанный с адресом. Является уникальным в пределах домена. Часто имя пользователя или идентификатор GUID владельца почтового ящика, используется как значение для локальной части.</span><span class="sxs-lookup"><span data-stu-id="4a513-p109">(Required)  *local-part*  is a string that identifies the mailbox associated with the address. This is unique within the domain. Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="4a513-148">(Обязательно)  *домен* — это полное доменное имя (FQDN) почтового сервера, на котором размещен почтовый ящик, обозначенный в локальной части адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4a513-148">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="4a513-149">Формат From: адрес, если не включить отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4a513-149">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="4a513-150"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-150"></span></span>

<span data-ttu-id="4a513-p110">A правильно отформатирован из: адрес, который не содержит отображаемое имя содержит только один адрес электронной почты или без угловые скобки. Корпорация Майкрософт рекомендует не разделяйте угловые скобки пробелами. Кроме того не добавляйте все действия после адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4a513-p110">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets. Microsoft recommends that you do not separate the angle brackets with spaces. In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="4a513-154">Допустимыми являются следующие примеры:</span><span class="sxs-lookup"><span data-stu-id="4a513-154">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="4a513-155">Следующий пример является допустимым, но не рекомендуется, поскольку он содержит пробелы между угловые скобки и адрес электронной почты:</span><span class="sxs-lookup"><span data-stu-id="4a513-155">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="4a513-156">Следующий пример является недопустимым, так как он содержит текст после адрес электронной почты:</span><span class="sxs-lookup"><span data-stu-id="4a513-156">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="4a513-157">Формат From: адрес при включении отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="4a513-157">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="4a513-158"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-158"></span></span>

<span data-ttu-id="4a513-159">Для из: адреса, которые включают значение в поле отображаемое имя, применяются следующие правила:</span><span class="sxs-lookup"><span data-stu-id="4a513-159">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="4a513-p111">Если адрес отправителя содержит отображаемое имя и отображаемое имя включает в себя запятыми, отображаемое имя должны быть заключены в кавычки. Например:</span><span class="sxs-lookup"><span data-stu-id="4a513-p111">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks. For example:</span></span>
    
    <span data-ttu-id="4a513-162">Следующий пример является допустимым:</span><span class="sxs-lookup"><span data-stu-id="4a513-162">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="4a513-163">Следующий пример является недопустимым:</span><span class="sxs-lookup"><span data-stu-id="4a513-163">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="4a513-164">Не заключение отображаемое имя в кавычки, если оно отображения содержит запятой является недопустимым RFC 5322.</span><span class="sxs-lookup"><span data-stu-id="4a513-164">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="4a513-165">Рекомендуется put кавычки вокруг отображаемое имя вне зависимости от ли является запятая в рамках отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="4a513-165">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="4a513-166">Если адрес отправителя содержит отображаемое имя, адрес электронной почты должны быть заключены в угловые скобки.</span><span class="sxs-lookup"><span data-stu-id="4a513-166">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="4a513-167">Рекомендуется, корпорация Майкрософт рекомендует вставить пробел между отображаемое имя и адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4a513-167">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="4a513-168">Дополнительные примеры допустимых и недопустимых из: адреса</span><span class="sxs-lookup"><span data-stu-id="4a513-168">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="4a513-169"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-169"></span></span>

- <span data-ttu-id="4a513-170">Допустимый:</span><span class="sxs-lookup"><span data-stu-id="4a513-170">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="4a513-p112">Недопустимый. Адрес электронной почты не заключено в угловые скобки:</span><span class="sxs-lookup"><span data-stu-id="4a513-p112">Invalid. The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="4a513-p113">Допустимый, но не рекомендуется. Отображаемое имя не в кавычках. Рекомендуется, всегда кавычки отображаемое имя:</span><span class="sxs-lookup"><span data-stu-id="4a513-p113">Valid, but not recommended. The display name is not in quotes. As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="4a513-p114">Недопустимый. Все, что заключен в кавычки, не только отображаемое имя:</span><span class="sxs-lookup"><span data-stu-id="4a513-p114">Invalid. Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="4a513-p115">Недопустимый. Существует не угловые скобки вокруг адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="4a513-p115">Invalid. There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="4a513-p116">Недопустимый. Нет места между отображаемое имя и левая угловая скобка:</span><span class="sxs-lookup"><span data-stu-id="4a513-p116">Invalid. There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="4a513-p117">Недопустимый. Нет места между quotation mark закрывающего тега вокруг отображаемое имя и левая угловая скобка.</span><span class="sxs-lookup"><span data-stu-id="4a513-p117">Invalid. There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="4a513-184">Не отображать автоматические ответы для настраиваемого домена без нарушения From: политика</span><span class="sxs-lookup"><span data-stu-id="4a513-184">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="4a513-185"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-185"></span></span>

<span data-ttu-id="4a513-p118">С помощью нового из: принудительное применение политики, больше не используется с: \< \> для отмены вывода автоматические ответы. Вместо этого необходимо настроить значение null, запись MX для настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="4a513-p118">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies. Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="4a513-p119">Запись ресурса почтового обменника (MX) представляет собой запись ресурса в DNS, которая идентифицирует почтовый сервер, который получает почту для домена. Автоматические ответы (и все ответы) естественно подавляются, так как не опубликованные адрес, на который отвечающий сервер может отправлять сообщения.</span><span class="sxs-lookup"><span data-stu-id="4a513-p119">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain. Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="4a513-190">При настройке значение null, запись MX для настраиваемого домена:</span><span class="sxs-lookup"><span data-stu-id="4a513-190">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="4a513-p120">Выберите домен, из которого необходимо отправлять сообщения, которые не принимает (принять) электронной почты. Например если основной домен contoso.com, можно выбрать noreply.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="4a513-p120">Choose a domain from which to send messages that doesn't accept (receive) email. For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="4a513-p121">Задайте значение null, запись MX для вашего домена. Значение null, запись MX состоит из одной точки, например:</span><span class="sxs-lookup"><span data-stu-id="4a513-p121">Set up the null MX record for your domain. A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="4a513-195">Дополнительные сведения о публикации значение null, MX можно [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="4a513-195">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="4a513-196">Переопределение Office 365 из: адрес принудительное применение политики</span><span class="sxs-lookup"><span data-stu-id="4a513-196">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="4a513-197"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-197"></span></span>

<span data-ttu-id="4a513-198">После завершения развертывание новой политики только можно пропустить эту политику для входящей почты, полученные из Office 365 с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="4a513-198">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="4a513-199">Списков разрешенных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="4a513-199">IP allow lists</span></span>
    
- <span data-ttu-id="4a513-200">Exchange Online правила потока почты</span><span class="sxs-lookup"><span data-stu-id="4a513-200">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="4a513-p122">Корпорация Майкрософт рекомендует переопределение принудительные From: политика. Переопределение эта политика может увеличить риск доступом для защиты от нежелательной почты, фишинга и других cybercrimes вашей организации.</span><span class="sxs-lookup"><span data-stu-id="4a513-p122">Microsoft strongly recommends against overriding the enforcement of the From: policy. Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="4a513-p123">Не может переопределить эту политику для исходящей почты, отправляемые в Office 365. Кроме того Outlook.com не даст переопределений любого типа, даже благодаря поддержке.</span><span class="sxs-lookup"><span data-stu-id="4a513-p123">You cannot override this policy for outbound mail you send in Office 365. In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="4a513-205">Другие способы защиты от cybercrimes в Office 365</span><span class="sxs-lookup"><span data-stu-id="4a513-205">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="4a513-206"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="4a513-206"></span></span>

<span data-ttu-id="4a513-207">Дополнительные сведения о как повышение эффективности организацию от cybercrimes как фишинга рассылки, нарушения конфиденциальности данных и других угроз, просмотрите [рекомендации по обеспечению безопасности для Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span><span class="sxs-lookup"><span data-stu-id="4a513-207">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="4a513-208">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="4a513-208">Related Topics</span></span>

[<span data-ttu-id="4a513-209">Подложные уведомления о недоставленном сообщении и EOP</span><span class="sxs-lookup"><span data-stu-id="4a513-209">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

