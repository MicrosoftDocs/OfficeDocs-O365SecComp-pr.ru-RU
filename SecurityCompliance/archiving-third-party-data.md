---
title: Архивация сторонних данных в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Администраторы могут импортировать сторонние данные с платформ социальных сетей, платформы обмена мгновенными сообщениями и платформы совместной работы с документами в почтовые ящики в организации Office 365. Это позволяет архивировать данные из Facebook, Twitter и источников данных в Office 365. После этого вы можете апппли возможности соответствия требованиям Office 365 (например, "юридические удержания", "поиск контента" и "политики хранения") с данными сторонних производителей.
ms.openlocfilehash: 0f9f8b5a4ce5b4359430a3b15acc7bf16b2f0290
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296682"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="5d324-105">Архивация сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="5d324-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="5d324-p102">Office 365 позволяет администраторам импортировать и архивировать сторонние данные с платформ социальных сетей, платформ обмена мгновенными сообщениями и платформ совместной работы с документами в почтовые ящики в организации Office 365. Примеры сторонних источников данных, которые можно импортировать в Office 365, включают следующие:</span><span class="sxs-lookup"><span data-stu-id="5d324-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="5d324-108">**Социальные** сети — Twitter, Facebook, Yammer и LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5d324-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="5d324-109">\*\*\*\* Обмен мгновенными сообщениями Yahoo Messenger, Гуглеталк и Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="5d324-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="5d324-110">**Совместная работа с документами** и Dropbox</span><span class="sxs-lookup"><span data-stu-id="5d324-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="5d324-111">**Вертикальные отрасли** — Управление отношениями с клиентами (например, Salesforce chatter;) и финансовые функции (например, Thomson Reuters и Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="5d324-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="5d324-112">**SMS/Text Messaging** -BlackBerry</span><span class="sxs-lookup"><span data-stu-id="5d324-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="5d324-p103">После импорта сторонних данных можно применить функции соответствия требованиям Office 365, такие как хранение для судебного разбирательства, поиск контента, Архивация на месте, аудит и политики хранения Office 365, в эти данные. Например, если почтовый ящик размещается на хранение для судебного разбирательства, данные сторонних поставщиков будут сохранены. С помощью поиска контента можно выполнять поиск по сторонним данным. Кроме того, вы можете применять политики архивации и хранения к сторонним данным, как и к данным Майкрософт. Коротко говоря, архивация сторонних данных в Office 365 поможет организациям соответствовать стандартам государственных и законодательных политик.</span><span class="sxs-lookup"><span data-stu-id="5d324-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="5d324-118">Ниже приводится обзор процесса и действия, необходимые для импорта сторонних данных в Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="5d324-119">Шаг 1. Поиск партнера по работе со сторонними данными</span><span class="sxs-lookup"><span data-stu-id="5d324-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="5d324-120">Шаг 2. Создание и настройка почтового ящика сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="5d324-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="5d324-121">Шаг 3. Настройка поддержки сторонних данных для почтовых ящиков пользователей</span><span class="sxs-lookup"><span data-stu-id="5d324-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="5d324-122">Шаг 4. Предоставление сведений партнеру</span><span class="sxs-lookup"><span data-stu-id="5d324-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="5d324-123">Шаг 5: заРегистрируйте сторонний соединитель данных в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d324-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="5d324-124">Как Воркс_гт_ процесс импорта данных стороннего производителя</span><span class="sxs-lookup"><span data-stu-id="5d324-124">How the third-party data import process works></span></span>

