---
title: Развертывание соединителя для архивации данных Facebook в Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
ROBOTS: NOINDEX, NOFOLLOW
description: Администраторы могут настроить собственный соединитель для импорта и архивации бизнес-страниц Facebook в Office 365. После импорта этих данных в Office 365 вы можете использовать такие функции обеспечения соответствия, как судебное удержание, поиск контента и политики хранения, для управления управлением данными Facebook Организации.
ms.openlocfilehash: d90714072bdeb609fe4af14208476bfa2f60b6d7
ms.sourcegitcommit: 63a10dc5ffa9d709fac437d3fc9e554b1bcd826f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/25/2019
ms.locfileid: "33308264"
---
# <a name="deploy-a-connector-to-archive-facebook-data-in-office-365"></a><span data-ttu-id="e8e43-104">Развертывание соединителя для архивации данных Facebook в Office 365</span><span class="sxs-lookup"><span data-stu-id="e8e43-104">Deploy a connector to archive Facebook data in Office 365</span></span>

<span data-ttu-id="e8e43-105">В этой статье представлено пошаговое руководство по развертыванию соединителя, использующего службу импорта Office 365 для импорта данных из бизнес-страниц Facebook в Office 365.</span><span class="sxs-lookup"><span data-stu-id="e8e43-105">This article contains the step-by-step process to deploy a connector that uses the Office 365 Import service to import data from Facebook Business pages to Office 365.</span></span> <span data-ttu-id="e8e43-106">Общий обзор этого процесса и список необходимых компонентов, необходимых для развертывания соединителя Facebook, приведены в статье [Использование образцов соединителей для архивации сторонних данных в Office 365](archive-third-party-data-with-sample-connector.md).</span><span class="sxs-lookup"><span data-stu-id="e8e43-106">For a high-level overview of this process and a list of prerequisites required to deploy a Facebook connector, see [Use sample connectors to archive third-party data in Office 365](archive-third-party-data-with-sample-connector.md).</span></span> 


## <a name="step-1-download-the-package"></a><span data-ttu-id="e8e43-107">Шаг 1: Загрузка пакета</span><span class="sxs-lookup"><span data-stu-id="e8e43-107">Step 1: Download the package</span></span>

<span data-ttu-id="e8e43-108">Скачайте предварительно подготовленный пакет из раздела Release в репозиторий по адресу <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>.</span><span class="sxs-lookup"><span data-stu-id="e8e43-108">Download the prebuilt package from repository’s Release section at <https://github.com/Microsoft/m365-sample-connector-csharp-aspnet/releases>.</span></span> <span data-ttu-id="e8e43-109">В последнем выпуске Скачайте ZIP-файл с именем **самплеконнектор. zip**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-109">Under the latest release, download the zip file named **SampleConnector.zip**.</span></span> <span data-ttu-id="e8e43-110">Вы будете отправлять этот ZIP-файл в Azure на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="e8e43-110">You will upload this zip file to Azure in Step 4.</span></span>

## <a name="step-2-create-an-app-in-azure-active-directory"></a><span data-ttu-id="e8e43-111">Шаг 2: создание приложения в Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="e8e43-111">Step 2: Create an app in Azure Active Directory</span></span>

1. <span data-ttu-id="e8e43-112">Перейдите на <https://portal.azure.com> страницу и войдите, используя учетные данные глобального администратора Office 365.</span><span class="sxs-lookup"><span data-stu-id="e8e43-112">Go to <https://portal.azure.com> and sign in using the credentials of an Office 365 global admin account.</span></span>

    ![Создание приложения в AAD](media/FBCimage1.png)

2. <span data-ttu-id="e8e43-114">В области навигации слева выберите **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-114">In the left navigation pane, click **Azure Active Directory**.</span></span>

    ![](media/FBCimage2.png)

3. <span data-ttu-id="e8e43-115">В левой области навигации щелкните **Регистрация приложений (предварительНая версия)** , а затем нажмите кнопку **создать регистрацию**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-115">In the left navigation pane, click **App registrations (Preview)** and then click **New registration**.</span></span>

    ![](media/FBCimage3.png)

