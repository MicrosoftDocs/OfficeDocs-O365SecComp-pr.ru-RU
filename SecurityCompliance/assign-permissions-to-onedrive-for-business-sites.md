---
title: Назначение разрешений обнаружения электронных данных на сайтах OneDrive для бизнеса
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Центр обнаружения электронных данных в SharePoint Online можно использовать для поиска всех OneDrive для бизнеса сайтов в определенные ключевые слова, конфиденциальной информации и других критериев поиска в вашей организации. Каждому пользователю в организации является владельцем их OneDrive для бизнеса сайт, который находится в коллекции веб-сайтов с именем https://domain-my.sharepoint.com. По умолчанию глобального администратора Office 365 или compliance manager нельзя использовать центр обнаружения электронных данных в SharePoint Online для поиска любого OneDrive для бизнеса сайтов. Для поиска OneDrive for Business сайтов, Администраторы или руководителями соответствия необходимо быть администратором семейства сайтов, onedrive для бизнеса сайта.
ms.openlocfilehash: 61f068a03bcce599d9f1b7eb62d7b317b7feab68
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038092"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a><span data-ttu-id="0743c-106">Назначение разрешений обнаружения электронных данных на сайтах OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="0743c-106">Assign eDiscovery permissions to OneDrive for Business sites</span></span>

<span data-ttu-id="0743c-p102">Центр обнаружения электронных данных в SharePoint Online можно использовать для поиска всех OneDrive для бизнеса сайтов в определенные ключевые слова, конфиденциальной информации и других критериев поиска в вашей организации. Каждому пользователю в организации является владельцем их OneDrive для бизнеса сайт, который находится в коллекции веб-сайтов с именем https://domain-my.sharepoint.com. По умолчанию глобального администратора Office 365 или compliance manager нельзя использовать центр обнаружения электронных данных в SharePoint Online для поиска любого OneDrive для бизнеса сайтов. Для поиска OneDrive for Business сайтов, Администраторы или руководителями соответствия необходимо быть администратором семейства сайтов, onedrive для бизнеса сайта.</span><span class="sxs-lookup"><span data-stu-id="0743c-p102">You can use the eDiscovery Center in SharePoint Online to search all OneDrive for Business sites in your organization for certain keywords, sensitive information, and other search criteria. Each user in your organization is the owner of their OneDrive for Business site, which is located in the site collection named https://domain-my.sharepoint.com. By default, an Office 365 global administrator or compliance manager can't use the eDiscovery Center in SharePoint Online to search any OneDrive for Business sites. To search a OneDrive for Business site, administrators or compliance managers must be a site collection administrator for that OneDrive for Business site.</span></span> 
  
<span data-ttu-id="0743c-111">В этой статье описывается шаги, чтобы администратор или соответствия диспетчера администратором семейства сайтов для каждого OneDrive для бизнеса сайта в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0743c-111">This article guides you through the steps to make an administrator or compliance manager a site collection administrator for every OneDrive for Business site in your organization.</span></span> 
  
