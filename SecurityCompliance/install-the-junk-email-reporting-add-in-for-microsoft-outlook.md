---
title: Установка надстройки создания отчетов о нежелательной почте для Microsoft Outlook
ms.author: MSFTTracyP
author: tracyp
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8dcc752f-e22e-44ce-a104-4cc4d7e439f3
ms.collection:
- M365-security-compliance
description: В этом Артиклесуппортед Лангуажесинсталл создание сообщения о неЖелательной почте Добавление дополнительных сведений о надстройке создания отчетов о неЖелательной почте
ms.openlocfilehash: ee7d1ef3f906c7c03433140c50c5c975f456cb08
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693018"
---
# <a name="install-the-junk-email-reporting-add-in-for-microsoft-outlook"></a><span data-ttu-id="a063d-103">Установка надстройки создания отчетов о нежелательной почте для Microsoft Outlook</span><span class="sxs-lookup"><span data-stu-id="a063d-103">Install the Junk Email Reporting Add-in for Microsoft Outlook</span></span>
  
<span data-ttu-id="a063d-p101">В этом разделе описывается установка и удаление надстройки создания отчетов о нежелательной почте для Microsoft Outlook на клиентских компьютерах в организации. Текущая версия надстройки (январь 2016 г.) поддерживает Outlook 2016, Outlook 2013, Outlook 2010 и Outlook 2007.</span><span class="sxs-lookup"><span data-stu-id="a063d-p101">This topic describes how to install (and uninstall) the Microsoft Junk Email Reporting Add-in for Outlook on client computers in your organization. The current version of the add-in (January 2016) includes support for Outlook 2016, Outlook 2013, Outlook 2010, and Outlook 2007.</span></span> 
  
<span data-ttu-id="a063d-p102">Надстройка позволяет сообщать о нежелательной почте непосредственно в ленте Outlook (для всех поддерживаемых языков). В английской версии надстройки непосредственно из ленты также можно сообщать о других проблемах с электронной почтой:</span><span class="sxs-lookup"><span data-stu-id="a063d-p102">The add-in (for all supported languages) allows you to report junk email directly from the Outlook ribbon. The English version of the add-in includes additional options for reporting email issues to Microsoft, directly from the ribbon:</span></span>
  
-  <span data-ttu-id="a063d-108">полученных фишинговых сообщениях;</span><span class="sxs-lookup"><span data-stu-id="a063d-108">Report phishing scam emails that you receive</span></span> 
    
- <span data-ttu-id="a063d-109">сообщениях, ошибочно помеченных как нежелательные.</span><span class="sxs-lookup"><span data-stu-id="a063d-109">Report email incorrectly identified as junk mail.</span></span>
    
## <a name="supported-languages"></a><span data-ttu-id="a063d-110">Поддерживаемые языки</span><span class="sxs-lookup"><span data-stu-id="a063d-110">Supported Languages</span></span>
<span data-ttu-id="a063d-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-111"></span></span>

<span data-ttu-id="a063d-112">Надстройка создания отчетов о нежелательной почте поддерживает следующие языки:</span><span class="sxs-lookup"><span data-stu-id="a063d-112">The Junk Email Reporting Add-in supports the following languages:</span></span> 
  
- <span data-ttu-id="a063d-113">китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="a063d-113">Simplified Chinese</span></span>
    
- <span data-ttu-id="a063d-114">китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="a063d-114">Traditional Chinese</span></span>
    
- <span data-ttu-id="a063d-115">Голландский язык</span><span class="sxs-lookup"><span data-stu-id="a063d-115">Dutch</span></span>
    
- <span data-ttu-id="a063d-116">Английский</span><span class="sxs-lookup"><span data-stu-id="a063d-116">English</span></span>
    
- <span data-ttu-id="a063d-117">Французский язык</span><span class="sxs-lookup"><span data-stu-id="a063d-117">French</span></span>
    
- <span data-ttu-id="a063d-118">Немецкий язык</span><span class="sxs-lookup"><span data-stu-id="a063d-118">German</span></span>
    
- <span data-ttu-id="a063d-119">Итальянский язык</span><span class="sxs-lookup"><span data-stu-id="a063d-119">Italian</span></span>
    
- <span data-ttu-id="a063d-120">Японский</span><span class="sxs-lookup"><span data-stu-id="a063d-120">Japanese</span></span>
    
