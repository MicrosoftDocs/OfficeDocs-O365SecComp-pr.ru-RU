---
title: Установка надстройки контроля для классической версии Outlook
ms.author: robmazz
author: robmazz
manager: laurawi
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
ms.openlocfilehash: b0cb0d78ab5f8887628528dd53b49fb15de44126
ms.sourcegitcommit: 204fb0269b5c10b63941055824e863d77e3e9b02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/06/2018
ms.locfileid: "27180869"
---
# <a name="install-the-supervision-add-in-for-outlook-desktop"></a><span data-ttu-id="00c90-103">Установка надстройки контроля для классической версии Outlook</span><span class="sxs-lookup"><span data-stu-id="00c90-103">Install the Supervision add-in for Outlook desktop</span></span>

<span data-ttu-id="00c90-p101">Для просмотра коммуникаций, определяемую средством политика контроля использования рецензентов контроля надстройки для Outlook и Outlook веб-приложения. Надстройка устанавливается автоматически в Outlook web app для всех рецензентов, указанному в политике. Тем не менее проверяющие должны работать с помощью некоторые действия, чтобы установить в версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="00c90-p101">To review communications identified by a supervision policy, reviewers use the Supervision add-in for Outlook and Outlook web app. The add-in is installed automatically in Outlook web app for all reviewers you specified in the policy. However, reviewers must run through some steps to install it in the desktop version of Outlook.</span></span>
  
> [!NOTE]
> <span data-ttu-id="00c90-p102">Пользователи, контактным лицом политики контроля должен иметь либо лицензию Office 365 для предприятий E3 с помощью надстройки дополнительные соответствия или включаться в подписки на Office 365 корпоративный E5. Если нет существующего плана Enterprise E5 и попытайтесь контроля, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="00c90-p102">Users monitored by supervision policies must have either an Office 365 Enterprise E3 license with the Advanced Compliance add-on or be included in an Office 365 Enterprise E5 subscription. If you don't have an existing Enterprise E5 plan and want to try supervision, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span>
  
## <a name="step-1-copy-the-address-for-the-supervision-mailbox"></a><span data-ttu-id="00c90-109">Шаг 1: Скопируйте адрес почтового ящика контроля</span><span class="sxs-lookup"><span data-stu-id="00c90-109">Step 1: Copy the address for the supervision mailbox</span></span>

<span data-ttu-id="00c90-110">Чтобы установить надстройки для Outlook на рабочем столе, вам потребуются адрес для контроля почтового ящика, который был создан как часть процесса установки политики контроля.</span><span class="sxs-lookup"><span data-stu-id="00c90-110">To install the add-in for Outlook desktop, you'll need the address for the supervision mailbox that was created as part of the supervision policy setup.</span></span>
  
> [!NOTE]
> <span data-ttu-id="00c90-111">Если созданный другим пользователем политики, то необходимо получить этот адрес из них, чтобы установить надстройку.</span><span class="sxs-lookup"><span data-stu-id="00c90-111">If someone else created the policy, you'll need to get this address from them to install the add-in.</span></span>
 
 <span data-ttu-id="00c90-112">**Чтобы найти адрес почтового ящика контроля**</span><span class="sxs-lookup"><span data-stu-id="00c90-112">**To find the supervision mailbox address**</span></span>
  
