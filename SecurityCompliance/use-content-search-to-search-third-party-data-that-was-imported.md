---
title: Поиск данных третьих сторон, импортированных в Office 365, с помощью поиска контента
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/27/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: ec2677ff-c4d7-4363-a9e7-22c80e015688
description: Воспользуйтесь средством поиска обнаружения электронных данных поиска контента для поиска элементов, импортированных в почтовые ящики в Office 365, из стороннего источника данных. Можно создать запрос для поиска всех импортированных элементов или создать запрос для поиска определенных типов данных третьих сторон. В этой статье перечислены значения, которые можно использовать в запросе с ключевыми словами для поиска в сторонних типах данных, которые можно импортировать в Office 365.
ms.openlocfilehash: f1ab3cfc8dd866aa0d70014b22a301de2a65f3c5
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296042"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="ccc88-105">Поиск данных третьих сторон, импортированных в Office 365, с помощью поиска контента</span><span class="sxs-lookup"><span data-stu-id="ccc88-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="ccc88-p102">[Средство обнаружения электронных данных поиска контента](content-search.md) в центре безопасности &amp; и соответствия требованиям Office 365 используется для поиска элементов, импортированных в почтовые ящики в Office 365 из стороннего источника данных. Вы можете создать запрос для поиска всех импортированных сторонних элементов данных или создать запрос для поиска только определенных элементов данных стороннего производителя. Кроме того, вы также можете создать политику сохранения на основе запросов или удержание обнаружения электронных данных на основе запросов для сохранения сторонних данных в Office 365.</span><span class="sxs-lookup"><span data-stu-id="ccc88-p102">You can use the [Content Search eDiscovery tool](content-search.md) in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items. Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="ccc88-109">Дополнительные сведения об импорте сторонних данных и списке типов данных сторонних производителей, которые можно импортировать в Office 365, приведены в разделе Архивация сторонних [данных в office 365](archiving-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="ccc88-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Archiving third-party data in Office 365](archiving-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="ccc88-110">Создание запроса для поиска всех сторонних данных</span><span class="sxs-lookup"><span data-stu-id="ccc88-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="ccc88-p103">Чтобы выполнить поиск (или поместиться на удержании) любого типа сторонних данных, импортированных в Office 365, можно использовать параметр `kind:externaldata` Message-value в поле ключевое слово для поиска контента или при создании удержания на основе запроса. Например, чтобы найти элементы, импортированные из стороннего источника данных и содержащие слово "contoso" в свойстве subject импортированного элемента, используйте следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="ccc88-p103">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold. For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="ccc88-p104">Пример запроса к предыдущему ключевому слову включает свойство Subject. Список других свойств сторонних элементов данных, которые можно включить в запрос ключевых слов, можно найти в разделе "Дополнительные сведения" [архивации сторонних данных в Office 365](archiving-third-party-data.md#more-information).</span><span class="sxs-lookup"><span data-stu-id="ccc88-p104">The previous keyword query example includes the subject property. For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Archiving third-party data in Office 365](archiving-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="ccc88-p105">При создании запросов для поиска и хранения сторонних данных можно также использовать условия для сужения результатов поиска. Дополнительные сведения о создании поисковых запросов можно узнать в статье [запросы и условия поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="ccc88-p105">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results. For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="ccc88-117">Создание запроса для поиска определенных типов сторонних данных</span><span class="sxs-lookup"><span data-stu-id="ccc88-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="ccc88-118">Вместо того чтобы искать все типы сторонних данных, можно создать запросы, которые ищут только сведения об указанном типе сторонних данных, используя следующую комбинацию свойства сообщения в поле ключевое слово для поиска контента:</span><span class="sxs-lookup"><span data-stu-id="ccc88-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="ccc88-119">Например, чтобы искать только данные Facebook, содержащие слово "contoso" в свойстве subject, используйте следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="ccc88-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="ccc88-p106">В следующей таблице приведены типы данных третьих сторон, которые можно найти, а также значение, которое будет использоваться для свойства `itemclass:` Message для точного поиска этого типа сторонних данных. Обратите внимание, что в синтаксисе запроса регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="ccc88-p106">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data. Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="ccc88-122">**Сторонний тип данных**</span><span class="sxs-lookup"><span data-stu-id="ccc88-122">**Third-party data type**</span></span>|<span data-ttu-id="ccc88-123">**Значение `itemclass:` свойства**</span><span class="sxs-lookup"><span data-stu-id="ccc88-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ccc88-124">AIM;</span><span class="sxs-lookup"><span data-stu-id="ccc88-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="ccc88-125">American Idol;</span><span class="sxs-lookup"><span data-stu-id="ccc88-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="ccc88-126">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="ccc88-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="ccc88-127">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="ccc88-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="ccc88-128">Ares;</span><span class="sxs-lookup"><span data-stu-id="ccc88-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="ccc88-129">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="ccc88-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="ccc88-130">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="ccc88-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="ccc88-131">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="ccc88-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="ccc88-132">ЗаПолнитель AXS</span><span class="sxs-lookup"><span data-stu-id="ccc88-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="ccc88-133">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="ccc88-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="ccc88-134">Базаарвоице</span><span class="sxs-lookup"><span data-stu-id="ccc88-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="ccc88-135">Беаршаре</span><span class="sxs-lookup"><span data-stu-id="ccc88-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="ccc88-136">БитТоррент</span><span class="sxs-lookup"><span data-stu-id="ccc88-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="ccc88-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ccc88-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="ccc88-138">Журналы звонков BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ccc88-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="ccc88-139">Служба обмена сообщениями BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ccc88-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="ccc88-140">ПИН-код BlackBerry</span><span class="sxs-lookup"><span data-stu-id="ccc88-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="ccc88-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="ccc88-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="ccc88-142">Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="ccc88-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="ccc88-143">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="ccc88-144">Обмен сообщениями Bloomberg</span><span class="sxs-lookup"><span data-stu-id="ccc88-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="ccc88-145">Box</span><span class="sxs-lookup"><span data-stu-id="ccc88-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="ccc88-146">Сервер присутствия &amp; для обмена МГНОВЕНными сообщениями Cisco</span><span class="sxs-lookup"><span data-stu-id="ccc88-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="ccc88-147">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="ccc88-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="ccc88-148">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="ccc88-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="ccc88-149">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="ccc88-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="ccc88-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="ccc88-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="ccc88-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="ccc88-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="ccc88-152">FXConnect;</span><span class="sxs-lookup"><span data-stu-id="ccc88-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="ccc88-153">Flickr;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="ccc88-154">Gnutella;</span><span class="sxs-lookup"><span data-stu-id="ccc88-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="ccc88-155">Google+;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="ccc88-156">Google говорите</span><span class="sxs-lookup"><span data-stu-id="ccc88-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="ccc88-157">Готомипк</span><span class="sxs-lookup"><span data-stu-id="ccc88-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="ccc88-158">Хипчат</span><span class="sxs-lookup"><span data-stu-id="ccc88-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="ccc88-159">Hopster;</span><span class="sxs-lookup"><span data-stu-id="ccc88-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="ccc88-160">Хубконнекс</span><span class="sxs-lookup"><span data-stu-id="ccc88-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="ccc88-161">Подключения IBM</span><span class="sxs-lookup"><span data-stu-id="ccc88-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="ccc88-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="ccc88-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="ccc88-163">Чат</span><span class="sxs-lookup"><span data-stu-id="ccc88-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="ccc88-164">Indii Messenger;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="ccc88-165">Instagram;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="ccc88-166">Instant Bloomberg;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="ccc88-167">Инвестедже</span><span class="sxs-lookup"><span data-stu-id="ccc88-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="ccc88-168">IRC;</span><span class="sxs-lookup"><span data-stu-id="ccc88-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="ccc88-169">Jive;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="ccc88-170">Живеапиретентион</span><span class="sxs-lookup"><span data-stu-id="ccc88-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="ccc88-171">JXTA;</span><span class="sxs-lookup"><span data-stu-id="ccc88-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="ccc88-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="ccc88-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="ccc88-173">MFTP;</span><span class="sxs-lookup"><span data-stu-id="ccc88-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="ccc88-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="ccc88-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="ccc88-175">ВыРовнять по расМнению</span><span class="sxs-lookup"><span data-stu-id="ccc88-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="ccc88-176">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="ccc88-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="ccc88-177">MSN;</span><span class="sxs-lookup"><span data-stu-id="ccc88-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="ccc88-178">Миспаце</span><span class="sxs-lookup"><span data-stu-id="ccc88-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="ccc88-179">NEONetwork;</span><span class="sxs-lookup"><span data-stu-id="ccc88-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="ccc88-180">Опеннап</span><span class="sxs-lookup"><span data-stu-id="ccc88-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="ccc88-181">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="ccc88-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="ccc88-182">Pivot;</span><span class="sxs-lookup"><span data-stu-id="ccc88-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="ccc88-183">QQ;</span><span class="sxs-lookup"><span data-stu-id="ccc88-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="ccc88-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="ccc88-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="ccc88-185">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="ccc88-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="ccc88-186">Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="ccc88-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="ccc88-187">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="ccc88-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="ccc88-188">Софтесер</span><span class="sxs-lookup"><span data-stu-id="ccc88-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="ccc88-189">
Squawker;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="ccc88-190">Symphony;</span><span class="sxs-lookup"><span data-stu-id="ccc88-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="ccc88-191">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="ccc88-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="ccc88-192">Thomson Reuters Eikon Messenger.
</span><span class="sxs-lookup"><span data-stu-id="ccc88-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="ccc88-193">Tor;</span><span class="sxs-lookup"><span data-stu-id="ccc88-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="ccc88-194">TTT;</span><span class="sxs-lookup"><span data-stu-id="ccc88-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="ccc88-195">Твиттер</span><span class="sxs-lookup"><span data-stu-id="ccc88-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="ccc88-196">UBS Chat;
</span><span class="sxs-lookup"><span data-stu-id="ccc88-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="ccc88-197">Vimeo.</span><span class="sxs-lookup"><span data-stu-id="ccc88-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="ccc88-198">Винмкс</span><span class="sxs-lookup"><span data-stu-id="ccc88-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="ccc88-199">Winny;</span><span class="sxs-lookup"><span data-stu-id="ccc88-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="ccc88-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="ccc88-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="ccc88-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="ccc88-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="ccc88-202">Елловжаккет</span><span class="sxs-lookup"><span data-stu-id="ccc88-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="ccc88-203">Своему</span><span class="sxs-lookup"><span data-stu-id="ccc88-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