- <span data-ttu-id="a063d-121">Корейский</span><span class="sxs-lookup"><span data-stu-id="a063d-121">Korean</span></span>
    
- <span data-ttu-id="a063d-122">Португальский</span><span class="sxs-lookup"><span data-stu-id="a063d-122">Portuguese</span></span>
    
- <span data-ttu-id="a063d-123">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="a063d-123">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="a063d-124">Испанский</span><span class="sxs-lookup"><span data-stu-id="a063d-124">Spanish</span></span>
    
## <a name="install-the-junk-email-reporting-add-in"></a><span data-ttu-id="a063d-125">Установка надстройки создания отчетов о нежелательной почте</span><span class="sxs-lookup"><span data-stu-id="a063d-125">Install the Junk Email Reporting Add-in</span></span>
<span data-ttu-id="a063d-126"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-126"></span></span>

<span data-ttu-id="a063d-127">Как установить надстройку создания отчетов о нежелательной почте</span><span class="sxs-lookup"><span data-stu-id="a063d-127">You can install the Junk Email Reporting Add-in:</span></span>
  
- <span data-ttu-id="a063d-p103">C помощью пакета установщика Windows, который запускается так же, как любой другой MSI-файл. При установке надстройки откроется графический интерфейс пользователя, который состоит из последовательных экранов установки с запросами. Подробнее см. в разделе [Установка надстройки создания отчетов о нежелательной почте с помощью мастера установки](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard). ИЛИ</span><span class="sxs-lookup"><span data-stu-id="a063d-p103">By running the Windows Installer package as you would any other .msi file. When you install the add-in, a GUI interface opens and prompts you through the installation screens. For more information, see [Install the Junk Email Reporting Add-In using the Setup wizard](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard). OR</span></span>
    
- <span data-ttu-id="a063d-p104">Запустив автоматическую установку, которая подавляет пользовательский интерфейс установки. Вместо него указываются параметры командной строки, которые управляют сценарием установки. При установке надстройки доступны дополнительные параметры конфигурации, которых нет в графическом интерфейсе пользователя. Подробнее см. в разделе [Установка надстройки создания отчетов о нежелательной почте в автоматическом режиме](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode).</span><span class="sxs-lookup"><span data-stu-id="a063d-p104">By running a silent installation which suppresses the installation user interface. Instead, you specify command-line options which run an installation script. When you install the add-in, additional configuration options are available which are not available through the GUI interface. For more information, see [Install the Junk Email Reporting Add-In using Silent Mode](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode).</span></span>
    
### <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="a063d-136">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="a063d-136">What do you need to know before you begin?</span></span>

<span data-ttu-id="a063d-137">Для установки надстройки создания отчетов о нежелательной почте для Microsoft Outlook требуется следующее.</span><span class="sxs-lookup"><span data-stu-id="a063d-137">Installation of the Microsoft Junk Email Reporting Add-in for Microsoft Outlook requires:</span></span>
  
- <span data-ttu-id="a063d-138">Одна из таких операционных систем: Windows 10, Windows 8.1, Windows 8, Windows 7 с пакетом обновления 1 (SP1), Windows 10 Server, Windows Server 2012 R2, Windows Server 2012 или Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a063d-138">One of the following operating systems: Windows 10, Windows 8.1, Windows 8, Windows 7 Service Pack 1, Windows 10 Server, Windows Server 2012 R2, Windows Server 2012, or Windows Server 2008 R2</span></span>
    
- <span data-ttu-id="a063d-139">Outlook 2016, Outlook 2013 или Outlook 2010 или Outlook 2007 (с пакетом обновления 2 или выше).</span><span class="sxs-lookup"><span data-stu-id="a063d-139">Outlook 2016, Outlook 2013, Outlook 2010, or Outlook 2007 (Service Pack 2 or higher)</span></span>
    
