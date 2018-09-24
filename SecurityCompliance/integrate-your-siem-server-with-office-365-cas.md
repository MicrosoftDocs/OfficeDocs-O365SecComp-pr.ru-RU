---
title: Интеграция сервера SIEM с Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: dd6d2417-49c4-4de6-9294-67fdabbf8532
description: Сервер SIEM можно интегрировать с Office 365 облачных приложений безопасности. В этой статье Обзор принцип работы и способы ее настройки.
ms.openlocfilehash: a2bd75e73ddccef9359ace304faa3c8b1dd4a728
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972331"
---
# <a name="integrate-your-siem-server-with-office-365-cloud-app-security"></a><span data-ttu-id="13d8d-104">Интеграция сервера SIEM с Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="13d8d-104">Integrate your SIEM server with Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="13d8d-105">Оценка **\>**</span><span class="sxs-lookup"><span data-stu-id="13d8d-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="13d8d-106">Планирование **\>**</span><span class="sxs-lookup"><span data-stu-id="13d8d-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="13d8d-107">Развертывание **\>**</span><span class="sxs-lookup"><span data-stu-id="13d8d-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="13d8d-108">Использование \*\*\*</span><span class="sxs-lookup"><span data-stu-id="13d8d-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="13d8d-109">Начать оценку</span><span class="sxs-lookup"><span data-stu-id="13d8d-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="13d8d-110">Начать планирование</span><span class="sxs-lookup"><span data-stu-id="13d8d-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="13d8d-111">Вы находитесь здесь!</span><span class="sxs-lookup"><span data-stu-id="13d8d-111">You are here!</span></span>  <br/> [<span data-ttu-id="13d8d-112">Следующий шаг</span><span class="sxs-lookup"><span data-stu-id="13d8d-112">Next step</span></span>](utilization-activities-for-ocas.md) <br/> |[<span data-ttu-id="13d8d-113">Начать использование</span><span class="sxs-lookup"><span data-stu-id="13d8d-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="13d8d-p102">Можно интегрировать [Приложения облаке Безопасность в Office 365](get-ready-for-office-365-cas.md) с сервером для включения централизованного мониторинга предупреждений безопасности сведения и события управления (SIEM). Это особенно удобно использовать для организаций, использующих облачных служб и локального сервера приложений. Интеграция с сервером SIEM позволяет ваша группа безопасности для улучшения защиты приложений Office 365 без снижения безопасности обычного рабочего процесса, автоматизация некоторых процедуры безопасности и сопоставления между облачной и локальной события.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p102">You can integrate [Office 365 Cloud App Security](get-ready-for-office-365-cas.md) with your security information and event management (SIEM) server to enable centralized monitoring of alerts. This is especially beneficial for organizations who are using cloud services and on-premises server applications. Integrating with a SIEM server allows your security team to better protect your Office 365 applications while maintaining your usual security workflow, by automating certain security procedures and correlating between cloud-based and on-premises events.</span></span>  
  
<span data-ttu-id="13d8d-p103">При SIEM сервера сначала интеграции с Office 365 облачных приложений безопасности, оповещения о от последних двух дней будут переадресовываться SIEM сервера, а также все оповещения из then на (основан на все фильтры, которые вы выбрали). Кроме того Если отключить этот компонент в течение длительного, при включении его еще раз, он будет перенаправлять за последние два дня оповещений и затем все оповещения в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p103">When you first integrate your SIEM server with Office 365 Cloud App Security, alerts from the last two days are forwarded to the SIEM server, as well as all alerts from then on (based on any filters you select). Additionally, if you disable this feature for an extended period, when you enable it again, it will forward the past two days of alerts and then all alerts from then on.</span></span>
 
## <a name="siem-integration-architecture"></a><span data-ttu-id="13d8d-119">Архитектура интеграции SIEM</span><span class="sxs-lookup"><span data-stu-id="13d8d-119">SIEM integration architecture</span></span>

<span data-ttu-id="13d8d-p104">Агент SIEM настраивается в сети организации. При развертывания и настройки агента SIEM берет типов данных, которые были настроены (оповещения) с помощью Office 365 облачных приложений безопасности RESTful API-интерфейсы. Затем передачи через зашифрованный канал HTTPS через порт 443.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p104">A SIEM agent is set up in your organization's network. When deployed and configured, the SIEM agent pulls the data types that were configured (alerts) using Office 365 Cloud App Security RESTful APIs. The traffic is then sent over an encrypted HTTPS channel on port 443.</span></span>
  