<span data-ttu-id="5d324-125">Ниже приведены иллюстрация и описание того, как происходит импорт сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="5d324-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Как происходит импорт сторонних данных](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="5d324-127">Клиент работает с партнером по выбору, чтобы настроить соединитель, который будет извлекать элементы из стороннего источника данных, а затем импортировать эти элементы в Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="5d324-p104">Соединитель партнера подключается к сторонним источникам данных с помощью стороннего API (на основе запланированной или настроенной конфигурации) и извлекает элементы из источника данных. Соединитель партнера преобразует содержимое элемента в формат сообщения электронной почты. Описание схемы формата сообщений представлено в разделе " [Дополнительные сведения](#more-information) ".</span><span class="sxs-lookup"><span data-stu-id="5d324-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="5d324-131">Партнерский соединитель подключается к службе Azure в Office 365 с помощью веб-службы Exchange (EWS) через хорошо известную конечную точку.</span><span class="sxs-lookup"><span data-stu-id="5d324-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="5d324-p105">Элементы импортируются в почтовый ящик определенного пользователя или общий почтовый ящик для сторонних данных. Элемент импортируется в почтовый ящик определенного пользователя или общий почтовый ящик для сторонних данных, исходя из следующих критериев:</span><span class="sxs-lookup"><span data-stu-id="5d324-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="5d324-p106">a. **элементы с идентификатором пользователя, который соответствует учетной записи пользователя Office 365** — если соединитель партнера может сопоставить идентификатор пользователя элемента в источнике данных стороннего производителя с определенным идентификатором пользователя в Office 365, он будет скопирован в папку " **очистки** " пользователя. Папка "элементы для восстановления". Пользователи не могут получить доступ к элементам в папке "очистки". Тем не менее, вы можете использовать средства обнаружения электронных данных Office 365 для поиска элементов в папке "очистки".</span><span class="sxs-lookup"><span data-stu-id="5d324-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="5d324-p107">б. **элементы, которые не имеют идентификатора пользователя, соответствующего учетной записи пользователя Office 365** — если соединителю партнера не удается сопоставить идентификатор пользователя с определенным идентификатором пользователя в Office 365, элемент будет скопирован в папку **"Входящие"** стороннего почтового ящика данных. При импорте элементов в папку "Входящие" вы или другой пользователь в Организации можете войти в почтовый ящик стороннего производителя для просмотра этих элементов и управления ими, а также узнать, нужно ли вносить какие-либо изменения в конфигурацию соединителя партнера.</span><span class="sxs-lookup"><span data-stu-id="5d324-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="5d324-141">Шаг 1. Поиск партнера по работе со сторонними данными</span><span class="sxs-lookup"><span data-stu-id="5d324-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="5d324-p108">Ключевой компонент для архивации сторонних данных в Office 365: Поиск и работа с партнером Майкрософт, специализирующимся на сборе данных из стороннего источника данных и их импорте в Office 365. После импорта данные можно заархивировать и сохранить вместе с другими данными Майкрософт, такими как электронная почта от Exchange и документы из SharePoint и OneDrive для бизнеса. Партнер создает соединитель, который извлекает данные из сторонних источников данных Организации (таких как BlackBerry, Facebook, Google +, Thomson Reuters, Twitter и YouTube), и передает эти данные в API Office 365, который импортирует элементы в почтовые ящики Exchange как сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="5d324-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="5d324-145">В следующих разделах перечислены партнеры Майкрософт, а также сторонние источники данных, которые они поддерживают, которые участвуют в программе для архивации сторонних данных в Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="5d324-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="5d324-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="5d324-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="5d324-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="5d324-148">АрчивесоЦиал</span><span class="sxs-lookup"><span data-stu-id="5d324-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="5d324-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="5d324-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="5d324-150">Опентекст</span><span class="sxs-lookup"><span data-stu-id="5d324-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="5d324-151">Verba</span><span class="sxs-lookup"><span data-stu-id="5d324-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="5d324-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="5d324-152">17a-4 LLC</span></span>

<span data-ttu-id="5d324-153">17a-4 LLC поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="5d324-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="5d324-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="5d324-154">BlackBerry</span></span>
    
- <span data-ttu-id="5d324-155">потоки данных Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="5d324-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="5d324-156">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="5d324-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="5d324-157">Факт</span><span class="sxs-lookup"><span data-stu-id="5d324-157">FactSet</span></span>
    
- <span data-ttu-id="5d324-158">Хипчат</span><span class="sxs-lookup"><span data-stu-id="5d324-158">HipChat</span></span>
    
- <span data-ttu-id="5d324-159">Инвестедже</span><span class="sxs-lookup"><span data-stu-id="5d324-159">InvestEdge</span></span>
    
- <span data-ttu-id="5d324-160">Ливеперсон</span><span class="sxs-lookup"><span data-stu-id="5d324-160">LivePerson</span></span>
    
- <span data-ttu-id="5d324-161">
MessageLabs Data Streams;
</span><span class="sxs-lookup"><span data-stu-id="5d324-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="5d324-162">Опентекст</span><span class="sxs-lookup"><span data-stu-id="5d324-162">OpenText</span></span>
    
- <span data-ttu-id="5d324-163">Oracle/ATG Click-to-Call Live Help;
</span><span class="sxs-lookup"><span data-stu-id="5d324-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="5d324-164">Pivot IMTRADER;
</span><span class="sxs-lookup"><span data-stu-id="5d324-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="5d324-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="5d324-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="5d324-166">Миндалигн</span><span class="sxs-lookup"><span data-stu-id="5d324-166">MindAlign</span></span>
    
- <span data-ttu-id="5d324-167">Sitrion One (Newsgator);</span><span class="sxs-lookup"><span data-stu-id="5d324-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="5d324-168">
Skype для бизнеса (Lync/OCS);</span><span class="sxs-lookup"><span data-stu-id="5d324-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="5d324-169">
Skype для бизнеса Online (Lync Online);
</span><span class="sxs-lookup"><span data-stu-id="5d324-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="5d324-170">базы данных SQL;</span><span class="sxs-lookup"><span data-stu-id="5d324-170">SQL Databases</span></span>
    
- <span data-ttu-id="5d324-171">
Squawker;
</span><span class="sxs-lookup"><span data-stu-id="5d324-171">Squawker</span></span>
    
- <span data-ttu-id="5d324-172">Thomson Reuters Eikon Messenger.
</span><span class="sxs-lookup"><span data-stu-id="5d324-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="5d324-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="5d324-173">Actiance</span></span>

<span data-ttu-id="5d324-174">[Актианце](https://www.actiance.com) поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="5d324-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5d324-175">AIM;</span><span class="sxs-lookup"><span data-stu-id="5d324-175">AIM</span></span>
    
- <span data-ttu-id="5d324-176">American Idol;</span><span class="sxs-lookup"><span data-stu-id="5d324-176">American Idol</span></span>
    
- <span data-ttu-id="5d324-177">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="5d324-177">Apple Juice</span></span>
    
- <span data-ttu-id="5d324-178">
AOL с клиентом Pivot;
</span><span class="sxs-lookup"><span data-stu-id="5d324-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="5d324-179">Ares;</span><span class="sxs-lookup"><span data-stu-id="5d324-179">Ares</span></span>
    
- <span data-ttu-id="5d324-180">Bazaar Voice;</span><span class="sxs-lookup"><span data-stu-id="5d324-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="5d324-181">Bear Share;</span><span class="sxs-lookup"><span data-stu-id="5d324-181">Bear Share</span></span>
    
- <span data-ttu-id="5d324-182">Bit Torrent;</span><span class="sxs-lookup"><span data-stu-id="5d324-182">Bit Torrent</span></span>
    
- <span data-ttu-id="5d324-183">журналы вызовов BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-184">BlackBerry Messenger (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-185">PIN-код BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-186">BlackBerry SMS (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-187">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="5d324-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="5d324-188">Целлтруст</span><span class="sxs-lookup"><span data-stu-id="5d324-188">CellTrust</span></span>
    
- <span data-ttu-id="5d324-189">импорт чата;
</span><span class="sxs-lookup"><span data-stu-id="5d324-189">Chat Import</span></span>
    
- <span data-ttu-id="5d324-190">политика и ведение журнала чата в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="5d324-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="5d324-191">Chatter;
</span><span class="sxs-lookup"><span data-stu-id="5d324-191">Chatter</span></span>
    
- <span data-ttu-id="5d324-192">Сервер Cisco &amp; IM Presence Server (v 9.0.1, v 9.1, v 9.1.1 SU1, 10, v 10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="5d324-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="5d324-193">Cisco Unified Presence Server (версии 8.6.3, 8.6.4, 8.6.5);
</span><span class="sxs-lookup"><span data-stu-id="5d324-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="5d324-194">импорт совместной работы;</span><span class="sxs-lookup"><span data-stu-id="5d324-194">Collaboration Import</span></span>
    
- <span data-ttu-id="5d324-195">ведение журнала совместной работы в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="5d324-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="5d324-196">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="5d324-196">Direct Connect</span></span>
    
- <span data-ttu-id="5d324-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="5d324-197">Facebook</span></span>
    
- <span data-ttu-id="5d324-198">Факт</span><span class="sxs-lookup"><span data-stu-id="5d324-198">FactSet</span></span>
    
- <span data-ttu-id="5d324-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="5d324-199">FastTrack</span></span>
    
- <span data-ttu-id="5d324-200">Gnutella;</span><span class="sxs-lookup"><span data-stu-id="5d324-200">Gnutella</span></span>
    
- <span data-ttu-id="5d324-201">Google+;
</span><span class="sxs-lookup"><span data-stu-id="5d324-201">Google+</span></span>
    
- <span data-ttu-id="5d324-202">Готомипк</span><span class="sxs-lookup"><span data-stu-id="5d324-202">GoToMyPC</span></span>
    
- <span data-ttu-id="5d324-203">Hopster;</span><span class="sxs-lookup"><span data-stu-id="5d324-203">Hopster</span></span>
    
- <span data-ttu-id="5d324-204">Хубконнекс</span><span class="sxs-lookup"><span data-stu-id="5d324-204">HubConnex</span></span>
    
- <span data-ttu-id="5d324-205">IBM Connections (версии 3.0.1, 4.0, 4.5, 4.5 CR3, 5);
</span><span class="sxs-lookup"><span data-stu-id="5d324-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="5d324-206">IBM Connections Chat Cloud;
</span><span class="sxs-lookup"><span data-stu-id="5d324-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="5d324-207">IBM Connections Social Cloud;
</span><span class="sxs-lookup"><span data-stu-id="5d324-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="5d324-208">IBM SameTime Advanced 8.5.2 IFR1;
</span><span class="sxs-lookup"><span data-stu-id="5d324-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="5d324-209">IBM SameTime Communicate 9.0;
</span><span class="sxs-lookup"><span data-stu-id="5d324-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="5d324-210">IBM SameTime Community (версии 8.0.2, 8.5.1 IFR2, 8.5.2 IFR1, 9.1);
</span><span class="sxs-lookup"><span data-stu-id="5d324-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="5d324-211">IBM SameTime Complete 9.0;
</span><span class="sxs-lookup"><span data-stu-id="5d324-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="5d324-212">IBM SameTime Conference 9.0;
</span><span class="sxs-lookup"><span data-stu-id="5d324-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="5d324-213">IBM SameTime Meeting 8.5.2 IFR1;
</span><span class="sxs-lookup"><span data-stu-id="5d324-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="5d324-214">ICE/Елловжаккет</span><span class="sxs-lookup"><span data-stu-id="5d324-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="5d324-215">импорт мгновенных сообщений;
</span><span class="sxs-lookup"><span data-stu-id="5d324-215">IM Import</span></span>
    
- <span data-ttu-id="5d324-216">политика и ведение журнала обмена мгновенными сообщениями в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="5d324-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="5d324-217">Indii Messenger;
</span><span class="sxs-lookup"><span data-stu-id="5d324-217">Indii Messenger</span></span>
    
- <span data-ttu-id="5d324-218">Instant Bloomberg;
</span><span class="sxs-lookup"><span data-stu-id="5d324-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="5d324-219">IRC;</span><span class="sxs-lookup"><span data-stu-id="5d324-219">IRC</span></span>
    
- <span data-ttu-id="5d324-220">Jive;
</span><span class="sxs-lookup"><span data-stu-id="5d324-220">Jive</span></span>
    
- <span data-ttu-id="5d324-221">Jive 6 Real Time Logging (версии 6, 7);
</span><span class="sxs-lookup"><span data-stu-id="5d324-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="5d324-222">импорт Jive;</span><span class="sxs-lookup"><span data-stu-id="5d324-222">Jive Import</span></span>
    
- <span data-ttu-id="5d324-223">JXTA;</span><span class="sxs-lookup"><span data-stu-id="5d324-223">JXTA</span></span>
    
- <span data-ttu-id="5d324-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5d324-224">LinkedIn</span></span>
    
- <span data-ttu-id="5d324-225">
Microsoft Lync (2010, 2013);
</span><span class="sxs-lookup"><span data-stu-id="5d324-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="5d324-226">MFTP;</span><span class="sxs-lookup"><span data-stu-id="5d324-226">MFTP</span></span>
    
- <span data-ttu-id="5d324-227">Microsoft Lync 2013 Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="5d324-228">Microsoft SharePoint (2010, 2013);
</span><span class="sxs-lookup"><span data-stu-id="5d324-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="5d324-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="5d324-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="5d324-230">Microsoft UC (Unified Communications);</span><span class="sxs-lookup"><span data-stu-id="5d324-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="5d324-231">Миндалигн</span><span class="sxs-lookup"><span data-stu-id="5d324-231">MindAlign</span></span>
    
- <span data-ttu-id="5d324-232">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="5d324-232">Mobile Guard</span></span>
    
- <span data-ttu-id="5d324-233">MSN;</span><span class="sxs-lookup"><span data-stu-id="5d324-233">MSN</span></span>
    
- <span data-ttu-id="5d324-234">My Space;</span><span class="sxs-lookup"><span data-stu-id="5d324-234">My Space</span></span>
    
- <span data-ttu-id="5d324-235">NEONetwork;</span><span class="sxs-lookup"><span data-stu-id="5d324-235">NEONetwork</span></span>
    
- <span data-ttu-id="5d324-236">Office 365 Lync Dedicated;
</span><span class="sxs-lookup"><span data-stu-id="5d324-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="5d324-237">групповой чат Office 365;
</span><span class="sxs-lookup"><span data-stu-id="5d324-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="5d324-238">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="5d324-238">Pinterest</span></span>
    
- <span data-ttu-id="5d324-239">Pivot;</span><span class="sxs-lookup"><span data-stu-id="5d324-239">Pivot</span></span>
    
- <span data-ttu-id="5d324-240">QQ;</span><span class="sxs-lookup"><span data-stu-id="5d324-240">QQ</span></span>
    
- <span data-ttu-id="5d324-241">Skype для бизнеса 2015</span><span class="sxs-lookup"><span data-stu-id="5d324-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="5d324-242">Софтесер</span><span class="sxs-lookup"><span data-stu-id="5d324-242">SoftEther</span></span>
    
- <span data-ttu-id="5d324-243">Symphony;
</span><span class="sxs-lookup"><span data-stu-id="5d324-243">Symphony</span></span>
    
- <span data-ttu-id="5d324-244">Thomson Reuters Eikon;
</span><span class="sxs-lookup"><span data-stu-id="5d324-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="5d324-245">Thomson Reuters Messenger;
</span><span class="sxs-lookup"><span data-stu-id="5d324-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="5d324-246">Tor;</span><span class="sxs-lookup"><span data-stu-id="5d324-246">Tor</span></span>
    
- <span data-ttu-id="5d324-247">TTT;</span><span class="sxs-lookup"><span data-stu-id="5d324-247">TTT</span></span>
    
- <span data-ttu-id="5d324-248">Твиттер</span><span class="sxs-lookup"><span data-stu-id="5d324-248">Twitter</span></span>
    
- <span data-ttu-id="5d324-249">Винмкс</span><span class="sxs-lookup"><span data-stu-id="5d324-249">WinMX</span></span>
    
- <span data-ttu-id="5d324-250">Winny;</span><span class="sxs-lookup"><span data-stu-id="5d324-250">Winny</span></span>
    
- <span data-ttu-id="5d324-251">Yahoo;
</span><span class="sxs-lookup"><span data-stu-id="5d324-251">Yahoo</span></span>
    
- <span data-ttu-id="5d324-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="5d324-252">Yammer</span></span>
    
- <span data-ttu-id="5d324-253">Своему</span><span class="sxs-lookup"><span data-stu-id="5d324-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="5d324-254">АрчивесоЦиал</span><span class="sxs-lookup"><span data-stu-id="5d324-254">ArchiveSocial</span></span>

<span data-ttu-id="5d324-255">[АрчивесоЦиал](https://www.archivesocial.com) поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="5d324-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5d324-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="5d324-256">Facebook</span></span>
    
- <span data-ttu-id="5d324-257">Flickr;
</span><span class="sxs-lookup"><span data-stu-id="5d324-257">Flickr</span></span>
    
- <span data-ttu-id="5d324-258">Instagram;
</span><span class="sxs-lookup"><span data-stu-id="5d324-258">Instagram</span></span>
    
- <span data-ttu-id="5d324-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="5d324-259">LinkedIn</span></span>
    
- <span data-ttu-id="5d324-260">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="5d324-260">Pinterest</span></span>
    
- <span data-ttu-id="5d324-261">Твиттер</span><span class="sxs-lookup"><span data-stu-id="5d324-261">Twitter</span></span>
    
- <span data-ttu-id="5d324-262">Своему</span><span class="sxs-lookup"><span data-stu-id="5d324-262">YouTube</span></span>
    
- <span data-ttu-id="5d324-263">Vimeo.</span><span class="sxs-lookup"><span data-stu-id="5d324-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="5d324-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="5d324-264">Globanet</span></span>

<span data-ttu-id="5d324-265">[Глобанет](https://www.globanet.com) поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="5d324-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5d324-266">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="5d324-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="5d324-267">журналы вызовов BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-268">BlackBerry Messenger (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-269">PIN-код BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-270">BlackBerry SMS (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="5d324-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="5d324-271">Bloomberg Chat;
</span><span class="sxs-lookup"><span data-stu-id="5d324-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="5d324-272">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="5d324-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="5d324-273">Box</span><span class="sxs-lookup"><span data-stu-id="5d324-273">Box</span></span>
    
- <span data-ttu-id="5d324-274">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="5d324-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="5d324-275">Сервер для &amp; обмена МГНОВЕНными сообщениями Cisco (10, v 10.5.1 SU1, v SU2, v 11.5)</span><span class="sxs-lookup"><span data-stu-id="5d324-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="5d324-276">Cisco Вебекс Teams</span><span class="sxs-lookup"><span data-stu-id="5d324-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="5d324-277">ShareFile рабочей &amp; области Citrix</span><span class="sxs-lookup"><span data-stu-id="5d324-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="5d324-278">Кровдкомпасс</span><span class="sxs-lookup"><span data-stu-id="5d324-278">CrowdCompass</span></span>

- <span data-ttu-id="5d324-279">настраиваемые текстовые файлы с разделителями;
</span><span class="sxs-lookup"><span data-stu-id="5d324-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="5d324-280">настраиваемые XML-файлы;
</span><span class="sxs-lookup"><span data-stu-id="5d324-280">Custom XML files</span></span>
    
- <span data-ttu-id="5d324-281">Facebook (страницы)</span><span class="sxs-lookup"><span data-stu-id="5d324-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="5d324-282">Factset;
</span><span class="sxs-lookup"><span data-stu-id="5d324-282">Factset</span></span>
    
- <span data-ttu-id="5d324-283">FXConnect;</span><span class="sxs-lookup"><span data-stu-id="5d324-283">FXConnect</span></span>
    
- <span data-ttu-id="5d324-284">ICE Chat или YellowJacket;</span><span class="sxs-lookup"><span data-stu-id="5d324-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="5d324-285">Jive;
</span><span class="sxs-lookup"><span data-stu-id="5d324-285">Jive</span></span>
    
- <span data-ttu-id="5d324-286">Macgregor XIP;
</span><span class="sxs-lookup"><span data-stu-id="5d324-286">Macgregor XIP</span></span>

- <span data-ttu-id="5d324-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="5d324-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="5d324-288">Microsoft OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="5d324-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="5d324-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5d324-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="5d324-290">Microsoft Yammer;
</span><span class="sxs-lookup"><span data-stu-id="5d324-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="5d324-291">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="5d324-291">Mobile Guard</span></span>
    
- <span data-ttu-id="5d324-292">Pivot;</span><span class="sxs-lookup"><span data-stu-id="5d324-292">Pivot</span></span>
    
- <span data-ttu-id="5d324-293">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="5d324-293">Salesforce Chatter</span></span>

- <span data-ttu-id="5d324-294">Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="5d324-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="5d324-295">Skype для бизнеса, версии от 2007 R2 до 2016 (локальные);
</span><span class="sxs-lookup"><span data-stu-id="5d324-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="5d324-296">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="5d324-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="5d324-297">Symphony;</span><span class="sxs-lookup"><span data-stu-id="5d324-297">Symphony</span></span>
    
- <span data-ttu-id="5d324-298">Thomson Reuters Eikon;
</span><span class="sxs-lookup"><span data-stu-id="5d324-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="5d324-299">Thomson Reuters Messenger;
</span><span class="sxs-lookup"><span data-stu-id="5d324-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="5d324-300">Thomson Reuters Dealings 3000 или FX Trading;
</span><span class="sxs-lookup"><span data-stu-id="5d324-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="5d324-301">Твиттер</span><span class="sxs-lookup"><span data-stu-id="5d324-301">Twitter</span></span>
    
- <span data-ttu-id="5d324-302">UBS Chat;
</span><span class="sxs-lookup"><span data-stu-id="5d324-302">UBS Chat</span></span>
    
- <span data-ttu-id="5d324-303">Своему</span><span class="sxs-lookup"><span data-stu-id="5d324-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="5d324-304">Опентекст</span><span class="sxs-lookup"><span data-stu-id="5d324-304">OpenText</span></span>

<span data-ttu-id="5d324-305">[Опентекст](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="5d324-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5d324-306">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="5d324-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="5d324-307">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="5d324-307">Axs Exchange</span></span>
    
- <span data-ttu-id="5d324-308">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="5d324-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="5d324-309">Axs PlaceHolder;</span><span class="sxs-lookup"><span data-stu-id="5d324-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="5d324-310">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="5d324-310">Axs Signed</span></span>
    
- <span data-ttu-id="5d324-311">Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="5d324-311">Bloomberg</span></span>
    
- <span data-ttu-id="5d324-312">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="5d324-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="5d324-313">Verba</span><span class="sxs-lookup"><span data-stu-id="5d324-313">Verba</span></span>

<span data-ttu-id="5d324-314">[Verb](https://www.verba.com) поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="5d324-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="5d324-315">Avaya Aura Video;
</span><span class="sxs-lookup"><span data-stu-id="5d324-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="5d324-316">Avaya Aura Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="5d324-317">Avtec Radio;
</span><span class="sxs-lookup"><span data-stu-id="5d324-317">Avtec Radio</span></span>
    
- <span data-ttu-id="5d324-318">Bosch/Telex Radio;
</span><span class="sxs-lookup"><span data-stu-id="5d324-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="5d324-319">BroadSoft Video;
</span><span class="sxs-lookup"><span data-stu-id="5d324-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="5d324-320">BroadSoft Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="5d324-321">Centile Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-321">Centile Voice</span></span>
    
- <span data-ttu-id="5d324-322">Cisco Jabber IM;
</span><span class="sxs-lookup"><span data-stu-id="5d324-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="5d324-323">Cisco UC Video;
</span><span class="sxs-lookup"><span data-stu-id="5d324-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="5d324-324">Cisco UC Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="5d324-325">Cisco UCCX/UCCE Video</span><span class="sxs-lookup"><span data-stu-id="5d324-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="5d324-326">Cisco UCCX/UCCE Voice</span><span class="sxs-lookup"><span data-stu-id="5d324-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="5d324-327">ESChat Radio;</span><span class="sxs-lookup"><span data-stu-id="5d324-327">ESChat Radio</span></span>
    
- <span data-ttu-id="5d324-328">Geoman Contact Expert;</span><span class="sxs-lookup"><span data-stu-id="5d324-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="5d324-329">IP Trade Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="5d324-330">Luware LUCS Contact Center;</span><span class="sxs-lookup"><span data-stu-id="5d324-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="5d324-331">Microsoft UC (Unified Communications);</span><span class="sxs-lookup"><span data-stu-id="5d324-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="5d324-332">Mitel MiContact Center для Lync (prairieFyre);
</span><span class="sxs-lookup"><span data-stu-id="5d324-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="5d324-333">Oracle / Acme Packet Session Border Controller Video;
</span><span class="sxs-lookup"><span data-stu-id="5d324-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="5d324-334">Oracle / Acme Packet Session Border Controller Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="5d324-335">Singtel Mobile Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="5d324-336">SIPREC Video;</span><span class="sxs-lookup"><span data-stu-id="5d324-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="5d324-337">SIPREC Voice;</span><span class="sxs-lookup"><span data-stu-id="5d324-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="5d324-338">Skype для бизнеса / Lync IM;
</span><span class="sxs-lookup"><span data-stu-id="5d324-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="5d324-339">Skype для бизнеса / Lync Video;
</span><span class="sxs-lookup"><span data-stu-id="5d324-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="5d324-340">Skype для бизнеса / Lync Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="5d324-341">Speakerbus Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="5d324-342">Standard SIP/H.323 Video;
</span><span class="sxs-lookup"><span data-stu-id="5d324-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="5d324-343">Standard SIP/H.323 Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="5d324-344">Truphone Voice;
</span><span class="sxs-lookup"><span data-stu-id="5d324-344">Truphone Voice</span></span>
    
- <span data-ttu-id="5d324-345">TwistedPair Radio;
</span><span class="sxs-lookup"><span data-stu-id="5d324-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="5d324-346">рабочий стол Windows.
</span><span class="sxs-lookup"><span data-stu-id="5d324-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="5d324-347">Шаг 2. Создание и настройка почтового ящика сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="5d324-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="5d324-p109">Ниже приведены действия по созданию и настройке почтового ящика данных стороннего производителя для импорта данных в Office 365. Как было сказано выше, элементы импортируются в этот почтовый ящик, если соединитель партнера не может сопоставить идентификатор пользователя с учетной записью пользователя Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="5d324-350">**Выполните эти действия в центре администрирования Office 365**</span><span class="sxs-lookup"><span data-stu-id="5d324-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="5d324-p110">Создайте новую учетную запись пользователя в Office 365 и назначьте ей лицензию на Exchange Online (план 2). Ознакомьтесь [со статьЕй Добавление пользователей в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Лицензия на план 2 необходима, чтобы поместить почтовый ящик на хранение для судебного разбирательства или включить архивный почтовый ящик с неограниченной квотой.</span><span class="sxs-lookup"><span data-stu-id="5d324-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="5d324-353">Добавьте учетную запись пользователя для почтового ящика данных стороннего производителя в роль администратора **администратора Exchange** в Office 365; [в разделе Назначение ролей администратора в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="5d324-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="5d324-p111">Запишите данные этой учетной записи. Их необходимо предоставить партнеру, как описано в шаге 4.</span><span class="sxs-lookup"><span data-stu-id="5d324-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="5d324-356">**Выполнение этих задач в центре администрирования Exchange**</span><span class="sxs-lookup"><span data-stu-id="5d324-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="5d324-p112">Скрытие почтового ящика сторонних данных из адресной книги и других списков адресов в Организации; в разделе [Управление почтовыми ящиками пользователей](https://go.microsoft.com/fwlink/p/?LinkId=616058). Кроме того, можно выполнить следующую команду PowerShell:</span><span class="sxs-lookup"><span data-stu-id="5d324-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="5d324-359">Назначьте разрешение **FullAccess** для почтового ящика данных стороннего производителя, чтобы администраторы или руководители соответствия могли открыть сторонний почтовый ящик данных в клиенте Outlook для настольных ПК. Ознакомьтесь с разрешениями [Управление разрешениями для получателей](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span><span class="sxs-lookup"><span data-stu-id="5d324-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="5d324-360">Включите следующие функции Office 365, связанные с соответствием требованиям, для почтового ящика данных стороннего производителя:</span><span class="sxs-lookup"><span data-stu-id="5d324-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="5d324-p113">Включение архивного почтового ящика; в разделе [Включение архивных почтовых ящиков в центре безопасности &amp; Office 365](enable-archive-mailboxes.md) и включение неограниченного архивирования [в Office 365](enable-unlimited-archiving.md). Это позволит освободить дисковое пространство в основном почтовом ящике, настроив политику архивации, которая перемещает сторонние элементы данных в архивный почтовый ящик. Это обеспечит неограниченное хранение данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="5d324-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="5d324-p114">Поместите сторонний почтовый ящик данных на удержание для судебного разбирательства. Вы также можете применить политику хранения Office 365 в центре безопасности &amp; и соответствия требованиям Office 365. При размещении этого почтового ящика на удержании будут сохраняться сторонние элементы данных (неограниченно или не определен длительность), и их не следует удалять из почтового ящика. Просмотрите один из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="5d324-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="5d324-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="5d324-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="5d324-369">Общие сведения о политиках хранения в Office 365</span><span class="sxs-lookup"><span data-stu-id="5d324-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="5d324-p115">Включение ведения журнала аудита почтовых ящиков для владельца, представителя и административного доступа к почтовому ящику данных стороннего производителя; [в разделе включить аудит почтовых ящиков в Office 365](enable-mailbox-auditing.md). Это позволит отслеживать все действия, выполненные любым пользователем, имеющим доступ к почтовому ящику данных стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="5d324-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="5d324-372">Шаг 3. Настройка поддержки сторонних данных для почтовых ящиков пользователей</span><span class="sxs-lookup"><span data-stu-id="5d324-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="5d324-p116">Следующий шаг — настройка почтовых ящиков пользователей для поддержки сторонних данных. Выполните указанные ниже действия с помощью центра администрирования Exchange или соответствующих командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d324-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="5d324-375">Включите архивный почтовый ящик для каждого пользователя; в разделе [Включение архивных почтовых ящиков в центре безопасности &amp; Office 365](enable-archive-mailboxes.md) и включение неограниченного архивирования [в Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="5d324-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="5d324-376">ПоМещайте почтовые ящики пользователей на хранение для судебного разбирательства или примените политику хранения Office 365; Просмотрите один из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="5d324-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="5d324-377">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="5d324-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="5d324-378">Общие сведения о политиках хранения в Office 365</span><span class="sxs-lookup"><span data-stu-id="5d324-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="5d324-379">Как отмечалось ранее, при помещении почтовых ящиков на хранение можно указать длительность хранения элементов из источника сторонних данных или выбрать бессрочное хранение.</span><span class="sxs-lookup"><span data-stu-id="5d324-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="5d324-380">Шаг 4. Предоставление сведений партнеру</span><span class="sxs-lookup"><span data-stu-id="5d324-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="5d324-381">Последний шаг — предоставить партнеру указанные ниже сведения, чтобы он смог настроить соединитель для подключения к организации Office 365 и импорта данных в почтовые ящики пользователей и почтовый ящик сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="5d324-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="5d324-382">Конечная точка, используемая для подключения к службе Azure в Office 365:</span><span class="sxs-lookup"><span data-stu-id="5d324-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="5d324-p117">Учетные данные для входа (Office 365 ID пользователя и пароль) почтового ящика данных стороннего производителя, созданного в шаге 2. Эти учетные данные необходимы для того, чтобы соединитель партнера мог получать доступ к почтовым ящикам пользователей и импортировать их в почтовые ящики данных сторонних поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5d324-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="5d324-385">Шаг 5: заРегистрируйте сторонний соединитель данных в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5d324-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="5d324-p118">Начиная с 30 сентября 2018, служба Azure в Office 365 начнет использовать современные проверки подлинности в Exchange Online для проверки подлинности сторонних соединителей данных, пытающихся подключиться к организации Office 365 для импорта данных. Причина этого изменения заключается в том, что современная проверка подлинности обеспечивает большую безопасность, чем текущий метод, основанный на соединителях третьих сторон вхителистинг, использующих ранее описанную конечную точку для подключения к службе Azure.</span><span class="sxs-lookup"><span data-stu-id="5d324-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="5d324-p119">Чтобы включить сторонний соединитель данных для подключения к Office 365 с помощью нового метода проверки подлинности, администратору в организации Office 365 необходимо согласиться на регистрацию соединителя как доверенного приложения службы в Azure Active Directory. Для этого необходимо принять запрос на разрешение соединителя, чтобы разрешить соединителю получать доступ к данным вашей организации в Azure Active Directory. После принятия этого запроса сторонний соединитель данных добавляется в качестве корпоративного приложения в Azure Active Directory и представляется в качестве субъекта-службы. Более подробную информацию можно найти в разделе [согласие администратора клиента](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="5d324-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="5d324-392">Ниже описаны действия, которые необходимо выполнить, чтобы получить доступ и принять запрос на регистрацию соединителя:</span><span class="sxs-lookup"><span data-stu-id="5d324-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="5d324-393">Перейдите на [эту страницу](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) и войдите в систему, используя учетные данные глобального администратора Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="5d324-p120">Отображается следующее диалоговое окно. Вы можете развернуть символы крышки, чтобы просмотреть разрешения, которые будут назначены соединителю.</span><span class="sxs-lookup"><span data-stu-id="5d324-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="5d324-396">![Отображается диалоговое окно запроса разрешений](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="5d324-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="5d324-397">Нажмите кнопку **принять**.</span><span class="sxs-lookup"><span data-stu-id="5d324-397">Click **Accept**.</span></span>

<span data-ttu-id="5d324-p121">После принятия запроса отображается [портал Azure](https://portal.azure.com) . Чтобы просмотреть список приложений для вашей организации, щелкните элемент **Azure Active Directory** > **Enterprise Applications**. Сторонний соединитель данных Office 365 указан в колонке **корпоративные приложения** .</span><span class="sxs-lookup"><span data-stu-id="5d324-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d324-p122">После 30 сентября 2018 данные сторонних поставщиков больше не будут импортироваться в почтовые ящики в вашей организации, если вы не зарегистрируете сторонний соединитель данных в Azure Active Directory. Обратите внимание, что существующие сторонние соединители данных (созданные до 30 сентября 2018) также должны быть зарегистрированы в Azure Active Directory, выполнив действия, описанные в шаге 5.</span><span class="sxs-lookup"><span data-stu-id="5d324-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="5d324-403">Отзыв согласия с сторонним соединителем данных</span><span class="sxs-lookup"><span data-stu-id="5d324-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="5d324-p123">После того как ваша организация отправила запрос на разрешения на регистрацию стороннего соединителя данных в Azure Active Directory, ваша организация может в любой момент отозвать это согласие. Однако отзыв согласия для соединителя будет означать, что данные из стороннего источника данных больше не будут импортироваться в Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="5d324-p124">Чтобы отозвать согласие на сторонние соединители данных, можно удалить приложение (удалив соответствующий субъект-службу) из Azure Active Directory, используя колонку **корпоративных приложений** на портале Azure, или с помощью [ ReMove – MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. Вы также можете использовать командлет [Remove – азуреадсервицепринЦипал](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) в Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d324-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="5d324-408">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="5d324-408">More information</span></span>

- <span data-ttu-id="5d324-p125">Как показано выше, элементы из сторонних источников данных импортируются в почтовые ящики Exchange как сообщения электронной почты. Соединитель партнера импортирует элемент, используя схему, требуемую API Office 365. В следующей таблице описаны свойства сообщения элемента из стороннего источника данных после его импорта в почтовый ящик Exchange в виде сообщения электронной почты. В таблице также указано, является ли свойство Message обязательным. Обязательные свойства должны быть заполнены. Если для элемента отсутствует обязательное свойство, оно не будет импортировано в Office 365. Процесс импорта возвратит сообщение об ошибке, объясняющее, почему элемент не был импортирован и какое свойство отсутствует.</span><span class="sxs-lookup"><span data-stu-id="5d324-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="5d324-416">**Свойство сообщения**</span><span class="sxs-lookup"><span data-stu-id="5d324-416">**Message property**</span></span>|<span data-ttu-id="5d324-417">**Обязателен?**</span><span class="sxs-lookup"><span data-stu-id="5d324-417">**Mandatory?**</span></span>|<span data-ttu-id="5d324-418">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d324-418">**Description**</span></span>|<span data-ttu-id="5d324-419">**Пример значения**</span><span class="sxs-lookup"><span data-stu-id="5d324-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="5d324-420">**FROM**</span><span class="sxs-lookup"><span data-stu-id="5d324-420">**FROM**</span></span> <br/> |<span data-ttu-id="5d324-421">Да</span><span class="sxs-lookup"><span data-stu-id="5d324-421">Yes</span></span>  <br/> |<span data-ttu-id="5d324-p126">Пользователь, который изначально создал или отправил элемент в источнике данных стороннего разработчика. Соединитель партнера попытается сопоставить идентификатор пользователя из исходного элемента (например, дескриптора Twitter) с учетной записью пользователя Office 365 для всех участников (в полях "от" и "Кому"). Копия сообщения будет импортирована в почтовый ящик каждого участника. Если ни один из участников этого элемента не может быть сопоставлен с учетной записью пользователя Office 365, он будет импортирован в почтовый ящик стороннего пользователя для архивации в Office 365.</span><span class="sxs-lookup"><span data-stu-id="5d324-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="5d324-p127">Участник, идентифицированный как отправитель элемента, должен иметь в организации Office 365 активный почтовый ящик, в который импортируется элемент. Если отправитель не имеет активного почтового ящика, возвращается следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="5d324-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="5d324-428">**TO**</span><span class="sxs-lookup"><span data-stu-id="5d324-428">**TO**</span></span> <br/> |<span data-ttu-id="5d324-429">Да</span><span class="sxs-lookup"><span data-stu-id="5d324-429">Yes</span></span>  <br/> |<span data-ttu-id="5d324-430">Пользователь, получивший элемент, если это применимо к элементу в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="5d324-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="5d324-431">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="5d324-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="5d324-432">Нет</span><span class="sxs-lookup"><span data-stu-id="5d324-432">No</span></span>  <br/> |<span data-ttu-id="5d324-433">Тема исходного элемента.</span><span class="sxs-lookup"><span data-stu-id="5d324-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="5d324-434">**БУДУЩ**</span><span class="sxs-lookup"><span data-stu-id="5d324-434">**DATE**</span></span> <br/> |<span data-ttu-id="5d324-435">Да</span><span class="sxs-lookup"><span data-stu-id="5d324-435">Yes</span></span>  <br/> |<span data-ttu-id="5d324-436">Дата создания или публикации элемента в источнике данных клиента, например дата отправки сообщения в Твиттере.</span><span class="sxs-lookup"><span data-stu-id="5d324-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="5d324-437">**BODY**</span><span class="sxs-lookup"><span data-stu-id="5d324-437">**BODY**</span></span> <br/> |<span data-ttu-id="5d324-438">Нет</span><span class="sxs-lookup"><span data-stu-id="5d324-438">No</span></span>  <br/> |<span data-ttu-id="5d324-p128">Содержимое сообщения или сообщения. Для некоторых источников данных содержимое этого свойства может совпадать с содержимым свойства **subject** . Во время процесса импорта соединитель партнера будет пытаться поддерживать полную точность источника контента, как это возможно. Если в это свойство включено несколько файлов, графика или другое содержимое из основного текста исходного элемента. В противном случае содержимое из исходного элемента будет включено в свойство **вложения** . Содержимое этого свойства будет зависеть от соединителя партнера и возможности исходной платформы.</span><span class="sxs-lookup"><span data-stu-id="5d324-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="5d324-445">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="5d324-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="5d324-446">Нет</span><span class="sxs-lookup"><span data-stu-id="5d324-446">No</span></span>  <br/> |<span data-ttu-id="5d324-p129">Если элемент в источнике данных (например, твит в Twitter или беседе обмена мгновенными сообщениями) имеет вложенный файл или включает изображения, то партнер по подключению будет сначала пытаться включить вложения в свойство **Body** . Если это невозможно, то оно добавляется в свойство \* \* вложение \* \*. К другим примерам вложений относятся "нравится Facebook", "метаданные источника контента" и "ответы на сообщения" или "Post".</span><span class="sxs-lookup"><span data-stu-id="5d324-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the \*\* ATTACHMENT \*\* property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="5d324-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="5d324-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="5d324-451">Да</span><span class="sxs-lookup"><span data-stu-id="5d324-451">Yes</span></span>  <br/> | <span data-ttu-id="5d324-p130">Это свойство с несколькими значениями, которое создается и заполняется соединителем партнера. Это свойство имеет `IPM.NOTE.Source.Event`следующий формат. (Это свойство должно начинаться `IPM.NOTE`с; этот формат аналогичен параметру класса `IPM.NOTE.X` Message.) Это свойство содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="5d324-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="5d324-455">`Source`— Указывает источник данных стороннего производителя; Например, Twitter, Facebook или BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="5d324-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="5d324-p131">`Event`— Указывает тип действия, выполненного в источнике данных стороннего производителя, который создал элементы; Например, твит в Twitter или в учетной записи Facebook. События относятся к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="5d324-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="5d324-p132">Одно из целей этого свойства является фильтрация определенных элементов на основе источника данных, в котором был создан элемент, или на основе типа события. Например, при поиске с обнаружением электронных данных вы можете создать поисковый запрос, чтобы найти все твиты, которые были отправлены определенным пользователем.</span><span class="sxs-lookup"><span data-stu-id="5d324-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="5d324-p133">При успешном импорте элементов в почтовые ящики в Office 365, в качестве части HTTP-ответа возвращается уникальный идентификатор. Этот идентификатор называется `x-IngestionCorrelationID`— может использоваться для последующих задач по устранению неполадок, которые являются участниками для сквозного отслеживания элементов. Рекомендуется захватывать эти сведения и заносить их в журнал в соответствии с их окончанием. Ниже приведен пример HTTP-ответа, в котором показан этот идентификатор:</span><span class="sxs-lookup"><span data-stu-id="5d324-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="5d324-p134">С помощью средства "поиск контента" в центре безопасности &amp; и соответствия требованиям Office 365 можно искать элементы, импортированные в почтовые ящики в Office 365 из стороннего источника данных. Чтобы выполнить поиск в этих импортированных элементах, можно использовать следующие пары "свойство: значение сообщения" в поле ключевое слово для поиска контента. .</span><span class="sxs-lookup"><span data-stu-id="5d324-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="5d324-p135">**`kind:externaldata`**— Используйте эту комбинацию свойства и значения для поиска всех сторонних типов данных. Например, чтобы найти элементы, импортированные из стороннего источника данных и содержали слово "contoso" в свойстве subject импортированного элемента, используйте запрос `kind:externaldata AND subject:contoso`ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="5d324-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="5d324-p136">**`itemclass:ipm.externaldata.<third-party data type>`**— Используйте эту комбинацию свойства и значения, чтобы выполнять поиск только по указанному типу сторонних данных. Например, чтобы искать только данные Facebook, содержащие слово "contoso" в свойстве subject, следует использовать запрос `itemclass:ipm.externaldata.Facebook* AND subject:contoso`ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="5d324-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="5d324-471">Полный список значений, которые необходимо использовать для сторонних типов данных для `itemclass` свойства, приведен в разделе [Использование поиска контента для поиска данных сторонних производителей, импортированных в Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="5d324-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="5d324-472">Дополнительные сведения об использовании средства "Поиск контента" и создании поисковых запросов по ключевым словам см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="5d324-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="5d324-473">Поиск контента в Office 365</span><span class="sxs-lookup"><span data-stu-id="5d324-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="5d324-474">Запросы ключевых слов и условия поиска контента</span><span class="sxs-lookup"><span data-stu-id="5d324-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