- <span data-ttu-id="a063d-140">Базовые комплекты средств взаимодействия Microsoft Office:</span><span class="sxs-lookup"><span data-stu-id="a063d-140">Microsoft Office Primary Interop Assemblies:</span></span> 
    
  - <span data-ttu-id="a063d-141">Чтобы загрузить базовые комплекты средств взаимодействия для Microsoft Office 2010 или более поздней версии, перейдите в [Центр загрузки Майкрософт](https://go.microsoft.com/fwlink/?LinkID=166026).</span><span class="sxs-lookup"><span data-stu-id="a063d-141">To download the Primary Interop Assemblies for Microsoft Office 2010 or higher, go to the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkID=166026).</span></span>
    
  - <span data-ttu-id="a063d-142">Чтобы загрузить базовые комплекты средств взаимодействия для Microsoft Office 2007, перейдите в [Центр загрузки Майкрософт](https://go.microsoft.com/fwlink/?LinkId=72637).</span><span class="sxs-lookup"><span data-stu-id="a063d-142">To download the Primary Interop Assemblies for Microsoft Office 2007, go to the [Microsoft Download Center](https://go.microsoft.com/fwlink/?LinkId=72637).</span></span>
    
- <span data-ttu-id="a063d-143">Microsoft .NET Framework [2.0](https://go.microsoft.com/fwlink/?LinkID=208706).</span><span class="sxs-lookup"><span data-stu-id="a063d-143">Microsoft .NET Framework [Version 2.0](https://go.microsoft.com/fwlink/?LinkID=208706).</span></span>
    
> [!NOTE]
> <span data-ttu-id="a063d-144">Требуются права администратора на компьютере, на котором устанавливается надстройка.</span><span class="sxs-lookup"><span data-stu-id="a063d-144">You must have administrator privileges on the computer on which you are installing the add-in.</span></span> 
  
### <a name="install-the-junk-email-reporting-add-in-using-the-setup-wizard"></a><span data-ttu-id="a063d-145">Установка надстройки создания отчетов о нежелательной почте с помощью мастера установки</span><span class="sxs-lookup"><span data-stu-id="a063d-145">Install the Junk Email Reporting Add-In using the Setup wizard</span></span>
<span data-ttu-id="a063d-146"><a name="BKMK_InstalltheJunkEmailReportingAdd-InUsingtheSetupWizard"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-146"></span></span>

1. <span data-ttu-id="a063d-147">Закройте Outlook на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a063d-147">On your computer, close Outlook.</span></span>
    
2. <span data-ttu-id="a063d-148">Перейдите в Центр загрузки Майкрософт на страницу надстройки создания отчетов о нежелательной почте для Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkID=147248](https://go.microsoft.com/fwlink/?LinkID=147248) и загрузите файл MSI.</span><span class="sxs-lookup"><span data-stu-id="a063d-148">Go to the Microsoft Download Center page for the Microsoft Junk E-mail Reporting Add-In for Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkID=147248](https://go.microsoft.com/fwlink/?LinkID=147248) and download the .msi file.</span></span> 
    
3. <span data-ttu-id="a063d-149">Дважды щелкните файл MSI.</span><span class="sxs-lookup"><span data-stu-id="a063d-149">Double-click the .msi file.</span></span> 
    
4. <span data-ttu-id="a063d-150">На странице **Добро пожаловать в мастер установки надстройки создания отчетов о нежелательной почте** нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a063d-150">On the **Welcome to Microsoft Junk Email Reporting Add-in Setup** page, click **Next**.</span></span> 
    
5. <span data-ttu-id="a063d-p105">Ознакомьтесь с условиями лицензионного соглашения и нажмите кнопку **Я принимаю условия лицензионного соглашения**, если вы согласны с условиями установки (это обязательно для продолжения установки). Чтобы продолжить, нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="a063d-p105">Review the license agreement, and then click **I accept the terms in the License Agreement** if you agree to the terms of installation (required to continue installation). Click **Next** to continue.</span></span> 
    
6. <span data-ttu-id="a063d-153">После завершения мастера нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="a063d-153">When the wizard is complete, click **Finish**.</span></span> 
    
7. <span data-ttu-id="a063d-154">Запустите приложение Outlook.</span><span class="sxs-lookup"><span data-stu-id="a063d-154">Start Outlook.</span></span>
    
8. <span data-ttu-id="a063d-p106">Найдите кнопку **Нежелательная почта** в ленте Outlook. С ее помощью можно сообщить корпорации Майкрософт о нежелательных сообщениях электронной почты. Выберите эти письма в папке "Входящие" и нажмите кнопку **Сообщить о нежелательной почте**.</span><span class="sxs-lookup"><span data-stu-id="a063d-p106">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span> 
    
9. <span data-ttu-id="a063d-p107">Нажмите стрелку вниз рядом с кнопкой **Нежелательная почта**, чтобы открыть дополнительные параметры, например **Фишинговое сообщение**, если вы хотите сообщить корпорации Майкрософт о фишинговых сообщениях. В папке нежелательной почты можно также выбрать параметр **Не является нежелательным**, если сообщение ошибочно помечено как нежелательное.</span><span class="sxs-lookup"><span data-stu-id="a063d-p107">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span> 
    
### <a name="install-the-junk-email-reporting-add-in-using-silent-mode"></a><span data-ttu-id="a063d-159">Установка надстройки создания отчетов о нежелательной почте в автоматическом режиме</span><span class="sxs-lookup"><span data-stu-id="a063d-159">Install the Junk Email Reporting Add-In using Silent Mode</span></span>
<span data-ttu-id="a063d-160"><a name="BKMK_InstalltheJunkEmailReportingAdd-IninSilentMode"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-160"></span></span>

1. <span data-ttu-id="a063d-161">Закройте Outlook на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a063d-161">On your computer, close Outlook.</span></span>
    
2. <span data-ttu-id="a063d-162">Откройте окно командной строки.</span><span class="sxs-lookup"><span data-stu-id="a063d-162">Open a command prompt.</span></span>
    
3. <span data-ttu-id="a063d-163">Если вы хотите выполнить простую установку надстройки без дополнительных параметров, введите следующую команду.</span><span class="sxs-lookup"><span data-stu-id="a063d-163">If you want to perform a straight installation of the add-in, without any optional parameters, specify the following:</span></span>
    
  - <span data-ttu-id="a063d-164">Компьютеры с Outlook версии x86:  `msiexec /qn /i JunkReportingAdd-in.x86-en.msi`</span><span class="sxs-lookup"><span data-stu-id="a063d-164">Computers running x86 Outlook:  `msiexec /qn /i JunkReportingAdd-in.x86-en.msi`</span></span>
    
  - <span data-ttu-id="a063d-165">Компьютеры с Outlook версии x64:  `msiexec /qn /i JunkReportingAdd-in.x64-en.msi`</span><span class="sxs-lookup"><span data-stu-id="a063d-165">Computers running x64 Outlook:  `msiexec /qn /i JunkReportingAdd-in.x64-en.msi`</span></span>
    
    <span data-ttu-id="a063d-166">Также можно указать дополнительные параметры MaxMessageSelection и BccEmailAddress.</span><span class="sxs-lookup"><span data-stu-id="a063d-166">You can also specify the optional MaxMessageSelection and BccEmailAddress parameters:</span></span>
    
  - <span data-ttu-id="a063d-p108">Параметр MaxMessageSelection позволяет администратору задать максимальное число сообщений, которые могут быть выбраны пользователями для отправки за один раз. Допускаются значения от 1 до 50; значение по умолчанию  10.</span><span class="sxs-lookup"><span data-stu-id="a063d-p108">MaxMessageSelection Allows administrators to define the maximum number of messages that can be selected by users for submission in a single click. The range is 1 to 50 messages, and the default value is 10 messages.</span></span>
    
    <span data-ttu-id="a063d-169">Пример. Чтобы задать значение 16 в качестве максимального числа сообщений, которые пользователи могут выбрать для отправки за один раз, укажите в команде установки следующий параметр.  `MaxMessageSelection=16`</span><span class="sxs-lookup"><span data-stu-id="a063d-169">Example: If you want to set the maximum number of messages that can be selected by users for submission in a single click to 16, use the following option as part of the installation command:  `MaxMessageSelection=16`</span></span>
    
  - <span data-ttu-id="a063d-p109">Параметр BccEmailAddress позволяет администратору настроить почтовый ящик для получения копий всех отправок пользователей. Для этого задается адрес в поле «Скрытая копия». После настройки почтового ящика копии всех отправляемых сообщений будут отправляться на адрес, указанный в параметре BccEmailAddress. По умолчанию адрес для отправки скрытой копии не задается.</span><span class="sxs-lookup"><span data-stu-id="a063d-p109">BccEmailAddress Allows Administrators to set up a mailbox to receive a copy of all their user submissions by setting a Bcc email address. When the mailbox is set up, a copy of all submitted emails will be sent to the BccEmailAddress. Otherwise, the default setting is no Bcc email address.</span></span>
    
    <span data-ttu-id="a063d-173">Пример. Чтобы использовать для отправки скрытой копии адрес junkReports@contoso.com, введите следующую команду.  `BccEmailAddress="junkReports@contoso.com"`</span><span class="sxs-lookup"><span data-stu-id="a063d-173">Example: If you want to use junkReports@contoso.com as the Bcc email address for all submissions, use the following command:  `BccEmailAddress="junkReports@contoso.com"`</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a063d-p110">Можно задать несколько адресов для отправки скрытой копии, разделив их точкой с запятой. Пример.  `BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`</span><span class="sxs-lookup"><span data-stu-id="a063d-p110">You can set multiple Bcc email addresses by entering them with a semicolon delimiter. Example:  `BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"`</span></span>
  
    <span data-ttu-id="a063d-176">Чтобы добавить оба необязательных параметра, описанных в предыдущих примерах, введите следующую команду на компьютере с Outlook версии x86:</span><span class="sxs-lookup"><span data-stu-id="a063d-176">To add both of these optional parameters based on the above examples, you would specify the following for a computer running x86 Outlook:</span></span> 
    
  ```
  msiexec /qn /i JunkReportingAdd-in.x86-en.msi. MaxMessageSelection=16 BccEmailAddress="junkReports@contoso.com; hollyd@treyresearch.net"
  ```

4. <span data-ttu-id="a063d-177">После завершения установки запустите Outlook.</span><span class="sxs-lookup"><span data-stu-id="a063d-177">After the installation is complete, start Outlook.</span></span>
    
5. <span data-ttu-id="a063d-p111">Найдите кнопку **Нежелательная почта** в ленте Outlook. С ее помощью можно сообщить корпорации Майкрософт о нежелательных сообщениях электронной почты. Выберите эти письма в папке "Входящие" и нажмите кнопку **Сообщить о нежелательной почте**.</span><span class="sxs-lookup"><span data-stu-id="a063d-p111">Look for the **Junk** button on your Outlook ribbon. You can now report junk email messages to Microsoft by selecting the junk email messages in your Inbox and clicking the **Report Junk** button.</span></span> 
    
6. <span data-ttu-id="a063d-p112">Нажмите стрелку вниз рядом с кнопкой **Нежелательная почта**, чтобы открыть дополнительные параметры, например **Фишинговое сообщение**, если вы хотите сообщить корпорации Майкрософт о фишинговых сообщениях. В папке нежелательной почты можно также выбрать параметр **Не является нежелательным**, если сообщение ошибочно помечено как нежелательное.</span><span class="sxs-lookup"><span data-stu-id="a063d-p112">Choose the down arrow next to **Junk** for more options such as **Report as Phishing** if you want to report phishing scam emails to Microsoft. In your junk mail folder, you can also select, **Report not junk** if an email was incorrectly identified as junk mail.</span></span> 
    
## <a name="uninstall-the-junk-email-reporting-add-in"></a><span data-ttu-id="a063d-182">Удаление надстройки создания отчетов о нежелательной почте</span><span class="sxs-lookup"><span data-stu-id="a063d-182">Uninstall the Junk Email Reporting Add-in</span></span>
<span data-ttu-id="a063d-183"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-183"></span></span>

<span data-ttu-id="a063d-184">Чтобы удалить надстройку создания отчетов о нежелательной почте:</span><span class="sxs-lookup"><span data-stu-id="a063d-184">Use one of these options to uninstall the Junk Email Reporting Add-in:</span></span>
  
- <span data-ttu-id="a063d-p113">Удалите надстройку с помощью панели управления Windows. Дополнительные сведения см. в разделе [Удаление надстройки создания отчетов о нежелательной почте с помощью панели управления](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel). ИЛИ</span><span class="sxs-lookup"><span data-stu-id="a063d-p113">Remove the add-in using Windows Control Panel. For more information, see [Uninstall the Junk Email Reporting Add-in from Control Panel](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel). OR</span></span>
    
- <span data-ttu-id="a063d-p114">Запустите пакет установщика Windows и выберите параметр удаления. Дополнительные сведения см. в разделе [Удаление надстройки создания отчетов о нежелательной почте с помощью пакета установщика Windows](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage). ИЛИ</span><span class="sxs-lookup"><span data-stu-id="a063d-p114">Run the Windows installer package and select the uninstall option. For more information, see [Uninstall the Junk Email Reporting Add-in by Running the Windows Installer Package](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage).OR</span></span>
    
- <span data-ttu-id="a063d-p115">Запустите автоматическую установку с помощью параметра удаления. Дополнительные сведения см. в разделе [Удаление надстройки создания отчетов о нежелательной почте в автоматическом режиме](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#MK_UninstalltheJunkEmailReportingAdd-ininSilentMode).</span><span class="sxs-lookup"><span data-stu-id="a063d-p115">Run a silent installation using the uninstall option. For more information, see [Uninstall the Junk Email Reporting Add-in in Silent Mode](install-the-junk-email-reporting-add-in-for-microsoft-outlook.md#MK_UninstalltheJunkEmailReportingAdd-ininSilentMode).</span></span>
    
> [!NOTE]
> <span data-ttu-id="a063d-192">Требуются права администратора на компьютере, с которого удаляется надстройка.</span><span class="sxs-lookup"><span data-stu-id="a063d-192">You must have administrator privileges on the computer on which you are uninstalling the add-in.</span></span> 
  
### <a name="uninstall-the-junk-email-reporting-add-in-from-control-panel"></a><span data-ttu-id="a063d-193">Удаление надстройки создания отчетов о нежелательной почте с помощью панели управления</span><span class="sxs-lookup"><span data-stu-id="a063d-193">Uninstall the Junk Email Reporting Add-in from Control Panel</span></span>
<span data-ttu-id="a063d-194"><a name="BKMK_UninstalltheJunkEmailReportingAdd-infromControlPanel"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-194"></span></span>

1. <span data-ttu-id="a063d-195">Закройте Outlook на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a063d-195">On your computer, close Outlook.</span></span>
    
2. <span data-ttu-id="a063d-196">На компьютере в меню пуск выберите **Панель управления**.</span><span class="sxs-lookup"><span data-stu-id="a063d-196">From the Start menu on your computer, select **Control Panel**.</span></span>
    
3. <span data-ttu-id="a063d-197">Выберите **Программы и компоненты**.</span><span class="sxs-lookup"><span data-stu-id="a063d-197">Select **Programs and Features**.</span></span>
    
4. <span data-ttu-id="a063d-198">Выберите **Надстройка создания отчетов о нежелательной почте для Microsoft Office Outlook**.</span><span class="sxs-lookup"><span data-stu-id="a063d-198">Select **Microsoft Junk E-mail Reporting Add-In for Microsoft Office Outlook**.</span></span>
    
5. <span data-ttu-id="a063d-199">Выберите **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="a063d-199">Select **Uninstall**.</span></span>
    
6. <span data-ttu-id="a063d-200">Снова запустите Outlook, чтобы убедиться, что надстройка больше не отображается в ленте.</span><span class="sxs-lookup"><span data-stu-id="a063d-200">Start Outlook again to confirm that the add-in is no longer displayed on your Outlook ribbon.</span></span>
    
### <a name="uninstall-the-junk-email-reporting-add-in-by-running-the-windows-installer-package"></a><span data-ttu-id="a063d-201">Удаление надстройки создания отчетов о нежелательной почте с помощью пакета установщика Windows</span><span class="sxs-lookup"><span data-stu-id="a063d-201">Uninstall the Junk Email Reporting Add-in by Running the Windows Installer Package</span></span>
<span data-ttu-id="a063d-202"><a name="BKMK_UninstalltheJunkEmailReportingAddinbyRunningtheWindowsInstallerPackage"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-202"></span></span>

1. <span data-ttu-id="a063d-203">Закройте Outlook на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a063d-203">On your computer, close Outlook.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a063d-204">Если во время удаления Outlook будет работать, его нужно будет перезапустить, чтобы надстройка была полностью удалена.</span><span class="sxs-lookup"><span data-stu-id="a063d-204">If Outlook is running during the uninstall process, it will need to be restarted in order for the add-in to be completely uninstalled.</span></span> 
  
2. <span data-ttu-id="a063d-205">Запустите повторно файл MSI, который вы запускали для установки надстройки.</span><span class="sxs-lookup"><span data-stu-id="a063d-205">Re-run the .msi file you previously ran to install the add-in.</span></span> 
    
    <span data-ttu-id="a063d-206">(Перейдите в Центр загрузки Майкрософт на страницу надстройки создания отчетов о нежелательной почте для Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkId=147248](https://go.microsoft.com/fwlink/?LinkId=147248) и загрузите файл MSI, а затем запустите его двойным щелчком).</span><span class="sxs-lookup"><span data-stu-id="a063d-206">(Go to the Microsoft Download Center page for the Microsoft Junk E-mail Reporting Add-In for Microsoft Outlook [https://go.microsoft.com/fwlink/?LinkId=147248](https://go.microsoft.com/fwlink/?LinkId=147248), download the .msi file, and then double-click the .msi file.)</span></span> 
    
3. <span data-ttu-id="a063d-207">Следуйте указаниям для удаления надстройки.</span><span class="sxs-lookup"><span data-stu-id="a063d-207">Follow the prompts to uninstall the add-in.</span></span>
    
4. <span data-ttu-id="a063d-208">Снова запустите Outlook, чтобы убедиться, что надстройка больше не отображается в ленте.</span><span class="sxs-lookup"><span data-stu-id="a063d-208">Start Outlook again to confirm that the add-in is no longer displayed on your Outlook ribbon.</span></span>
    
### <a name="uninstall-the-junk-email-reporting-add-in-in-silent-mode"></a><span data-ttu-id="a063d-209">Удаление надстройки создания отчетов о нежелательной почте в автоматическом режиме</span><span class="sxs-lookup"><span data-stu-id="a063d-209">Uninstall the Junk Email Reporting Add-in in Silent Mode</span></span>
<span data-ttu-id="a063d-210"><a name="MK_UninstalltheJunkEmailReportingAdd-ininSilentMode"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-210"></span></span>

1. <span data-ttu-id="a063d-211">Закройте Outlook на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a063d-211">On your computer, close Outlook.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a063d-212">Если во время удаления Outlook будет работать, его нужно будет перезапустить, чтобы надстройка была полностью удалена.</span><span class="sxs-lookup"><span data-stu-id="a063d-212">If Outlook is running during the uninstall process, it will need to be restarted in order for the add-in to be completely uninstalled.</span></span> 
  
2. <span data-ttu-id="a063d-213">Откройте окно командной строки.</span><span class="sxs-lookup"><span data-stu-id="a063d-213">Open a command prompt.</span></span>
    
3. <span data-ttu-id="a063d-214">Укажите следующий параметр командной строки.</span><span class="sxs-lookup"><span data-stu-id="a063d-214">Specify the following command line parameter:</span></span>
    
    <span data-ttu-id="a063d-215">Компьютеры с Outlook версии x86:  `msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span><span class="sxs-lookup"><span data-stu-id="a063d-215">Computers running x86 Outlook:  `msiexec /x JunkReportingAdd-in.x86-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span></span>
    
    <span data-ttu-id="a063d-216">Компьютеры с Outlook версии x64:  `msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span><span class="sxs-lookup"><span data-stu-id="a063d-216">Computers running x64 Outlook:  `msiexec /x JunkReportingAdd-in.x64-en.msi /qn MSIRESTARTMANAGERCONTROL="DisableShutdown"`</span></span>
    
4. <span data-ttu-id="a063d-217">Снова запустите Outlook, чтобы убедиться, что надстройка больше не отображается в ленте.</span><span class="sxs-lookup"><span data-stu-id="a063d-217">Start Outlook again to confirm that the add-in is no longer displayed on your Outlook ribbon.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="a063d-218">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="a063d-218">For more information</span></span>
<span data-ttu-id="a063d-219"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="a063d-219"></span></span>

[<span data-ttu-id="a063d-220">Отправка отчетов о нежелательных сообщениях в корпорацию Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a063d-220">Report junk email messages to Microsoft</span></span>](report-junk-email-messages-to-microsoft.md)
  
[<span data-ttu-id="a063d-221">Сведения об устранении неполадок и поддержке</span><span class="sxs-lookup"><span data-stu-id="a063d-221">Troubleshooting and support information</span></span>](troubleshooting-and-support-information.md)
  