<span data-ttu-id="13d8d-123">Когда SIEM агент получает данные из приложения облаке Безопасность в Office 365, он отправляет сообщения Syslog на локальном сервере SIEM, с помощью конфигурации сети, которые предоставляются во время установки (TCP или UDP-ПОРТ с помощью настраиваемых портов).</span><span class="sxs-lookup"><span data-stu-id="13d8d-123">When a SIEM agent retrieves data from Office 365 Cloud App Security, it sends the Syslog messages to your local SIEM server using the network configurations that are provided during setup (TCP or UDP with a custom port).</span></span>

![Архитектура SIEM и облачных безопасности приложения](media/siem-architecture.png)

## <a name="supported-siem-servers"></a><span data-ttu-id="13d8d-125">Поддерживаемые SIEM серверы</span><span class="sxs-lookup"><span data-stu-id="13d8d-125">Supported SIEM servers</span></span>

<span data-ttu-id="13d8d-126">В настоящее время безопасности облаке приложения Office 365 поддерживает следующие серверы SIEM:</span><span class="sxs-lookup"><span data-stu-id="13d8d-126">Office 365 Cloud App Security currently supports the following SIEM servers:</span></span>
- <span data-ttu-id="13d8d-127">Разработанное Micro Focus</span><span class="sxs-lookup"><span data-stu-id="13d8d-127">Micro Focus ArcSight</span></span>
- <span data-ttu-id="13d8d-128">Универсальный CEF</span><span class="sxs-lookup"><span data-stu-id="13d8d-128">Generic CEF</span></span>

## <a name="prerequisites"></a><span data-ttu-id="13d8d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="13d8d-129">Prerequisites</span></span>

- <span data-ttu-id="13d8d-p105">Необходимо быть глобальным администратором или администратор безопасности для выполнения задач, описанных в этой статье. Просмотреть [разрешения безопасности Office 365 &amp; центре соответствия требованиям](permissions-in-the-security-and-compliance-center.md)</span><span class="sxs-lookup"><span data-stu-id="13d8d-p105">You must be a global administrator or security administrator to perform the tasks described in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)</span></span>

- <span data-ttu-id="13d8d-132">Необходимо иметь [поддержкой безопасности приложения Office 365 облако](turn-on-office-365-cas.md) для вашей организации.</span><span class="sxs-lookup"><span data-stu-id="13d8d-132">You must have [Office 365 Cloud App Security enabled](turn-on-office-365-cas.md) for your organization.</span></span>

- <span data-ttu-id="13d8d-133">[Ведение журнала аудита](turn-audit-log-search-on-or-off.md) может быть включена для Office 365</span><span class="sxs-lookup"><span data-stu-id="13d8d-133">[Audit logging](turn-audit-log-search-on-or-off.md) must be turned on for Office 365</span></span>