4. <span data-ttu-id="e8e43-116">ЗаРегистрируйте приложение.</span><span class="sxs-lookup"><span data-stu-id="e8e43-116">Register the application.</span></span> <span data-ttu-id="e8e43-117">В разделе URI переНаправления выберите пункт веб-сайт в раскрывающемся списке Тип <https://portal.azure.com> приложения, а затем введите в поле для URI.</span><span class="sxs-lookup"><span data-stu-id="e8e43-117">Under Redirect URI, select Web in the application type dropdown list and then type <https://portal.azure.com> in the box for the URI.</span></span>

   ![](media/FBCimage4.png)

5. <span data-ttu-id="e8e43-118">Скопируйте идентификатор **приложения (идентификатор клиента)** и **идентификатор каталога (клиента)** и сохраните их в текстовый файл или другое надежное расположение.</span><span class="sxs-lookup"><span data-stu-id="e8e43-118">Copy the **Application (client) ID** and **Directory (tenant) ID** and save them to a text file or other safe location.</span></span> <span data-ttu-id="e8e43-119">Эти идентификаторы будут использоваться на последующих этапах.</span><span class="sxs-lookup"><span data-stu-id="e8e43-119">You’ll use these IDs in later steps.</span></span>

   ![](media/FBCimage5.png)

6. <span data-ttu-id="e8e43-120">Перейдите в раздел **Сертификаты _амп_ секреты для нового приложения.**</span><span class="sxs-lookup"><span data-stu-id="e8e43-120">Go to **Certificates & secrets for the new app.**</span></span>

   ![](media/FBCimage6.png)

7. <span data-ttu-id="e8e43-121">Щелкните **новый секрет клиента**</span><span class="sxs-lookup"><span data-stu-id="e8e43-121">Click **New client secret**</span></span>

   ![](media/FBCimage7.png)

8. <span data-ttu-id="e8e43-122">Создайте новый секрет.</span><span class="sxs-lookup"><span data-stu-id="e8e43-122">Create a new secret.</span></span> <span data-ttu-id="e8e43-123">В поле Описание введите секрет, а затем выберите срок действия.</span><span class="sxs-lookup"><span data-stu-id="e8e43-123">In the description box, type the secret and then choose an expiration period.</span></span> 

    ![](media/FBCimage8.png)

9. <span data-ttu-id="e8e43-124">Скопируйте значение секрета и сохраните его в текстовый файл или другое место хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-124">Copy the value of the secret and save it to a text file or other storage location.</span></span> <span data-ttu-id="e8e43-125">Это секрет приложения AAD, который вы будете использовать на последующих этапах.</span><span class="sxs-lookup"><span data-stu-id="e8e43-125">This is the AAD application secret that you will use in later steps.</span></span>

   ![](media/FBCimage9.png)

10. <span data-ttu-id="e8e43-126">Перейдите к **манифесту** и скопируйте с identifieruris (который также называется URI приложения AAD), выделенный на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="e8e43-126">Go to **Manifest** and copy the identifierUris (which is also called the AAD application Uri) as highlighted in the following screenshot.</span></span> <span data-ttu-id="e8e43-127">Скопируйте универсальный код ресурса (URI) приложения AAD в текстовый файл или другое место хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-127">Copy the AAD application Uri to a text file or other storage location.</span></span> <span data-ttu-id="e8e43-128">Вы будете использовать его в действии 6.</span><span class="sxs-lookup"><span data-stu-id="e8e43-128">You’ll use it in Step 6.</span></span>

   ![](media/FBCimage10.png)

## <a name="step-3-create-an-azure-storage-account"></a><span data-ttu-id="e8e43-129">Шаг 3: создание учетной записи хранения Azure</span><span class="sxs-lookup"><span data-stu-id="e8e43-129">Step 3: Create an Azure storage account</span></span>

1. <span data-ttu-id="e8e43-130">Перейдите на домашнюю страницу Azure для своей организации.</span><span class="sxs-lookup"><span data-stu-id="e8e43-130">Go to the Azure home page for your organization.</span></span>

    ![](media/FBCimage11.png)

2. <span data-ttu-id="e8e43-131">Выберите **создать ресурс** и введите учетную **запись хранения** в поле поиска.</span><span class="sxs-lookup"><span data-stu-id="e8e43-131">Click **Create a resource** and they type **storage account** in the search box.</span></span>

    ![](media/FBCimage12.png)

3. <span data-ttu-id="e8e43-132">Щелкните **хранилище**, а затем выберите **учетная запись хранилища**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-132">Click **Storage**, and then click **Storage account**.</span></span>

    ![](media/FBCimage13.png)

