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
ms.openlocfilehash: 4a611ed04cc102aad4d978a379efbf46a0bd70e2
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156211"
---
# <a name="use-content-search-to-search-third-party-data-that-was-imported-to-office-365"></a><span data-ttu-id="6d3f4-105">Поиск данных третьих сторон, импортированных в Office 365, с помощью поиска контента</span><span class="sxs-lookup"><span data-stu-id="6d3f4-105">Use Content Search to search third-party data that was imported to Office 365</span></span>

<span data-ttu-id="6d3f4-106">Для поиска элементов, импортированных в почтовые ящики в Office 365 из стороннего источника данных, можно использовать [средство обнаружения электронных данных поиска контента](content-search.md) в центре обеспечения безопасности _амп_.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-106">You can use the [Content Search eDiscovery tool](content-search.md) in the Security & Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source.</span></span> <span data-ttu-id="6d3f4-107">Вы можете создать запрос для поиска всех импортированных сторонних элементов данных или создать запрос для поиска только определенных элементов данных стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-107">You can create a query to search all imported third-party data items or you can create a query to only search specific third-party data items.</span></span> <span data-ttu-id="6d3f4-108">Кроме того, вы также можете создать политику сохранения на основе запросов или удержание обнаружения электронных данных на основе запросов для сохранения сторонних данных в Office 365.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-108">Additionally, you can also create a query-based Preservation Policy or a query-based eDiscovery hold to preserve third-party data in Office 365.</span></span> 
  
<span data-ttu-id="6d3f4-109">Дополнительные сведения об импорте сторонних данных и списке типов данных сторонних производителей, которые можно импортировать в Office 365, приведены в статье [Работа с партнером для архивации сторонних данных в office 365](work-with-partner-to-archive-third-party-data.md).</span><span class="sxs-lookup"><span data-stu-id="6d3f4-109">For more information about importing third-party data and a list of the third-party data types that can be imported to Office 365, see [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md).</span></span> 
  
## <a name="creating-a-query-to-search-all-third-party-data"></a><span data-ttu-id="6d3f4-110">Создание запроса для поиска всех сторонних данных</span><span class="sxs-lookup"><span data-stu-id="6d3f4-110">Creating a query to search all third-party data</span></span>

<span data-ttu-id="6d3f4-111">Чтобы выполнить поиск (или поместиться на удержании) любого типа сторонних данных, импортированных в Office 365, можно использовать параметр `kind:externaldata` Message-value в поле ключевое слово для поиска контента или при создании удержания на основе запроса.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-111">To search (or place on hold) any type of third-party data that you've imported to Office 365, you can you can use the  `kind:externaldata` message property-value pair in the keyword box for a Content Search or when creating a query-based hold.</span></span> <span data-ttu-id="6d3f4-112">Например, чтобы найти элементы, импортированные из стороннего источника данных и содержащие слово "contoso" в свойстве subject импортированного элемента, используйте следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="6d3f4-112">For example, to search for items that were imported from any third-party data source and contain the word "contoso" in the Subject property of the imported item, you would use the following query:</span></span> 
  
```
kind:externaldata AND subject:contoso
```