- <span data-ttu-id="13d8d-134">Необходимо иметь стандартный сервер, который соответствует следующим требованиям для настройки интеграции сервера SIEM:</span><span class="sxs-lookup"><span data-stu-id="13d8d-134">You must have a standard server that meets the following requirements in order to configure SIEM server integration:</span></span>
    - <span data-ttu-id="13d8d-135">Операционная система: Windows или Linux (это может быть виртуальной машины)</span><span class="sxs-lookup"><span data-stu-id="13d8d-135">OS: Windows or Linux (this can be a virtual machine)</span></span>
    - <span data-ttu-id="13d8d-136">ЦП: 2</span><span class="sxs-lookup"><span data-stu-id="13d8d-136">CPU: 2</span></span>
    - <span data-ttu-id="13d8d-137">Место на диске: 20 ГБ</span><span class="sxs-lookup"><span data-stu-id="13d8d-137">Disk space: 20 GB</span></span>
    - <span data-ttu-id="13d8d-138">ОЗУ: 2 ГБ</span><span class="sxs-lookup"><span data-stu-id="13d8d-138">RAM: 2 GB</span></span>
    - <span data-ttu-id="13d8d-139">Установленные [Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html)</span><span class="sxs-lookup"><span data-stu-id="13d8d-139">[Oracle Java 8](http://www.oracle.com/technetwork/java/javase/downloads/index.html) installed</span></span>
    - <span data-ttu-id="13d8d-140">Брандмауэр, как описано в [требования к сети](https://docs.microsoft.com/cloud-app-security/network-requirements)</span><span class="sxs-lookup"><span data-stu-id="13d8d-140">Firewall configured as described in [Network requirements](https://docs.microsoft.com/cloud-app-security/network-requirements)</span></span>

- <span data-ttu-id="13d8d-p106">Необходимо иметь подробные сведения об **удаленных syslog узла** и **номер порта Syslot**. Администратор или администратор безопасности должна появиться возможность помогают найти эти сведения.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p106">You must have details about your **Remote syslog host** and **Syslot port number**. A network administrator or security administrator should be able to help you locate that information.</span></span> 

- <span data-ttu-id="13d8d-143">Для загрузки [БАНКИ файлов](https://go.microsoft.com/fwlink/?linkid=838596) необходимо интегрировать сервера SIEM, необходимо согласиться [Лицензионное соглашение на использование программного обеспечения](https://go.microsoft.com/fwlink/?linkid=862491) .</span><span class="sxs-lookup"><span data-stu-id="13d8d-143">You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) to download the [JAR file](https://go.microsoft.com/fwlink/?linkid=838596) you'll need to integrate your SIEM server.</span></span>
 
## <a name="integrate-office-365-cloud-app-security"></a><span data-ttu-id="13d8d-144">Интеграция безопасности облаке приложения Office 365</span><span class="sxs-lookup"><span data-stu-id="13d8d-144">Integrate Office 365 Cloud App Security</span></span>
    
### <a name="step-1-set-it-up-in-the-office-365-cloud-app-security-portal"></a><span data-ttu-id="13d8d-145">Этап 1: Настройка его на портале облачных приложений Office 365 безопасности</span><span class="sxs-lookup"><span data-stu-id="13d8d-145">Step 1: Set it up in the Office 365 Cloud App Security portal</span></span>

1. <span data-ttu-id="13d8d-p107">Последовательно выберите пункты [https://protection.office.com](https://protection.office.com) и выполнить вход с помощью учетной записи рабочего или школы для Office 365. (Вы перейдете к безопасности &amp; центре соответствия требованиям.)</span><span class="sxs-lookup"><span data-stu-id="13d8d-p107">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="13d8d-148">Последовательно выберите пункты **оповещения** \> **Управление расширенного оповещения**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-148">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="13d8d-p108">Выберите, **перейдите к безопасности приложения Office 365 облака**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p108">Choose **Go to Office 365 Cloud App Security**. </span></span><br/>
    <span data-ttu-id="13d8d-150">![В разделе Безопасность &amp; центре соответствия требованиям, выберите дополнительные оповещения для перехода к безопасности Office 365 облаке приложения](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-150">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="13d8d-151">Щелкните **Параметры** \> **расширения безопасности**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-151">Click **Settings** \> **Security extensions**.</span></span><br/>
<span data-ttu-id="13d8d-152">![Выберите параметры > расширения безопасности](media/Settings-SecurityExtensions.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-152">![Choose Settings > Security extensions](media/Settings-SecurityExtensions.png)</span></span>

5. <span data-ttu-id="13d8d-153">Выберите пункт **Добавить SIEM агента**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-153">Choose **Add SIEM agent**.</span></span><br/><span data-ttu-id="13d8d-154">![Выберите пункт Добавить SIEM агента.](media/SIEMAgents.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-154">![Choose Add SIEM agent.](media/SIEMAgents.png)</span></span>
    
6. <span data-ttu-id="13d8d-155">Нажмите кнопку **запустить мастер**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-155">Choose **Start wizard**.</span></span><br/><span data-ttu-id="13d8d-156">![Получение справки или запустить мастер](media/HelpOrWizard.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-156">![Get help or start the wizard](media/HelpOrWizard.png)</span></span> 
    
7. <span data-ttu-id="13d8d-p109">**Общие** шаге укажите имя и **выберите в качестве формата SIEM формат** и задайте любые **Дополнительные параметры** , которые важны для этого формата. Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p109">In the **General** step, specify a name, and **Select your SIEM format** and set any **Advanced settings** that are relevant to that format. Then choose **Next**.</span></span><br/><span data-ttu-id="13d8d-159">![Укажите имя и тип](media/ChooseAgentTypeAndName.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-159">![Specify a name and type](media/ChooseAgentTypeAndName.png)</span></span>
    
8. <span data-ttu-id="13d8d-p110">На этапе **Удаленного Syslog** укажите IP-адрес или имя узла **удаленного syslog узла** и **номер порта Syslog**. Выберите в качестве протокола удаленного Syslog TCP или UDP-ПОРТ. (Можно работать с администратором сети или администратор безопасности для получения этих сведений, если у них нет.) Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p110">In the **Remote Syslog** step, specify the IP address or hostname of the **Remote syslog host** and the **Syslog port number**. Select TCP or UDP as the Remote Syslog protocol. (You can work with your network administrator or security administrator to get these details if you don't have them.) Then choose **Next**.</span></span><br/><span data-ttu-id="13d8d-163">![Укажите сведения о удаленного Syslog](media/ArcSightS1Syslog.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-163">![Specify Remote Syslog details](media/ArcSightS1Syslog.png)</span></span>
  
9. <span data-ttu-id="13d8d-164">На этапе **Типы данных** , выполните одно из следующих действий и нажмите кнопку **Далее**:</span><span class="sxs-lookup"><span data-stu-id="13d8d-164">In the **Data Types** step, do one of the following, and then click **Next**:</span></span>
    - <span data-ttu-id="13d8d-165">Оставьте значение по умолчанию **Все оповещения**</span><span class="sxs-lookup"><span data-stu-id="13d8d-165">Keep the default setting of **All Alerts**</span></span><br/><span data-ttu-id="13d8d-166">OR</span><span class="sxs-lookup"><span data-stu-id="13d8d-166">OR</span></span>
    - <span data-ttu-id="13d8d-p111">Щелкните **все оповещения**и нажмите кнопку **Специальные фильтры**. Определение фильтров для выбора типа оповещений, которое требуется отправить на сервер SIEM.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p111">Click **All alerts**, and then choose **Specific filters**. Define filters to select the kinds of alerts you want to send to your SIEM server. </span></span><br/><span data-ttu-id="13d8d-169">![Этап типы данных мастера](media/ArcSightS1ExportOptions.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-169">![Data Types step of the wizard](media/ArcSightS1ExportOptions.png)</span></span>
  
10. <span data-ttu-id="13d8d-170">На странице приветствия Скопируйте маркер и сохраните его для последующих операций.</span><span class="sxs-lookup"><span data-stu-id="13d8d-170">On the Congratulations screen, copy the token and save it for later.</span></span><br/>![Агент создан SIEM экрана](media/SIEMAgentFinished.png) 

> [!IMPORTANT]
> <span data-ttu-id="13d8d-p112">На этом этапе настройки агента SIEM в облаке приложения Office 365 безопасности, однако интеграция сервера вашей SIEM еще не выполнено. Перейти к следующему шагу для продолжения интеграции сервера SIEM.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p112">At this point, you have set up a SIEM agent in Office 365 Cloud App Security, but your SIEM server integration is not yet finished. Proceed to the next step to continue your SIEM server integration.</span></span>

<span data-ttu-id="13d8d-p113">После нажмите кнопку Закрыть и закрыть мастер, на экране расширений безопасности, можно просмотреть агента SIEM, добавленной в таблице. Пока он подключен более поздней версии, он будет отображается статус **создано** .</span><span class="sxs-lookup"><span data-stu-id="13d8d-p113">After you click Close and leave the wizard, on the Security extensions screen, you can see the SIEM agent you added in the table. It will show a status of **Created** until it's connected later.</span></span>

![Агент SIEM создан](media/SIEMAgentCreated.png)
    
### <a name="step-2-download-the-jar-file-and-run-it-on-your-server"></a><span data-ttu-id="13d8d-177">Шаг 2: Загрузите файл БАНКЕ и запустите его на сервере</span><span class="sxs-lookup"><span data-stu-id="13d8d-177">Step 2: Download the JAR file and run it on your server</span></span>

1. <span data-ttu-id="13d8d-p114">Загрузите [Microsoft Cloud приложения безопасности SIEM агента](https://go.microsoft.com/fwlink/?linkid=838596) и распакуйте папку. (Необходимо согласиться [Лицензионное соглашение на использование программного обеспечения](https://go.microsoft.com/fwlink/?linkid=862491) для продолжения.)</span><span class="sxs-lookup"><span data-stu-id="13d8d-p114">Download the [Microsoft Cloud App Security SIEM Agent](https://go.microsoft.com/fwlink/?linkid=838596) and unzip the folder. (You must agree to [software license terms](https://go.microsoft.com/fwlink/?linkid=862491) in order to proceed.)</span></span> 
    
2. <span data-ttu-id="13d8d-180">Извлеките файл .jar из ZIP-папку и запустите его на сервере.</span><span class="sxs-lookup"><span data-stu-id="13d8d-180">Extract the .jar file from the zipped folder and run it on your server.</span></span>
    
3. <span data-ttu-id="13d8d-181">После запуска файла, выполните следующие действия: команду:</span><span class="sxs-lookup"><span data-stu-id="13d8d-181">After running the file, run the following: command:</span></span><br/>
  ```
  java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN
  ```
#### <a name="important-notes"></a><span data-ttu-id="13d8d-182">Важные замечания</span><span class="sxs-lookup"><span data-stu-id="13d8d-182">Important notes</span></span>

- <span data-ttu-id="13d8d-183">Имя файла может отличаться в зависимости от версии SIEM агента.</span><span class="sxs-lookup"><span data-stu-id="13d8d-183">The file name may differ depending on the version of the SIEM agent.</span></span> 

- <span data-ttu-id="13d8d-184">Рекомендуется запускать заливки БАНКЕ на сервере во время установки сервера.</span><span class="sxs-lookup"><span data-stu-id="13d8d-184">We recommend that you run the JAR fill on your server during server setup.</span></span>
    - <span data-ttu-id="13d8d-185">**Windows**: запустите как запланированная задача, сохраняя настройки задачи для **запуска ли пользователь вошел в систему, или не** и снять флажок **останавливать при выполнении дольше, чем** .</span><span class="sxs-lookup"><span data-stu-id="13d8d-185">**Windows**: Run as a scheduled task, making sure to configure the task to **Run whether the user is logged on or not** and clear the **Stop the task if it runs longer than** option.</span></span>

    - <span data-ttu-id="13d8d-186">**Linux**: Добавление выполнения команды с **&** для `rc.local` файла.</span><span class="sxs-lookup"><span data-stu-id="13d8d-186">**Linux**: Add the run command with an **&** to the `rc.local` file.</span></span> <br/><span data-ttu-id="13d8d-187">Пример.</span><span class="sxs-lookup"><span data-stu-id="13d8d-187">Example:</span></span><br/> 
    ```
    java -jar mcas-siemagent-0.87.20-signed.jar [--logsDirectory DIRNAME] [--proxy ADDRESS[:PORT]] --token TOKEN &
    ```

- <span data-ttu-id="13d8d-p115">Параметры в квадратных скобок являются необязательными и следует использовать только при необходимости. Используйте следующие переменные:</span><span class="sxs-lookup"><span data-stu-id="13d8d-p115">Parameters in brackets [] are optional, and should be used only if relevant. Use the following variables:</span></span>
    - <span data-ttu-id="13d8d-190">**DIRNAME** — это путь каталог, который вы хотите использовать для локального агента журналы отладки.</span><span class="sxs-lookup"><span data-stu-id="13d8d-190">**DIRNAME** is the path to the directory you want to use for local agent debug logs.</span></span>
    - <span data-ttu-id="13d8d-191">**Адрес [: ПОРТ]** — это адрес прокси-сервера и порт, который используется сервером для подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="13d8d-191">**ADDRESS[:PORT]** is the proxy server address and port that the server uses to connect to the Internet.</span></span>
    - <span data-ttu-id="13d8d-192">**МАРКЕР** является маркером агента SIEM, скопированные в первой процедуре.</span><span class="sxs-lookup"><span data-stu-id="13d8d-192">**TOKEN** is the SIEM agent token you copied in the first procedure.</span></span>
    - <span data-ttu-id="13d8d-193">Чтобы получить справку, введите `-h`.</span><span class="sxs-lookup"><span data-stu-id="13d8d-193">To get help, type `-h`.</span></span> 
  
### <a name="step-3-validate-that-the-siem-agent-is-working"></a><span data-ttu-id="13d8d-194">Шаг 3: Проверка работы агента SIEM</span><span class="sxs-lookup"><span data-stu-id="13d8d-194">Step 3: Validate that the SIEM agent is working</span></span>

1. <span data-ttu-id="13d8d-195">Убедитесь, что состояние агента SIEM на портале облачных приложений Office 365 безопасности не отображается как **Ошибка подключения** или **отключен** , который отсутствии агента уведомлений.</span><span class="sxs-lookup"><span data-stu-id="13d8d-195">Make sure the status of the SIEM agent in the Office 365 Cloud App Security portal is not displayed as **Connection error** or **Disconnected** and that there are no agent notifications.</span></span><br/><span data-ttu-id="13d8d-196">Например здесь можно увидеть, что подключения к серверу SIEM:</span><span class="sxs-lookup"><span data-stu-id="13d8d-196">For example, here we can see the SIEM server is connected:</span></span><br/><span data-ttu-id="13d8d-197">![Подключение сервера SIEM](media/siem-connected.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-197">![SIEM server connected](media/siem-connected.png)</span></span><br/><span data-ttu-id="13d8d-198">А здесь, можно увидеть, что сервер SIEM отключен:</span><span class="sxs-lookup"><span data-stu-id="13d8d-198">And here, we can see the SIEM server is disconnected:</span></span><br/><span data-ttu-id="13d8d-199">![SIEM сервер не подключен](media/siem-not-connected.png)</span><span class="sxs-lookup"><span data-stu-id="13d8d-199">![SIEM server not connected](media/siem-not-connected.png)</span></span> 
  
2. <span data-ttu-id="13d8d-200">На сервере Syslog/SIEM убедитесь, что видно, что оповещения поступили от приложения облаке Безопасность в Office 365.</span><span class="sxs-lookup"><span data-stu-id="13d8d-200">In your Syslog/SIEM server, make sure you see that alerts have arrived from Office 365 Cloud App Security.</span></span>
  
## <a name="regenerating-your-token"></a><span data-ttu-id="13d8d-201">Повторное создание ключа</span><span class="sxs-lookup"><span data-stu-id="13d8d-201">Regenerating your token</span></span>

<span data-ttu-id="13d8d-p116">При разрыве вашей маркера, всегда можно восстановить его. В таблице найдите строку для агента SIEM. Нажмите кнопку с многоточием и выберите **восстановить маркер**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p116">If you lose your token, you can always regenerate it. In the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Regenerate token**.</span></span>

![Обновите маркера, нажав кнопку с многоточием для агента SIEM](media/04de368a-b88e-4a9c-a830-58025cb98db6.png)
  
## <a name="editing-your-siem-agent"></a><span data-ttu-id="13d8d-206">Редактирование агента SIEM</span><span class="sxs-lookup"><span data-stu-id="13d8d-206">Editing your SIEM agent</span></span>

<span data-ttu-id="13d8d-p117">Для изменения агента SIEM, таблицы, найдите строку для агента SIEM. Нажмите кнопку с многоточием и выберите команду **Изменить**. Если изменить агента SIEM, не требуется повторно запустите файл .jar; автоматически обновляется.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p117">To edit your SIEM agent, in the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Edit**. If you edit the SIEM agent, you do not need to re-run the .jar file; it updates automatically.</span></span>

![Для изменения агента SIEM, щелкните многоточие и нажмите кнопку Изменить.](media/96d0b362-3e0c-4dff-b2b4-d7af5b1bfb91.png)
  
## <a name="deleting-your-siem-agent"></a><span data-ttu-id="13d8d-211">Удаление агента SIEM</span><span class="sxs-lookup"><span data-stu-id="13d8d-211">Deleting your SIEM agent</span></span>

<span data-ttu-id="13d8d-p118">Для удаления агента SIEM, таблицы, найдите строку для агента SIEM. Нажмите кнопку с многоточием и затем выберите команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p118">To delete your SIEM agent, in the table, locate the row for the SIEM agent. Click the ellipses, and then choose **Delete**.</span></span>

![Чтобы удалить SIEM агентов, щелкните многоточие и нажмите кнопку Удалить.](media/540b5bdf-5574-4ecc-a7b0-92a499a387d7.png)

## <a name="sample-logfiles"></a><span data-ttu-id="13d8d-215">Пример файлов журнала</span><span class="sxs-lookup"><span data-stu-id="13d8d-215">Sample logfiles</span></span>

<span data-ttu-id="13d8d-216">Ниже приведен пример файла журнала оповещений, которое может отправить на сервер SIEM:</span><span class="sxs-lookup"><span data-stu-id="13d8d-216">Here's an alerts logfile example that might be sent to a SIEM server:</span></span>

```
2017-07-15T20:42:30.531Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|myPolicy|3|externalId=596a7e360c204203a335a3fb start=1500151350531 end=1500151350531 msg=Activity policy ''myPolicy'' was triggered by ''admin@box-contoso.com'' suser=admin@box-contoso.com destinationServiceName=Box cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596a7e360c204203a335a3fb cs2Label=uniqueServiceAppIds cs2=APPID_BOX cs3Label=relatedAudits cs3=1500151288183_acc891bf-33e1-424b-a021-0d4370789660 cs4Label=policyIDs cs4=59f0ab82f797fa0681e9b1c7

2017-07-16T09:36:26.550Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b339b0c204203a33a51ae start=1500197786550 end=1500197786550 msg=Activity policy ''test-activity-policy'' was triggered by ''user@contoso.com'' suser=user@contoso.com destinationServiceName=Salesforce cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b339b0c204203a33a51ae cs2Label=uniqueServiceAppIds cs2=APPID_SALESFORCE cs3Label=relatedAudits cs3=1500197720691_b7f6317c-b8de-476a-bc8f-dfa570e00349 cs4Label=policyIDs cs4=

2017-07-16T09:17:03.361Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy3|3|externalId=596b2fd70c204203a33a3eeb start=1500196623361 end=1500196623361 msg=Activity policy ''test-activity-policy3'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Office 365 cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eeb cs2Label=uniqueServiceAppIds cs2=APPID_O365 cs3Label=relatedAudits cs3=1500196549157_a0e01f8a-e29a-43ae-8599-783c1c11597d cs4Label=policyIDs cs4=

2017-07-16T09:17:15.426Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy|3|externalId=596b2fd70c204203a33a3eec start=1500196635426 end=1500196635426 msg=Activity policy ''test-activity-policy'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Office 365 admin center cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b2fd70c204203a33a3eec cs2Label=uniqueServiceAppIds cs2=APPID_O365_PORTAL cs3Label=relatedAudits cs3=1500196557398_3e102b20-d9fa-4f66-b550-8c7a403bb4d8 cs4Label=policyIDs cs4=59f0ab35f797fa9811e9b1c7

2017-07-16T09:17:46.290Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy4|3|externalId=596b30200c204203a33a4765 start=1500196666290 end=1500196666290 msg=Activity policy ''test-activity-policy4'' was triggered by ''admin@contoso.com'' suser=admin@contoso.com destinationServiceName=Microsoft Exchange Online cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b30200c204203a33a4765 cs2Label=uniqueServiceAppIds cs2=APPID_OUTLOOK cs3Label=relatedAudits cs3=1500196587034_a8673602-7e95-46d6-a1fe-c156c4709c5d cs4Label=policyIDs cs4=

2017-07-16T09:41:04.369Z CEF:0|MCAS|SIEM_Agent|0.102.17|ALERT_CABINET_EVENT_MATCH_AUDIT|test-activity-policy2|3|externalId=596b34b10c204203a33a5240 start=1500198064369 end=1500198064369 msg=Activity policy ''test-activity-policy2'' was triggered by ''user2@test15-adallom.com'' suser=user2@test15-adallom.com destinationServiceName=Google cn1Label=riskScore cn1= cs1Label=portalURL cs1=https://cloud-app-security.com/#/alerts/596b34b10c204203a33a5240 cs2Label=uniqueServiceAppIds cs2=APPID_33626 cs3Label=relatedAudits cs3=1500197996117_fd71f265-1e46-4f04-b372-2e32ec874cd3 cs4Label=policyIDs cs4=
```

<span data-ttu-id="13d8d-217">Вот пример в формате CEF</span><span class="sxs-lookup"><span data-stu-id="13d8d-217">And here's a sample in CEF format</span></span>


|<span data-ttu-id="13d8d-218">Имя поля CEF</span><span class="sxs-lookup"><span data-stu-id="13d8d-218">CEF field name</span></span>  | <span data-ttu-id="13d8d-219">Описание</span><span class="sxs-lookup"><span data-stu-id="13d8d-219">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="13d8d-220">Запуск</span><span class="sxs-lookup"><span data-stu-id="13d8d-220">start</span></span>     | <span data-ttu-id="13d8d-221">Метка времени оповещения</span><span class="sxs-lookup"><span data-stu-id="13d8d-221">alert timestamp</span></span>        |
|<span data-ttu-id="13d8d-222">End</span><span class="sxs-lookup"><span data-stu-id="13d8d-222">end</span></span>     | <span data-ttu-id="13d8d-223">Метка времени оповещения</span><span class="sxs-lookup"><span data-stu-id="13d8d-223">alert timestamp</span></span>        |
|<span data-ttu-id="13d8d-224">время выполнения</span><span class="sxs-lookup"><span data-stu-id="13d8d-224">rt</span></span>     | <span data-ttu-id="13d8d-225">Метка времени оповещения</span><span class="sxs-lookup"><span data-stu-id="13d8d-225">alert timestamp</span></span>        |
|<span data-ttu-id="13d8d-226">MSG</span><span class="sxs-lookup"><span data-stu-id="13d8d-226">msg</span></span>     | <span data-ttu-id="13d8d-227">предупреждения описание, как показано на портале облачных приложений Office 365 безопасности</span><span class="sxs-lookup"><span data-stu-id="13d8d-227">alert description as shown in the Office 365 Cloud App Security portal</span></span>        |
|<span data-ttu-id="13d8d-228">suser</span><span class="sxs-lookup"><span data-stu-id="13d8d-228">suser</span></span>     | <span data-ttu-id="13d8d-229">Тема оповещения пользователя</span><span class="sxs-lookup"><span data-stu-id="13d8d-229">alert subject user</span></span>        |
|<span data-ttu-id="13d8d-230">destinationServiceName</span><span class="sxs-lookup"><span data-stu-id="13d8d-230">destinationServiceName</span></span>     | <span data-ttu-id="13d8d-231">оповещение, поступающих приложения, такие как Office 365, SharePoint или OneDrive</span><span class="sxs-lookup"><span data-stu-id="13d8d-231">alert originating app, such as Office 365, SharePoint, or OneDrive</span></span>        |
|<span data-ttu-id="13d8d-232">csLabel</span><span class="sxs-lookup"><span data-stu-id="13d8d-232">csLabel</span></span>     | <span data-ttu-id="13d8d-p119">Зависит от (метки имеют различные значения). Как правило метки очевидны, как targetObjects.</span><span class="sxs-lookup"><span data-stu-id="13d8d-p119">Varies (labels have different meanings). Typically, labels are self-explanatory, like targetObjects.</span></span>        |
|<span data-ttu-id="13d8d-235">cs</span><span class="sxs-lookup"><span data-stu-id="13d8d-235">cs</span></span>     | <span data-ttu-id="13d8d-236">Сведения, относящиеся к метки (например, целевого пользователя оповещения на примере метки)</span><span class="sxs-lookup"><span data-stu-id="13d8d-236">Information corresponding to a label (such as the target user of an alert as per the label example)</span></span>        |
  
## <a name="next-steps"></a><span data-ttu-id="13d8d-237">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="13d8d-237">Next steps</span></span>

- [<span data-ttu-id="13d8d-238">Действия, связанные с использованием, после развертывания Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="13d8d-238">Utilization activities after rolling out Office 365 Cloud App Security</span></span>](utilization-activities-for-ocas.md)
    
- [<span data-ttu-id="13d8d-239">Просмотрите и выполнять операции с оповещениями</span><span class="sxs-lookup"><span data-stu-id="13d8d-239">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="13d8d-240">Групповой IP-адреса для упрощения управления</span><span class="sxs-lookup"><span data-stu-id="13d8d-240">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

