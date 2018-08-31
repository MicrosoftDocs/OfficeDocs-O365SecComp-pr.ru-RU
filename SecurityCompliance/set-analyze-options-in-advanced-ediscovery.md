---
title: Настройка параметров анализа в Office 365 Advanced eDiscovery
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Рассмотрим эти действия, чтобы настроить параметры для процесса анализа в Office 365 расширенного обнаружения электронных данных, включая рядом с дубликаты, потоков электронной почты и темы.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "22534838"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="0b217-103">Настройка параметров анализа в Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0b217-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="0b217-p101">Расширенные обнаружения электронных данных требуется E3 Office 365 с помощью надстройки дополнительные соответствия или подписка на E5 для вашей организации. Если нет этого плана и попытайтесь расширенной обнаружения электронных данных, можно [подписаться на пробную версию Office 365 корпоративный E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="0b217-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="0b217-106">В расширенной eDiscovery, параметры анализа перед запуском анализ.</span><span class="sxs-lookup"><span data-stu-id="0b217-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="0b217-107">Установка параметров анализа</span><span class="sxs-lookup"><span data-stu-id="0b217-107">Set Analyze options</span></span>

<span data-ttu-id="0b217-p102">Открыть **Подготовка \> анализ** \> **программы установки**. Отображается следующее окно.</span><span class="sxs-lookup"><span data-stu-id="0b217-p102">Open **Prepare \> Analyze** \> **Setup**. The following window is displayed.</span></span>
  
![Настройка параметров анализа](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="0b217-p103">**Рядом с дубликаты и электронной почты потоков** Установите этот флажок, если требуется выполнить анализ. Установлен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b217-p103">**Near-duplicates and email threads** Check this box if you want to run the analysis. It is selected by default.</span></span> 
  
 <span data-ttu-id="0b217-113">**Подобия документов** Введите значение порога дубликаты Near или примите значение по умолчанию 65%.</span><span class="sxs-lookup"><span data-stu-id="0b217-113">**Document similarity**Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="0b217-p104">**Темы** Установите флажок, чтобы обрабатывать все файлы и назначить их тем. По умолчанию этот флажок не установлен. Введите следующие параметры, если вы хотите выполнить тем обработки.</span><span class="sxs-lookup"><span data-stu-id="0b217-p104">**Themes**Check this box to process all files and assign themes to them. By default, this check box is not selected. Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="0b217-p105">**Максимальное количество тем** Введите или выберите значение для количества тем для создания. Значение по умолчанию равно 200.</span><span class="sxs-lookup"><span data-stu-id="0b217-p105">**Max number of themes**Enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="0b217-p106">Увеличение числа тем влияет на производительность, а также возможность темы Подготовка к использованию. Чем больше число тем, большую детализацию эти атрибуты. Например, если набор 50 темы включают темы, такие как «Баскетбольная, данных стимулирует, Ножницы, Lakers»; 300 тем может включать отдельные тем: «Подстегивает», «Ножницы», «Lakers». Если бы не знают темы «Баскетбольная» и использовать эту функцию для ECA видеть темы «Баскетбольная» может быть полезна. Однако если обработки слишком много тем, никогда не может отображаться слово «Баскетбольная» и могут не знать данных стимулирует и Ножницы, хороший Баскетбольная тем для просмотра, а не загружается и используются для Сверхтонкая элементов, которые будут входить на.</span><span class="sxs-lookup"><span data-stu-id="0b217-p106">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="0b217-p107">**Предлагаемые тем** Можно предложить слова темы для управления тем обработки. Расширенные обнаружения электронных данных будет сосредоточиться на этих предложенного слов и попытаться создать один или несколько соответствующих темы на основе параметров «Максимальное количество темы».</span><span class="sxs-lookup"><span data-stu-id="0b217-p107">**Suggested themes**You can suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="0b217-p108">Например если предложенного слово «computer» и указанного «2» в качестве «максимальное количество темы», расширенные обнаружения электронных данных будет пытаться создать две темы, влияющие на слово «computer». Две темы может быть «компьютерного программного обеспечения» и «hardware компьютер», например.</span><span class="sxs-lookup"><span data-stu-id="0b217-p108">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Добавление предложенной темы](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="0b217-129">Для просмотра, добавления или изменения предложенного тем, нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="0b217-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="0b217-p109">В области **предлагаемые тем** , нажмите кнопку **Добавить**![добавить значок](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) значок, чтобы добавить тему. В панели **Добавить тему предложенного** Добавление ключевых слов, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="0b217-p109">In the **Suggested themes** panel, click the **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme. In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="0b217-132">В **число тем**выберите значение для определения количества тем, которые дополнительно обнаружения электронных данных будет пытаться создать для этих слов (значение по умолчанию — 1 темы).</span><span class="sxs-lookup"><span data-stu-id="0b217-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="0b217-133">Нажмите кнопку **Сохранить** и закройте диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0b217-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="0b217-p110">Общее количество тем включает в себя предложенных тем. Общее тем предложенных не может превышать общее тем. Если существует множество предложенных тем относительно общее тем, несколько темы «novel» будет обнаружен системой потому что большая часть темы будет назначаться предложенных тем.</span><span class="sxs-lookup"><span data-stu-id="0b217-p110">The total number of themes includes Suggested Themes. The total Suggested Themes cannot exceed the total themes. If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="0b217-137">**Режим** В раскрывающемся списке выберите вариант **темы** :</span><span class="sxs-lookup"><span data-stu-id="0b217-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="0b217-138">**Создание и применение модели**: вычисляет тем с моделями из сегмента файлов и затем распределяет файлы между ними.</span><span class="sxs-lookup"><span data-stu-id="0b217-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="0b217-p111">**Создать модель**: вычисляет модель тем для сегмента файлов. Применить процесс разделения файлов выполняется отдельно в другое время.</span><span class="sxs-lookup"><span data-stu-id="0b217-p111">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="0b217-p112">**Применить модель**: этот параметр доступен только в том случае, если модель была создана ранее и еще не были применены. Это будет разделить файлы на основании тем.</span><span class="sxs-lookup"><span data-stu-id="0b217-p112">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="0b217-143">Можно также [набор игнорировать текст](set-ignore-text-in-advanced-ediscovery.md) и [Задайте дополнительные параметры анализ](set-analyze-advanced-settings-in-advanced-ediscovery.md) для анализа.</span><span class="sxs-lookup"><span data-stu-id="0b217-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="0b217-p113">После установки эти параметры, щелкните **Анализ** для запуска. [Просмотр анализа результаты](view-analyze-results-in-advanced-ediscovery.md) отображаются.</span><span class="sxs-lookup"><span data-stu-id="0b217-p113">After you've set these options, click **Analyze** to run. [View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b217-146">См. также</span><span class="sxs-lookup"><span data-stu-id="0b217-146">See also</span></span>

[<span data-ttu-id="0b217-147">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0b217-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="0b217-148">Общие сведения о документе подобия</span><span class="sxs-lookup"><span data-stu-id="0b217-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0b217-149">Задать текст пропустить</span><span class="sxs-lookup"><span data-stu-id="0b217-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0b217-150">Настройка дополнительных параметров на вкладке "Анализ"</span><span class="sxs-lookup"><span data-stu-id="0b217-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0b217-151">Просмотр результатов анализа</span><span class="sxs-lookup"><span data-stu-id="0b217-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

