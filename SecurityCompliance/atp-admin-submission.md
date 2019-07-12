---
title: Отправки администраторов в Office 365 ATP
ms.author: brwilcox
author: briwilcox
manager: dansimp
ms.date: 07/09/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Сведения о том, как отсылать потенциально опасные сообщения, URL-адреса и файлы в корпорацию Майкрософт.
ms.openlocfilehash: 6f7ea63cae4d7cafb0d1386b29d99101d290ef30
ms.sourcegitcommit: 9e2df36b05a2c93ce2629a7a5eda8f44159d114d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2019
ms.locfileid: "35632229"
---
# <a name="admin-submissions-in-office-365-atp"></a><span data-ttu-id="70831-103">Отправки администраторов в Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="70831-103">Admin submissions in Office 365 ATP</span></span>

<span data-ttu-id="70831-104">Теперь администраторы могут отправлять сообщения электронной почты с помощью файлов или сетевых ИДЕНТИФИКАТОРов сообщений, URL-адресов и файлов для сканирования корпорацией Майкрософт в Office 365.</span><span class="sxs-lookup"><span data-stu-id="70831-104">Admins can now send emails by using file or network message ID, URLs, and files for scanning by Microsoft in Office 365.</span></span> <span data-ttu-id="70831-105">В разделе обновленные отправки по-прежнему содержатся сообщения о пользователях.</span><span class="sxs-lookup"><span data-stu-id="70831-105">The updated submissions section still includes user reported messages.</span></span> 

<span data-ttu-id="70831-106">При отсылке сообщения электронной почты вы получите сведения о политиках, которые могут разрешить входящую электронную почту в клиент, а также о том, как все URL-адреса и вложения в почте.</span><span class="sxs-lookup"><span data-stu-id="70831-106">When you submit an email, you will get information about any policies that may have allowed the incoming email into your tenant, as well as examination of any URLs and attachments in the mail.</span></span> <span data-ttu-id="70831-107">Политики, которые могут разрешить почту, включают список надежных отправителей отдельного пользователя, а также политики уровня клиента, такие как правила ETR.</span><span class="sxs-lookup"><span data-stu-id="70831-107">Policies that may have allowed a mail include an individual user's safe sender list as well as tenant level policies such as ETR rules.</span></span> 


## <a name="how-to-submit-content"></a><span data-ttu-id="70831-108">Способы отсылки контента</span><span class="sxs-lookup"><span data-stu-id="70831-108">How to submit content</span></span>

<span data-ttu-id="70831-109">Чтобы отправить контент в корпорацию Майкрософт, нажмите кнопку **создать** отправку в верхней левой части страницы отправки.</span><span class="sxs-lookup"><span data-stu-id="70831-109">To submit content to Microsoft click the **New submission** button in the top left hand side of the submissions page.</span></span> <span data-ttu-id="70831-110">Откроется всплывающее окно с правой стороны страницы с возможностью отправки сообщения электронной почты, URL-адреса или файла.</span><span class="sxs-lookup"><span data-stu-id="70831-110">A flyout on the right side of the page appears with the option to submit either an email, URL, or file.</span></span> 

### <a name="email"></a><span data-ttu-id="70831-111">Email</span><span class="sxs-lookup"><span data-stu-id="70831-111">Email</span></span>
![Пример отправки электронной почты](media/submission-flyout-email.PNG)
1. <span data-ttu-id="70831-113">Чтобы отправить сообщение электронной почты, выберите пункт **Электронная почта** и укажите идентификатор почтового **сообщения** или отправьте файл электронной почты.</span><span class="sxs-lookup"><span data-stu-id="70831-113">To submit an email, select **email** and specify the email **network message ID** or upload the email file.</span></span> 

2. <span data-ttu-id="70831-114">Укажите получателей, для которых требуется выполнить проверку политики.</span><span class="sxs-lookup"><span data-stu-id="70831-114">Specify the recipient(s) that you would like to run the policy check against.</span></span> <span data-ttu-id="70831-115">Проверка политики определяет, пропускается ли сканирование сообщений электронной почты в соответствии с политиками уровня пользователя или клиента.</span><span class="sxs-lookup"><span data-stu-id="70831-115">The policy check will determine if the email bypassed scanning due to user or tenant level policies.</span></span> 

