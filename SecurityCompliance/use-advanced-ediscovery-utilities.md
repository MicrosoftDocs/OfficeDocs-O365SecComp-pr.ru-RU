---
title: Использование служебных программ Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Узнайте о служебных программ в Office 365 расширенного обнаружения электронных данных, включая журнал обращения, очистку данных, обработки ошибок, изменить прозрачность анализ и релевантности.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534330"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="eb28f-103">Использование служебных программ Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eb28f-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="eb28f-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="eb28f-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="eb28f-106">Служебные программы, которые отображаются и доступны в расширенной eDiscovery зависят от роли пользователя и контекста.</span><span class="sxs-lookup"><span data-stu-id="eb28f-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="eb28f-107">Журнал обращений</span><span class="sxs-lookup"><span data-stu-id="eb28f-107">Case log</span></span>

<span data-ttu-id="eb28f-p102">Журнал обращения предоставляет подробный список функций приложения обработки действий, которые можно использовать для отслеживания, устранение неполадок и устранение ошибок и предупреждений. Журнал можно создается и хранятся на узел или сервер либо непосредственно в адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p102">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings. The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="eb28f-p103">Файл журнала можно также загрузить на клиентский компьютер. Параметр загрузки клиента могут включаться и отключаться согласно конфигурации и роли.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p103">The log file can also be downloaded to the client's computer. The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="eb28f-112">В строке меню щелкните значок **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="eb28f-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="eb28f-113">В **Параметры и служебные программы \> служебных программ** выберите **журнала обращения \> установки**.</span><span class="sxs-lookup"><span data-stu-id="eb28f-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="eb28f-114">Выберите **уровень журнала** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb28f-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="eb28f-p104">**Стандартный**: включает в себя данные журнала basic. Этот параметр обычно требуются для мониторинга и следует использовать, если не рекомендуется, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p104">**Standard**: Includes the basic log data. This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="eb28f-117">**Минимальная**: используется для очень больших случаев и возвращает только последних данных.</span><span class="sxs-lookup"><span data-stu-id="eb28f-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="eb28f-p105">Нажмите кнопку **Запуск примера журнала**. Журнал создается и отображается путь. Сведения о ходе выполнения задач для текущего и последнего задачи отображается в области состояния задач.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p105">Click **Run Case log**. The log is generated and path is displayed. The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="eb28f-121">Очистка данных</span><span class="sxs-lookup"><span data-stu-id="eb28f-121">Clear data</span></span>

<span data-ttu-id="eb28f-p106">Если это необходимо удалить или повторной инициализации данные вариантов, должен быть инициализирован экземпляр базы данных. Служебная программа очистки данных удаляет все указанные элементы из социальной базы данных, текстовые файлы, case папки и накопленная результатов. Функция может выполняться только администратором.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p106">If it is necessary to delete or reinitialize case data, the database instance must be initialized. The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results. The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="eb28f-p107">Это действие не является обратимое и будет снимите все теги релевантности и анализа, выполняемой эксперт. Сохраните резервную копию данных, если это необходимо. Этот параметр используется с особой осторожностью. Удаление файлов с тегами и ранжированных могут влиять на релевантности результатов.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p107">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert. Save a backup of data, if necessary. Use this option with extreme care. Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="eb28f-129">В строке меню щелкните значок **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="eb28f-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="eb28f-130">В **Параметры и служебные программы \> служебных программ** выберите **очистку данных \> установки**.</span><span class="sxs-lookup"><span data-stu-id="eb28f-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="eb28f-131">Выберите соответствующее значение параметра сведения для инициализации:</span><span class="sxs-lookup"><span data-stu-id="eb28f-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="eb28f-p108">**Релевантность**: Удаляет все операции, выполняемые в релевантности, включая определения нагрузок и связи файлов для загрузки. Удаляет все примеры и маркировки.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p108">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads. It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="eb28f-134">**Рядом с дубликаты и электронной почты потоков**: удаляются все данные анализа рядом с дубликатов и электронной почты потоков.</span><span class="sxs-lookup"><span data-stu-id="eb28f-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="eb28f-135">**Темы**: Удаляет данные, связанные с тем.</span><span class="sxs-lookup"><span data-stu-id="eb28f-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="eb28f-136">**Экспортировать журнал**: Удаляет сведения о журнале экспорт пакетов.</span><span class="sxs-lookup"><span data-stu-id="eb28f-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="eb28f-p109">Нажмите кнопку **Очистить данные**. Данные вариантов снят. Сведения о ходе выполнения задач для текущего и последнего задачи отображается в области **состояния задачи** .</span><span class="sxs-lookup"><span data-stu-id="eb28f-p109">Click **Clear data**. The case data is cleared. The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="eb28f-140">Изменение релевантности</span><span class="sxs-lookup"><span data-stu-id="eb28f-140">Modify Relevance</span></span>