4. <span data-ttu-id="e8e43-133">На странице " **Создание учетной записи хранения** " в поле подписка выберите вариант **Оплата от имени** или **бесплатной пробной версии** в зависимости от того, какой тип подписки Azure вы используете.</span><span class="sxs-lookup"><span data-stu-id="e8e43-133">On the **Create storage account** page, in the Subscription box, select **Pay-As-You-Go** or **Free Trial** depending on which type of Azure subscription you have.</span></span> <span data-ttu-id="e8e43-134">Затем выберите или создайте группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8e43-134">Then select or create a resource group.</span></span>

    ![](media/FBCimage14.png)

5. <span data-ttu-id="e8e43-135">Введите имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-135">Type a name for the storage account.</span></span>

    ![](media/FBCimage15.png)

6. <span data-ttu-id="e8e43-136">Просмотрите, а затем нажмите кнопку **создать** , чтобы создать учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-136">Review and then click **Create** to create the storage account.</span></span>

    ![](media/FBCimage16.png)

7. <span data-ttu-id="e8e43-137">Через несколько секунд нажмите кнопку **Обновить** , а затем выберите **Перейти** к ресурсу, чтобы перейти к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-137">After a few moments, click **Refresh** and then click **Go to resource** to navigate to the storage account.</span></span>

    ![](media/FBCimage17.png)

8. <span data-ttu-id="e8e43-138">Нажмите **клавиши доступа** в левой области навигации.</span><span class="sxs-lookup"><span data-stu-id="e8e43-138">Click **Access keys** in the left navigation pane.</span></span>

    ![](media/FBCimage18.png)

9. <span data-ttu-id="e8e43-139">Скопируйте **строку подключения** и сохраните ее в текстовый файл или другое место хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-139">Copy a **Connection string** and save it to a text file or other storage location.</span></span> <span data-ttu-id="e8e43-140">Этот параметр используется при создании ресурса веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-140">You’ll use this when creating a web app resource.</span></span>

    ![](media/FBCimage19.png)

## <a name="step-4-create-a-new-web-app-resource-in-azure"></a><span data-ttu-id="e8e43-141">Шаг 4: создание нового ресурса веб-приложения в Azure</span><span class="sxs-lookup"><span data-stu-id="e8e43-141">Step 4: Create a new web app resource in Azure</span></span>

1. <span data-ttu-id="e8e43-142">На **домашней** странице на портале Azure выберите **создать веб-приложение " \> все \> ресурсы**".</span><span class="sxs-lookup"><span data-stu-id="e8e43-142">On the **Home** page in the Azure portal, click **Create a resource \> Everything \> Web app**.</span></span> <span data-ttu-id="e8e43-143">На странице **веб-приложение** нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-143">On the **Web app** page, click **Create**.</span></span> 

   ![](media/FBCimage20.png)

2. <span data-ttu-id="e8e43-144">ЗаПолните сведения (как показано ниже) и создайте веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="e8e43-144">Fill in the details (as shown below) and then create the Web app.</span></span> <span data-ttu-id="e8e43-145">Обратите внимание, что имя, введенное в поле **имя приложения** , будет использоваться для создания URL-адреса службы приложений Azure; Например, fbconnector.azurewebsites.NET.</span><span class="sxs-lookup"><span data-stu-id="e8e43-145">Note that the name that you enter in the **App name** box will be used to create the Azure app service URL; for example fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage21.png)

