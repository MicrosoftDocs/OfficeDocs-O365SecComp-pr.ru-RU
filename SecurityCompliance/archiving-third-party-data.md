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
ms.openlocfilehash: 7af88338333e90bd208d693fbfd5bb691d44b538
ms.sourcegitcommit: 4c6c937ec51e8b754332e4c1c8d286e73e197e2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/04/2018
ms.locfileid: "23827093"
---
# <a name="archiving-third-party-data-in-office-365"></a><span data-ttu-id="36a8d-105">Архивация сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="36a8d-105">Archiving third-party data in Office 365</span></span>

<span data-ttu-id="36a8d-p102">Office 365 позволяет администраторам импортировать и архивация данных сторонних производителей с платформ, социальные сети, обмен мгновенными сообщениями на разных платформах и платформах документов совместной работы, к почтовым ящикам в организации Office 365. Следующие примеры источников данных сторонних производителей, которые можно импортировать в Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p102">Office 365 lets administrators import and archive third-party data from social media platforms, instant messaging platforms, and document collaboration platforms, to mailboxes in your Office 365 organization. Examples of third-party data sources that you can import to Office 365 include the following:</span></span> 
  
- <span data-ttu-id="36a8d-108">**Социальные** - Twitter, Facebook, LinkedIn и Yammer</span><span class="sxs-lookup"><span data-stu-id="36a8d-108">**Social** - Twitter, Facebook, Yammer, and LinkedIn</span></span> 
    
- <span data-ttu-id="36a8d-109">**Обмен мгновенными сообщениями** — Yahoo Messenger, GoogleTalk и Cisco Jabber</span><span class="sxs-lookup"><span data-stu-id="36a8d-109">**Instant messaging** - Yahoo Messenger, GoogleTalk, and Cisco Jabber</span></span> 
    
- <span data-ttu-id="36a8d-110">**Совместная работа над документами** - поля и общего банка данных</span><span class="sxs-lookup"><span data-stu-id="36a8d-110">**Document collaboration** - Box and DropBox</span></span> 
    
- <span data-ttu-id="36a8d-111">**В различных отраслях** — управление отношениями с клиентами (например, Salesforce задержку) и финансирование (например, Thomson Reuters и Bloomberg)</span><span class="sxs-lookup"><span data-stu-id="36a8d-111">**Vertical industries** - Customer Relationship Management (such as Salesforce Chatter) and Financials (such as Thomson Reuters and Bloomberg)</span></span> 
    
- <span data-ttu-id="36a8d-112">**SMS или текстовых сообщений** - BlackBerry</span><span class="sxs-lookup"><span data-stu-id="36a8d-112">**SMS/text messaging** - BlackBerry</span></span> 
    
<span data-ttu-id="36a8d-p103">После импорта данных сторонних производителей могут применять функции контроля соответствия требованиям Office 365 — например, политики хранения хранение для судебного разбирательства, поиск контента, в архивирование на месте, аудит и Office 365 — для этих данных. Например когда почтовый ящик располагается на хранение для судебного разбирательства, сторонних производителей данные будут сохранены. Можно выполнить поиск данных сторонних производителей с помощью поиска контента. Или можно применить архивации и политики хранения к данным сторонних производителей так же, как и для данных Майкрософт. Одним словом архивирование данных в Office 365 в сторонних производителей могут помочь организации всегда оставаться на соответствующий стандарту государственных организаций и нормативных политик.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p103">After third-party data is imported, you can apply Office 365 compliance features—such as Litigation Hold, Content Search, In-Place Archiving, Auditing, and Office 365 retention policies—to this data. For example, when a mailbox is placed on Litigation Hold, third-party data will be preserved. You can search third-party data by using Content Search. Or you can apply archiving and retention polices to third-party data just like you can for Microsoft data. In short, archiving third-party data in Office 365 can help your organization stay compliant with government and regulatory policies.</span></span>
  
<span data-ttu-id="36a8d-118">Ниже приведен обзор процесса и действия, необходимо использовать для импорта данных сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-118">Here's an overview of the process and the steps necessary to import third-party data to Office 365.</span></span>

