---
title: Создание пользовательского типа конфиденциальной информации
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Узнайте, как создавать, редактировать, удалять и тестировать собственные типы конфиденциальной информации для DLP в графическом пользовательском интерфейсе Центра безопасности и соответствия требованиям Office 365.
ms.openlocfilehash: 16bc49f23de20479ed18ce56720fd70a05b986e3
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410814"
---
# <a name="create-a-custom-sensitive-information-type"></a><span data-ttu-id="185d5-103">Создание пользовательского типа конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="185d5-103">Create a custom sensitive information type</span></span>

<span data-ttu-id="185d5-p101">DLP в Office 365 включает много встроенных [типов конфиденциальной информации](what-the-sensitive-information-types-look-for.md), которые вы можете использовать в своих политиках защиты от потери данных. С помощью этих типов можно обнаруживать и защищать номера кредитных карт, банковских счетов, паспортов и многие другие сведения.</span><span class="sxs-lookup"><span data-stu-id="185d5-p101">Data loss prevention (DLP) in Office 365 includes many built-in [sensitive information types](what-the-sensitive-information-types-look-for.md) that are ready for you to use in your DLP policies. These built-in types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more.</span></span> 

<span data-ttu-id="185d5-106">Если вам нужно обнаруживать и защищать конфиденциальную информацию другого типа (например, идентификаторы сотрудников или номера проектов, для которых в вашей организации используется особой формат), вы можете создать пользовательский тип конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="185d5-106">But if you need to identify and protect a different type of sensitive information (for example, employee IDs or project numbers that uses a format specific to your organization) you can create a custom sensitive information type.</span></span>

<span data-ttu-id="185d5-107">Основные компоненты пользовательского типа конфиденциальной информации:</span><span class="sxs-lookup"><span data-stu-id="185d5-107">The fundamental parts of a custom sensitive information type are:</span></span>

- <span data-ttu-id="185d5-108">**Основной шаблон**: коды сотрудников, номера проектов и т. д. Как правило, он определяется регулярным выражением (RegEx), но также может представлять собой список ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="185d5-108">**Primary pattern**: employee ID numbers, project numbers, etc. This is typically identified by a regular expression (RegEx), but it can also be a list of keywords.</span></span>

- <span data-ttu-id="185d5-p102">**Дополнительные признаки.** Допустим, вы рассматриваете девятизначный код сотрудника. Не все девятизначные числа являются идентификаторами сотрудников, поэтому вы можете искать дополнительный текст: ключевые слова (например, "сотрудник", "бейдж", "ИД") или другие текстовые шаблоны, основанные на дополнительных регулярных выражениях. Дополнительные признаки (также называемые _вспомогательными_ или _подтверждающими_ признаками) повышают вероятность того, что девятизначный номер в содержимом действительно является кодом сотрудника.</span><span class="sxs-lookup"><span data-stu-id="185d5-p102">**Additional evidence**: Suppose you're looking for a nine-digit employee ID number. Not all nine-digit numbers are employee ID numbers, so you can look for additional text: keywords like "employee", "badge", "ID", or other text patterns based on additional regular expressions. This supporting evidence (also known as _supporting_ or _corroborative_ evidence) increases the likelihood that nine-digit number found in content is really an employee ID number.</span></span>

- <span data-ttu-id="185d5-p103">**Расстояние между символами.** Будет логично предположить, что чем ближе основной шаблон и вспомогательные признаки друг к другу, тем вероятнее, что обнаруженный контент будет именно тем, что вам нужно. Вы можете задать расстояние в символах между основным шаблоном и вспомогательными признаками (также называемое _интервалом вероятности_), как показано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="185d5-p103">**Character proximity**: It makes sense that the closer the primary pattern and the supporting evidence are to each other, the more likely the detected content is going to be what you're looking for. You can specify the character distance between the primary pattern and the supporting evidence (also known as the _proximity window_) as shown in the following diagram:</span></span>

    ![Схема подтверждающего признака и интервала вероятности](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)