3. <span data-ttu-id="e8e43-146">Перейдите к только что созданному ресурсу веб-приложения, щелкните **Параметры приложения** в левой области навигации.</span><span class="sxs-lookup"><span data-stu-id="e8e43-146">Go to the newly created web app resource, click **Application Settings** in the left navigation pane.</span></span> <span data-ttu-id="e8e43-147">В разделе Параметры приложения щелкните Добавить новый параметр и добавьте следующие три параметра.</span><span class="sxs-lookup"><span data-stu-id="e8e43-147">Under Application settings, click Add new setting and add the following three settings.</span></span> <span data-ttu-id="e8e43-148">Используйте значения (скопированные в текстовый файл из предыдущих шагов):</span><span class="sxs-lookup"><span data-stu-id="e8e43-148">Use the values (that you copied to the text file from the previous steps):</span></span> 

    - <span data-ttu-id="e8e43-149">**Аписекреткэй** — в качестве секрета можно ввести любое значение.</span><span class="sxs-lookup"><span data-stu-id="e8e43-149">**APISecretKey** – You can type any value as the secret.</span></span> <span data-ttu-id="e8e43-150">Он будет использоваться для доступа к веб-приложению Connector на шаге 7.</span><span class="sxs-lookup"><span data-stu-id="e8e43-150">This will be used to access the connector web app in Step 7.</span></span>

    - <span data-ttu-id="e8e43-151">**Сторажеаккаунтконнектионстринг** — универсальный код ресурса (URI) строки подключения, скопированный после создания учетной записи хранилища Azure на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="e8e43-151">**StorageAccountConnectionString** – The connection string Uri that you copied after creating the Azure storage account in Step 3.</span></span>

    - <span data-ttu-id="e8e43-152">**tenantId** — идентификатор клиента организации Office 365, который вы скопировали после создания приложения соединителя Facebook в Azure Active Directory в действии 2.</span><span class="sxs-lookup"><span data-stu-id="e8e43-152">**tenantId** – The tenant ID of your Office 365 organization that you copied after creating the Facebook connector app in Azure Active Directory in Step 2.</span></span>

    ![](media/FBCimage22.png)

4. <span data-ttu-id="e8e43-153">В разделе **Общие параметры**нажмите \*\*\*\* кнопку рядом с параметрОм **Always On (включено**).</span><span class="sxs-lookup"><span data-stu-id="e8e43-153">Under **General settings**, click **On** next to the **Always On**.</span></span> <span data-ttu-id="e8e43-154">В верхней части страницы нажмите кнопку **сохранить** , чтобы сохранить параметры аппликатон.</span><span class="sxs-lookup"><span data-stu-id="e8e43-154">Click **Save** at the top of the page to save applicaton settings.</span></span>

   ![](media/FBCimage23.png)

5. <span data-ttu-id="e8e43-155">Последним шагом является отправка исходного кода приложения соединителя в Azure, который был загружен в действии 1.</span><span class="sxs-lookup"><span data-stu-id="e8e43-155">The final step is to upload the connector app source code to Azure that you downloaded in Step 1.</span></span> <span data-ttu-id="e8e43-156">В веб-браузере перейдите по адресу<AzureAppResourceName>https://. SCM.azurewebsites.NET/ZipDeployUi.</span><span class="sxs-lookup"><span data-stu-id="e8e43-156">In a web browser, go to https://<AzureAppResourceName>.scm.azurewebsites.net/ZipDeployUi.</span></span> <span data-ttu-id="e8e43-157">Например, если имя ресурса приложения Azure (с именем, указанным в шаге 2 в этом разделе) — **фбконнектор**, перейдите на https://fbconnector.scm.azurewebsites.net/ZipDeployUiстраницу.</span><span class="sxs-lookup"><span data-stu-id="e8e43-157">For example, if the name of your Azure app resource (which you named in step 2 in this section) is **fbconnector**, then you would go to https://fbconnector.scm.azurewebsites.net/ZipDeployUi.</span></span> 

6. <span data-ttu-id="e8e43-158">Перетащите Самплеконнектор. zip (, скачанный на шаге 1) на эту страницу.</span><span class="sxs-lookup"><span data-stu-id="e8e43-158">Drag and drop the SampleConnector.zip (that you downloaded in Step 1) to this page.</span></span> <span data-ttu-id="e8e43-159">После отправки файлов и успешного развертывания страница будет выглядеть примерно так, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="e8e43-159">After the files are uploaded and the deployment is successful, the page will look similar to the following screenshot.</span></span>

   ![](media/FBCimage24.png)

## <a name="step-5-register-the-facebook-app"></a><span data-ttu-id="e8e43-160">Шаг 5: регистрация приложения Facebook</span><span class="sxs-lookup"><span data-stu-id="e8e43-160">Step 5: Register the Facebook app</span></span>

1. <span data-ttu-id="e8e43-161">Перейдите к <https://developers.facebook.com> , войдите в систему, используя учетные данные для учетной записи для бизнес-страниц Facebook вашей организации, а затем щелкните **Добавить новое приложение**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-161">Go to <https://developers.facebook.com> , log in using the credentials for the account for your organization’s Facebook Business pages, and then click **Add New App**.</span></span>

   ![](media/FBCimage25.png)

