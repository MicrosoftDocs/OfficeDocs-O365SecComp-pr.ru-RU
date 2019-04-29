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
ms.openlocfilehash: c71472b5e6d9b992196780aba55e3775823447ab
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33402907"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="b206e-105">Поиск данных третьих сторон, импортированных в Office 365, с помощью поиска контента</span><span class="sxs-lookup"><span data-stu-id="b206e-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="b206e-106">Для поиска элементов, импортированных в почтовые ящики в Office 365 из стороннего источника данных, можно использовать [средство обнаружения электронных данных поиска контента](content-search.md) в центре обеспечения безопасности _амп_.</span><span class="sxs-lookup"><span data-stu-id="b206e-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="b206e-107">Вы можете создать запрос для поиска всех импортированных сторонних элементов данных или создать запрос для поиска только определенных элементов данных стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="b206e-107">You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items.</span></span> <span data-ttu-id="b206e-108">Кроме того, вы также можете создать политику сохранения на основе запросов или удержание обнаружения электронных данных на основе запросов для сохранения сторонних данных в Office 365.</span><span class="sxs-lookup"><span data-stu-id="b206e-108">Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="b206e-109">Дополнительные сведения об импорте сторонних данных и списке типов данных сторонних производителей, которые можно импортировать в Office 365, приведены в статье [Работа с партнером для архивации сторонних данных в office 365](work-with-partner-to-archive-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="b206e-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="b206e-110">Создание запроса для поиска всех сторонних данных</span><span class="sxs-lookup"><span data-stu-id="b206e-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="b206e-111">Чтобы выполнить поиск (или поместиться на удержании) любого типа сторонних данных, импортированных в Office 365, можно использовать параметр `kind:externaldata` Message-value в поле ключевое слово для поиска контента или при создании удержания на основе запроса.</span><span class="sxs-lookup"><span data-stu-id="b206e-111">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="b206e-112">Например, чтобы найти элементы, импортированные из стороннего источника данных и содержащие слово "contoso" в свойстве subject импортированного элемента, используйте следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="b206e-112">For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="b206e-113">Пример запроса к предыдущему ключевому слову включает свойство Subject.</span><span class="sxs-lookup"><span data-stu-id="b206e-113">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="b206e-114">Список других свойств сторонних элементов данных, которые можно включить в запрос ключевых слов, приведен в разделе "Дополнительные сведения" в разделе " [Работа с партнером для архивации сторонних данных в Office 365](work-with-partner-to-archive-third-party-data.md#more-information)".</span><span class="sxs-lookup"><span data-stu-id="b206e-114">For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="b206e-115">При создании запросов для поиска и хранения сторонних данных можно также использовать условия для сужения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="b206e-115">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="b206e-116">Дополнительные сведения о создании поисковых запросов можно узнать в статье [запросы и условия поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="b206e-116">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="b206e-117">Создание запроса для поиска определенных типов сторонних данных</span><span class="sxs-lookup"><span data-stu-id="b206e-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="b206e-118">Вместо того чтобы искать все типы сторонних данных, можно создать запросы, которые ищут только сведения об указанном типе сторонних данных, используя следующую комбинацию свойства сообщения в поле ключевое слово для поиска контента:</span><span class="sxs-lookup"><span data-stu-id="b206e-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="b206e-119">Например, чтобы искать только данные Facebook, содержащие слово "contoso" в свойстве subject, используйте следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="b206e-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="b206e-120">В следующей таблице приведены типы данных третьих сторон, которые можно найти, а также значение, которое будет использоваться для свойства `itemclass:` Message для точного поиска этого типа сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="b206e-120">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="b206e-121">Обратите внимание, что в синтаксисе запроса регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="b206e-121">Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="b206e-122">**Сторонний тип данных**</span><span class="sxs-lookup"><span data-stu-id="b206e-122">**Third-party data type**</span></span>|<span data-ttu-id="b206e-123">**Значение `itemclass:` свойства**</span><span class="sxs-lookup"><span data-stu-id="b206e-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b206e-124">СТАРАЙТЕСЬ</span><span class="sxs-lookup"><span data-stu-id="b206e-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="b206e-125">American Idol;</span><span class="sxs-lookup"><span data-stu-id="b206e-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="b206e-126">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="b206e-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="b206e-127">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="b206e-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="b206e-128">Арес</span><span class="sxs-lookup"><span data-stu-id="b206e-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="b206e-129">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="b206e-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="b206e-130">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="b206e-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="b206e-131">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="b206e-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="b206e-132">ЗаПолнитель AXS</span><span class="sxs-lookup"><span data-stu-id="b206e-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="b206e-133">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="b206e-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="b206e-134">Базаарвоице</span><span class="sxs-lookup"><span data-stu-id="b206e-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="b206e-135">Беаршаре</span><span class="sxs-lookup"><span data-stu-id="b206e-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="b206e-136">БитТоррент</span><span class="sxs-lookup"><span data-stu-id="b206e-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="b206e-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="b206e-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="b206e-138">Журналы звонков BlackBerry</span><span class="sxs-lookup"><span data-stu-id="b206e-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="b206e-139">Служба обмена сообщениями BlackBerry</span><span class="sxs-lookup"><span data-stu-id="b206e-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="b206e-140">ПИН-код BlackBerry</span><span class="sxs-lookup"><span data-stu-id="b206e-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="b206e-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="b206e-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="b206e-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="b206e-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="b206e-143">Bloomberg Mail;</span><span class="sxs-lookup"><span data-stu-id="b206e-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="b206e-144">Обмен сообщениями Bloomberg</span><span class="sxs-lookup"><span data-stu-id="b206e-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="b206e-145">Box</span><span class="sxs-lookup"><span data-stu-id="b206e-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="b206e-146">Сервер присутствия &amp; для обмена МГНОВЕНными сообщениями Cisco</span><span class="sxs-lookup"><span data-stu-id="b206e-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="b206e-147">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="b206e-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="b206e-148">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="b206e-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="b206e-149">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="b206e-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="b206e-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="b206e-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="b206e-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="b206e-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="b206e-152">Фксконнект</span><span class="sxs-lookup"><span data-stu-id="b206e-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="b206e-153">Flickr</span><span class="sxs-lookup"><span data-stu-id="b206e-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="b206e-154">Гнутелла</span><span class="sxs-lookup"><span data-stu-id="b206e-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="b206e-155">Google +</span><span class="sxs-lookup"><span data-stu-id="b206e-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="b206e-156">Google говорите</span><span class="sxs-lookup"><span data-stu-id="b206e-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="b206e-157">Готомипк</span><span class="sxs-lookup"><span data-stu-id="b206e-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="b206e-158">Хипчат</span><span class="sxs-lookup"><span data-stu-id="b206e-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="b206e-159">Хопстер</span><span class="sxs-lookup"><span data-stu-id="b206e-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="b206e-160">Хубконнекс</span><span class="sxs-lookup"><span data-stu-id="b206e-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="b206e-161">Подключения IBM</span><span class="sxs-lookup"><span data-stu-id="b206e-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="b206e-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="b206e-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="b206e-163">Чат</span><span class="sxs-lookup"><span data-stu-id="b206e-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="b206e-164">Indii Messenger;</span><span class="sxs-lookup"><span data-stu-id="b206e-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="b206e-165">Инстаграм</span><span class="sxs-lookup"><span data-stu-id="b206e-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="b206e-166">Instant Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="b206e-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="b206e-167">Инвестедже</span><span class="sxs-lookup"><span data-stu-id="b206e-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="b206e-168">IRC</span><span class="sxs-lookup"><span data-stu-id="b206e-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="b206e-169">Jive</span><span class="sxs-lookup"><span data-stu-id="b206e-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="b206e-170">Живеапиретентион</span><span class="sxs-lookup"><span data-stu-id="b206e-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="b206e-171">ЖКСТА</span><span class="sxs-lookup"><span data-stu-id="b206e-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="b206e-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="b206e-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="b206e-173">МФТП</span><span class="sxs-lookup"><span data-stu-id="b206e-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="b206e-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="b206e-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="b206e-175">ВыРовнять по расМнению</span><span class="sxs-lookup"><span data-stu-id="b206e-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="b206e-176">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="b206e-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="b206e-177">СЕТЬЮ</span><span class="sxs-lookup"><span data-stu-id="b206e-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="b206e-178">Миспаце</span><span class="sxs-lookup"><span data-stu-id="b206e-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="b206e-179">Неонетворк</span><span class="sxs-lookup"><span data-stu-id="b206e-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="b206e-180">Опеннап</span><span class="sxs-lookup"><span data-stu-id="b206e-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="b206e-181">Пинтерест</span><span class="sxs-lookup"><span data-stu-id="b206e-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="b206e-182">Сводка</span><span class="sxs-lookup"><span data-stu-id="b206e-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="b206e-183">QQ</span><span class="sxs-lookup"><span data-stu-id="b206e-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="b206e-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="b206e-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="b206e-185">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="b206e-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="b206e-186">Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="b206e-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="b206e-187">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="b206e-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="b206e-188">Софтесер</span><span class="sxs-lookup"><span data-stu-id="b206e-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="b206e-189">Скуавкер</span><span class="sxs-lookup"><span data-stu-id="b206e-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="b206e-190">Симфони</span><span class="sxs-lookup"><span data-stu-id="b206e-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="b206e-191">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="b206e-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="b206e-192">Thomson Reuters Eikon Messenger.</span><span class="sxs-lookup"><span data-stu-id="b206e-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="b206e-193">Тор</span><span class="sxs-lookup"><span data-stu-id="b206e-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="b206e-194">ТТТ</span><span class="sxs-lookup"><span data-stu-id="b206e-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="b206e-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="b206e-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="b206e-196">UBS Chat;</span><span class="sxs-lookup"><span data-stu-id="b206e-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="b206e-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="b206e-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="b206e-198">Винмкс</span><span class="sxs-lookup"><span data-stu-id="b206e-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="b206e-199">Винни</span><span class="sxs-lookup"><span data-stu-id="b206e-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="b206e-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="b206e-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="b206e-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="b206e-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="b206e-202">Елловжаккет</span><span class="sxs-lookup"><span data-stu-id="b206e-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="b206e-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="b206e-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
