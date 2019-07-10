---
title: Как работают безопасные ссылки Office 365 ATP
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: Admin
ms.date: 05/19/2019
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Функция "безопасные ссылки" обеспечивает проверку гиперссылок в документах Office и в сообщениях электронной почты. Прочтите эту статью, чтобы узнать, как работают безопасные ссылки ATP.
ms.openlocfilehash: 7570fd65a9831a6436eec8c402a2bc0c2ae09b40
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2019
ms.locfileid: "35599185"
---
# <a name="how-office-365-atp-safe-links-works"></a><span data-ttu-id="3be76-104">Как работают безопасные ссылки Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="3be76-104">How Office 365 ATP Safe Links works</span></span>
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a><span data-ttu-id="3be76-105">Как безопасные ссылки ATP работают с URL-адресами в электронной почте</span><span class="sxs-lookup"><span data-stu-id="3be76-105">How ATP Safe Links works with URLs in email</span></span>

<span data-ttu-id="3be76-106">На высоком уровне: в этой статье описывается работа защиты [ATP-ссылок](atp-safe-links.md) в адресах электронной почты (размещенной в Office 365, а не в локальной среде).</span><span class="sxs-lookup"><span data-stu-id="3be76-106">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in email (hosted in Office 365, not on-premises):</span></span>
  
1. <span data-ttu-id="3be76-107">Пользователи получают сообщения электронной почты, некоторые из которых содержат URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="3be76-107">People receive email messages, some of which contain URLs.</span></span>
    
2. <span data-ttu-id="3be76-108">Вся электронная почта проходит через Exchange Online Protection, в которой применяются фильтры IP-адресов и конвертов, защита от вредоносных программ на основе подписей, защита от нежелательной почты и фильтры защиты от вредоносных программ.</span><span class="sxs-lookup"><span data-stu-id="3be76-108">All email goes through Exchange Online Protection, where internet protocol (IP) and envelope filters, signature-based malware protection, anti-spam and anti-malware filters are applied.</span></span> 
    
3. <span data-ttu-id="3be76-109">Сообщения электронной почты приходят в папках "Входящие" пользователей.</span><span class="sxs-lookup"><span data-stu-id="3be76-109">Email arrives in people's inboxes.</span></span>
    
4. <span data-ttu-id="3be76-110">Пользователь входит в Office 365 и отправляется в папку "Входящие" электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3be76-110">A user signs in to Office 365, and goes to their email inbox.</span></span>
    
5. <span data-ttu-id="3be76-111">Пользователь открывает сообщение электронной почты и щелкает URL-адрес в сообщении электронной почты.</span><span class="sxs-lookup"><span data-stu-id="3be76-111">The user opens an email message, and clicks on a URL in the email message.</span></span>
    
6. <span data-ttu-id="3be76-112">Функция безопасных ссылок ATP немедленно проверяет URL-адрес перед открытием веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="3be76-112">The ATP Safe Links feature immediately checks the URL before opening the website.</span></span> <span data-ttu-id="3be76-113">URL-адрес идентифицируется как заблокированный, злонамеренный или безопасный.</span><span class="sxs-lookup"><span data-stu-id="3be76-113">The URL is identified as blocked, malicious, or safe.</span></span>
    
    - <span data-ttu-id="3be76-114">Если URL-адрес относится к веб-сайту, который включен в [настраиваемый список URL-адресов "не перезаписывать"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) для политики, которая применяется к пользователю, веб-сайт откроется.</span><span class="sxs-lookup"><span data-stu-id="3be76-114">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, the website opens.</span></span> 
    
    - <span data-ttu-id="3be76-115">Если URL-адрес относится к веб-сайту, который включен в [список пользовательских заблокированных URL-адресов](set-up-a-custom-blocked-urls-list-wtih-atp.md)Организации, откроется [страница](atp-safe-links-warning-pages.md) с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="3be76-115">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="3be76-116">Если URL-адрес относится к веб-сайту, который был определен как вредоносный, откроется [страница](atp-safe-links-warning-pages.md) с предупреждением.</span><span class="sxs-lookup"><span data-stu-id="3be76-116">If the URL is to a website that has been determined to be malicious, a [warning page](atp-safe-links-warning-pages.md) opens.</span></span> 
    
    - <span data-ttu-id="3be76-117">Если URL-адрес помещается в загружаемый файл, а [политики безопасных ссылок ATP](set-up-atp-safe-links-policies.md) в организации настроены на проверку такого содержимого, загружаемый файл проверяется.</span><span class="sxs-lookup"><span data-stu-id="3be76-117">If the URL goes to a downloadable file and your organization's [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such content, the downloadable file is checked.</span></span> 
    
    - <span data-ttu-id="3be76-118">Если URL-адрес определен как безопасный, откроется веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="3be76-118">If the URL is determined to be safe, the website opens.</span></span>
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a><span data-ttu-id="3be76-119">Как безопасные ссылки ATP работают с URL-адресами в документах Office</span><span class="sxs-lookup"><span data-stu-id="3be76-119">How ATP Safe Links works with URLs in Office documents</span></span>