2. <span data-ttu-id="e8e43-162">Создайте идентификатор нового приложения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-162">Create a new app ID.</span></span>

   ![](media/FBCimage26.png)

3. <span data-ttu-id="e8e43-163">В левой области навигации щелкните **Добавить продукты** , а затем — **Настройка** на плитке **входа Facebook** .</span><span class="sxs-lookup"><span data-stu-id="e8e43-163">In the left navigation pane, click **Add Products** and then click **Set Up** in the **Facebook Login** tile.</span></span>

   ![](media/FBCimage27.png)

4. <span data-ttu-id="e8e43-164">На странице Интеграция входа в Facebook нажмите кнопку **веб**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-164">On the Integrate Facebook Login page, click **Web**.</span></span>

   ![](media/FBCimage28.png)

5. <span data-ttu-id="e8e43-165">Добавьте URL-адрес службы приложений Azure; например https://fbconnector.azurewebsites.net:.</span><span class="sxs-lookup"><span data-stu-id="e8e43-165">Add the Azure app service URL; for example https://fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage29.png)

6. <span data-ttu-id="e8e43-166">ЗаПолните раздел Краткое руководство по настройке входа в Facebook.</span><span class="sxs-lookup"><span data-stu-id="e8e43-166">Complete the QuickStart section of the Facebook Login setup.</span></span>

   ![](media/FBCimage30.png)

7. <span data-ttu-id="e8e43-167">В левой области навигации в разделе **Login Facebook**щелкните **Параметры**, а затем добавьте URI перенаправления OAuth в поле **допустимые URI перенаправления OAuth** ; Используйте формат \*\* \<коннекторсервицеури_гт_/views/фацебукоаус\*\*, где значением коннекторсервицеури является URL-адрес службы приложений Azure для вашей организации; например https://fbconnector.azurewebsites.net:.</span><span class="sxs-lookup"><span data-stu-id="e8e43-167">In the left navigation pane under **Facebook Login**, click **Settings**, and add the OAuth redirect URI in the **Valid OAuth Redirect URIs** box; use the format **\<connectorserviceuri>/Views/FacebookOAuth**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example https://fbconnector.azurewebsites.net.</span></span>

   ![](media/FBCimage31.png)

8. <span data-ttu-id="e8e43-168">В левой области навигации щелкните **Добавить продукты** и выберите **веб-перехватчики.**</span><span class="sxs-lookup"><span data-stu-id="e8e43-168">In the left navigation pane, click **Add Products** and then click **Webhooks.**</span></span> <span data-ttu-id="e8e43-169">В раскрывающемся меню **Page (страница** ) выберите пункт **Page (страница**).</span><span class="sxs-lookup"><span data-stu-id="e8e43-169">In the **Page** pull-down menu, click **Page**.</span></span> 

   ![](media/FBCimage32.png)

9. <span data-ttu-id="e8e43-170">Добавьте URL-адрес обратного вызова для веб-перехватчиков и добавьте маркер проверки.</span><span class="sxs-lookup"><span data-stu-id="e8e43-170">Add Webhooks Callback URL and add a verify token.</span></span> <span data-ttu-id="e8e43-171">Формат URL-адреса обратного вызова, используйте формат \*\* <connectorserviceuri>/АПИ/фбпажевебхук\*\*, где значение параметра коннекторсервицеури — это URL-адрес службы приложений Azure для вашей организации; например https://fbconnector.azurewebsites.net:.</span><span class="sxs-lookup"><span data-stu-id="e8e43-171">The format of the callback URL, use the format **<connectorserviceuri>/api/FbPageWebhook**, where the value for connectorserviceuri is the Azure app service URL for your organization; for example https://fbconnector.azurewebsites.net.</span></span> 

    <span data-ttu-id="e8e43-172">Маркер проверки должен быть похож на надежный пароль.</span><span class="sxs-lookup"><span data-stu-id="e8e43-172">The verify token should similar to a strong password.</span></span> <span data-ttu-id="e8e43-173">Скопируйте токен проверки в текстовый файл или другое место хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-173">Copy the verify token to a text file or other storage location.</span></span>

     ![](media/FBCimage33.png)