[<span data-ttu-id="36a8d-119">Шаг 1. Поиск партнера по работе со сторонними данными</span><span class="sxs-lookup"><span data-stu-id="36a8d-119">Step 1: Find a third-party data partner</span></span>](#step-1-find-a-third-party-data-partner)

[<span data-ttu-id="36a8d-120">Шаг 2. Создание и настройка почтового ящика сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="36a8d-120">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[<span data-ttu-id="36a8d-121">Шаг 3. Настройка поддержки сторонних данных для почтовых ящиков пользователей</span><span class="sxs-lookup"><span data-stu-id="36a8d-121">Step 3: Configure user mailboxes for third-party data</span></span>](#step-3-configure-user-mailboxes-for-third-party-data)

[<span data-ttu-id="36a8d-122">Шаг 4. Предоставление сведений партнеру</span><span class="sxs-lookup"><span data-stu-id="36a8d-122">Step 4: Provide your partner with information</span></span>](#step-4-provide-your-partner-with-information)

[<span data-ttu-id="36a8d-123">Шаг 5: Регистрация соединителя данных сторонних производителей в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="36a8d-123">Step 5: Register the third-party data connector in Azure Active Directory</span></span>](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a><span data-ttu-id="36a8d-124">Как импортировать данные сторонних производителей процесс работы ></span><span class="sxs-lookup"><span data-stu-id="36a8d-124">How the third-party data import process works></span></span>

<span data-ttu-id="36a8d-125">Ниже приведены иллюстрация и описание того, как происходит импорт сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="36a8d-125">The following illustration and description explain how the third-party data import process works.</span></span>
  
![Как происходит импорт сторонних данных](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. <span data-ttu-id="36a8d-127">Клиента для работы с их партнеров вариант, чтобы настроить соединитель, который будет извлечение элементов из источника данных сторонних производителей, а затем импортировать эти элементы в Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-127">Customer works with their partner of choice to configure a connector that will extract items from the third-party data source and then import those items to Office 365.</span></span>
    
2. <span data-ttu-id="36a8d-p104">Partner соединитель подключается к источникам данных сторонних производителей с помощью API сторонних производителей (на основе запланированного или как настроен) и извлекает элементов из источника данных. Partner соединитель преобразует контента элемента в формат сообщения электронной почты. Описание схемы формата сообщения в разделе [Дополнительные сведения](#more-information) .</span><span class="sxs-lookup"><span data-stu-id="36a8d-p104">The partner connector connects to third-party data sources via a third-party API (on a scheduled or as-configured basis) and extracts items from the data source. The partner connector converts the content of an item to an email message format. See the [More information](#more-information) section for a description of the message format schema.</span></span> 
    
3. <span data-ttu-id="36a8d-131">Partner соединитель подключается к службе Azure в Office 365 с помощью веб-служб Exchange (EWS) с помощью известных конечная точка.</span><span class="sxs-lookup"><span data-stu-id="36a8d-131">Partner connector connects to the Azure service in Office 365 by using Exchange Web Service (EWS) via a well-known end point.</span></span>
    
4. <span data-ttu-id="36a8d-p105">Элементы импортируются в почтовый ящик определенного пользователя или общий почтовый ящик для сторонних данных. Элемент импортируется в почтовый ящик определенного пользователя или общий почтовый ящик для сторонних данных, исходя из следующих критериев:</span><span class="sxs-lookup"><span data-stu-id="36a8d-p105">Items are imported into the mailbox of a specific user or into a "catch-all" third-party data mailbox. Whether an item is imported into a specific user mailbox or to the third-party data mailbox is based on the following criteria:</span></span>
    
    <span data-ttu-id="36a8d-p106">**элементы, у которых идентификатор пользователя, который соответствует учетной записи пользователя в Office 365** — Если соединитель партнеров можно сопоставить идентификатор элемента в источнике данных сторонних производителей для конкретного пользователя, который идентификатор в Office 365, элемент копируется в папку **очищаются** в списке пользователя а. Папки восстанавливаемых элементов. Пользователи не могут получить доступ к элементов в папке удаляет. Тем не менее можно использовать средства обнаружения электронных данных в Office 365 для поиска элементов в папке удаляет.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p106">a. **Items that have a user ID that corresponds to an Office 365 user account** - If the partner connector can map the user ID of the item in the third-party data source to a specific user ID in Office 365, the item is copied to the **Purges** folder in the user's Recoverable Items folder. Users can't access items in the Purges folder. However, you can use Office 365 eDiscovery tools to search for items in the Purges folder.</span></span>
    
    <span data-ttu-id="36a8d-p107">б. **элементов, которые не содержат идентификатор пользователя, который соответствует учетной записи пользователя в Office 365** — Если partner соединитель нельзя сопоставить идентификатор элемента для конкретного пользователя, который ID в Office 365, элемент копируется в папку **"Входящие"** почтового ящика данных сторонних производителей. Импорт элементов в папке "Входящие" позволяет или кто-то в вашей организации, чтобы войти в почтовый ящик сторонних производителей для просмотра и управления эти элементы и просматривать, если все настройки должны быть выполнены в конфигурацию соединителя партнера.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p107">b. **Items that don't have a user ID that corresponds to an Office 365 user account** - If the partner connector can't map the user ID of an item to a specific user ID in Office 365, the item is copied to the **Inbox** folder of the third-party data mailbox. Importing items to the inbox allows you or someone in your organization to sign in to the third-party mailbox to view and manage these items, and see if any adjustments need to be made in the partner connector configuration.</span></span>
 
## <a name="step-1-find-a-third-party-data-partner"></a><span data-ttu-id="36a8d-141">Шаг 1. Поиск партнера по работе со сторонними данными</span><span class="sxs-lookup"><span data-stu-id="36a8d-141">Step 1: Find a third-party data partner</span></span>

<span data-ttu-id="36a8d-p108">Основной компонент для архивации данных сторонних производителей в Office 365 поиск и работа с партнера корпорации Майкрософт, который специализируется в записи данных из источника данных сторонних производителей и импорт в Office 365. После импорта данных его можно архивировать и сохраняются вместе с вашей организации и других данных Майкрософт, например электронной почты из Exchange и документов из SharePoint и OneDrive для бизнеса. Партнер создает соединитель, который извлекает данные из источников данных сторонних производителей вашей организации (например, BlackBerry, Facebook, Google +, Thomson Reuters, Twitter и YouTube) и передает эти данные в API Office 365, который импортируется в почтовые ящики Exchange как элементы сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p108">A key component for archiving third-party data in Office 365 is finding and working with a Microsoft partner that specializes in capturing data from a third-party data source and importing it to Office 365. After the data is imported, it can be archived and preserved along with your organization's other Microsoft data, such as email from Exchange and documents from SharePoint and OneDrive for Business. A partner creates a connector that extracts data from your organization's third-party data sources (such as BlackBerry, Facebook, Google+, Thomson Reuters, Twitter, and YouTube) and passes that data to an Office 365 API that imports items to Exchange mailboxes as email messages.</span></span> 
  
<span data-ttu-id="36a8d-145">В следующих разделах перечислены партнеров Майкрософт — и источники данных сторонних производителей, они поддерживают —, участвующие в программе для архивации данных сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-145">The following sections list the Microsoft partners—and the third-party data sources they support—that are participating in the program for archiving third-party data in Office 365.</span></span>

[<span data-ttu-id="36a8d-146">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="36a8d-146">17a-4 LLC</span></span>](#17a-4-llc)
  
[<span data-ttu-id="36a8d-147">Actiance</span><span class="sxs-lookup"><span data-stu-id="36a8d-147">Actiance</span></span>](#actiance)
  
[<span data-ttu-id="36a8d-148">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="36a8d-148">ArchiveSocial</span></span>](#archivesocial)
  
[<span data-ttu-id="36a8d-149">Globanet</span><span class="sxs-lookup"><span data-stu-id="36a8d-149">Globanet</span></span>](#globanet)
  
[<span data-ttu-id="36a8d-150">OpenText</span><span class="sxs-lookup"><span data-stu-id="36a8d-150">OpenText</span></span>](#opentext)
  
[<span data-ttu-id="36a8d-151">Verba</span><span class="sxs-lookup"><span data-stu-id="36a8d-151">Verba</span></span>](#verba)
  
### <a name="17a-4-llc"></a><span data-ttu-id="36a8d-152">17a-4 LLC</span><span class="sxs-lookup"><span data-stu-id="36a8d-152">17a-4 LLC</span></span>

<span data-ttu-id="36a8d-153">17a-4 LLC поддерживает следующие сторонние источники данных:</span><span class="sxs-lookup"><span data-stu-id="36a8d-153">17a-4 LLC supports the following third-party data sources:</span></span>
  
- <span data-ttu-id="36a8d-154">BlackBerry</span><span class="sxs-lookup"><span data-stu-id="36a8d-154">BlackBerry</span></span>
    
- <span data-ttu-id="36a8d-155">потоки данных Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="36a8d-155">Bloomberg Data Streams</span></span>
    
- <span data-ttu-id="36a8d-156">Cisco Jabber;</span><span class="sxs-lookup"><span data-stu-id="36a8d-156">Cisco Jabber</span></span>
    
- <span data-ttu-id="36a8d-157">FactSet</span><span class="sxs-lookup"><span data-stu-id="36a8d-157">FactSet</span></span>
    
- <span data-ttu-id="36a8d-158">HipChat</span><span class="sxs-lookup"><span data-stu-id="36a8d-158">HipChat</span></span>
    
- <span data-ttu-id="36a8d-159">InvestEdge</span><span class="sxs-lookup"><span data-stu-id="36a8d-159">InvestEdge</span></span>
    
- <span data-ttu-id="36a8d-160">LivePerson</span><span class="sxs-lookup"><span data-stu-id="36a8d-160">LivePerson</span></span>
    
- <span data-ttu-id="36a8d-161">
MessageLabs Data Streams;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-161">MessageLabs Data Streams</span></span>
    
- <span data-ttu-id="36a8d-162">OpenText</span><span class="sxs-lookup"><span data-stu-id="36a8d-162">OpenText</span></span>
    
- <span data-ttu-id="36a8d-163">Oracle/ATG Click-to-Call Live Help;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-163">Oracle/ATG 'click-to-call' Live Help</span></span>
    
- <span data-ttu-id="36a8d-164">Pivot IMTRADER;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-164">Pivot IMTRADER</span></span>
    
- <span data-ttu-id="36a8d-165">Microsoft SharePoint</span><span class="sxs-lookup"><span data-stu-id="36a8d-165">Microsoft SharePoint</span></span>
    
- <span data-ttu-id="36a8d-166">MindAlign</span><span class="sxs-lookup"><span data-stu-id="36a8d-166">MindAlign</span></span>
    
- <span data-ttu-id="36a8d-167">Sitrion One (Newsgator);</span><span class="sxs-lookup"><span data-stu-id="36a8d-167">Sitrion One (Newsgator)</span></span>
    
- <span data-ttu-id="36a8d-168">
Skype для бизнеса (Lync/OCS);</span><span class="sxs-lookup"><span data-stu-id="36a8d-168">Skype for Business (Lync/OCS)</span></span>
    
- <span data-ttu-id="36a8d-169">
Skype для бизнеса Online (Lync Online);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-169">Skype for Business Online (Lync Online)</span></span>
    
- <span data-ttu-id="36a8d-170">базы данных SQL;</span><span class="sxs-lookup"><span data-stu-id="36a8d-170">SQL Databases</span></span>
    
- <span data-ttu-id="36a8d-171">
Squawker;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-171">Squawker</span></span>
    
- <span data-ttu-id="36a8d-172">Thomson Reuters Eikon Messenger.
</span><span class="sxs-lookup"><span data-stu-id="36a8d-172">Thomson Reuters Eikon Messenger</span></span>
  
### <a name="actiance"></a><span data-ttu-id="36a8d-173">Actiance</span><span class="sxs-lookup"><span data-stu-id="36a8d-173">Actiance</span></span>

<span data-ttu-id="36a8d-174">[Actiance](https://www.actiance.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-174">[Actiance](https://www.actiance.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="36a8d-175">AIM;</span><span class="sxs-lookup"><span data-stu-id="36a8d-175">AIM</span></span>
    
- <span data-ttu-id="36a8d-176">American Idol;</span><span class="sxs-lookup"><span data-stu-id="36a8d-176">American Idol</span></span>
    
- <span data-ttu-id="36a8d-177">Apple Juice;</span><span class="sxs-lookup"><span data-stu-id="36a8d-177">Apple Juice</span></span>
    
- <span data-ttu-id="36a8d-178">
AOL с клиентом Pivot;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-178">AOL with Pivot client</span></span>
    
- <span data-ttu-id="36a8d-179">Ares;</span><span class="sxs-lookup"><span data-stu-id="36a8d-179">Ares</span></span>
    
- <span data-ttu-id="36a8d-180">Bazaar Voice;</span><span class="sxs-lookup"><span data-stu-id="36a8d-180">Bazaar Voice</span></span>
    
- <span data-ttu-id="36a8d-181">Bear Share;</span><span class="sxs-lookup"><span data-stu-id="36a8d-181">Bear Share</span></span>
    
- <span data-ttu-id="36a8d-182">Bit Torrent;</span><span class="sxs-lookup"><span data-stu-id="36a8d-182">Bit Torrent</span></span>
    
- <span data-ttu-id="36a8d-183">журналы вызовов BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-183">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-184">BlackBerry Messenger (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-184">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-185">PIN-код BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-185">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-186">BlackBerry SMS (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-186">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-187">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-187">Bloomberg Mail</span></span>
    
- <span data-ttu-id="36a8d-188">CellTrust</span><span class="sxs-lookup"><span data-stu-id="36a8d-188">CellTrust</span></span>
    
- <span data-ttu-id="36a8d-189">импорт чата;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-189">Chat Import</span></span>
    
- <span data-ttu-id="36a8d-190">политика и ведение журнала чата в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-190">Chat Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="36a8d-191">Chatter;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-191">Chatter</span></span>
    
- <span data-ttu-id="36a8d-192">Cisco обмена мгновенными Сообщениями &amp; Server сведения о присутствии (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span><span class="sxs-lookup"><span data-stu-id="36a8d-192">Cisco IM &amp; Presence Server (v9.0.1, v9.1, v9.1.1 SU1, v10, v10.5.1 SU1)</span></span>
    
- <span data-ttu-id="36a8d-193">Cisco Unified Presence Server (версии 8.6.3, 8.6.4, 8.6.5);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-193">Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)</span></span>
    
- <span data-ttu-id="36a8d-194">импорт совместной работы;</span><span class="sxs-lookup"><span data-stu-id="36a8d-194">Collaboration Import</span></span>
    
- <span data-ttu-id="36a8d-195">ведение журнала совместной работы в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-195">Collaboration Real Time Logging</span></span>
    
- <span data-ttu-id="36a8d-196">Direct Connect;</span><span class="sxs-lookup"><span data-stu-id="36a8d-196">Direct Connect</span></span>
    
- <span data-ttu-id="36a8d-197">Facebook</span><span class="sxs-lookup"><span data-stu-id="36a8d-197">Facebook</span></span>
    
- <span data-ttu-id="36a8d-198">FactSet</span><span class="sxs-lookup"><span data-stu-id="36a8d-198">FactSet</span></span>
    
- <span data-ttu-id="36a8d-199">FastTrack</span><span class="sxs-lookup"><span data-stu-id="36a8d-199">FastTrack</span></span>
    
- <span data-ttu-id="36a8d-200">Gnutella;</span><span class="sxs-lookup"><span data-stu-id="36a8d-200">Gnutella</span></span>
    
- <span data-ttu-id="36a8d-201">Google+;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-201">Google+</span></span>
    
- <span data-ttu-id="36a8d-202">GoToMyPC</span><span class="sxs-lookup"><span data-stu-id="36a8d-202">GoToMyPC</span></span>
    
- <span data-ttu-id="36a8d-203">Hopster;</span><span class="sxs-lookup"><span data-stu-id="36a8d-203">Hopster</span></span>
    
- <span data-ttu-id="36a8d-204">HubConnex</span><span class="sxs-lookup"><span data-stu-id="36a8d-204">HubConnex</span></span>
    
- <span data-ttu-id="36a8d-205">IBM Connections (версии 3.0.1, 4.0, 4.5, 4.5 CR3, 5);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-205">IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)</span></span>
    
- <span data-ttu-id="36a8d-206">IBM Connections Chat Cloud;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-206">IBM Connections Chat Cloud</span></span>
    
- <span data-ttu-id="36a8d-207">IBM Connections Social Cloud;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-207">IBM Connections Social Cloud</span></span>
    
- <span data-ttu-id="36a8d-208">IBM SameTime Advanced 8.5.2 IFR1;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-208">IBM SameTime Advanced 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="36a8d-209">IBM SameTime Communicate 9.0;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-209">IBM SameTime Communicate 9.0</span></span>
    
- <span data-ttu-id="36a8d-210">IBM SameTime Community (версии 8.0.2, 8.5.1 IFR2, 8.5.2 IFR1, 9.1);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-210">IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)</span></span>
    
- <span data-ttu-id="36a8d-211">IBM SameTime Complete 9.0;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-211">IBM SameTime Complete 9.0</span></span>
    
- <span data-ttu-id="36a8d-212">IBM SameTime Conference 9.0;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-212">IBM SameTime Conference 9.0</span></span>
    
- <span data-ttu-id="36a8d-213">IBM SameTime Meeting 8.5.2 IFR1;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-213">IBM SameTime Meeting 8.5.2 IFR1</span></span>
    
- <span data-ttu-id="36a8d-214">ICE/YellowJacket</span><span class="sxs-lookup"><span data-stu-id="36a8d-214">ICE/YellowJacket</span></span>
    
- <span data-ttu-id="36a8d-215">импорт мгновенных сообщений;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-215">IM Import</span></span>
    
- <span data-ttu-id="36a8d-216">политика и ведение журнала обмена мгновенными сообщениями в реальном времени;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-216">IM Real Time Logging and Policy</span></span>
    
- <span data-ttu-id="36a8d-217">Indii Messenger;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-217">Indii Messenger</span></span>
    
- <span data-ttu-id="36a8d-218">Instant Bloomberg;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-218">Instant Bloomberg</span></span>
    
- <span data-ttu-id="36a8d-219">IRC;</span><span class="sxs-lookup"><span data-stu-id="36a8d-219">IRC</span></span>
    
- <span data-ttu-id="36a8d-220">Jive;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-220">Jive</span></span>
    
- <span data-ttu-id="36a8d-221">Jive 6 Real Time Logging (версии 6, 7);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-221">Jive 6 Real Time Logging (v6, v7)</span></span>
    
- <span data-ttu-id="36a8d-222">импорт Jive;</span><span class="sxs-lookup"><span data-stu-id="36a8d-222">Jive Import</span></span>
    
- <span data-ttu-id="36a8d-223">JXTA;</span><span class="sxs-lookup"><span data-stu-id="36a8d-223">JXTA</span></span>
    
- <span data-ttu-id="36a8d-224">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="36a8d-224">LinkedIn</span></span>
    
- <span data-ttu-id="36a8d-225">
Microsoft Lync (2010, 2013);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-225">Microsoft Lync (2010, 2013)</span></span>
    
- <span data-ttu-id="36a8d-226">MFTP;</span><span class="sxs-lookup"><span data-stu-id="36a8d-226">MFTP</span></span>
    
- <span data-ttu-id="36a8d-227">Microsoft Lync 2013 Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-227">Microsoft Lync 2013 Voice</span></span>
    
- <span data-ttu-id="36a8d-228">Microsoft SharePoint (2010, 2013);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-228">Microsoft SharePoint (2010, 2013)</span></span>
    
- <span data-ttu-id="36a8d-229">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="36a8d-229">Microsoft SharePoint Online</span></span>
    
- <span data-ttu-id="36a8d-230">Microsoft UC (Unified Communications);</span><span class="sxs-lookup"><span data-stu-id="36a8d-230">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="36a8d-231">MindAlign</span><span class="sxs-lookup"><span data-stu-id="36a8d-231">MindAlign</span></span>
    
- <span data-ttu-id="36a8d-232">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="36a8d-232">Mobile Guard</span></span>
    
- <span data-ttu-id="36a8d-233">MSN;</span><span class="sxs-lookup"><span data-stu-id="36a8d-233">MSN</span></span>
    
- <span data-ttu-id="36a8d-234">My Space;</span><span class="sxs-lookup"><span data-stu-id="36a8d-234">My Space</span></span>
    
- <span data-ttu-id="36a8d-235">NEONetwork;</span><span class="sxs-lookup"><span data-stu-id="36a8d-235">NEONetwork</span></span>
    
- <span data-ttu-id="36a8d-236">Office 365 Lync Dedicated;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-236">Office 365 Lync Dedicated</span></span>
    
- <span data-ttu-id="36a8d-237">групповой чат Office 365;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-237">Office 365 Shared IM</span></span>
    
- <span data-ttu-id="36a8d-238">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="36a8d-238">Pinterest</span></span>
    
- <span data-ttu-id="36a8d-239">Pivot;</span><span class="sxs-lookup"><span data-stu-id="36a8d-239">Pivot</span></span>
    
- <span data-ttu-id="36a8d-240">QQ;</span><span class="sxs-lookup"><span data-stu-id="36a8d-240">QQ</span></span>
    
- <span data-ttu-id="36a8d-241">Skype для бизнеса 2015</span><span class="sxs-lookup"><span data-stu-id="36a8d-241">Skype for Business 2015</span></span>
    
- <span data-ttu-id="36a8d-242">SoftEther</span><span class="sxs-lookup"><span data-stu-id="36a8d-242">SoftEther</span></span>
    
- <span data-ttu-id="36a8d-243">Symphony;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-243">Symphony</span></span>
    
- <span data-ttu-id="36a8d-244">Thomson Reuters Eikon;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-244">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="36a8d-245">Thomson Reuters Messenger;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-245">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="36a8d-246">Tor;</span><span class="sxs-lookup"><span data-stu-id="36a8d-246">Tor</span></span>
    
- <span data-ttu-id="36a8d-247">TTT;</span><span class="sxs-lookup"><span data-stu-id="36a8d-247">TTT</span></span>
    
- <span data-ttu-id="36a8d-248">Твиттер</span><span class="sxs-lookup"><span data-stu-id="36a8d-248">Twitter</span></span>
    
- <span data-ttu-id="36a8d-249">WinMX</span><span class="sxs-lookup"><span data-stu-id="36a8d-249">WinMX</span></span>
    
- <span data-ttu-id="36a8d-250">Winny;</span><span class="sxs-lookup"><span data-stu-id="36a8d-250">Winny</span></span>
    
- <span data-ttu-id="36a8d-251">Yahoo;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-251">Yahoo</span></span>
    
- <span data-ttu-id="36a8d-252">Yammer</span><span class="sxs-lookup"><span data-stu-id="36a8d-252">Yammer</span></span>
    
- <span data-ttu-id="36a8d-253">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="36a8d-253">YouTube</span></span>
    
  
### <a name="archivesocial"></a><span data-ttu-id="36a8d-254">ArchiveSocial</span><span class="sxs-lookup"><span data-stu-id="36a8d-254">ArchiveSocial</span></span>

<span data-ttu-id="36a8d-255">[ArchiveSocial](https://www.archivesocial.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-255">[ArchiveSocial ](https://www.archivesocial.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="36a8d-256">Facebook</span><span class="sxs-lookup"><span data-stu-id="36a8d-256">Facebook</span></span>
    
- <span data-ttu-id="36a8d-257">Flickr;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-257">Flickr</span></span>
    
- <span data-ttu-id="36a8d-258">Instagram;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-258">Instagram</span></span>
    
- <span data-ttu-id="36a8d-259">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="36a8d-259">LinkedIn</span></span>
    
- <span data-ttu-id="36a8d-260">Pinterest;</span><span class="sxs-lookup"><span data-stu-id="36a8d-260">Pinterest</span></span>
    
- <span data-ttu-id="36a8d-261">Твиттер</span><span class="sxs-lookup"><span data-stu-id="36a8d-261">Twitter</span></span>
    
- <span data-ttu-id="36a8d-262">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="36a8d-262">YouTube</span></span>
    
- <span data-ttu-id="36a8d-263">Vimeo.</span><span class="sxs-lookup"><span data-stu-id="36a8d-263">Vimeo</span></span>
  
### <a name="globanet"></a><span data-ttu-id="36a8d-264">Globanet</span><span class="sxs-lookup"><span data-stu-id="36a8d-264">Globanet</span></span>

<span data-ttu-id="36a8d-265">[Globanet](https://www.globanet.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-265">[Globanet](https://www.globanet.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="36a8d-266">AOL с клиентом Pivot;</span><span class="sxs-lookup"><span data-stu-id="36a8d-266">AOL with Pivot Client</span></span> 
    
- <span data-ttu-id="36a8d-267">журналы вызовов BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-267">BlackBerry Call Logs (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-268">BlackBerry Messenger (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-268">BlackBerry Messenger (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-269">PIN-код BlackBerry (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-269">BlackBerry PIN (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-270">BlackBerry SMS (версии 5, 10, 12);</span><span class="sxs-lookup"><span data-stu-id="36a8d-270">BlackBerry SMS (v5, v10, v12)</span></span>
    
- <span data-ttu-id="36a8d-271">Bloomberg Chat;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-271">Bloomberg Chat</span></span>
    
- <span data-ttu-id="36a8d-272">Bloomberg Mail;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-272">Bloomberg Mail</span></span>
    
- <span data-ttu-id="36a8d-273">Box;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-273">Box</span></span>
    
- <span data-ttu-id="36a8d-274">CipherCloud для Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="36a8d-274">CipherCloud for Salesforce Chatter</span></span>
    
- <span data-ttu-id="36a8d-275">Cisco обмена мгновенными Сообщениями &amp; Server сведения о присутствии (v11.0 v10 v10.5.1 SU1 v11.5 SU2)</span><span class="sxs-lookup"><span data-stu-id="36a8d-275">Cisco IM &amp; Presence Server (v10, v10.5.1 SU1, v11.0, v11.5 SU2)</span></span>

- <span data-ttu-id="36a8d-276">Cisco Webex групп</span><span class="sxs-lookup"><span data-stu-id="36a8d-276">Cisco Webex Teams</span></span>

- <span data-ttu-id="36a8d-277">Рабочая область Citrix &amp; ShareFile</span><span class="sxs-lookup"><span data-stu-id="36a8d-277">Citrix Workspace &amp; ShareFile</span></span>

- <span data-ttu-id="36a8d-278">CrowdCompass</span><span class="sxs-lookup"><span data-stu-id="36a8d-278">CrowdCompass</span></span>

- <span data-ttu-id="36a8d-279">настраиваемые текстовые файлы с разделителями;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-279">Custom delimited text files</span></span>
    
- <span data-ttu-id="36a8d-280">настраиваемые XML-файлы;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-280">Custom XML files</span></span>
    
- <span data-ttu-id="36a8d-281">Facebook (страницы)</span><span class="sxs-lookup"><span data-stu-id="36a8d-281">Facebook (Pages)</span></span>
    
- <span data-ttu-id="36a8d-282">Factset;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-282">Factset</span></span>
    
- <span data-ttu-id="36a8d-283">FXConnect;</span><span class="sxs-lookup"><span data-stu-id="36a8d-283">FXConnect</span></span>
    
- <span data-ttu-id="36a8d-284">ICE Chat или YellowJacket;</span><span class="sxs-lookup"><span data-stu-id="36a8d-284">ICE Chat/YellowJacket</span></span>
    
- <span data-ttu-id="36a8d-285">Jive;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-285">Jive</span></span>
    
- <span data-ttu-id="36a8d-286">Macgregor XIP;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-286">Macgregor XIP</span></span>

- <span data-ttu-id="36a8d-287">Microsoft Exchange Server</span><span class="sxs-lookup"><span data-stu-id="36a8d-287">Microsoft Exchange Server</span></span>
    
- <span data-ttu-id="36a8d-288">Microsoft OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="36a8d-288">Microsoft OneDrive for Business</span></span>

- <span data-ttu-id="36a8d-289">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="36a8d-289">Microsoft Teams</span></span>
       
- <span data-ttu-id="36a8d-290">Microsoft Yammer;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-290">Microsoft Yammer</span></span>
    
- <span data-ttu-id="36a8d-291">Mobile Guard;</span><span class="sxs-lookup"><span data-stu-id="36a8d-291">Mobile Guard</span></span>
    
- <span data-ttu-id="36a8d-292">Pivot;</span><span class="sxs-lookup"><span data-stu-id="36a8d-292">Pivot</span></span>
    
- <span data-ttu-id="36a8d-293">Salesforce Chatter;</span><span class="sxs-lookup"><span data-stu-id="36a8d-293">Salesforce Chatter</span></span>

- <span data-ttu-id="36a8d-294">Skype для бизнеса Online</span><span class="sxs-lookup"><span data-stu-id="36a8d-294">Skype for Business Online</span></span>
    
- <span data-ttu-id="36a8d-295">Skype для бизнеса, версии от 2007 R2 до 2016 (локальные);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-295">Skype for Business, versions 2007 R2 - 2016 (on-premises)</span></span>
    
- <span data-ttu-id="36a8d-296">Slack Enterprise Grid;</span><span class="sxs-lookup"><span data-stu-id="36a8d-296">Slack Enterprise Grid</span></span>
    
- <span data-ttu-id="36a8d-297">Symphony;</span><span class="sxs-lookup"><span data-stu-id="36a8d-297">Symphony</span></span>
    
- <span data-ttu-id="36a8d-298">Thomson Reuters Eikon;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-298">Thomson Reuters Eikon</span></span>
    
- <span data-ttu-id="36a8d-299">Thomson Reuters Messenger;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-299">Thomson Reuters Messenger</span></span>
    
- <span data-ttu-id="36a8d-300">Thomson Reuters Dealings 3000 или FX Trading;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-300">Thomson Reuters Dealings 3000 / FX Trading</span></span>
    
- <span data-ttu-id="36a8d-301">Твиттер</span><span class="sxs-lookup"><span data-stu-id="36a8d-301">Twitter</span></span>
    
- <span data-ttu-id="36a8d-302">UBS Chat;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-302">UBS Chat</span></span>
    
- <span data-ttu-id="36a8d-303">Youtube (en)</span><span class="sxs-lookup"><span data-stu-id="36a8d-303">YouTube</span></span>
  
### <a name="opentext"></a><span data-ttu-id="36a8d-304">OpenText</span><span class="sxs-lookup"><span data-stu-id="36a8d-304">OpenText</span></span>

<span data-ttu-id="36a8d-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-305">[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="36a8d-306">Axs Encrypted;</span><span class="sxs-lookup"><span data-stu-id="36a8d-306">Axs Encrypted</span></span>
    
- <span data-ttu-id="36a8d-307">Axs Exchange;</span><span class="sxs-lookup"><span data-stu-id="36a8d-307">Axs Exchange</span></span>
    
- <span data-ttu-id="36a8d-308">Axs Local Archive;</span><span class="sxs-lookup"><span data-stu-id="36a8d-308">Axs Local Archive</span></span>
    
- <span data-ttu-id="36a8d-309">Axs PlaceHolder;</span><span class="sxs-lookup"><span data-stu-id="36a8d-309">Axs PlaceHolder</span></span>
    
- <span data-ttu-id="36a8d-310">Axs Signed;</span><span class="sxs-lookup"><span data-stu-id="36a8d-310">Axs Signed</span></span>
    
- <span data-ttu-id="36a8d-311">Bloomberg;</span><span class="sxs-lookup"><span data-stu-id="36a8d-311">Bloomberg</span></span>
    
- <span data-ttu-id="36a8d-312">Thomson Reuters.</span><span class="sxs-lookup"><span data-stu-id="36a8d-312">Thomson Reuters</span></span>
  
### <a name="verba"></a><span data-ttu-id="36a8d-313">Verba</span><span class="sxs-lookup"><span data-stu-id="36a8d-313">Verba</span></span>

<span data-ttu-id="36a8d-314">[Verba](https://www.verba.com) поддерживает следующие источники данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-314">[Verba](https://www.verba.com) supports the following third-party data sources:</span></span> 
  
- <span data-ttu-id="36a8d-315">Avaya Aura Video;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-315">Avaya Aura Video</span></span>
    
- <span data-ttu-id="36a8d-316">Avaya Aura Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-316">Avaya Aura Voice</span></span>
    
- <span data-ttu-id="36a8d-317">Avtec Radio;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-317">Avtec Radio</span></span>
    
- <span data-ttu-id="36a8d-318">Bosch/Telex Radio;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-318">Bosch/Telex Radio</span></span>
    
- <span data-ttu-id="36a8d-319">BroadSoft Video;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-319">BroadSoft Video</span></span>
    
- <span data-ttu-id="36a8d-320">BroadSoft Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-320">BroadSoft Voice</span></span>
    
- <span data-ttu-id="36a8d-321">Centile Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-321">Centile Voice</span></span>
    
- <span data-ttu-id="36a8d-322">Cisco Jabber IM;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-322">Cisco Jabber IM</span></span>
    
- <span data-ttu-id="36a8d-323">Cisco UC Video;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-323">Cisco UC Video</span></span>
    
- <span data-ttu-id="36a8d-324">Cisco UC Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-324">Cisco UC Voice</span></span>
    
- <span data-ttu-id="36a8d-325">Cisco UCCX/UCCE видео</span><span class="sxs-lookup"><span data-stu-id="36a8d-325">Cisco UCCX/UCCE Video</span></span>
    
- <span data-ttu-id="36a8d-326">Cisco UCCX/UCCE голосовой связи</span><span class="sxs-lookup"><span data-stu-id="36a8d-326">Cisco UCCX/UCCE Voice</span></span>
    
- <span data-ttu-id="36a8d-327">ESChat Radio;</span><span class="sxs-lookup"><span data-stu-id="36a8d-327">ESChat Radio</span></span>
    
- <span data-ttu-id="36a8d-328">Geoman Contact Expert;</span><span class="sxs-lookup"><span data-stu-id="36a8d-328">Geoman Contact Expert</span></span>
    
- <span data-ttu-id="36a8d-329">IP Trade Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-329">IP Trade Voice</span></span>
    
- <span data-ttu-id="36a8d-330">Luware LUCS Contact Center;</span><span class="sxs-lookup"><span data-stu-id="36a8d-330">Luware LUCS Contact Center</span></span>
    
- <span data-ttu-id="36a8d-331">Microsoft UC (Unified Communications);</span><span class="sxs-lookup"><span data-stu-id="36a8d-331">Microsoft UC (Unified Communications)</span></span>
    
- <span data-ttu-id="36a8d-332">Mitel MiContact Center для Lync (prairieFyre);
</span><span class="sxs-lookup"><span data-stu-id="36a8d-332">Mitel MiContact Center for Lync (prairieFyre)</span></span>
    
- <span data-ttu-id="36a8d-333">Oracle / Acme Packet Session Border Controller Video;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-333">Oracle / Acme Packet Session Border Controller Video</span></span>
    
- <span data-ttu-id="36a8d-334">Oracle / Acme Packet Session Border Controller Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-334">Oracle / Acme Packet Session Border Controller Voice</span></span>
    
- <span data-ttu-id="36a8d-335">Singtel Mobile Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-335">Singtel Mobile Voice</span></span>
    
- <span data-ttu-id="36a8d-336">SIPREC Video;</span><span class="sxs-lookup"><span data-stu-id="36a8d-336">SIPREC Video</span></span>
    
-  <span data-ttu-id="36a8d-337">SIPREC Voice;</span><span class="sxs-lookup"><span data-stu-id="36a8d-337">SIPREC Voice</span></span> 
    
- <span data-ttu-id="36a8d-338">Skype для бизнеса / Lync IM;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-338">Skype for Business / Lync IM</span></span>
    
- <span data-ttu-id="36a8d-339">Skype для бизнеса / Lync Video;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-339">Skype for Business / Lync Video</span></span>
    
- <span data-ttu-id="36a8d-340">Skype для бизнеса / Lync Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-340">Skype for Business / Lync Voice</span></span>
    
- <span data-ttu-id="36a8d-341">Speakerbus Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-341">Speakerbus Voice</span></span>
    
- <span data-ttu-id="36a8d-342">Standard SIP/H.323 Video;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-342">Standard SIP/H.323 Video</span></span>
    
- <span data-ttu-id="36a8d-343">Standard SIP/H.323 Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-343">Standard SIP/H.323 Voice</span></span>
    
- <span data-ttu-id="36a8d-344">Truphone Voice;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-344">Truphone Voice</span></span>
    
- <span data-ttu-id="36a8d-345">TwistedPair Radio;
</span><span class="sxs-lookup"><span data-stu-id="36a8d-345">TwistedPair Radio</span></span>
    
- <span data-ttu-id="36a8d-346">рабочий стол Windows.
</span><span class="sxs-lookup"><span data-stu-id="36a8d-346">Windows Desktop Computer Screen</span></span>
  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a><span data-ttu-id="36a8d-347">Шаг 2. Создание и настройка почтового ящика сторонних данных в Office 365</span><span class="sxs-lookup"><span data-stu-id="36a8d-347">Step 2: Create and configure a third-party data mailbox in Office 365</span></span>

<span data-ttu-id="36a8d-p109">Далее приведены шаги по созданию и настройке почтового ящика данных сторонних производителей для импорта данных в Office 365. В предыдущем описываются элементы импортируются этого почтового ящика, если partner соединитель нельзя сопоставить идентификатор элемента для учетной записи пользователя в Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p109">Here are the steps for creating and configuring a third-party data mailbox for importing data to Office 365. As previous explained, items are imported to this mailbox if the partner connector can't map the user ID of the item to an Office 365 user account.</span></span>
  
 <span data-ttu-id="36a8d-350">**Выполнить эти задачи в центре администрирования Office 365**</span><span class="sxs-lookup"><span data-stu-id="36a8d-350">**Complete these tasks in the Office 365 admin center**</span></span>
  
1. <span data-ttu-id="36a8d-p110">Создание учетной записи пользователя в Office 365 и назначьте его лицензии Exchange Online (план 2); Просмотрите [Добавить пользователей в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Для помещения почтового ящика на хранение для судебного разбирательства или включение архивного почтового ящика, который имеет квота хранилища неограниченное число требуется лицензия (план 2).</span><span class="sxs-lookup"><span data-stu-id="36a8d-p110">Create a new user account in Office 365 and assign it an Exchange Online Plan 2 license; see [Add users to Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). A Plan 2 license is required to place the mailbox on Litigation Hold or enable an archive mailbox that has an unlimited storage quota.</span></span>
    
2. <span data-ttu-id="36a8d-353">Добавьте учетную запись пользователя для почтового ящика данных сторонних производителей в роль **администратора Exchange** администратора в Office 365; в разделе [Назначение ролей администратора в Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span><span class="sxs-lookup"><span data-stu-id="36a8d-353">Add the user account for the third-party data mailbox to the **Exchange administrator** admin role in Office 365; see [Assign admin roles in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="36a8d-p111">Запишите данные этой учетной записи. Их необходимо предоставить партнеру, как описано в шаге 4.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p111">Write down the credentials for this user account. You need to provide them to your partner, as described in Step 4.</span></span> 
  
 <span data-ttu-id="36a8d-356">**Выполнить эти задачи в центре администрирования Exchange**</span><span class="sxs-lookup"><span data-stu-id="36a8d-356">**Complete these tasks in the Exchange admin center**</span></span>
  
1. <span data-ttu-id="36a8d-p112">Скрыть почтовый ящик сторонних производителей данные из адресной книги и другие списки адресов в организации; в разделе [Управление почтовые ящики пользователей](https://go.microsoft.com/fwlink/p/?LinkId=616058). Кроме того можно выполнить следующую команду PowerShell:</span><span class="sxs-lookup"><span data-stu-id="36a8d-p112">Hide the third-party data mailbox from the address book and other address lists in your organization; see [Manage user mailboxes](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternatively, you can run the following PowerShell command:</span></span>
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. <span data-ttu-id="36a8d-359">Назначьте разрешения **FullAccess** к почтовому ящику данных сторонних производителей, чтобы администраторы или контролеры можно открыть почтовый ящик данных сторонних производителей в клиентском Outlook; [Управление разрешениями для получателей](https://go.microsoft.com/fwlink/p/?LinkId=692104)см.</span><span class="sxs-lookup"><span data-stu-id="36a8d-359">Assign the **FullAccess** permission to the third-party data mailbox so that administrators or compliance officers can open the third-party data mailbox in the Outlook desktop client; see [Manage permissions for recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).</span></span>
    
3. <span data-ttu-id="36a8d-360">Включите следующие связанные с соответствием требованиям Office 365 функции для почтового ящика сторонних производителей данных:</span><span class="sxs-lookup"><span data-stu-id="36a8d-360">Enable the following compliance-related Office 365 features for the third-party data mailbox:</span></span>
    
    - <span data-ttu-id="36a8d-p113">Включение архивного почтового ящика; просмотреть [Enable архивных почтовых ящиков в Office 365 безопасность &amp; центре соответствия требованиям](enable-archive-mailboxes.md) и [Включить неограниченном архивировании в Office 365](enable-unlimited-archiving.md). Это позволит освободить дисковое пространство в основной почтовый ящик, настраивая политики архивирования, который перемещает элементы данных сторонних производителей в архивный почтовый ящик. Это предоставит без ограничений хранилища для данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p113">Enable the archive mailbox; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md). This will let you free-up storage space in the primary mailbox by setting up an archive policy that moves third-party data items to the archive mailbox. This will provide you with unlimited storage for third-party data.</span></span>
    
    - <span data-ttu-id="36a8d-p114">Помещение почтового ящика данных сторонних производителей на хранение для судебного разбирательства. Также можно применить политику хранения Office 365 безопасности Office 365 &amp; центре соответствия требованиям. Размещение этого почтового ящика на удержание хранения данных сторонних элементов (неограниченное время или в течение указанного периода времени) и предотвратить очищаются из почтового ящика. Отображается одно из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="36a8d-p114">Place the third-party data mailbox on Litigation Hold. You can also apply an Office 365 retention policy in the Office 365 Security &amp; Compliance Center. Placing this mailbox on hold will retain third-party data items (indefinitely or for a specified duration) and prevent them from being purged from the mailbox. See one of the following topics:</span></span>
    
      - [<span data-ttu-id="36a8d-368">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="36a8d-368">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [<span data-ttu-id="36a8d-369">Общие сведения о политиках хранения в Office 365</span><span class="sxs-lookup"><span data-stu-id="36a8d-369">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
       
    
    - <span data-ttu-id="36a8d-p115">Включение почтового ящика ведения журнала аудита для владельца, делегат и администрирования доступ к почтовому ящику данных сторонних производителей; в разделе [Включить аудит в Office 365 почтового ящика](enable-mailbox-auditing.md). Это позволит аудита все операции, выполненные любым пользователем, обладающим доступом к почтовому ящику данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p115">Enable mailbox audit logging for owner, delegate, and admin access to the third-party data mailbox; see [Enable mailbox auditing in Office 365](enable-mailbox-auditing.md). This will allow you to audit all activity performed by any user who has access to the third-party data mailbox.</span></span>

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a><span data-ttu-id="36a8d-372">Шаг 3. Настройка поддержки сторонних данных для почтовых ящиков пользователей</span><span class="sxs-lookup"><span data-stu-id="36a8d-372">Step 3: Configure user mailboxes for third-party data</span></span>

<span data-ttu-id="36a8d-p116">Следующим шагом является Настройка почтовых ящиков пользователей для поддержки данных сторонних производителей. Выполните эти задачи с помощью центра администрирования Exchange или с помощью соответствующего командлетов Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p116">The next step is to configure user mailboxes to support third-party data. Complete these tasks by using the Exchange admin center or by using the corresponding Windows PowerShell cmdlets.</span></span>
  
1. <span data-ttu-id="36a8d-375">Включение архивного почтового ящика для каждого пользователя; просмотреть [Enable архивных почтовых ящиков в Office 365 безопасность &amp; центре соответствия требованиям](enable-archive-mailboxes.md) и [Включить неограниченном архивировании в Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="36a8d-375">Enable the archive mailbox for each user; see [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
2. <span data-ttu-id="36a8d-376">Помещение почтовых ящиков пользователей на хранение для судебного разбирательства или применить политику хранения Office 365; отображается одно из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="36a8d-376">Place user mailboxes on Litigation Hold or apply an Office 365 retention policy; see one of the following topics:</span></span> 
    
    - [<span data-ttu-id="36a8d-377">Place a mailbox on Litigation Hold</span><span class="sxs-lookup"><span data-stu-id="36a8d-377">Place a mailbox on Litigation Hold</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [<span data-ttu-id="36a8d-378">Общие сведения о политиках хранения в Office 365</span><span class="sxs-lookup"><span data-stu-id="36a8d-378">Overview of retention policies in Office 365</span></span>](retention-policies.md)
    
    <span data-ttu-id="36a8d-379">Как отмечалось ранее, при помещении почтовых ящиков на хранение можно указать длительность хранения элементов из источника сторонних данных или выбрать бессрочное хранение.</span><span class="sxs-lookup"><span data-stu-id="36a8d-379">As previously stated, when you place mailboxes on hold, you can set a duration for how long to hold items from the third-party data source or you can choose to hold items indefinitely.</span></span>

## <a name="step-4-provide-your-partner-with-information"></a><span data-ttu-id="36a8d-380">Шаг 4. Предоставление сведений партнеру</span><span class="sxs-lookup"><span data-stu-id="36a8d-380">Step 4: Provide your partner with information</span></span>

<span data-ttu-id="36a8d-381">Последний шаг — предоставить партнеру указанные ниже сведения, чтобы он смог настроить соединитель для подключения к организации Office 365 и импорта данных в почтовые ящики пользователей и почтовый ящик сторонних данных.</span><span class="sxs-lookup"><span data-stu-id="36a8d-381">The final step is to provide your partner with the following information so they can configure the connector to connect to your Office 365 organization to import data to user mailboxes and to the third-party data mailbox.</span></span> 
  
- <span data-ttu-id="36a8d-382">Конечная точка, используемый для подключения к службе Azure в Office 365:</span><span class="sxs-lookup"><span data-stu-id="36a8d-382">The endpoint used to connect to the Azure service in Office 365:</span></span>

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- <span data-ttu-id="36a8d-p117">Знак в учетных данных (Office 365 идентификатор пользователя и пароль) для почтового ящика данных сторонних производителей, созданный на шаге 2. Эти учетные данные необходимы, чтобы соединитель партнеров можно получить доступ к и импорт элементов для почтовых ящиков пользователей и почтовых ящиков данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p117">The sign in credentials (Office 365 user ID and password) of the third-party data mailbox that you created in Step 2. These credentials are required so that the partner connector can access and import items to user mailboxes and to the third-party data mailbox.</span></span>
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a><span data-ttu-id="36a8d-385">Шаг 5: Регистрация соединителя данных сторонних производителей в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="36a8d-385">Step 5: Register the third-party data connector in Azure Active Directory</span></span>

<span data-ttu-id="36a8d-p118">Запуск 30 сентября 2018, Azure службы в Office 365 начинаются с использованием современных проверки подлинности в Exchange Online для проверки подлинности соединители данных сторонних производителей, которые пытаются подключиться к своей организации Office 365 для импорта данных. Причиной данного изменения является, современный проверку подлинности обеспечивает более высокий уровень безопасности, чем текущий метод, который был основан на соединителях разрабатывает сторонних производителей, которые используют уже было сказано конечной точки для подключения к службе Azure.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p118">Starting September 30, 2018, the Azure service in Office 365 will begin using modern authentication in Exchange Online to authenticate third-party data connectors that attempt to connect to your Office 365 organization to import data. The reason for this change is that modern authentication provides more security than the current method, which was based on whitelisting third-party connectors that use the previously described endpoint to connect to the Azure service.</span></span>

<span data-ttu-id="36a8d-p119">Чтобы включить соединителя сторонних производителей данные для подключения к Office 365 с помощью метода new современных проверки подлинности, администратора в организации Office 365 необходимо соглашаетесь Чтобы зарегистрировать соединитель в качестве доверенной службы приложения в Azure Active Directory. Это делается путем принятия запроса разрешений, чтобы разрешить соединитель для доступа к данным вашей организации в Azure Active Directory. После принятия этого запроса добавляется в качестве приложения предприятия для Azure Active Directory и представленные в виде участников службы соединителя данных сторонних производителей. Для получения дополнительных сведений процесс подтверждения видеть [Разрешения администратора клиента](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span><span class="sxs-lookup"><span data-stu-id="36a8d-p119">To enable a third-party data connector to connect to Office 365 using the new modern authentication method, an administrator in your Office 365 organization must consent to register the connector as a trusted service application in Azure Active Directory. This is done by accepting a permissions request to allow the connector to access your organization's data in Azure Active Directory. After you accept this request, the third-party data connector is added as an enterprise application to Azure Active Directory and represented as a service principal. For more information the consent process, see  [Tenant Admin Consent](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).</span></span>

<span data-ttu-id="36a8d-392">Далее приведены шаги для доступа и принять запрос, чтобы зарегистрировать соединитель в:</span><span class="sxs-lookup"><span data-stu-id="36a8d-392">Here are the steps to access and accept the request to register the connector:</span></span>

1. <span data-ttu-id="36a8d-393">На [этой странице](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) и вход с использованием учетных данных из глобального администратора Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-393">Go to [this page](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) and sign in using the credentials of an Office 365 global administrator.</span></span><br/><br/><span data-ttu-id="36a8d-p120">Отображается диалоговое окно следующие. Можно развернуть расположенных для просмотра разрешений, которые будут назначены для соединителя.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p120">The following dialog box is displayed. You can expand the carets to review the permissions that will be assigned to the connector.</span></span><br/><br/><span data-ttu-id="36a8d-396">![Отображается диалоговое окно запроса разрешения](media/O365_ThirdPartyDataConnector_OptIn1.png)</span><span class="sxs-lookup"><span data-stu-id="36a8d-396">![The permissions request dialog is displayed](media/O365_ThirdPartyDataConnector_OptIn1.png)</span></span>
2. <span data-ttu-id="36a8d-397">Нажмите кнопку **принять**.</span><span class="sxs-lookup"><span data-stu-id="36a8d-397">Click **Accept**.</span></span>

<span data-ttu-id="36a8d-p121">После принятия запроса отображается [Azure портала](https://portal.azure.com) . Чтобы просмотреть список приложений для вашей организации, выберите **Azure Active Directory** > **корпоративных приложений**. Соединитель сторонних производителей данные Office 365 указана на blade **корпоративных приложений** .</span><span class="sxs-lookup"><span data-stu-id="36a8d-p121">After you accept the request, the [Azure portal](https://portal.azure.com) is displayed. To view the list of applications for your organization, click **Azure Active Directory** > **Enterprise applications**. The Office 365 third-party data connector is listed on the **Enterprise applications** blade.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36a8d-p122">После 30 сентября 2018 сторонних производителей данных больше не импортироваться в почтовых ящиков в организации при не регистрация соединителя данных сторонних производителей в Azure Active Directory. Примечание существующих соединителей сторонних производителей данных (которые были созданы до 30 сентября 2018) также должны быть зарегистрированы в Azure Active Directory, выполнив процедуру, описанную в шаге 5.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p122">After September 30, 2018, third-party data will no longer be imported into mailboxes in your organization if you don't register a third-party data connector in Azure Active Directory. Note existing third-party data connectors (those created before September 30, 2018) must also be registered in Azure Active Directory by following the procedure in Step 5.</span></span>

### <a name="revoking-consent-for-a-third-party-data-connector"></a><span data-ttu-id="36a8d-403">Отмена разрешения для соединителя данных сторонних производителей</span><span class="sxs-lookup"><span data-stu-id="36a8d-403">Revoking consent for a third-party data connector</span></span>

<span data-ttu-id="36a8d-p123">После согласия вашей организации для запроса разрешений, чтобы зарегистрировать соединитель данных сторонних производителей в Azure Active Directory вашей организации можно отозвать этого разрешения в любое время. Тем не менее отзыва разрешения для соединителя означает, что в Office 365 больше не требуется импортировать данные из источника данных сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p123">After your organization consents to the permissions request to register a third-party data connector in Azure Active Directory, your organization can revoke that consent at any time. However, revoking the consent for a connector will mean that data from the third-party data source will no longer be imported into Office 365.</span></span>

<span data-ttu-id="36a8d-p124">Чтобы отменить разрешения для соединителя данных сторонних производителей, можно удалить приложения (при удалении соответствующих участников-служб) из Azure Active Directory с помощью blade **корпоративных приложений** на портале Azure или с помощью [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) в Office 365 PowerShell. Также можно использовать командлет [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) в Windows Azure Active Directory PowerShell.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p124">To revoke consent for a third-party data connector, you can delete the application (by deleting the corresponding service principal) from Azure Active Directory using the **Enterprise applications** blade in the Azure portal, or by using the [Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. You can also use the [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) cmdlet in Azure Active Directory PowerShell.</span></span>
  
## <a name="more-information"></a><span data-ttu-id="36a8d-408">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="36a8d-408">More information</span></span>

- <span data-ttu-id="36a8d-p125">В предыдущем описываются элементы из данных сторонних производителей, которые источники импортируются в почтовые ящики Exchange как сообщения электронной почты. Соединитель партнеров импортирует элемента, с помощью схемы, необходимые для Office 365 API. В следующей таблице представлены свойства сообщения элемента из источника данных сторонних производителей после импорта в почтовый ящик Exchange, как сообщения электронной почты. В таблице также указывается, если свойство сообщения является обязательным. Обязательные свойства должны быть заполнены. Если элемент отсутствует обязательное свойство, он не будет импортирован Office 365. Процесс импорта возвращает сообщение об ошибке, объясняющее почему элемента не были импортированы, а какие свойства отсутствует.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p125">As previous explained, items from third-party data sources are imported to Exchange mailboxes as email messages. The partner connector imports the item using a schema required by the Office 365 API. The following table describes the message properties of an item from a third-party data source after it's imported to an Exchange mailbox as an email message. The table also indicates if the message property is mandatory. Mandatory properties must be populated. If an item is missing a mandatory property, it won't be imported to Office 365. The import process will return an error message explaining why an item wasn't imported and which property is missing.</span></span>
    
    |<span data-ttu-id="36a8d-416">**Свойство сообщения**</span><span class="sxs-lookup"><span data-stu-id="36a8d-416">**Message property**</span></span>|<span data-ttu-id="36a8d-417">**Обязательный?**</span><span class="sxs-lookup"><span data-stu-id="36a8d-417">**Mandatory?**</span></span>|<span data-ttu-id="36a8d-418">**Описание**</span><span class="sxs-lookup"><span data-stu-id="36a8d-418">**Description**</span></span>|<span data-ttu-id="36a8d-419">**Пример значения**</span><span class="sxs-lookup"><span data-stu-id="36a8d-419">**Example value**</span></span>|
    |:-----|:-----|:-----|:-----|
    |<span data-ttu-id="36a8d-420">**FROM**</span><span class="sxs-lookup"><span data-stu-id="36a8d-420">**FROM**</span></span> <br/> |<span data-ttu-id="36a8d-421">Да</span><span class="sxs-lookup"><span data-stu-id="36a8d-421">Yes</span></span>  <br/> |<span data-ttu-id="36a8d-p126">Пользователь, который изначально создать или отправить элемента в источнике данных сторонних производителей. Partner соединитель пытается сопоставить идентификатор пользователя из исходного элемента (например, маркер Twitter) для учетной записи пользователя в Office 365 для всех участников (пользователей в полях FROM и TO). Копия сообщения будут импортированы в почтовый ящик все остальные. Если ни один из участников из элемента может быть сопоставлен учетной записи пользователя в Office 365, элемент будет импортирован в почтовый ящик архивации сторонних производителей в Office 365.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p126">The user who originally created or sent the item in the third-party data source. The partner connector will attempt to map the user ID from the source item (for example a Twitter handle) to an Office 365 user account for all participants (users in the FROM and TO fields). A copy of the message will be imported to the mailbox of every participant. If none of the participants from the item can be mapped to an Office 365 user account, the item will be imported to the third-party archiving mailbox in Office 365.  </span></span><br/> <br/> <span data-ttu-id="36a8d-p127">Участник, который идентифицируется как отправителя элемента должны иметь активного хранилища почтовых ящиков в организации Office 365, импортируемый элемент в. Если отправитель не имеет активных почтовых ящиков, возвращается следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="36a8d-p127">The participant who's identified as the sender of the item must have an active mailbox in the Office 365 organization that the item is being imported to. If the sender doesn't have an active mailbox, the following error is returned:</span></span><br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |<span data-ttu-id="36a8d-428">**TO**</span><span class="sxs-lookup"><span data-stu-id="36a8d-428">**TO**</span></span> <br/> |<span data-ttu-id="36a8d-429">Да</span><span class="sxs-lookup"><span data-stu-id="36a8d-429">Yes</span></span>  <br/> |<span data-ttu-id="36a8d-430">Пользователь, получивший элемент, если это применимо к элементу в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="36a8d-430">The user who received an item, if applicable for an item in the data source.</span></span>  <br/> | `bob@contoso.com` <br/> |
    |<span data-ttu-id="36a8d-431">**SUBJECT**</span><span class="sxs-lookup"><span data-stu-id="36a8d-431">**SUBJECT**</span></span> <br/> |<span data-ttu-id="36a8d-432">Нет</span><span class="sxs-lookup"><span data-stu-id="36a8d-432">No</span></span>  <br/> |<span data-ttu-id="36a8d-433">Тема исходного элемента.</span><span class="sxs-lookup"><span data-stu-id="36a8d-433">The subject from the source item.</span></span>  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |<span data-ttu-id="36a8d-434">**ДАТА**</span><span class="sxs-lookup"><span data-stu-id="36a8d-434">**DATE**</span></span> <br/> |<span data-ttu-id="36a8d-435">Да</span><span class="sxs-lookup"><span data-stu-id="36a8d-435">Yes</span></span>  <br/> |<span data-ttu-id="36a8d-436">Дата создания или публикации элемента в источнике данных клиента, например дата отправки сообщения в Твиттере.</span><span class="sxs-lookup"><span data-stu-id="36a8d-436">The date the item was originally created or posted in the customer data source; for example, that date when a Twitter message was tweeted.</span></span>  <br/> | `01 NOV 2015` <br/> |
    |<span data-ttu-id="36a8d-437">**BODY**</span><span class="sxs-lookup"><span data-stu-id="36a8d-437">**BODY**</span></span> <br/> |<span data-ttu-id="36a8d-438">Нет</span><span class="sxs-lookup"><span data-stu-id="36a8d-438">No</span></span>  <br/> |<span data-ttu-id="36a8d-p128">Содержимое сообщения или post. Для некоторых источников данных содержимое этого свойства может быть таким же, как содержимое для свойства **ТЕМЫ** . Во время импорта partner соединитель будет пытаться Ведение корректном из источника контента можно. Если это возможно файлов, рисунков или другого контента из текста элемента источника включен в это свойство. В противном случае контент из исходного элемента включен в свойстве **ВЛОЖЕНИЯ** . Содержимое этого свойства будет зависят от соединителя партнеров и возможность платформы источника.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p128">The contents of the message or post. For some data sources, the contents of this property could be the same as the content for the **SUBJECT** property. During the import process, the partner connector will attempt to maintain full fidelity from the content source as possible. If possible files, graphics, or other content from the body of the source item is included in this property. Otherwise, content from the source item is included in the **ATTACHMENT** property. The contents of this property will depend on the partner connector and on the capability of the source platform.  </span></span><br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |<span data-ttu-id="36a8d-445">**ATTACHMENT**</span><span class="sxs-lookup"><span data-stu-id="36a8d-445">**ATTACHMENT**</span></span> <br/> |<span data-ttu-id="36a8d-446">Нет</span><span class="sxs-lookup"><span data-stu-id="36a8d-446">No</span></span>  <br/> |<span data-ttu-id="36a8d-p129">Если элемент в источнике данных (например, tweet в Twitter или сеанс обмена мгновенными сообщениями) имеет вложенный файл или включить изображения, партнера подключение будет первая попытка для включения вложений в свойство **BODY** . Если, который невозможно, то он добавляется в ** ВЛОЖЕНИЯ ** свойство. Другие вложения примеры мне нравится в Facebook, метаданные из источника контента и ответа на сообщение или post.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p129">If an item in the data source (such as a tweet in Twitter or an instant messaging conversation) has an attached file or include images, the partner connect will first attempt to include attachments in the **BODY** property. If that isn't possible, then it's added to the ** ATTACHMENT ** property. Other examples of attachments include Likes in Facebook, metadata from the content source, and responses to a message or post.  </span></span><br/> | `image.gif` <br/> |
    |<span data-ttu-id="36a8d-450">**MESSAGECLASS**</span><span class="sxs-lookup"><span data-stu-id="36a8d-450">**MESSAGECLASS**</span></span> <br/> |<span data-ttu-id="36a8d-451">Да</span><span class="sxs-lookup"><span data-stu-id="36a8d-451">Yes</span></span>  <br/> | <span data-ttu-id="36a8d-p130">Это свойство Многозначный, которое созданы и заполнены соединителем партнера. Формат этого свойства — это `IPM.NOTE.Source.Event`. (Это свойство должен начинаться с `IPM.NOTE`; в этом формате похожего для `IPM.NOTE.X` класс сообщения.) Это свойство содержит следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="36a8d-p130">This is a multi-value property, which is created and populated by partner connector. The format of this property is  `IPM.NOTE.Source.Event`. (This property must begin with  `IPM.NOTE`; this format is similar to the one for the  `IPM.NOTE.X` message class.) This property includes the following information:  </span></span><br/><br/><span data-ttu-id="36a8d-455">`Source`— Определяет источник данных сторонних производителей; Например Twitter Facebook и BlackBerry.</span><span class="sxs-lookup"><span data-stu-id="36a8d-455">`Source` - Indicates the third-party data source; for example, Twitter, Facebook, or BlackBerry.</span></span>  <br/> <br/>  <span data-ttu-id="36a8d-p131">`Event`— Определяет тип действия, выполняемого в источнике данных сторонних производителей, на котором элементов; Например tweet в Twitter или сообщение в сети Facebook. События относятся к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p131">`Event` - Indicates the type of activity that was performed in the third-party data source that produced the items; for example, a tweet in Twitter or a post in Facebook. Events are specific to the data source.  </span></span><br/> <br/>  <span data-ttu-id="36a8d-p132">Один это свойство предназначено для фильтрации определенных элементов на основе источника данных, где произошла элемента или на основе типа события. Например поиска обнаружения электронных данных можно создать запрос поиска, чтобы найти все tweets, разнесенных по определенного пользователя.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p132">One purpose of this property is to filter specific items based on the data source where an item originated or based on the type of event. For example, in an eDiscovery search you could create a search query to find all the tweets that were posted by a specific user.  </span></span><br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- <span data-ttu-id="36a8d-p133">После успешного импорта элементов для почтовых ящиков в Office 365 уникальный идентификатор возвращается вызывающему как часть HTTP-ответа. Этот идентификатор — вызов `x-IngestionCorrelationID`— можно использовать для последующих в целях устранения неполадок с партнерами для отслеживания начала до конца элементов. Рекомендуется, что партнеры эти сведения и войдите соответствующим образом по завершении своей работы. Ниже приведен пример из HTTP-ответа, отражающая этот идентификатор:</span><span class="sxs-lookup"><span data-stu-id="36a8d-p133">When items are successfully imported to mailboxes in Office 365, a unique identifier is returned back to the caller as part of the HTTP response. This identifier—called  `x-IngestionCorrelationID`—can be used for subsequent troubleshooting purposes by partners for end-to-end tracking of items. It's recommended that partners capture this information and log it accordingly at their end. Here's an example of an HTTP response showing this identifier:</span></span>

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- <span data-ttu-id="36a8d-p134">Можно использовать средство поиска контента в Office 365 безопасность &amp; центре соответствия требованиям для поиска элементов, которые были импортированы из источника данных сторонних производителей для почтовых ящиков в Office 365. Для поиска специально для этих импортированных элементов, можно использовать следующие значения свойства пары сообщение в поле ключевое слово для поиска контента. .</span><span class="sxs-lookup"><span data-stu-id="36a8d-p134">You can use the Content Search tool in the Office 365 Security &amp; Compliance Center to search for items that were imported to mailboxes in Office 365 from a third-party data source. To search specifically for these imported items, you can use the following message property-value pairs in the keyword box for a Content Search. .</span></span> 
    
  - <span data-ttu-id="36a8d-p135">**`kind:externaldata`**-Используется Эта пара значение свойства для поиска всех типов данных сторонних производителей. Например, для поиска элементов, которые были импортированы из источника данных сторонних производителей и содержится слово «contoso» в свойстве тема импортированного элемента, используется ключевое слово запроса `kind:externaldata AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p135">**`kind:externaldata`** - Use this property-value pair to search all third-party data types. For example, to search for items that were imported from a third-party data source and contained the word "contoso" in the Subject property of the imported item, you would use the keyword query  `kind:externaldata AND subject:contoso`.</span></span>
    
  - <span data-ttu-id="36a8d-p136">**`itemclass:ipm.externaldata.<third-party data type>`**-Используйте это значение свойства пары только поиска укажите тип данных сторонних производителей. Например, для поиска только данные Facebook (en), содержащий слово «contoso» в свойстве темы, используется запроса ключевого слова `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span><span class="sxs-lookup"><span data-stu-id="36a8d-p136">**`itemclass:ipm.externaldata.<third-party data type>`** - Use this property-value pair to only search a specify type of third-party data. For example, to only search Facebook data that contains the word "contoso" in the Subject property, you would use the keyword query  `itemclass:ipm.externaldata.Facebook* AND subject:contoso`.</span></span> 

  <span data-ttu-id="36a8d-471">Полный список значений, используемых для типов данных сторонних производителей для `itemclass` свойства, видеть [Используйте поиска контента для поиска данных сторонних производителей, которая была импортирована в Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span><span class="sxs-lookup"><span data-stu-id="36a8d-471">For a complete list of values to use for third-party data types for the  `itemclass` property, see [Use Content Search to search third-party data that was imported to Office 365](use-content-search-to-search-third-party-data-that-was-imported.md)</span></span>
    
   <span data-ttu-id="36a8d-472">Дополнительные сведения об использовании средства "Поиск контента" и создании поисковых запросов по ключевым словам см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="36a8d-472">For more information about using Content Search and creating keyword search queries, see:</span></span>
    
  - [<span data-ttu-id="36a8d-473">Поиск контента в Office 365</span><span class="sxs-lookup"><span data-stu-id="36a8d-473">Content Search in Office 365</span></span>](content-search.md)
    
  - [<span data-ttu-id="36a8d-474">Запросы ключевых слов и условия поиска контента</span><span class="sxs-lookup"><span data-stu-id="36a8d-474">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
 
