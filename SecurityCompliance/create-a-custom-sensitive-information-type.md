---
title: Создание пользовательского типа конфиденциальных данных
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 10/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 82c382a5-b6db-44fd-995d-b333b3c7fc30
description: Если вам необходимо обнаруживать и защищать конфиденциальные сведения другого типа, например идентификаторы сотрудников, для которых в вашей организации используется особый формат, вы можете создать пользовательский тип конфиденциальных данных. Для определения типа конфиденциальных данных используется XML-файл, который называется пакетом правил. В этой статье рассказывается, как создать XML-файл, в котором вы можете определить собственный пользовательский тип конфиденциальных данных. Для этого вы должны уметь создавать регулярные выражения.
ms.openlocfilehash: 56683dd8ceac286f79084d2c2f19f48f5849a02f
ms.sourcegitcommit: 4be502d1fc6cbaef4c72d599758d51efe3a173c9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/06/2018
ms.locfileid: "23849432"
---
# <a name="create-a-custom-sensitive-information-type"></a><span data-ttu-id="60933-106">Создание пользовательского типа конфиденциальных данных</span><span class="sxs-lookup"><span data-stu-id="60933-106">Create a custom sensitive information type</span></span>

<span data-ttu-id="60933-p102">В системе защиты от потери данных Office 365 имеется много [типов конфиденциальных данных](what-the-sensitive-information-types-look-for.md), которые вы можете использовать в своих политиках защиты от потери данных. С помощью встроенных типов можно обнаруживать и защищать номера кредитных карт, банковских счетов, паспортов и многие другие конфиденциальные сведения.</span><span class="sxs-lookup"><span data-stu-id="60933-p102">Data loss prevention (DLP) in Office 365 includes many [sensitive information types](what-the-sensitive-information-types-look-for.md) that are ready for you to use in your DLP policies. These built-in types can help identify and protect credit card numbers, bank account numbers, passport numbers, and more.</span></span> 
  
<span data-ttu-id="60933-p103">Если вам необходимо обнаруживать и защищать конфиденциальные сведения другого типа, например идентификаторы сотрудников, для которых в вашей организации используется особый формат, вы можете создать пользовательский тип конфиденциальных данных. Для определения типа конфиденциальных данных используется XML-файл, который называется пакетом правил.</span><span class="sxs-lookup"><span data-stu-id="60933-p103">But if you need to identify and protect a different type of sensitive information - for example, an employee ID that uses a format specific to your organization - you can create a custom sensitive information type. A sensitive information type is defined in an XML file called a rule package.</span></span>
  
<span data-ttu-id="60933-p104">В этой статье рассказывается, как создать XML-файл, в котором вы можете определить собственный пользовательский тип конфиденциальных данных. Для этого вы должны уметь создавать регулярные выражения. В качестве примера здесь описан процесс создания пользовательского типа конфиденциальных данных, с помощью которого можно обнаруживать идентификаторы сотрудников. Вы можете использовать этот пример XML-файла в качестве основы для собственного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="60933-p104">This topic shows you how to create an XML file that defines your own custom sensitive information type. You need to know how to create a regular expression. As an example, this topic creates a custom sensitive information type that identifies an employee ID. You can use this example XML as a starting point for your own XML file.</span></span>
  
<span data-ttu-id="60933-p105">Создав XML-документ правильного формата, вы можете отправить его в Office 365 с помощью PowerShell. Затем вы сможете использовать этот пользовательский тип конфиденциальных данных в своих политиках защиты от потери данных и проверить, обнаруживает ли система конфиденциальные данные так, как вы задумали.</span><span class="sxs-lookup"><span data-stu-id="60933-p105">After you've created a well-formed XML file, you can upload it to Office 365 by using PowerShell. Then you're ready to use your custom sensitive information type in your DLP policies and test that it's detecting the sensitive information as you intended.</span></span>

## <a name="important-disclaimer"></a><span data-ttu-id="60933-117">Отказ от ответственности</span><span class="sxs-lookup"><span data-stu-id="60933-117">Important disclaimer</span></span>