<span data-ttu-id="0743c-112">Советы по использованию скрипта в этой статье, включая Пересмотр скрипта в шаге 3, чтобы удалить пользователя как администратора семейства сайтов из службы OneDrive для бизнеса сайтов в разделе [Дополнительные сведения](#more-information) .</span><span class="sxs-lookup"><span data-stu-id="0743c-112">See the [More information](#more-information) section for tips about using the script in this article, including revising the script in Step 3 to remove a user as a site collection administrator from OneDrive for Business sites.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="0743c-113">Перед началом работы</span><span class="sxs-lookup"><span data-stu-id="0743c-113">Before you begin</span></span>

- <span data-ttu-id="0743c-p103">Установите командную консоль SharePoint Online. Дополнительные сведения см. в статье [Настройка среды Windows PowerShell для командной консоли SharePoint Online](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span><span class="sxs-lookup"><span data-stu-id="0743c-p103">Install the SharePoint Online Management Shell. For information, see [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span></span>
    
- <span data-ttu-id="0743c-116">Запустите сценарий в шаге 3 каждый раз, необходимо назначить пользователя как администратора семейства сайтов в любой OneDrive для бизнеса сайтов в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0743c-116">Run the script in Step 3 each time you want to assign a user as a site collection administrator to any OneDrive for Business sites in your organization.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="0743c-p104">Администратор или соответствия руководителя, который является администратором семейства сайтов для OneDrive для сайтов бизнес-можно открыть пользователей OneDrive для бизнеса с библиотеками документов и выполнять те же задачи, что владельца. Важно для элемента управления и отслеживать пользователей, имеющей разрешение обнаружения электронных данных в OneDrive для бизнеса сайтов в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0743c-p104">An administrator or compliance manager who is a site collection administrator for OneDrive for Business sites can open users' OneDrive for Business document libraries and perform the same tasks as the owner. It's important to control and monitor who has been assigned eDiscovery permissions to OneDrive for Business sites in your organization.</span></span> 
  
- <span data-ttu-id="0743c-p105">Пример сценария, представленные в этой статье не поддерживается в любой программе стандартной поддержки корпорации Майкрософт и службы. Образец сценария предоставляются как есть без какой-либо. Дополнительно корпорация Майкрософт не все подразумеваемых гарантий, включая, без ограничения, какие-либо подразумеваемых гарантий окупаемость или определенного случаях. Весь риск, возникающих в результате использования или производительности образец сценария и документация остается с вами. Событие не Майкрософт, ее автора или другим способом соблюдать создания, рабочей или доставки сценария несут ответственности для любых убытков ни при каких обстоятельствах (включая, без ограничений, убытков для потере бизнеса прибыли, перерывах в коммерческой деятельности, потеря бизнес-информация, или другие упущенную потери) возникающих в результате использования или невозможности использовать образец сценария или документация, даже если Microsoft поступали предупреждения о возможности такого ущерба.</span><span class="sxs-lookup"><span data-stu-id="0743c-p105">The sample script provided in this article isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the script be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample script or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a><span data-ttu-id="0743c-124">Этап 1: Сбор список всех OneDrive для бизнеса сайтов</span><span class="sxs-lookup"><span data-stu-id="0743c-124">Step 1: Collect a list of all OneDrive for Business sites</span></span>

<span data-ttu-id="0743c-p106">Первым шагом является создание списка всех OneDrive для бизнеса сайтов в вашей организации. Сведения содержатся в разделе [Создание списка всех расположений OneDrive в вашей организации](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Этот сценарий в этой статье создает текстового файла со списком всех сайтов OneDrive. Скрипт, на котором запущен на шаге 3 назначает указанного пользователя как администратора семейства сайтов в каждом OneDrive для бизнеса сайтов, перечисленные в текстовый файл, созданный на этом этапе. Следующий текст пример форматирования в список сайтов в этом файле. При необходимости можно удалить сайты из этого файла.</span><span class="sxs-lookup"><span data-stu-id="0743c-p106">The first step is to create a list of all OneDrive for Business sites in your organization. For instructions, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. The script that you run in Step 3 assigns a specified user as a site collection administrator to each OneDrive for Business site listed in the text file that's created in this step. The following text provides an example of how the list of sites in this file should be formatted. You can remove sites from this file if necessary.</span></span>

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a><span data-ttu-id="0743c-131">Шаг 2: Командная консоль SharePoint Online подключиться к своей организации</span><span class="sxs-lookup"><span data-stu-id="0743c-131">Step 2: Connect SharePoint Online Management Shell to your organization</span></span>

1. <span data-ttu-id="0743c-132">Откройте на локальном компьютере командную консоль SharePoint Online и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0743c-132">On your local computer, open the SharePoint Online Management Shell, and run the following command:</span></span>

    ```
    $credentials = Get-Credential
    ```

2. <span data-ttu-id="0743c-133">В диалоговом окне **Запрос учетных данных Windows PowerShell** введите имя пользователя и пароль глобального администратора Office 365, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0743c-133">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global administrator account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="0743c-134">Чтобы подключить командную консоль к своей организации SharePoint Online, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="0743c-134">Run the following command to connect the Shell to your SharePoint Online organization:</span></span>
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. <span data-ttu-id="0743c-135">Убедитесь, что подключение к организации SharePoint Online установлено, получив список всех сайтов в организации с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="0743c-135">To verify that you are connected to your SharePoint Online organization, run the following command to get a list of all the sites in your organization:</span></span>
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a><span data-ttu-id="0743c-136">Этап 3. Назначение пользователя администратором семейства веб-сайтов на сайтах OneDrive для бизнеса</span><span class="sxs-lookup"><span data-stu-id="0743c-136">Step 3: Assign a user as a site collection administrator to OneDrive for Business sites</span></span>

<span data-ttu-id="0743c-p107">Следующим шагом является запуск сценарий, который присваивает указанному пользователю как администратора семейства сайтов в каждом OneDrive для бизнеса сайта в вашей организации. Этот сценарий использует список OneDrive для бизнеса сайтов, созданной на шаге 1. Как было сказано ранее необходимо запустить этот скрипт каждый раз, когда необходимо назначить пользователя как администратора семейства сайтов OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="0743c-p107">The next step is to run a script that assigns a specified user as a site collection administrator in every OneDrive for Business site in your organization. This script uses the list of OneDrive for Business sites that you created in Step 1. As previously stated, you have to run this script each time that you want to assign a user as a site collection administrator to OneDrive for Business sites.</span></span>
  
1. <span data-ttu-id="0743c-p108">Сохраните приведенный ниже текст в текстовый файл. Этот файл можно назвать, например, OD4BAssignSCA.txt.</span><span class="sxs-lookup"><span data-stu-id="0743c-p108">Save the following text to a text file. For example, you could save it to a file named OD4BAssignSCA.txt.</span></span>

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. <span data-ttu-id="0743c-p109">Изменение следующих переменных в начале файла сценария и используйте сведения, необходимые для вашей организации. В следующих примерах предполагается, что указано имя домена вашей организации contoso.onmicrosoft.com. Убедитесь, что заключите значения для переменных с двойные кавычки (» «).</span><span class="sxs-lookup"><span data-stu-id="0743c-p109">Edit the following variables in the beginning of the script file, and use information that's specific to your organization. The following examples assume that the domain name of your organization is contoso.onmicrosoft.com. Be sure to surround the values for the variables with double-quotation marks (" ").</span></span>
    
    - <span data-ttu-id="0743c-145">**$AdminURI** — этот параметр указывает URI для службы администрирования SharePoint Online, например, `"https://contoso-admin.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="0743c-145">**$AdminURI** - This specifies the URI for your SharePoint Online admin service, for example,  `"https://contoso-admin.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="0743c-146">**$AdminAccount** - это указывает учетную запись глобального администратора в организации Office 365, например `"admin@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="0743c-146">**$AdminAccount** - This specifies a global administrator account in your Office 365 organization, for example,  `"admin@contoso.onmicrosoft.com"`.</span></span>
    
    - <span data-ttu-id="0743c-147">**$eDiscoveryUser** - это учетная запись администратора или соответствия руководителя, который будет назначен в качестве администратора семейства сайтов для каждого OneDrive для бизнеса сайта в вашей организации, например, `"annb@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="0743c-147">**$eDiscoveryUser** - This specifies the user account of an administrator or compliance manager who will be assigned as a site collection administrator for every OneDrive for Business site in your organization, for example,  `"annb@contoso.onmicrosoft.com"`.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="0743c-148">Изменение учетной записи пользователя, заданной переменной **$eDiscoveryUser** и повторно выполните скрипт, чтобы назначить другого пользователя как администратора семейства сайтов в OneDrive для бизнеса сайты, которые указаны в переменной **$MySiteListFile** .</span><span class="sxs-lookup"><span data-stu-id="0743c-148">Change the user account specified by the **$eDiscoveryUser** variable and re-run the script to assign a different user as a site collection administrator to the OneDrive for Business sites that are specified by the **$MySiteListFile** variable.</span></span> 
  
    - <span data-ttu-id="0743c-p110">**$MySitePrefix** Это URL-адрес для домена MySite вашей организации. Это домен, который содержит все OneDrive для бизнеса сайтов в вашей организации, например, `"https://contoso-my.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="0743c-p110">**$MySitePrefix**This specifies the URL for your organization's MySite domain. This is the domain that contains all the OneDrive for Business sites in your organization, for example,  `"https://contoso-my.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="0743c-p111">**$MySiteListFile** Это указывает полный путь текстовый файл, созданный на шаге 1. Этот файл содержит список OneDrive для бизнеса сайтов в вашей организации, например `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Убедитесь, что заключите значение для этой переменной с одним кавычки (""). Обратите внимание, что следует указать место сохранения текстового файла в шаге 1.</span><span class="sxs-lookup"><span data-stu-id="0743c-p111">**$MySiteListFile**This specifies the full path of the text file that you created in Step 1. This file contains a list of OneDrive for Business sites in your organization, for example,  `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Be sure to surround the value for this variable with single-quotation marks (' '). Note that you should specify the location that you saved the text file to in Step 1.</span></span>
    
3. <span data-ttu-id="0743c-p112">Сохраните текстовый файл как файл сценария PowerShell, изменив расширение его имени на PS1. Например, файл OD4BAssignSCA.txt сохраняется как OD4BAssignSCA.ps1.</span><span class="sxs-lookup"><span data-stu-id="0743c-p112">Save the text file as a PowerShell script file by changing the file name suffix to .ps1. For example, save the file OD4BAssignSCA.txt as OD4BAssignSCA.ps1.</span></span>
    
4. <span data-ttu-id="0743c-157">В командной консоли SharePoint Online перейдите к папке, содержащей сценарий PowerShell, созданный на предыдущем этапе, а затем запустите сценарий. Пример:</span><span class="sxs-lookup"><span data-stu-id="0743c-157">In SharePoint Online Management Shell, go to the folder that contains the PowerShell script that you created in the previous step, and then run the script, for example:</span></span>
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    <span data-ttu-id="0743c-p113">Будет предложено ввести пароль для учетной записи администратора, который указан в скрипте. Если сценарий выполнен успешно, сообщение `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` , отображаемых для каждого OneDrive для бизнеса сайт, указанный в входного файла, указанного идентификатором **$MySiteListFile**.</span><span class="sxs-lookup"><span data-stu-id="0743c-p113">You will be prompted to enter the password for the administrator account that you specified in the script. If the script runs successfully, the message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` is displayed for each OneDrive for Business site that's listed in the input file specified by **$MySiteListFile**.</span></span>

## <a name="more-information"></a><span data-ttu-id="0743c-160">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="0743c-160">More information</span></span>

- <span data-ttu-id="0743c-p114">Скрипта, выполняемого на шаге 3 с помощью командлета **Set-SPOUser** назначение указанного пользователя как администратора семейства сайтов в каждом OneDrive для бизнеса, указанный в файл, указанный в переменной **$MySiteListFile** . Если имеется очень большой организации с помощью тысяч пользователей, попробуйте выполнить следующие действия, чтобы упростить управление предоставление разрешений для обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="0743c-p114">The script that you ran in Step 3 uses the **Set-SPOUser** cmdlet to assign the specified user as a site collection administrator to every OneDrive for Business that's listed in the file specified by the **$MySiteListFile** variable. If you have a very large organization with thousands of users, consider doing the following to make it easier to manage assigning eDiscovery permissions.</span></span> 
    
  - <span data-ttu-id="0743c-163">Отредактируйте файл, созданный на шаге 1, содержащий список OneDrive для бизнеса сайтов, чтобы оно включало только тех сайтов для пользователей, что, участвующие в активной юридических случаев.</span><span class="sxs-lookup"><span data-stu-id="0743c-163">Edit the file that you created in Step 1 that contains the list of OneDrive for Business sites so that it includes only the sites for users are that are involved in active legal cases.</span></span>
    
  - <span data-ttu-id="0743c-p115">Назначение разрешений не более чем 2500 OneDrive для бизнеса сайтов в день. Например предположим, у вас есть 10 000 OneDrive для бизнеса сайтов в вашей организации. Можно создать список на шаге 1 необходимо собрать все сайты. Затем можно использовать этот файл для создания четыре файла, которые содержат 2500 пользователей. С первого дня будет выполняться скрипт в шаге 3 для назначения разрешений сначала 2500 OneDrive для бизнеса сайтов. На второй день выполните скрипт Далее 2500 onedrive для бизнеса сайтов и так далее.</span><span class="sxs-lookup"><span data-stu-id="0743c-p115">Assign permissions to no more than 2,500 OneDrive for Business sites per day. For example, let's say you have 10,000 OneDrive for Business sites in your organization. You could create the list in Step 1 to collect all the sites. Then you could use that file to create four files that each contain 2,500 users. On the first day, you would run the script in Step 3 to assign permissions to the first 2,500 OneDrive for Business sites. On the second day, you would run the script for the next 2,500 OneDrive for Business sites, and so on.</span></span>
    
- <span data-ttu-id="0743c-p116">Вести запись OneDrive для бизнеса сайтов, которые были им назначены разрешения обнаружения электронных данных и пользователя, который назначен в качестве администратора семейства сайтов. Например после назначения разрешений можно Сохраните текстовый файл, содержащий список OneDrive для бизнеса сайтов и добавьте строку к нему, которое идентифицирует пользователя, который назначен в качестве администратора семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="0743c-p116">Keep a record of the OneDrive for Business sites that were assigned eDiscovery permissions and the user who is assigned as the site collection administrator. For example, after you assign permissions, you can save the text file that contains the list of OneDrive for Business sites and add a line to it that identifies the user who is assigned as the site collection administrator.</span></span>
    
- <span data-ttu-id="0743c-p117">Пользователи могут просматривать список administators семейства сайтов для их OneDrive для бизнеса сайта. Поскольку пользователи, администратор семейства сайтов для собственных OneDrive для бизнеса сайта, их удаление администраторов семейства сайтов. Попробуйте выполнить следующие действия, чтобы снизить вероятность пользователи удаление пользователей, которым назначена разрешения обнаружения электронных данных в OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="0743c-p117">Users can view the list of site collection administators for their OneDrive for Business site. Because users are site collection administrator for their own OneDrive for Business site, they can remove site collection administrators. Consider doing the following to mitigate the chance of users removing the user who is assigned eDiscovery permissions to OneDrive for Business sites.</span></span>
    
  - <span data-ttu-id="0743c-175">Сообщите пользователям, что в целях обнаружения электронных данных и обеспечения соответствия требованиям, специалисты по соответствию требованиям была назначена администратором семейства сайтов в OneDrive для бизнеса сайтов в вашей организации.</span><span class="sxs-lookup"><span data-stu-id="0743c-175">Communicate to users that for eDiscovery and compliance purposes, a compliance officer has been assigned as a site collection administrator to OneDrive for Business sites in your organization.</span></span>
    
  - <span data-ttu-id="0743c-176">Повторно запустите скрипт в шаге 3, если необходимо, чтобы повторно назначить пользователя как администратора семейства сайтов для OneDrive для бизнеса сайтов.</span><span class="sxs-lookup"><span data-stu-id="0743c-176">Re-run the script in Step 3, if necessary, to re-assign a user as the site collection administrator for OneDrive for Business sites.</span></span>
    
- <span data-ttu-id="0743c-p118">Можно также использовать скрипта, выполняемого на шаге 3 для удаления пользователя как администратора семейства сайтов из службы OneDrive для бизнеса сайтов. Чтобы удалить пользователя как администратора семейства сайтов, необходимо изменить следующую команду (в конце скрипта) из:</span><span class="sxs-lookup"><span data-stu-id="0743c-p118">You can also use the script that you ran in Step 3 to remove a user as the site collection administrator from OneDrive for Business sites. To remove a user as a site collection administrator, you have to change the following command (near the end of the script) from:</span></span> 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    <span data-ttu-id="0743c-179">на:</span><span class="sxs-lookup"><span data-stu-id="0743c-179">to:</span></span>
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    <span data-ttu-id="0743c-180">Кроме того, можно изменить следующую строку с:</span><span class="sxs-lookup"><span data-stu-id="0743c-180">You can also change the following line in the script from:</span></span>

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    <span data-ttu-id="0743c-181">на:</span><span class="sxs-lookup"><span data-stu-id="0743c-181">to:</span></span>
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    <span data-ttu-id="0743c-182">После внесения изменений сохранить сценарий с другим именем, например OD4BRemoveSCA.ps1 и затем использовать его для удаления пользователя из группы OneDrive для бизнеса сайтов как администратора семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="0743c-182">After you make these changes, save the script with a different name, such as OD4BRemoveSCA.ps1, and then use it to remove a user as a site collection administrator from a group of OneDrive for Business sites.</span></span>
