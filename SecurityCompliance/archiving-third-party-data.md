---
title: Архивация сторонних данных в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Администраторы могут импортировать данные сторонних производителей из платформ социальные сети, платформ мгновенного обмена сообщениями и совместной работы платформ документов к почтовым ящикам в организации Office 365. Это позволяет архивировать данные из Facebook, Twitter и источники данных в Office 365. После этого можно appply функции контроля соответствия требованиям Office 365 (например, удержания по юридическим причинам, поиск контента и политик хранения) к данным сторонних производителей.
ms.openlocfilehash: 3d51d9f5cb546b33fa636fab0ca319e4d24b1ad4
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230041"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="d8f4b-105">Архивация сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f4b-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="d8f4b-p102">Office 365 позволяет администраторам импортировать и архивация данных сторонних производителей с платформ, социальные сети, обмен мгновенными сообщениями на разных платформах и платформах документов совместной работы, к почтовым ящикам в организации Office 365. Следующие примеры источников данных сторонних производителей, которые можно импортировать в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="d8f4b-108">**Социальные** - Twitter, Facebook, LinkedIn и Yammer</span><span class="sxs-lookup"><span data-stu-id="d8f4b-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="d8f4b-109">**Обмен мгновенными сообщениями** — Yahoo Messenger, GoogleTalk и Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="d8f4b-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="d8f4b-110">**Совместная работа над документами** - поля и общего банка данных</span><span class="sxs-lookup"><span data-stu-id="d8f4b-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="d8f4b-111">**В различных отраслях** — управление отношениями с клиентами (например, Salesforce задержку) и финансирование (например, Thomson Reuters и Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="d8f4b-112">**SMS или текстовых сообщений** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="d8f4b-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="d8f4b-p103">После импорта данных сторонних производителей могут применять функции контроля соответствия требованиям Office 365 — например, политики хранения хранение для судебного разбирательства, поиск контента, в архивирование на месте, аудит и Office 365 — для этих данных. Например когда почтовый ящик располагается на хранение для судебного разбирательства, сторонних производителей данные будут сохранены. Можно выполнить поиск данных сторонних производителей с помощью поиска контента. Или можно применить архивации и политики хранения к данным сторонних производителей так же, как и для данных Майкрософт. Одним словом архивирование данных в Office 365 в сторонних производителей могут помочь организации всегда оставаться на соответствующий стандарту государственных организаций и нормативных политик.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="d8f4b-118">Ниже приведен обзор процесса и действия, необходимо использовать для импорта данных сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="d8f4b-119">Шаг 1. Поиск партнера по работе со сторонними данными</span><span class="sxs-lookup"><span data-stu-id="d8f4b-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="d8f4b-120">Шаг 2. Создание и настройка почтового ящика сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f4b-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="d8f4b-121">Шаг 3. Настройка поддержки сторонних данных для почтовых ящиков пользователей</span><span class="sxs-lookup"><span data-stu-id="d8f4b-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="d8f4b-122">Шаг 4. Предоставление сведений партнеру</span><span class="sxs-lookup"><span data-stu-id="d8f4b-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="d8f4b-123">Как импортировать данные сторонних производителей процесс работы ></span><span class="sxs-lookup"><span data-stu-id="d8f4b-123">How the third-party data import process works></span></span>

<span data-ttu-id="d8f4b-124">Ниже приведены иллюстрация и описание того, как происходит импорт сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-124">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Как происходит импорт сторонних данных](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="d8f4b-126">Клиента для работы с их партнеров вариант, чтобы настроить соединитель, который будет извлечение элементов из источника данных сторонних производителей, а затем импортировать эти элементы в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-126">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="d8f4b-p104">Partner соединитель подключается к источникам данных сторонних производителей с помощью API сторонних производителей (на основе запланированного или как настроен) и извлекает элементов из источника данных. Partner соединитель преобразует контента элемента в формат сообщения электронной почты. Описание схемы формата сообщения в разделе [Дополнительные сведения](#more-information) .</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="d8f4b-130">Partner соединитель подключается к службе Azure в Office 365 с помощью веб-служб Exchange (EWS) с помощью известных конечная точка.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-130">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="d8f4b-p105">Элементы импортируются в почтовый ящик определенного пользователя или общий почтовый ящик для сторонних данных. Элемент импортируется в почтовый ящик определенного пользователя или общий почтовый ящик для сторонних данных, исходя из следующих критериев:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="d8f4b-p106">**элементы, у которых идентификатор пользователя, который соответствует учетной записи пользователя в Office 365** — Если соединитель партнеров можно сопоставить идентификатор элемента в источнике данных сторонних производителей для конкретного пользователя, который идентификатор в Office 365, элемент копируется в папку **очищаются** в списке пользователя а. Папки восстанавливаемых элементов. Пользователи не могут получить доступ к элементов в папке удаляет. Тем не менее можно использовать средства обнаружения электронных данных в Office 365 для поиска элементов в папке удаляет.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="d8f4b-p107">б. **элементов, которые не содержат идентификатор пользователя, который соответствует учетной записи пользователя в Office 365** — Если partner соединитель нельзя сопоставить идентификатор элемента для конкретного пользователя, который ID в Office 365, элемент копируется в папку **"Входящие"** почтового ящика данных сторонних производителей. Импорт элементов в папке "Входящие" позволяет или кто-то в вашей организации, чтобы войти в почтовый ящик сторонних производителей для просмотра и управления эти элементы и просматривать, если все настройки должны быть выполнены в конфигурацию соединителя партнера.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="d8f4b-140">Шаг 1. Поиск партнера по работе со сторонними данными</span><span class="sxs-lookup"><span data-stu-id="d8f4b-140">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="d8f4b-p108">Основной компонент для архивации данных сторонних производителей в Office 365 поиск и работа с партнера корпорации Майкрософт, который специализируется в записи данных из источника данных сторонних производителей и импорт в Office 365. После импорта данных его можно архивировать и сохраняются вместе с вашей организации и других данных Майкрософт, например электронной почты из Exchange и документов из SharePoint и OneDrive для бизнеса. Партнер создает соединитель, который извлекает данные из источников данных сторонних производителей вашей организации (например, BlackBerry, Facebook, Google +, Thomson Reuters, Twitter и YouTube) и передает эти данные в API Office 365, который импортируется в почтовые ящики Exchange как элементы сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="d8f4b-144">В следующих разделах перечислены партнеров Майкрософт — и источники данных сторонних производителей, они поддерживают —, участвующие в программе для архивации данных сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-144">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="d8f4b-145">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="d8f4b-145">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="d8f4b-146">Actiance</span><span class="sxs-lookup"><span data-stu-id="d8f4b-146">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="d8f4b-147">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="d8f4b-147">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="d8f4b-148">Globanet</span><span class="sxs-lookup"><span data-stu-id="d8f4b-148">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="d8f4b-149">OpenText</span><span class="sxs-lookup"><span data-stu-id="d8f4b-149">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="d8f4b-150">Verba</span><span class="sxs-lookup"><span data-stu-id="d8f4b-150">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="d8f4b-151">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="d8f4b-151">17a-4 LLC</span></span>

<span data-ttu-id="d8f4b-152">17a-4 LLC поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-152">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="d8f4b-153">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="d8f4b-153">BlackBerry</span></span>
    
- <span data-ttu-id="d8f4b-154">потоки данных Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-154">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="d8f4b-155">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-155">Cisco Jabber</span></span>
    
- <span data-ttu-id="d8f4b-156">FactSet</span><span class="sxs-lookup"><span data-stu-id="d8f4b-156">FactSet</span></span>
    
- <span data-ttu-id="d8f4b-157">HipChat</span><span class="sxs-lookup"><span data-stu-id="d8f4b-157">HipChat</span></span>
    
- <span data-ttu-id="d8f4b-158">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="d8f4b-158">InvestEdge</span></span>
    
- <span data-ttu-id="d8f4b-159">LivePerson</span><span class="sxs-lookup"><span data-stu-id="d8f4b-159">LivePerson</span></span>
    
- <span data-ttu-id="d8f4b-160">
MessageLabs Data Streams;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-160">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="d8f4b-161">OpenText</span><span class="sxs-lookup"><span data-stu-id="d8f4b-161">OpenText</span></span>
    
- <span data-ttu-id="d8f4b-162">Oracle/ATG Click-to-Call Live Help;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-162">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="d8f4b-163">Pivot IMTRADER;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-163">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="d8f4b-164">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="d8f4b-164">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="d8f4b-165">MindAlign</span><span class="sxs-lookup"><span data-stu-id="d8f4b-165">MindAlign</span></span>
    
- <span data-ttu-id="d8f4b-166">Sitrion One (Newsgator);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-166">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="d8f4b-167">
Skype для бизнеса (Lync/OCS);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-167">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="d8f4b-168">
Skype для бизнеса Online (Lync Online);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-168">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="d8f4b-169">базы данных SQL;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-169">SQL Databases</span></span>
    
- <span data-ttu-id="d8f4b-170">
Squawker;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-170">Squawker</span></span>
    
- <span data-ttu-id="d8f4b-171">Thomson Reuters Eikon Messenger.
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-171">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="d8f4b-172">Actiance</span><span class="sxs-lookup"><span data-stu-id="d8f4b-172">Actiance</span></span>

<span data-ttu-id="d8f4b-173">[Actiance](https://www.actiance.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-173">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="d8f4b-174">AIM;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-174">AIM</span></span>
    
- <span data-ttu-id="d8f4b-175">American Idol;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-175">American Idol</span></span>
    
- <span data-ttu-id="d8f4b-176">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-176">Apple Juice</span></span>
    
- <span data-ttu-id="d8f4b-177">
AOL с клиентом Pivot;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-177">AOL with Pivot client</span></span>
    
- <span data-ttu-id="d8f4b-178">Ares;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-178">Ares</span></span>
    
- <span data-ttu-id="d8f4b-179">Bazaar Voice;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-179">Bazaar Voice</span></span>
    
- <span data-ttu-id="d8f4b-180">Bear Share;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-180">Bear Share</span></span>
    
- <span data-ttu-id="d8f4b-181">Bit Torrent;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-181">Bit Torrent</span></span>
    
- <span data-ttu-id="d8f4b-182">журналы вызовов BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-182">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-183">BlackBerry Messenger (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-183">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-184">PIN-код BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-184">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-185">BlackBerry SMS (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-185">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-186">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-186">Bloomberg Mail</span></span>
    
- <span data-ttu-id="d8f4b-187">CellTrust</span><span class="sxs-lookup"><span data-stu-id="d8f4b-187">CellTrust</span></span>
    
- <span data-ttu-id="d8f4b-188">импорт чата;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-188">Chat Import</span></span>
    
- <span data-ttu-id="d8f4b-189">политика и ведение журнала чата в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-189">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="d8f4b-190">Chatter;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-190">Chatter</span></span>
    
- <span data-ttu-id="d8f4b-191">Cisco обмена мгновенными Сообщениями &amp; Server сведения о присутствии (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-191">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="d8f4b-192">Cisco Unified Presence Server (версии 8.6.3, 8.6.4, 8.6.5);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-192">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="d8f4b-193">импорт совместной работы;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-193">Collaboration Import</span></span>
    
- <span data-ttu-id="d8f4b-194">ведение журнала совместной работы в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-194">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="d8f4b-195">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-195">Direct Connect</span></span>
    
- <span data-ttu-id="d8f4b-196">Facebook</span><span class="sxs-lookup"><span data-stu-id="d8f4b-196">Facebook</span></span>
    
- <span data-ttu-id="d8f4b-197">FactSet</span><span class="sxs-lookup"><span data-stu-id="d8f4b-197">FactSet</span></span>
    
- <span data-ttu-id="d8f4b-198">FastTrack</span><span class="sxs-lookup"><span data-stu-id="d8f4b-198">FastTrack</span></span>
    
- <span data-ttu-id="d8f4b-199">Gnutella;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-199">Gnutella</span></span>
    
- <span data-ttu-id="d8f4b-200">Google+;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-200">Google+</span></span>
    
- <span data-ttu-id="d8f4b-201">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="d8f4b-201">GoToMyPC</span></span>
    
- <span data-ttu-id="d8f4b-202">Hopster;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-202">Hopster</span></span>
    
- <span data-ttu-id="d8f4b-203">HubConnex</span><span class="sxs-lookup"><span data-stu-id="d8f4b-203">HubConnex</span></span>
    
- <span data-ttu-id="d8f4b-204">IBM Connections (версии 3.0.1, 4.0, 4.5, 4.5 CR3, 5);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-204">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="d8f4b-205">IBM Connections Chat Cloud;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-205">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="d8f4b-206">IBM Connections Social Cloud;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-206">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="d8f4b-207">IBM SameTime Advanced 8.5.2 IFR1;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-207">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="d8f4b-208">IBM SameTime Communicate 9.0;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-208">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="d8f4b-209">IBM SameTime Community (версии 8.0.2, 8.5.1 IFR2, 8.5.2 IFR1, 9.1);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-209">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="d8f4b-210">IBM SameTime Complete 9.0;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-210">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="d8f4b-211">IBM SameTime Conference 9.0;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-211">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="d8f4b-212">IBM SameTime Meeting 8.5.2 IFR1;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-212">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="d8f4b-213">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="d8f4b-213">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="d8f4b-214">импорт мгновенных сообщений;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-214">IM Import</span></span>
    
- <span data-ttu-id="d8f4b-215">политика и ведение журнала обмена мгновенными сообщениями в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-215">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="d8f4b-216">Indii Messenger;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-216">Indii Messenger</span></span>
    
- <span data-ttu-id="d8f4b-217">Instant Bloomberg;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-217">Instant Bloomberg</span></span>
    
- <span data-ttu-id="d8f4b-218">IRC;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-218">IRC</span></span>
    
- <span data-ttu-id="d8f4b-219">Jive;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-219">Jive</span></span>
    
- <span data-ttu-id="d8f4b-220">Jive 6 Real Time Logging (версии 6, 7);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-220">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="d8f4b-221">импорт Jive;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-221">Jive Import</span></span>
    
- <span data-ttu-id="d8f4b-222">JXTA;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-222">JXTA</span></span>
    
- <span data-ttu-id="d8f4b-223">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="d8f4b-223">LinkedIn</span></span>
    
- <span data-ttu-id="d8f4b-224">
Microsoft Lync (2010, 2013);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-224">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="d8f4b-225">MFTP;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-225">MFTP</span></span>
    
- <span data-ttu-id="d8f4b-226">Microsoft Lync 2013 Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-226">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="d8f4b-227">Microsoft SharePoint (2010, 2013);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-227">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="d8f4b-228">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="d8f4b-228">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="d8f4b-229">Microsoft UC (Unified Communications);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-229">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="d8f4b-230">MindAlign</span><span class="sxs-lookup"><span data-stu-id="d8f4b-230">MindAlign</span></span>
    
- <span data-ttu-id="d8f4b-231">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-231">Mobile Guard</span></span>
    
- <span data-ttu-id="d8f4b-232">MSN;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-232">MSN</span></span>
    
- <span data-ttu-id="d8f4b-233">My Space;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-233">My Space</span></span>
    
- <span data-ttu-id="d8f4b-234">NEONetwork;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-234">NEONetwork</span></span>
    
- <span data-ttu-id="d8f4b-235">Office 365 Lync Dedicated;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-235">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="d8f4b-236">групповой чат Office 365;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-236">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="d8f4b-237">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-237">Pinterest</span></span>
    
- <span data-ttu-id="d8f4b-238">Pivot;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-238">Pivot</span></span>
    
- <span data-ttu-id="d8f4b-239">QQ;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-239">QQ</span></span>
    
- <span data-ttu-id="d8f4b-240">Skype для бизнеса 2015</span><span class="sxs-lookup"><span data-stu-id="d8f4b-240">Skype for Business 2015</span></span>
    
- <span data-ttu-id="d8f4b-241">SoftEther</span><span class="sxs-lookup"><span data-stu-id="d8f4b-241">SoftEther</span></span>
    
- <span data-ttu-id="d8f4b-242">Symphony;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-242">Symphony</span></span>
    
- <span data-ttu-id="d8f4b-243">Thomson Reuters Eikon;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-243">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="d8f4b-244">Thomson Reuters Messenger;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-244">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="d8f4b-245">Tor;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-245">Tor</span></span>
    
- <span data-ttu-id="d8f4b-246">TTT;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-246">TTT</span></span>
    
- <span data-ttu-id="d8f4b-247">Твиттер</span><span class="sxs-lookup"><span data-stu-id="d8f4b-247">Twitter</span></span>
    
- <span data-ttu-id="d8f4b-248">WinMX</span><span class="sxs-lookup"><span data-stu-id="d8f4b-248">WinMX</span></span>
    
- <span data-ttu-id="d8f4b-249">Winny;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-249">Winny</span></span>
    
- <span data-ttu-id="d8f4b-250">Yahoo;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-250">Yahoo</span></span>
    
- <span data-ttu-id="d8f4b-251">Yammer</span><span class="sxs-lookup"><span data-stu-id="d8f4b-251">Yammer</span></span>
    
- <span data-ttu-id="d8f4b-252">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-252">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="d8f4b-253">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="d8f4b-253">ArchiveSocial</span></span>

<span data-ttu-id="d8f4b-254">[ArchiveSocial](https://www.archivesocial.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-254">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="d8f4b-255">Facebook</span><span class="sxs-lookup"><span data-stu-id="d8f4b-255">Facebook</span></span>
    
- <span data-ttu-id="d8f4b-256">Flickr;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-256">Flickr</span></span>
    
- <span data-ttu-id="d8f4b-257">Instagram;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-257">Instagram</span></span>
    
- <span data-ttu-id="d8f4b-258">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="d8f4b-258">LinkedIn</span></span>
    
- <span data-ttu-id="d8f4b-259">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-259">Pinterest</span></span>
    
- <span data-ttu-id="d8f4b-260">Твиттер</span><span class="sxs-lookup"><span data-stu-id="d8f4b-260">Twitter</span></span>
    
- <span data-ttu-id="d8f4b-261">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-261">YouTube</span></span>
    
- <span data-ttu-id="d8f4b-262">Vimeo.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-262">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="d8f4b-263">Globanet</span><span class="sxs-lookup"><span data-stu-id="d8f4b-263">Globanet</span></span>

<span data-ttu-id="d8f4b-264">[Globanet](https://www.globanet.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-264">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="d8f4b-265">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-265">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="d8f4b-266">журналы вызовов BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-266">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-267">BlackBerry Messenger (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-267">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-268">PIN-код BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-268">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-269">BlackBerry SMS (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-269">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="d8f4b-270">Bloomberg Chat;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-270">Bloomberg Chat</span></span>
    
- <span data-ttu-id="d8f4b-271">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-271">Bloomberg Mail</span></span>
    
- <span data-ttu-id="d8f4b-272">Box;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-272">Box</span></span>
    
- <span data-ttu-id="d8f4b-273">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-273">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="d8f4b-274">Cisco обмена мгновенными Сообщениями &amp; Server сведения о присутствии (v11.0 v10 v10.5.1 SU1 v11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-274">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="d8f4b-275">Cisco Webex групп</span><span class="sxs-lookup"><span data-stu-id="d8f4b-275">Cisco Webex Teams</span></span>

- <span data-ttu-id="d8f4b-276">Рабочая область Citrix &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="d8f4b-276">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="d8f4b-277">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="d8f4b-277">CrowdCompass</span></span>

- <span data-ttu-id="d8f4b-278">настраиваемые текстовые файлы с разделителями;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-278">Custom delimited text files</span></span>
    
- <span data-ttu-id="d8f4b-279">настраиваемые XML-файлы;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-279">Custom XML files</span></span>
    
- <span data-ttu-id="d8f4b-280">Facebook (страницы)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-280">Facebook (Pages)</span></span>
    
- <span data-ttu-id="d8f4b-281">Factset;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-281">Factset</span></span>
    
- <span data-ttu-id="d8f4b-282">FXConnect;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-282">FXConnect</span></span>
    
- <span data-ttu-id="d8f4b-283">ICE Chat или YellowJacket;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-283">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="d8f4b-284">Jive;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-284">Jive</span></span>
    
- <span data-ttu-id="d8f4b-285">Macgregor XIP;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-285">Macgregor XIP</span></span>

- <span data-ttu-id="d8f4b-286">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="d8f4b-286">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="d8f4b-287">Microsoft OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="d8f4b-287">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="d8f4b-288">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="d8f4b-288">Microsoft Teams</span></span>
       
- <span data-ttu-id="d8f4b-289">Microsoft Yammer;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-289">Microsoft Yammer</span></span>
    
- <span data-ttu-id="d8f4b-290">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-290">Mobile Guard</span></span>
    
- <span data-ttu-id="d8f4b-291">Pivot;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-291">Pivot</span></span>
    
- <span data-ttu-id="d8f4b-292">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-292">Salesforce Chatter</span></span>

- <span data-ttu-id="d8f4b-293">Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="d8f4b-293">Skype for Business Online</span></span>
    
- <span data-ttu-id="d8f4b-294">Skype для бизнеса, версии от 2007 R2 до 2016 (локальные);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-294">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="d8f4b-295">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-295">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="d8f4b-296">Symphony;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-296">Symphony</span></span>
    
- <span data-ttu-id="d8f4b-297">Thomson Reuters Eikon;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-297">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="d8f4b-298">Thomson Reuters Messenger;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-298">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="d8f4b-299">Thomson Reuters Dealings 3000 или FX Trading;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-299">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="d8f4b-300">Твиттер</span><span class="sxs-lookup"><span data-stu-id="d8f4b-300">Twitter</span></span>
    
- <span data-ttu-id="d8f4b-301">UBS Chat;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-301">UBS Chat</span></span>
    
- <span data-ttu-id="d8f4b-302">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-302">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="d8f4b-303">OpenText</span><span class="sxs-lookup"><span data-stu-id="d8f4b-303">OpenText</span></span>

<span data-ttu-id="d8f4b-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-304">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="d8f4b-305">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-305">Axs Encrypted</span></span>
    
- <span data-ttu-id="d8f4b-306">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-306">Axs Exchange</span></span>
    
- <span data-ttu-id="d8f4b-307">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-307">Axs Local Archive</span></span>
    
- <span data-ttu-id="d8f4b-308">Axs PlaceHolder;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-308">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="d8f4b-309">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-309">Axs Signed</span></span>
    
- <span data-ttu-id="d8f4b-310">Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-310">Bloomberg</span></span>
    
- <span data-ttu-id="d8f4b-311">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-311">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="d8f4b-312">Verba</span><span class="sxs-lookup"><span data-stu-id="d8f4b-312">Verba</span></span>

<span data-ttu-id="d8f4b-313">[Verba](https://www.verba.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-313">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="d8f4b-314">Avaya Aura Video;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-314">Avaya Aura Video</span></span>
    
- <span data-ttu-id="d8f4b-315">Avaya Aura Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-315">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="d8f4b-316">Avtec Radio;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-316">Avtec Radio</span></span>
    
- <span data-ttu-id="d8f4b-317">Bosch/Telex Radio;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-317">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="d8f4b-318">BroadSoft Video;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-318">BroadSoft Video</span></span>
    
- <span data-ttu-id="d8f4b-319">BroadSoft Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-319">BroadSoft Voice</span></span>
    
- <span data-ttu-id="d8f4b-320">Centile Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-320">Centile Voice</span></span>
    
- <span data-ttu-id="d8f4b-321">Cisco Jabber IM;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-321">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="d8f4b-322">Cisco UC Video;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-322">Cisco UC Video</span></span>
    
- <span data-ttu-id="d8f4b-323">Cisco UC Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-323">Cisco UC Voice</span></span>
    
- <span data-ttu-id="d8f4b-324">Cisco UCCX/UCCE видео</span><span class="sxs-lookup"><span data-stu-id="d8f4b-324">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="d8f4b-325">Cisco UCCX/UCCE голосовой связи</span><span class="sxs-lookup"><span data-stu-id="d8f4b-325">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="d8f4b-326">ESChat Radio;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-326">ESChat Radio</span></span>
    
- <span data-ttu-id="d8f4b-327">Geoman Contact Expert;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-327">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="d8f4b-328">IP Trade Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-328">IP Trade Voice</span></span>
    
- <span data-ttu-id="d8f4b-329">Luware LUCS Contact Center;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-329">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="d8f4b-330">Microsoft UC (Unified Communications);</span><span class="sxs-lookup"><span data-stu-id="d8f4b-330">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="d8f4b-331">Mitel MiContact Center для Lync (prairieFyre);
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-331">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="d8f4b-332">Oracle / Acme Packet Session Border Controller Video;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-332">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="d8f4b-333">Oracle / Acme Packet Session Border Controller Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-333">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="d8f4b-334">Singtel Mobile Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-334">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="d8f4b-335">SIPREC Video;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-335">SIPREC Video</span></span>
    
-  <span data-ttu-id="d8f4b-336">SIPREC Voice;</span><span class="sxs-lookup"><span data-stu-id="d8f4b-336">SIPREC Voice</span></span> 
    
- <span data-ttu-id="d8f4b-337">Skype для бизнеса / Lync IM;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-337">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="d8f4b-338">Skype для бизнеса / Lync Video;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-338">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="d8f4b-339">Skype для бизнеса / Lync Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-339">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="d8f4b-340">Speakerbus Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-340">Speakerbus Voice</span></span>
    
- <span data-ttu-id="d8f4b-341">Standard SIP/H.323 Video;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-341">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="d8f4b-342">Standard SIP/H.323 Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-342">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="d8f4b-343">Truphone Voice;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-343">Truphone Voice</span></span>
    
- <span data-ttu-id="d8f4b-344">TwistedPair Radio;
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-344">TwistedPair Radio</span></span>
    
- <span data-ttu-id="d8f4b-345">рабочий стол Windows.
</span><span class="sxs-lookup"><span data-stu-id="d8f4b-345">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="d8f4b-346">Шаг 2. Создание и настройка почтового ящика сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f4b-346">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="d8f4b-p109">Далее приведены шаги по созданию и настройке почтового ящика данных сторонних производителей для импорта данных в Office 365. В предыдущем описываются элементы импортируются этого почтового ящика, если partner соединитель нельзя сопоставить идентификатор элемента для учетной записи пользователя в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="d8f4b-349">**Выполнить эти задачи в центре администрирования Office 365**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-349">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="d8f4b-p110">Создание учетной записи пользователя в Office 365 и назначьте его лицензии Exchange Online (план 2); Просмотрите [Добавить пользователей в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Для помещения почтового ящика на хранение для судебного разбирательства или включение архивного почтового ящика, который имеет квота хранилища неограниченное число требуется лицензия (план 2).</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="d8f4b-352">Добавьте учетную запись пользователя для почтового ящика данных сторонних производителей в роль **администратора Exchange** администратора в Office 365; в разделе [Назначение ролей администратора в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="d8f4b-352">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="d8f4b-p111">Запишите данные этой учетной записи. Их необходимо предоставить партнеру, как описано в шаге 4.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="d8f4b-355">**Выполнить эти задачи в центре администрирования Exchange**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-355">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="d8f4b-p112">Скрыть почтовый ящик сторонних производителей данные из адресной книги и другие списки адресов в организации; в разделе [Управление почтовые ящики пользователей](https://go.microsoft.com/fwlink/p/?LinkId=616058). Кроме того можно выполнить следующую команду PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="d8f4b-358">Назначьте разрешения **FullAccess** к почтовому ящику данных сторонних производителей, чтобы администраторы или контролеры можно открыть почтовый ящик данных сторонних производителей в клиентском Outlook; [Управление разрешениями для получателей](https://go.microsoft.com/fwlink/p/?LinkId=692104)см.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-358">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="d8f4b-359">Включите следующие связанные с соответствием требованиям Office 365 функции для почтового ящика сторонних производителей данных:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-359">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="d8f4b-p113">Включение архивного почтового ящика; просмотреть [Enable архивных почтовых ящиков в Office 365 безопасность &amp; центре соответствия требованиям](enable-archive-mailboxes.md) и [Включить неограниченном архивировании в Office 365](enable-unlimited-archiving.md). Это позволит освободить дисковое пространство в основной почтовый ящик, настраивая политики архивирования, который перемещает элементы данных сторонних производителей в архивный почтовый ящик. Это предоставит без ограничений хранилища для данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="d8f4b-p114">Помещение почтового ящика данных сторонних производителей на хранение для судебного разбирательства. Также можно применить политику хранения Office 365 безопасности Office 365 &amp; центре соответствия требованиям. Размещение этого почтового ящика на удержание хранения данных сторонних элементов (неограниченное время или в течение указанного периода времени) и предотвратить очищаются из почтового ящика. Отображается одно из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="d8f4b-367">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="d8f4b-367">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="d8f4b-368">Общие сведения о политиках хранения в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f4b-368">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="d8f4b-p115">Включение почтового ящика ведения журнала аудита для владельца, делегат и администрирования доступ к почтовому ящику данных сторонних производителей; в разделе [Включить аудит в Office 365 почтового ящика](enable-mailbox-auditing.md). Это позволит аудита все операции, выполненные любым пользователем, обладающим доступом к почтовому ящику данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="d8f4b-371">Шаг 3. Настройка поддержки сторонних данных для почтовых ящиков пользователей</span><span class="sxs-lookup"><span data-stu-id="d8f4b-371">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="d8f4b-p116">Следующим шагом является Настройка почтовых ящиков пользователей для поддержки данных сторонних производителей. Выполните эти задачи с помощью центра администрирования Exchange или с помощью соответствующего командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="d8f4b-374">Включение архивного почтового ящика для каждого пользователя; просмотреть [Enable архивных почтовых ящиков в Office 365 безопасность &amp; центре соответствия требованиям](enable-archive-mailboxes.md) и [Включить неограниченном архивировании в Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="d8f4b-374">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="d8f4b-375">Помещение почтовых ящиков пользователей на хранение для судебного разбирательства или применить политику хранения Office 365; отображается одно из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-375">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="d8f4b-376">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="d8f4b-376">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="d8f4b-377">Общие сведения о политиках хранения в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f4b-377">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="d8f4b-378">Как отмечалось ранее, при помещении почтовых ящиков на хранение можно указать длительность хранения элементов из источника сторонних данных или выбрать бессрочное хранение.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-378">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="d8f4b-379">Шаг 4. Предоставление сведений партнеру</span><span class="sxs-lookup"><span data-stu-id="d8f4b-379">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="d8f4b-380">Последний шаг — предоставить партнеру указанные ниже сведения, чтобы он смог настроить соединитель для подключения к организации Office 365 и импорта данных в почтовые ящики пользователей и почтовый ящик сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-380">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="d8f4b-381">Конечная точка, используемый для подключения к службе Azure в Office 365:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-381">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="d8f4b-p117">Знак в учетных данных (Office 365 идентификатор пользователя и пароль) для почтового ящика данных сторонних производителей, созданный на шаге 2. Эти учетные данные необходимы, чтобы соединитель партнеров можно получить доступ к и импорт элементов для почтовых ящиков пользователей и почтовых ящиков данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
    

  
## <a name="more-information"></a><span data-ttu-id="d8f4b-384">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="d8f4b-384">More information</span></span>

- <span data-ttu-id="d8f4b-p118">В предыдущем описываются элементы из данных сторонних производителей, которые источники импортируются в почтовые ящики Exchange как сообщения электронной почты. Соединитель партнеров импортирует элемента, с помощью схемы, необходимые для Office 365 API. В следующей таблице представлены свойства сообщения элемента из источника данных сторонних производителей после импорта в почтовый ящик Exchange, как сообщения электронной почты. В таблице также указывается, если свойство сообщения является обязательным. Обязательные свойства должны быть заполнены. Если элемент отсутствует обязательное свойство, он не будет импортирован Office 365. Процесс импорта возвращает сообщение об ошибке, объясняющее почему элемента не были импортированы, а какие свойства отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p118">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="d8f4b-392">**Свойство сообщения**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-392">**Message property**</span></span>|<span data-ttu-id="d8f4b-393">**Обязательный?**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-393">**Mandatory?**</span></span>|<span data-ttu-id="d8f4b-394">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-394">**Description**</span></span>|<span data-ttu-id="d8f4b-395">**Пример значения**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-395">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="d8f4b-396">**FROM**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-396">**FROM**</span></span> <br/> |<span data-ttu-id="d8f4b-397">Да</span><span class="sxs-lookup"><span data-stu-id="d8f4b-397">Yes</span></span>  <br/> |<span data-ttu-id="d8f4b-p119">Пользователь, который изначально создать или отправить элемента в источнике данных сторонних производителей. Partner соединитель пытается сопоставить идентификатор пользователя из исходного элемента (например, маркер Twitter) для учетной записи пользователя в Office 365 для всех участников (пользователей в полях FROM и TO). Копия сообщения будут импортированы в почтовый ящик все остальные. Если ни один из участников из элемента может быть сопоставлен учетной записи пользователя в Office 365, элемент будет импортирован в почтовый ящик архивации сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p119">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="d8f4b-p120">Участник, который идентифицируется как отправителя элемента должны иметь активного хранилища почтовых ящиков в организации Office 365, импортируемый элемент в. Если отправитель не имеет активных почтовых ящиков, возвращается следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p120">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="d8f4b-404">**TO**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-404">**TO**</span></span> <br/> |<span data-ttu-id="d8f4b-405">Да</span><span class="sxs-lookup"><span data-stu-id="d8f4b-405">Yes</span></span>  <br/> |<span data-ttu-id="d8f4b-406">Пользователь, получивший элемент, если это применимо к элементу в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-406">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="d8f4b-407">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-407">**SUBJECT**</span></span> <br/> |<span data-ttu-id="d8f4b-408">Нет</span><span class="sxs-lookup"><span data-stu-id="d8f4b-408">No</span></span>  <br/> |<span data-ttu-id="d8f4b-409">Тема исходного элемента.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-409">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="d8f4b-410">**ДАТА**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-410">**DATE**</span></span> <br/> |<span data-ttu-id="d8f4b-411">Да</span><span class="sxs-lookup"><span data-stu-id="d8f4b-411">Yes</span></span>  <br/> |<span data-ttu-id="d8f4b-412">Дата создания или публикации элемента в источнике данных клиента, например дата отправки сообщения в Твиттере.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-412">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="d8f4b-413">**BODY**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-413">**BODY**</span></span> <br/> |<span data-ttu-id="d8f4b-414">Нет</span><span class="sxs-lookup"><span data-stu-id="d8f4b-414">No</span></span>  <br/> |<span data-ttu-id="d8f4b-p121">Содержимое сообщения или post. Для некоторых источников данных содержимое этого свойства может быть таким же, как содержимое для свойства **ТЕМЫ** . Во время импорта partner соединитель будет пытаться Ведение корректном из источника контента можно. Если это возможно файлов, рисунков или другого контента из текста элемента источника включен в это свойство. В противном случае контент из исходного элемента включен в свойстве **ВЛОЖЕНИЯ** . Содержимое этого свойства будет зависят от соединителя партнеров и возможность платформы источника.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p121">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="d8f4b-421">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-421">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="d8f4b-422">Нет</span><span class="sxs-lookup"><span data-stu-id="d8f4b-422">No</span></span>  <br/> |<span data-ttu-id="d8f4b-p122">Если элемент в источнике данных (например, tweet в Twitter или сеанс обмена мгновенными сообщениями) имеет вложенный файл или включить изображения, партнера подключение будет первая попытка для включения вложений в свойство **BODY** . Если, который невозможно, то он добавляется в ** ВЛОЖЕНИЯ ** свойство. Другие вложения примеры мне нравится в Facebook, метаданные из источника контента и ответа на сообщение или post.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p122">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the ** ATTACHMENT ** property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="d8f4b-426">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="d8f4b-426">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="d8f4b-427">Да</span><span class="sxs-lookup"><span data-stu-id="d8f4b-427">Yes</span></span>  <br/> | <span data-ttu-id="d8f4b-p123">Это свойство Многозначный, которое созданы и заполнены соединителем партнера. Формат этого свойства — это `IPM.NOTE.Source.Event`. (Это свойство должен начинаться с `IPM.NOTE`; в этом формате похожего для `IPM.NOTE.X` класс сообщения.) Это свойство содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p123">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="d8f4b-431">`Source`— Определяет источник данных сторонних производителей; Например Twitter Facebook и BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-431">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="d8f4b-p124">`Event`— Определяет тип действия, выполняемого в источнике данных сторонних производителей, на котором элементов; Например tweet в Twitter или сообщение в сети Facebook. События относятся к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p124">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="d8f4b-p125">Один это свойство предназначено для фильтрации определенных элементов на основе источника данных, где произошла элемента или на основе типа события. Например поиска обнаружения электронных данных можно создать запрос поиска, чтобы найти все tweets, разнесенных по определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p125">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="d8f4b-p126">После успешного импорта элементов для почтовых ящиков в Office 365 уникальный идентификатор возвращается вызывающему как часть HTTP-ответа. Этот идентификатор — вызов `x-IngestionCorrelationID`— можно использовать для последующих в целях устранения неполадок с партнерами для отслеживания начала до конца элементов. Рекомендуется, что партнеры эти сведения и войдите соответствующим образом по завершении своей работы. Ниже приведен пример из HTTP-ответа, отражающая этот идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p126">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="d8f4b-p127">Можно использовать средство поиска контента в Office 365 безопасность &amp; центре соответствия требованиям для поиска элементов, которые были импортированы из источника данных сторонних производителей для почтовых ящиков в Office 365. Для поиска специально для этих импортированных элементов, можно использовать следующие значения свойства пары сообщение в поле ключевое слово для поиска контента. .</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p127">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="d8f4b-p128">**`kind:externaldata`**-Используется Эта пара значение свойства для поиска всех типов данных сторонних производителей. Например, для поиска элементов, которые были импортированы из источника данных сторонних производителей и содержится слово «contoso» в свойстве тема импортированного элемента, используется ключевое слово запроса `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p128">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="d8f4b-p129">**`itemclass:ipm.externaldata.<third-party data type>`**-Используйте это значение свойства пары только поиска укажите тип данных сторонних производителей. Например, для поиска только данные Facebook (en), содержащий слово «contoso» в свойстве темы, используется запроса ключевого слова `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="d8f4b-p129">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="d8f4b-447">Полный список значений, используемых для типов данных сторонних производителей для `itemclass` свойства, видеть [Используйте поиска контента для поиска данных сторонних производителей, которая была импортирована в Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="d8f4b-447">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="d8f4b-448">Дополнительные сведения об использовании средства "Поиск контента" и создании поисковых запросов по ключевым словам см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="d8f4b-448">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="d8f4b-449">Поиск контента в Office 365</span><span class="sxs-lookup"><span data-stu-id="d8f4b-449">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="d8f4b-450">Запросы ключевых слов и условия поиска контента</span><span class="sxs-lookup"><span data-stu-id="d8f4b-450">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