<span data-ttu-id="3be76-120">На высоком уровне ниже показано, как работает защита [ATP для безопасных ссылок](atp-safe-links.md) для URL-адресов в приложениях Office 365 ProPlus (текущие версии Word, Excel и PowerPoint для Windows или Mac, приложения Office на устройствах с iOS или Android, Visio в Windows, OneNote Online и Office). В сети):</span><span class="sxs-lookup"><span data-stu-id="3be76-120">At a high level, here's how [ATP Safe Links](atp-safe-links.md) protection works for URLs in Office 365 ProPlus applications (current versions of Word, Excel, and PowerPoint on Windows or Mac, Office apps on iOS or Android devices, Visio on Windows, OneNote Online, and Office Online):</span></span>
  
1. <span data-ttu-id="3be76-121">Пользователи установили Office 365 профессиональный плюс на своем компьютере, смартфоне или планшете.</span><span class="sxs-lookup"><span data-stu-id="3be76-121">People have installed Office 365 ProPlus on their computer, smartphone, or tablet.</span></span> <span data-ttu-id="3be76-122">(Или в браузере используются Office Online.)</span><span class="sxs-lookup"><span data-stu-id="3be76-122">(Or, they are using Office Online in their browser.)</span></span>
    
2. <span data-ttu-id="3be76-123">Пользователь открывает Word, Excel, PowerPoint или Visio и входит в Office 365 корпоративный, используя рабочую или учебную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="3be76-123">A user opens a Word, Excel, PowerPoint, or Visio, and signs in to Office 365 Enterprise using their work or school account.</span></span> <span data-ttu-id="3be76-124">Документ содержит URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="3be76-124">The document contains URLs.</span></span>
    
3. <span data-ttu-id="3be76-125">Когда пользователь щелкает URL-адрес в документе, эта ссылка проверяется службой "безопасные ссылки ATP".</span><span class="sxs-lookup"><span data-stu-id="3be76-125">When the user clicks on a URL in the document, the link is checked by the ATP Safe Links service.</span></span>
    
      - <span data-ttu-id="3be76-126">Если URL-адрес относится к веб-сайту, который включен в [настраиваемый список URL-адресов "не перезаписывать"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) для политики, которая применяется к пользователю, этот пользователь передается на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="3be76-126">If the URL is to a website that is included in a [custom "Do not rewrite" URLs list](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) for a policy that applies to the user, that user is taken to the website.</span></span> 
    
      - <span data-ttu-id="3be76-127">Если URL-адрес относится к веб-сайту, который включен в [список пользовательских заблокированных URL-адресов](set-up-a-custom-blocked-urls-list-wtih-atp.md)Организации, пользователь переводится на [страницу предупреждения](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="3be76-127">If the URL is to a website that is included in the organization's [custom blocked URLs list](set-up-a-custom-blocked-urls-list-wtih-atp.md), the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
      - <span data-ttu-id="3be76-128">Если URL-адрес относится к веб-сайту, который был определен как вредоносный, пользователь переводится на [страницу предупреждения](atp-safe-links-warning-pages.md).</span><span class="sxs-lookup"><span data-stu-id="3be76-128">If the URL is to a website that has been determined to be malicious, the user is taken to a [warning page](atp-safe-links-warning-pages.md).</span></span>
    
      - <span data-ttu-id="3be76-129">Если URL-адрес помещается в загружаемый файл, а [политики безопасных ссылок ATP](set-up-atp-safe-links-policies.md) настроены на проверку таких загружаемых файлов, то загружаемый файл проверяется.</span><span class="sxs-lookup"><span data-stu-id="3be76-129">If the URL goes to a downloadable file and the [ATP Safe Links policies](set-up-atp-safe-links-policies.md) are configured to scan such downloads, the downloadable file is checked.</span></span> 
    
      - <span data-ttu-id="3be76-130">Если URL-адрес считается безопасным, пользователь передается на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="3be76-130">If the URL is considered safe, the user is taken to the website.</span></span>