3. <span data-ttu-id="70831-116">Укажите, следует ли блокировать сообщение электронной почты.</span><span class="sxs-lookup"><span data-stu-id="70831-116">Specify if the email should have been blocked or not.</span></span> <span data-ttu-id="70831-117">Если сообщение должно быть заблокировано, укажите, должно ли оно быть заблокировано как спам, фишинг или вредоносная программа.</span><span class="sxs-lookup"><span data-stu-id="70831-117">If the email should have been blocked, specify if it should have been blocked as Spam, Phishing, or Malware.</span></span> <span data-ttu-id="70831-118">Если вы не знаете, какой тип может быть выбран, используйте наилучшее.</span><span class="sxs-lookup"><span data-stu-id="70831-118">If you are not sure what type it might be, use your best judgement.</span></span>  

* <span data-ttu-id="70831-119">Если фильтр обходится из-за политик при отправке, вы увидите сведения об этой политике.</span><span class="sxs-lookup"><span data-stu-id="70831-119">If the filter was bypassed due to policies upon submission, you'll see information about that policy.</span></span>

* <span data-ttu-id="70831-120">Если фильтр не обходится из-за одной или нескольких политик, сканирование будет завершено через несколько минут.</span><span class="sxs-lookup"><span data-stu-id="70831-120">If the filter was not bypassed due to one or more policies, the scan will complete in several minutes.</span></span> <span data-ttu-id="70831-121">Вы увидите дополнительные сведения об отправке, щелкнув ссылку состояние.</span><span class="sxs-lookup"><span data-stu-id="70831-121">You'll see additional information about the submission by clicking on the status link.</span></span> <span data-ttu-id="70831-122">К ним относятся результаты проверки политики и вредоносности повторного сканирования.</span><span class="sxs-lookup"><span data-stu-id="70831-122">This includes the results of the policy check and the rescan verdict.</span></span> <span data-ttu-id="70831-123">Примечание Это не приводит к повторному выполнению электронной почты через стек полного фильтра Office 365 ATP, но выполняет частичное повторное сканирование, основанное на определенных атрибутах почты, URL-адреса или файла.</span><span class="sxs-lookup"><span data-stu-id="70831-123">Note this does not run the email through the Office 365 ATP full filtering stack again but runs a partial rescan based on certain attributes of the mail, URL, or file.</span></span> 

4. <span data-ttu-id="70831-124">Нажмите кнопку " **послать** ".</span><span class="sxs-lookup"><span data-stu-id="70831-124">Click the **Submit** button.</span></span>

### <a name="url"></a><span data-ttu-id="70831-125">URL-адрес</span><span class="sxs-lookup"><span data-stu-id="70831-125">URL</span></span>
![Пример отправки электронной почты](media/submission-url-flyout.png)
1. <span data-ttu-id="70831-127">Чтобы добавить URL-адрес, выберите **URL-адрес** из всплывающего меню.</span><span class="sxs-lookup"><span data-stu-id="70831-127">To submit a URL select **URL** from the flyout.</span></span> <span data-ttu-id="70831-128">Введите полный URL-адрес, включая протокол (**https://**).</span><span class="sxs-lookup"><span data-stu-id="70831-128">Type in the full URL including the protocol (**https://**).</span></span> 

* <span data-ttu-id="70831-129">Если вы выбрали **фильтрацию**, укажите, является ли URL-адрес фишингом или вредоносным по.</span><span class="sxs-lookup"><span data-stu-id="70831-129">If you selected **Should have been filtered**, specify if the URL is phishing or malware.</span></span>

2. <span data-ttu-id="70831-130">Нажмите кнопку " **послать** ".</span><span class="sxs-lookup"><span data-stu-id="70831-130">Click the **Submit** button.</span></span> 


### <a name="file"></a><span data-ttu-id="70831-131">Файл</span><span class="sxs-lookup"><span data-stu-id="70831-131">File</span></span>
![Пример отправки электронной почты](media/submission-file-flyout.PNG)
1. <span data-ttu-id="70831-133">Чтобы отправить файл, выберите **файл** из всплывающего меню и отправьте файл, который требуется проверить.</span><span class="sxs-lookup"><span data-stu-id="70831-133">To submit a file select **File** from the flyout and upload the file you would like to scan.</span></span> 

2. <span data-ttu-id="70831-134">Нажмите кнопку " **послать** ".</span><span class="sxs-lookup"><span data-stu-id="70831-134">Click the **Submit** button.</span></span>


## <a name="related-topics"></a><span data-ttu-id="70831-135">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="70831-135">Related topics</span></span>

[<span data-ttu-id="70831-136">Office 365 Advanced Threat protection (план 2)</span><span class="sxs-lookup"><span data-stu-id="70831-136">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="70831-137">Защита от угроз в Office 365</span><span class="sxs-lookup"><span data-stu-id="70831-137">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="70831-138">Просмотр отчетов для Office 365 Advanced Threat protection</span><span class="sxs-lookup"><span data-stu-id="70831-138">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