10. <span data-ttu-id="e8e43-174">ПроТестируйте и подпишитесь на конечную точку для веб-канала.</span><span class="sxs-lookup"><span data-stu-id="e8e43-174">Test and subscribe to the endpoint for feed.</span></span>

    ![](media/FBCimage34.png)

11. <span data-ttu-id="e8e43-175">Добавьте URL-адрес конфиденциальности, значок приложения и использование для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="e8e43-175">Add a privacy URL, app icon, and business use.</span></span> <span data-ttu-id="e8e43-176">Кроме того, скопируйте идентификатор приложения и секрет приложения в текстовый файл или другое место хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-176">Also, copy the app ID and app secret to a text file or other storage location.</span></span>

    ![](media/FBCimage35.png)

12. <span data-ttu-id="e8e43-177">Сделайте приложение общедоступным.</span><span class="sxs-lookup"><span data-stu-id="e8e43-177">Make the app public.</span></span>

    ![](media/FBCimage36.png)

13. <span data-ttu-id="e8e43-178">Добавьте пользователя к роли администратора или тестера.</span><span class="sxs-lookup"><span data-stu-id="e8e43-178">Add user to the admin or tester role.</span></span>

    ![](media/FBCimage37.png)

14. <span data-ttu-id="e8e43-179">Добавьте разрешение на **доступ к общему содержимОму страницы** .</span><span class="sxs-lookup"><span data-stu-id="e8e43-179">Add the **Page Public Content Access** permission.</span></span>

    ![](media/FBCimage38.png)

15. <span data-ttu-id="e8e43-180">Разрешение "добавить Управление страницами".</span><span class="sxs-lookup"><span data-stu-id="e8e43-180">Add Manage Pages permission.</span></span>

    ![](media/FBCimage39.png)

16. <span data-ttu-id="e8e43-181">Получение приложения, проверенного Facebook.</span><span class="sxs-lookup"><span data-stu-id="e8e43-181">Get the application reviewed by Facebook.</span></span>

    ![](media/FBCimage40.png)

## <a name="step-6-configure-the-connector-web-app"></a><span data-ttu-id="e8e43-182">Шаг 6: Настройка соединительного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="e8e43-182">Step 6: Configure the connector web app</span></span>

1. <span data-ttu-id="e8e43-183">Перейдите в раздел\<HTTPS://азуреаппресаурценаме_гт_. азуревебситес. NET (где азуреаппресаурценаме — это имя ресурса приложения Azure, которое вы назвали на шаге 4) например, если имя имеет значение **фбконнектор**, перейдите на https://fbconnector.azurewebsites.netстраницу.</span><span class="sxs-lookup"><span data-stu-id="e8e43-183">Go to https://\<AzureAppResourceName>.azurewebsites.net (where AzureAppResourceName is the name of your Azure app resource that you named in Step 4) For example, if the name is **fbconnector**, go to https://fbconnector.azurewebsites.net.</span></span> <span data-ttu-id="e8e43-184">Домашняя страница приложения будет выглядеть так, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="e8e43-184">The home page of the app will look like the following screenshot.</span></span>


  ![](media/FBCimage41.png)

2. <span data-ttu-id="e8e43-185">Нажмите кнопку **настроить** , чтобы отобразить страницу входа.</span><span class="sxs-lookup"><span data-stu-id="e8e43-185">Click **Configure** to display a sign in page.</span></span>
 
   ![](media/FBCimage42.png)

3. <span data-ttu-id="e8e43-186">В поле Идентификатор клиента введите или вставьте идентификатор клиента (полученный на шаге 2).</span><span class="sxs-lookup"><span data-stu-id="e8e43-186">In the Tenant Id box, type or paste your tenant Id (that you obtained in Step 2).</span></span> <span data-ttu-id="e8e43-187">В поле Пароль введите или вставьте Аписекреткэй (полученное в действии 2), а затем нажмите кнопку **Настройка параметров конфигурации** , чтобы отобразить страницу **сведений о конфигурации** .</span><span class="sxs-lookup"><span data-stu-id="e8e43-187">In the password box, type or paste the APISecretKey (that you obtained in Step 2), and then click **Set Configuration Settings** to display the **Configuration Details** page.</span></span>

    ![](media/FBCimage43.png)