1. <span data-ttu-id="00c90-113">Вход в [безопасности &amp; центре соответствия требованиям](https://protection.office.com) с использованием учетных данных для учетной записи администратора в организации Office 365.</span><span class="sxs-lookup"><span data-stu-id="00c90-113">Sign into the [Security &amp; Compliance Center](https://protection.office.com) using credentials for an admin account in your Office 365 organization.</span></span>
    
2. <span data-ttu-id="00c90-114">Последовательно выберите пункты **данных управления** \> **контроля**.</span><span class="sxs-lookup"><span data-stu-id="00c90-114">Go to **Data governance** \> **Supervision**.</span></span>
    
3. <span data-ttu-id="00c90-115">Выберите политику контроля, сбор коммуникаций, которые необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="00c90-115">Click the supervision policy that's gathering the communications you want to review.</span></span>
    
4. <span data-ttu-id="00c90-116">В политике приведены сведения о всплывающее окно, в разделе \*\* почтового ящика контроля \*\*, скопируйте адрес.</span><span class="sxs-lookup"><span data-stu-id="00c90-116">In the policy details flyout, under \*\* Supervision mailbox \*\*, copy the address.</span></span><br/>![В разделе «Контроля почтового ящика» отображаются с выделением адрес почтового ящика контроля всплывающее окно сведений политики контроля](media/71779d0e-4f01-4dd3-8234-5f9c30eeb067.jpg)
  
## <a name="step-2-configure-the-supervision-mailbox-for-outlook-desktop-access"></a><span data-ttu-id="00c90-118">Шаг 2: Настройка почтовых ящиков контроля для доступа к Outlook для настольных систем</span><span class="sxs-lookup"><span data-stu-id="00c90-118">Step 2: Configure the supervision mailbox for Outlook desktop access</span></span>

<span data-ttu-id="00c90-119">Далее рецензентов потребуется выполнить две команды Exchange Online PowerShell, необходимые для подключения к почтовому ящику контроля Outlook.</span><span class="sxs-lookup"><span data-stu-id="00c90-119">Next, reviewers will need to run a couple Exchange Online PowerShell commands so they can connect Outlook to the supervision mailbox.</span></span>
  
1. <span data-ttu-id="00c90-p103">Подключение к Exchange Online PowerShell. [Как это сделать?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span><span class="sxs-lookup"><span data-stu-id="00c90-p103">Connect to Exchange Online PowerShell. [How do I do this?](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)</span></span>
    
2. <span data-ttu-id="00c90-122">Выполните следующие команды, где *SupervisoryReview{GUID}@domain.onmicrosoft.com* — адрес, скопированный в шаге 1, а *пользователь* — это имя проверяющий пользователей, которые будут подключаться к почтовому ящику контроля на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="00c90-122">Run the following commands, where  *SupervisoryReview{GUID}@domain.onmicrosoft.com*  is the address you copied in Step 1 above, and  *User*  is the name of the reviewer who will be connecting to the supervision mailbox in Step 3.</span></span>
    - ```Add-MailboxPermission "SupervisoryReview{GUID}@domain.onmicrosoft.com" -User <alias or email address of the account that has reviewer permissions to the supervision mailbox> -AccessRights FullAccess```<br/>
    - ```Set-Mailbox "<SupervisoryReview{GUID}@domain.onmicrosoft.com>" -HiddenFromAddressListsEnabled: $false```
    
3. <span data-ttu-id="00c90-123">Подождите, пока по крайней мере один час, прежде чем перейти к шагу 3 ниже.</span><span class="sxs-lookup"><span data-stu-id="00c90-123">Wait at least an hour before moving on to Step 3 below.</span></span>
    
## <a name="step-3-create-an-outlook-profile-to-connect-to-the-supervision-mailbox"></a><span data-ttu-id="00c90-124">Шаг 3: Создание профиля Outlook для подключения к почтовому ящику контроля</span><span class="sxs-lookup"><span data-stu-id="00c90-124">Step 3: Create an Outlook profile to connect to the supervision mailbox</span></span>

<span data-ttu-id="00c90-125">На последнем этапе рецензентов потребуется создать профиль Outlook для подключения к почтовому ящику контроля.</span><span class="sxs-lookup"><span data-stu-id="00c90-125">For the final step, reviewers will need to create an Outlook profile to connect to the supervision mailbox.</span></span>
 
> [!NOTE]
> <span data-ttu-id="00c90-p104">Чтобы создать новый профиль Outlook, используется параметры электронной почты в панели управления Windows. Путь, который времени для получения этих параметров могут зависеть от операционной системы Windows (Windows 7, Windows 8 или Windows 10), используете и какие версии Outlook.</span><span class="sxs-lookup"><span data-stu-id="00c90-p104">To create a new Outlook profile, you'll use the Mail settings in the Windows Control Panel. The path you take to get to these settings might depend on which Windows operating system (Windows 7, Windows 8, or Windows 10) you're using and which version of Outlook is installed.</span></span>
  
1. <span data-ttu-id="00c90-128">Откройте панель управления, а в поле **поиска** в верхней части окна введите **почты**.</span><span class="sxs-lookup"><span data-stu-id="00c90-128">Open the Control Panel, and in the **Search** box at the top of the window, type **Mail**.</span></span><br/><span data-ttu-id="00c90-p105">(Не том, как получить в панели управления? Просмотреть [где — панель управления?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span><span class="sxs-lookup"><span data-stu-id="00c90-p105">(Not sure how to get to the Control Panel? See [Where is Control Panel?](https://support.microsoft.com/help/13764/windows-where-is-control-panel))</span></span>
  
2. <span data-ttu-id="00c90-131">Откройте **почтовое** приложение.</span><span class="sxs-lookup"><span data-stu-id="00c90-131">Open the **Mail** app.</span></span>
    
3. <span data-ttu-id="00c90-132">**Настройка почты - Outlook**нажмите кнопку **Показать**.</span><span class="sxs-lookup"><span data-stu-id="00c90-132">In **Mail Setup - Outlook**, click **Show Profiles**.</span></span><br/><span data-ttu-id="00c90-133">![«Настройка почты - Outlook» диалоговое окно с кнопкой Показать конфигурации с выделением](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span><span class="sxs-lookup"><span data-stu-id="00c90-133">![The 'Mail Setup - Outlook' dialog box with the 'Show Profiles' button highlighted](media/28b5dae9-d10c-4f2b-926a-294c857d555c.jpg)</span></span>
  
4. <span data-ttu-id="00c90-p106">В **почты**нажмите кнопку **Добавить**. В **Новый профиль**, введите имя почтового ящика контроля (например, **контроля**).</span><span class="sxs-lookup"><span data-stu-id="00c90-p106">In **Mail**, click **Add**. Then, in **New Profile**, enter a name for the supervision mailbox (such as **Supervision**).</span></span><br/><span data-ttu-id="00c90-136">![Диалоговое окно «Новый профиль», отображающее имя «Контроля» в поле «Имя профиля»](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span><span class="sxs-lookup"><span data-stu-id="00c90-136">![The 'New Profile' dialog showing the name 'Supervision' in the 'Profile Name' box](media/d02ae181-b541-4ec6-8f51-698f30033204.jpg)</span></span>
  
5. <span data-ttu-id="00c90-137">В **Outlook подключение к Office 365**выберите **подключение к другой учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="00c90-137">In **Connect Outlook to Office 365**, click **Connect to a different account**.</span></span><br/><span data-ttu-id="00c90-138">![Сообщение «подключение Outlook к Office 365"с выделением ссылки «Подключиться к другой учетной записи»](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span><span class="sxs-lookup"><span data-stu-id="00c90-138">![The 'Connect Outlook to Office 365' message with the 'Connect to a different account' link highlighted](media/fac49ff8-a7f0-4e82-a271-9ec045a95de1.jpg)</span></span>
  
6. <span data-ttu-id="00c90-139">**Автоматическая настройка учетной записи**выберите пункт **настройки вручную или дополнительные типы серверов**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="00c90-139">In **Auto Account Setup**, choose **Manual setup or additional server types**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="00c90-p107">В списке **Выберите тип учетной записи**выберите **Office 365**. В поле **Адрес электронной почты** введите адрес почтового ящика контроля, скопированные ранее.</span><span class="sxs-lookup"><span data-stu-id="00c90-p107">In **Choose Your Account Type**, choose **Office 365**. Then, in the **Email Address** box, enter the address of the supervision mailbox you copied previously.</span></span><br/><span data-ttu-id="00c90-142">![Страница «Выбор типа вашей учетной записи» диалоговое окно «Добавить учетную запись» в Outlook, отображается в поле «Адрес электронной почты» с выделением.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span><span class="sxs-lookup"><span data-stu-id="00c90-142">![The 'Choose Your Account Type' page of the 'Add Account' dialog in Outlook showing the 'Email Address' box highlighted.](media/4f601236-9f69-4cf6-a58c-0b91204aa8cb.jpg)</span></span>
  
8. <span data-ttu-id="00c90-143">При появлении запроса введите учетные данные Office 365.</span><span class="sxs-lookup"><span data-stu-id="00c90-143">When prompted, enter your Office 365 credentials.</span></span>
    
9. <span data-ttu-id="00c90-144">Если успешно завершена, вы увидите \*\*контроля - \<имя политики\> \*\* папка отображается в представлении списка папки в Outlook.</span><span class="sxs-lookup"><span data-stu-id="00c90-144">If successful, you'll see the **Supervision - \<policy name\>** folder listed in the Folder List view in Outlook.</span></span>