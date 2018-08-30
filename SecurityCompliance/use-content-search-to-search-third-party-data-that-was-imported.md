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
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="90183-105">Использование поиска контента для поиска данных сторонних производителей, которая была импортирована в Office 365</span><span class="sxs-lookup"><span data-stu-id="90183-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="90183-p102">Можно использовать [средство поиска контента обнаружения электронных данных](content-search.md) в Office 365 безопасность &amp; центре соответствия требованиям для поиска элементов, которые были импортированы из источника данных сторонних производителей для почтовых ящиков в Office 365. Можно создать запрос для поиска всех импортированных элементов данных в сторонних производителей или создать запрос для поиска только элементов конкретного данных сторонних производителей. Кроме того можно также создать политику хранения на основе запроса или обнаружения электронных данных запроса на удержание для сохранения данных сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="90183-p102">You can use the [Content Search eDiscovery tool](content-search.md) in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items. Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="90183-109">Дополнительные сведения об импорте данных сторонних производителей и список типов данных сторонних производителей, которые могут быть импортированы в Office 365 можно [данных архивации сторонних производителей в Office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="90183-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="90183-110">Создание запроса для поиска всех данных сторонних производителей</span><span class="sxs-lookup"><span data-stu-id="90183-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="90183-p103">Для поиска (или поместить на удержание) любого типа данных сторонних производителей, импортированные в Office 365, вы можете вы можно использовать `kind:externaldata` значение свойства пара сообщений в поле ключевое слово для поиска контента или при создании запроса на удержание. Например для поиска элементов, которые были импортированы из любого источника данных сторонних производителей и со словом «contoso» в свойство Subject импортированного элемента, можно использовать следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="90183-p103">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold. For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="90183-p104">Свойство subject включает в себя в предыдущем примере запроса ключевого слова. Список других свойств для данных сторонних производителей элементов, которые могут включать в запрос ключевого слова, обратитесь к разделу «Дополнительные сведения» в [данных архивации сторонних производителей в Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="90183-p104">The previous keyword query example includes the subject property. For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="90183-p105">При создании запросов для поиска и хранения данных сторонних производителей, чтобы сузить результаты поиска можно также использовать условия. Дополнительные сведения о создании запросов поиска контента видеть [запросах по ключевым словам и условия поиска для поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="90183-p105">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results. For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="90183-117">Создание запроса для поиска определенных типов данных сторонних производителей</span><span class="sxs-lookup"><span data-stu-id="90183-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="90183-118">Вместо поиск всех типов данных сторонних производителей, можно создавать запросы, что только поиск укажите тип данных сторонних производителей с помощью следующей пары значение свойства сообщения в поле ключевое слово для поиска контента:</span><span class="sxs-lookup"><span data-stu-id="90183-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="90183-119">Например для поиска только данные Facebook (en), содержащий слово «contoso» в свойстве темы, можно использовать следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="90183-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="90183-p106">В следующей таблице приведены типы данных сторонних производителей, которые можно выполнить поиск и значения будут использоваться для `itemclass:` сообщений свойство для поиска специально для этого типа данных сторонних производителей. Обратите внимание на то, что синтаксис запроса не учитывают регистр.</span><span class="sxs-lookup"><span data-stu-id="90183-p106">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data. Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="90183-122">**Тип данных сторонних производителей**</span><span class="sxs-lookup"><span data-stu-id="90183-122">**Third-party data type**</span></span>|<span data-ttu-id="90183-123">**Значение `itemclass:` свойства**</span><span class="sxs-lookup"><span data-stu-id="90183-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90183-124">AIM;</span><span class="sxs-lookup"><span data-stu-id="90183-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="90183-125">American Idol;</span><span class="sxs-lookup"><span data-stu-id="90183-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="90183-126">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="90183-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="90183-127">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="90183-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="90183-128">Ares;</span><span class="sxs-lookup"><span data-stu-id="90183-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="90183-129">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="90183-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="90183-130">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="90183-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="90183-131">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="90183-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="90183-132">Заполнитель Axs</span><span class="sxs-lookup"><span data-stu-id="90183-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="90183-133">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="90183-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="90183-134">Bazaarvoice</span><span class="sxs-lookup"><span data-stu-id="90183-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="90183-135">BearShare</span><span class="sxs-lookup"><span data-stu-id="90183-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="90183-136">Отправляемому BitTorrent</span><span class="sxs-lookup"><span data-stu-id="90183-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="90183-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="90183-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="90183-138">Журналы звонков blackBerry</span><span class="sxs-lookup"><span data-stu-id="90183-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="90183-139">BlackBerry Messenger</span><span class="sxs-lookup"><span data-stu-id="90183-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="90183-140">BlackBerry ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="90183-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="90183-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="90183-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="90183-142">Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="90183-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="90183-143">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="90183-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="90183-144">Bloomberg системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="90183-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="90183-145">Box;
</span><span class="sxs-lookup"><span data-stu-id="90183-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="90183-146">Cisco обмена мгновенными Сообщениями &amp; Server сведения о присутствии</span><span class="sxs-lookup"><span data-stu-id="90183-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="90183-147">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="90183-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="90183-148">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="90183-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="90183-149">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="90183-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="90183-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="90183-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="90183-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="90183-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="90183-152">FXConnect;</span><span class="sxs-lookup"><span data-stu-id="90183-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="90183-153">Flickr;
</span><span class="sxs-lookup"><span data-stu-id="90183-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="90183-154">Gnutella;</span><span class="sxs-lookup"><span data-stu-id="90183-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="90183-155">Google+;
</span><span class="sxs-lookup"><span data-stu-id="90183-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="90183-156">Google Talk</span><span class="sxs-lookup"><span data-stu-id="90183-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="90183-157">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="90183-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="90183-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="90183-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="90183-159">Hopster;</span><span class="sxs-lookup"><span data-stu-id="90183-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="90183-160">HubConnex</span><span class="sxs-lookup"><span data-stu-id="90183-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="90183-161">Подключения к IBM</span><span class="sxs-lookup"><span data-stu-id="90183-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="90183-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="90183-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="90183-163">ICE чата</span><span class="sxs-lookup"><span data-stu-id="90183-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="90183-164">Indii Messenger;
</span><span class="sxs-lookup"><span data-stu-id="90183-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="90183-165">Instagram;
</span><span class="sxs-lookup"><span data-stu-id="90183-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="90183-166">Instant Bloomberg;
</span><span class="sxs-lookup"><span data-stu-id="90183-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="90183-167">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="90183-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="90183-168">IRC;</span><span class="sxs-lookup"><span data-stu-id="90183-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="90183-169">Jive;
</span><span class="sxs-lookup"><span data-stu-id="90183-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="90183-170">JiveApiRetention</span><span class="sxs-lookup"><span data-stu-id="90183-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="90183-171">JXTA;</span><span class="sxs-lookup"><span data-stu-id="90183-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="90183-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="90183-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="90183-173">MFTP;</span><span class="sxs-lookup"><span data-stu-id="90183-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="90183-174">Майкрософт для объединенных Коммуникаций</span><span class="sxs-lookup"><span data-stu-id="90183-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="90183-175">Выровнять виду</span><span class="sxs-lookup"><span data-stu-id="90183-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="90183-176">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="90183-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="90183-177">MSN;</span><span class="sxs-lookup"><span data-stu-id="90183-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="90183-178">MySpace</span><span class="sxs-lookup"><span data-stu-id="90183-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="90183-179">NEONetwork;</span><span class="sxs-lookup"><span data-stu-id="90183-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="90183-180">OpenNap</span><span class="sxs-lookup"><span data-stu-id="90183-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="90183-181">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="90183-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="90183-182">Pivot;</span><span class="sxs-lookup"><span data-stu-id="90183-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="90183-183">QQ;</span><span class="sxs-lookup"><span data-stu-id="90183-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="90183-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="90183-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="90183-185">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="90183-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="90183-186">Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="90183-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="90183-187">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="90183-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="90183-188">SoftEther</span><span class="sxs-lookup"><span data-stu-id="90183-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="90183-189">
Squawker;
</span><span class="sxs-lookup"><span data-stu-id="90183-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="90183-190">Symphony;</span><span class="sxs-lookup"><span data-stu-id="90183-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="90183-191">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="90183-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="90183-192">Thomson Reuters Eikon Messenger.
</span><span class="sxs-lookup"><span data-stu-id="90183-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="90183-193">Tor;</span><span class="sxs-lookup"><span data-stu-id="90183-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="90183-194">TTT;</span><span class="sxs-lookup"><span data-stu-id="90183-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="90183-195">Твиттер</span><span class="sxs-lookup"><span data-stu-id="90183-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="90183-196">UBS Chat;
</span><span class="sxs-lookup"><span data-stu-id="90183-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="90183-197">Vimeo.</span><span class="sxs-lookup"><span data-stu-id="90183-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="90183-198">WinMX</span><span class="sxs-lookup"><span data-stu-id="90183-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="90183-199">Winny;</span><span class="sxs-lookup"><span data-stu-id="90183-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="90183-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="90183-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="90183-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="90183-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="90183-202">YellowJacket</span><span class="sxs-lookup"><span data-stu-id="90183-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="90183-203">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="90183-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