4. <span data-ttu-id="e8e43-188">В разделе **сведения о конфигурации**введите следующие параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e8e43-188">Under **Configuration Details**, enter the following configuration settings</span></span> 

   - <span data-ttu-id="e8e43-189">**Application ID Application ID** — идентификатор приложения для приложения Facebook, полученного в шаге 5.</span><span class="sxs-lookup"><span data-stu-id="e8e43-189">**Facebook application ID** - The app ID for the Facebook application that you obtained in Step 5.</span></span>
   - <span data-ttu-id="e8e43-190">**Секрет приложения Facebook** — секрет приложения для приложения Facebook, полученного в действии 5.</span><span class="sxs-lookup"><span data-stu-id="e8e43-190">**Facebook application secret** - The app secret for the Facebook application that you obtained in Step 5.</span></span>
   - <span data-ttu-id="e8e43-191">**Веб-перехватчики Facebook проверьте токен** — маркер проверки, созданный на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="e8e43-191">**Facebook webhooks verify token** - The verify token that you created in Step 5.</span></span>
   - <span data-ttu-id="e8e43-192">**Идентификатор приложения AAD** — идентификатор приложения для приложения Azure Active Directory, созданного в шаге 2.</span><span class="sxs-lookup"><span data-stu-id="e8e43-192">**AAD application ID** - The application ID for the Azure Active Directory app that you created in Step 2</span></span>
   - <span data-ttu-id="e8e43-193">**Секрет приложения AAD** — значение для секрета аписекреткэй, созданного на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="e8e43-193">**AAD application secret** - The value for the APISecretKey secret that you created in Step 4.</span></span>
   - <span data-ttu-id="e8e43-194">**URI приложения AAD** — URI приложения AAD, полученный в шаге 2. Пример: https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span><span class="sxs-lookup"><span data-stu-id="e8e43-194">**AAD application Uri** - The AAD application Uri obtained in Step 2; for example, https://microsoft.onmicrosoft.com/2688yu6n-12q3-23we-e3ee-121111123213.</span></span>
   - <span data-ttu-id="e8e43-195">**Ключ инструментирования Application Insights** — оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="e8e43-195">**App insights instrumentation key** - Leave this box blank.</span></span>

5. <span data-ttu-id="e8e43-196">Нажмите кнопку **сохранить** , чтобы сохранить параметры соединителя.</span><span class="sxs-lookup"><span data-stu-id="e8e43-196">Click **Save** to save the connector settings.</span></span>

## <a name="step-7-set-up-a-custom-connector-in-the-security--compliance-center"></a><span data-ttu-id="e8e43-197">Шаг 7: Настройка настраиваемого соединителя в центре безопасности _Амп_ соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="e8e43-197">Step 7: Set up a custom connector in the Security & Compliance Center</span></span>

1. <span data-ttu-id="e8e43-198">Перейдите в <https://protection.office.com> раздел **Управление \> данными и выберите пункт \> архивы импорта данных сторонних поставщиков**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-198">Go to <https://protection.office.com> and then click **Data governance \> Import \> Archive third-party data**.</span></span>

   ![](media/FBCimage44.png)

2.  <span data-ttu-id="e8e43-199">Нажмите кнопку **Добавить соединитель** , а затем \*\*\*\* выберите пункт Настраиваемая.</span><span class="sxs-lookup"><span data-stu-id="e8e43-199">Click **Add a connector** and then click **Custom**.</span></span>

    ![](media/FBCimage46.png)

3.  <span data-ttu-id="e8e43-200">На странице **Добавление приложения соединителя** введите следующие сведения и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-200">On the **Add Connector App** page, enter the following information and then click **Next**.</span></span>

    - <span data-ttu-id="e8e43-201">В первом поле введите имя соединителя, например **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-201">In the first box, type a name for the connector, such as **Facebook**.</span></span>
    - <span data-ttu-id="e8e43-202">Во втором поле введите или вставьте значение Аписекреткэй, добавленное на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="e8e43-202">In the second box, type or paste the value of the APISecretKey that you added in Step 4.</span></span>
    - <span data-ttu-id="e8e43-203">В третьем поле введите URL-адрес службы приложений Azure. например **https://fbconnector.azurewebsites.net**:.</span><span class="sxs-lookup"><span data-stu-id="e8e43-203">In the third box, type of paste the Azure app service URL; for example **https://fbconnector.azurewebsites.net**.</span></span>
    
    ![](media/FBCimage47.png)