- <span data-ttu-id="185d5-p104">**Уровень вероятности.** Чем больше вспомогательных признаков, тем выше вероятность того, что обнаруженное совпадение относится к конфиденциальным данным. Вы можете назначать более высокие уровни вероятности для совпадений, обнаруженных по большему количеству признаков.</span><span class="sxs-lookup"><span data-stu-id="185d5-p104">**Confidence level**: The more supporting evidence you have, the higher the likelihood that a match contains the sensitive information you're looking for. You can assign higher levels of confidence for matches that are detected by using more evidence.</span></span>

  <span data-ttu-id="185d5-p105">При выполнении условия шаблон возвращает значения количества и уровня вероятности, которые вы можете использовать в условиях политик защиты от потери данных. Добавляя условие для обнаружения типа конфиденциальной информации в политику защиты от потери данных, вы можете изменить значения количества и уровня вероятности, как показано на следующей схеме:</span><span class="sxs-lookup"><span data-stu-id="185d5-p105">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policies. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown in the following diagram:</span></span>

    ![Пример параметров количества экземпляров и точности совпадения](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)

<span data-ttu-id="185d5-120">Создать пользовательский тип конфиденциальной информации для защиты от потери данных в Центре безопасности и соответствия требованиям Office 365 можно следующими способами:</span><span class="sxs-lookup"><span data-stu-id="185d5-120">To create custom sensitive information types in the Office 365 Security & Compliance Center, you have the following options:</span></span>

- <span data-ttu-id="185d5-p106">**Через пользовательский интерфейс.** Этот способ проще и быстрее, но обеспечивает меньше возможностей настройки, чем PowerShell. Эти процедуры описаны далее в статье.</span><span class="sxs-lookup"><span data-stu-id="185d5-p106">**Use the UI**: This method is easier and faster, but you have less configuration options than PowerShell. The rest of this topic describes these procedures.</span></span>