<span data-ttu-id="eb28f-141">В этом разделе описывается, как пропустить или откат примера релевантности.</span><span class="sxs-lookup"><span data-stu-id="eb28f-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="eb28f-142">В строке меню щелкните значок **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="eb28f-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="eb28f-143">В **Параметры и служебные программы \> служебных программ** выберите **Изменить релевантности**.</span><span class="sxs-lookup"><span data-stu-id="eb28f-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="eb28f-144">Выберите один из вариантов:</span><span class="sxs-lookup"><span data-stu-id="eb28f-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="eb28f-p110">**Пример текущей пропустить — для текущего пользователя**: это будет пометить, как **Пропустить**все файлы без тегов в образце open обращения пользователя, выполняющего программу. На файлы, помеченные как **Пропустить**не выполняется обработка релевантности.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p110">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility. Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="eb28f-p111">**Пропустить текущий пример — все открытые примеры**: это будет пометить, как **Пропустить**все файлы без тегов в всех открытых примеры для всех пользователей. Этот параметр не рекомендуется, если пользователи в настоящее время тегов примеры.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p111">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users. This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="eb28f-p112">**Откат последнего примера**: последнего выполненного релевантности, учебные примеры будет выполнен откат, независимо от того, будет ли это до или после процесса «Вычислить». Откат дополнительной пример не допускается.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p112">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process. Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="eb28f-151">Нажмите кнопку **выполнить** , чтобы выполнить.</span><span class="sxs-lookup"><span data-stu-id="eb28f-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="eb28f-152">Анализ прозрачность</span><span class="sxs-lookup"><span data-stu-id="eb28f-152">Transparency analysis</span></span>

<span data-ttu-id="eb28f-p113">Служебная программа анализа прозрачность включает подробное представление файлов и их назначенный показатель релевантности. Отчет можно использовать, как выполняется проверка работоспособности или для сравнения релевантности файла, определяется специалиста по проверке по сравнению с релевантности, назначенный с расширенной обнаружения электронных данных.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p113">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score. The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="eb28f-p114">В дополнение к показателям релевантности расширенной eDiscovery вычисляет и назначает вес ключевого слова, которые необходимо учитывать контекст ключевого слова. То же слово в файле можно назначить разные веса, в зависимости от контекста и расположение. Каждое ключевое слово помечается с помощью увеличение масштаба интенсивности цвета от желтого цвета до темно-оранжевый и различная оттенки серого цвета. Цвет используется для отображения слово относительный положительное или отрицательное влияние на оценку релевантности.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p114">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context. The same word in a file can be assigned different weights, depending on context and location. Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray. Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="eb28f-159">В сценарий делами проблем с несколькими прозрачность анализа созданием отчета для каждой проблемы.</span><span class="sxs-lookup"><span data-stu-id="eb28f-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="eb28f-160">В строке меню щелкните значок **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="eb28f-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="eb28f-161">В **Параметры и служебные программы \> служебных программ** выберите **анализа прозрачность \> установки**.</span><span class="sxs-lookup"><span data-stu-id="eb28f-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="eb28f-162">В ** идентификатор файла **, введите идентификатор файла файла для обработки.</span><span class="sxs-lookup"><span data-stu-id="eb28f-162">In ** File ID **, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="eb28f-163">В списке **проблему** выберите соответствующую проблему.</span><span class="sxs-lookup"><span data-stu-id="eb28f-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="eb28f-p115">Нажмите кнопку **прозрачность анализа**. По завершении отображается отчет анализа прозрачность для файла, показано, как цвета ключевое слово соответствуют общий показатель релевантности.</span><span class="sxs-lookup"><span data-stu-id="eb28f-p115">Click **Transparency analysis**. Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb28f-166">См. также</span><span class="sxs-lookup"><span data-stu-id="eb28f-166">See also</span></span>

[<span data-ttu-id="eb28f-167">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eb28f-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="eb28f-168">Определение параметров case и клиента</span><span class="sxs-lookup"><span data-stu-id="eb28f-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