4.  <span data-ttu-id="e8e43-204">Щелкните **имя входа с приложением Connector Connector**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-204">Click **Login with Connector App**.</span></span>

    ![](media/FBCimage45.png)

5. <span data-ttu-id="e8e43-205">Введите или вставьте Аписекреткэй еще раз, а затем щелкните **Вход в службу соединителя**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-205">Type or paste the APISecretKey again and then click  **Login to Connector Service**.</span></span>

   ![](media/FBCimage48.png)


6. <span data-ttu-id="e8e43-206">Выберите **Вход с помощью Facebook.**</span><span class="sxs-lookup"><span data-stu-id="e8e43-206">Click **Login with Facebook.**</span></span>

   ![](media/FBCimage49.png)

7. <span data-ttu-id="e8e43-207">На странице **Вход в Facebook** Войдите в систему, используя учетные данные для учетной записи для бизнес-страниц Facebook вашей организации.</span><span class="sxs-lookup"><span data-stu-id="e8e43-207">On the **Log in to Facebook** page, log in using the credentials for the account for your organization’s Facebook Business pages.</span></span> <span data-ttu-id="e8e43-208">Убедитесь, что учетной записи Facebook, в которой вы вошли в систему, назначена роль администратора для бизнес-страниц Facebook Организации.</span><span class="sxs-lookup"><span data-stu-id="e8e43-208">Make sure the Facebook account you logged in to is assigned the admin role for your organization’s Facebook Business pages</span></span>

   ![](media/FBCimage50.png)

8. <span data-ttu-id="e8e43-209">Нажмите кнопку **Выбор страниц** , чтобы выбрать деловые страницы Организации, которые нужно архивировать в Office 365.</span><span class="sxs-lookup"><span data-stu-id="e8e43-209">Click **Select Pages** to choose your organization’s business pages that you want to archive in Office 365.</span></span>

   ![](media/FBCimage51.png)

9. <span data-ttu-id="e8e43-210">Отображается список бизнес-страниц, управляемых учетной записью Facebook, в которой выполнен вход.</span><span class="sxs-lookup"><span data-stu-id="e8e43-210">A list of the Business pages managed by the Facebook account that you logged in to is displayed.</span></span> <span data-ttu-id="e8e43-211">Выберите страницу для архивации и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-211">Select the page to archive and then click **Save**.</span></span>

    ![](media/FBCimage52.png)

10. <span data-ttu-id="e8e43-212">Нажмите кнопку **Готово** , чтобы выйти из программы установки приложения службы соединителя.</span><span class="sxs-lookup"><span data-stu-id="e8e43-212">Click **Finish** to exit the setup of the connector service app.</span></span>

    ![](media/FBCimage53.png)

11. <span data-ttu-id="e8e43-213">На странице " **Настройка фильтров** " можно применить фильтр для импорта (и архивирования) элементов с определенным сроком хранения.</span><span class="sxs-lookup"><span data-stu-id="e8e43-213">On the **Set Filters** page, you can apply a filter to import (and archive) items that are a certain age.</span></span> <span data-ttu-id="e8e43-214">Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e8e43-214">Click **Next**.</span></span>

    ![](media/FBCimage54.png)

12. <span data-ttu-id="e8e43-215">На странице " **Настройка учетНой записи хранения** " выберите почтовый ящик Office 365, в который будут импортированы элементы из ранее выбранных страниц Facebook бизнес-страниц.</span><span class="sxs-lookup"><span data-stu-id="e8e43-215">On the **Set Storage Account** page, select the Office 365 mailbox that the items from the Facebook Business pages that you previously selected will be imported to.</span></span>

    ![](media/FBCimage55.png)

13. <span data-ttu-id="e8e43-216">Проверьте параметры и нажмите кнопку **Готово** , чтобы завершить настройку соединителя в центре безопасности _Амп_ соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="e8e43-216">Review your settings and then click **Finish** to complete the connector setup in the Security & Compliance Center.</span></span>

    ![](media/FBCimage56.png)

14. <span data-ttu-id="e8e43-217">Перейдите на страницу **архивации сторонних данных** , чтобы просмотреть ход процесса импорта.</span><span class="sxs-lookup"><span data-stu-id="e8e43-217">Go to the **Archive third-party data** page to see the progress of the import process.</span></span>

    ![](media/FBCimage58.png)
