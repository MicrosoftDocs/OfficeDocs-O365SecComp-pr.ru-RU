---
title: Интеграция сервера SIEM с Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Вы можете интегрировать сервер SIEM с Office 365 Cloud App Security. В этой статье приводятся общие сведения о том, как она работает и как ее настроить.
ms.openlocfilehash: b4baeda3cb836c0b1aa528d29176bbf4321d1fe2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215879"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="378cd-104">Интеграция сервера SIEM с Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="378cd-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="378cd-105">Ознакомительная версия \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="378cd-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="378cd-106">Планирование \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="378cd-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="378cd-107">Развертывание \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="378cd-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="378cd-108">Использование \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="378cd-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="378cd-109">Начало оценки</span><span class="sxs-lookup"><span data-stu-id="378cd-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="378cd-110">Начало планирования</span><span class="sxs-lookup"><span data-stu-id="378cd-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="378cd-111">Вот что вам!</span><span class="sxs-lookup"><span data-stu-id="378cd-111">You are here!</span></span>  <br/> [<span data-ttu-id="378cd-112">Следующее действие</span><span class="sxs-lookup"><span data-stu-id="378cd-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="378cd-113">Начало использования</span><span class="sxs-lookup"><span data-stu-id="378cd-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
## <a name="overview-and-prerequisites"></a><span data-ttu-id="378cd-114">Общие сведения и необходимые условия</span><span class="sxs-lookup"><span data-stu-id="378cd-114">Overview and prerequisites</span></span>

<span data-ttu-id="378cd-p102">Для обеспечения централизованного мониторинга оповещений можно интегрировать [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) со сведениями о безопасности и сервером управления событиями (SIEM). Это особенно полезно для организаций, использующих облачные службы и локальные серверные приложения. Интеграция с сервером SIEM позволяет группе безопасности улучшить защиту приложений Office 365, сохранив при этом обычный рабочий процесс безопасности, путем автоматизации определенных процедур безопасности и корреляции между облачными и локальными событиями.</span><span class="sxs-lookup"><span data-stu-id="378cd-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="378cd-p103">При первоначальной интеграции сервера SIEM с Office 365 Cloud App Security оповещения за последние два дня пересылаются на сервер SIEM, а также все оповещения в зависимости от выбранных фильтров. Кроме того, если отключить эту функцию для расширенного периода, то при его повторном включении будут переадресованы два предыдущих дня оповещения, а затем все оповещения.</span><span class="sxs-lookup"><span data-stu-id="378cd-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>

### <a name="siem-integration-architecture"></a><span data-ttu-id="378cd-120">Архитектура интеграции SIEM</span><span class="sxs-lookup"><span data-stu-id="378cd-120">SIEM integration architecture</span></span>

<span data-ttu-id="378cd-p104">Агент SIEM настраивается в сети Организации. При развертывании и настройке агент SIEM извлекает типы данных, которые были настроены (оповещения) с помощью API Office 365 Cloud App Security REST API. Затем трафик отправляется по зашифрованному HTTPS-каналу на порте 443.</span><span class="sxs-lookup"><span data-stu-id="378cd-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="378cd-124">Когда агент SIEM получает данные из Office 365 Cloud App Security, он отправляет сообщения syslog на локальный сервер SIEM с помощью конфигураций сети, которые предоставляются во время установки (TCP или UDP с настраиваемым портом).</span><span class="sxs-lookup"><span data-stu-id="378cd-124">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![Архитектура Cloud App Security and SIEM and Cloud App](media/siem-architecture.png)

### <a name="supported-siem-servers"></a><span data-ttu-id="378cd-126">Поддерживаемые серверы SIEM</span><span class="sxs-lookup"><span data-stu-id="378cd-126">Supported SIEM servers</span></span>

<span data-ttu-id="378cd-127">Office 365 Cloud App Security в настоящее время поддерживает следующие серверы SIEM:</span><span class="sxs-lookup"><span data-stu-id="378cd-127">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="378cd-128">Micro Focus Арксигхт</span><span class="sxs-lookup"><span data-stu-id="378cd-128">Micro Focus ArcSight</span></span>
- <span data-ttu-id="378cd-129">Универсальный ЦЕФ</span><span class="sxs-lookup"><span data-stu-id="378cd-129">Generic CEF</span></span>

### <a name="prerequisites"></a><span data-ttu-id="378cd-130">Необходимые компоненты</span><span class="sxs-lookup"><span data-stu-id="378cd-130">Prerequisites</span></span>

- <span data-ttu-id="378cd-p105">Для выполнения задач, описанных в этой статье, необходимо быть глобальным администратором или администратором безопасности. Ознакомьтесь с разРешениями [в центре &amp; безопасности и соответствия требованиям Office 365](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="378cd-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="378cd-133">Для Организации необходимо [включить безопасность облачНого приложения Office 365](turn-on-office-365-cas.md) .</span><span class="sxs-lookup"><span data-stu-id="378cd-133">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="378cd-134">Для Office 365 должна быть включена функция [ведения журнала аудита](turn-audit-log-search-on-or-off.md)</span><span class="sxs-lookup"><span data-stu-id="378cd-134">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="378cd-135">Для настройки интеграции сервера SIEM должен быть установлен стандартный сервер, отвечающий следующим требованиям:</span><span class="sxs-lookup"><span data-stu-id="378cd-135">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="378cd-136">ОС: Windows или Linux (это может быть виртуальная машина)</span><span class="sxs-lookup"><span data-stu-id="378cd-136">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="378cd-137">ЦП: 2</span><span class="sxs-lookup"><span data-stu-id="378cd-137">CPU: 2</span></span>
    - <span data-ttu-id="378cd-138">Место на диске: 20 ГБ</span><span class="sxs-lookup"><span data-stu-id="378cd-138">Disk space: 20 GB</span></span>
    - <span data-ttu-id="378cd-139">ОЗУ: 2 ГБ</span><span class="sxs-lookup"><span data-stu-id="378cd-139">RAM: 2 GB</span></span>
    - <span data-ttu-id="378cd-140">Установлен [Java Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html)</span><span class="sxs-lookup"><span data-stu-id="378cd-140">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="378cd-141">Брандмауэр настроен в соответствии с [требованиями к сети](https://docs.microsoft.com/cloud-app-security/network-requirements)</span><span class="sxs-lookup"><span data-stu-id="378cd-141">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="378cd-p106">Необходимо получить сведения об удаленном **узле syslog** и **номере порта сислот**. Эту информацию можно искать администратору сети или администратору безопасности.</span><span class="sxs-lookup"><span data-stu-id="378cd-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="378cd-144">Вы должны согласиться с [условиями лицензионного соглашения](https://go.microsoft.com/fwlink/?linkid=862491) на использование программного обеспечения, чтобы скачать [JAR – файл](https://go.microsoft.com/fwlink/?linkid=838596) , который потребуется для интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-144">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="step-1-set-it-up-a-siem-agent-in-office-365-cloud-app-security"></a><span data-ttu-id="378cd-145">Шаг 1: Настройка агента SIEM в Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="378cd-145">Step 1: Set it up a SIEM agent in Office 365 Cloud App Security</span></span>

1. <span data-ttu-id="378cd-146">Перейдите на портал Cloud App Security ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) и выполните вход.</span><span class="sxs-lookup"><span data-stu-id="378cd-146">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="378cd-147">Щелкните **Параметры** \> **расширения безопасности**, а затем выберите SIEM агенты.</span><span class="sxs-lookup"><span data-stu-id="378cd-147">Click **Settings** \> **Security extensions**, and then choose SIEM agents.</span></span><br/>
<span data-ttu-id="378cd-148">![Выберите параметры _Гт_ расширения безопасности](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-148">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

3. <span data-ttu-id="378cd-149">Выберите **Добавить агент SIEM**.</span><span class="sxs-lookup"><span data-stu-id="378cd-149">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="378cd-150">![Выберите Добавить агент SIEM.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-150">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
4. <span data-ttu-id="378cd-151">Нажмите кнопку **запустить мастер**.</span><span class="sxs-lookup"><span data-stu-id="378cd-151">Choose **Start wizard**.</span></span><br/><span data-ttu-id="378cd-152">![Получение справки или запуск мастера](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-152">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
5. <span data-ttu-id="378cd-p107">В разделе **Общие** действия укажите имя и **выберите формат SIEM** и настройте любые **Дополнительные параметры** , относящиеся к этому формату. Затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="378cd-p107">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="378cd-155">![Укажите имя и тип](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-155">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
6. <span data-ttu-id="378cd-p108">На удаленном этапе **syslog** укажите IP-адрес или имя узла **удаленного сервера Syslog** и **номер порта syslog**. Выберите TCP или UDP в качестве удаленного протокола syslog. (Вы можете обратиться к администратору сети или администратору безопасности, чтобы получить эти сведения, если у вас их нет.) Затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="378cd-p108">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="378cd-159">![Указание сведений об удаленном syslog](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-159">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
7. <span data-ttu-id="378cd-160">На шаге **типы данных** выполните одно из следующих действий, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="378cd-160">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="378cd-161">Оставить значение по умолчанию для **всех оповещений**</span><span class="sxs-lookup"><span data-stu-id="378cd-161">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="378cd-162">ИЛИ</span><span class="sxs-lookup"><span data-stu-id="378cd-162">OR</span></span>
    - <span data-ttu-id="378cd-p109">Щелкните **все оповещения**, а затем выберите **определенные фильтры**. Определите фильтры, чтобы выбрать типы оповещений, которые нужно отправить на сервер SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-p109">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="378cd-165">![Типы данных шаг мастера](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-165">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
8. <span data-ttu-id="378cd-166">На экране приветствия Скопируйте маркер и сохраните его для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="378cd-166">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![Экран агента SIEM](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="378cd-p110">На этом шаге вы настроили агент SIEM в Office 365 Cloud App Security, но интеграция сервера SIEM еще не завершена. Перейдите к следующему шагу, чтобы продолжить интеграцию сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-p110">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="378cd-p111">После нажатия кнопки Закрыть и закрытия мастера на экране расширения безопасности можно увидеть агент SIEM, добавленный в таблице. Отображается состояние **создано** , пока оно не будет подключено позже.</span><span class="sxs-lookup"><span data-stu-id="378cd-p111">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![Создан агент SIEM](media/SIEMAgentCreated.png)
    
## <a name="step-2-download-a-jar-file-and-run-it-on-your-siem-server"></a><span data-ttu-id="378cd-173">Шаг 2: Скачайте JAR — файл и запустите его на сервере SIEM</span><span class="sxs-lookup"><span data-stu-id="378cd-173">Step 2: Download a JAR file and run it on your SIEM server</span></span>

1. <span data-ttu-id="378cd-p112">Скачайте [агент Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) и распакуйте папку. Чтобы продолжить, необходимо согласиться с [условиями лицензионного соглашения](https://go.microsoft.com/fwlink/?linkid=862491) на использование программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="378cd-p112">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="378cd-176">ИзВлеките JAR файл из архивной папки и запустите его на сервере SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-176">Extract the .jar file from the zipped folder and run it on your SIEM server.</span></span>
    
3. <span data-ttu-id="378cd-177">После запуска файла выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="378cd-177">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
### <a name="important-notes"></a><span data-ttu-id="378cd-178">Важные замечания</span><span class="sxs-lookup"><span data-stu-id="378cd-178">Important notes</span></span>

- <span data-ttu-id="378cd-179">Имя файла может различаться в зависимости от версии агента SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-179">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="378cd-180">Рекомендуется запускать файл JAR на сервере SIEM во время установки сервера.</span><span class="sxs-lookup"><span data-stu-id="378cd-180">We recommend that you run the JAR file on your SIEM server during server setup.</span></span>

    - <span data-ttu-id="378cd-181">**Windows**: запуск в качестве запланированного задания, поэтому необходимо настроить задачу для запуска независимо от того, **вошел ли пользователь в систему, или нет** , **остановить задачу, если она выполняется дольше, чем** параметр.</span><span class="sxs-lookup"><span data-stu-id="378cd-181">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="378cd-182">**Linux**: добавьте команду Run с параметром **&** в `rc.local` файл.</span><span class="sxs-lookup"><span data-stu-id="378cd-182">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="378cd-183">Пример.</span><span class="sxs-lookup"><span data-stu-id="378cd-183">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="378cd-p113">Параметры в квадратных скобках являются необязательными, и их следует использовать только в случае необходимости. Используйте следующие переменные:</span><span class="sxs-lookup"><span data-stu-id="378cd-p113">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>

    - <span data-ttu-id="378cd-186">**Дирнаме** это путь к каталогу, который вы хотите использовать для локальных журналов отладки агентов.</span><span class="sxs-lookup"><span data-stu-id="378cd-186">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>

    - <span data-ttu-id="378cd-187">**Address [:P ОРТ]** — это адрес прокси-сервера и порт, который сервер использует для подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="378cd-187">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>

    - <span data-ttu-id="378cd-188">**Token** — это маркер агента SIEM, скопированный в первой процедуре.</span><span class="sxs-lookup"><span data-stu-id="378cd-188">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>

    - <span data-ttu-id="378cd-189">Чтобы получить справку, введите `-h`.</span><span class="sxs-lookup"><span data-stu-id="378cd-189">To get help, type `-h`.</span></span> 
  
## <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="378cd-190">Шаг 3: Проверка работоспособности агента SIEM</span><span class="sxs-lookup"><span data-stu-id="378cd-190">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="378cd-191">Убедитесь, что состояние агента SIEM на портале Cloud App Security (Office 365) не отображается как **Ошибка подключения** или **отключено** , а также отсутствуют уведомления агентов.</span><span class="sxs-lookup"><span data-stu-id="378cd-191">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="378cd-192">Например, здесь можно увидеть, что сервер SIEM подключен:</span><span class="sxs-lookup"><span data-stu-id="378cd-192">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="378cd-193">![Подключенный сервер SIEM](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-193">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="378cd-194">Кроме того, вы увидите, что сервер SIEM отключен:</span><span class="sxs-lookup"><span data-stu-id="378cd-194">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="378cd-195">![Сервер SIEM не подключен](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-195">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="378cd-196">Убедитесь, что в вашем syslog/SIEM Server получены оповещения от Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="378cd-196">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="what-the-logfiles-look-like"></a><span data-ttu-id="378cd-197">Как выглядят файлы журнала</span><span class="sxs-lookup"><span data-stu-id="378cd-197">What the logfiles look like</span></span>

<span data-ttu-id="378cd-198">Ниже приведен пример файла журнала оповещений, который можно отправить на сервер SIEM:</span><span class="sxs-lookup"><span data-stu-id="378cd-198">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="378cd-199">А вот еще один пример, на этот раз в формате ЦЕФ:</span><span class="sxs-lookup"><span data-stu-id="378cd-199">And here's another sample, this time in CEF format:</span></span>


|<span data-ttu-id="378cd-200">Имя поля ЦЕФ</span><span class="sxs-lookup"><span data-stu-id="378cd-200">CEF field name</span></span>  | <span data-ttu-id="378cd-201">Описание</span><span class="sxs-lookup"><span data-stu-id="378cd-201">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="378cd-202">начал</span><span class="sxs-lookup"><span data-stu-id="378cd-202">start</span></span>     | <span data-ttu-id="378cd-203">Метка времени оповещения</span><span class="sxs-lookup"><span data-stu-id="378cd-203">alert timestamp</span></span>        |
|<span data-ttu-id="378cd-204">оканчиваться</span><span class="sxs-lookup"><span data-stu-id="378cd-204">end</span></span>     | <span data-ttu-id="378cd-205">Метка времени оповещения</span><span class="sxs-lookup"><span data-stu-id="378cd-205">alert timestamp</span></span>        |
|<span data-ttu-id="378cd-206">RT</span><span class="sxs-lookup"><span data-stu-id="378cd-206">rt</span></span>     | <span data-ttu-id="378cd-207">Метка времени оповещения</span><span class="sxs-lookup"><span data-stu-id="378cd-207">alert timestamp</span></span>        |
|<span data-ttu-id="378cd-208">MSG</span><span class="sxs-lookup"><span data-stu-id="378cd-208">msg</span></span>     | <span data-ttu-id="378cd-209">Описание оповещения, как показано на портале Cloud App Security для Office 365</span><span class="sxs-lookup"><span data-stu-id="378cd-209">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="378cd-210">SUSE</span><span class="sxs-lookup"><span data-stu-id="378cd-210">suser</span></span>     | <span data-ttu-id="378cd-211">пользователь темы оповещения</span><span class="sxs-lookup"><span data-stu-id="378cd-211">alert subject user</span></span>        |
|<span data-ttu-id="378cd-212">Дестинатионсервиценаме</span><span class="sxs-lookup"><span data-stu-id="378cd-212">destinationServiceName</span></span>     | <span data-ttu-id="378cd-213">исходное приложение оповещения, например Office 365, SharePoint или OneDrive</span><span class="sxs-lookup"><span data-stu-id="378cd-213">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="378cd-214">Кслабел</span><span class="sxs-lookup"><span data-stu-id="378cd-214">csLabel</span></span>     | <span data-ttu-id="378cd-p114">Различаются (метки имеют разный смысл). Как правило, метки говорят сами по себе, как Таржетобжектс.</span><span class="sxs-lookup"><span data-stu-id="378cd-p114">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="378cd-217">cs</span><span class="sxs-lookup"><span data-stu-id="378cd-217">cs</span></span>     | <span data-ttu-id="378cd-218">Сведения, соответствующие метке (например, конечному пользователю оповещения в соответствии с примером метки);</span><span class="sxs-lookup"><span data-stu-id="378cd-218">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |

## <a name="additional-tasks-as-needed"></a><span data-ttu-id="378cd-219">Дополнительные задачи (при необходимости)</span><span class="sxs-lookup"><span data-stu-id="378cd-219">Additional tasks (as needed)</span></span>

<span data-ttu-id="378cd-p115">После настройки сервера SIEM и интеграции его с Office 365 Cloud App Security может потребоваться повторно создать маркер, изменить агент SIEM или удалить агент SIEM. В следующих разделах описано, как выполнить эти задачи.</span><span class="sxs-lookup"><span data-stu-id="378cd-p115">After you have configured your SIEM server and have integrated it with Office 365 Cloud App Security, you might need to regenerate a token, edit a SIEM agent, or delete a SIEM agent. The following sections describe how to perform these tasks.</span></span>

### <a name="regenerate-a-token"></a><span data-ttu-id="378cd-222">Повторное создание маркера</span><span class="sxs-lookup"><span data-stu-id="378cd-222">Regenerate a token</span></span>

<span data-ttu-id="378cd-223">Если вы потеряете маркер, вы можете восстановить его.</span><span class="sxs-lookup"><span data-stu-id="378cd-223">If you lose your token, you can regenerate one.</span></span> 

1. <span data-ttu-id="378cd-224">[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)на портале Cloud App security () Office 365 выберите **параметры** > **расширения безопасности**.</span><span class="sxs-lookup"><span data-stu-id="378cd-224">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="378cd-225">В таблице выберите строку для агента SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-225">In the table, locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="378cd-226">Нажмите многоточие, а затем выберите пункт **повторно создать маркер**.</span><span class="sxs-lookup"><span data-stu-id="378cd-226">Click the ellipses, and then choose **Regenerate token**.</span></span><br/><span data-ttu-id="378cd-227">![Повторно создайте маркер, нажав кнопку с многоточием для своего агента SIEM.](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-227">![Regenerate a token by clicking the ellipsis for your SIEM agent](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)</span></span>
  
### <a name="edit-a-siem-agent"></a><span data-ttu-id="378cd-228">Изменение агента SIEM</span><span class="sxs-lookup"><span data-stu-id="378cd-228">Edit a SIEM agent</span></span>

1. <span data-ttu-id="378cd-229">[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)на портале Cloud App security () Office 365 выберите **параметры** > **расширения безопасности**.</span><span class="sxs-lookup"><span data-stu-id="378cd-229">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="378cd-230">Поиск строки для агента SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-230">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="378cd-p116">Нажмите кнопку с многоточием, а затем выберите команду **изменить**. (Если вы изменяете агент SIEM, вам не потребуется повторно запускать файл. jar; он обновляется автоматически.)</span><span class="sxs-lookup"><span data-stu-id="378cd-p116">Click the ellipses, and then choose **Edit**. (If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.) </span></span><br/><span data-ttu-id="378cd-233">![Чтобы изменить агент SIEM, нажмите многоточия, а затем нажмите кнопку Изменить.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-233">![To edit your SIEM agent, choose the ellipses, and then choose Edit.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)</span></span>
  
### <a name="delete-a-siem-agent"></a><span data-ttu-id="378cd-234">Удаление агента SIEM</span><span class="sxs-lookup"><span data-stu-id="378cd-234">Delete a SIEM agent</span></span>

1. <span data-ttu-id="378cd-235">[https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)на портале Cloud App security () Office 365 выберите **параметры** > **расширения безопасности**.</span><span class="sxs-lookup"><span data-stu-id="378cd-235">In the Office 365 Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), choose **Settings** > **Security extensions**.</span></span>

2. <span data-ttu-id="378cd-236">Поиск строки для агента SIEM.</span><span class="sxs-lookup"><span data-stu-id="378cd-236">Locate the row for the SIEM agent.</span></span> 

3. <span data-ttu-id="378cd-237">Нажмите многоточие, а затем выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="378cd-237">Click the ellipses, and then choose **Delete**.</span></span><br/><span data-ttu-id="378cd-238">![Чтобы удалить агент SIEM, нажмите многоточия, а затем нажмите кнопку Удалить.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span><span class="sxs-lookup"><span data-stu-id="378cd-238">![To delete a SIEM agent, choose the ellipses, and then choose Delete.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)</span></span>

  
## <a name="next-steps"></a><span data-ttu-id="378cd-239">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="378cd-239">Next steps</span></span>

- [<span data-ttu-id="378cd-240">Действия, связанные с использованием, после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="378cd-240">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="378cd-241">Просмотр оповещений и выполнение действий с ними</span><span class="sxs-lookup"><span data-stu-id="378cd-241">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="378cd-242">Группировка IP-адресов для упрощения управления</span><span class="sxs-lookup"><span data-stu-id="378cd-242">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