- <span data-ttu-id="185d5-p107">**С помощью PowerShell.** Для этого необходимо сначала создать XML-файл (называемый _пакетом правил_), который содержит один или несколько типов конфиденциальной информации, а затем использовать PowerShell для импорта пакета правил (эта задача тривиальна по сравнению с его созданием). Этот способ намного сложнее, чем применение пользовательского интерфейса, но предоставляет более широкие возможности настройки. Инструкции см. в статье [Создание пользовательского типа конфиденциальной информации в PowerShell Центра безопасности и соответствия требованиям Office 365](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="185d5-p107">**Use PowerShell**: This method requires that you first create an XML file (called a _rule package_) that contains one or more sensitive information types, and then you use PowerShell to import the rule package (importing the rule package is trivial compared to creating the rule package. This method is much more complex than the UI, but you have more configuration options. For instructions, see [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span>

<span data-ttu-id="185d5-126">Основные различия между ними описаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="185d5-126">The key differences are described in the following table:</span></span>

|<span data-ttu-id="185d5-127">**Создание пользовательских типов конфиденциальной информации в пользовательском интерфейсе**</span><span class="sxs-lookup"><span data-stu-id="185d5-127">**Custom sensitive information types in the UI**</span></span>|<span data-ttu-id="185d5-128">**Создание пользовательских типов конфиденциальной информации в PowerShell**</span><span class="sxs-lookup"><span data-stu-id="185d5-128">**Custom sensitive information types in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="185d5-129">Для названия и описания используется один язык.</span><span class="sxs-lookup"><span data-stu-id="185d5-129">Name and Description are in one language.</span></span>|<span data-ttu-id="185d5-130">Поддерживает несколько языков для имени и описания.</span><span class="sxs-lookup"><span data-stu-id="185d5-130">Supports multiple languages for Name and Description.</span></span>|
|<span data-ttu-id="185d5-131">Поддерживает один шаблон.</span><span class="sxs-lookup"><span data-stu-id="185d5-131">Supports one pattern.</span></span>|<span data-ttu-id="185d5-132">Поддерживает несколько шаблонов.</span><span class="sxs-lookup"><span data-stu-id="185d5-132">Supports multiple patterns.</span></span>|
|<span data-ttu-id="185d5-133">Вспомогательными признаками могут быть:</span><span class="sxs-lookup"><span data-stu-id="185d5-133">Supporting evidence can be:</span></span> <br/><span data-ttu-id="185d5-134">• регулярные выражения;</span><span class="sxs-lookup"><span data-stu-id="185d5-134">• Regular expressions</span></span> <br/><span data-ttu-id="185d5-135">• ключевые слова;</span><span class="sxs-lookup"><span data-stu-id="185d5-135">• Keywords</span></span> <br/><span data-ttu-id="185d5-136">• словари ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="185d5-136">• Keyword dictionaries</span></span>|<span data-ttu-id="185d5-137">Вспомогательными признаками могут быть:</span><span class="sxs-lookup"><span data-stu-id="185d5-137">Supporting evidence can be:</span></span> <br/><span data-ttu-id="185d5-138">• регулярные выражения;</span><span class="sxs-lookup"><span data-stu-id="185d5-138">• Regular expressions</span></span> <br/><span data-ttu-id="185d5-139">• ключевые слова;</span><span class="sxs-lookup"><span data-stu-id="185d5-139">• Keywords</span></span> <br/><span data-ttu-id="185d5-140">• словари ключевых слов;</span><span class="sxs-lookup"><span data-stu-id="185d5-140">• Keyword dictionaries</span></span> <br/><span data-ttu-id="185d5-141">• [встроенные функции защиты от потери данных.](what-the-dlp-functions-look-for.md)</span><span class="sxs-lookup"><span data-stu-id="185d5-141">• [Built-in DLP functions](what-the-dlp-functions-look-for.md)</span></span>|
|<span data-ttu-id="185d5-142">Пользовательские типы конфиденциальной информации добавляются в пакет правил Microsoft.SCCManaged.CustomRulePack.</span><span class="sxs-lookup"><span data-stu-id="185d5-142">Custom sensitive information types are added to the rule package named Microsoft.SCCManaged.CustomRulePack</span></span>|<span data-ttu-id="185d5-143">Вы можете создать до 10 пакетов правил, которые содержат пользовательские типы конфиденциальной информации.</span><span class="sxs-lookup"><span data-stu-id="185d5-143">You can create up to 10 rule packages that contain custom sensitive information types.</span></span>|
|<span data-ttu-id="185d5-144">Для соответствия шаблону необходимо обнаружить основной шаблон и все вспомогательные признаки (используется неявный оператор И).</span><span class="sxs-lookup"><span data-stu-id="185d5-144">Pattern match requires the detection of the primary pattern and all supporting evidence (the implicit AND operator is used).</span></span>|<span data-ttu-id="185d5-145">Для соответствия шаблону необходимо обнаружить основной шаблон и настраиваемое количество вспомогательных признаков (используются неявные операторы И и ИЛИ).</span><span class="sxs-lookup"><span data-stu-id="185d5-145">Pattern match requires the detection of the primary pattern and a configurable amount of supporting evidence (implicit AND and OR operators can be used).</span></span>|

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="185d5-146">Что нужно знать перед началом работы</span><span class="sxs-lookup"><span data-stu-id="185d5-146">What do you need to know before you begin?</span></span>

- <span data-ttu-id="185d5-147">Сведения о том, как открыть Центр безопасности и соответствия требованиям, см. в статье [Центр безопасности и соответствия требованиям Office 365](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="185d5-147">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="185d5-p108">Для работы с пользовательскими типами конфиденциальной информации вы должны быть знакомы с регулярными выражениями (RegEx). Дополнительные сведения о модуле Boost.RegEx (прежнее название — RegEx++), используемом для обработки текста, см. в статье [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span><span class="sxs-lookup"><span data-stu-id="185d5-p108">Custom sensitive information types require familiarity with regular expressions (RegEx). For more information about the Boost.RegEx (formerly known as RegEx++) engine that's used for processing the text, see [Boost.Regex 5.1.3](https://www.boost.org/doc/libs/1_68_0/libs/regex/doc/html/).</span></span>

  <span data-ttu-id="185d5-p109">Центр обслуживания клиентов Майкрософт не может предоставлять вам пользовательские определения для сопоставления контента (создавать пользовательские категории или шаблоны регулярных выражений). Инженеры службы поддержки могут оказывать ограниченную поддержку по этой функции (например, предоставлять примеры шаблонов регулярных выражений для тестирования или помогать с устранением неполадок имеющегося шаблона, который не срабатывает должным образом), но не могут гарантировать, что то или иное решение для сопоставления контента будет соответствовать вашим требованиям или обязательствам.</span><span class="sxs-lookup"><span data-stu-id="185d5-p109">Microsoft Customer Service & Support can't assist with providing custom content-matching definitions (creating custom classifications or regular expression patterns). Support engineers can provide limited support for the feature (for example, providing sample regular expression patterns for testing purposes, or assisting with troubleshooting an existing regular expression pattern that's not triggering as expected), but can't provide assurances that any custom content-matching development will fulfill your requirements or obligations.</span></span>

- <span data-ttu-id="185d5-p110">DLP использует программу-обходчик для поиска, чтобы обнаруживать и классифицировать конфиденциальную информацию на сайтах SharePoint Online и OneDrive для бизнеса. Чтобы определить новый пользовательский тип конфиденциальной информации в имеющемся контенте, необходимо выполнить повторный обход контента для семейства веб-сайтов, списка или библиотеки. Дополнительные сведения см. в статье [Запрашивание обхода и повторного индексирования сайта, библиотеки или списка вручную](https://docs.microsoft.com/sharepoint/crawl-site-content).</span><span class="sxs-lookup"><span data-stu-id="185d5-p110">DLP uses the search crawler to identify and classify sensitive information in SharePoint Online and OneDrive for Business sites. To identify your new custom sensitive information type in existing content, the content must be recrawled. Content is recrawled based on a schedule, but you can manually recrawl content for a site collection, list, or library. For more information, see [Manually request crawling and re-indexing of a site, a library or a list](https://docs.microsoft.com/sharepoint/crawl-site-content).</span></span>

## <a name="create-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="185d5-156">Создание пользовательского типа конфиденциальной информации в Центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="185d5-156">Create custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="185d5-157">В Центре безопасности и соответствия требованиям выберите **Классификации** \> **Типы конфиденциальной информации** и нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="185d5-157">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

<span data-ttu-id="185d5-158">Параметры не требуют особых пояснений и описываются на соответствующей странице мастера.</span><span class="sxs-lookup"><span data-stu-id="185d5-158">The settings are fairly self-evident, and are explained on the associate page of the wizard:</span></span>

- <span data-ttu-id="185d5-159">**Имя**</span><span class="sxs-lookup"><span data-stu-id="185d5-159">**Name**</span></span>

- <span data-ttu-id="185d5-160">**Описание**</span><span class="sxs-lookup"><span data-stu-id="185d5-160">**Description**</span></span>

- <span data-ttu-id="185d5-161">**Расстояние**</span><span class="sxs-lookup"><span data-stu-id="185d5-161">**Proximity**</span></span>

- <span data-ttu-id="185d5-162">**Уровень вероятности**</span><span class="sxs-lookup"><span data-stu-id="185d5-162">**Confidence level**</span></span>

- <span data-ttu-id="185d5-163">**Элемент основного шаблона** (ключевые слова, регулярное выражение или словарь)</span><span class="sxs-lookup"><span data-stu-id="185d5-163">**Primary pattern element** (keywords, regular expression, or dictionary)</span></span>

- <span data-ttu-id="185d5-164">Необязательные **элементы вспомогательного шаблона** (ключевые слова, регулярное выражение или словарь) и соответствующее значение **минимальной стоимости**.</span><span class="sxs-lookup"><span data-stu-id="185d5-164">Optional **Supporting pattern elements** (keywords, regular expression, or dictionary) and a corresponding **Minimum cost** value.</span></span>

<span data-ttu-id="185d5-p111">Предположим, вам нужен пользовательский тип конфиденциальной информации, обнаруживающий в контенте 9-значные номера сотрудников, а также ключевые слова "сотрудник", "ИД" и "бейдж". Чтобы создать этот тип, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="185d5-p111">Here's a scenario: You want a custom sensitive information type that detects 9-digit employee numbers in content, along with the keywords "employee" "ID" and "badge". To create this custom sensitive information type, do the following steps:</span></span>

1. <span data-ttu-id="185d5-167">В Центре безопасности и соответствия требованиям выберите **Классификации** \> **Типы конфиденциальной информации** и нажмите **Создать**.</span><span class="sxs-lookup"><span data-stu-id="185d5-167">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and click **Create**.</span></span>

    ![Расположение элемента "Типы конфиденциальной информации" и кнопки "Создать"](media/scc-cust-sens-info-type-new.png)

2. <span data-ttu-id="185d5-169">На открывшейся странице **Выберите имя и описание** введите следующие значения:</span><span class="sxs-lookup"><span data-stu-id="185d5-169">In the **Choose a name and description** page that opens, enter the following values:</span></span>

  - <span data-ttu-id="185d5-170">**Имя**: "ИД сотрудника".</span><span class="sxs-lookup"><span data-stu-id="185d5-170">**Name**: Employee ID.</span></span>

  - <span data-ttu-id="185d5-171">**Описание**: "Обнаружение девятизначных кодов сотрудников Contoso".</span><span class="sxs-lookup"><span data-stu-id="185d5-171">**Description**: Detect nine-digit Contoso employee ID numbers.</span></span>

    ![Страница имени и описания](media/scc-cust-sens-info-type-new-name-desc.png)

    <span data-ttu-id="185d5-173">По завершении нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="185d5-173">When you're finished, click **Next**.</span></span>

3. <span data-ttu-id="185d5-174">На открывшейся странице **Требования для сопоставления** нажмите **Добавить элемент** и настройте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="185d5-174">In the **Requirements for matching** page that opens, click **Add an element** configure the following settings:</span></span>

    - <span data-ttu-id="185d5-175">Чтобы настроить **Обнаруживать контент, содержащий**:</span><span class="sxs-lookup"><span data-stu-id="185d5-175">**Detect content containing**:</span></span>
 
      <span data-ttu-id="185d5-p112">Щелкните **Любое из указанных** и выберите **Регулярное выражение**.</span><span class="sxs-lookup"><span data-stu-id="185d5-p112">a. Click **Any of these** and select **Regular expression**.</span></span>

      <span data-ttu-id="185d5-p113">В поле регулярного выражения введите `(\s)(\d{9})(\s)` (девятизначное число с пробелами с обеих сторон).</span><span class="sxs-lookup"><span data-stu-id="185d5-p113">b. In the regular expression box, enter `(\s)(\d{9})(\s)` (nine-digit numbers surrounded by white space).</span></span>
  
    - <span data-ttu-id="185d5-180">Чтобы настроить **Вспомогательные элементы**, нажмите **Добавить вспомогательные элементы** и выберите **Содержит этот список ключевых слов**.</span><span class="sxs-lookup"><span data-stu-id="185d5-180">**Supporting elements**: Click **Add supporting elements** and select **Contains this keyword list**.</span></span>

    - <span data-ttu-id="185d5-181">В открывшейся области **Содержит этот список ключевых слов** настройте указанные ниже параметры.</span><span class="sxs-lookup"><span data-stu-id="185d5-181">In the **Contains this keyword list** area that appears, configure the following settings:</span></span>

      - <span data-ttu-id="185d5-182">**Список ключевых слов.** Введите следующее значение: сотрудник,ИД,бейдж.</span><span class="sxs-lookup"><span data-stu-id="185d5-182">**Keyword list**: Enter the following value: employee,ID,badge.</span></span>

      - <span data-ttu-id="185d5-183">**Минимальное количество.** Оставьте значение по умолчанию (1).</span><span class="sxs-lookup"><span data-stu-id="185d5-183">**Minimum count**: Leave the default value 1.</span></span>

    - <span data-ttu-id="185d5-184">Оставьте для параметра **Уровень вероятности** значение по умолчанию (60).</span><span class="sxs-lookup"><span data-stu-id="185d5-184">Leave the default **Confidence level** value 60.</span></span> 

    - <span data-ttu-id="185d5-185">Оставьте для параметра **Расстояние между символами** значение по умолчанию (300).</span><span class="sxs-lookup"><span data-stu-id="185d5-185">Leave the default **Character proximity** value 300.</span></span>

    ![Страница "Требования для сопоставления"](media/scc-cust-sens-info-type-new-reqs.png)

    <span data-ttu-id="185d5-187">По завершении нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="185d5-187">When you're finished, click **Next**.</span></span>

4. <span data-ttu-id="185d5-188">На открывшейся странице **Проверка и завершение** проверьте параметры и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="185d5-188">On the **Review and finalize** page that opens, review the settings and click **Finish**.</span></span>

    ![Страница "Проверка и завершение"](media/scc-cust-sens-info-type-new-review.png)

5. <span data-ttu-id="185d5-p114">На следующей странице вам предлагается протестировать новый тип конфиденциальной информации, нажав кнопку **Да**. Дополнительные сведения см. в статье [Тестирование пользовательских типов конфиденциальной информации в Центре безопасности и соответствия требованиям](#test-custom-sensitive-information-types-in-the-security--compliance-center). Чтобы протестировать правило позже, нажмите кнопку **Нет**.</span><span class="sxs-lookup"><span data-stu-id="185d5-p114">The next page encourages you to test the new custom sensitive information type by clicking **Yes**. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center). To test the rule later, click **No**.</span></span>

    ![Страница с рекомендацией провести тестирование](media/scc-cust-sens-info-type-new-test.png)

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="185d5-194">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="185d5-194">How do you know this worked?</span></span>

<span data-ttu-id="185d5-195">Чтобы убедиться, что вы успешно создали новый тип конфиденциальной информации, выполните любое из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="185d5-195">To verify that you've successfully created a new sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="185d5-196">Откройте раздел **Классификации** \> **Типы конфиденциальной информации** и убедитесь, что новый тип присутствует в списке.</span><span class="sxs-lookup"><span data-stu-id="185d5-196">Go to **Classifications** \> **Sensitive info types** and verify the new custom sensitive information type is listed.</span></span>

  - <span data-ttu-id="185d5-p115">Протестируйте новый тип конфиденциальной информации. Дополнительные сведения см. в статье [Тестирование пользовательских типов конфиденциальной информации в Центре безопасности и соответствия требованиям](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="185d5-p115">Test the new custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="modify-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="185d5-199">Редактирование пользовательских типов конфиденциальной информации в Центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="185d5-199">Modify custom sensitive information types in the Security & Compliance Center</span></span>

<span data-ttu-id="185d5-200">**Примечания**.</span><span class="sxs-lookup"><span data-stu-id="185d5-200">**Notes**:</span></span>

- <span data-ttu-id="185d5-p116">Редактировать можно только пользовательские типы конфиденциальной информации. Изменить встроенный тип невозможно. Однако вы можете использовать PowerShell, чтобы экспортировать встроенные типы конфиденциальной информации, настроить их и импортировать в качестве пользовательских типов. Дополнительные сведения см. в статье [Настройка встроенных типов конфиденциальной информации](customize-a-built-in-sensitive-information-type.md).</span><span class="sxs-lookup"><span data-stu-id="185d5-p116">You can only modify custom sensitive information types; you can't modify built-in sensitive information types. But you can use PowerShell to export built-in custom sensitive information types, customize them, and import them as custom sensitive information types. For more information, see [Customize a built-in sensitive information type](customize-a-built-in-sensitive-information-type.md).</span></span>

- <span data-ttu-id="185d5-p117">Редактировать можно только пользовательские типы конфиденциальной информации, созданные в интерфейсе. Если вы использовали [процедуру PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) для импорта пакета правил с типом пользовательской конфиденциальной информации, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="185d5-p117">You can only modify custom sensitive information types that you created in the UI. If you used the [PowerShell procedure](create-a-custom-sensitive-information-type-in-scc-powershell.md) to import a custom sensitive information type rule package, you'll get an error.</span></span>

<span data-ttu-id="185d5-206">В Центре безопасности и соответствия требованиям откройте раздел **Классификации** \> **Типы конфиденциальной информации**, выберите нужный пользовательский тип и нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="185d5-206">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**, select the custom sensitive information type that you want to modify, and then click **Edit**.</span></span>

  ![Расположение элемента "Типы конфиденциальной информации" и кнопки "Изменить"](media/scc-cust-sens-info-type-edit.png)

<span data-ttu-id="185d5-p118">При этом доступны те же параметры, что и при создании типа конфиденциальной информации в Центре безопасности и соответствия требованиям. Дополнительные сведения см. в статье [Создание пользовательского типа конфиденциальной информации в Центре безопасности и соответствия требованиям](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="185d5-p118">The same options are available here as when you created the custom sensitive information type in the Security & Compliance Center. For more information, see [Create custom sensitive information types in the Security & Compliance Center](#create-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="185d5-210">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="185d5-210">How do you know this worked?</span></span>

<span data-ttu-id="185d5-211">Чтобы убедиться, что вы успешно изменили тип конфиденциальной информации, выполните любое из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="185d5-211">To verify that you've successfully modified a sensitive information type, do any of the following steps:</span></span>

  - <span data-ttu-id="185d5-212">Откройте раздел **Классификации** \> **Типы конфиденциальной информации** и проверьте параметры измененного типа.</span><span class="sxs-lookup"><span data-stu-id="185d5-212">Go to **Classifications** \> **Sensitive info types** to verify the properties of the modified custom sensitive information type.</span></span> 

  - <span data-ttu-id="185d5-p119">Протестируйте измененный тип конфиденциальной информации. Дополнительные сведения см. в статье [Тестирование пользовательских типов конфиденциальной информации в Центре безопасности и соответствия требованиям](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span><span class="sxs-lookup"><span data-stu-id="185d5-p119">Test the modified custom sensitive information type. For more information, see [Test custom sensitive information types in the Security & Compliance Center](#test-custom-sensitive-information-types-in-the-security--compliance-center).</span></span>

## <a name="remove-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="185d5-215">Удаление пользовательского типа конфиденциальной информации в Центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="185d5-215">Remove custom sensitive information types in the Security & Compliance Center</span></span> 

<span data-ttu-id="185d5-216">**Примечания**:</span><span class="sxs-lookup"><span data-stu-id="185d5-216">**Notes**:</span></span>

- <span data-ttu-id="185d5-217">Удалять можно только пользовательские типы конфиденциальной информации. Удалить встроенный тип невозможно.</span><span class="sxs-lookup"><span data-stu-id="185d5-217">You can only remove custom sensitive information types; you can't remove built-in sensitive information types.</span></span>

- <span data-ttu-id="185d5-218">Перед удалением пользовательского типа конфиденциальной информации убедитесь, что политики защиты от потери данных и правила потока обработки почты Exchange (также называемые правилами транспорта) не ссылаются на этот тип.</span><span class="sxs-lookup"><span data-stu-id="185d5-218">Before your remove a custom sensitive information type, verify that no DLP policies or Exchange mail flow rules (also known as transport rules) still reference the sensitive information type.</span></span>

1. <span data-ttu-id="185d5-219">В Центре безопасности и соответствия требованиям откройте раздел **Классификации** \> **Типы конфиденциальной информации** и выберите один или несколько пользовательских типов.</span><span class="sxs-lookup"><span data-stu-id="185d5-219">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types** and select one or more custom sensitive information types that you want to remove.</span></span>

2. <span data-ttu-id="185d5-220">В открывшемся всплывающем окне нажмите **Удалить** (или **Удалить типы конфиденциальной информации**, если выбрано несколько типов).</span><span class="sxs-lookup"><span data-stu-id="185d5-220">In the fly-out that opens, click **Delete** (or **Delete sensitive info types** if you selected more than one).</span></span>

    ![Расположение элемента "Типы конфиденциальной информации" и кнопки "Удалить"](media/scc-cust-sens-info-type-delete.png)

3. <span data-ttu-id="185d5-222">В появившемся предупреждающем сообщении нажмите **Да**.</span><span class="sxs-lookup"><span data-stu-id="185d5-222">In the warning message that appears, click **Yes**.</span></span>

### <a name="how-do-you-know-this-worked"></a><span data-ttu-id="185d5-223">Как убедиться, что все получилось?</span><span class="sxs-lookup"><span data-stu-id="185d5-223">How do you know this worked?</span></span>

<span data-ttu-id="185d5-224">Чтобы убедиться, что вы успешно удалили пользовательский тип конфиденциальной информации, откройте раздел **Классификации** \> **Типы конфиденциальной информации** и проверьте, исчез ли этот тип из списка.</span><span class="sxs-lookup"><span data-stu-id="185d5-224">To verify that you've successfully removed a custom sensitive information type, go to **Classifications** \> **Sensitive info types** to verify the custom sensitive information type is no longer listed.</span></span>

## <a name="test-custom-sensitive-information-types-in-the-security--compliance-center"></a><span data-ttu-id="185d5-225">Тестирование пользовательских типов конфиденциальной информации в Центре безопасности и соответствия требованиям</span><span class="sxs-lookup"><span data-stu-id="185d5-225">Test custom sensitive information types in the Security & Compliance Center</span></span>

1. <span data-ttu-id="185d5-226">В Центре безопасности и соответствия требованиям выберите **Классификации** \> **Типы конфиденциальной информации**.</span><span class="sxs-lookup"><span data-stu-id="185d5-226">In the Security & Compliance Center, go to **Classifications** \> **Sensitive info types**.</span></span>

2. <span data-ttu-id="185d5-p120">Выберите один или несколько типов конфиденциальной информации. В появившемся всплывающем окне нажмите **Тестировать тип** (или **Тестировать типы конфиденциальной информации**, если выбрано несколько типов).</span><span class="sxs-lookup"><span data-stu-id="185d5-p120">Select one or more custom sensitive information types to test. In the fly-out that opens, click **Test type** (or **Test sensitive info types** if you selected more than one).</span></span>

    ![Расположение элемента "Типы конфиденциальной информации" и кнопки "Тестировать тип"](media/scc-cust-sens-info-type-test.png)

3. <span data-ttu-id="185d5-230">На открывшейся странице **Добавление файла для тестирования** отправьте документ на проверку, перетащив файл или нажав кнопку **Обзор** и выбрав файл.</span><span class="sxs-lookup"><span data-stu-id="185d5-230">On the **Upload file to test** page that opens, upload a document to test by dragging and dropping a file or by clicking **Browse** and selecting a file.</span></span>

    ![Страница "Добавление файла для тестирования"](media/scc-cust-sens-info-type-test-upload.png)

4. <span data-ttu-id="185d5-232">Нажмите кнопку **Тестировать**, чтобы проверить документ на совпадения с шаблоном.</span><span class="sxs-lookup"><span data-stu-id="185d5-232">Click the **Test** button to test the document for pattern matches in the file.</span></span>

5. <span data-ttu-id="185d5-233">На странице **Результаты проверки соответствия** нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="185d5-233">On the **Match results** page, click **Finish**.</span></span>

    ![Результаты проверки соответствия](media/scc-cust-sens-info-type-test-results.png)