<span data-ttu-id="6d3f4-113">Пример запроса к предыдущему ключевому слову включает свойство Subject.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-113">The previous keyword query example includes the subject property.</span></span> <span data-ttu-id="6d3f4-114">Список других свойств сторонних элементов данных, которые можно включить в запрос ключевых слов, приведен в разделе "Дополнительные сведения" в разделе " [Работа с партнером для архивации сторонних данных в Office 365](work-with-partner-to-archive-third-party-data.md#more-information)".</span><span class="sxs-lookup"><span data-stu-id="6d3f4-114">For a list of other properties for third-party data items that can included in a keyword query, see the "More information" section in [Work with a partner to archive third-party data in Office 365](work-with-partner-to-archive-third-party-data.md#more-information).</span></span>
  
<span data-ttu-id="6d3f4-115">При создании запросов для поиска и хранения сторонних данных можно также использовать условия для сужения результатов поиска.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-115">When creating queries to search and hold third-party data, you can also use conditions to narrow the search results.</span></span> <span data-ttu-id="6d3f4-116">Дополнительные сведения о создании поисковых запросов можно узнать в статье [запросы и условия поиска контента](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="6d3f4-116">For more information about creating Content Search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="creating-a-query-to-search-specific-types-of-third-party-data"></a><span data-ttu-id="6d3f4-117">Создание запроса для поиска определенных типов сторонних данных</span><span class="sxs-lookup"><span data-stu-id="6d3f4-117">Creating a query to search specific types of third-party data</span></span>

<span data-ttu-id="6d3f4-118">Вместо того чтобы искать все типы сторонних данных, можно создать запросы, которые ищут только сведения об указанном типе сторонних данных, используя следующую комбинацию свойства сообщения в поле ключевое слово для поиска контента:</span><span class="sxs-lookup"><span data-stu-id="6d3f4-118">Instead of searching all types of third-party data, you can create queries that only search for a specify type of third-party data by using the following message property-value pair in the keyword box for a Content Search:</span></span>
  
```
itemclass:ipm.externaldata.<third-party data type>* 
```

<span data-ttu-id="6d3f4-119">Например, чтобы искать только данные Facebook, содержащие слово "contoso" в свойстве subject, используйте следующий запрос:</span><span class="sxs-lookup"><span data-stu-id="6d3f4-119">For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the following query:</span></span>
  
```
itemclass:ipm.externaldata.Facebook* AND subject:contoso
```

<span data-ttu-id="6d3f4-120">В следующей таблице приведены типы данных третьих сторон, которые можно найти, а также значение, которое будет использоваться для свойства `itemclass:` Message для точного поиска этого типа сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-120">The following table lists the third-party data types that you can search, and the value to use for the  `itemclass:` message property to specifically search for that type of third-party data.</span></span> <span data-ttu-id="6d3f4-121">Обратите внимание, что в синтаксисе запроса регистр не учитывается.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-121">Note that the query syntax isn't case sensitive.</span></span> 
  
|<span data-ttu-id="6d3f4-122">**Сторонний тип данных**</span><span class="sxs-lookup"><span data-stu-id="6d3f4-122">**Third-party data type**</span></span>|<span data-ttu-id="6d3f4-123">**Значение `itemclass:` свойства**</span><span class="sxs-lookup"><span data-stu-id="6d3f4-123">**Value for  `itemclass:` property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d3f4-124">СТАРАЙТЕСЬ</span><span class="sxs-lookup"><span data-stu-id="6d3f4-124">AIM</span></span>  <br/> | `ipm.externaldata.AIM*` <br/> |
|<span data-ttu-id="6d3f4-125">American Idol;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-125">American Idol</span></span>  <br/> | `ipm.externaldata.AmericanIdol*` <br/> |
|<span data-ttu-id="6d3f4-126">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-126">AOL with Pivot Client</span></span>  <br/> | `ipm.externaldata.Pivot.IM` <br/> |
|<span data-ttu-id="6d3f4-127">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-127">Apple Juice</span></span>  <br/> | `ipm.externaldata.AppleJuice*` <br/> |
|<span data-ttu-id="6d3f4-128">Арес</span><span class="sxs-lookup"><span data-stu-id="6d3f4-128">Ares</span></span>  <br/> | `ipm.externaldata.Ares*` <br/> |
|<span data-ttu-id="6d3f4-129">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-129">Axs Encrypted</span></span>  <br/> | `ipm.externaldata.AxsEncrypted*` <br/> |
|<span data-ttu-id="6d3f4-130">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-130">Axs Exchange</span></span>  <br/> | `ipm.externaldata.AxsExchange*` <br/> |
|<span data-ttu-id="6d3f4-131">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-131">Axs Local Archive</span></span>  <br/> | `ipm.externaldata.AxsLocalArchive*` <br/> |
|<span data-ttu-id="6d3f4-132">Заполнитель AXS</span><span class="sxs-lookup"><span data-stu-id="6d3f4-132">Axs Placeholder</span></span>  <br/> | `ipm.externaldata.AxsPlaceHolder*` <br/> |
|<span data-ttu-id="6d3f4-133">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-133">Axs Signed</span></span>  <br/> | `ipm.externaldata.AxsSigned*` <br/> |
|<span data-ttu-id="6d3f4-134">Базаарвоице</span><span class="sxs-lookup"><span data-stu-id="6d3f4-134">Bazaarvoice</span></span>  <br/> | `ipm.externaldata.Bazaarvoice*` <br/> |
|<span data-ttu-id="6d3f4-135">Беаршаре</span><span class="sxs-lookup"><span data-stu-id="6d3f4-135">Bearshare</span></span>  <br/> | `ipm.externaldata.Bearshare*` <br/> |
|<span data-ttu-id="6d3f4-136">БитТоррент</span><span class="sxs-lookup"><span data-stu-id="6d3f4-136">BitTorrent</span></span>  <br/> | `ipm.externaldata.BitTorrent*` <br/> |
|<span data-ttu-id="6d3f4-137">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6d3f4-137">Blackberry</span></span>  <br/> | `ipm.externaldata.Blackberry*` <br/> |
|<span data-ttu-id="6d3f4-138">Журналы звонков BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6d3f4-138">BlackBerry Call Logs</span></span>  <br/> | `ipm.externaldata.BlackBerryCall*` <br/> |
|<span data-ttu-id="6d3f4-139">Служба обмена сообщениями BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6d3f4-139">BlackBerry Messenger</span></span>  <br/> | `ipm.externaldata.BlackBerryMessenger*` <br/> |
|<span data-ttu-id="6d3f4-140">ПИН-код BlackBerry</span><span class="sxs-lookup"><span data-stu-id="6d3f4-140">BlackBerry PIN</span></span>  <br/> | `ipm.externaldata.BlackBerryPIN*` <br/> |
|<span data-ttu-id="6d3f4-141">BlackBerry SMS</span><span class="sxs-lookup"><span data-stu-id="6d3f4-141">BlackBerry SMS</span></span>  <br/> | `ipm.externaldata.BlackBerrySMS*` <br/> |
|<span data-ttu-id="6d3f4-142">Bloomberg</span><span class="sxs-lookup"><span data-stu-id="6d3f4-142">Bloomberg</span></span>  <br/> | `ipm.externaldata.Bloomberg*` <br/> |
|<span data-ttu-id="6d3f4-143">Bloomberg Mail;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-143">Bloomberg Mail</span></span>  <br/> | `ipm.externaldata.BloombergMail*` <br/> |
|<span data-ttu-id="6d3f4-144">Обмен сообщениями Bloomberg</span><span class="sxs-lookup"><span data-stu-id="6d3f4-144">Bloomberg Messaging</span></span>  <br/> | `ipm.externaldata.BloombergMessaging*` <br/> |
|<span data-ttu-id="6d3f4-145">Box</span><span class="sxs-lookup"><span data-stu-id="6d3f4-145">Box</span></span>  <br/> | `ipm.externaldata.Box*` <br/> |
|<span data-ttu-id="6d3f4-146">Сервер присутствия &amp; для обмена мгновенными сообщениями Cisco</span><span class="sxs-lookup"><span data-stu-id="6d3f4-146">Cisco IM &amp; Presence Server</span></span>  <br/> | `ipm.externaldata.Jabber.IM` <br/> |
|<span data-ttu-id="6d3f4-147">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-147">Cisco Jabber</span></span>  <br/> | `ipm.externaldata.Jabber*` <br/> |
|<span data-ttu-id="6d3f4-148">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-148">CipherCloud for Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter.Post` <br/>  `ipm.externaldata.Chatter.Comment` <br/> |
|<span data-ttu-id="6d3f4-149">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-149">Direct Connect</span></span>  <br/> | `ipm.externaldata.DirectConnect*` <br/> |
|<span data-ttu-id="6d3f4-150">Facebook</span><span class="sxs-lookup"><span data-stu-id="6d3f4-150">Facebook</span></span>  <br/> | `ipm.externaldata.Facebook*` <br/> |
|<span data-ttu-id="6d3f4-151">FastTrack</span><span class="sxs-lookup"><span data-stu-id="6d3f4-151">FastTrack</span></span>  <br/> | `ipm.externaldata.FastTrack*` <br/> |
|<span data-ttu-id="6d3f4-152">Фксконнект</span><span class="sxs-lookup"><span data-stu-id="6d3f4-152">FXConnect</span></span>  <br/> | `ipm.externaldata.FXConnect.chat` <br/> |
|<span data-ttu-id="6d3f4-153">Flickr</span><span class="sxs-lookup"><span data-stu-id="6d3f4-153">Flickr</span></span>  <br/> | `ipm.externaldata.Flickr*` <br/> |
|<span data-ttu-id="6d3f4-154">Гнутелла</span><span class="sxs-lookup"><span data-stu-id="6d3f4-154">Gnutella</span></span>  <br/> | `ipm.externaldata.Gnutella*` <br/> |
|<span data-ttu-id="6d3f4-155">Google +</span><span class="sxs-lookup"><span data-stu-id="6d3f4-155">Google+</span></span>  <br/> | `ipm.externaldata.GooglePlus*` <br/> |
|<span data-ttu-id="6d3f4-156">Google говорите</span><span class="sxs-lookup"><span data-stu-id="6d3f4-156">Google Talk</span></span>  <br/> | `ipm.externaldata.GoogleTalk*` <br/> |
|<span data-ttu-id="6d3f4-157">Готомипк</span><span class="sxs-lookup"><span data-stu-id="6d3f4-157">GoToMyPC</span></span>  <br/> | `ipm.externaldata.GoToMyPC*` <br/> |
|<span data-ttu-id="6d3f4-158">Хипчат</span><span class="sxs-lookup"><span data-stu-id="6d3f4-158">HipChat</span></span>  <br/> | `ipm.externaldata.HipChat*` <br/> |
|<span data-ttu-id="6d3f4-159">Хопстер</span><span class="sxs-lookup"><span data-stu-id="6d3f4-159">Hopster</span></span>  <br/> | `ipm.externaldata.Hopster*` <br/> |
|<span data-ttu-id="6d3f4-160">Хубконнекс</span><span class="sxs-lookup"><span data-stu-id="6d3f4-160">HubConnex</span></span>  <br/> | `ipm.externaldata.HubConnex*` <br/> |
|<span data-ttu-id="6d3f4-161">Подключения IBM</span><span class="sxs-lookup"><span data-stu-id="6d3f4-161">IBM Connections</span></span>  <br/> | `ipm.externaldata.Connections*` <br/> |
|<span data-ttu-id="6d3f4-162">IBM SameTime</span><span class="sxs-lookup"><span data-stu-id="6d3f4-162">IBM SameTime</span></span>  <br/> | `ipm.externaldata.Sametime*` <br/> |
|<span data-ttu-id="6d3f4-163">Чат</span><span class="sxs-lookup"><span data-stu-id="6d3f4-163">ICE Chat</span></span>  <br/> | `ipm.externaldata.ICEChat.Chat` <br/> |
|<span data-ttu-id="6d3f4-164">Indii Messenger;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-164">Indii Messenger</span></span>  <br/> | `ipm.externaldata.Indii*` <br/> |
|<span data-ttu-id="6d3f4-165">Инстаграм</span><span class="sxs-lookup"><span data-stu-id="6d3f4-165">Instagram</span></span>  <br/> | `ipm.externaldata.Instagram*` <br/> |
|<span data-ttu-id="6d3f4-166">Instant Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-166">Instant Bloomberg</span></span>  <br/> | `ipm.externaldata.InstantBloomberg*` <br/> |
|<span data-ttu-id="6d3f4-167">Инвестедже</span><span class="sxs-lookup"><span data-stu-id="6d3f4-167">InvestEdge</span></span>  <br/> | `ipm.externaldata.InvestEdge*` <br/> |
|<span data-ttu-id="6d3f4-168">IRC</span><span class="sxs-lookup"><span data-stu-id="6d3f4-168">IRC</span></span>  <br/> | `ipm.externaldata.IRC*` <br/> |
|<span data-ttu-id="6d3f4-169">Jive</span><span class="sxs-lookup"><span data-stu-id="6d3f4-169">Jive</span></span>  <br/> | `ipm.externaldata.Jive*` <br/> |
|<span data-ttu-id="6d3f4-170">Живеапиретентион</span><span class="sxs-lookup"><span data-stu-id="6d3f4-170">JiveApiRetention</span></span>  <br/> | `ipm.externaldata.JiveApiRetention*` <br/> |
|<span data-ttu-id="6d3f4-171">ЖКСТА</span><span class="sxs-lookup"><span data-stu-id="6d3f4-171">JXTA</span></span>  <br/> | `ipm.externaldata.JXTA*` <br/> |
|<span data-ttu-id="6d3f4-172">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6d3f4-172">LinkedIn</span></span>  <br/> | `ipm.externaldata.LinkedIn*` <br/> |
|<span data-ttu-id="6d3f4-173">МФТП</span><span class="sxs-lookup"><span data-stu-id="6d3f4-173">MFTP</span></span>  <br/> | `ipm.externaldata.MFTP*` <br/> |
|<span data-ttu-id="6d3f4-174">Microsoft UC</span><span class="sxs-lookup"><span data-stu-id="6d3f4-174">Microsoft UC</span></span>  <br/> | `ipm.externaldata.MicrosoftUC*` <br/> |
|<span data-ttu-id="6d3f4-175">Выровнять по расмнению</span><span class="sxs-lookup"><span data-stu-id="6d3f4-175">Mind Align</span></span>  <br/> | `ipm.externaldata.MindAlign*` <br/> |
|<span data-ttu-id="6d3f4-176">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-176">Mobile Guard</span></span>  <br/> | `ipm.externaldata.MobileGuard*` <br/> |
|<span data-ttu-id="6d3f4-177">СЕТЬЮ</span><span class="sxs-lookup"><span data-stu-id="6d3f4-177">MSN</span></span>  <br/> | `ipm.externaldata.MSN*` <br/> |
|<span data-ttu-id="6d3f4-178">Миспаце</span><span class="sxs-lookup"><span data-stu-id="6d3f4-178">MySpace</span></span>  <br/> | `ipm.externaldata.MySpace*` <br/> |
|<span data-ttu-id="6d3f4-179">Неонетворк</span><span class="sxs-lookup"><span data-stu-id="6d3f4-179">NEONetwork</span></span>  <br/> | `ipm.externaldata.NEONetwork*` <br/> |
|<span data-ttu-id="6d3f4-180">Опеннап</span><span class="sxs-lookup"><span data-stu-id="6d3f4-180">OpenNap</span></span>  <br/> | `ipm.externaldata.OpenNap*` <br/> |
|<span data-ttu-id="6d3f4-181">Пинтерест</span><span class="sxs-lookup"><span data-stu-id="6d3f4-181">Pinterest</span></span>  <br/> | `ipm.externaldata.Pinterest*` <br/> |
|<span data-ttu-id="6d3f4-182">Сводка</span><span class="sxs-lookup"><span data-stu-id="6d3f4-182">Pivot</span></span>  <br/> | `ipm.externaldata.Pivot*` <br/> |
|<span data-ttu-id="6d3f4-183">QQ</span><span class="sxs-lookup"><span data-stu-id="6d3f4-183">QQ</span></span>  <br/> | `ipm.externaldata.QQ*` <br/> |
|<span data-ttu-id="6d3f4-184">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="6d3f4-184">Microsoft SharePoint</span></span>  <br/> | `ipm.externaldata.SharePoint*` <br/> |
|<span data-ttu-id="6d3f4-185">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-185">Salesforce Chatter</span></span>  <br/> | `ipm.externaldata.Chatter*` <br/> |
|<span data-ttu-id="6d3f4-186">Skype для бизнеса</span><span class="sxs-lookup"><span data-stu-id="6d3f4-186">Skype for Business</span></span>  <br/> | `ipm.externaldata.Skype*` <br/> |
|<span data-ttu-id="6d3f4-187">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-187">Slack Enterprise Grid</span></span>  <br/> | `ipm.externaldata.Slack.IM` <br/> |
|<span data-ttu-id="6d3f4-188">Софтесер</span><span class="sxs-lookup"><span data-stu-id="6d3f4-188">SoftEther</span></span>  <br/> | `ipm.externaldata.SoftEther*` <br/> |
|<span data-ttu-id="6d3f4-189">Скуавкер</span><span class="sxs-lookup"><span data-stu-id="6d3f4-189">Squawker</span></span>  <br/> | `ipm.externaldata.Squawker*` <br/> |
|<span data-ttu-id="6d3f4-190">Симфони</span><span class="sxs-lookup"><span data-stu-id="6d3f4-190">Symphony</span></span>  <br/> | `ipm.externaldata.Symphony*` <br/> |
|<span data-ttu-id="6d3f4-191">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-191">Thomson Reuters</span></span>  <br/> | `ipm.externaldata.Reuters*` <br/> |
| <span data-ttu-id="6d3f4-192">Thomson Reuters Eikon Messenger.</span><span class="sxs-lookup"><span data-stu-id="6d3f4-192">Thomson Reuters Eikon Messenger</span></span>  <br/> | `ipm.externaldata.ReutersEikon*` <br/> |
|<span data-ttu-id="6d3f4-193">Тор</span><span class="sxs-lookup"><span data-stu-id="6d3f4-193">Tor</span></span>  <br/> | `ipm.externaldata.Tor*` <br/> |
|<span data-ttu-id="6d3f4-194">ТТТ</span><span class="sxs-lookup"><span data-stu-id="6d3f4-194">TTT</span></span>  <br/> | `ipm.externaldata.TTT*` <br/> |
|<span data-ttu-id="6d3f4-195">Twitter</span><span class="sxs-lookup"><span data-stu-id="6d3f4-195">Twitter</span></span>  <br/> | `ipm.externaldata.Twitter*` <br/> |
|<span data-ttu-id="6d3f4-196">UBS Chat;</span><span class="sxs-lookup"><span data-stu-id="6d3f4-196">UBS Chat</span></span>  <br/> | `ipm.externaldata.UBS*` <br/> |
|<span data-ttu-id="6d3f4-197">Vimeo</span><span class="sxs-lookup"><span data-stu-id="6d3f4-197">Vimeo</span></span>  <br/> | `ipm.externaldata.Vimeo*` <br/> |
|<span data-ttu-id="6d3f4-198">Винмкс</span><span class="sxs-lookup"><span data-stu-id="6d3f4-198">WinMX</span></span>  <br/> | `ipm.externaldata.WinMX*` <br/> |
|<span data-ttu-id="6d3f4-199">Винни</span><span class="sxs-lookup"><span data-stu-id="6d3f4-199">Winny</span></span>  <br/> | `ipm.externaldata.Winny*` <br/> |
|<span data-ttu-id="6d3f4-200">Yahoo!</span><span class="sxs-lookup"><span data-stu-id="6d3f4-200">Yahoo!</span></span>  <br/> | `ipm.externaldata.Yahoo!*` <br/> |
|<span data-ttu-id="6d3f4-201">Yammer</span><span class="sxs-lookup"><span data-stu-id="6d3f4-201">Yammer</span></span>  <br/> | `ipm.externaldata.Yammer*` <br/> |
|<span data-ttu-id="6d3f4-202">Елловжаккет</span><span class="sxs-lookup"><span data-stu-id="6d3f4-202">YellowJacket</span></span>  <br/> | `ipm.externaldata.YellowJacket*` <br/> |
|<span data-ttu-id="6d3f4-203">YouTube</span><span class="sxs-lookup"><span data-stu-id="6d3f4-203">YouTube</span></span>  <br/> | `ipm.externaldata.YouTube*` <br/> |