<span data-ttu-id="60933-p106">В связи с разнообразием сред клиентов и требований к совпадению содержимого служба поддержки Майкрософт не может помочь в определении совпадений содержимого, например определении пользовательских классов или шаблонов регулярных выражений (RegEx). В вопросах разработки, тестирования и отладки совпадений содержимого пользователям Office 365 придется рассчитывать только на внутренние ИТ-ресурсы. Кроме того, можно использовать внешние консультационные ресурсы, такие как Консультационные службы Майкрософт (MCS). Специалисты службы поддержки могут в некоторой степени помочь настроить функцию, но они не гарантируют, что разработка в области совпадений содержимого будет соответствовать требованиям или обязательствам клиента. Примером такой возможной поддержки может служить предоставление шаблона регулярного выражения во время тестирования. В службе поддержки также могут помочь устранить неполадки в уже имеющемся шаблоне, который не срабатывает должным образом, на одном конкретном примере сравнения содержимого.</span><span class="sxs-lookup"><span data-stu-id="60933-p106">Due to the variances in customer environments and content match requirements, Microsoft Support cannot assist in providing custom content-matching definitions – e.g. defining custom classifications or regular expression patterns (“RegEx”). For custom content-matching development, testing, and debugging, Office 365 customers will need to rely upon internal IT resources, or use an external consulting resource such as Microsoft Consulting Services (MCS).  Support engineers can provide limited support for the feature, but cannot provide assurances that any custom content-matching development will fulfill the customer’s requirements or obligations.  As an example of the type of support which can be provided, sample regular expression patterns may be provided for testing purposes. Or support can assist with troubleshooting an existing RegEx pattern which is not triggering as expected with a single specific content example.</span></span>

 <span data-ttu-id="60933-123">Дополнительные сведения о модуле RegEx в .NET, используемом для обработки текста, см. в документации по [регулярным выражениям в .NET](https://docs.microsoft.com/ru-RU/dotnet/standard/base-types/regular-expressions).</span><span class="sxs-lookup"><span data-stu-id="60933-123">For additional information on the .NET regex engine that's used for processing the text, see the documentaiton on [Regular Expressions in .NET](https://docs.microsoft.com/ru-RU/dotnet/standard/base-types/regular-expressions).</span></span>
    
## <a name="sample-xml-of-a-rule-package"></a><span data-ttu-id="60933-124">Пример XML-файла пакета правил</span><span class="sxs-lookup"><span data-stu-id="60933-124">Sample XML of a rule package</span></span>

<span data-ttu-id="60933-p107">Вот пример XML-файла пакета правил, который мы создадим в этой статье. Его элементы и атрибуты описаны в разделах ниже.</span><span class="sxs-lookup"><span data-stu-id="60933-p107">Here's the sample XML of the rule package that we'll create in this topic. Elements and attributes are explained in the sections below.</span></span>
  
```
<?xml version="1.0" encoding="UTF-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
<RulePack id="DAD86A92-AB18-43BB-AB35-96F7C594ADAA">
    <Version build="0" major="1" minor="0" revision="0"/>
    <Publisher id="619DD8C3-7B80-4998-A312-4DF0402BAC04"/>
    <Details defaultLangCode="en-us">
        <LocalizedDetails langcode="en-us">
            <PublisherName>Contoso</PublisherName>
            <Name>Employee ID Custom Rule Pack</Name>
            <Description>
            This rule package contains the custom Employee ID entity.
            </Description>
        </LocalizedDetails>
    </Details>
</RulePack>
<Rules>
<!-- Employee ID -->
    <Entity id="E1CC861E-3FE9-4A58-82DF-4BD259EAB378" patternsProximity="300" recommendedConfidence="70">
        <Pattern confidenceLevel="60">
            <IdMatch idRef="Regex_employee_id"/>
        </Pattern>
        <Pattern confidenceLevel="70">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
        </Pattern>
        <Pattern confidenceLevel="80">
            <IdMatch idRef="Regex_employee_id"/>
            <Match idRef="Func_us_date"/>
            <Any minMatches="1">
                <Match idRef="Keyword_badge" minCount="2"/>
                <Match idRef="Keyword_employee"/>
            </Any>
            <Any minMatches="0" maxMatches="0">
                <Match idRef="Keyword_false_positives_local"/>
                <Match idRef="Keyword_false_positives_intl"/>
            </Any>
        </Pattern>
    </Entity>
    <Regex id="Regex_employee_id">(\s)(\d{9})(\s)</Regex>
    <Keyword id="Keyword_employee">
        <Group matchStyle="word">
            <Term>Identification</Term>
            <Term>Contoso Employee</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_badge">
        <Group matchStyle="string">
            <Term>card</Term>
            <Term>badge</Term>
            <Term caseSensitive="true">ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_local">
        <Group matchStyle="word">
            <Term>credit card</Term>
            <Term>national ID</Term>
        </Group>
    </Keyword>
    <Keyword id="Keyword_false_positives_intl">
        <Group matchStyle="word">
            <Term>identity card</Term>
            <Term>national ID</Term>
            <Term>EU debit card</Term>
        </Group>
    </Keyword>
    <LocalizedStrings>
        <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB378">
            <Name default="true" langcode="en-us">Employee ID</Name>
            <Description default="true" langcode="en-us">
            A custom classification for detecting Employee IDs.
            </Description>
            <Name default="true" langcode="de-de">Name for German locale</Name>
            <Description default="true" langcode="de-de">
            Description for German locale.
            </Description>
        </Resource>
    </LocalizedStrings>
</Rules>
</RulePackage>

```

## <a name="what-are-your-key-requirements-rule-entity-pattern-elements"></a><span data-ttu-id="60933-p108">Каковы ваши основные требования? [Элементы Rule, Entity, Pattern]</span><span class="sxs-lookup"><span data-stu-id="60933-p108">What are your key requirements? [Rule, Entity, Pattern elements]</span></span>

<span data-ttu-id="60933-129">Прежде чем приступать к работе, желательно разобраться в базовой структуре схемы XML правила и понять, как с помощью этой структуры определять собственные типы конфиденциальных данных для обнаружения необходимого контента.</span><span class="sxs-lookup"><span data-stu-id="60933-129">Before you get started, it's helpful to understand the basic structure of the XML schema for a rule, and how you can use this structure to define your custom sensitive information type so that it will identify the right content.</span></span>
  
<span data-ttu-id="60933-p109">Правило определяет один или несколько объектов (типов конфиденциальных данных), а каждый объект определяет один или несколько шаблонов. Шаблон — это то, что ищет система защиты от потери данных, когда оценивает контент, например почту или документы.</span><span class="sxs-lookup"><span data-stu-id="60933-p109">A rule defines one or more entities (sensitive information types), and each entity defines one or more patterns. A pattern is what DLP looks for when it evaluates content such as email and documents.</span></span>
  
<span data-ttu-id="60933-p110">(Замечание по терминологии: если вы знакомы с политиками защиты от потери данных, вы знаете, что политика содержит одно или несколько правил, которые состоят из условий и действий. В этой статье в разметке XML используется правило для обозначения шаблонов, которые определяют объект, также называемый типом конфиденциальных данных. Таким образом, когда вы видите правило в данной статье, имейте в виду объект или тип конфиденциальных данных, а не условия и действия.)</span><span class="sxs-lookup"><span data-stu-id="60933-p110">(A quick note on terminology - if you're familiar with DLP policies, you know that a policy contains one or more rules comprised of conditions and actions. However, in this topic, the XML markup uses rule to mean the patterns that define an entity, also known as a sensitive information type. So in this topic, when you see rule, think entity or sensitive information type, not conditions and actions.)</span></span>
  
### <a name="simplest-scenario-entity-with-one-pattern"></a><span data-ttu-id="60933-135">Простейший сценарий: объект с одним шаблоном</span><span class="sxs-lookup"><span data-stu-id="60933-135">Simplest scenario: entity with one pattern</span></span>

<span data-ttu-id="60933-p111">Вот простейший сценарий. Вам необходимо, чтобы политика защиты от потери данных обнаруживала контент, содержащий идентификаторы сотрудников вашей организации, которые имеют формат девятизначного числа. Таким образом, шаблон ссылается на регулярное выражение, содержащееся в правиле, которое обнаруживает девятизначные числа. Любой контент, содержащий девятизначные числа, соответствует шаблону.</span><span class="sxs-lookup"><span data-stu-id="60933-p111">Here's the simplest scenario. You want your DLP policy to identify content that contains your organization's employee ID, which is formatted as a nine-digit number. So the pattern refers to a regular expression contained in the rule that identifies nine-digit numbers. Any content containing a nine-digit number satisfies the pattern.</span></span>
  
![Схема объекта с одним шаблоном](media/4cc82dcf-068f-43ff-99b2-bac3892e9819.png)
  
<span data-ttu-id="60933-141">Из-за своей простоты этот шаблон может часто приводить к ложным срабатываниям, обнаруживая контент, который содержит любые девятизначные числа. Такие числа не всегда являются идентификаторами сотрудников.</span><span class="sxs-lookup"><span data-stu-id="60933-141">However, while simple, this pattern may identify many false positives by matching content that contains any nine-digit number that is not necessarily an employee ID.</span></span>
  
### <a name="more-common-scenario-entity-with-multiple-patterns"></a><span data-ttu-id="60933-142">Более распространенный сценарий: объект с несколькими шаблонами</span><span class="sxs-lookup"><span data-stu-id="60933-142">More common scenario: entity with multiple patterns</span></span>

<span data-ttu-id="60933-143">По этой причине для определения объекта чаще используют несколько шаблонов, и эти шаблоны обнаруживают подтверждающие признаки (например, ключевые слова или даты) в дополнение к объекту (например, девятизначному номеру).</span><span class="sxs-lookup"><span data-stu-id="60933-143">For this reason, it's more common to define an entity by using more than one pattern, where the patterns identify supporting evidence (such as a keyword or date) in addition to the entity (such as a nine-digit number).</span></span>
  
<span data-ttu-id="60933-144">Например, чтобы повысить вероятность обнаружения контента, содержащего идентификатор сотрудника, вы можете определить еще один шаблон, который помимо девятизначного числа обнаруживает дату найма сотрудника на работу либо дату найма и какие-либо ключевые слова (например, "идентификатор сотрудника").</span><span class="sxs-lookup"><span data-stu-id="60933-144">For example, to increase the likelihood of identifying content that contains an employee ID, you can define another pattern that also identifies a hire date, and define yet another pattern that identifies both a hire date and a keyword (such as "employee ID"), in addition to the nine-digit number.</span></span>
  
![Схема объекта с несколькими шаблонами](media/c8dc2c9d-00c6-4ebc-889a-53b41a90024a.png)
  
<span data-ttu-id="60933-146">Обратите внимание на некоторые указанные ниже важные аспекты этой структуры.</span><span class="sxs-lookup"><span data-stu-id="60933-146">Note a couple of important aspects of this structure:</span></span>
  
- <span data-ttu-id="60933-p112">Шаблоны, для которых требуются дополнительные признаки, имеют более высокий уровень надежности. Это удобно, так как когда вы будете использовать этот тип конфиденциальных данных в политике защиты от потери данных, вы сможете применять действия с более строгими ограничениями (например, блокировать контент) c помощью одного соответствия с высоким уровнем надежности и действия с не очень строгими ограничениями (например, отправлять уведомления) для соответствий с низким уровнем надежности.</span><span class="sxs-lookup"><span data-stu-id="60933-p112">Patterns that require more evidence have a higher confidence level. This is useful because when you later use this sensitive information type in a DLP policy, you can use more restrictive actions (such as block content) with only the higher-confidence matches, and you can use less restrictive actions (such as send notification) with the lower-confidence matches.</span></span>
    
- <span data-ttu-id="60933-p113">Вспомогательные элементы IdMatch и Match ссылаются на регулярные выражения и ключевые слова, которые фактически являются дочерними элементами элемента Rule, а не элемента Pattern. Элемент Pattern ссылается на эти вспомогательные элементы, но они входят в состав элемента Rule. Это означает, что на одно определение вспомогательного элемента, например регулярного выражения или списка ключевых слов, может ссылаться несколько объектов и шаблонов.</span><span class="sxs-lookup"><span data-stu-id="60933-p113">The supporting IdMatch and Match elements reference regexes and keywords that are actually children of the Rule element, not the Pattern. These supporting elements are referenced by the Pattern but included in the Rule. This means that a single definition of a supporting element, like a regular expression or a keyword list, can be referenced by multiple entities and patterns.</span></span>
    
## <a name="what-entity-do-you-need-to-identify-entity-element-id-attribute"></a><span data-ttu-id="60933-p114">Какой объект вам необходимо определить? [Элемент Entity, атрибут id]</span><span class="sxs-lookup"><span data-stu-id="60933-p114">What entity do you need to identify? [Entity element, id attribute]</span></span>

<span data-ttu-id="60933-p115">Объект — это тип конфиденциальной информации, например номер кредитной карты, имеющий правильно определенный шаблон. У каждого объекта имеется уникальный GUID, используемый в качестве идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="60933-p115">An entity is a sensitive information type, such as a credit card number, that has a well-defined pattern. Each entity has a unique GUID as its ID.</span></span>
  
### <a name="name-the-entity-and-generate-its-guid"></a><span data-ttu-id="60933-156">Присваивание объекту имени и создание GUID для него</span><span class="sxs-lookup"><span data-stu-id="60933-156">Name the entity and generate its GUID</span></span>

<span data-ttu-id="60933-p116">Добавьте элементы Rules и Entity. Затем добавьте комментарий, в котором указано имя вашего пользовательского объекта (в этом примере Employee ID). Позже вы добавите имя объекта в раздел локализованных строк, и это имя будет отображаться в пользовательском интерфейсе при создании политики защиты от потери данных.</span><span class="sxs-lookup"><span data-stu-id="60933-p116">Add the Rules and Entity elements. Then add a comment that contains the name of your custom entity - in this example, Employee ID. Later, you'll add the entity name to the localized strings section, and that name is what appears in the UI when you create a DLP policy.</span></span>
  
<span data-ttu-id="60933-p117">Затем создайте GUID для своего объекта. Существует несколько способов создания GUID, но вы можете без труда сделать это в PowerShell, введя [guid]::NewGuid(). Далее вы добавите GUID объекта в раздел локализованных строк.</span><span class="sxs-lookup"><span data-stu-id="60933-p117">Next, generate a GUID for your entity. There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing [guid]::NewGuid(). Later, you'll also add the entity GUID to the localized strings section.</span></span>
  
![Разметка XML с элементами Rules и Entity](media/c46c0209-0947-44e0-ac3a-8fd5209a81aa.png)
  
## <a name="what-pattern-do-you-want-to-match-pattern-element-idmatch-element-regex-element"></a><span data-ttu-id="60933-p118">Соответствие какому шаблону необходимо проверять? [Элемент Pattern, элемент IdMatch, элемент Regex]</span><span class="sxs-lookup"><span data-stu-id="60933-p118">What pattern do you want to match? [Pattern element, IdMatch element, Regex element]</span></span>

<span data-ttu-id="60933-p119">Шаблон содержит список того, для поиска чего следует использовать тип конфиденциальной информации. Он может включать регулярные выражения, ключевые слова и встроенные функции (которые предназначены для различных задач, например они могут выполнять регулярные выражения для поиска дат или адресов). Типы конфиденциальных данных могут иметь несколько шаблонов с уникальными уровнями надежности.</span><span class="sxs-lookup"><span data-stu-id="60933-p119">The pattern contains the list of what the sensitive information type is looking for. This can include regexes, keywords, and built-in functions (which perform tasks like running regexes to find dates or addresses). Sensitive information types can have multiple patterns with unique confidences.</span></span>
  
<span data-ttu-id="60933-p120">Все указанные ниже шаблоны объединяет то, что они ссылаются на одно и то же регулярное выражение, которое выполняет поиск девятизначного числа (\d{9}) с пробелами в начале и в конце (\s) … (\s). На это регулярное выражение ссылается элемент IdMatch, и оно представляет собой общее требование для всех шаблонов, которые выполняют поиск объекта Employee ID. IdMatch — это идентификатор, соответствие которому пытается найти шаблон, например идентификатор сотрудника, номер кредитной карты или номер социального страхования. У элемента Pattern должен быть строго один элемент IdMatch.</span><span class="sxs-lookup"><span data-stu-id="60933-p120">What all of the below patterns have in common is that they all reference the same regular expression, which looks for a nine-digit number (\d{9}) surrounded by white space (\s) … (\s). This regular expression is referenced by the IdMatch element and is the common requirement for all patterns that look for the Employee ID entity. IdMatch is the identifier that the pattern is to trying to match, such as Employee ID or credit card number or social security number. A Pattern element must have exactly one IdMatch element.</span></span>
  
![Разметка XML c несколькими элементами Pattern, которые ссылаются на один элемент Regex](media/8f3f497b-3b8b-4bad-9c6a-d9abf0520854.png)
  
<span data-ttu-id="60933-p121">При выполнении условия шаблон возвращает значения количества и уровня надежности, которые вы можете использовать в условиях в своей политике защиты от потери данных DLP. Когда вы добавляете условие для обнаружения типа конфиденциальных данных в политику защиты от потери данных, вы можете изменить значения количества и уровня надежности, как показано здесь. Понятие уровня надежности (также называемого точностью совпадения) мы объясним далее в этой статье.</span><span class="sxs-lookup"><span data-stu-id="60933-p121">When satisfied, a pattern returns a count and confidence level, which you can use in the conditions in your DLP policy. When you add a condition for detecting a sensitive information type to a DLP policy, you can edit the count and confidence level as shown here. Confidence level (also called match accuracy) is explained later in this topic.</span></span>
  
![Пример параметров количества и точности совпадения](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
<span data-ttu-id="60933-p122">Составляя регулярное выражение, вы должны иметь в виду, что имеется ряд потенциальных проблем, о которых вам следует знать. Например, если вы напишете и отправите регулярное выражение, которое обнаруживает слишком большое количество контента, это может ухудшить производительность. Дополнительные сведения об этих потенциальных проблемах см. в разделе [Проблемы, которые могут возникнуть при проверке](#potential-validation-issues-to-be-aware-of) ниже.</span><span class="sxs-lookup"><span data-stu-id="60933-p122">When you create your regular expression, keep in mind that there are potential issues to be aware of. For example, if you write and upload a regex that identifies too much content, this can impact performance. To learn more about these potential issues, see the later section [Potential validation issues to be aware of](#potential-validation-issues-to-be-aware-of).</span></span>
  
## <a name="do-you-want-to-require-additional-evidence-match-element-mincount-attribute"></a><span data-ttu-id="60933-p123">Необходимо ли вам требовать дополнительные признаки? [Элемент Match, атрибут minCount]</span><span class="sxs-lookup"><span data-stu-id="60933-p123">Do you want to require additional evidence? [Match element, minCount attribute]</span></span>

<span data-ttu-id="60933-184">Помимо элемента IdMatch в шаблоне можно использовать элемент Match, чтобы требовать дополнительные подтверждающие признаки, например ключевое слово, регулярное выражение, дату или адрес.</span><span class="sxs-lookup"><span data-stu-id="60933-184">In addition to the IdMatch, a pattern can use the Match element to require additional supporting evidence, such as a keyword, regex, date, or address.</span></span>
  
<span data-ttu-id="60933-p124">Элемент Pattern может содержать несколько элементов Match. Их можно включить непосредственно в элемент Pattern либо объединить с помощью элемента Any. Для объединения элементов Match используется неявный оператор AND. Чтобы сработал шаблон, должны быть выполнены условия всех элементов Match. Чтобы использовать операторы AND или OR, можно применить элемент Any (более подробные сведения об этом см. в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="60933-p124">A Pattern can include multiple Match elements; they can be included directly in the Pattern element or combined by using the Any element. Match elements are joined by an implicit AND operator; all Match elements must be satisfied for the pattern to be matched. You can use the Any element to introduce AND or OR operators (more on that in a later section).</span></span>
  
<span data-ttu-id="60933-p125">С помощью необязательного атрибута minCount вы можете указать количество экземпляров соответствия, которые необходимо найти для каждого элемента Match. Например, вы можете указать, что шаблон срабатывает, только если найдено не менее двух ключевых слов из списка ключевых слов.</span><span class="sxs-lookup"><span data-stu-id="60933-p125">You can use the optional minCount attribute to specify how many instances of a match need to be found for each of the Match elements. For example, you can specify that a pattern is satisfied only when at least two keywords from a keyword list are found.</span></span>
  
![Разметка XML, в которой используется элемент Match с атрибутом minOccurs](media/607f6b5e-2c7d-43a5-a131-a649f122e15a.png)
  
### <a name="keywords-keyword-group-and-term-elements-matchstyle-and-casesensitive-attributes"></a><span data-ttu-id="60933-191">Ключевые слова [элементы Keyword, Group и Term, атрибуты matchStyle и caseSensitive]</span><span class="sxs-lookup"><span data-stu-id="60933-191">Keywords [Keyword, Group, and Term elements, matchStyle and caseSensitive attributes]</span></span>

<span data-ttu-id="60933-p126">Если вам необходимо обнаруживать конфиденциальные сведения, например идентификаторы сотрудников, то вам, скорее всего, потребуется использовать ключевые слова в качестве подтверждающих признаков. Например, помимо поиска девятизначного числа вам может потребоваться искать слова "карта", "эмблема" или "идентификатор". Для этого используйте элемент Keyword. У элемента Keyword есть атрибут id, на который могут ссылаться несколько элементов Match в нескольких шаблонах или объектах.</span><span class="sxs-lookup"><span data-stu-id="60933-p126">When you identify sensitive information, like an employee ID, you often want to require keywords as corroborative evidence. For example, in addition to matching a nine-digit number, you may want to look for words like "card", "badge", or "ID". To do this, you use the Keyword element. The Keyword element has an id attribute that can be referenced by multiple Match elements in multiple patterns or entities.</span></span>
  
<span data-ttu-id="60933-p127">Ключевые слова добавляют в виде списка элементов Term в элементе Group. У элемента Group есть атрибут matchStyle, который может принимать два указанных ниже значения.</span><span class="sxs-lookup"><span data-stu-id="60933-p127">Keywords are included as a list of Term elements in a Group element. The Group element has a matchStyle attribute with two possible values:</span></span>
  
- <span data-ttu-id="60933-p128">**matchStyle="word"**. Соответствие word позволяет обнаруживать целые слова с пробелами или другими разделителями слева и справа. Вам всегда следует использовать соответствие word кроме случаев, когда необходимо находить соответствия частям слов или словам в азиатских языках.</span><span class="sxs-lookup"><span data-stu-id="60933-p128">**matchStyle="word"** Word match identifies whole words surrounded by white space or other delimiters. You should always use word unless you need to match parts of words or match words in Asian languages.</span></span> 
    
- <span data-ttu-id="60933-p129">**matchStyle="string"** Соответствие string позволяет обнаруживать строки независимо от того, какие символы расположены слева и справа от них. Например, строке "кон" будут соответствовать выражения "консул" и "закон". Используйте соответствие string, только если вам необходимо находить соответствия словам на азиатских языках либо если ключевое слово может быть в составе других строк.</span><span class="sxs-lookup"><span data-stu-id="60933-p129">**matchStyle="string"** String match identifies strings no matter what they're surrounded by. For example, "id" will match "bid" and "idea". Use string only when you need to match Asian words or if your keyword may be included as part of other strings.</span></span> 
    
<span data-ttu-id="60933-203">И, наконец, с помощью атрибута caseSensitive элемента Term вы можете указать, что контент должен точно соответствовать ключевому слову с учетом регистра символов.</span><span class="sxs-lookup"><span data-stu-id="60933-203">Finally, you can use the caseSensitive attribute of the Term element to specify that the content must match the keyword exactly, including lower- and upper-case letters.</span></span>
  
![Разметка XML с элементами Match, которые ссылаются на ключевые слова](media/e729ba27-dec6-46f4-9242-584c6c12fd85.png)
  
### <a name="regular-expressions-regex-element"></a><span data-ttu-id="60933-205">Регулярные выражения [элемент Regex]</span><span class="sxs-lookup"><span data-stu-id="60933-205">Regular expressions [Regex element]</span></span>

<span data-ttu-id="60933-p130">В этом примере в объекте идентификатора сотрудника уже используется элемент IdMatch для ссылки на регулярное выражение для шаблона — девятизначное число с пробелами слева и справа. Помимо этого, в шаблоне можно использовать элемент Match для ссылки на дополнительный элемент Regex, чтобы обнаруживать подтверждающие признаки, например пяти- или шестизначные числа в формате почтового индекса США.</span><span class="sxs-lookup"><span data-stu-id="60933-p130">In this example, the employee ID entity already uses the IdMatch element to reference a regex for the pattern - a nine-digit number surrounded by whitespace. In addition, a pattern can use a Match element to reference an additional Regex element to identify corroborative evidence, such as a five- or nine-digit number in the format of a US zip code.</span></span>
  
### <a name="additional-patterns-such-as-dates-or-addresses-built-in-functions"></a><span data-ttu-id="60933-208">Дополнительные шаблоны, например даты или адреса [встроенные функции]</span><span class="sxs-lookup"><span data-stu-id="60933-208">Additional patterns such as dates or addresses [built-in functions]</span></span>

<span data-ttu-id="60933-p131">Помимо встроенных типов конфиденциальных данных в системе защиты от потери данных имеются встроенные функции, которые могут обнаруживать подтверждающие признаки, например даты в формате США, даты в формате ЕС, даты окончания сроков действия или адреса в США. Система защиты от потери данных не поддерживает отправку пользовательских функций, но когда вы создаете пользовательский тип конфиденциальных данных, ваш объект может ссылаться на встроенные функции.</span><span class="sxs-lookup"><span data-stu-id="60933-p131">In addition to the built-in sensitive information types, DLP also includes built-in functions that can identify corroborative evidence such as a US date, EU date, expiration date, or US address. DLP does not support uploading your own custom functions, but when you create a custom sensitive information type, your entity can reference the built-in functions.</span></span>
  
<span data-ttu-id="60933-211">Например, на эмблеме с идентификатором сотрудника имеется дата найма сотрудника на работу, поэтому этот пользовательский объект может использовать встроенную функцию `Func_us_date`, чтобы обнаруживать дату в формате, обычно применяемом в США.</span><span class="sxs-lookup"><span data-stu-id="60933-211">For example, an employee ID badge has a hire date on it, so this custom entity can use the built-in function  `Func_us_date` to identify a date in the format commonly used in the US.</span></span> 
  
<span data-ttu-id="60933-212">Дополнительные сведения см. в статье [Сведения, для обнаружения которых используются функции защиты от потери данных](what-the-dlp-functions-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="60933-212">For more information, see [What the DLP functions look for](what-the-dlp-functions-look-for.md).</span></span>
  
![Разметка XML с элементом Match, который ссылается на встроенную функцию](media/dac6eae3-9c52-4537-b984-f9f127cc9c33.png)
  
## <a name="different-combinations-of-evidence-any-element-minmatches-and-maxmatches-attributes"></a><span data-ttu-id="60933-214">Различные сочетания признаков [элемент Any, атрибуты minMatches и maxMatches]</span><span class="sxs-lookup"><span data-stu-id="60933-214">Different combinations of evidence [Any element, minMatches and maxMatches attributes]</span></span>

<span data-ttu-id="60933-p132">В элементе Pattern все элементы IdMatch и Match соединены неявным оператором AND: чтобы сработал шаблон, необходимо, чтобы имели место все совпадения. Тем не менее вы можете создать более гибкую логику совпадений, группируя элементы Match с помощью элемента Any. Например, вы можете использовать элемент Any для соответствия всем, никаким или конкретному подмножеству его дочерних элементов Match.</span><span class="sxs-lookup"><span data-stu-id="60933-p132">In a Pattern element, all IdMatch and Match elements are joined by an implicit AND operator - all of the matches must be satisfied before the pattern can be satisfied. However, you can create more flexible matching logic by using the Any element to group Match elements. For example, you can use the Any element to match all, none, or an exact subset of its children Match elements.</span></span>
  
<span data-ttu-id="60933-p133">У элемента Any имеется необязательные атрибуты minMatches и maxMatches, с помощью которых вы можете указать, сколько дочерних элементов Match необходимо выполнить, чтобы сработал шаблон. Учтите, что эти атрибуты определяют количество элементов Match, которые необходимо выполнить, а не количество признаков, обнаруженных для соответствий. Чтобы определить минимальное количество экземпляров для определенного совпадения, например два ключевых слова из списка, используйте атрибут minCount для элемента Match (см. выше).</span><span class="sxs-lookup"><span data-stu-id="60933-p133">The Any element has optional minMatches and maxMatches attributes that you can use to define how many of the children Match elements must be satisfied before the pattern is matched. Note that these attributes define the number of Match elements that must be satisfied, not the number of instances of evidence found for the matches. To define a minimum number of instances for a specific match, such as two keywords from a list, use the minCount attribute for a Match element (see above).</span></span>
  
### <a name="match-at-least-one-child-match-element"></a><span data-ttu-id="60933-221">Совпадение для хотя бы одного дочернего элемента Match</span><span class="sxs-lookup"><span data-stu-id="60933-221">Match at least one child Match element</span></span>

<span data-ttu-id="60933-p134">Если необходимо, чтобы выполнялось только минимальное количество элементов Match, можно использовать атрибут minMatches. По сути, эти элементы Match соединены неявным оператором OR. Этот элемент Any выполняется при обнаружении даты в формате США или ключевого слова из любого списка.</span><span class="sxs-lookup"><span data-stu-id="60933-p134">If you want to require that only a minimum number of Match elements must be met, you can use the minMatches attribute. In effect, these Match elements are joined by an implicit OR operator. This Any element is satisfied if a US-formatted date or a keyword from either list is found.</span></span>
  
![Разметка XML, в которой используется элемент Any с атрибутом minMatches](media/385db1b1-571b-4a05-81b3-db28f5099c17.png)
  
### <a name="match-an-exact-subset-of-any-children-match-elements"></a><span data-ttu-id="60933-226">Точное соответствие подмножеству любых дочерних элементов Match</span><span class="sxs-lookup"><span data-stu-id="60933-226">Match an exact subset of any children Match elements</span></span>

<span data-ttu-id="60933-p135">Если необходимо, чтобы выполнялось строго определенное количество элементов Match, вы можете задать одинаковые значения для элементов minMatches и maxMatches. Этот элемент Any будет выполняться только при обнаружении строго одной даты или одного ключевого слова. При обнаружении нескольких дат или ключевых слов шаблон не сработает.</span><span class="sxs-lookup"><span data-stu-id="60933-p135">If you want to require that an exact number of Match elements must be met, you can set minMatches and maxMatches to the same value. This Any element is satisfied only if exactly one date or keyword is found - any more than that, and the pattern won't be matched.</span></span>
  
![Разметка XML, в которой используется элемент Any с атрибутами minMatches и maxMatches](media/97b10002-7781-42e8-ac5a-20ad8c5a887e.png)
  
### <a name="match-none-of-children-match-elements"></a><span data-ttu-id="60933-230">Несоответствие никаким дочерним элементам Match</span><span class="sxs-lookup"><span data-stu-id="60933-230">Match none of children Match elements</span></span>

<span data-ttu-id="60933-p136">Если необходимо, чтобы не выполнялся ни один определенный признак для шаблона, вы можете задать для элементов minMatches и maxMatches значение 0. Это может быть удобно, если у вас есть список ключевых слов либо другой признак, которые, скорее всего, приведут к ложному срабатыванию.</span><span class="sxs-lookup"><span data-stu-id="60933-p136">If you want to require the absence of specific evidence for a pattern to be satisfied, you can set both minMatches and maxMatches to 0. This can be useful if you have a keyword list or other evidence that are likely to indicate a false positive.</span></span>
  
<span data-ttu-id="60933-p137">Например, объект идентификатора сотрудника выполняет поиск ключевого слова "карта", так как это слово может быть связано с выражением "идентификационная карта". Тем не менее если слово "карта" появляется только во фразе "кредитная карта", то в этом контексте маловероятно, что оно будет означать "идентификационная карта". Поэтому вы можете добавить выражение "кредитная карта" в качестве ключевого слова в список терминов, для которых не должно быть совпадений, чтобы сработал шаблон.</span><span class="sxs-lookup"><span data-stu-id="60933-p137">For example, the employee ID entity looks for the keyword "card" because it might refer to an "ID card". However, if card appears only in the phrase "credit card", "card" in this content is unlikely to mean "ID card". So you can add "credit card" as a keyword to a list of terms that you want to exclude from satisfying the pattern.</span></span>
  
![Разметка XML, в которой атрибут maxMatches имеет значение 0](media/f81d44e5-3db8-48a8-8919-f483a386afdf.png)
  
## <a name="how-close-to-the-entity-must-the-other-evidence-be-patternsproximity-attribute"></a><span data-ttu-id="60933-p138">Насколько близко к объекту должен находиться другой признак? [Атрибут patternsProximity]</span><span class="sxs-lookup"><span data-stu-id="60933-p138">How close to the entity must the other evidence be? [patternsProximity attribute]</span></span>

<span data-ttu-id="60933-p139">Ваш тип конфиденциальных данных используется для поиска шаблона, который представляет идентификатор сотрудника, и в рамках этого шаблона также выполняется поиск подтверждающего признака, например ключевого слова "ID". Это логично, так как чем ближе этот признак, тем больше вероятность того, что шаблон окажется реальным идентификатором сотрудника. Вы можете указать, насколько близко должен находиться другой признак в шаблоне к объекту, используя обязательный атрибут patternsProximity элемента Entity.</span><span class="sxs-lookup"><span data-stu-id="60933-p139">Your sensitive information type is looking for a pattern that represents an employee ID, and as part of that pattern it's also looking for corroborative evidence like a keyword such as "ID". It makes sense that the closer together this evidence is, the more likely the pattern is to be an actual employee ID. You can determine how close other evidence in the pattern must be to the entity by using the required patternsProximity attribute of the Entity element.</span></span>
  
![Разметка XML с атрибутом patternsProximity](media/e97eb7dc-b897-4e11-9325-91c742d9839b.png)
  
<span data-ttu-id="60933-p140">Для каждого шаблона в объекте значение атрибута patternsProximity определяет расстояние (в количестве символов Юникод) от расположения элемента IdMatch для всех остальных элементов Matches, указанных для этого элемента Pattern. Интервал вероятности закрепляется расположением элемента IdMatch, при этом интервал простирается влево и вправо от этого элемента.</span><span class="sxs-lookup"><span data-stu-id="60933-p140">For each pattern in the entity, the patternsProximity attribute value defines the distance (in Unicode characters) from the IdMatch location for all other Matches specified for that Pattern. The proximity window is anchored by the IdMatch location, with the window extending to the left and right of the IdMatch.</span></span>
  
![Схема интервала вероятности](media/b593dfd1-5eef-4d79-8726-a28923f7c31e.png)
  
<span data-ttu-id="60933-p141">В примере ниже показано, как интервал вероятности влияет на соответствие шаблону, в котором для элемента IdMatch пользовательского объекта идентификатора сотрудника требуется хотя бы одно подтверждающее соответствие ключевому слову или дате. Срабатывает только соответствие ID1, так как для соответствий ID2 и ID3 не найдено подтверждающих признаков либо найдены частичные подтверждающие признаки в пределах интервала вероятности.</span><span class="sxs-lookup"><span data-stu-id="60933-p141">The example below illustrates how the proximity window affects the pattern matching where IdMatch element for the employee ID custom entity requires at least one corroborating match of keyword or date. Only ID1 matches because for ID2 and ID3, either no or only partial corroborating evidence is found within the proximity window.</span></span>
  
![Схема подтверждающего признака и интервала вероятности](media/dc68e38e-dfa1-45b8-b204-89c8ba121f96.png)
  
<span data-ttu-id="60933-p142">Обратите внимание, что в случае электронного письма тело сообщения и все вложения обрабатываются как отдельные элементы. Это означает, что интервал вероятности не распространяется за пределы каждого из этих элементов. В каждом элементе (вложении или теле) должен быть и элемент idMatch, и подтверждающий признак.</span><span class="sxs-lookup"><span data-stu-id="60933-p142">Note that for email, the message body and each attachment are treated as separate items. This means that the proximity window does not extend beyond the end of each of these items. For each item (attachment or body), both the idMatch and corroborative evidence needs to reside in that item.</span></span>
  
## <a name="what-are-the-right-confidence-levels-for-different-patterns-confidencelevel-attribute-recommendedconfidence-attribute"></a><span data-ttu-id="60933-p143">Каков должен быть уровень надежности для различных шаблонов? [Атрибуты confidenceLevel и recommendedConfidence]</span><span class="sxs-lookup"><span data-stu-id="60933-p143">What are the right confidence levels for different patterns? [confidenceLevel attribute, recommendedConfidence attribute]</span></span>

<span data-ttu-id="60933-p144">Чем больше признаков требуется для шаблона, тем выше уровень надежности обнаружения необходимого объекта (например, идентификатора сотрудника) при срабатывании шаблона. Например, уровень надежности шаблона, для которого требуется девятизначное число идентификатора, дата найма сотрудника на работу и ключевое слово в непосредственной близости, выше уровня надежности шаблона, для которого требуется только девятизначное число идентификатора.</span><span class="sxs-lookup"><span data-stu-id="60933-p144">The more evidence that a pattern requires, the more confidence you have that an actual entity (such as employee ID) has been identified when the pattern is matched. For example, you have more confidence in a pattern that requires a nine-digit ID number, hire date, and keyword in close proximity, than you do in a pattern that requires only a nine-digit ID number.</span></span>
  
<span data-ttu-id="60933-p145">Элемент Pattern имеет обязательный атрибут confidenceLevel. Можно считать значение атрибута confidenceLevel (целое число от 1 до 100) уникальным идентификатором для каждого шаблона в объекте: у шаблонов в объекте должны быть разные назначенные вами уровни надежности. Не нужно стараться точно выбирать целые значения, просто выберите числа, которые будут понятны группе, отвечающей за соответствие требованиям в вашей организации. После того как вы отправите свой пользовательский тип конфиденциальных данных и создадите политику защиты от потери данных, вы сможете ссылаться на эти уровни надежности в условиях создаваемых вами правил.</span><span class="sxs-lookup"><span data-stu-id="60933-p145">The Pattern element has a required confidenceLevel attribute. You can think of the value of confidenceLevel (an integer between 1 and 100) as a unique ID for each pattern in an entity - the patterns in an entity must have different confidence levels that you assign. The precise value of the integer doesn't matter - simply pick numbers that make sense to your compliance team. After you upload your custom sensitive information type and then create a DLP policy, you can reference these confidence levels in the conditions of the rules that you create.</span></span>
  
![Разметка XML, в которой используются элементы Pattern с различными значениями атрибута confidenceLevel](media/301e0ba1-2deb-4add-977b-f6e9e18fba8b.png)
  
<span data-ttu-id="60933-p146">Помимо атрибута confidenceLevel для каждого элемента Pattern у элемента Entity имеется атрибут recommendedConfidence. Атрибут рекомендуемого уровня надежности можно считать уровнем надежности, используемым по умолчанию для правила. Если в процессе создания правила для политики защиты от потери данных вы не укажете уровень надежности, который необходимо использовать для правила, это правило будет срабатывать на основании рекомендованного уровня надежности для объекта.</span><span class="sxs-lookup"><span data-stu-id="60933-p146">In addition to confidenceLevel for each Pattern, the Entity has a recommendedConfidence attribute. The recommended confidence attribute can be thought of as the default confidence level for the rule. When you create a rule in a DLP policy, if you don't specify a confidence level for the rule to use, that rule will match based on the recommended confidence level for the entity.</span></span>
  
## <a name="do-you-want-to-support-other-languages-in-the-ui-of-the-security-amp-compliance-center-localizedstrings-element"></a><span data-ttu-id="60933-p147">Вам необходима поддержка других языков в пользовательском интерфейсе Центра безопасности и соответствия требованиям? [Элемент LocalizedStrings]</span><span class="sxs-lookup"><span data-stu-id="60933-p147">Do you want to support other languages in the UI of the Security &amp; Compliance Center? [LocalizedStrings element]</span></span>

<span data-ttu-id="60933-p148">Если группа обеспечения соответствия требованиям вашей организации использует Центр безопасности и соответствия требованиям Office 365 для создания политик защиты от потери данных для различных языковых стандартов и различных языков, вы можете предоставить локализованные версии имени и описания вашего пользовательского типа конфиденциальных данных. Когда участники группы обеспечения соответствия требованиям будут использовать Office 365 на поддерживаемом вами языке, для них в пользовательском интерфейсе будет отображаться локализованное имя.</span><span class="sxs-lookup"><span data-stu-id="60933-p148">If your compliance team uses the Office 365 Security &amp; Compliance Center to create DLP policies in different locales and in different languages, you can provide localized versions of the name and description of your custom sensitive information type. When your compliance team uses Office 365 in a language that you support, they'll see the localized name in the UI.</span></span>
  
![Пример параметров количества и точности совпадения](media/11d0b51e-7c3f-4cc6-96d8-b29bcdae1aeb.png)
  
<span data-ttu-id="60933-p149">Элемент Rules должен содержать элемент LocalizedStrings, который содержит элемент Resource, ссылающийся на GUID вашего пользовательского объекта. В свою очередь, каждый элемент Resource содержит один или несколько элементов Name и Description, в каждом из которых с помощью атрибута langcode предоставляется локализованная строка для определенного языка.</span><span class="sxs-lookup"><span data-stu-id="60933-p149">The Rules element must contain a LocalizedStrings element, which contains a Resource element that references the GUID of your custom entity. In turn, each Resource element contains one or more Name and Description elements that each use the langcode attribute to provide a localized string for a specific language.</span></span>
  
![Разметка XML с содержимым элемента LocalizedStrings](media/a96fc34a-b93d-498f-8b92-285b16a7bbe6.png)
  
<span data-ttu-id="60933-p150">Обратите внимание, что локализованные строки определяют только способ отображения пользовательского типа конфиденциальных данных в пользовательском интерфейсе Центра безопасности и соответствия требованиям. Вам не удастся использовать локализованные строки для предоставления различных локализованных версий списка ключевых слов или регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="60933-p150">Note that you use localized strings only for how your custom sensitive information type appears in the UI of the Security &amp; Compliance Center. You can't use localized strings to provide different localized versions of a keyword list or regular expression.</span></span>
  
## <a name="other-rule-package-markup-rulepack-guid"></a><span data-ttu-id="60933-274">Еще одна разметка пакета правил [GUID RulePack]</span><span class="sxs-lookup"><span data-stu-id="60933-274">Other rule package markup [RulePack GUID]</span></span>

<span data-ttu-id="60933-p151">В начале каждого элемента RulePackage содержатся общие сведения, которые вам необходимо внести. Вы можете использовать показанную ниже разметку в качестве шаблона и заменить заполнители ". . ." собственной информацией.</span><span class="sxs-lookup"><span data-stu-id="60933-p151">Finally, the beginning of each RulePackage contains some general information that you need to fill in. You can use the following markup as a template and replace the ". . ." placeholders with your own info.</span></span>
  
<span data-ttu-id="60933-p152">Самое важное — создать GUID для элемента RulePackage. Ранее вы создали GUID для объекта; это второй GUID для элемента RulePackage. Создавать идентификаторы GUID можно несколькими способами, но проще всего это сделать в PowerShell, введя [guid]::NewGuid().</span><span class="sxs-lookup"><span data-stu-id="60933-p152">Most importantly, you'll need to generate a GUID for the RulePack. Above, you generated a GUID for the entity; this is a second GUID for the RulePack. There are several ways to generate GUIDs, but you can do it easily in PowerShell by typing [guid]::NewGuid().</span></span>
  
<span data-ttu-id="60933-p153">Элемент Version также важен. Когда вы в первый раз отправляете свой пакет правил, Office 365 запоминает номер версии. Если затем вы измените пакет правил и отправите его новую версию, не забудьте изменить номер версии. В противном случае Office 365 не сможет развернуть пакет правил.</span><span class="sxs-lookup"><span data-stu-id="60933-p153">The Version element is also important. When you upload your rule package for the first time, Office 365 notes the version number. Later, if you update the rule package and upload a new version, make sure to update the version number or Office 365 won't deploy the rule package.</span></span>
  
```
<?xml version="1.0" encoding="utf-16"?>
<RulePackage xmlns="http://schemas.microsoft.com/office/2011/mce">
  <RulePack id=". . .">
    <Version major="1" minor="0" build="0" revision="0" />
    <Publisher id=". . ." /> 
    <Details defaultLangCode=". . .">
      <LocalizedDetails langcode=" . . . ">
         <PublisherName>. . .</PublisherName>
         <Name>. . .</Name>
         <Description>. . .</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  
 <Rules>
    . . .
 </Rules>
</RulePackage>

```

<span data-ttu-id="60933-286">По завершении этих действий элемент RulePack должен выглядеть, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="60933-286">When complete, your RulePack element should look like this.</span></span>
  
![Разметка XML с элементом RulePack](media/fd0f31a7-c3ee-43cd-a71b-6a3813b21155.png)
  
## <a name="changes-for-exchange-online"></a><span data-ttu-id="60933-288">Изменения для Exchange Online</span><span class="sxs-lookup"><span data-stu-id="60933-288">Changes for Exchange Online</span></span>

<span data-ttu-id="60933-p154">Ранее вы, возможно, использовали PowerShell в Exchange Online для импорта своих пользовательских типов конфиденциальных данных для системы защиты от потери данных. Теперь ваши пользовательские типы конфиденциальных данных можно использовать и в Центре администрирования Exchange, и в Центре безопасности и соответствия требованиям. В рамках этого усовершенствования вам следует использовать Центр безопасности и соответствия требованиям для импорта своих пользовательских типов конфиденциальных данных: вам больше не удастся импортировать их из PowerShell в Exchange. Ваши пользовательские типы конфиденциальных данных будут работать, как и раньше. Тем не менее может потребоваться до одного часа на то чтобы пользовательские типы конфиденциальных данных в Центре безопасности и соответствия требованиям появились в Центре администрирования Exchange.</span><span class="sxs-lookup"><span data-stu-id="60933-p154">Previously, you might have used Exchange Online PowerShell to import your custom sensitive information types for DLP. Now your custom sensitive information types can be used in both the Exchange Admin Center and the Security &amp; Compliance Center. As part of this improvement, you should use Security &amp; Compliance Center PowerShell to import your custom sensitive information types - you can't import them from the Exchange PowerShell anymore. Your custom sensitive information types will continue to work just like before; however, it may take up to one hour for changes made to custom sensitive information types in the Security &amp; Compliance Center to appear in the Exchange Admin Center.</span></span>
  
<span data-ttu-id="60933-p155">Обратите внимание, что для отправки пакета правил в Центре безопасности и соответствия требованиям необходимо использовать командлет `DlpSensitiveInformationTypeRulePackage`. Ранее в Центре администрирования Exchange вы использовали командлет `ClassificationRuleCollection`.</span><span class="sxs-lookup"><span data-stu-id="60933-p155">Note that in the Security &amp; Compliance Center, you use the  `DlpSensitiveInformationTypeRulePackage` cmdlet to upload a rule package. Previously, in the Exchange Admin Center, you used the  `ClassificationRuleCollection` cmdlet.</span></span> 
  
## <a name="upload-your-rule-package"></a><span data-ttu-id="60933-295">Отправка пакета правил</span><span class="sxs-lookup"><span data-stu-id="60933-295">Upload your rule package</span></span>

<span data-ttu-id="60933-296">Чтобы отправить пакет правил, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="60933-296">To upload your rule package, do the following.</span></span>
  
1. <span data-ttu-id="60933-297">Сохраните правило в виде XML-файла с кодировкой Юникод.</span><span class="sxs-lookup"><span data-stu-id="60933-297">Save it as an .xml file with Unicode encoding.</span></span>
    
2. <span data-ttu-id="60933-298">[Подключитесь к Центру безопасности и соответствия требованиям Office 365 с помощью удаленного сеанса PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="60933-298">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)</span></span>
    
3. <span data-ttu-id="60933-299">В Центре безопасности и соответствия требованиям введите команду New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\путь\НовыйПакетПравил.xml" -Encoding Byte).</span><span class="sxs-lookup"><span data-stu-id="60933-299">In the Security &amp; Compliance Center PowerShell, type New-DlpSensitiveInformationTypeRulePackage -FileData (Get-Content -Path "C:\custompath\MyNewRulePack.xml" -Encoding Byte).</span></span>
    
    <span data-ttu-id="60933-p156">Обязательно используйте расположение файла, в котором фактически хранится ваш пакет правил. Путь C:\путь\ — это просто заполнитель.</span><span class="sxs-lookup"><span data-stu-id="60933-p156">Make sure that you use the file location where your rule pack is actually stored. C:\custompath\ is a placeholder.</span></span>
    
4. <span data-ttu-id="60933-302">Для подтверждения введите Y и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="60933-302">To confirm, type Y, and then press ENTER.</span></span>
    
5. <span data-ttu-id="60933-p157">Убедитесь, что ваш новый тип конфиденциальных данных отправлен. Для этого введите команду Get-DlpSensitiveInformationType, чтобы отобразить список всех типов конфиденциальных данных. Вы можете быстро отделить пользовательские типы конфиденциальных данных от встроенных, взглянув на столбец "Издатель". Отфильтруйте список для определенного типа конфиденциальных данных, выполнив команду Get-DlpSensitiveInformationType -Identity "имя типа конфиденциальных данных".</span><span class="sxs-lookup"><span data-stu-id="60933-p157">Verify that your new sensitive information type was uploaded by typing Get-DlpSensitiveInformationType to see a list of all sensitive types. You can quickly separate custom sensitive information types from those which come built in by looking at the Publisher column. You can filter the list to a specific sensitive information type by running Get-DlpSensitiveInformationType -Identity "name of sensitive information type".</span></span>
    
## <a name="potential-validation-issues-to-be-aware-of"></a><span data-ttu-id="60933-306">Проблемы, которые могут возникнуть при проверке</span><span class="sxs-lookup"><span data-stu-id="60933-306">Potential validation issues to be aware of</span></span>

<span data-ttu-id="60933-p158">Когда вы отправляете XML-файл пакета правил, система проверяет XML и ищет известные неправильные фрагменты и очевидные проблемы производительности. Ниже перечислен ряд известных проблем, возникающих при проверке и связанных с регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="60933-p158">When you upload your rule package XML file, the system validates the XML and checks for known bad patterns and obvious performance issues. Here are some known issues that the validation checks for — a regular expression:</span></span>
  
- <span data-ttu-id="60933-309">Выражение не должно начинаться или заканчиваться альтернатором |, который имеет универсальное соответствие, так как он считается пустым совпадением.</span><span class="sxs-lookup"><span data-stu-id="60933-309">Cannot begin or end with alternator "|", which matches everything because it's considered an empty match.</span></span>
    
    <span data-ttu-id="60933-310">Например, выражения "|a" или "b|" не пройдут проверку.</span><span class="sxs-lookup"><span data-stu-id="60933-310">For example, "|a" or "b|" will not pass validation.</span></span>
    
- <span data-ttu-id="60933-311">Выражение не должно начинаться или заканчиваться шаблоном ".{0,m}", у которого нет функциональной цели и который только снижает производительность.</span><span class="sxs-lookup"><span data-stu-id="60933-311">Cannot begin or end with a ".{0,m}" pattern, which has no functional purpose and only impairs performance.</span></span>
    
    <span data-ttu-id="60933-312">Например, выражение ".{0,50}ASDF" или "ASDF.{0,50}" не пройдет проверку.</span><span class="sxs-lookup"><span data-stu-id="60933-312">For example, ".{0,50}ASDF" or "ASDF.{0,50}" will not pass validation.</span></span>
    
- <span data-ttu-id="60933-313">Выражение не должно содержать фрагменты ".{0,m}" или ".{1,m}" в группах, и в нем не должно быть фрагментов ".\*" или ".+" в группах.</span><span class="sxs-lookup"><span data-stu-id="60933-313">Cannot have ".{0,m}" or ".{1,m}" in groups, and cannot have ".\*" or ".+" in groups.</span></span>
    
    <span data-ttu-id="60933-314">Например, выражение "(.{0,50000})" не пройдет проверку.</span><span class="sxs-lookup"><span data-stu-id="60933-314">For example, "(.{0,50000})" will not pass validation.</span></span>
    
- <span data-ttu-id="60933-315">Выражение не должно содержать знаки с повторителями "{0,m}" или "{1,m}" в группах.</span><span class="sxs-lookup"><span data-stu-id="60933-315">Cannot have any character with "{0,m}" or "{1,m}" repeaters in groups.</span></span>
    
    <span data-ttu-id="60933-316">Например, выражение "(a\*)" не пройдет проверку.</span><span class="sxs-lookup"><span data-stu-id="60933-316">For example, "(a\*)" will not pass validation.</span></span>
    
- <span data-ttu-id="60933-317">Выражение не должно начинаться с фрагмента ".{1,m}". Вместо него используйте выражение ".".</span><span class="sxs-lookup"><span data-stu-id="60933-317">Cannot begin or end with ".{1,m}"; instead, use just "."</span></span>
    
    <span data-ttu-id="60933-318">Например, выражение ".{1,m}asdf" не пройдет проверку. Вместо него используйте выражение ".asdf".</span><span class="sxs-lookup"><span data-stu-id="60933-318">For example, ".{1,m}asdf" will not pass validation; instead, use just ".asdf".</span></span>
    
- <span data-ttu-id="60933-319">В выражении не должно быть неограниченного повторителя (например, "\*" или "+") в группе.</span><span class="sxs-lookup"><span data-stu-id="60933-319">Cannot have an unbounded repeater (such as "\*" or "+") on a group.</span></span>
    
    <span data-ttu-id="60933-320">Например, выражения "(xx)\*" и "(xx)+" не пройдут проверку.</span><span class="sxs-lookup"><span data-stu-id="60933-320">For example, "(xx)\*" and "(xx)+" will not pass validation.</span></span>
    
<span data-ttu-id="60933-321">Если в пользовательском типе конфиденциальных данных имеется проблема, которая может снизить производительность, этот тип не будет отправлен, и, возможно, будет отображено одно из указанных ниже сообщений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="60933-321">If a custom sensitive information type contains an issue that may affect performance, it won't be uploaded and you may see one of these error messages:</span></span>
  
- <span data-ttu-id="60933-322">**Универсальные квантификаторы, соответствующие большему количеству контента, чем ожидалось (например, +, \*)**</span><span class="sxs-lookup"><span data-stu-id="60933-322">**Generic quantifiers which match more content than expected (e.g., '+', '\*')**</span></span>
    
- <span data-ttu-id="60933-323">**Окрестные утверждения**</span><span class="sxs-lookup"><span data-stu-id="60933-323">**Lookaround assertions**</span></span>
    
- <span data-ttu-id="60933-324">**Сочетание сложной группировки с общими квантификаторами**</span><span class="sxs-lookup"><span data-stu-id="60933-324">**Complex grouping in conjunction with general quantifiers**</span></span>
    
## <a name="recrawl-your-content-to-identify-the-sensitive-information"></a><span data-ttu-id="60933-325">Повторный обход контента для обнаружения конфиденциальных данных</span><span class="sxs-lookup"><span data-stu-id="60933-325">Recrawl your content to identify the sensitive information</span></span>

<span data-ttu-id="60933-p159">Система защиты от потери данных использует программу-обходчик поиска для обнаружения и классификации конфиденциальных данных в контенте сайта. Повторный обход контента на сайтах SharePoint Online и OneDrive для бизнеса выполняется автоматически при обновлении контента. Чтобы можно было обнаруживать конфиденциальные данные вашего нового пользовательского типа во всем существующем контенте, необходимо выполнить повторный обход этого контента.</span><span class="sxs-lookup"><span data-stu-id="60933-p159">DLP uses the search crawler to identify and classify sensitive information in site content. Content in SharePoint Online and OneDrive for Business sites is recrawled automatically whenever it's updated. But to identify your new custom type of sensitive information in all existing content, that content must be recrawled.</span></span>
  
<span data-ttu-id="60933-329">В Office 365 вам не удастся вручную запросить повторный обход всего клиента, но вы можете сделать это для семейства веб-сайтов, списка или библиотеки. См. статью [Ручной запрос обхода контента и переиндексации сайта, библиотеки или списка](https://support.office.com/article/9afa977d-39de-4321-b4ca-8c7c7e6d264e).</span><span class="sxs-lookup"><span data-stu-id="60933-329">In Office 365, you can't manually request a recrawl of an entire tenant, but you can do this for a site collection, list, or library - see [Manually request crawling and re-indexing of a site, a library or a list](https://support.office.com/article/9afa977d-39de-4321-b4ca-8c7c7e6d264e).</span></span>
  
## <a name="remove-a-custom-sensitive-information-type"></a><span data-ttu-id="60933-330">Удаление пользовательского типа конфиденциальных данных</span><span class="sxs-lookup"><span data-stu-id="60933-330">Remove a custom sensitive information type</span></span>

1. <span data-ttu-id="60933-331">[Подключитесь к Центру безопасности и соответствия требованиям Office 365 с помощью удаленного сеанса PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="60933-331">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)</span></span>
    
2. <span data-ttu-id="60933-332">В PowerShell в Центре безопасности и соответствия требованиям выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="60933-332">In the Security &amp; Compliance Center PowerShell, do one of the following:</span></span>
    
  - <span data-ttu-id="60933-333">Чтобы удалить весь пакет правил и все содержащиеся в нем объекты, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="60933-333">To remove an entire rule package and all of the entities that it contains</span></span>
    
    <span data-ttu-id="60933-334">Введите команду Remove-DlpSensitiveInformationTypeRulePackage "ИмяВашегоПакетаПравил". Для приведенного выше примера XML следует ввести Remove-DlpSensitiveInformationTypeRulePackage "Employee ID Custom Rule Pack".</span><span class="sxs-lookup"><span data-stu-id="60933-334">Type Remove-DlpSensitiveInformationTypeRulePackage "NameOfYourRulePack" - for the example XML above, you would type Remove-DlpSensitiveInformationTypeRulePackage "Employee ID Custom Rule Pack".</span></span>
    
    <span data-ttu-id="60933-335">Учтите следующее: чтобы идентифицировать ваш пакет правил, можно использовать элемент \<Name\> (для любого языка) в элементе \<Rule Pack\> или GUID атрибута id элемента RulePack.</span><span class="sxs-lookup"><span data-stu-id="60933-335">Note that to identify your rule package, you can use the \<Name\> element (for any language) in the \<Rule Pack\> element or the GUID of the id attribute of the RulePack element.</span></span>
    
  - <span data-ttu-id="60933-336">Чтобы удалить один объект из пакета правил, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="60933-336">To remove a single entity from a rule package</span></span>
    
    <span data-ttu-id="60933-p160">Отправьте новую версию пакета правил, в котором удален соответствующий объект, выполнив команду Set-DlpSensitiveInformationTypeRulePackage. Прежде чем удалять тип конфиденциальных данных, убедитесь, что на него больше не ссылается ни одна политика защиты от потери данных или правило транспорта.</span><span class="sxs-lookup"><span data-stu-id="60933-p160">You must upload a new version of your rulepack with that specific entity removed using Set-DlpSensitiveInformationTypeRulePackage. You'll need to make sure that no DLP policies or Exchange transport rules still reference the sensitive information type before removing it.</span></span>
    
3. <span data-ttu-id="60933-339">Для подтверждения введите Y и нажмите клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="60933-339">To confirm, type Y, and then press ENTER.</span></span>
    
4. <span data-ttu-id="60933-340">Убедитесь, что новое правило удалено, выполнив команду Get- DlpSensitiveInformationType. В отображенном списке не должно быть имени вашего типа конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="60933-340">Verify that your new rule was removed by typing Get- DlpSensitiveInformationType, which should no longer display the name of your sensitive information type.</span></span>
    
## <a name="reference-rule-package-xml-schema-definition"></a><span data-ttu-id="60933-341">Справка: определение схемы XML пакета правил</span><span class="sxs-lookup"><span data-stu-id="60933-341">Reference: Rule package XML schema definition</span></span>

<span data-ttu-id="60933-342">Вы можете скопировать эту разметку, сохранить ее в виде XSD-файла и использовать для проверки XML-файла пакета правил.</span><span class="sxs-lookup"><span data-stu-id="60933-342">You can copy this markup, save it as an XSD file, and use it to validate your rule package XML file.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<xs:schema xmlns:mce="http://schemas.microsoft.com/office/2011/mce"
           targetNamespace="http://schemas.microsoft.com/office/2011/mce" 
           xmlns:xs="http://www.w3.org/2001/XMLSchema"
           elementFormDefault="qualified"
           attributeFormDefault="unqualified"
           id="RulePackageSchema">
  <!-- Use include if this schema has the same target namespace as the schema being referenced, otherwise use import -->
  <xs:element name="RulePackage" type="mce:RulePackageType"/>
  <xs:simpleType name="LangType">
    <xs:union memberTypes="xs:language">
      <xs:simpleType>
        <xs:restriction base="xs:string">
          <xs:enumeration value=""/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="GuidType" final="#all">
    <xs:restriction base="xs:token">
      <xs:pattern value="[0-9a-fA-F]{8}\-([0-9a-fA-F]{4}\-){3}[0-9a-fA-F]{12}"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulePackageType">
    <xs:sequence>
      <xs:element name="RulePack" type="mce:RulePackType"/>
      <xs:element name="Rules" type="mce:RulesType">
        <xs:key name="UniqueRuleId">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueProcessorId">
          <xs:selector xpath="mce:Regex|mce:Keyword|mce:Fingerprint"></xs:selector>
          <xs:field xpath="@id"/>
        </xs:key>
        <xs:key name="UniqueResourceIdRef">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:key>        
        <xs:keyref name="ReferencedRuleMustExist" refer="mce:UniqueRuleId">
          <xs:selector xpath="mce:LocalizedStrings/mce:Resource"/>
          <xs:field xpath="@idRef"/>
        </xs:keyref>
        <xs:keyref name="RuleMustHaveResource" refer="mce:UniqueResourceIdRef">
          <xs:selector xpath="mce:Entity|mce:Affinity|mce:Version/mce:Entity|mce:Version/mce:Affinity"/>
          <xs:field xpath="@id"/>
        </xs:keyref>
      </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="RulePackType">
    <xs:sequence>
      <xs:element name="Version" type="mce:VersionType"/>
      <xs:element name="Publisher" type="mce:PublisherType"/>
      <xs:element name="Details" type="mce:DetailsType">
        <xs:key name="UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="mce:LocalizedDetails"/>
          <xs:field xpath="@langcode"/>
        </xs:key>
        <xs:keyref name="DefaultLangCodeMustExist" refer="mce:UniqueLangCodeInLocalizedDetails">
          <xs:selector xpath="."/>
          <xs:field xpath="@defaultLangCode"/>
        </xs:keyref>
      </xs:element>
      <xs:element name="Encryption" type="mce:EncryptionType" minOccurs="0" maxOccurs="1"/>
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="VersionType">
    <xs:attribute name="major" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="minor" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="build" type="xs:unsignedShort" use="required"/>
    <xs:attribute name="revision" type="xs:unsignedShort" use="required"/>
  </xs:complexType>
  <xs:complexType name="PublisherType">
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="LocalizedDetailsType">
    <xs:sequence>
      <xs:element name="PublisherName" type="mce:NameType"/>
      <xs:element name="Name" type="mce:RulePackNameType"/>
      <xs:element name="Description" type="mce:OptionalNameType"/>
    </xs:sequence>
    <xs:attribute name="langcode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="DetailsType">
    <xs:sequence>
      <xs:element name="LocalizedDetails" type="mce:LocalizedDetailsType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="defaultLangCode" type="mce:LangType" use="required"/>
  </xs:complexType>
  <xs:complexType name="EncryptionType">
    <xs:sequence>
      <xs:element name="Key" type="xs:normalizedString"/>
      <xs:element name="IV" type="xs:normalizedString"/>
    </xs:sequence>
  </xs:complexType>
  <xs:simpleType name="RulePackNameType">
    <xs:restriction base="xs:token">
      <xs:minLength value="1"/>
      <xs:maxLength value="64"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="NameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="1"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="OptionalNameType">
    <xs:restriction base="xs:normalizedString">
      <xs:minLength value="0"/>
      <xs:maxLength value="256"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="RestrictedTermType">
    <xs:restriction base="xs:string">
      <xs:minLength value="1"/>
      <xs:maxLength value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="RulesType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Entity" type="mce:EntityType"/>
        <xs:element name="Affinity" type="mce:AffinityType"/>
        <xs:element name="Version" type="mce:VersionedRuleType"/>
      </xs:choice>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Regex" type="mce:RegexType"/>
        <xs:element name="Keyword" type="mce:KeywordType"/>
        <xs:element name="Fingerprint" type="mce:FingerprintType"/>
        <xs:element name="ExtendedKeyword" type="mce:ExtendedKeywordType"/>
      </xs:choice>
      <xs:element name="LocalizedStrings" type="mce:LocalizedStringsType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="EntityType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedPatternType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="patternsProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="recommendedConfidence" type="mce:ProbabilityType"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="PatternType">
    <xs:sequence>
      <xs:element name="IdMatch" type="mce:IdMatchType"/>
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="AffinityType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
      <xs:element name="Version" type="mce:VersionedEvidenceType" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
    <xs:attribute name="id" type="mce:GuidType" use="required"/>
    <xs:attribute name="evidencesProximity" type="mce:ProximityType" use="required"/>
    <xs:attribute name="thresholdConfidenceLevel" type="mce:ProbabilityType" use="required"/>
    <xs:attribute name="workload" type="mce:WorkloadType"/>
  </xs:complexType>
  <xs:complexType name="EvidenceType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="confidenceLevel" type="mce:ProbabilityType" use="required"/>
  </xs:complexType>
  <xs:complexType name="IdMatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
  </xs:complexType>
  <xs:complexType name="MatchType">
    <xs:attribute name="idRef" type="xs:string" use="required"/>
    <xs:attribute name="minCount" type="xs:positiveInteger" use="optional"/>
    <xs:attribute name="uniqueResults" type="xs:boolean" use="optional"/>
  </xs:complexType>
  <xs:complexType name="AnyType">
    <xs:sequence>
      <xs:choice maxOccurs="unbounded">
        <xs:element name="Match" type="mce:MatchType"/>
        <xs:element name="Any" type="mce:AnyType"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="minMatches" type="xs:nonNegativeInteger" default="1"/>
    <xs:attribute name="maxMatches" type="xs:nonNegativeInteger" use="optional"/>
  </xs:complexType>
  <xs:simpleType name="ProximityType">
    <xs:union>
      <xs:simpleType>
        <xs:restriction base='xs:string'>
          <xs:enumeration value="unlimited"/>
        </xs:restriction>
      </xs:simpleType>
      <xs:simpleType>
        <xs:restriction base="xs:positiveInteger">
          <xs:minInclusive value="1"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:union>
  </xs:simpleType>
  <xs:simpleType name="ProbabilityType">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="1"/>
      <xs:maxInclusive value="100"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="WorkloadType">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Exchange"/>
      <xs:enumeration value="Outlook"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:simpleType name="EngineVersionType">
    <xs:restriction base="xs:token">
      <xs:pattern value="^\d{2}\.01?\.\d{3,4}\.\d{1,3}$"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="VersionedRuleType">
    <xs:choice maxOccurs="unbounded">
      <xs:element name="Entity" type="mce:EntityType"/>
      <xs:element name="Affinity" type="mce:AffinityType"/>
    </xs:choice>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedPatternType">
    <xs:sequence>
      <xs:element name="Pattern" type="mce:PatternType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:complexType name="VersionedEvidenceType">
    <xs:sequence>
      <xs:element name="Evidence" type="mce:EvidenceType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="minEngineVersion" type="mce:EngineVersionType" use="required" />
  </xs:complexType>
  <xs:simpleType name="FingerprintValueType">
    <xs:restriction base="xs:string">
      <xs:minLength value="2732"/>
      <xs:maxLength value="2732"/>
    </xs:restriction>
  </xs:simpleType>
  <xs:complexType name="FingerprintType">
    <xs:simpleContent>
      <xs:extension base="mce:FingerprintValueType">
        <xs:attribute name="id" type="xs:token" use="required"/>
        <xs:attribute name="threshold" type="mce:ProbabilityType" use="required"/>
        <xs:attribute name="shingleCount" type="xs:positiveInteger" use="required"/>
        <xs:attribute name="description" type="xs:string" use="optional"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="RegexType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="KeywordType">
    <xs:sequence>
      <xs:element name="Group" type="mce:GroupType" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:token" use="required"/>
  </xs:complexType>
  <xs:complexType name="GroupType">
    <xs:sequence>
      <xs:choice>
        <xs:element name="Term" type="mce:TermType" maxOccurs="unbounded"/>
      </xs:choice>
    </xs:sequence>
    <xs:attribute name="matchStyle" default="word">
      <xs:simpleType>
        <xs:restriction base="xs:NMTOKEN">
          <xs:enumeration value="word"/>
          <xs:enumeration value="string"/>
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  <xs:complexType name="TermType">
    <xs:simpleContent>
      <xs:extension base="mce:RestrictedTermType">
        <xs:attribute name="caseSensitive" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="ExtendedKeywordType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="id" type="xs:token" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="LocalizedStringsType">
    <xs:sequence>
      <xs:element name="Resource" type="mce:ResourceType" maxOccurs="unbounded">
      <xs:key name="UniqueLangCodeUsedInNamePerResource">
        <xs:selector xpath="mce:Name"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
      <xs:key name="UniqueLangCodeUsedInDescriptionPerResource">
        <xs:selector xpath="mce:Description"/>
        <xs:field xpath="@langcode"/>
      </xs:key>
    </xs:element>
    </xs:sequence>
  </xs:complexType>
  <xs:complexType name="ResourceType">
    <xs:sequence>
      <xs:element name="Name" type="mce:ResourceNameType" maxOccurs="unbounded"/>
      <xs:element name="Description" type="mce:DescriptionType" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
    <xs:attribute name="idRef" type="mce:GuidType" use="required"/>
  </xs:complexType>
  <xs:complexType name="ResourceNameType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
  <xs:complexType name="DescriptionType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="default" type="xs:boolean" default="false"/>
        <xs:attribute name="langcode" type="mce:LangType" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>
</xs:schema>

```

## <a name="more-information"></a><span data-ttu-id="60933-343">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="60933-343">More information</span></span>

- [<span data-ttu-id="60933-344">Обзор политик защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="60933-344">Overview of data loss prevention policies</span></span>](data-loss-prevention-policies.md)
    
- [<span data-ttu-id="60933-345">Что позволяют искать типы конфиденциальной информации</span><span class="sxs-lookup"><span data-stu-id="60933-345">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)
    
- [<span data-ttu-id="60933-346">Сведения, для обнаружения которых используются функции защиты от потери данных</span><span class="sxs-lookup"><span data-stu-id="60933-346">What the DLP functions look for</span></span>](what-the-dlp-functions-look-for.md)
    

