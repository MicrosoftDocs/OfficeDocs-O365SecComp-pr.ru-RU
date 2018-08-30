---
title: Установка надстройки контроля для классической версии Outlook
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/19/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
- ZOL160
ms.assetid: 6c5620e6-aba3-4910-8f3a-b55451656ff7
description: Установка надстройки контроля Office 365 для настольных систем версии Outlook
ms.openlocfilehash: 0bddf305087bf0d9552c7671da5306db8352143f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534359"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="f4dec-103">Установка надстройки контроля для классической версии Outlook</span><span class="sxs-lookup"><span data-stu-id="f4dec-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="f4dec-p101">Для просмотра коммуникаций, определяемую средством политика контроля использования рецензентов контроля надстройки для Outlook и Outlook веб-приложения. Надстройка устанавливается автоматически в Outlook web app для всех рецензентов, указанному в политике. Тем не менее проверяющие должны работать с помощью некоторые действия, чтобы установить в версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="f4dec-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f4dec-p102">С помощью политики контроля требуется подписка на Office 365 E5 для вашей организации. Если нет этого плана и попытайтесь контроля, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f4dec-p102">Using supervision policies requires an Office 365 E5 subscription for your organization. If you don't have that plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="f4dec-109">Шаг 1: Скопируйте адрес почтового ящика контроля</span><span class="sxs-lookup"><span data-stu-id="f4dec-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="f4dec-110">Чтобы установить надстройки для Outlook на рабочем столе, вам потребуются адрес для контроля почтового ящика, который был создан как часть процесса установки политики контроля.</span><span class="sxs-lookup"><span data-stu-id="f4dec-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f4dec-111">Если созданный другим пользователем политики, то необходимо получить этот адрес из них, чтобы установить надстройку.</span><span class="sxs-lookup"><span data-stu-id="f4dec-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span> 
  
 <span data-ttu-id="f4dec-112">**Чтобы найти адрес почтового ящика контроля**</span><span class="sxs-lookup"><span data-stu-id="f4dec-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="f4dec-113">Вход в [безопасности &amp; центре соответствия требованиям](https://protection.office.com) с использованием учетных данных для учетной записи администратора в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="f4dec-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span> 
    
2. <span data-ttu-id="f4dec-114">Последовательно выберите пункты **данных управления** \> **контроля**.</span><span class="sxs-lookup"><span data-stu-id="f4dec-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="f4dec-115">Выберите политику контроля, сбор коммуникаций, которые необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="f4dec-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="f4dec-116">В политике приведены сведения о всплывающее окно, в разделе ** почтового ящика контроля **, скопируйте адрес.</span><span class="sxs-lookup"><span data-stu-id="f4dec-116">In the policy details flyout, under ** Supervision mailbox **, copy the address.</span></span> 
    
    ![В разделе «Контроля почтового ящика» отображаются с выделением адрес почтового ящика контроля всплывающее окно сведений политики контроля](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="f4dec-118">Шаг 2: Настройка почтовых ящиков контроля для доступа к Outlook для настольных систем</span><span class="sxs-lookup"><span data-stu-id="f4dec-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="f4dec-119">Далее рецензентов потребуется выполнить две команды Exchange Online PowerShell, необходимые для подключения к почтовому ящику контроля Outlook.</span><span class="sxs-lookup"><span data-stu-id="f4dec-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="f4dec-p103">Подключение к Exchange Online PowerShell. [Как это сделать?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="f4dec-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="f4dec-122">Выполните следующие команды:</span><span class="sxs-lookup"><span data-stu-id="f4dec-122">Run the following commands.</span></span>
    
  ```
  Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccessSet-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false
  ```

    <span data-ttu-id="f4dec-123">Где *SupervisoryReview{GUID}@domain.onmicrosoft.com* — адрес, скопированный в шаге 1, а *пользователь* — это имя проверяющий пользователей, которые будут подключаться к почтовому ящику контроля на следующем этапе.</span><span class="sxs-lookup"><span data-stu-id="f4dec-123">Where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in the next step.</span></span> 
    
3. <span data-ttu-id="f4dec-124">Подождите, пока по крайней мере один час, прежде чем перейти к шагу 3 ниже.</span><span class="sxs-lookup"><span data-stu-id="f4dec-124">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="f4dec-125">Шаг 3: Создание профиля Outlook для подключения к почтовому ящику контроля</span><span class="sxs-lookup"><span data-stu-id="f4dec-125">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="f4dec-126">На последнем этапе рецензентов потребуется создать профиль Outlook для подключения к почтовому ящику контроля.</span><span class="sxs-lookup"><span data-stu-id="f4dec-126">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f4dec-p104">Чтобы создать новый профиль Outlook, используется параметры электронной почты в панели управления Windows. Путь, который времени для получения этих параметров могут зависеть от операционной системы Windows (Windows 7, Windows 8 или Windows 10), используете и какие версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="f4dec-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span> 
  
1. <span data-ttu-id="f4dec-129">Откройте панель управления, а в поле **поиска** в верхней части окна введите **почты**.</span><span class="sxs-lookup"><span data-stu-id="f4dec-129">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="f4dec-p105">Не том, как получить в панели управления? Просмотреть [где — панель управления?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span><span class="sxs-lookup"><span data-stu-id="f4dec-p105">Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel)</span></span>
  
2. <span data-ttu-id="f4dec-132">Откройте **почтовое** приложение.</span><span class="sxs-lookup"><span data-stu-id="f4dec-132">Open the **Mail** app.</span></span> 
    
3. <span data-ttu-id="f4dec-133">**Настройка почты - Outlook**нажмите кнопку **Показать**.</span><span class="sxs-lookup"><span data-stu-id="f4dec-133">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span>
    
    ![«Настройка почты - Outlook» диалоговое окно с кнопкой Показать конфигурации с выделением](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)
  
4. <span data-ttu-id="f4dec-p106">В **почты**нажмите кнопку **Добавить**. В **Новый профиль**, введите имя почтового ящика контроля (например, **контроля**).</span><span class="sxs-lookup"><span data-stu-id="f4dec-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span>
    
    ![Диалоговое окно «Новый профиль», отображающее имя «Контроля» в поле «Имя профиля»](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)
  
5. <span data-ttu-id="f4dec-138">В **Outlook подключение к Office 365**выберите **подключение к другой учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="f4dec-138">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span>
    
    ![Сообщение «подключение Outlook к Office 365"с выделением ссылки «Подключиться к другой учетной записи»](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)
  
6. <span data-ttu-id="f4dec-140">**Автоматическая настройка учетной записи**выберите пункт **настройки вручную или дополнительные типы серверов**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="f4dec-140">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="f4dec-p107">В списке **Выберите тип учетной записи**выберите **Office 365**. В поле **Адрес электронной почты** введите адрес почтового ящика контроля, скопированные ранее.</span><span class="sxs-lookup"><span data-stu-id="f4dec-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span> 
    
    ![Страница «Выбор типа вашей учетной записи» диалоговое окно «Добавить учетную запись» в Outlook, отображается в поле «Адрес электронной почты» с выделением.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)
  
8. <span data-ttu-id="f4dec-144">При появлении запроса введите учетные данные Office 365.</span><span class="sxs-lookup"><span data-stu-id="f4dec-144">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="f4dec-145">Если успешно завершена, вы увидите **контроля - \<имя политики\> ** папка отображается в представлении списка папки в Outlook.</span><span class="sxs-lookup"><span data-stu-id="f4dec-145">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span> 
    

